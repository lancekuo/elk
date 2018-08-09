# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:6.3.2

#COPY config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml

COPY docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh
RUN chgrp 0 /usr/local/bin/docker-entrypoint.sh && chmod 0775 /usr/local/bin/docker-entrypoint.sh

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
