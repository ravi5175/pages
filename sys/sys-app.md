title: sys-app
subtitle: releax OS package manager

<br>
<br>

### sys-app
sys-app is a releax OS package manager that is capable of performing both source and binary installations. sys-app can perform installation, uninstallation, describe, update, check, pack apps and also provide *hints* in case of command failure for easy debugging and fixing 


##### Commands:
- **Basic**
	- sys-app install _appname_ : to install applications
	- sys-app remove _appname_ : to uninstall application
	- sys-app info _appname_ : to print information of specified application
	- sys-app search _text_ : to search any app
	- sys-app refresh : to refresh repository
	- sys-appadd _appfile_ : to install app from app file

<br>

- **Update**
	- sys-app update : to update the complete system
	- sys-appupdate _appname_ : to update any specific app

<br>

- **check**
	- sys-app check _appname_ : to perfrom app checkup
	- sys-appcheckup checkup : to perfrom all apps checkup

<br>

- **Compilation**
	- sys-app compile _appname_ : to compile app from source
	- sys-appbuild : to compile app from recipie file

<br>

- **packing**
	- sys-apppack : to pack the application into installable releax os package


<br>
<br>

#### Recipies
releax os use recipie to manage database of applications present inside **/usr/recipies/**. Recipies of any app is a folder containing all informations of that app, patches, server files etc.

**recipie information file template**:

    # Description: 
    # URL: 
    # Maintainer: releax core team
    # Depends on: 
    # License: 

    name=
    version=
    release=1
    source=()

    build() {
        cd $name-$version

            ./configure \
                    --prefix=/usr

            make
            
            [ $check ] && make check
            make DESTDIR=$pkg install 
    }


<br>

sys-app read these files to build packages from source, and make binary packages inside **/var/cache/build/** , these packages are then installed with command ```sys-app install ```, 

**sys-app install**  skip the process of compilations and build time dependencies, and download the package from repository and install them. 

this method provide user the independence of installation a binary package from repo, or compile package from source if needed modifications

<br>

### Configurations
sys-app read configuration file from **/etc/sysconfig/app.conf**, the values can be modified or customized according to the needs

<br>

### Developers Area
sys-app is completely written in shell script (some part in c++), and source codes are avaliable on [Github](https://github.com/itsmanjeet/sys-app).
plus sys-app provide shell *API* that can be used in custom softwares or automated scipts
simple source the ```/lib/rsb/app.sh ``` file inside your script

<br>

###### Example

	#!/bin/sh

	# Example script to describe the use of sys-app API's
	# This script will list files inside a releax os package  /var/cache/build/acl-$version-$releax-x86_64.tar.xz
	# and write files list inside ./appfiles

	source /lib/rsb/app.sh

	appname="acl"

	repo_dir="/usr/recipies/"
	build_dir="/var/cache/build/"
	recipie_path=$(GetRecipiePath $appname)
	source $recipie_path/recipie

	ListPackFiles $appname "appfiles"