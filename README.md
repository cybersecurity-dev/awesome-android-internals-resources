<div align="center">
    <p align="center">
        <a href="https://wikipedia.org/wiki/Android_(operating_system)">
          <img width="25%" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/Android.svg" />
        </a>
    </p>

```mermaid
architecture-beta
    group apps(cloud)[Applications]
    group framework(cloud)[Framework]
    group runtime(cloud)[Runtime and Native]
    group hal(cloud)[HAL]
    group kernel(cloud)[Linux Kernel]
    group hardware(cloud)[Hardware]

    service app(server)[Applications] in apps

    service api(server)[Java API Framework] in framework
    service system(server)[System Services] in framework

    service art(server)[ART] in runtime
    service native(server)[Native Libraries] in runtime

    service hals(server)[HAL Modules] in hal

    service binder(server)[Binder] in kernel
    service drivers(server)[Device Drivers] in kernel
    service memory(server)[Memory and Scheduler] in kernel

    service hw(server)[CPU GPU Devices] in hardware

    app:B --> T:api
    api:B --> T:system
    system:B --> T:art
    system:B --> T:hals
    art:B --> T:native
    hals:B --> T:drivers
    system:B --> T:binder
    native:B --> T:memory
    drivers:B --> T:hw
```

# **`Awesome`** Android Internals Resources [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
</div>

[![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)]()
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)]() 
[![Reddit](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)]()

<p align="center">
    <a href="https://github.com/cybersecurity-dev/"><img height="25" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/github.svg" alt="GitHub"></a>
    &nbsp;
    <a href="https://www.youtube.com/@CyberThreatDefense"><img height="25" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/youtube.svg" alt="YouTube"></a>
    &nbsp;
    <a href="https://cyberthreatdefence.com/my_awesome_lists"><img height="20" src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/blog.svg" alt="My Awesome Lists"></a>
    <img src="https://github.com/cybersecurity-dev/cybersecurity-dev/blob/main/assets/bar.gif">
</p>

```mermaid
block-beta
    columns 4

    block:USERSPACE:4
        A["Applications"]
        B["Framework"]
        C["ART"]
        D["Native"]
    end

    space:4

    block:KERNEL:4
        E["Process
Scheduler"]
        F["Memory
Management"]
        G["VFS /
Filesystems"]
        H["Network
Stack"]
        I["Binder
IPC"]
        J["SELinux /
LSM"]
        K["Power
Management"]
        L["Device
Drivers"]
    end

    space:4

    block:HW:4
        M["CPU"]
        N["RAM"]
        O["Storage"]
        P["Devices"]
    end
```

## 📖 Contents
- [My Other Awesome Lists](#my-other-awesome-lists)
- [Contributing](#contributing)
- [Contributors](#contributors)

##

### My Other Awesome Lists
You can access the my other awesome lists [here](https://cyberthreatdefence.com/my_awesome_lists)

### Contributing
[Contributions of any kind welcome, just follow the guidelines](contributing.md)!

### Contributors
[Thanks goes to these contributors](https://github.com/cybersecurity-dev/awesome-android-internals/graphs/contributors)!

### License
[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0)

[🔼 Back to top](#awesome-android-internals-resources-)
