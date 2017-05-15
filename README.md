# Socket Sever

@(php)[Socket,php,sever,workerman]

## WorkerMan套件

WorkerMan-Windows
[https://github.com/walkor/workerman-for-win](https://github.com/walkor/workerman-for-win)

## 簡易的監聽器

```php
<?php
use Workerman\Worker;
require_once './Workerman/Autoloader.php';
$Listener= new Worker("tcp://127.0.0.1:8000");
$Listener->count = 10;
$Listener->onMessage = function($connection, $data)

    $connection->send('Hello' . $data);
  
};
Worker::runAll();
```
將以上代碼儲存，並放置於WorkerMan資料夾外
## 執行方法

請在打開命令提示字元，並下指令

    php filename.php
## SVN

    svn/SeverZion/phpsocket

