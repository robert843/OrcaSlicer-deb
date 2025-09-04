---
layout: home
title: OrcaSlicer DEB Repository
---
This project provides a non-official DEB repository for the popular 3D printing slicer, OrcaSlicer. It offers a convenient way for users on Debian-based systems (like Debian, Ubuntu, and Linux Mint) to install and update OrcaSlicer directly via their system's package manager.

By packaging the application as a DEB, this repository ensures proper system integration, including automatic updates and correct desktop environment shortcuts. This eliminates the need for manual handling of AppImage files, offering a seamless and native installation experience.

## How to Install?

### Add a Debian Repository

Run:

```
wget -qO- {{ site.url }}{{ site.baseurl }}/public.asc | sudo tee /etc/apt/keyrings/orca-slicer.asc >/dev/null
```

Next, create the source in `/etc/apt/sources.list.d/`

```
echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/orca-slicer.asc] {{ site.url }}{{ site.baseurl }} stable main" | sudo tee /etc/apt/sources.list.d/orca-slicer.list >/dev/null
```

Then run `apt update && apt install -y` followed by the names of the packages you want to install.