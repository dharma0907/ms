# here we are writting multi stage docker file because to to build the code we need maven
FROM maven as build
WORKDIR /app
COPY . .
RUN mvn install
# above command will help us to build maven code
FROM openjdk:11.0.10-jre
WORKDIR /app
COPY --from=build /app/target/offers-0.0.1-SNAPSHOT.jar /app/
EXPOSE 1001
CMD ["java","-jar","/app/target/offers-0.0.1-SNAPSHOT.jar "]


