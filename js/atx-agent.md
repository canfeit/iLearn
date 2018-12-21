## 坑集

```js
// 接口: /packages/${packageName}/info
[
  {
    packageName: "io.appium.android.apis",
    name: "API Demos",
    activityName: "ApiDemos", //缺少包名，完整应为io.appium.android.apis.ApiDemos
    version: ""
  },
  {
    packageName: "io.appium.unlock",
    name: "Unlock",
    activityName: "Unlock", //缺少包名，完整应为io.appium.unlock.Unlock
    version: "2.0.0"
  },
  {
    packageName: "com.duokan.reader",
    name: "དཔེ་ཀློག", //藏语:阅读
    activityName: "com.duokan.reader.DkReaderActivity",
    version: "5.7.5"
  },
  {
    packageName: "com.duokan.phone.remotecontroller",
    name: "Mi রিমোট", //孟加拉语:远程
    activityName:
      "com.xiaomi.mitv.phone.remotecontroller.HoriWidgetMainActivityV2",
    version: "5.8.1"
  }
];
```
