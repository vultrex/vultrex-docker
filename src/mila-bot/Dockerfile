FROM azul/zulu-openjdk:13

# Run as non-root user
RUN groupadd -g 322 lavalink && \
    useradd -r -u 322 -g lavalink lavalink
USER lavalink

EXPOSE 8090

WORKDIR /opt/Lavalink

COPY Lavalink.jar Lavalink.jar

COPY application.yml application.yml

ENTRYPOINT ["java", "-Djdk.tls.client.protocols=TLSv1.1,TLSv1.2", "-Xmx2G", "-jar", "Lavalink.jar"]