# Java Spring Boot CI Demo

A minimal Spring Boot web application that returns `Hello, Spring Boot!` at `/`.

## Run locally

```bash
mvn spring-boot:run
```

Then open `http://localhost:8080`.

## Build

```bash
mvn clean package
```

The runnable JAR is written to `target/demo-0.0.1-SNAPSHOT.jar`.

## Build the Docker image

Build the JAR first, then run:

```bash
docker build -t java-springboot-ci-demo .
docker run --rm -p 8080:8080 java-springboot-ci-demo
```

`buildspec.yml` defines an AWS CodeBuild build using Java 17.
