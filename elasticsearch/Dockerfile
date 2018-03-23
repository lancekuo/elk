# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.3

RUN mkdir /opt/elasticsearch
COPY config/elasticsearch.yml /opt/elasticsearch/config/elasticsearch.yml
#COPY config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
