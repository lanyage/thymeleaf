# thymeleaf
spring boot采用thymeleaf

配置如下:

 ```
  spring.thymeleaf.prefix=classpath:/templates/
  spring.thymeleaf.suffix=.html
  spring.thymeleaf.mode=HTML5
  spring.thymeleaf.encoding=UTF-8
  spring.thymeleaf.content-type=text/html
  spring.thymeleaf.cache=false
  spring.resources.chain.strategy.content.enabled=true
  spring.resources.chain.strategy.content.paths=/**
```

例：在如下目录创建如下文件

spring-boot项目静态文件目录：/src/java/resources/static 
spring-boot项目模板文件目录：/src/java/resources/templates 
所以greeting.html文件在/src/java/resources/templates下。

```
<!DOCTYPE HTML>
<html xmlns="http://www.w3.org/1999/xhtml" xmlns:th="http://www.thymeleaf.org" >
  <head>
        <title>Getting Started: Serving Web Content</title>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
        <link th:href="@{/css/1.css}" rel="stylesheet"/>
  </head>
  <body>
        <p th:text="'Hello, ' + ${title}" /><br/>

        <script th:src="@{/js/jquery/1.11.0/jquery.js}"></script>
        <script>
            $(function(){
               alert("page load finish.");
            });
        </script>
  </body>
</html>
```

常用标签: `th:src="@{/js/jquery/1.11.0/jquery.js}"`，`th:href="@{/css/1.css}"`，`th:href="@{/hello}"`
