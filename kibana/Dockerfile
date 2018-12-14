ARG ELK_VERSION

FROM docker.elastic.co/kibana/kibana-oss:${ELK_VERSION}

ARG ELK_VERSION

# Prometheus exporter plugin
RUN bin/kibana-plugin install https://github.com/pjhampton/kibana-prometheus-exporter/releases/download/${ELK_VERSION}/kibana-prometheus-exporter-${ELK_VERSION}.zip
