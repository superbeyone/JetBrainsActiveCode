插件安装

插件中心 File -> Settings -> Install Plugin From Disk，通过磁盘安装插件

检查一下javaagent是否配置成功？

```
## 以windows为例，正确配置如下：-javaagent:C:\Users\Public\.BetterIntelliJ\BetterIntelliJ-版本号.jar

## 以unix为例，正确配置如下：-javaagent:${HOME}//.BetterIntelliJ/BetterIntelliJ-版本号.jar
```

注意：破解补丁的位置不要更换，不要删除，否则激活之后还会失效

打不开IDEA？
由于你安装了其它的破解补丁，需要去看看idea64.exe.vmoptions的配置对不对？

建议去掉之前的 -javaagent 的配置。然后，再根据上面的教程安装咱们的破解补丁~

vmoptions找不到？打开IDEA，菜单栏:Help -> Edit Custom Properties，进行修改即可


---

- [reset scripts](reset scripts/)

- [插件](BetterIntelliJ.zip)

- [激活码](license.md)