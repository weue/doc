# android 打包

打包前，请先配置好android原生环境，（android,studio,adb环境变量），最好先使用android studio打成功一次

1.修改configs/weexplus.json debug=false  关闭debug模式  showerror=false 关闭报错提示

 2.修改签名文件（只用设置一次），生成一个签名文件，名字改成keystore.jks,并覆盖（项目名称/platforms/android/项目名称/keystore.jks），

修改（项目名称/platforms/android/项目名称/gradle.properties）里面的keyAlias，keyPassword，storePassword为你创建签名文件时设置的值

2.执行weexplus publish android，等待执行完毕，不报错的话，会弹出有apk的文件夹

