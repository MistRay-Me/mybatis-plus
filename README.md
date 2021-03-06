<p align="center">
  <a href="https://github.com/baomidou/mybatis-plus">
   <img alt="Mybatis-Plus-Logo" src="https://raw.githubusercontent.com/baomidou/logo/master/mybatis-plus-logo-new-mini.png">
  </a>
</p>

<h2 align="center">MyBatis-Plus</h2>

<p align="center">
  Born To Simplify Development
</p>

<p align="center">
  <a href="http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22com.baomidou%22%20AND%20a%3A%22mybatis-plus%22">
    <img alt="maven" src="https://img.shields.io/maven-central/v/com.baomidou/mybatis-plus.svg?style=flat-square">
  </a>

  <a href="https://www.apache.org/licenses/LICENSE-2.0">
    <img alt="code style" src="https://img.shields.io/badge/license-Apache%202-4EB1BA.svg?style=flat-square">
  </a>
</p>

---

## What is MyBatis-Plus?

MyBatis-Plus is an powerful enhanced toolkit of MyBatis for simplify development. This toolkit provides some efficient, useful, out-of-the-box features for MyBatis, use it can effectively save your development time.

## Links

-   [Documentation](https://mybatis.plus)
-   [Samples](https://github.com/baomidou/mybatis-plus-samples.git)
-   [Showcase](https://github.com/baomidou/awosome-mybaits-plus)

## Features

-   Fully compatible with MyBatis
-   Auto configuration on startup
-   Out-of-the-box interfaces for operate database
-   Powerful and flexible where condition wrapper
-   Multiple strategy to generate primary key
-   Lambda-style API
-   Almighty and highly customizable code generator
-   Automatic paging operation
-   SQL Injection defense
-   Support active record
-   Support pluggable custom interface
-   Build-in many extensions

## Getting started

-   Create a basic Maven or Gradle spring boot project
-   Add MyBatis-Plus dependency
    -   Maven:
        ```xml
        <dependency>
            <groupId>com.baomidou</groupId>
            <artifactId>mybatis-plus-boot-starter</artifactId>
            <version>3.0.6</version>
        </dependency>
        ```
    -   Gradle
        ```groovy
        compile group: 'com.baomidou', name: 'mybatis-plus-boot-starter', version: '3.0.6'
        ```
-   Modify mapper file extends BaseMapper interface
    ```java
    public interface UserMapper extends BaseMapper<User> {

    }
    ```
-   Use it
    ```java
    List<User> userList = userMapper.selectList(
            new QueryWrapper<User>()
                    .lambda()
                    .ge(User::getAge, 18)
    );
    ```
    SQL executed
    ```sql
    SELECT * FROM user WHERE age >= 18
    ```

## Reporting bugs


## License

MyBatis-Plus is under the Apache 2.0 license. See the [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0) file for details.
