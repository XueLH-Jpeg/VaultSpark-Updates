# VaultSpark 更新发布库

VaultSpark 是用于拍摄素材下卡、分类整理、多目标备份与校验的桌面工具。本仓库用于发布安装包、版本说明及公开更新清单，不包含用户素材、任务记录或设备信息。

## Windows 下载

当前版本：**1.2.26**（Windows 10/11 x64）。

- [安装版 Setup.exe](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.26/VaultSpark-1.2.26-Windows-x64-Setup.exe)：用于首次安装或覆盖升级。
- [免安装版 Portable.exe](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.26/VaultSpark-1.2.26-Windows-x64-Portable.exe)：不替换已安装客户端。
- [SHA-256 校验文件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/download/v1.2.26/VaultSpark-1.2.26-Windows-SHA256SUMS.txt)。
- [本版说明与附件](https://github.com/XueLH-Jpeg/VaultSpark-Updates/releases/tag/v1.2.26)。

升级前请结束正在拷贝的任务并退出旧版，选择原安装位置覆盖安装。Windows 安装包尚未进行数字签名，系统可能提示“未知发布者”。旧版未完成任务需核对原素材后重新选择来源追加，不会直接按旧账本自动续传。

macOS 新安装包尚未提供，不要把 Windows 附件用于 Mac。

## 本次更新

- 新建与继续导入增加名称、修改时间、大小的升序/降序，预整理、拷贝和自动编号顺序一致。
- 保留手动归类和素材选择，避免旧扫描或预检覆盖新设置；追加去重后连续编号，恢复保留账本顺序。
- 软件发现新版本后提示，可查看更新说明或稍后处理，不自动下载或安装。
- 官网软件页提供更新日志入口，客户端与官网从同一份发布记录生成说明。

## 官网与更新数据

- [软件官网](https://xuelh.cn/software/vaultspark)
- [官网更新日志](https://xuelh.cn/software/vaultspark#changelog)
- 新版客户端读取官网 `/software/vaultspark-update.json`。
- 本仓库 `updates/vaultspark-update.json` 同步保留，供仍使用 GitHub 地址的旧客户端检查更新。
- `updates/release-catalog.json` 为公开版本记录，`updates/website-releases.json` 为官网格式数据。安装包上传并核对成功后才发布新清单；没有对应平台附件就不标记该平台可更新。

安装前请使用 SHA-256 核对文件。软件的更新流程也会核对下载文件的字节数和摘要，安装由用户主动确认。
