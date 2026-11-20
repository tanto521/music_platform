# 听见 · Music Platform

Android 音乐应用的版本与更新发布仓库。当前预览版要求 Android 12 或以上，支持 ARM64 和 x86_64。

## 下载

- [下载听见 1.0.0.7](https://github.com/tanto521/music_platform/releases/download/updates-preview/tingjian-android12-64bit-v1.0.0.7.apk)
- [Preview 发布通道](https://github.com/tanto521/music_platform/releases/tag/updates-preview)
- [该版本完整源码快照](https://github.com/tanto521/music_platform/releases/download/updates-preview/music-platform-source-v1.0.0.7.zip)

## 更新机制

应用内“版本管理”支持检查整包更新、下载签名页面资源及回退。CSS、JavaScript和图片的兼容调整可通过热更分发；Go服务、Android权限与原生能力、HTML模板及接口不兼容调整仍需要新APK。

资源清单采用 Ed25519 签名，资源包检查 SHA256、兼容范围和大小；试运行资源未成功初始化时下次启动回退。APK由系统确认安装，不静默安装。固定清单地址为：

`https://github.com/tanto521/music_platform/releases/download/updates-preview/manifest.json`

安装1.0.0.6或更早版本的设备需要先安装一次新的基础包，才能使用这套更新机制。GitHub下载在部分网络下可能较慢或不可达，应用检查失败时保留当前已验证版本。

## 源码与许可证

本应用基于 [guohuiyuan/go-music-dl](https://github.com/guohuiyuan/go-music-dl) 二次开发，遵循 AGPL-3.0。每次APK发布同时提供对应源码快照，包含项目许可证与构建脚本；依赖及其许可证以源码中的声明为准。

预览版使用开发签名。应用与音源可用性受平台接口、网络及登录状态影响。请仅使用有权使用的内容。
