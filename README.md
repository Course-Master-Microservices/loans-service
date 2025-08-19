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

## Jib Configuration
```
<plugin>
    <groupId>com.google.cloud.tools</groupId>
    <artifactId>jib-maven-plugin</artifactId>
    <version>3.4.6</version>
    <configuration>
      <to>
        <image>myimage</image>
      </to>
    </configuration>
</plugin>
```

### Build Docker Image

```
mvn compile jib:build
```
or
```
mvn compile jib:dockerBuild
```

See the [Jib documentation](https://github.com/GoogleContainerTools/jib/tree/master/jib-maven-plugin#build-your-image)