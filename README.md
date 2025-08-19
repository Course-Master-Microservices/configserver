# configserver
Spring Cloud Config

## RabbitMQ

### Install RabbitMQ

```bash
# latest RabbitMQ 4.x
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:4-management
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