# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash:6.3.2

COPY config/logstash.yml /usr/share/logstash/config/logstash.yml
COPY pipeline/logstash.conf /usr/share/logstash/pipeline/logstash.conf
USER root
RUN chown logstash.logstash /usr/share/logstash/config/logstash.yml
USER logstash
# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
