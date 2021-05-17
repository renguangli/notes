## Tomcat
## Tomcat 传特殊字符返回 400 错误
Tomcat Url 中只允许包含

- a-zA-Z
- 0-9
- **- _ . ~** 4个特殊字符以及所有保留字符

RFC3986中指定了以下字符为保留字符

- ! * ’ ( ) ; : @ & = + $ , / ? # [ ])

解决办法：

- 1、使用低版本的Tomcat
- 2、对相应的特殊字符进行URL编码
- 3、在Tomcat的配置文件 catalina.properties 最后一行添加允许的特殊字符 tomcat.util.http.parser.HttpParser.requestTargetAllow=|{}
- 4、将请求参数放在请求体中
- 5、**relaxedPathChars && relaxedQueryChars**

```
或者添加 relaxedPathChars 属性
<Connector port="8080" protocol="HTTP/1.1" connectionTimeout="20000" relaxedPathChars="[]" relaxedQueryChars="[]" redirectPort="8443" />
```