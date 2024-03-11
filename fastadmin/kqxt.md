# fastadmin 制作的考勤统计系统
## 一、tp5的伪静态代码
    <IfModule mod_rewrite.c>
     RewriteEngine on
     RewriteBase /
     RewriteCond %{REQUEST_FILENAME} !-d
     RewriteCond %{REQUEST_FILENAME} !-f
     RewriteRule ^(.*)$ index.php?s=/$1 [QSA,PT,L]
    </IfModule>
## 二、前端使用后端生成的bootstraptable时需要将backend控制器中的相应变量和方法复制到frontend中。
    两个变量：
    protected $relationSearch = false;
    protected $dataLimit = false;
    两个方法：
    function buildparams
    function getDataLimitAdminIds
## 三、js中的注意事项
1.如果在html中使用组件时应加入 Form.api.bindevent($("form[role=form]")); 这段代码。
## 四、控制器相关
1.控制器中在数据库添加数据后，需加入
    $thsi->success();
这行语句，才会判断数据插入成功。
