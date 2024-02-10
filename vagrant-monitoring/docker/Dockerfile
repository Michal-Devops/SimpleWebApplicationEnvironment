# Używamy oficjalnego obrazu Prometheusa
FROM prom/prometheus:v2.26.0

# Kopiujemy plik konfiguracyjny Prometheusa do kontenera
COPY prometheus.yml /etc/prometheus/prometheus.yml

# Port, na którym Prometheus będzie dostępny
EXPOSE 9090

# Punkt startowy Prometheusa z użyciem pliku konfiguracyjnego
ENTRYPOINT [ "/bin/prometheus" ]
CMD [ "--config.file=/etc/prometheus/prometheus.yml", \
      "--storage.tsdb.path=/prometheus", \
      "--web.console.libraries=/usr/share/prometheus/console_libraries", \
      "--web.console.templates=/usr/share/prometheus/consoles" ]
