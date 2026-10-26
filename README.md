# CineArm 下载与版本记录

CineArm 用于机械臂拍摄的项目编辑、时间线与节点编排。本仓库用于发布安装包与更新说明。

**[进入版本下载页](https://github.com/Kikuku10/CineArm-Releases/releases)**

下载页提供当前测试版本及历史版本；请按平台和版本号选择安装包。

## 选择安装包

| 平台 | 文件 | 说明 |
| --- | --- | --- |
| macOS Apple Silicon | `CineArm-macOS-AppleSilicon-版本号.zip` | M 系列芯片，macOS 14 及以上；解压后将整个 CineArm.app 放入应用程序 |
| Windows x64 | `CineArm-Windows-版本号-x64-setup.exe` | Intel/AMD 64 位电脑；运行安装程序，缺少 WebView2 时使用随包离线运行库补装 |

以每个发布页列出的实际资产和系统要求为准。测试版会标记为 Pre-release；历史版本保留在下载页。

安装包包含所需 Python、Dobot SDK 与跟焦运行环境，无须额外安装开发工具。系统相机、蓝牙及设备网络仍按实际用途配置和授权。

Mac 当前测试包使用 Apple Development 签名，未做 Developer ID 公证；Windows 当前测试包未做发行者代码签名，首次打开可能出现系统信任提示。请先核对下载来源和校验值，再按系统界面确认。

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

Mac、Windows 和 iPad 使用同一个安装包体系，安装后默认为免费版，无需登录。项目文件数量、虚拟编辑、预览、保存和导出不限；实体机械臂连接、使能、手动控制、拖拽示教、Air4 与跟焦也无需商业许可，仍须满足设备兼容、连接和安全条件。

免费版可执行整个项目最多 1 条时间线，且每条时间线最多 4 个姿态关键帧或节点；跟焦、目标、音频和自定义设备轨道不占姿态额度。超过额度的项目仍可完整编辑、预览和保存，但项目实机播放、定位、导航、回位及暂停后继续需要 **CineArm Studio**。

Studio 解除上述时间线和姿态数量限制，不放宽机械臂兼容、安全校验、停止和现场条件。已有永久授权对应 Studio，已有 14 天试用对应 Studio 试用；永久授权最多绑定两台设备，成功联网验证后可取得最多 7 天离线许可。当前没有应用内自助注册、购买或领取试用入口，授权和试用由发行者开通；本下载仓库不公布未确认的价格或付款方式。

平台支持与验证范围见对应版本的更新说明。离线或虚拟验证不代表真实机械臂现场验收。

CineArm 保持闭源。本仓库公开用于下载，不授予 CineArm 源码或安装包内容的开源许可；第三方组件遵循安装包内各自的许可声明。

## 反馈

可以通过本仓库 Issues 提交版本号、系统与芯片类型、复现步骤。请勿上传账号令牌、激活凭据或含个人信息的项目与日志。
