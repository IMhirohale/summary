### 一、有用的Linux命令：

##### 1.了解机器的连接数情况：

	netstat -n | grep XX	
	常用参数：-lnpta

多和grep和awk连接使用。

##### 2.从已经备份好的日志中查询数据：

查看bz2压缩日志：

```
bzcat file | grep 'xx' | wc -l

bzgrep 'xx' file | wc -l

less file | grep 'xx' | wc -l

```

查看gz压缩日志：

```
zcat

zgrep 

```

##### 3.查询线程数：

```
ps -eLf | wc -l

pstree -p | grep xx
```

##### 4.磁盘报警，清空某个最大文件：echo 

（1）找到改文件：
	find / -type f -name "*log*" | xargs ls -lSh | more
	du -ah | sort -rn | grep log | more

（2）将文件清空：
	echo "">a.log
#####5.显示文件，过滤注释：

```
grep -v "^#" file

sed -e '/^#/d' file

sed -n '/^[#]/!p' file
```



##### 6.磁盘IO异常排查

iotop -o

##### 7.服务CPU100%问题快速定位：

(1)找到最耗CPU的进程
	top
	top -c 显示进程运行信息列表
	键入P（大写p），进程按照CPU使用率排序

(2)找到最CPU的线程

	top -Hp 进程PID

(3)将线程PID转化成16进制
	printf "%x\n" 线程PID

(4)查看堆栈，看看线程在干嘛

	工具：pstack/jstack/grep

​	












