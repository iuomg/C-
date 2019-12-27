# C++大作业报告



#### 步骤一：将github上的nebula克隆到本地:
`git clone https://github.com/iuomg/nebula.git`

克隆了好多次都出现了error：提前读取到eof

处理方法：最后直接从github上下载压缩包解压完成
####步骤二：进入到nebula目录中并安装依赖：

`cd nebula && ./build_dep.sh`

#### 步骤三：应用source ~/.bashrc修改

`source ~/.bashrc`

#### 步骤四：构建 Debug 版本
`mkdir build && d build`

`cmake ..`

`make`

`sudo make install`

遇到的问题：
- 1. cmake ..之后报错error：缺少cmake

下载完cmake之后再一次报错error： not findBzip2

下载完Bzip2之后又缺少文件double conversion上网搜索没有找到结局方案

最后重新安装系统解决cmake问题

- 2. make的时候缺少文件

更新软件包 `sudo apt-get update`解决

- 3. make100%结束后出现错误`/usr/bin/ld: cannot find Scrt1.o: No such file or directory`

解决方案：在 ~/.bashrc 末添加如下行

`export LIBRARY_PATH=/usr/lib/x86_64-linux-gnu:$LIBRARY_PATH`

然后应用~/.bashrc修改
`source ~/.bashrc`

#### 步骤五 设置本地登录github账户
- 设置账户名：`git config --global user.name iuomg`

- 设置github邮箱地址：`git config --global user.email xxx@qq.com`

- 生成ssh key：`ssh-keygen -t rsa -C xxx@qq.com`

- github上添加ssh key：
将目录/root/.ssh/id_rsa.pub的信息输入到github网页上个人设置页面中的SSH and GPG Keys中





