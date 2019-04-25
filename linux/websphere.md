# WAS 节点不同步解决办法一

## 依次关闭server、node、dmgr
> /opt/IBM/WebSphere/AppServer/profiles/AppSrv02/bin/stopServer.sh  server1 --servername<br>
> /opt/IBM/WebSphere/AppServer/profiles/AppSrv02/bin/stopNode.sh<br>
> /opt/IBM/WebSphere/AppServer/bin/stopManager.sh

## 删除 wstemp, temp 和 config/temp 文件夹下面的临时文件
> /opt/IBM/WebSphere/AppServer/profiles/Dmgr01/temp、wstemp、tranlog<br>
> /opt/IBM/WebSphere/AppServer/profiles/Dmgr01/config/temp

## 同步节点
> syncNode.sh hostName 8879 -username appname -password 000000

## 依次启动 dmgr、node、server
> /opt/IBM/WebSphere/AppServer/bin/startManager.sh<br>
> /opt/IBM/WebSphere/AppServer/profiles/AppSrv02/bin/startNode.sh<br>
> /opt/IBM/WebSphere/AppServer/profiles/AppSrv02/bin/startServer.sh  server1


