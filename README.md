# Jump
🚀 🔥 🌈 基于webman使用 KingBes/Jump 包实现的页面跳转解决方案
# 页面跳转 composer
```shell
composer require kingbes/jump
```

返回成功页面
```php
use Kingbes\Jump\Jump; //引入

class IndexController extends Jump
{
    public function index(Request $request)
    {
        // @param mixed $msg — 提示信息
        // @param string $url — 跳转的URL地址
        // @param mixed $data — 返回的数据
        // @param integer $wait — 跳转等待时间
        // @param array $header — 发送的Header信息
        return $this->success("ok"); //返回成功页面
    }
}
```
![alt 成功页面](/截图success.png)
ajax请求则返回json

返回失败页面
```php
use Kingbes\Jump\Jump; //引入

class IndexController extends Jump
{
    public function index(Request $request)
    {
        // @param mixed $msg — 提示信息
        // @param string $url — 跳转的URL地址
        // @param mixed $data — 返回的数据
        // @param integer $wait — 跳转等待时间
        // @param array $header — 发送的Header信息
        return $this->error("no"); //返回失败页面
    }
}
```
![alt 失败页面](/截图error.png)
ajax请求则返回json

自定义返回模板,配置config/plugin/kingbes/jump/app.php
```php
<?php
return [
    'enable' => true,
    'jump' => BASE_PATH . '/vendor/kingbes/jump/src/jump.html' // 配置模板
];
```
