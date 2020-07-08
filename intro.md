title: Introduction to releax OS
subtitle: A Basic intro of interface and workflow


<br>
<br>


### Home Screen
releax OS uses a 2 [xfce]() panel system:

- Top panel : *for Menu, Status Indicator, Notification Area and logout menu*
- Bottom Panel : *for dock and extra plugins*

<br>

<img class="dimg" src="{{ url_for('static', filename='images/home.png')}}" width=800px>

<br>
<br>

#### Menu
[whisker-menu]() is the application menu of releax OS, which help you find your apps and games

<img class="dimg" src="{{ url_for('static', filename='images/menu.png')}}" width=500px>

<br>

#### Dock panel
[docklike-plugin]() in bottom panel provide fast access to your pinned apps, and active windows

<img class="dimg" src="{{ url_for('static', filename='images/dockpanel.png')}}" width=500px>

<br>

#### Fast Launcher
[xfce-appfinder]() is a program to find and launch installed applications on your system, and quickly execute commands  
press ``` alt-f2 ``` to activate fast launcher

<img class="dimg" src="{{ url_for('static', filename='images/launcher.png')}}" width=800px>

<br>

#### Drop down terminal
[xfce4-terminal]() is fast terminal to *speedify* your workflow, to access the drop down terminal press ```ctrl-alt-space```

<img class="dimg" src="{{ url_for('static', filename='images/drop-down-terminal.png')}}" width=800px>

<br>
<br>


### Multitasking
customizable [workspace]() and task switching for a fast workflow is necessary,

- ```ctrl-alt-<arrow-key>``` : *to switch between workspaces* by default releax OS provide a 4 workspace system, but can be modified
- ```alt-tab``` : *to switch between tasks*

<br>
<br>

---
## Package Managment
releax OS offer both commandline and graphical interface to manage both system and user applications

- **[sys-app](/sys/sys-app)** : is a releax OS homegrown package manager written completely in [shell script]() *some parts in c++ also* [Github link](https://github.com/itsmanjeet/sys-app)
- **[bazaar]()** : is a Frontend of *sys-app* to provide a graphical interface to easily manager applications [Github Link](https://github.com/itsmanjeet/Bazaar)
- **[flatpak]()** : is a linux universal package manager, *releax os is written from scratch, that why their is a very little applications in the repository, that's why flatpak is provided, so that you do not miss out you faviourate applications*

<br>

### Bazaar
releax OS app market, you can search your faviourate applications, install, uninstall and upgrade them with ease, with bazaar you need not to remember any of the [sys-app commands]()

<br>

<img class="dimg" src="{{ url_for('static', filename='images/appmarket.png')}}" width=800px>


<br>
<br>
