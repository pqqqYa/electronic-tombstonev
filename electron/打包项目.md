# 问题

打包项目大概率会遇到网络问题

# 解决

参考[这篇文章](https://www.cnblogs.com/DevFans/p/14402077.html)，下载对应的软件包放置于缓存文件夹

1.直接下载对应版本winCodeSign、nsis与nsis-reso到本地

2.下载后放于对应目录`C:\Users\ASUS\AppData\Local\electron\Cache`和`C:\Users\ASUS\AppData\Local\electron-builder\Cache`

3.在Cache目录下创建nsis和winCodeSign

4.将对应的压缩包拷贝到目录中去完整解压,最终效果如下：