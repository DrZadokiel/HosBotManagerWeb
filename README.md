# 简介

基于一个叫`hoshinoV2服务开关网页版.zip`的东西改出来的玩意儿，web管理hoshino的service开关的东西。

## 安装

前略装好hoshinobot

整个`bot_manager_web`目录塞进`hoshino/modules`目录下面

在`hoshino/config`目录下塞个叫`bot_manager_web.py`的文件，里面写下面这些变量，让模块可以正常被使用。

```python
import os
from .__bot__ import HOST, PORT

ICP_CONTENT = os.environ.get('ICP_CONTENT') if os.environ.get('ICP_CONTENT') else ''
PUBLIC_ADDRESS = os.environ.get('PUBLIC_ADDRESS') if os.environ.get('PUBLIC_ADDRESS') else f"http://{HOST}:{PORT}"
PASSWORD = os.environ.get('BOT_MANAGER_WEB_PASSWORD') if os.environ.get('BOT_MANAGER_WEB_PASSWORD') else '987654321'
```

PS: 至于为啥要用os.environ，因为习惯性扔进容器里所以需要环境变量赋值┓( ´∀` )┏

## 使用

访问`https://bcr.yourdomain.com/manage`

输入上面文件里设定的密码登录（至于为啥没有用户名，反正只有一个人会去登录的东西要什么用户名！）

然后是进入服务里管理群功能开关，还是进入群列表管理服务功能开关，正常人都能看懂吧。

PS: 注销按钮我也不知道为啥要存在，想了想也没啥意义就没做了。

PPS: 还有部分垃圾文件懒得看了，体积也不算太过夸张懒得抽了，有人有空可以抽一抽。

## 图示

![图1](Thumbnail/1.png)
![图2](Thumbnail/2.png)
![图3](Thumbnail/3.png)
![图4](Thumbnail/4.png)
![图5](Thumbnail/5.png)
