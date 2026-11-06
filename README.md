# VaultSpark

用于拍摄素材下卡、整理、多目标备份与校验的桌面工具。当前版本 **1.2.34**。

## 下载

- [Windows 10/11 x64 安装包](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.34/VaultSpark-1.2.34-Windows-x64-Setup.exe) · [SHA-256 校验文件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.34/VaultSpark-1.2.34-Windows-SHA256SUMS.txt)
- [macOS · Apple Silicon 安装包](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.34/VaultSpark-1.2.34-arm64.dmg) · [SHA-256 校验文件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.34/VaultSpark-1.2.34-arm64.dmg.sha256.txt)
- [本版说明与附件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/tag/v1.2.34)
- [软件官网](https://xuelh.cn/software/vaultspark)

## 本次更新

- 新增“只保存转正视频”：直接读取来源生成目标视频，不再额外保存一份电脑原片。
- 多个目标共用一次转正结果，再分发和核验；来源素材保持不变。
- 支持 MP4、MOV、M4V 的原始画面转正和更改方向标记；方向不确定或格式不支持时原样导入并提示。
- 仍可选择保留原片和转正副本，旧任务与旧模板维持原来的保存方式。
- 手动重新指定方向后可再次导入，已有文件保留，新结果自动换名保存。
- 修复自动分类预检中的“文件夹名称无效”，并补齐 Mac 的 MP4 输出支持。

## 安装与核验

- 升级前结束正在运行的任务并完全退出旧版；Windows 使用 Setup 安装版，Mac 打开 DMG 后将应用拖入 Applications。
- 原始画面转正会重新编码；转正结果与原片分别记录指纹，不能将转正结果当作原片逐字节备份或据此安全放卡。
- Windows 安装包未配置 Authenticode 签名；已完成构建和实际安装载荷校验，尚未在 Windows 实机验证安装及原生媒体功能。
- Mac 适用于 Apple Silicon，已通过本机实际视频转正测试；采用本地 ad-hoc 签名，未进行 Developer ID 签名与公证。

## 更新数据

客户端读取官网的 /software/vaultspark-update.json；本仓库 updates/vaultspark-update.json 供使用 GitHub 地址的旧客户端检查更新。公开发布记录保存在 updates/release-catalog.json，官网格式数据保存在 updates/website-releases.json。
