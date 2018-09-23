# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:6.4.0

COPY healthcheck /usr/local/bin/
RUN chmod +x /usr/local/bin/healthcheck

HEALTHCHECK CMD ["healthcheck"]

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
