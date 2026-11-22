# Spring Boot + NGINX demo

Requirements: JDK 17+ and Maven 3.6.3+; Docker Desktop for the container setup.

## Build the executable Spring Boot JAR

From this directory run:

```bash
mvn clean package
```

The executable JAR will be created at:

`target/spring-nginx-demo-0.0.1-SNAPSHOT.jar`

Run it locally with:

```bash
java -jar target/spring-nginx-demo-0.0.1-SNAPSHOT.jar
```

Then open `http://localhost:8080/` or `http://localhost:8080/info`.

## Run with Docker and NGINX

```bash
mvn clean package
docker compose up -d --build
```

Open `http://localhost:8080/` or `http://localhost:8080/info`. Requests go through NGINX to the Spring Boot container.

Stop and remove the containers/network with:

```bash
docker compose down
```
