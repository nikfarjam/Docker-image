# Docker-image

## Run command
1. Open JDK 14.0.1
   
   ```docker run -it nikfarjam/java:14.0.1``` 
2. Open JDK 11.0.2
    
    ```docker run -it nikfarjam/java:11.0.2 bash``` 

## Build commands
1. Open JDK 14.0.1

    ```docker build -t open-jdk:14.0.1 -f ./java/Dockerfile-java-14 .```
2. Open JDK 11.0.2
   
   ```docker build -t open-jdk:11.0.2 -f ./java/11/Dockerfile .```
