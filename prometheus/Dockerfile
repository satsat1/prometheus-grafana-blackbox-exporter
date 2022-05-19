FROM prom/prometheus:v2.0.0

COPY prometheus.yml /etc/prometheus/prometheus.yml

USER [nobody]
EXPOSE 9090/tcp
VOLUME [/prometheus]
WORKDIR /prometheus
ENTRYPOINT &{["/bin/prometheus"]}
CMD ["--config.file=/etc/prometheus/prometheus.yml" "--storage.tsdb.path=/prometheus" "--web.console.libraries=/usr/share/prometheus/console_libraries" "--web.console.templates=/usr/share/prometheus/consoles"]
