FROM openjdk:17-jdk-slim
RUN apt-get update && apt-get install -y \
x11-apps \
xauth \
libxtst6 \
&& rm -rf /var/lib/apt/lists/*

WORKDIR /pr5
COPY calc.jar /pr5/calc.jar


ENV DISPLAY=host.docker.internal:0 
CMD ["java", "-jar", "calc.jar"]