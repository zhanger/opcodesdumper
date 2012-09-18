Opcodes Dumper
================

##介绍
一个用来查看PHP code 以及opcode_handler的小工具.

##截图
![小截图](http://ww3.sinaimg.cn/large/a74ecc4cjw1dwzbmmlzi9j.jpg)

##相关原理

[使用PHP Embed SAPI实现Opcodes查看器](http://www.laruence.com/2008/09/23/539.html)      

[由opcodes找到其处理函数的方法](http://zhangabc.com/2011/08/27/find-opcodes-to-implements/)

原Goole Code 代码地址： http://code.google.com/p/opcodesdumper/    

##自行判断php的版本
目前支持php 5.3和php 5.4 ，分别对应的handlers文件为: 
```
php 5.3 : php_5_3_opcodes_handlers
php 5.4 : php_5_4_opcodes_handlers
(当然 ，你可以自定义为)
php 6.1 : php_6_1_opcodes_handlers
```

##安装示例

###1. 编译PHP源码：
```
./configure --prefix=/home/tony/php310 --enable-debug --enable-embed
make && make install
```

###2. 复制PHP链接库：
```
sudo cp /home/tony/php310/lib/libphp5.so /lib/libphp5.so
```

###3. 修改Makefile中关于PHP路径的定义

```
(vi Makefile)
PHPPATH=/home/tony/php310
```

###4. 执行make 

###5. 测试
```
./opd test.php
```


