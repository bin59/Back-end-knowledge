### jdk11 以上没有 jre 文件

![没jre.png](https://cdn.jsdelivr.net/gh/bin59/imgs@main/%E6%B2%A1jre.png)

在 jdk 安装目录下 cmd:

```
bin\jlink.exe --module-path jmods --add-modules java.desktop --output jre
```

![jre.png](https://cdn.jsdelivr.net/gh/bin59/imgs@main/jre.png)

