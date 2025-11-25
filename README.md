 Banque Service – API GraphQL (Spring Boot)
 Description

Ce projet est un service Spring Boot (Java 17) exposant une API GraphQL pour gérer des comptes bancaires et leurs transactions. Il utilise une base H2 en mémoire afin de simplifier le développement.
Technologies utilisées

Java 17

Spring Boot 4

Spring Data JPA (H2 in-memory)

GraphQL

Maven (wrapper mvnw fourni)

Prérequis

JDK 17 installé

Windows PowerShell recommandé pour les commandes

Aucun besoin d’installer Maven (utiliser .\mvnw.cmd)

 Build (Windows PowerShell)
$env:MAVEN_OPTS='-Xmx512m'; & .\mvnw.cmd -DskipTests package

 Exécution
Mode développement
$env:MAVEN_OPTS='-Xmx512m'; & .\mvnw.cmd spring-boot:run

Exécution du JAR
java -jar target/banque-service-0.0.1-SNAPSHOT.jar

Changer le port
java -jar target/banque-service-0.0.1-SNAPSHOT.jar --server.port=8083

 Endpoint GraphQL

POST /graphql

 Configuration

Fichier : src/main/resources/application.properties

Paramètres :

server.port=8082
spring.datasource.url=jdbc:h2:mem:banque

 Tests
& .\mvnw.cmd test



<img width="1031" height="488" alt="image" src="https://github.com/user-attachments/assets/26953c36-866e-458a-b719-3ec1c1083097" />

