# Kafka Connect docker images

## APM Datapath - Elasticsearch sink

   cd kafka-connect/connectors
   docker build -f APM-Dockerfile -t user/repo:tag .

## APM Datapath - S3 sink

   cd kafka-connect/connectors
   docker build -f Archival-Dockerfile -t user/repo:tag .

## APM Datapath - Authenticator

  cd authenticator
  docker build -t user/repo:tag .

## APM Datapath - APM-Kafka-Interface

  cd sf-kafka-interface
  docker build -t user/repo:tag .

## APM Datapath - Kafka REST proxy

  cd kafka-rest-custom-auth
  docker build -t user/repo:tag .

## APM Datapath - Signature service

  cd signature-rest
  docker build -t user/repo:tag .

## APM Datapath - Schema generator

  cd schema-generator
  docker build -t user/repo:tag .


# Hadoop and Hive docker images

## All Docker images needed for archival hadoop/hive

  cd hadoop-and-hive
  download everything from https://maplelabsblr.sharepoint.com/:f:/r/sites/MapleLabsFileServer/Shared%20Documents/MapleLabsAll/Archival%20JARs?csf=1&web=1&e=5QRYhj and paste it into this folder
  ls would print
    aws-jars                   Hadoop-Datanode-Dockerfile  hadoop-namenode-run.sh  Hive-Metastore-Dockerfile  hive.tar.gz
    build-and-push.sh          hadoop-datanode-run.sh      hadoop.tar.gz           hive-metastore-startup.sh  README.md
    Hadoop-Base-Dockerfile     hadoop-hive.env             hive-conf               Hive-Server-Dockerfile
    hadoop-base-entrypoint.sh  Hadoop-Namenode-Dockerfile  hive-entrypoint.sh      hive-server-startup.sh
  login to snappyflowml docker repository
  sh ./build-and-push.sh

For detail instructions on how to build dockers visit https://docs.docker.com/engine/reference/commandline/build

