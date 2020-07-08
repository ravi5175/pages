title: Developers Guide

<br>
<br>


### Packages Management
releax OS uses its own home grown package manager [sys-app](/sys/sys-app), which has capability to install apps from both source and binary format,  
sys-app reads recipies from **/usr/recipies/** to manager applications, [recipie](/sys/sys-app) recipie of any app is a directory containing a complete information about the app - its version, release, source url, build function, description, dependencies, patches, etc.
