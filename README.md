# OpenWRT

---

## Overview

- https://github.com/P3TERX/Actions-OpenWrt
- https://github.com/esirplayground/AutoBuild-OpenWrt


## Actions

- Select `Build OpenWRT for xxx` on the Actions page.
- Click the `Run workflow` button.
- When the build is complete, click the `Artifacts` button in the upper right corner of the Actions page to download the binaries.

### Tips

- It may take a long time to create a `.config` file and build the OpenWrt firmware. Thus, before create repository to build your own firmware, you may check out if others have already built it which meet your needs by simply [search `Actions-Openwrt` in GitHub](https://github.com/search?q=Actions-openwrt).

- Add some meta info of your built firmware (such as firmware architecture and installed packages) to your repository introduction, this will save others' time.

## Docker

```bash
# create image
sudo docker build -t openwrt-lede-ubuntu2004:v1 .

# create & run container
sudo docker run -it --name openwrt-lede-build -v ./lede:/app openwrt-lede-ubuntu2004:v1 bash
```
