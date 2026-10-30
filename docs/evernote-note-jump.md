# 印象笔记跳转指定笔记，evernote:///链接

手机打开对应笔记

```bash
adb shell am start -a com.yinxiang.action.VIEW_NOTE --es NOTE_GUID "eaca2c43-345c-45a6-9bf4-d029dfc9006d"
```

```bash
adb shell am start -a android.intent.action.VIEW -d "https://app.yinxiang.com/shard/s61/nl/11553084/eaca2c43-345c-45a6-9bf4-d029dfc9006d/
```

手机浏览器可以查看网页

https://app.yinxiang.com/shard/s61/nl/11553084/9a542e26-e892-4440-934c-189c019027b5/

假如允许跳转，部分浏览器会自动跳转到对应的笔记页面

原因

- 印象笔记 APP 注册了  https  scheme +  [app.yinxiang.com](http://app.yinxiang.com/)  域名 + 路径白名单  /shard/s.*/nl/.* （URIBrokerActivity）

<https://app.yinxiang.com/shard/s61/nl/11553084/723950cd-1cd0-4989-88b0-e302aff7a11e>

电脑可以实现跳转，手机不行

evernote://view/11553084/s61/723950cd-1cd0-4989-88b0-e302aff7a11e/723950cd-1cd0-4989-88b0-e302aff7a11e/

evernote://view/11553084/s61/723950cd-1cd0-4989-88b0-e302aff7a11e/nl/

evernote:///view/user id/shard id/note guid/client specific id/[linked notebook guid]/

手机可以，电脑不行

evernote:///view/11553084/s61/723950cd-1cd0-4989-88b0-e302aff7a11e/
