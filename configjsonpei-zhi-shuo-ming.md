# weexplus.json配置说明

在configs下有个weexplus.json,请不要改变它的位置与名称，修改此文件之后必须重新打包才能生效

```js
{
  "schema":"",
  "debug":true, 是不是debug模式，是的话，会出现调试的button,进入app是也不会预加载preload的界面
  "showerror":true 是否显示错误提示
  "isPortriot":true,首页是竖屏，false未横屏
  "debugIp":"127.0.0.1", 调试用的ip，调试模式下扫码之后会自动保存那个ip,如果没有扫码过，则会使用次ip

  "releaseEntry":"app/entry.js",debug=false时加载的入口页面地址，
  "debugEntry":"http://192.168.199.248:9999/index.js",debug=true 入口页面地址，调试模式下会优先加载扫描之后保存的地址，如果没有才加载这个，
  "notifyEntry":'app/notifyEntry.js' 接收通知之后的处理页面，详情参考 模块->jpush->配置

  "static":
  {
    "umeng":
    {
      "ios":
      {
        "appkey":"5989828d717c191ffe0005c1"
      },
      "android":
      {
        "appkey":"598a841b2ae85b7e280008c5"
      }

    }


  },
  "platform":
  {
     "wx":
     {
       "appkey":"wxb9760e8d21f7979b",
       "appsecret":""
     },
     "qq":
     {
       "appkey":"1105821097",
       "appsecret":""
     },
     "weibo":
     {
       "appkey":"1105821097",
       "appsecret":"",
       "url":""
     }
  }

}
```



