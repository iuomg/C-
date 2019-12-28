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

#### 步骤六 修改代码
- 在/home/iu/nebala/src/中的CmdProcessor.cpp最后添加返回系统时间的函数。

#### 步骤七 提交PR
- `git remote -v`
- `git remote rm origin`
- `git remote add origin https://github.com/iuomg/nebula.git`
- 创建分支myfeature `git checkout -b myfeature`
- add修改文件 `git add src/console/CmdProcessor.cpp`
- 添加说明 `git commit -m "time output change"`
- 关联上游分支并且上传新建的myfeature分支 `git push --set-upstream origin myfeature`
- 提交PR
**遇到的问题：** push完之后 网页没有出现new pr

切换分支之后可以提交pr但是修改后的代码没有被accpeted

### 总结：
不得不说，这是一个充实的学期，遇见c++ primer，遇见wumin，真快乐！虽然课堂上人丁越来越稀少，但是每周二345节课我始终坚守在6教北306教室，即使听着听着偶有神游。通过本学期吴敏老师的熏陶，我了解了github、markdown，同时也了解了更多关于行业方面的信息，这让我着实超越了不选吴敏老师课的同学们一大截啊！虽并未完全领会其精髓，但是对c++函数、容器等的应用还是精进了。更为难得的是，此次的c++大作业让我基本掌握了Ubuntu的基本操作，同时也通过相互之间的答疑解惑与同学之间建立了更加友好的关系。以后我会更加努力学习，不断锻炼自己，让自己逐渐充实，富有知识的芬芳馥郁！



