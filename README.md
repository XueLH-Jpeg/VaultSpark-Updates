# VaultSpark 更新发布库

VaultSpark 是用于拍摄素材下卡、分类整理、多目标备份与校验的桌面工具。本仓库发布安装包、版本说明及公开更新清单。

## Windows 下载

当前版本：**1.2.30**（Windows 10/11 x64）。

- [安装版 Setup.exe](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.30/VaultSpark-1.2.30-Windows-x64-Setup.exe)：用于首次安装或覆盖升级。
- [免安装版 Portable.exe](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.30/VaultSpark-1.2.30-Windows-x64-Portable.exe)：不替换已安装客户端。
- [SHA-256 校验文件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.30/VaultSpark-1.2.30-Windows-SHA256SUMS.txt)。
- [本版说明与附件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/tag/v1.2.30)。

## 本次更新

- 保存任务记录时，如果文件被其他程序短暂占用，软件会自动等待并重试，减少偶发中断。
- 如果记录一直无法保存，会说明问题出在任务记录，并提示检查文件占用、权限或磁盘空间，方便排查。已经拷贝的素材会保留。
- 任务历史暂时读不出来时，会保留原有记录，避免已有任务被新记录覆盖。
- 改善同时保存多个任务、从列表移除项目时的稳定性，减少记录遗漏或互相覆盖。
- 文件持续被占用时，不再反复堆积进度保存请求，避免任务迟迟停不下来。
- 任务历史读取失败时，软件仍可打开并显示原因；处理后可点击「刷新」重新读取。

## 升级说明

- 请先结束当前任务，并完全退出旧版（包括托盘图标），再运行 Setup 安装包覆盖升级。原有任务记录会保留。
- 如果之前的导入已经中断，请保留原素材，处理问题后重新导入并核验，再决定是否清理素材卡。
- 免安装版适合直接运行；升级已经安装的软件请使用 Setup 安装包。
- Windows 安装包暂未进行数字签名，系统可能显示「未知发布者」。
- 本次发布 Windows 10/11 x64 版。macOS 已同步相关代码修复，暂不提供新版安装包。

## 官网与更新数据

- [软件官网](https://xuelh.cn/software/vaultspark)
- [官网更新日志](https://xuelh.cn/software/vaultspark#changelog)
- 新版客户端读取官网 /software/vaultspark-update.json。
- 本仓库 updates/vaultspark-update.json 供仍使用 GitHub 地址的旧客户端检查更新。
- updates/release-catalog.json 是公开版本记录，updates/website-releases.json 是官网格式数据。仅在对应平台附件发布并核对成功后才更新清单。

安装前可使用 SHA-256 核对文件。软件更新流程也会核对下载文件的字节数和摘要，安装由用户主动确认。
