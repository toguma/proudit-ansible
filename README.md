# proudit-ansible
##利用方法

###wordpress.yml
*hostsを編集

 [blog]　
 X.X.X.Xの部分を対象サーバIP or ホスト名に修正

 [all:vars]
 以下の下記情報を編集
 　※印の箇所は変更必須項目
 　それ以外の箇所は必要に応じて編集

>-Mysql Wordpress用　新規DB情報（指定した情報で初期構築します）
>wp_db_name=wordpress
>wp_db_user=wordpress
>wp_db_password=Passwd$1

>-サイトURL　※
>server_hostname=Your-Wordpress-Server-URL
>-Nginx DocumentRoot
>webroot=/usr/share/nginx/html

*実行
 $ansible-playbook -i hosts wordpress.yml
