FROM openjdk:11.0.2-jre-slim
COPY signalfx-tracing.jar .

CMD /usr/bin/java -javaagent:signalfx-tracing.jar -Dhttp://13.59.9.233 -Dsignalfx.service.name=invoicing -Xmx400m -Xms400m  -XX:TieredStopAtLevel=1 -noverify -jar microservice-kafka-invoicing-0.0.1-SNAPSHOT.jar
EXPOSE 8080
