#### 关于virtualenv

virtualenv是用来为一个应用创建一套“隔离”的Python运行环境。

#####一、使用方式：

（1）创建一个项目文件夹：mkdir myproject，进入该目录。

（2）创建一个独立的Python运行环境，命名为`venv`：virtualenv --no-site-packages venv。

加上参数--no-site-packages，已经安装到系统Python环境中的所有第三方包都不会复制过来，得到了一个不带任何第三方包的“干净”的Python运行环境。

（3）新建的Python环境被放到项目目录下的`venv`目录。

（4）使用命令，进入该环境：

```
source venv/bin/activate
```

有个`(venv)`前缀，表示当前环境是一个名为`venv`的Python环境。

在`venv`环境下，用`pip`安装的包都被安装到`venv`这个环境下，系统Python环境不受任何影响。

`venv`环境是专门针对`myproject`应用创建的。

（5）退出当前的`venv`环境，使用`deactivate`命令：

```
deactivate
```

原理：把系统Python复制一份到virtualenv的环境，用命令`source venv/bin/activate`进入一个virtualenv环境时，virtualenv会修改相关环境变量，让命令`python`和`pip`均指向当前的virtualenv环境。

##### 总结

Venv完全可以针对每个应用创建独立的Python运行环境，这样就可以对每个应用的Python环境进行隔离。

#####virtualenv为应用提供了隔离的Python运行环境，解决了不同应用间多版本的冲突问题。

















