# SpringCloud 配置管理中心

### 配置服务的路径规则
 - /{application}/{profile}[/{label}]
 - /{application}-{profile}.yml
 - /{label}/{application}-{profile}.yml
 - /{application}-{profile}.properties
 - /{label}/{application}-{profile}.properties

&nbsp;

```bash
    # 下面通过具体例子说明以上url的意思, 如果我们的配置文件名称spring-cloud-config-prod.yml, 则其和URL中各个字段对应的值为:
    
    # application: spring-cloud-config
    # profile: prod | dev | answer | ...
    # label: 9500e50f08c43e3e4391175c8f6d5a326b11302f
    
    # 我们访问以下地址都可以访问到配置文件config-prod.yml和特定版本下此文件
    # http://127.0.0.1:8888/spring-cloud-config/prod 
    # http://127.0.0.1:8888/spring-cloud-config/prod/9500e50f08c43e3e4391175c8f6d5a326b11302f 
    # http://127.0.0.1:8888/spring-cloud-config-prod.yml 
    # http://127.0.0.1:8888/9500e50f08c43e3e4391175c8f6d5a326b11302f/spring-cloud-config-prod.yml 
    # http://127.0.0.1:8888/spring-cloud-config-prod.properties 
    # http://127.0.0.1:8888/9500e50f08c43e3e4391175c8f6d5a326b11302f/spring-cloud-config-prod.properties
```  

### 附录 - 参考文档
 - [x] [Spring Cloud 配置中心的基本用法](http://www.cnblogs.com/heqiyoujing/p/9445475.html)