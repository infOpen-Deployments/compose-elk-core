ARG ELK_LOGSTASH_IMAGE_NAME
ARG ELK_VERSION

FROM ${ELK_LOGSTASH_IMAGE_NAME}:${ELK_VERSION}

# Install Beats plugin
RUN /opt/logstash/bin/logstash-plugin install logstash-input-beats
