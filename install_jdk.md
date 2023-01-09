1.下载
```bash
wget https://repo.huaweicloud.com/java/jdk/8u202-b08/jdk-8u202-linux-x64.tar.gz
```
2.安装
（1）创建安装目录
```bash
mkdir /usr/local/java/
```
（2）解压至安装目录
```bash
tar -zxvf jdk-8u202-linux-x64.tar.gz -C /usr/local/java
```
配置环境变量
打开文件
```bash
vim /etc/profile
```
在末尾添加
```bash
export JAVA_HOME=/usr/local/java/jdk1.8.0_202
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
export PATH=${JAVA_HOME}/bin:$PATH
```
保存并退出
```bash
:wq
```
使环境变量生效
```bash
source /etc/profile
```
添加软链接
```bash
ln -s /usr/local/java/jdk1.8.0_202/bin/java /usr/bin/java
```
检查
```bash
java -version
```
