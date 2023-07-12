起因：
新建一个Github账户，并新建一个远程仓库，使用 https git clone 到本地，记录以后的算法学习笔记，使用代理加速 Github

问题：
fatal: unable to access 'https://github.com/Psychorayda/DailyProblems.git/': Recv failure: Connection was reset

解决：
- 找到自己的代理软件，查到代理端口是 7890
- 打开 C:\\Users\\xxx\\gitconfig 文件
- 添加：
	 [http]
		 proxy = http://127.0.0.1:7890

思考：
- 为什么使用代理软件，修改代理端口后会出现此问题
	- 代理软件的功能原理是什么
- 为什么配置文件添加的是 http 配置，而 https 连接恢复可用
	- http 与 https 的区别是什么
- 可以考虑将 https clone 换成使用 ssh clone，如何实现
	- ssh 是什么，两种 clone 方式的区别是什么