# Java HttpClient for Spring Web Client Boot Starter
[![javadoc](https://javadoc.io/badge2/com.integralblue/java-httpclient-webclient-spring-boot-starter/javadoc.svg)](https://javadoc.io/doc/com.integralblue/java-httpclient-webclient-spring-boot-starter)
![Maven Central](https://img.shields.io/maven-central/v/com.integralblue/java-httpclient-webclient-spring-boot-starter)
![GitHub](https://img.shields.io/github/license/candrews/java-httpclient-webclient-spring-boot-starter)

The Java HttpClient for Spring Web Client Boot Starter provides a quick and easy way to use [Java 11's HttpClient](https://docs.oracle.com/en/java/javase/11/docs/api/java.net.http/java/net/http/HttpClient.html) as [Spring WebClient's](https://docs.spring.io/spring-boot/docs/2.3.4.RELEASE/reference/htmlsingle/#boot-features-webclient) client HTTP connector.

By default, [Spring WebClient will try to use Reactor Netty then Jetty Client as it's client HTTP connector](https://docs.spring.io/spring-boot/docs/2.3.4.RELEASE/reference/htmlsingle/#boot-features-webclient-runtime). This starter will instead use Java 11's HTTP client.

Benefits of using this starter include:
* not needing additional dependencies such as on Netty or Eclipse
* getting the benefits and features of Java's built in HttpClient
* Being able to use tooling for Java's HttpClient, such as [HttpClientMock](https://github.com/PGSSoft/HttpClientMock)

## Using This Starter
To use this starter, you must:
* Be using Java 11 (or later)
* Be using Spring Boot 2.3.0 (or later)

Add a dependency on this starter your dependency manager of choice, making sure to use the latest version: ![Maven Central](https://img.shields.io/maven-central/v/com.integralblue/java-httpclient-webclient-spring-boot-starter)

For Gradle:
```groovy
dependencies {
	runtimeOnly 'com.integralblue:java-httpclient-webclient-spring-boot-starter:VERSION'
}
```

For Maven:
```xml
<dependency>
	<groupId>com.integralblue</groupId>
	<artifactId>java-httpclient-webclient-spring-boot-starter</artifactId>
	<version>VERSION</version>
    <scope>runtime</scope>
</dependency>
```

That's it - Spring Boot autoconfiguration will take care of the rest.

## Future of This Starter
Eventually, a future version of Spring will likely include this functionality. Follow [the Pull Request for JDK 11 HttpClient integration with WebClient](https://github.com/spring-projects/spring-framework/pull/23432/) for more information.

## Developing the Starter
This project requires Java 11 (or later).
Import this Gradle project using your IDE of choice.
Or, if you don't want to use an IDE, you can run the project from the command line: `./gradlew build` The test suite will run and a jar will be output at [build/libs/](build/libs/).

### Eclipse
The Project Lombok Eclipse integration must be setup. See the Eclipse instructions on [Project Lombok's site](https://projectlombok.org/features/index.html).