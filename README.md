# NotejsStudy
Nodejs学习，用Notejs+MongoDB搭建项目

1.安装nodejs。下载nodejs安装文件，这里安装的版本是：node-v6.9.4-x64.msi。
  安装完毕后，打开控制台，输入：node -v，如果，展示版本信息，则说明安装成功。
  
  安装完nodejs后，可以在控制台中，输入：npm install -g express。express是node的一种框架，npm是node的模块包管理程序，安装完node后，就已经安装好了      npm，可以在控制台输入：npm -v，查看安装的npm版本。
  注意，此处的npm可以选择国内的淘宝镜像
  npm install -g cnpm --registry=https://registry.npm.taobao.org
  
2.安装mongodb。下载mongodb的安装文件
  安装完毕后，启动mongodb。新建一个空文件夹，这里，我就新建了E:\mdData这个文件夹。
  打开cmd，进入mongodb安装的路径下，进入到bin路径下，
  在控制台执行：mongod.exe --dbpath E:\mdData，此控制台不关闭，再打开一个新的控制台，也进入到bin目录下，执行mongo.exe，连接上数据库。
  这里，连接上了测试的数据库test。若要退出，则输入exit。
  
  或者：以管理员打开cmd后，执行：
  mongod --dbpath="D:\MongoDB\Server\3.2\data" --logpath="D:\MongoDB\Server\3.2\log\log.txt" --install --serviceName MongoDB    --serviceDisplayName MongoDB
  注：dbpath，是mongodb的数据路径，logpath，是日志路径。
  这里新建了一个服务，MongoDB，可以在控制面板中，看到这个服务，可以进行启动与关闭操作。
  启动mongodb时，需要先启动服务，然后在控制台中，进入安装的bin路径下，输入mongo.exe进行启动。
 
 3.mongodb的简单语句
   创建项目数据库 use nodestudy
   创建用户、密码 db.createUser({user:"...",pwd:"...",roles:["readWrite"]})，roles为readWrite，表示有读写功能。
   创建users表： db.createCollection("users") 
   往users表中插入数据： db.users.insert({userName:"admin",password:"11"})
   查询users表的数据： db.users.find()
   删除users表的某条数据： db.users.remove({userName=""});
   修改users表的某条数据： db.users.update();
 
 4.下载mongoose
   在项目中（注意，是项目文件中），控制台打开到对应的node项目，执行npm install mongoose，下载mongoose。下载成功后，项目中
