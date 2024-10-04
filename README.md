# H2-Configuration-Spring
Configuracion para base de datos H2

# Dependencies
<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
			<scope>runtime</scope>
</dependency>
<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-security</artifactId>
</dependency>
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-web</artifactId>
</dependency>


# YAML Configuration
spring:
  jpa:
    # Provide database platform that is being used
    database-platform: org.hibernate.dialect.H2Dialect
    hibernate:
      # New database is created when app starts and destroyed when app stops
      ddl-auto: create-drop
    # Show sql when spring data jpa performs query
    show-sql: true
    properties:
      hibernate:
        # Format queries
        format_sql: true
  datasource:
    # URL connection to database (spring-security is database name)
    url: jdbc:h2:mem:spring-security
    # H2 SQL driver dependency
    driver-class-name: org.h2.Driver
    username: root
    password: 12345
