![](https://box.kancloud.cn/5a0aaa69a5ff42657b5c4715f3d49221) 
ThinkPHP 5.1（LTS） —— 12载初心，你值得信赖的PHP框架
===============

[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/top-think/framework/badges/quality-score.png?b=5.1)](https://scrutinizer-ci.com/g/top-think/framework/?branch=5.1)
[![Build Status](https://travis-ci.org/top-think/framework.svg?branch=master)](https://travis-ci.org/top-think/framework)
[![Total Downloads](https://poser.pugx.org/topthink/framework/downloads)](https://packagist.org/packages/topthink/framework)
[![Latest Stable Version](https://poser.pugx.org/topthink/framework/v/stable)](https://packagist.org/packages/topthink/framework)
[![PHP Version](https://img.shields.io/badge/php-%3E%3D5.6-8892BF.svg)](http://www.php.net/)
[![License](https://poser.pugx.org/topthink/framework/license)](https://packagist.org/packages/topthink/framework)

## CGLand
> 运行环境要求

   + 运行环境要求PHP7.3+、mysql 8.0.4、redis 3.2+、nginx 1.10+
   + web目录下的代码可自行搭建LNMP开发环境
   + 推荐使用[docker](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe)快速搭建


### 快速搭建localhost环境：
    docker-compose up

### docker常用命令
+ docker-compose up 运行容器
+ docker-compose down 停止容器

### 数据库

>创建迁移文件

    php think migrate:create Users
 
>运行迁移文件

    php think migrate:run
    
>创建数据填充

    php think seed:create PersonnelFile 

>执行数据填充

    php think seed:run
    php think seed:run -s Users

### 控制器

>新建资源控制器

     php think make:controller auth/AuthRule 

>新建控制器

     php think make:controller auth/AuthRule --plain

>新建 验证器类

     php think make:validate  index/User
  
### 模型
  
>新建模型(模型尽量放在common模块)
  
     php think make:model common/School
     
### 中间件
  
>新建中间件
  
     php think make:middleware Auth  
     
### 缓存
>生成路由映射缓存
   
    php think optimize:route


>默认生成应用的配置缓存文件，调用后会在runtime目录下面生成init.php文件，生成配置缓存文件后，应用目录下面的config.phpcommon.php以及tags.php不会被加载，被runtime/init.php取代。
  
    php think optimize:config  
    
>生成类库映射文件  
   
    php think optimize:autoload 
         
### 清除缓存
  
>不带任何参数调用clear命令的话，会清除runtime目录下文件
  
     php think clear  
     
>清除数据缓存目录
   
     php think clear --cache 
  
>清除路由缓存
   
     php think clear --route   
     
>清除日志目录
   
     php think clear --log   
     
       
   
### 快速生成模块

>可以用来自动生成需要的模块及目录结构和文件等
  
     php think build --module test     php think build --module test        
    

     
### 查看thinkphp版本

    php think version
    
### swoole

>启动
  
     php think swoole:server start      
     
>如果需要使用守护进程方式运行，可以使用
  
     php think swoole:server start -d   
     
>命令
     
      php think swoole:server [start|stop|reload|restart]    
     
     
         

