# proudit-ansible

###wordpress.yml
---
##特徴
AmazonLinuxをベースにyum利用可能なミドルウェアパッケージで構成。
また、ほぼインストール直後のデフォルト配置の為、運用管理が容易。

利用OSはAmazonLinux(2015.03)を想定。

##構成(2015/08/17時点)
AmazonLinux 2015.03-release  
nginx 1.6.2  
php-fpm 5.3  
mysql 5.5  
wordpress 4.1.2  

##利用方法
1.環境変数を定義 

 [blog]　
 X.X.X.Xの部分を対象サーバIP or ホスト名に修正  
  
 [all:vars]  
 以下の下記情報を編集  
 　※印の箇所は変更必須項目  
  
>-Mysql Wordpress用　新規DB情報（指定した情報で初期構築します） 
>wp_db_name=wordpress  
>wp_db_user=wordpress  
>wp_db_password=Your-DB-Password  ※  

>-サイトURL　
>server_hostname=Your-Wordpress-Server-URL  ※  
>-Nginx DocumentRoot  
>webroot=/usr/share/nginx/html  

  
  
2.実行  
 $ansible-playbook -i hosts wordpress.yml  
