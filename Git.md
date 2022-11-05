# git常用操作命令

clone仓库

```git
git clone https://gitee.com/fzy1999/GuoWang.git
```

添加全部修改

```
git add .
```

提交修改

```
git commit -m "修改日志"
```

push修改

```
git push
```

pull云端仓库

```
git pull
```



# git安装

# git 常用问题

## 1. git无法 clone

[(93条消息) 能访问github网页但git clone不下来_诺有缸的高飞鸟的博客-CSDN博客_github无法clone](https://blog.csdn.net/qq_41102371/article/details/122213285)

![在这里插入图片描述](https://img-blog.csdnimg.cn/71f7e4aa3da040f288aa89f867e2b3e5.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6K-65pyJ57y455qE6auY6aOe6bif,size_13,color_FFFFFF,t_70,g_se,x_16)

```
设置代理端口号
git config --global http.proxy 127.0.0.1:7890
查看端口设置
git config --list


```
## 2. git clone gitee无法下来
报错
```
fatal: unable to access 'https://gitee.com/fzy1999/GuoWang.git/': Failed to connect to 127.0.0.1 port 7890 after 2059 ms: Connection refused
```
### 1. 查看本地是否使用了代理
```
git config --global http.proxy 
```
### 2. 取消代理
```
git config --global --unset http.proxy
```

# git 分支处理



