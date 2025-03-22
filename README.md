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
New users want something that "just works" across any distro they install, be it Ubuntu, Debian, PopOS, Arch, or even Alpine Linux

<!-- You can use this to quickly install and run static apps on any linux distro -->

<!--This is comparable to Homebrew-->

<sub>(Image by SEO Galaxy at [Unsplash](https://unsplash.com/photos/a-woman-sitting-in-front-of-a-laptop-computer-dJpBpPUevSA))</sub>
<!--Fumbling with solutions is not a good look, neither are huge installs -->
<!-- Users load linux to escape bloat, not cause them -->

![bg left:40% 80%](https://images.unsplash.com/photo-1709718499883-7267d6ffae9c?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

---

# **Why AppImages?**

Difference: | Snap and snapd | Flatpak and runtimes | AppImages |
| --- | --- | --- | --- |
| Developed by | Canonical | Community ✅ | Community ✅ | 
| Lock in |Tied to Snap Ecosystem | No Lock in | No Lock in |
| Dependencies | snapd and many more | Flatpak Runtimes | <sub>One App = One File</sub> |

---

<!-- Give supporting screenshots and thoughts -->

![bg](assets/flatpakvsappimage.png)

---
<sub>Previous Image from https://github.com/prusa3d/PrusaSlicer/issues/13653#issuecomment-2500109771</sub>

When I spoke to Samuel about this, he said:
![top-left width:45% top](assets/samuel-update.png)
![bottom-right width:45% top](assets/samuel-on-ghostty.png)



---
<!--# **Introduction to PkgForge**

--- -->
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
    style A fill:#f9d5e5,stroke:#333,stroke-width:2px
    style B fill:#eeeeee,stroke:#333,stroke-width:2px
    style C fill:#d5f9e5,stroke:#333,stroke-width:2px
    linkStyle 0 stroke:#ff9900,stroke-width:2px
    linkStyle 1 stroke:#ff9900,stroke-width:2px






```

---
# **Quick Live Demo! Using soar and Installing Apps**
Installing Guide: https://soar.qaidvoid.dev/installation#install-script
Directly Running Apps without installing beforehand: `soar run appname`

Installing Apps to System: `soar install appname`
- Running the installed app: `appname`

It's. That. Simple. 

---
# **Live Demo Time! Making a quick soar Package using SBUILD**

--- 
<!--# **Credits**

--- --->

## **This Presentation was made completely with MarkDown thanks to Marp!**

https://marp.app/

View the slides: https://sounddrill31.github.io/FOSSUnited-Slides-AppImages/
