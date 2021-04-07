FROM hazelcast/hazelcast:4.2

ENV HZ_LIB $HZ_HOME/lib
WORKDIR $HZ_LIB

ENV HZ_VERSION 4.2
ENV BUCKET4J_VERSION 6.2.0
ENV JCACHE_VERSION 1.1.0

ADD hazelcast.xml $HZ_HOME

# Download jcache and bucket4j jars from maven repo.
ADD https://repo1.maven.org/maven2/javax/cache/cache-api/$JCACHE_VERSION/cache-api-$JCACHE_VERSION.jar $HZ_HOME
ADD https://repo1.maven.org/maven2/com/github/vladimir-bukhtoyarov/bucket4j-core/$BUCKET4J_VERSION/bucket4j-core-$BUCKET4J_VERSION.jar $HZ_HOME
ADD https://repo1.maven.org/maven2/com/github/vladimir-bukhtoyarov/bucket4j-jcache/$BUCKET4J_VERSION/bucket4j-jcache-$BUCKET4J_VERSION.jar $HZ_HOME
ADD https://repo1.maven.org/maven2/com/github/vladimir-bukhtoyarov/bucket4j-hazelcast/$BUCKET4J_VERSION/bucket4j-hazelcast-$BUCKET4J_VERSION.jar $HZ_HOME
ADD https://repo1.maven.org/maven2/javax/cache/cache-api/$JCACHE_VERSION/cache-api-$JCACHE_VERSION.jar $HZ_HOME/lib
ADD https://repo1.maven.org/maven2/com/github/vladimir-bukhtoyarov/bucket4j-core/$BUCKET4J_VERSION/bucket4j-core-$BUCKET4J_VERSION.jar $HZ_HOME/lib
ADD https://repo1.maven.org/maven2/com/github/vladimir-bukhtoyarov/bucket4j-jcache/$BUCKET4J_VERSION/bucket4j-jcache-$BUCKET4J_VERSION.jar $HZ_HOME/lib
ADD https://repo1.maven.org/maven2/com/github/vladimir-bukhtoyarov/bucket4j-hazelcast/$BUCKET4J_VERSION/bucket4j-hazelcast-$BUCKET4J_VERSION.jar $HZ_HOME/lib

USER root
RUN chmod -R +r ${HZ_HOME}