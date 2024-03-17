FROM confluentinc/cp-server-connect:7.5.0

USER root

RUN confluent-hub install --no-prompt debezium/debezium-connector-mysql:1.7.1

ADD connectors /etc/kafka-connect/connectors

WORKDIR /etc/kafka-connect/connectors

RUN chmod +x ./register_connectors.sh

CMD ["./register_connectors.sh"]