# Two parts, part 1 compile App.java
# Reference your image with "AS"
FROM mcr.microsoft.com/java/jdk:8-zulu-alpine AS mycompiler
COPY /app /usr/src/app
WORKDIR /usr/src/app
RUN javac App.java
CMD ["java", "App"]

# Second part: run compiled java application
FROM mcr.microsoft.com/java/jre:8-zulu-alpine
WORKDIR /app
# Copy from mycompiler image to working directory
COPY --from=mycompiler /usr/src/app .
CMD ["java", "App"]