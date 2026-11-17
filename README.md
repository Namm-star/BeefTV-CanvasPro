# BeefTV CanvasPro

[English](README.en.md)

BeefTV 的 CanvasPro 修改版 Windows 安装包与模型配置包。上游项目为 [glanderness/BeefTV](https://github.com/glanderness/BeefTV)，本仓库由独立维护者发布修改版，不代表上游官方发行。

[下载安装包与配置文件](https://github.com/Namm-star/BeefTV-CanvasPro/releases/latest)

## 安装与更新

1. 在 Release 中下载 `BeefTV-v2.2.5-windows-amd64-no-account-20261117-setup.exe`，退出 BeefTV 后运行安装程序。
2. 在「模型配置」中填写自己的 CanvasPro API Key。
3. 老用户升级后，如仍显示旧配置包，在「模型配置 → 模型配置包」预览并应用内置更新，或导入本次 Release 附带的 JSON 文件。

支持 Windows x64。安装包未做代码签名。安装包与公开配置不包含用户 API Key、项目、数据库或代理设置；模型调用由所选 API 服务按其规则收费。

## 本版变化

- 移除上游 BeefTV 登录、余额、充值、官方账户连接与自动恢复入口。侧栏提供工作台设置和本修改版发布页，旧登录及充值接口不可用。
- 关闭上游应用自动更新，后续版本从本仓库 Release 下载，避免安装回带有上游账户模块的官方版本。
- 基于 BeefTV v2.2.5，保留 CanvasPro 原生模型配置、协议适配、结果下载代理和 ComfyUI 接入修正。
- 内置执行引擎 3 和 350 款模型配置：文字 28 款、图片 45 款、视频 277 款。
- 为已适配的即梦系列增加临时参考素材上传，支持批次创建、上传、状态查询及恢复；本地参考素材无需另配图床。
- 现有导入配置保持有效，可手动应用内置更新；运行中的任务继续使用原有协议快照。
- 提供模型配置维护 Skill，后续可按最新 API 文档生成可导入的 JSON 配置包。

发行构建对应修改提交 `f3a8740`。模型配置包版本为 `20261116-temporary-reference-media-v1-pack1`。升级会保留 CanvasPro 和其他自带 Key 的服务连接；原先使用上游官方账户的节点需要改选自带 Key 的模型服务。

## 文件校验

Release 附带 `SHA256SUMS.txt`。在 PowerShell 中使用 `Get-FileHash -Algorithm SHA256 <文件路径>`，与文件中的校验值比较。

## 许可证与来源

发行保留上游的 [LICENSE](LICENSE)、[NOTICE](NOTICE) 和 [第三方声明](THIRD_PARTY_NOTICES.md)。历史 MIT 部分、BeefTV Source Available License 1.0 部分及第三方组件分别保留原有条款，详见这些文件。
