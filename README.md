# padavan
padavan迅雷下载宝

##一、padavan项目地址
https://bitbucket.org/padavan/rt-n56u

##二、文件说明

1. 目录结构同原项目目录结构

2. 添加中文语言文件，修复页面显示问题

3. 机型适配文件

##二、使用方法

1. 编辑install.sh，修改DESTDIR为你的项目目录

 默认 `DESTDIR=/opt/rt-n56u`

2. 执行install.sh将文件复制到你的项目中

 `sh install.sh`

3. 编辑你的项目trunk目录下的config,复制到.config

 `cp config .config`

4. 编译项目

 `./build_firmware`

##三、机型适配文件说明

1. 机型适配文件位于`rt-n56u/trunk/configs/boards`目录下，每个文件夹对应一个机型，需手动将所需机型适配文件复制到项目对应文件夹下

2. 编辑你的项目trunk目录下的.config，修改对应配置
 
 例如：编译Xunlei 下载宝固件的配置

 `CONFIG_PRODUCT=MT7621`
 
 `CONFIG_FIRMWARE_PRODUCT_ID="XZB"`

##四、刷机说明
1. 使用Breed刷机，选择固件

 `/opt/rt-n56u/trunk/images/XZB_3.4.3.9-099.trx`

2. 接入路由器LAN口上，进入路由管理界面获取下载宝IP

3. 浏览器登录下载宝，账号密码：

 `admin`

 `admin`

4. telnet登录下载宝，账号密码同3

 `telnet 192.168.x.x`

##五、更新说明

 [2016-8-8] 仅在原项目上添加下载宝的编译board，关闭防火墙，开启telnet、ssh
##六、感谢

 感谢gorden5566的汉化padavan项目对本项目的帮助
