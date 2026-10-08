# ths-linker（同花顺助手）发布页

本仓库**只存放**公开发布内容：安装包 Release、变更说明与基础文档（使用说明 / 接口文档）。  
**不含**产品源码。源码在私有仓库维护。

| 项 | 说明 |
| --- | --- |
| 平台 | Windows |
| 文档站点 | [GitHub Pages](https://awamwang.github.io/ths-linker-releases/)（启用后可用） |
| 使用与接口 | [docs/index.html](docs/index.html) |
| 变更记录 | [CHANGELOG.md](CHANGELOG.md) |

## 下载

请到本仓库 [Releases](https://github.com/awamwang/ths-linker-releases/releases) 下载最新 `ths-linker.exe`。

推荐使用带 `v` 前缀的版本标签（例如 `v0.1.0`）。

## 文档如何更新

使用说明与接口文档以私有主仓的 `docs/index.html` 为唯一维护源，发布流程会同步到本仓库 `docs/index.html`，请勿在本仓库直接改协议正文以免被覆盖。

## 自动更新

客户端支持多更新源按序探测、自动降级：

- 发布时自动生成并上传 `latest.json`（版本 / exe_url / sha256 / 说明），同时推送到 Pages 站点根目录：`https://awamwang.github.io/ths-linker-releases/latest.json`
- GitHub Releases 附件包含 `ths-linker-vX.Y.Z.exe`、`ths-linker-vX.Y.Z.exe.sha256` 与 `latest.json`，供 GitHub API 源解析
- 客户端默认源顺序：GitHub Pages（generic）→ GitHub Releases API（github）；可在本机 `~/.ths-linker/linker_config.json` 的 `update.sources` 中配置自有源并调整顺序（例如自建国内镜像，配置项示例见私有仓库文档）
- 托盘菜单「检查更新」可手动触发；启动时默认静默检查一次（可在 `update.check_on_startup` 关闭）

## 说明

- 本仓库由私有主仓在 **git tag** 触发的 CI 推送更新。
- 若 Pages 尚未启用，可直接打开 `docs/index.html` 或克隆后本地浏览。
