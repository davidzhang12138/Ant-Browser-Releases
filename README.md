# Ant Browser Releases

本仓库承载 `Ant Browser` 的公开发布自动化和安装包，不包含私有源码。

## 发布流程

- `sync-private-tags` 每 5 分钟读取私有源码仓库的版本 Tag，也支持手动指定 Tag。
- `release` 使用只读 Deploy Key 检出指定 Tag，构建 Windows、Linux 和 macOS 安装包。
- 构建成功后在本仓库创建同名 GitHub Release，并上传各平台安装包。

私有源码只会在受信任的 GitHub-hosted runner 中临时检出，不会提交到本公开仓库。

## 下载

前往 [Releases](https://github.com/davidzhang12138/Ant-Browser-Releases/releases) 下载最新版本。

首个自动同步版本为 `v1.6.0.4`。
