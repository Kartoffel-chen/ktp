# 简单课程管理系统

# 项目部署及运行

## 1.服务器软件
* 1.Tomcat(重要)   
* 2.MySql(重要)以及SQLYog(数据库操作软件)(可选)
----------------------------------
## 2.配置项目数据库环境
* 1.安装MYSQL以及SQLYog
* 2.使用SQLyog执行当前文件目录下的```数据库.sql```文件
* 2.tomcat配置环境变量(网上自己找教程,我记不得了)(下载时可选择安装版下载,会自动配置)
* 3.配置完成后
* 4.执行tomcat路径下的```bin\startup.bat```
* 5.打开浏览器输入```localhost:8080```,如果显示出一个有猫图片的页面说明tomcat部署成功
* 6.测试部署成功后,执行tomcat路径下的```bin\shutdown.bat```,关闭服务器

* [我的tomcat笔记](https://github.com/Kartoffel-chen/JavaWeb/blob/master/StudyNode/Tomcat&Servlet.md)

-----------------------------------

## 3.项目部署
* 1.部署到tomcat(方法一)
	* 解压当前文件所在目录下的```ktp.war```
	* 找到```ktp\WEB-INF\classes```目录下的```Jdbc.propertise```
	* 用记事本打开文件
	* 修改配置信息
	    * 你所创建的数据库名(URL)
	    * 数据库使用者(userName)
	    * 数据库密码(Password)
    * 找到tomcat安装路径
    * 打开```..\..\tomcat\webapps```
    * 将解压后的项目目录拷贝到tomcat路径下的webapps文件夹中
        * 注意解压的项目应该是一个名为```ktp```的单个文件,是将此文件夹拷贝到webapps中
    * 执行tomcat路径下的```bin\startup.bat```
    * 打开浏览器输入```localhost:8080/ktp/index.jsp```

* 2.方法二
    * 在运行tomcat服务器的情况下,将当前文件目录下的```ktp.war```直接拷贝到```../tomcat/webapps```目录下
    * 此时会自动解压出一个名为```ktp```的文件夹,打开文件夹
    * 找到```ktp\WEB-INF\classes```目录下的```Jdbc.propertise```
    * 用记事本打开文件
    	* 修改配置信息
    	    * 你所创建的数据库名(URL)
    	    * 数据库使用者(userName)
    	    * 数据库密码(Password)
    * 重启tomcat服务器
    * 打开浏览器输入```localhost:8080/ktp/index.jsp```
    
