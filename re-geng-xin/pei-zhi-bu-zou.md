# 热更新配置步骤

1. 准备更新包：

   运行：weex-builder  src native/dist --min

   将configs/weexplus.json jsVersion的值加一个版本，然后copy config.json 到dist下

     copy dist 目录，修改复制后的dist目录名为app,zip格式压缩app文件夹

   将app.zip丢到服务器上

2.数据库配置

```
  打开hotupdate表

  新增一条记录

  按字段要求填写

  url填写刚那个app.zip

  js_version填写为之前修改的值
```



