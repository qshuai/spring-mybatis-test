A spring mybatis usage example
===
##### Usage:

1. 创建数据库表：

   ```sql
   CREATE TABLE `user_info` (
     `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
     `username` varchar(20) NOT NULL,
     `password` varchar(40) NOT NULL,
     `created_time` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
     `updated_time` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
     PRIMARY KEY (`id`)
   ) ENGINE=InnoDB DEFAULT CHARSET=utf8;
   ```

2. 修改数据库配置文件：

   ```
   # 修改数据库DSN
   resources/mybatis-generator/generatorConfig.xml
   ```
   
3. 运行mybatis-generator

   ```shell
   mvn mybatis-generator:generate
   ```

##### Tips

- 如果出现以下错误，请在resources目录下添加develop目录

  ```
  [ERROR] Failed to execute goal org.mybatis.generator:mybatis-generator-maven-plugin:1.3.2:generate (default-cli) on project mybatis: Execution default-cli of goal org.mybatis.generator:mybatis-generator-maven-plugin:1.3.2:generate failed: Cannot resolve classpath entry: /Users/qshuai/project/java/mybatis/src/main/resources/develop -> [Help 1]
  ```

  