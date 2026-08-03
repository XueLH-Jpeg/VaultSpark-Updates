# VaultSpark GitHub 更新发布指南

VaultSpark 的联网能力只用于线上更新：客户端读取 GitHub 上的静态更新清单，下载 GitHub Release 安装包，并在打开安装包前校验文件大小与 SHA-256。软件不会上传任务、素材路径、日志或设备信息。

## 第一次配置

1. 新建一个公开 GitHub 仓库。公开仓库才能让已安装的客户端无登录读取更新清单和安装包。
2. 在本机项目目录运行：

   ```bash
   node tools/prepare-github-update.mjs --owner 你的GitHub用户名 --repo 仓库名 --notes "本次更新说明"
   ```

3. 工具会自动：
   - 检查 macOS 与 Windows 版本号是否一致；
   - 找到当前版本的 DMG 与 Windows Setup.exe；
   - 计算安装包大小和 SHA-256；
   - 生成 `updates/vaultspark-update.json`；
   - 把两端客户端的清单地址和 GitHub 主机白名单写入 `package.json`。
4. 再重新打包一次客户端，使 GitHub 清单地址进入正式安装包。

也可以直接双击项目根目录的 `发布VaultSpark更新.command`。它会按正确顺序完成地址配置、两端打包、哈希计算和清单生成，并打开三个待上传目录。

## 每次发布更新

1. 同时提高 `macOS/package.json` 和 `Windows/package.json` 的版本号。
2. 分别生成 DMG 与 Windows Setup.exe。
3. 运行上面的清单生成命令。
4. 在 GitHub 创建与版本一致的 Release 标签，例如 `v1.1.4-beta.1`。
5. 把两个安装包上传为该 Release 的附件。
6. 提交并推送 `updates/vaultspark-update.json`。

客户端启动约 12 秒后会静默检查一次，之后每 6 小时检查一次；用户也可以在“设置 → 线上更新”手动检查。

## 安装行为

- Windows：下载并校验 Setup.exe 后启动交互式安装程序，用户仍可选择安装目录。
- macOS：下载并校验 DMG 后打开磁盘映像，由用户把新版拖入“应用程序”替换旧版。

macOS 当前安装包未做 Apple Developer ID 签名，因此不执行静默自替换。以后完成签名与公证后，可以再升级为原生自动替换。
