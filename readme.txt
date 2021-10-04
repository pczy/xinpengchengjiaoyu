1，服务器搭建
	LEMP（LNMP）
2，修改默认启动首页
	cd /etc/nginx/conf.d
	root@vultr:/etc/nginx/conf.d# cp http.conf http.conf.bak
	root@vultr:/etc/nginx/conf.d# nano http.conf
	root@vultr:/etc/nginx/conf.d# cd /usr/sbin

	修改前：
	server {
	        listen 80 default_server;
	        server_name _;

	        root /usr/share/nginx/html;
	        index index.php index.html;

	修改后：
	server {
	        listen 80 default_server;
	        server_name _;

	        root /usr/share/nginx/html;
	        index index.php index.html index.htm;


	root@vultr:/usr/sbin# ./nginx -s reload