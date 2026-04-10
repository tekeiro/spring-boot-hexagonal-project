# Spring Boot - Hexagonal Architecture Template

It's a maven archetype to create a multimodule Spring Boot project following Hexagonal architecture.

Structure is as following:

* **domain**: All domain model classes
* **application**: Uses cases
* **boot**: It holds all Configuration beans, Spring boot main app class, src/main/resources and so on
* **infa**
  * **inbound**
    * **api-rest**: Spring MVC maven module with all Rest Controllers
  * **outbound**
    * **client-rest-external-service**: maven module sample to connect to an external service
* **utils**
  * **commons**: Utils classes to use in the others modules

 
## Install locally
```shell
mvn install
```

## Generate a new project
```shell
mvn archetype:generate \
  -DarchetypeGroupId=com.example \
  -DarchetypeArtifactId=spring-boot-hexagonal-archetype \
  -DarchetypeVersion=1.0.0-SNAPSHOT \
  -DgroupId=com.mycompany \
  -DartifactId=my-service \
  -Dversion=1.0.0-SNAPSHOT
```