# VaultSpark 更新发布库

VaultSpark 是用于拍摄素材下卡、分类整理、多目标备份与校验的桌面工具。本仓库发布安装包、版本说明及公开更新清单。

## Windows 下载

当前版本：**1.2.29**（Windows 10/11 x64）。

- [安装版 Setup.exe](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.29/VaultSpark-1.2.29-Windows-x64-Setup.exe)：用于首次安装或覆盖升级。
- [免安装版 Portable.exe](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.29/VaultSpark-1.2.29-Windows-x64-Portable.exe)：不替换已安装客户端。
- [SHA-256 校验文件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.29/VaultSpark-1.2.29-Windows-SHA256SUMS.txt)。
- [本版说明与附件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/tag/v1.2.29)。

## 本次更新

- 修复全新任务在“正在创建”“扫描素材”阶段长时间保持 0 的问题：保留目录、空间和设备检查，去除普通全新拷贝前多余的整批源文件校验扫描。
- 拷贝过程中同步保存文件指纹。完成后明确显示“已拷贝，未核验”，可选择“核验已拷贝素材”或“稍后核验”。
- 用户主动核验时仅读取目标副本，与拷贝时保存的指纹比对，不需要重新读取 SD 卡；可选媒体可读性检查也读取目标文件。
- 核验通过后再生成相应报告。缺失文件、内容损坏或基准不完整不会显示整体核验通过；完成提示、任务日志和收工统计同步区分“已拷贝”与“已核验”。
- 改善读取阶段的暂停和取消响应；拷贝中源文件变化或任一目标失败时，不会误报完成。
- 修复窄窗口下核验提示按钮被挤成竖排和文字溢出，支持按钮组随可用宽度换行。

## 升级说明

- 先结束正在运行的任务并完全退出旧版，再使用 Setup.exe 覆盖升级；免安装版不替换已安装客户端。
- 新流程的任务意外中断后，未完成部分需要重新导入。已有重复文件的检查规则继续保留。
- “已拷贝”不等于“已核验”，未核验前不能确认副本完整性。
- Windows 安装包尚未进行数字签名，系统可能提示“未知发布者”。macOS 本次不提供新版安装包。

## 官网与更新数据

- [软件官网](https://xuelh.cn/software/vaultspark)
- [官网更新日志](https://xuelh.cn/software/vaultspark#changelog)
- 新版客户端读取官网 /software/vaultspark-update.json。
- 本仓库 updates/vaultspark-update.json 供仍使用 GitHub 地址的旧客户端检查更新。
- updates/release-catalog.json 是公开版本记录，updates/website-releases.json 是官网格式数据。仅在对应平台附件发布并核对成功后才更新清单。

安装前可使用 SHA-256 核对文件。软件更新流程也会核对下载文件的字节数和摘要，安装由用户主动确认。
