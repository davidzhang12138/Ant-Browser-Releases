# Ant Browser Releases

本仓库承载 `Ant Browser` 的公开发布自动化，不包含私有源码。

## 发布流程

- `sync-private-tags` 每 5 分钟读取私有源码仓库的版本 Tag，也支持手动指定 Tag。
- `release` 使用只读 Deploy Key 检出指定 Tag，构建 Windows、Linux 和 macOS 安装包。
- 构建成功后在本仓库创建同名 GitHub Release，并上传各平台安装包。

## 安全与隐私

- 私有源码只在受信任的 GitHub-hosted runner 上临时检出，不写入本公开仓库、公共缓存或公开构建产物。
- 检出使用只读 Deploy Key（`SOURCE_DEPLOY_KEY`），仅对本仓库开放私有源码仓库的只读权限。
- 本仓库的 Release 与安装包是唯一对外公开的内容，私有仓库不保存任何发布产物。

## 下载

前往 [Releases](https://github.com/davidzhang12138/Ant-Browser-Releases/releases) 下载最新版本。

首个自动同步版本为 `v1.6.0.4`。
