FROM openjdk:11.0.2-jre-slim
COPY signalfx-tracing.jar .
COPY target/microservice-kafka-shipping-0.0.1-SNAPSHOT.jar .
CMD /usr/bin/java -javaagent:signalfx-tracing.jar -Dsignalfx.agent.host=13.59.9.233 -Dsignalfx.service.name=shipping -Xmx400m -Xms400m  -XX:TieredStopAtLevel=1 -noverify -jar microservice-kafka-shipping-0.0.1-SNAPSHOT.jar
EXPOSE 8080
