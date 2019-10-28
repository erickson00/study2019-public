# docker 中下载 mysql
docker pull mysql

#启动
docker run --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=six@Lacan -d mysql

#进入容器
docker exec -it mysql bash

#登录mysql
mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED BY 'Lzslov123!';

#添加远程登录用户
CREATE USER 'user1'@'%' IDENTIFIED WITH mysql_native_password BY 'six@Lacan';
GRANT ALL PRIVILEGES ON *.* TO 'user1'@'%';



# new mysql
docker pull mysql:5

docker run --name mysql5 -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 -d mysql:5
