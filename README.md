# Project-Monet
本项目通过 Magisk 模块挂载对第三方应用的运行时资源叠加层，为第三方应用适配 Android12+ 的动态取色

本仓库中有多个模块源码，请在上方切换分支

# 酷安莫奈取色

## 如何使用

- 已刷入版本号 1609+ 的模块：
    - 请下载 [MonetCoolapk.apk](https://github.com/N3kOk0/Project-Monet/releases/latest/download/MonetCoolapk.apk) 并安装
- 从旧版升级或全新安装：
    - 从最新的 Release 中下载 [last.zip](https://github.com/N3kOk0/Project-Monet/releases/latest/download/last.zip)
    - 使用支持 Magisk 模块的 Root 管理器刷入 last.zip
    - 重启设备

## 如何编译

- 使用 git 将项目拉取到本地
- 在应用目录中运行 `aapt2 compile -v --dir res/ -o res.zip` 编译 .flat 文件
- 运行 `aapt2 link --no-resource-removal -I [android.jar位置] --manifest Android Manifest.xml -o MonetCoolapk.apk res.zip` 生成 apk
- 将 apk 签名
- 放入模块挂载目录
