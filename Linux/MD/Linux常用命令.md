# Linux常用命令

这里记录一下平时开发工作中常用的Linux命令。

## 学习资料

- linux命令学习网站: [explainshell.com](https://explainshell.com/)

## 查找文件

- `find / -name filename.txt`: 根据名称查找/目录下的filename.txt文件。
- `find . -name "*.xml"`: 递归查找所有的xml文件
- `find . -name "*.xml" | xargs grep "hello world"`: 递归查找所有文件内容中包含hello world的xml文件
- `grep -H 'spring' *.xml`: 查找所以有的包含spring的xml文件
- `find ./ -size 0 | xargs rm -f &`: 删除文件大小为零的文件
- `ls -l | grep 'jar'`: 查找当前目录中的所有jar文件
- `grep 'test' d*`: 显示所有以d开头的文件中包含test的行。
- `grep 'test' aa bb cc`: 显示在aa，bb，cc文件中匹配test的行。
- `grep '[a-z]{5}' aa`: 显示所有包含每个字符串至少有5个连续小写字符的字符串的行。

## 查看文件，包含隐藏文件

- ls -al

## 查看一个程序是否运行

- `ps –ef | grep tomcat`: 查看所有有关tomcat的进程

## 终止线程

- `kill -9 19979`: 终止线程号位19979的线程

## 当前工作目录

- pwd

## 复制文件

- `cp source dest`: 复制文件
- `cp -r sourceFolder targetFolder`: 递归复制整个文件夹
- `scp sourecFile romoteUserName@remoteIp:remoteAddr`: 远程拷贝

## 创建目录

- mkdir newfolder

## 删除目录

- `rmdir deleteEmptyFolder`: 删除空目录
- `rm -rf deleteFile`: 递归删除目录中所有内容

## 移动文件

- mv /temp/movefile /targetFolder

## 重命令

- mv oldNameFile newNameFile

## 切换用户

- su -username

## 修改文件权限

- `chmod 777 file.java`: file.java的权限-rwxrwxrwx，r表示读、w表示写、x表示可执行

## 压缩文件

- tar -czf test.tar.gz /test1 /test2

## 列出压缩文件列表

- tar -tzf test.tar.gz

## 解压文件

- tar -xvzf test.tar.gz

## 查看文件头10行

- head -n 10 example.txt

## 查看文件尾10行

- tail -n 10 example.txt

## 查看日志类型文件

- `tail -f exmaple.log`: 这个命令会自动显示新增内容，屏幕只显示10行内容的（可设置）。

## 使用超级管理员身份执行命令

- `sudo rm a.txt`: 使用管理员身份删除文件

## 查看端口占用情况

- `netstat -tln | grep 8080`: 查看端口8080的使用情况

## 查看端口属于哪个程序

- lsof -i :8080

## 查看进程

- `ps aux | grep java`: 查看java进程
- `ps aux`: 查看所有进程

## 以树状图列出目录的内容

- tree a

## 文件下载

- wget http://file.tgz
- curl http://file.tgz

## 网络检测

- ping www.baidu.com

## 远程登录

- ssh userName@ip

## 打印信息

- `echo $JAVA_HOME`: 打印java home环境变量的值
