# macOS DMG 发布

提供 macOS 软件的 DMG 安装包和安装说明。

## AudioLoop 0.2.0

AudioLoop 是原生 macOS 应用声音内录工具，可选择应用录音，支持 WAV / CAF、分段保存和离线 MP3 转换。最低支持 macOS 14.2。

| Mac 类型 | 安装包 | 下载 |
| --- | --- | --- |
| Apple Silicon（M 系列芯片） | arm64 DMG | [AudioLoop-0.2.0-macOS-arm64.dmg](https://github.com/MRongM/dmg-release/releases/download/audioloop-v0.2.0/AudioLoop-0.2.0-macOS-arm64.dmg) |
| Intel Mac | x86_64 DMG | [AudioLoop-0.2.0-macOS-x86_64.dmg](https://github.com/MRongM/dmg-release/releases/download/audioloop-v0.2.0/AudioLoop-0.2.0-macOS-x86_64.dmg) |

[发行页面](https://github.com/MRongM/dmg-release/releases/tag/audioloop-v0.2.0)

## 安装

1. 按 Mac 芯片类型下载对应 DMG，并打开镜像。
2. 将 `AudioLoop.app` 拖入镜像中的“应用程序”快捷方式。
3. 推出镜像，从“应用程序”打开 AudioLoop；首次录音时按系统提示授予音频录制权限。

当前应用使用 ad-hoc 签名，尚未进行 Developer ID 签名与 Apple 公证，首次打开可能受 Gatekeeper 限制。

## 校验与许可证

下载附件 `DMG-SHA256SUMS.txt`，计算所下载安装包的 SHA-256 并与文件中的同名记录比较。例如 arm64 版：

```bash
shasum -a 256 "AudioLoop-0.2.0-macOS-arm64.dmg"
```

两个镜像均已验证架构、签名、macOS 14.2 部署目标和安装入口。上述检查不代表所有硬件与系统版本的功能验收。

AudioLoop 内置 LAME 3.100；LAME 许可证原文见 [LICENSES/COPYING.LAME](LICENSES/COPYING.LAME)，应用资源内同时保留许可证。

AudioLoop 应用源码仓库为私有；公开发布内容为安装包、校验文件、安装说明及第三方许可证。
