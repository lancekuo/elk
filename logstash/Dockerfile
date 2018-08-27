# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash:6.3.2

USER root
RUN chown logstash.logstash /usr/share/logstash/config/logstash.yml
RUN yum install epel-release -y && yum install jq -y && curl -s https://bootstrap.pypa.io/get-pip.py|python - && pip install awscli && yum clean all && rm -rf /var/cache/yum
COPY config/profile /etc/profile.d/ES_HOST.sh
RUN sed -i '1 a source /etc/profile.d/ES_HOST.sh' /usr/local/bin/docker-entrypoint

USER logstash
COPY config/logstash.yml /usr/share/logstash/config/logstash.yml
COPY pipeline/logstash.conf /usr/share/logstash/pipeline/logstash.conf
# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
