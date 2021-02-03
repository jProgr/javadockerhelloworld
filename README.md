# Hello world with Java and docker

Just a simple program to test out Docker's multi-stage builds.

## Simple compile and run

```
docker run --rm -v "$PWD":/usr/src/app -w /usr/src/app openjdk:15 bash -c "javac HelloWorld.java && java HelloWorld"
```

## Compile and run using a Dockerfile

```
docker build -t singlefileapp -f SingleFile .
docker run --rm singlefileapp
```

## Compile and run using multi-stage builds

```
docker build -t multistageapp -f MultiStage .
docker run --rm multistageapp
```
