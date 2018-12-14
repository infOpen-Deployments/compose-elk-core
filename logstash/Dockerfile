ARG ELK_VERSION

FROM docker.elastic.co/logstash/logstash-oss:${ELK_VERSION}

# Install Beats plugin
RUN /opt/logstash/bin/logstash-plugin install logstash-input-beats
