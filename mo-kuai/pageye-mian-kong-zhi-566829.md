# page

页面控制器

## api

```js
/**重新渲染本页面
reload()



/**启用双击退出
doubleBack()



/**是否拦截返回键（针对android）
enableBackKey(enbale)


/**拦截返回键触发的回调
setBackKeyCallback(callback)


/**退出应用（android有效）
exit()

/**设置启动的主页面 url(相对地址，支持root:写法)
setMainPage(url)


/** url(相对地址，支持root:写法) success 渲染成功之后的回调，如果新页面跳转后有明显的闪烁，可以调用此方法先预加载一下
                 ，当然跳转的逻辑得放到这个succes的回调函数里去
preRender(url,success)

/**设置键盘状态（只android有效）
/**mode adjust_nothing,adjust_pan,adjust_resize
setKeyboardMode(mode)


/**
* 模拟home键被按下，app回到主页（ios会真的退出app）
**/
pressHome()

/**获取最顶层页面的url,同步返回
getTopPage()
```

# Demo

```js
var page=weex.requireModule("page")
page.reload();
page.doubleBack();

page.enableBackKey(false);
page.setBackKeyCallback(()=>{
 page.enableBackKey(true);

})

page.exit();
```



