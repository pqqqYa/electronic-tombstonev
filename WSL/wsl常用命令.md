## 关闭

~~~cmd
wsl --shutdown
~~~

## 查看列表

~~~cmd
wsl --list -v
~~~

## 导出子系统

~~~cmd
wsl --export <子系统名字> <压缩包名字"unbuntu.tar">
~~~

## 导入虚拟机

~~~cmd
wsl --import <新子系统名字> <解压路径> <压缩包完整路径"D:\\unbuntu.tar">
~~~

## 移动文件

~~~cmd
sudo cp /mnt/c/Users/ASUS/Downloads/hadoop-2.7.1.tar.gz /home/hadoop/Downloads
~~~