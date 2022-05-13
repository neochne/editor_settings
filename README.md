idea 和 AS 的设置文件（包含快捷键、插件设置等），如果重装了，请直接导入

------

-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:5005

------

compile: pom 默认范围，编译范围依赖在所有的 classpath 中可用，同时它们也会被打包<br/>
provided: 不会被打包<br/>
runtime: 运行时需要<br/>
test: 测试阶段需要<br/>
system: 添加本地 jar 包，与 provided 类似，但你必须显式的提供一个对于本地系统中 JAR 文件的路径，即 <systemPath/> 元素，该范围是不推荐使用的<br/>
import: 仅支持在<dependencyManagement>中的类型依赖项上<br/>
  
------

[install local jar]<br/>
mvn install:install-file \
-Dfile=opc-ua-stack-1.3.344-173.jar \
-DgroupId=org.opcfoundation \
-DartifactId=opc-ua-stack \
-Dversion=1.3.344-173 \
-Dpackaging=jar
