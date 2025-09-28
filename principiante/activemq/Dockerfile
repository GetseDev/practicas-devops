FROM eclipse-temurin:17-jdk

WORKDIR /app

RUN apt-get update && \
    apt-get install -y unzip && \
    rm -rf /var/lib/apt/lists/* 

COPY . .

RUN unzip apache-activemq-5.19.0.zip && \ 
    rm -rf apache-activemq-5.19.0.zip && \
    chmod +x /app/apache-activemq-5.19.0/bin/activemq

ENV ACTIVEMQ_HOME=/app/apache-activemq-5.19.0
ENV PATH="$ACTIVEMQ_HOME/bin:$PATH"

EXPOSE 61616 8161 

CMD ["activemq", "console"]