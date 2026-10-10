# VaultSpark 更新发布库

VaultSpark 是用于拍摄素材下卡、分类整理、多目标备份与校验的桌面工具。本仓库发布安装包、版本说明及公开更新清单。

当前版本：**1.2.33**。[查看本版说明与附件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/tag/v1.2.33)。

## Windows 下载

适用于 **Windows 10/11 x64**，本版提供 Setup 安装版。

- [安装版 Setup.exe](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.33/VaultSpark-1.2.33-Windows-x64-Setup.exe)：用于首次安装或覆盖升级。
- [Windows SHA-256 校验文件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.33/VaultSpark-1.2.33-Windows-SHA256SUMS.txt)。

## macOS 下载

适用于 **Apple Silicon**。构建最低目标为 macOS 11，其他系统版本尚未实机验收。

- [macOS DMG 安装包](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.33/VaultSpark-1.2.33-arm64.dmg)：打开后将 VaultSpark 拖入 Applications。
- [macOS SHA-256 校验文件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.33/VaultSpark-1.2.33-arm64.dmg.sha256.txt)。

## 本次更新

Windows 与 macOS 同步更新教程和视频转正操作说明。

- 新手教程与视频转正教程统一为背景压暗、当前控件高亮和旁侧说明卡片。
- 教程支持上一步、下一步、跳过和重新查看，并保留已完成的教程记录。
- 视频转正教程可在未添加素材时浏览；实际导入、导出仍由你确认操作。
- 处理方式统一为“原始画面转正”和“更改方向标记”，转正结果另存为副本，保留原片。
- Windows 保留原有标题栏、窗口控制、任务记录及安装升级标识。

## 升级说明与验证范围

- 升级前请结束正在运行的任务并完全退出旧版。Windows 使用 Setup 安装版，macOS 打开 DMG 后将应用拖入 Applications。
- Windows 安装包未配置 Authenticode 签名；已完成编译、前端界面和包内容校验，尚未在 Windows 实机执行安装、卸载及原生媒体功能测试。
- macOS 采用本地 ad-hoc 签名，未做 Apple Developer ID 签名与公证。
- 安装前可使用对应平台的 SHA-256 文件核对安装包。

## 官网与更新数据

- [软件官网](https://xuelh.cn/software/vaultspark)
- [官网更新日志](https://xuelh.cn/software/vaultspark#changelog)
- 新版客户端读取官网 `/software/vaultspark-update.json`。
- 本仓库 `updates/vaultspark-update.json` 供仍使用 GitHub 地址的旧客户端检查更新。
- `updates/release-catalog.json` 是公开版本记录，`updates/website-releases.json` 是官网格式数据。仅在对应平台附件发布并核对成功后才更新清单。

软件更新流程会核对下载文件的字节数和摘要，安装由用户主动确认。
