---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
marp: true
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---


# **Soaring Through the Future**

With Self-Packaged Linux Apps

<sub>Providing a Quick, Easy and Painless Experience</sub>

--- 
# **About The PkgForge Team**

---
# **About The Presenters**
![bg right:40% 80%](https://avatars.githubusercontent.com/u/84176052?v=4)
Speaker: Souhrud Reddy

About me: A linux enthusiast in my spare time

Also a package maintainer for Soar, for Pixelpulse2

My Website: https://sounddrill31.github.io

--- 
# **About The Presenters**
<!--![bg left:40% 80%](https://avatars.githubusercontent.com/u/84176052?v=4) -->
Speaker: Aditya

About me: 

TODO: Fill

My Website: 

--- 
# **Topics Covered**
- Why is any of this needed?
- soar and PkgForge
- A Brief Look at AppImages
- `.SBUILD`, soar's yaml based package listing format


--- 

# **Quick Overview**
In this presentation, we'll explore the Soar Package Manager, how to use it and how you can submit your own AppImages and binaries.  

This will not be a technical deep-dive, just a quick demonstration.

--- 

# **The Elephant in the Room: Why?**
New users want something that "just works" across any distro they install, be it Ubuntu, Debian, PopOS, Arch, or even Alpine Linux

<!-- You can use this to quickly install and run static apps on any linux distro -->

<!--This is comparable to Homebrew-->

<sub>(Image by SEO Galaxy at [Unsplash](https://unsplash.com/photos/a-woman-sitting-in-front-of-a-laptop-computer-dJpBpPUevSA))</sub>
<!--Fumbling with solutions is not a good look, neither are huge installs -->
<!-- Users load linux to escape bloat, not cause them -->

![bg left:40% 80%](https://images.unsplash.com/photo-1709718499883-7267d6ffae9c?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

---
# **Introduction to PkgForge**

---
# **What is soar?**

---
# **The Elephant in the Room: Why soar?**
"Why would I use soar over existing solutions?"
Soar doesn't attempt to replace your OS level package manager(like apt, dnf, etc)
This helps you load completely portable packages that are independent from your OS install!
<sub>Image from XKCD, Ch 927 "STANDARDS"</sub>
![bg right:40% 80%](https://imgs.xkcd.com/comics/standards.png)

---
# **How to use soar?**

```mermaid
graph LR
    A[Install soar] --> B[Install app] --> C[Run app]
```

---
# **Quick Live Demo! Using soar and Installing Apps**
Installing Guide: https://soar.qaidvoid.dev/installation#install-script
Directly Running Apps without installing beforehand: `soar run appname`

Installing Apps to System: `soar install appname`
- Running the installed app: `appname`

It's. That. Simple. 

---
# **Another Elephant in the Room: Why AppImages?**

- Why not just use Flatpak/Snaps and avoid all of this? 
Eg. Flatpak vs AppImage: 

<sub>Image from https://github.com/prusa3d/PrusaSlicer/issues/13653#issuecomment-2500109771</sub>
<!-- Give supporting screenshots and thoughts -->
---

![bg](assets/flatpakvsappimage.png)

---

When I spoke to Samuel about this, he said:
![left:120% 240%](assets/samuel-update.png)
![right:40% 240%](assets/samuel-on-ghostty.png)

---

```plantuml
@startuml
title Flatpak vs AppImage: Execution Flow

actor User
box "Flatpak" #LightBlue
participant "Flatpak Runtime" as FRuntime
participant "Sandbox" as FSandbox
participant "App (/app)" as FApp
participant "Runtime (/usr)" as FLibs
end box

box "AppImage" #LightSalmon
participant "AppImage File" as AFile
participant "Runtime" as ARuntime
participant "SquashFS Image" as AFS
participant "AppRun" as AAppRun
end box

participant "Host System" as Host

== Flatpak Execution ==
User -> FRuntime: Execute Flatpak app
FRuntime -> FSandbox: Create isolated environment
FSandbox -> FApp: Load application files
FSandbox -> FLibs: Load shared libraries
FApp -> FLibs: Request libraries
FApp -> Host: Limited access via portals

== AppImage Execution ==
User -> AFile: Execute file
AFile -> ARuntime: Start runtime
ARuntime -> AFS: Mount via FUSE
ARuntime -> AAppRun: Execute entrypoint
AAppRun -> Host: Run application

@enduml
```

---
# **Live Demo Time! Making a quick soar Package using SBUILD**

--- 
<!--# **Credits**

--- --->
--- 
## **This Presentation was made completely with MarkDown thanks to Marp!**

https://marp.app/

View the slides: https://sounddrill31.github.io/FOSSUnited-Slides-AppImages/
