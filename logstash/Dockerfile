ARG ELK_VERSION

# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
# RUN logstash-plugin install logstash-input-google_cloud_storage
# RUN logstash-plugin install logstash-input-google_pubsub 
RUN logstash-plugin install logstash-filter-json