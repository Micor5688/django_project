# my_blog
### 利用python开发属于自己的博客网站
### 开发环境搭建
### 本教程的开发环境为：

## Win 10（64位）
## Python 3.7.0
## Django 2.2
## 为了避免开发环境不同而导致的错误，建议读者使用相同的版本。

## 注意：不少读者反馈 Django 2.1 版本在后面章节中会遇到 main.auth_user_old 的报错。这是版本兼容问题造成的。因此强烈建议读者使用其他小版本号，如 Django 2.2。

# 安装Python
## python的安装为比较简单，首先找到Python官方网站，选择python3.7的windows版本，下载并安装。

## 安装时注意勾选添加python到环境变量中。如果没有或者漏掉这一步，请安装完毕后自行添加。

# windows上安装python3教程以及环境变量配置

# 安装完成后打开命令行，输入python -V，系统打印出python的版本号，说明安装成功了：

## C:\Users\dusai> python -V
## Python 3.7.0
## 配置虚拟环境
## 虚拟环境（virtualenv，或venv ）是 Python 多版本管理的利器，可以使每个项目环境与其他项目独立开来，保持环境的干净，解决包冲突问题。你可以将虚拟环境理解为一个隔绝的小系统。

## 从Python3.3版本开始就自带了虚拟环境，不需要安装，配置一下就可以用了。

## 新建一个文件夹，教程中为django_project。进入此文件夹：

## E:\>cd django_project
## E:\django_project>
## 输入配置venv的命令，其中的env为虚拟环境的放置目录：

## E:\django_project> python -m venv env  
## 创建完成后，输入env\Scripts\activate.bat，即可进入虚拟环境：

## E:\django_project> env\Scripts\activate.bat
## (env) E:\django_project>
## 盘符前有(env)标识说明进入venv成功。

# 安装Django
## 在虚拟环境下，输入命令pip install django==2.2：

## (env) E:\django_project> pip install django==2.2

## Collecting django==2.2
  ### Using cached 
  ### ...
  ### ...
## Successfully installed django-2.2

## (env) E:\django_project>
## 通过指令pip install django==2.2来安装和教程相同版本的 Django。

## 系统打印出以上文字表示Django安装成功了。

## 这里一定要指定版本号，否则就默认安装 Django 3 了。新手不要纠结版本问题，先跟着教程把基础掌握好。

# 创建Django项目
## 还是在虚拟环境下，在django_project文件夹中创建Django项目：

## (env) E:\django_project>django-admin startproject my_blog
## 查看django_project文件夹，发现多了my_blog文件夹，其结构应该是这样：
### 
### my_blog
### │  db.sqlite3
### │  manage.py
### │
### └─my_blog
###    │  settings.py
###    │  urls.py
###    │  wsgi.py
###    └─ __init__.py
### 这就是我们刚创建出来的项目了。
###

## 运行Django服务器
## 非常幸运，Django自带一个轻量的Web开发服务器，也被叫做“runserver”。

## 开发服务器是为了让你快速开发Web程序，通过它可以避开配置生产环境的服务器的繁琐环节。

## 开发服务器会自动的检测代码的改变，并且自动加载它，因此在修改代码后不需要手动去重启服务器，非常的方便。

## 要运行这个django服务器，首先要进入my_blog文件夹，即含有manage.py文件的那个：

## (env) E:\django_project>cd my_blog
## (env) E:\django_project\my_blog>
## 输入命令python manage.py runserver：

## (env) E:\django_project\my_blog>python manage.py runserver
## Performing system checks...

## System check identified no issues (0 silenced).

## You have 15 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
## Run 'python manage.py migrate' to apply them.
## August 20, 2018 - 17:32:34
## Django version 2.2, using settings 'my_blog.settings'
## Starting development server at http://127.0.0.1:8000/
## Quit the server with CTRL-BREAK.
## 系统打印出这些信息，说明服务器启动成功了，打开chrome浏览器，输入http://127. 0.0.1:8000/ ，即倒数第2排信息提示我们的服务器地址。看到下面的界面：

