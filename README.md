# Maven项目管理工具说明

## 1、主要知识点

### Maven

#### 为什么学Maven

	在开发中经常需要依赖第三方的包，包与包之间的依赖关系，版本间兼容性问题。

#### 概述

	是当前最受欢迎的Java项目管理构建自动化综合工具。
	最强大的功能就是自动下载项目依赖库。
	Maven项目结构和内容在pom.xml中声明，pom.xml是整个Maven系统的基本单元
	Maven主要做了两件事:
		1. 统一了开发规范与工具
		2. 统一管理jar包

#### 名词解释

##### 1、POM

	Maven项目对象模型(POM-Project Object Model)，可以通过一小段描述信息来管理项目的构建，报告和文档的软件项目管理工具。

##### 2、坐标

    groupId , artifactId , version 三个元素是项目的坐标，唯一的标识这个项目。
    groupId 项目所在组，一般是组织或公司；
    artifactId 是当前项目在组中的唯一ID；
    version 表示版本，SNAPSHOT表示快照，表示此项目还在开发中，不稳定。
    groupId 和实际项目不一定是一一对应的，maven 有模块的概念，例如 spring-core, spring-context...；
    groupId 也不应该只对应公司或组织名，建议具体到项目名，因为公司或者组织下有多个项目，而artifactId只能代表模块名。
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.11</version>
      <scope>test</scope>
    </dependency>

##### 3、资源库

	本地资源库:用来存储所有项目的依赖关系(插件jar和其他文件）。
	默认的文件夹是“.m2”目录 Windows系统 – C:\Documents and Settings{your-username}\.m2
	中央存储库:当你建立一个 Maven 的项目，Maven 会检查你的 pom.xml 文件，以确定哪些依赖下载。
	首先，Maven 将从本地资源库获得 Maven 的本地资源库依赖资源，如果没有找到，然后把它会从默认的 Maven中央存储库–https://repo1.maven.org/maven2/查找下载。
	中央仓库资源：http://mvnrepository.com/ https://search.maven.org/

## 2、依赖
	官网：https://mvnrepository.com/
### MySQL
	mysql：https://mvnrepository.com/artifact/mysql/mysql-connector-java
### MyBatis
	mybatis：https://mvnrepository.com/artifact/org.mybatis/mybatis
### Spring
	context：https://mvnrepository.com/artifact/org.springframework/spring-context
### Log4j
	log4j：https://mvnrepository.com/artifact/log4j/log4j