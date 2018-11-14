# laravel5_admin

#### 项目介绍
基于laravel 5.1 框架的后台基础系统。包括登录验证、用户管理，修改密码，用户权限，用户组权限，功能管理，系统日志，文件上传、工作流。目前还附加了简单的blog功能。可以快速基于此系统进行laravel5的快速开发，免去每次都写一次后台基础的痛苦

#### 软件架构
laravel5.1 + mysql5.5


#### 安装教程

1. 建立数据库名为：mrblog
2. 把包目录下的mrblog.sql导到库mrblog中，建议使用mysql source命令导入
3. 复制doc/.env文件到根目录下，修改数据库连接为你的信息,这里是（host=localhost,username=root,pwd=root）
4. 默认使用的域名为admin.opcache.net和www.opcache.net，如果你需要修改，那么修改文件nginx或apache配置文件

apache的vhosts.conf文件

<VirtualHost *:80>
    ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "E:/phpStudy/PHPTutorial/WWW/laravel51/public"
    ServerName laravel51.com
    ErrorLog "logs/dummy-host2.example.com-error.log"
    CustomLog "logs/dummy-host2.example.com-access.log" common
</VirtualHost>

5.配置你的域名并指向目录public
6.默认后台密码，其实是md5，你可以改你想要的
####
帐号：admin
密码：11
7.要注意的是mysql_model不能开启严格模式
####
建议设置为：sql_mode=NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION

8.如果你使用blog的搜索功能的话，你需要安装php扩展sphinx，同时安装sphinx服务
####
sphinx 主要用于博客的搜索
自行安装与配置sphinx（如果你使用blog的搜索功能的话），这是建议的配置 doc/sphinx.conf
在mrblog.sql文件里面也有相关文章，安装后再内容管理中可以查看。

9.环境要求：
####
至少满足laravel 5.1框架的要求。
####
PHP >= 5.5.9
OpenSSL PHP 扩展
PDO PHP 扩展
Mbstring PHP 扩展
Tokenizer PHP 扩展
此外测试mysql5.5通过。或使用可以兼容的版本。

10. 配置虚拟主机 laravel51.com
####
<VirtualHost *:80>
####
    ServerAdmin webmaster@dummy-host2.example.com
####
    DocumentRoot "E:/phpStudy/PHPTutorial/WWW/laravel51/public"
####
    ServerName laravel51.com
####
    ErrorLog "logs/dummy-host2.example.com-error.log"
####
    CustomLog "logs/dummy-host2.example.com-access.log" common
####
</VirtualHost>


11. 添加host
####
127.0.0.1  laravel51.com

#### 使用说明

在浏览器输入 http://laravel51.com
