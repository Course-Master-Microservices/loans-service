# loans-service
Loans Microservice


## BuildPacks (Docker Image)

Buildpacks website - https://buildpacks.io

### Configs - pom.xml
```
<plugin>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-maven-plugin</artifactId>
    <configuration>
        <image>
            <name>luisalho/${project.artifactId}:s4</name>
        </image>
    </configuration>
</plugin>
```
### Build the image
```
mvn spring-boot:build-image
```

### Run the image
```
docker run -d -p 8080:8080 luisalho/loans-service:s4
```
