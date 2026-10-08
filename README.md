# ths-linker（同花顺助手）发布页

本仓库**只存放**公开发布内容：安装包 Release、变更说明与基础文档（使用说明 / 接口文档）。  
**不含**产品源码。

| 项 | 说明 |
| --- | --- |
| 平台 | Windows |
| 文档站点 | [GitHub Pages](https://awamwang.github.io/ths-linker-releases/) |
| 使用与接口 | [docs/index.html](docs/index.html) |
| 变更记录 | [CHANGELOG.md](CHANGELOG.md) |

## 下载

请到本仓库 [Releases](https://github.com/awamwang/ths-linker-releases/releases) 下载最新 `ths-linker.exe`。

推荐使用带 `v` 前缀的版本标签（例如 `v0.1.0`）。

## 文档如何更新

使用说明与接口文档以 `docs/index.html` 为唯一维护源，由发布流程自动同步到本仓库，请勿在本仓库直接改协议正文以免被覆盖。

## 自动更新

客户端支持多更新源按序探测、自动降级：

- 发布时自动生成并上传 `latest.json`（版本 / exe_url / sha256 / 说明），同时推送到 Pages 站点根目录：`https://awamwang.github.io/ths-linker-releases/latest.json`
- 托盘菜单「检查更新」可手动触发；启动时默认静默检查一次（可在 `update.check_on_startup` 关闭）

## 说明

- 本仓库由发布流程在 **git tag** 触发时自动推送更新。
- 若 Pages 尚未启用，可直接打开 `docs/index.html` 或克隆后本地浏览。
