# STM32MP157C-DK2 Buildroot Image

基于 [Buildroot](https://buildroot.org/) 自动构建 STM32MP157C Discovery Kit 2 的 SD 卡启动镜像。

## 获取镜像

两种方式：
1. **GitHub Actions Artifacts** — 进入 [Actions](../../actions) 页面，点击最新成功的 workflow run，下载 `stm32mp157c-dk2-sdcard`
2. **Release** — 推送 `v*` tag 后自动创建 Release

## 烧录 SD 卡

```bash
xz -d sdcard.img.xz
sudo dd if=sdcard.img of=/dev/sdX bs=4M status=progress conv=fsync
