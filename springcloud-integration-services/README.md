# SpringCloud多组件集成案例配置中心

 - **订单系统**： scis-order-service
   - **开发环境**: [scis-order-service-dev.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/scis-order-service-dev.yaml)
   - **生产环境**: [scis-order-service-prod.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/scis-order-service-prod.yaml)
 
 - **库存系统**： scis-inventory-service
   - **开发环境**: [scis-inventory-service-dev.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/scis-inventory-service-dev.yaml)
   - **生产环境**: [scis-inventory-service-dev.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/scis-inventory-service-prod.yaml)
 
 - **仓储系统**： scis-warehousing-service
   - **开发环境**: [scis-warehousing-service-dev.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/scis-warehousing-service-dev.yaml)
   - **生产环境**: [scis-warehousing-service-dev.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/scis-warehousing-service-prod.yaml)
 
 - **积分系统**： scis-integral-service
   - **开发环境**: [scis-integral-service-dev.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/scis-integral-service-dev.yaml)
   - **生产环境**: [scis-integral-service-dev.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/scis-integral-service-prod.yaml)

 - **默认配置**
   - **开发环境**: [application-dev.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/application-dev.yaml)
   - **生产环境**: [application-prod.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/application-prod.yaml)
   - **开发 & 生产环境**: [application.yaml](https://github.com/AnswerAICode/spring-cloud-config/blob/master/springcloud-integration-services/application.yaml)
  
&nbsp;   
   
### 举例说明
   
```properties
    # 配置文件名称
    application: scis-order-service

    # 如果不设置此值, 则系统设置此值为 spring.profiles.active 属性的值
    profile: prod

    # 配置文件所在分支, 可以使用之前的版本. 默认值可以是git label, branch name or commit id. 可以使用多个Label, 多个Label可以使用逗号分隔
    label: master
```
 - /{application}/{profile}[/{label}]
   - http://localhost:7072/scis-order-service/prod/master
   - http://localhost:7072/scis-order-service/prod
  
 - /{application}-{profile}.yml
   - http://localhost:7072/scis-order-service-prod.yaml
   
 - /{label}/{application}-{profile}.yml
   - http://localhost:7072/master/scis-order-service-prod.yaml
   
 - /{application}-{profile}.properties
   - http://localhost:7072/scis-order-service-prod.properties
   
 - /{label}/{application}-{profile}.properties
   - http://localhost:7072/master/scis-order-service-prod.properties   