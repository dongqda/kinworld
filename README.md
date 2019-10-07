# KinWorld-Knowledge In The World
세상의 모든 지식



## INDEX

+ [I. 개발환경 - Development Envirenment](#I-개발환경-Development-Environment)
+ [II. 설정 - Setup](#II-설정-Setup)
+ [III. 레이아웃-Layout](#III-레이아웃-Layout)



## I. 개발환경-Development Environment

![SpringBoot_Vue](md_pic/springBoot_vue.png)

+ IDE : Eclipse
+ SpringBoot 
+ Vue.js
+ Java
+ Gradle
+ MariaDB
+ Windows



## 설정-Setup

##### 1. Go to [SpringBoot Initializr](https://start.spring.io/)

![SpringBoot Initializr](md_pic/SpringBootInitializr.png)

##### 2. Add Dependencies

+ Spring Web
+ Thymeleaf

##### 3. Generate and Unzip

##### 4. Import Gradle Project 

![importGradle](md_pic/importGradle.png)

![basicGradlePj](md_pic/basicGradlePj.png)

##### 5.  Go to [node.js Download](https://nodejs.org/en/download/)

![downloadNodejs](md_pic/downloadNodejs.png)

##### 6.  명령프롬포트 실행 1

+ Windows 

```
  npm install -g vue-cli
```


##### 7. 환경변수 설정

+ 시스템 PATH에 ```C:\Users\유저명\AppData\Roaming\npm``` 경로 추가

##### 8.  명령프롬포트 실행

+ Move Gradle Project Directory

```
  cd kinworld
```

+ frontend 이름으로 webpack 생성

```
  vue init webpack frontend
```
+ 상세설정
```
  bash$ vue init webpack frontend 
    
  ? Project name frontend
  ? Project description A Vue.js project 
  ? Author dglee012@gmail.com 
  ? Vue build standalone 
  ? Install vue-router? Yes 
  ? Use ESLint to lint your code? Yes 
  ? Pick an ESLint preset Airbnb 
  ? Set up unit tests Yes 
  ? Pick a test runner karma 
  ? Setup e2e tests with Nightwatch? Yes 

      vue-cli · Generated "vue-test". 

      To get started: 

          cd vue-test 
          npm install 
          npm run dev 

      Documentation can be found at https://vuejs-templates.github.io/webpack
```

##### 9. Edit frontend\config\index.js 

+ webpack 빌드 시 index.html생성 위치를 Gradle Project 안의 resource\template로 변경(line 46)

```
...
    build: {
      // Template for index.html
      index: path.resolve(__dirname, '../../src/main/resources/templates/index.html'),

      // Paths
      assetsRoot: path.resolve(__dirname, '../../src/main/resources/static'),
      assetsSubDirectory: '',
      assetsPublicPath: '/',
...
```

##### 10. Build

```
    cd frontend
    npm install
    npm run build
```

##### 11. Add Dependencies in resource\application.properties

```
...
	runtimeOnly("org.mariadb.jdbc:mariadb-java-client")
...
```

##### 12. Maria DB Setting

```
    #datasource
    spring.datasource.driverClassName=org.mariadb.jdbc.Driver
    spring.datasource.url=jdbc:mariadb://localhost:3306/kinworld
    spring.datasource.username=root
    spring.datasource.password=password
```

##### 13. Go to http://localhost:8080/

![startVue](md_pic/startVue.png)

# III. 레이아웃 - Layout

##### 1.  Use vue-tree-nav

###### npm install --save vue-tree-nav

#####  ![](C:\workSpace\kinworld\md_pic\navmenu.gif)

