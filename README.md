# Vprofile
sample web-application

<?xml version="1.0"?>

-<project xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd" xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<modelVersion>4.0.0</modelVersion>

<groupId>com.visualpathit</groupId>

<artifactId>VProfile</artifactId>

<packaging>war</packaging>

<version>1.0</version>

<name>Visualpathit VProfile Webapp</name>

<url>http://maven.apache.org</url>


-<properties>

<spring.version>4.2.0.RELEASE</spring.version>

<spring-security.version>4.0.2.RELEASE</spring-security.version>

<spring-data-jpa.version>1.8.2.RELEASE</spring-data-jpa.version>

<hibernate.version>4.3.11.Final</hibernate.version>

<hibernate-validator.version>5.2.1.Final</hibernate-validator.version>

<mysql-connector.version>5.1.36</mysql-connector.version>

<commons-dbcp.version>1.4</commons-dbcp.version>

<jstl.version>1.2</jstl.version>

<junit.version>4.10</junit.version>

<logback.version>1.1.3</logback.version>

<maven.compiler.source>1.8</maven.compiler.source>

<maven.compiler.target>1.8</maven.compiler.target>

</properties>


-<dependencies>


-<dependency>

<groupId>org.springframework</groupId>

<artifactId>spring-web</artifactId>

<version>${spring.version}</version>

</dependency>


-<dependency>

<groupId>org.springframework</groupId>

<artifactId>spring-webmvc</artifactId>

<version>${spring.version}</version>

</dependency>


-<dependency>

<groupId>org.springframework.security</groupId>

<artifactId>spring-security-web</artifactId>

<version>${spring-security.version}</version>

</dependency>


-<dependency>

<groupId>org.springframework.security</groupId>

<artifactId>spring-security-config</artifactId>

<version>${spring-security.version}</version>

</dependency>


-<dependency>

<groupId>org.hibernate</groupId>

<artifactId>hibernate-validator</artifactId>

<version>${hibernate-validator.version}</version>

</dependency>


-<dependency>

<groupId>org.springframework.data</groupId>

<artifactId>spring-data-jpa</artifactId>

<version>${spring-data-jpa.version}</version>

</dependency>


-<dependency>

<groupId>org.hibernate</groupId>

<artifactId>hibernate-entitymanager</artifactId>

<version>${hibernate.version}</version>

</dependency>


-<dependency>

<groupId>mysql</groupId>

<artifactId>mysql-connector-java</artifactId>

<version>${mysql-connector.version}</version>

</dependency>


-<dependency>

<groupId>commons-dbcp</groupId>

<artifactId>commons-dbcp</artifactId>

<version>${commons-dbcp.version}</version>

</dependency>


-<dependency>

<groupId>javax.servlet</groupId>

<artifactId>jstl</artifactId>

<version>${jstl.version}</version>

</dependency>


-<dependency>

<groupId>junit</groupId>

<artifactId>junit</artifactId>

<version>${junit.version}</version>

<scope>test</scope>

</dependency>


-<dependency>

<groupId>org.mockito</groupId>

<artifactId>mockito-core</artifactId>

<version>1.9.5</version>

<scope>test</scope>

</dependency>


-<dependency>

<groupId>org.springframework</groupId>

<artifactId>spring-test</artifactId>

<version>3.2.3.RELEASE</version>

<scope>test</scope>

</dependency>


-<dependency>

<groupId>javax.servlet</groupId>

<artifactId>javax.servlet-api</artifactId>

<version>3.1.0</version>

<scope>provided</scope>

</dependency>


-<dependency>

<groupId>ch.qos.logback</groupId>

<artifactId>logback-classic</artifactId>

<version>${logback.version}</version>

</dependency>


-<dependency>

<groupId>org.hamcrest</groupId>

<artifactId>hamcrest-all</artifactId>

<version>1.3</version>

<scope>test</scope>

</dependency>

</dependencies>


-<build>


-<plugins>


-<plugin>

<groupId>org.eclipse.jetty</groupId>

<artifactId>jetty-maven-plugin</artifactId>

<version>9.2.11.v20150529</version>


-<configuration>

<scanIntervalSeconds>10</scanIntervalSeconds>


-<webApp>

<contextPath>/</contextPath>

</webApp>

</configuration>

</plugin>

<!-- CODE COVERAGE -->



-<plugin>

<groupId>org.jacoco</groupId>

<artifactId>jacoco-maven-plugin</artifactId>

<version>0.7.2.201409121644</version>


-<executions>


-<execution>

<id>jacoco-initialize</id>

<phase>process-resources</phase>


-<goals>

<goal>prepare-agent</goal>

</goals>

</execution>


-<execution>

<id>jacoco-site</id>

<phase>post-integration-test</phase>


-<goals>

<goal>report</goal>

</goals>

</execution>

</executions>

</plugin>

</plugins>

</build>

</project>
