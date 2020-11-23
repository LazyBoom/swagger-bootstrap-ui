::: danger 特别注意
1、目前已经发行的Knife4j版本，Knife4j本身已经引入了springfox，开发者在使用时不用再单独引入Springfox的具体版本，否额会导致版本冲突。另外在网关层聚合(例如gateway)时，必须禁用Knife4j的增强模式

2、使用Knife4j2.0.6及以上的版本，Spring Boot的版本必须大于等于`2.2.x`
:::

Java开发使用`Knife4j`目前有一些不同的版本变化,详见[版本说明](changelog.md)，主要如下：

1、如果开发者继续使用OpenAPI2的规范结构，底层框架依赖springfox2.10.5版本，那么可以考虑`Knife4j`的2.x版本

```xml
<dependency>
    <groupId>com.github.xiaoymin</groupId>
    <artifactId>knife4j-spring-boot-starter</artifactId>
    <!--在引用时请在maven中央仓库搜索2.X最新版本号-->
    <version>2.0.8</version>
</dependency>
```

2、如果开发者使用OpenAPI3的结构，底层框架依赖springfox3.0.0,可以考虑`Knife4j`的3.x版本

```xml
<dependency>
    <groupId>com.github.xiaoymin</groupId>
    <artifactId>knife4j-spring-boot-starter</artifactId>
    <!--在引用时请在maven中央仓库搜索3.X最新版本号-->
    <version>3.0.2</version>
</dependency>
```

3、如果开发者底层框架使用的是`springdoc-openapi`框架,则需要使用`Knife4j`提供的对应版本,需要注意的是该版本没有`Knife4j`提供的增强功能，是一个纯Ui。

```xml
<dependency>
    <groupId>com.github.xiaoymin</groupId>
    <artifactId>knife4j-springdoc-ui</artifactId>
    <!--在引用时请在maven中央仓库搜索3.X最新版本号-->
    <version>3.0.2</version>
</dependency>
```

