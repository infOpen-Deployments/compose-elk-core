ARG ELK_VERSION
ARG KIBANA_PLUGIN_ELASTALERT_VERSION
ARG KIBANA_PLUGIN_ENHANCED_TABLE_VERSION
ARG KIBANA_PLUGIN_LOGTRAIL_VERSION
ARG KIBANA_PLUGIN_WAZUH_VERSION

FROM docker.elastic.co/kibana/kibana-oss:${ELK_VERSION}

ARG ELK_VERSION
ARG KIBANA_PLUGIN_ELASTALERT_VERSION
ARG KIBANA_PLUGIN_ENHANCED_TABLE_VERSION
ARG KIBANA_PLUGIN_LOGTRAIL_VERSION
ARG KIBANA_PLUGIN_WAZUH_VERSION

# Analyze API plugin
RUN bin/kibana-plugin install https://github.com/johtani/analyze-api-ui-plugin/releases/download/${ELK_VERSION}/analyze_api_ui-${ELK_VERSION}.zip

# Elastalert plugin
RUN bin/kibana-plugin install https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/${KIBANA_PLUGIN_ELASTALERT_VERSION}/elastalert-kibana-plugin-${KIBANA_PLUGIN_ELASTALERT_VERSION}-${ELK_VERSION}.zip

# Enhanced table plugin
RUN bin/kibana-plugin install https://github.com/fbaligand/kibana-enhanced-table/releases/download/v${KIBANA_PLUGIN_ENHANCED_TABLE_VERSION}/enhanced-table-${KIBANA_PLUGIN_ENHANCED_TABLE_VERSION}_${ELK_VERSION}.zip

# Indices view plugin
#RUN bin/kibana-plugin install https://github.com/TrumanDu/indices_view/releases/download/v${ELK_VERSION}/indices_view-${ELK_VERSION}.zip

# Logtrail plugin
RUN bin/kibana-plugin install https://github.com/sivasamyk/logtrail/releases/download/v${KIBANA_PLUGIN_LOGTRAIL_VERSION}/logtrail-${ELK_VERSION}-${KIBANA_PLUGIN_LOGTRAIL_VERSION}.zip

# Prometheus exporter plugin
RUN bin/kibana-plugin install https://github.com/pjhampton/kibana-prometheus-exporter/releases/download/${ELK_VERSION}/kibana-prometheus-exporter-${ELK_VERSION}.zip

# Swimlane visualization plugin
# Not compatible with 7.3.0
# RUN bin/kibana-plugin install https://github.com/prelert/kibana-swimlane-vis/releases/download/v${ELK_VERSION}/prelert_swimlane_vis-${ELK_VERSION}.zip

# Wazuh plugin
RUN bin/kibana-plugin install https://packages.wazuh.com/wazuhapp/wazuhapp-${KIBANA_PLUGIN_WAZUH_VERSION}_${ELK_VERSION}.zip
