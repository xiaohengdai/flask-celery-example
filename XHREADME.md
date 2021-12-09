worker启动命令:celery -A tasks worker -l INFO

在 Flask 中使用 Celery：http://www.pythondoc.com/flask-celery/first.html
celery简单入门:http://t.zoukankan.com/landpack-p-5555955.html
celery+rabbitmq消息队列使用笔记：https://blog.csdn.net/weixin_43262264/article/details/111573159
mac brew install rabbitmq 启动 报"Error when reading /Users/liyaochu/.erlang.cookie: eacces：https://blog.csdn.net/weixin_42047790/article/details/92798324
Celery的监控工具flower：https://blog.csdn.net/hhd1988/article/details/108759042

worker启动命令:
这个命令会开启一个在前台运行的 worker，解释这个命令的意义：

worker: 运行 worker 模块。
-A: –app=APP, 指定使用的 Celery 实例。
-l: –loglevel=INFO, 指定日志级别，可选：DEBUG, INFO, WARNING, ERROR, CRITICAL, FATAL

其它常用的选项：
-P: –pool=prefork, 并发模型，可选：prefork (默认，multiprocessing), eventlet, gevent, threads.
-c: –concurrency=10, 并发级别，prefork 模型下就是子进程数量，默认等于 CPU 核心数

