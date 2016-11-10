<img src="http://139.129.42.87/wp-content/uploads/2016/02/php.jpg" alt="php" width="300" height="439" class="aligncenter size-full wp-image-124" />

通常情况下，我们建立PHP脚本做后台任务处理时，我们不会让一个PHP进程一直运行下去（考虑到PHP稳定性的问题），而是不断产生新的进程，并让老进程结束。这里我们给出了几个在Linux系统下实现PHP多进程的方法。


## 1. pcntl[^1]

pcntl_fork()是php自带的多进程实现方法。

`说明：当使用pcntl_fork()时，从当前程序的位置产生子进程，子进程和父进程都从当前位置执行，不同的是pcntl_fork()的返回值（对于父进程返回值是当前子进程的进程号，对于子进程返回的是0，如果fork失败返回-1）`

### 常用函数：

* pcntl_fork()
安装信号处理器
* pcntl_signal(int $signo, callback $handler)
子进程退出之前调用次函数，回收子进程资源，防止出现僵尸进程。
* pcntl_wait(); 

```php
function signal_handler($sig)
{
    switch($sig)
    {
        case SIGCHLD: 
            pcntl_wait($status); 
            break;
        case SIGTERM:
             // 处理SIGTERM信号
             exit;
             break;
        case SIGHUP:
             //处理SIGHUP信号
             break;
        case SIGUSR1:
             echo "Caught SIGUSR1...\n";
             break;
        default: echo "error\n";
    }
}

function fork()
{
    pcntl_signal(SIGCHLD, "signal_handler");
    $pid = pcntl_fork();
    if($pid > 0)
    {
        //主进程
    }
    else if($pid = 0)
    {
        //子进程
        //为了防止子进程继续执行,将子进程退出
        exit(0);
    }
    else
    {
        //建立子进程失败
        //$pid = -1
        echo "fork fail!\n";
    }
}

```

## 2. linux crontab

以下我们要执行的脚本，运行10分钟后这个任务脚本进程结束。

```php
//这是要执行的脚本"a.php"
$startTime = time();
while(1) 
{
    if (time() - $startTime > 600) 
    {
        break;
    }
 
    // ... Do SomeThing
}

```
使用以下方法，我们可以每两分钟建立一个这样的脚本。

```c
#范例
02 * * * * /usr/local/bin/php a.php
```

## 3. php exec函数

也可以使用PHP函数exec()执行shell命令建立任务脚本进程.

```php
$startTime = time();
while(1)
{
 	if (time() - $startTime > 600) 
    {
        break;
    }
	exec("nohup /user/local/bin/php a.php >> /dev/null &");
}

```

## 4. Python 实现

我们还可以通过Python执行任务脚本,这个方法可以严格限制系统中建立的任务脚本数, **在实际应用中，我们目前使用该方法。**

```python

#!/usr/bin/env python
import os
import time
import threading
def exec_php():
    os.system("/user/local/bin/php a.php")
if __name__ == '__main__':
    while 1:
        count = len(threading.enumerate());
        # 系统最多存在10个任务脚本
        if count<=10:
            t = threading.Thread(target=exec_php)
            t.setDaemon(True)
            t.start()
            # 每三分钟建立一个这样的任务脚本
            time.sleep(3)

```

## 参考文献
[^1]: http://www.cnblogs.com/yjf512/p/3436141.html




