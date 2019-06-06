# Kafka
aws kafka get-bootstrap-brokers --region us-east-1 --cluster-arn arn:aws:kafka:us-east-1:222385317864:cluster/kafkacluster/8153b230-07af-4413-ba63-9cb435832880-2

it gives:
{
    "BootstrapBrokerString": "b-1.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092,b-3.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092,b-2.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092"
}
Creating a topic 


sudo yum install java-1.8.0
wget https://archive.apache.org/dist/kafka/2.1.0/kafka_2.12-2.1.0.tgz
aws kafka describe-cluster --region us-east-1 --cluster-arn "arn:aws:kafka:us-east-1:222385317864:cluster/kafkacluster/8153b230-07af-4413-ba63-9cb435832880-2"
bin/kafka-topics.sh --create --zookeeper ZookeeperConnectString --replication-factor 3 --partitions 1 --topic AWSKafkaTutorialTopic
here ZookeeperConnectString = 10.0.8.66:2181,10.0.0.230:2181,10.0.1.59:2181 
bin/kafka-topics.sh --create --zookeeper 10.0.8.66:2181,10.0.0.230:2181,10.0.1.59:2181 --replication-factor 3 --partitions 1 --topic AWSKafkaTutorialTopic
created topic AWSKafkaTutorialTopic

Produce and consume

aws kafka get-bootstrap-brokers --region us-east-1 --cluster-arn arn:aws:kafka:us-east-1:222385317864:cluster/kafkacluster/8153b230-07af-4413-ba63-9cb435832880-2
output:
{
    "BootstrapBrokerString": "b-3.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092,b-1.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092,b-2.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092"
}

bin/kafka-console-producer.sh --broker-list BootstrapBrokerString --topic AWSKafkaTutorialTopic
bin/kafka-console-producer.sh --broker-list b-3.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092,b-1.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092,b-2.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092 --topic AWSKafkaTutorialTopic


In 2nd terminal,
bin/kafka-console-consumer.sh --bootstrap-server BootstrapBrokerString --topic AWSKafkaTutorialTopic --from-beginning
bin/kafka-console-consumer.sh --bootstrap-server b-3.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092,b-1.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092,b-2.kafkacluster.crff9c.c2.kafka.us-east-1.amazonaws.com:9092 --topic AWSKafkaTutorialTopic --from-beginning
