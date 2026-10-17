# EdgeRoute v1.6.5

## 下载内容

本 Release 提供 Linux amd64 的正式授权构建包：

- `edgeroute-admin-linux-amd64-licensed-v1.6.5.zip`：管理端
- `edgeroute-api-linux-amd64-licensed-v1.6.5.zip`：API 服务
- `edgeroute-node-linux-amd64-licensed-v1.6.5.zip`：边缘节点
- `edgeroute-user-linux-amd64-v1.6.5.zip`：用户端

每个组件都附带同名 `.manifest.json`。清单使用 Ed25519 签名，包含组件、版本、架构、文件大小和 SHA-256。请在安装前验证 `SHA256SUMS` 和清单签名。

## 验证材料

- `SHA256SUMS`：本 Release 上传文件的 SHA-256 校验值
- `production-20261009.pem`：发布验签公钥，仅用于验证签名，不是私钥
- `RELEASE_RECORD.json`：机器可读发布记录
- `RELEASE_RECORD.signature.json`：`RELEASE_RECORD.json` 的 Ed25519 签名
- `GITHUB_RELEASE_NOTES.md`：本次发布说明及安装注意事项

签名身份：`production-20261009`。构建编号：`v1.6.5-20261017-r1`。

## 安装前注意事项

1. 先备份现有配置和数据库。
2. 先升级管理端/API，再升级节点；升级节点前排空节点队列。
3. 安装前验证 SHA-256 和 Ed25519 清单，确认组件版本匹配。
4. EdgeLicense 是独立项目，本 Release 不替换许可证服务或其数据库。
5. 本 Release 的真实环境验收边界、已知问题和回滚注意事项以 `RELEASE_RECORD.md` 为准。

## 安全说明

发布私钥、许可证私钥、数据库、配置文件、客户数据和 SMTP/API 密钥均不包含在本 Release 中。不要把任何私钥上传到 GitHub。
