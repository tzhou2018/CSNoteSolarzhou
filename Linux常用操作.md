# Linux常用操作
<!-- GFM-TOC -->
    * [查看线程数](#查看线程数)
## 查看线程数
1. ps 后面加上H，能打印某个进程的所有线程
`ps hH p {pid} | wc -l`
2. top命令后面跟-H，会打印出所有线程列表
```
top -H
top -H -p {pid}
```
## 查看端口占用
1. 查看进程号
`ps -A | grep java`
2. 查看端口占用
```
lsof -i:端口号
netstat -tunlp | grep 端口号
```
## 查看tcp使用
1. `netstat -t`
## cpu使用
`top`
## 查看前几行后几行命令
查看/etc/profile的前10行内容，应该是：
`head -n 10 /etc/profile`、
查看/etc/profile的最后5行内容，应该是：
`tail  -n 5 /etc/profile`

## 参考文章
[linux参考文章--菜鸟编程](https://www.runoob.com/w3cnote/linux-check-port-usage.html)
[linux查看文件前几行和后几行的命令-csdn](https://blog.csdn.net/zmx19951103/article/details/78575265)