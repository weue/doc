# umanalyse\(友盟统计\)

**首次使用请执行weexplus plugin add umanalyse**

有支付和登录2个功能，请务必在首页调用regist方法，初始化微信

### api

```
(请务必在首页调用此方法，初始化微信)
/**appkey
**初始化
**/
 initUM(appkey)

/**页面统计
 beginPage(name)
 /**页面结束
 endPage(name)
 /**触发事件
 event(name)
 /**开始事件
 beginEvent(name)
 /**结束事件
 endEvent(name)
```

### demo

初始化微信模块，请在app的首页进行

```js
var um=weex.requireModule('umanalyse')
var appId=""
um.initUM('你的appKey')

```

微信支付

```js
var wechat=weex.requireModule('wechat')
var p={}
p.appId = "wxd930ea5d5a258f4f";
p.partnerId = "1900000109";
p.prepayId= "1101000000140415649af9fc314aa427",;
p.packageValue = "Sign=WXPay";
p.nonceStr= "1101000000140429eb40476f8896f4c9";
p.timeStamp= "1398746574";
p.sign= "7FFECB600D7157C5AA49810D2D8F28BC2811827B";
wechat.pay(p,(res)=>{

     if(res.errCode==0)
     {
        //success
     }
})
```

微信登录

```js
var wechat=weex.requireModule('wechat')
var p={}
p.state = "xxxxx";
p.scope = "xxxxx";

wechat.login(p,(res)=>{

     if(res.errCode==0)
     {
          //success
         var code=res.authCode; //do something


     }
})
```



