# spring-cloud-vue
---

## Project Description
* cloud-vue is a front-end and back-end separation framework based on springcloud + mybatis + vue family buckets (Vue2.x + Vue-router2.x + Vuex).
* The framwork uses Maven to modularize the project to improve the ease of development and scalability of the project.
* The system includes distributed configuration, eureka registration center, service center, zipkin distributed tracking, etc.
* Each module serves multiple system deployments and is registered to the same eureka cluster service registration center for cluster deployment.

## The main function
* Login, logout
* Change password, remember password
* Menu management
* System parameters
* Authority node
* Job management
* Department management
* User group management
* User Management

## Dependence
### java backend dependencies
* Maven 3
* Java 8
* MySQL 5.7
* Docker 1.13.1 (不是必须的)

### vue2 front-end environment
* node >= 6.9.0
* npm  >= 3.0.0
* vue 				<https://vuefe.cn/v2/guide/>
* element-ui@1.1.3  <http://element.eleme.io/1.1/#/zh-CN/component/installation>
* axios  			<https://github.com/mzabriskie/axios>
* fontawesome 		<http://fontawesome.io/icons/>
* js-cookie  		<https://github.com/js-cookie/js-cookie>
* lockr  			<https://github.com/tsironis/lockr>
* lodash  			<http://lodashjs.com/docs/>
* moment  			<http://momentjs.cn/>

## Engineering description
* cloud-config-server：Configuration Center.
* cloud-eureka-server：Registration Center.
* cloud-simple-service：Custom microservice.
* cloud-zipkin-ui：Distributed link call monitoring system, which aggregates call delay data of various business systems to achieve link call monitoring and tracking.
* cloud-vue : vue（Vue2.x + Vue-router2.x + Vuex) front-end project.

## Deployment Instructions
 * Import cloud-vue.sql from cloud-simple-service to the mysql database.
 * Modify the database configuration files in cloud-config-repo and cloud-zipkin-ui
 * Packaging command mvn package -DskipDockerBuild
 * Start cloud-eureka-server-1.0.0.jar、cloud-config-server-1.0.0.jar、cloud-zipkin-ui-1.0.0.jar、cloud-simple-service-1.0.0.jar, respectively.
 * Port: configuration center port (1111), registration center (8888), rest service (80), zipkin service (9012), UI front end (8080), if the ports conflict, please modify it yourself.

## Effect picture
![Login](./pic/登录.png)

![Department Management](./pic/部门管理.png)

![Department Management](./pic/部门管理.png)

![Menu Management](./pic/菜单管理.png)

![Job Management](./pic/岗位管理.png)

![Permission Rule Management](./pic/权限规则管理.png)

![User Group Management](./pic/用户组管理.png)

![Registration Center](./pic/注册中心.png)

![swagger](./pic/swagger.png)

![zipkin](./pic/zipkin.png)

## License
cloud-vue is based on apache2.0 <http://www.apache.org/licenses/LICENSE-2.0>


