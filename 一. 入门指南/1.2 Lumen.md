### Lumen使用laravel-modules



Lumen没有vendor发布，若要使用laravel-modules，必须手动设置。

在根目录中创建一个config文件夹，并将`vendor/nwidart/laravel modules/config/config.php`复制到config文件夹中并命名为modules.php

```bash
mkdir config
cp vendor/nwidart/laravel-modules/config/config.php config/modules.php
```

在Lumen中，默认情况下 laravel-modules 使用的path.public是未定义的，所以需要在加载服务提供程序之前注册path.public

```php
$app->bind('path.public', function() {
 return __DIR__ . 'public/';
});
```

然后在bootstrap/app.php中加载配置和注册服务提供程序(ServiceProvider)

```php
$app->configure('modules');
$app->register(\Nwidart\Modules\LumenModulesServiceProvider::class);
```

