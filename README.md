# CineArm 下载与版本记录

CineArm 用于机械臂拍摄的项目编辑、时间线与节点编排。本仓库用于发布安装包与更新说明。

**[进入版本下载页](https://github.com/Kikuku10/CineArm-Releases/releases)**

当前已建立发布入口；首个可下载版本将在下一次打包完成并通过对应检查后发布。

## 选择安装包

| 平台 | 文件 | 说明 |
| --- | --- | --- |
| macOS Apple Silicon | `CineArm-macOS-AppleSilicon-版本号.zip` | M 系列芯片，macOS 14 及以上；解压后将整个 CineArm.app 放入应用程序 |
| Windows x64 | `CineArm-Windows-版本号-x64-setup.exe` | Intel/AMD 64 位电脑；运行安装程序，缺少 WebView2 时使用随包离线运行库补装 |

以每个发布页列出的实际资产和系统要求为准。测试版会标记为 Pre-release；历史版本保留在下载页。

安装包包含所需 Python、Dobot SDK 与跟焦运行环境，无须额外安装开发工具。系统相机、蓝牙及设备网络仍按实际用途配置和授权。

Mac 当前测试包使用本地临时签名，未做 Apple 公证；Windows 当前测试包未做发行者代码签名，首次打开可能出现系统信任提示。请先核对下载来源和校验值，再按系统界面确认。

## 校验下载

每个版本提供 `SHA256SUMS.txt` 和 `release-manifest.json`，列出文件名、版本、平台、大小和 SHA-256。可使用系统工具核对：

macOS：

```sh
shasum -a 256 CineArm-macOS-AppleSilicon-版本号.zip
```

Windows PowerShell：

```powershell
Get-FileHash .\CineArm-Windows-版本号-x64-setup.exe -Algorithm SHA256
```

## 使用与授权

项目编辑、虚拟机械臂及 Air4 使用无需商业激活；新的实体机械臂连接与控制需要账号及有效许可，使用 Air4 仍须完成连接和安全接管。平台支持与验证范围见对应版本的更新说明。离线或虚拟验证不代表真实机械臂现场验收。

CineArm 保持闭源。本仓库公开用于下载，不授予 CineArm 源码或安装包内容的开源许可；第三方组件遵循安装包内各自的许可声明。

## 反馈

可以通过本仓库 Issues 提交版本号、系统与芯片类型、复现步骤。请勿上传账号令牌、激活凭据或含个人信息的项目与日志。
