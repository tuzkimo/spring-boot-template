# spring-boot-template

## 快速搭建
start.spring.io

## 命令
`mvn spring-boot:run` 运行项目
`mvn package` 打包项目

## 修改端口
application.properties 增加 `server.port={端口号}`

## 热加载
1. 添加 `spring-boot-start-devtool` 依赖
```
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-devtools</artifactId>
  <scope>runtime</scope>
</dependency>
```
2. `spring-boot-maven-plugin` 启用 `fork` 设置
```
<plugin>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-maven-plugin</artifactId>
  <configuration>
    <fork>true</fork>
  </configuration>
</plugin>
```

## 解决 idea 不能热加载
1. `Settings` - `Build, Execution, Deployment` - `Compiler`, 勾上 `Build project automatically`
2. `Ctrl + Shift + Alt + /` - `registry...`, 勾上 `compiler.automake.allow.when.app.runing`
