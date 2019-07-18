A spring mybatis usage example
===

1. 创建数据库表：

   ```sql
   CREATE TABLE `user_info` (
     `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
     `username` varchar(20) NOT NULL,
     `password` varchar(40) NOT NULL,
     `created_time` timpstamp NOT NULL DEFAULT current_timestamp,
     `updated_tiome` timestamp NOT NULL on update current_timestamp,
     PRIMARY KEY(`id`)
   ) ENGINE=InnoDB DEFAULT CHARSET=utf8;
   ```

   