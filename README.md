# Project-Monet
本项目通过对第三方应用的运行时资源叠加层，为第三方应用适配 Android12+ 的动态取色

本仓库中有多个模块源码，请在上方切换分支
# 酷安莫奈取色
## 如何使用
- 在 [Release](https://github.com/N3kOk0/Project-Monet/releases) 中下载最新的模块
- 在 Magisk/Apatch/KernelSU 管理器中刷入
- 重启设备

## 如何编译
- 使用 git 将项目拉取到本地
- 在应用目录中运行 `aapt2 compile -v --dir res/ -o res.zip` 编译 .flat 文件
- 运行 `aapt2 link --no-resource-removal -I [android.jar位置] --manifest Android Manifest.xml -o ProjectMonet.apk res.zip` 生成 apk
- 将 apk 签名
- 放入模块挂载目录
