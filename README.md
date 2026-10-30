# 印象笔记跳转指定笔记（evernote:/// 链接）

印象笔记（Yinxiang）笔记间跳转的实战方法：手机端 adb 命令直开指定笔记、evernote:/// 链接格式说明、手机浏览器/电脑端跳转差异。

## 文档

- [跳转方法与 evernote:/// 链接格式（笔记全文）](docs/evernote-note-jump.md)

## 背景速记

- 手机端可用 adb 直接拉起笔记：`am start -a com.yinxiang.action.VIEW_NOTE --es NOTE_GUID "<guid>"`，或 `am start -a android.intent.action.VIEW -d "<笔记网页链接>"`；
- 印象笔记 APP 注册了 `https` scheme + `app.yinxiang.com` 域名 + 路径白名单 `/shard/s.*/nl/.*`（URIBrokerActivity），部分手机浏览器允许跳转时会自动打开对应笔记页；
- `evernote://view/<user id>/<shard id>/<note guid>/<client specific id>/[linked notebook guid]/` —— 电脑端可实现跳转，手机端不行；`evernote:///view/` 格式则手机可以、电脑不行。

## 免责声明

- 内容为个人实战记录，仅供参考；不同平台版本（APP/浏览器/系统）行为可能有差异，请以实际表现为准。
- 文中出现的笔记 GUID 为用户个人笔记标识，仅作示例。
