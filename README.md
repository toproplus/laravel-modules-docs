# LARAVEL-MODULES  `v6`

> [laravel-modules中文(简体)文档](https://github.com/toproplus/laravel-modules-docs) 

[nwidart/laravel-modules](https://github.com/nWidart/laravel-modules) 是一个基于laravel 的composer包，创建该包是为了便于模块化管理大型 laravel 应用。每个模块相当于一个 laravel "框架"，它含有视图views、控制器controllers和模型models。laravel版本支持： >= laravel5.8.x

这个包是基于 [pingpong/modules](https://github.com/pingpong-labs/modules) 重新整理发布的版本，因其已不再维护更新。应用案例：[AsgardCMS](https://asgardcms.com/)

请在此链接中了解为什么要使用此包：[Writing modular applications with laravel-modules](https://nicolaswidart.com/blog/writing-modular-applications-with-laravel-modules)

```
小提示:
如果你想从旧版本升级到V6, 执行命令: php artisan module:v6:migrate
```



#### 快速示例

执行命令`php artisan module:make Blog`生成你的第一个模块，将会生成下面的结构：

```
app/
bootstrap/
vendor/
Modules/
  ├── Blog/
      ├── Assets/
      ├── Config/
      ├── Console/
      ├── Database/
          ├── Migrations/
          ├── Seeders/
      ├── Entities/
      ├── Http/
          ├── Controllers/
          ├── Middleware/
          ├── Requests/
      ├── Providers/
          ├── BlogServiceProvider.php
          ├── RouteServiceProvider.php
      ├── Resources/
          ├── assets/
              ├── js/
                ├── app.js
              ├── sass/
                ├── app.scss
          ├── lang/
          ├── views/
      ├── Routes/
          ├── api.php
          ├── web.php
      ├── Repositories/
      ├── Tests/
      ├── composer.json
      ├── module.json
      ├── package.json
      ├── webpack.mix.js
```

