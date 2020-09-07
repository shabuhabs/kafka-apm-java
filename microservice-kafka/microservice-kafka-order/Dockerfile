FROM openjdk:11.0.2-jre-slim
COPY signalfx-tracing.jar .
COPY target/microservice-kafka-order-0.0.1-SNAPSHOT.jar .

ENV SIGNALFX_ENDPOINT_URL=http://ec2-13-59-9-233.us-east-2.compute.amazonaws.com:9080/v1/trace
ENV SIGNALFX_SERVICE_NAME=order
ENV SIGNALFX_AGENT_HOST=13.59.9.233
CMD /usr/bin/java -javaagent:signalfx-tracing.jar -Xmx400m -Xms400m  -XX:TieredStopAtLevel=1 -noverify -jar microservice-kafka-order-0.0.1-SNAPSHOT.jar
EXPOSE 8080
