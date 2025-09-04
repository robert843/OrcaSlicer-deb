---
layout: home
title: OrcaSlicer deb
---

## How to Install?

### Add a Debian Repository

Run:

```
wget -qO- {{ site.url }}/{{ site.base_url }}/public.asc | sudo tee /etc/apt/keyrings/orca-slicer.asc >/dev/null
```

Next, create the source in `/etc/apt/sources.list.d/`

```
echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/orca-slicer.asc] {{ site.url }}/{{ site.base_url }}/deb stable main" | sudo tee /etc/apt/sources.list.d/orca-slicer.list >/dev/null
```

Then run `apt update && apt install -y` followed by the names of the packages you want to install.