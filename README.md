# LibreTranslate 懒猫微服包

自托管机器翻译服务与网页界面，翻译引擎由开源 Argos Translate 驱动。

- 上游：<https://github.com/LibreTranslate/LibreTranslate>
- 镜像：`libretranslate/libretranslate`
- 许可：AGPL-3.0（全文见 content/licenses/LICENSE）

## 组成
单容器，监听 5000 端口，无需外部数据库。

## 关键配置说明
- 模型目录 `/home/libretranslate/.local` 必须持久化，否则每次重启都重新下载模型。
- API keys 数据库 `/app/db` 也做持久化（仅当启用 LT_API_KEYS 时使用）。
- 本应用没有账号体系，访问由懒猫入口鉴权，因此不设 public_path。

## 未验证部分
未在真机上实测：首次启动下载模型、网页与 API 翻译、重启后模型留存。
