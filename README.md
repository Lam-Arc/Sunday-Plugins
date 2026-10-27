# Sunday 插件市场

Sunday 的独立插件仓库，目前提供 **QQ robot**（`qq-bot`）和**刷B站**（`bili-scroll`）。插件不随主程序内置。

在 Sunday 0.3.23 或更新版本的「插件 → 插件市场」中点击安装。宿主从本仓库的 GitHub Release 下载 ZIP，校验 SHA-256、插件名称和版本，保留运行数据后完成安装或更新。网络拓展可用时自动优化 GitHub 下载；无需访问官网。

命令行：`sunday-core plugin market list`、`sunday-core plugin market install qq-bot`、`sunday-core plugin market install bili-scroll`。需连接正在运行的 Sunday。

QQ 账号凭据请在安装后的设置中配置；刷B站首次使用请按插件内指引连接账号与准备运行环境。发布包不含账号凭据、用户配置或运行数据。

## 开发和发布

源码位于 `plugins/qq-bot` 与 `plugins/bili-scroll`，各自保留 LICENSE、NOTICE.md 和第三方许可证。

构建：`python scripts/package-market-plugins.py --tag plugins-2026.10.27 --output dist`。产物包括两个 ZIP、`catalog.json` 和 `SHA256SUMS`。新建 `plugins-*` 标签会由 GitHub Actions 构建并发布，市场自动读取最新目录。每次更新插件代码必须同步提高该插件的版本号。
