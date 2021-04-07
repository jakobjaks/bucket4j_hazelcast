# Hazelcast for Bucket 4J Quick Start

Hazelcast Docker image with JCache and Bucket4J jars in the classpath, for people willing to quickly use Bucket4J with a remote Hazlecast Server.

It is the same as the [original Hazelcast docker image](https://github.com/hazelcast/hazelcast-docker/blob/master/hazelcast-oss/Dockerfile ) with the addition of:
1. hazelcast.xml with the ability to expose the TCP port to the external world based on this [Stackoverflow post](https://stackoverflow.com/a/47868251/815022)
2. JCache and Bucket4J jars added to the classpath to make it easy to use with Bucket4J. More details in this [Github issue](https://github.com/hazelcast/hazelcast-docker/issues/50)


Docker image available at:
https://hub.docker.com/jakobjaks/hazelcast-bucket4j/

# Running

```
docker run -dp 5701:5701 bucket4j-hazelcast 
```


# Building
```
docker build -t bucket4j-hazelcast .  
```

# Publishing
`docker tag d379a94e9a9a jakobjaks/bucket4j_hazelcast:firsttry`
`docker push jakobjaks/bucket4j_hazelcast`