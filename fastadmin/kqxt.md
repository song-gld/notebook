# fastadmin 制作的考勤统计系统
## 一、tp5的伪静态代码
    <IfModule mod_rewrite.c>
     RewriteEngine on
     RewriteBase /
     RewriteCond %{REQUEST_FILENAME} !-d
     RewriteCond %{REQUEST_FILENAME} !-f
     RewriteRule ^(.*)$ index.php?s=/$1 [QSA,PT,L]
    </IfModule>
