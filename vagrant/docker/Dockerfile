# Użycie lekkiego obrazu Nginx jako bazy
FROM nginx:alpine

# Ustawienie katalogu roboczego w kontenerze
WORKDIR /usr/share/nginx/html

# Usunięcie domyślnych plików Nginx
RUN rm -rf ./*

# Skopiowanie plików aplikacji do katalogu roboczego
COPY ./html /usr/share/nginx/html

# Port, na którym nginx nasłuchuje
EXPOSE 80

# Uruchomienie Nginx i utrzymanie działania procesu w tle
CMD ["nginx", "-g", "daemon off;"]
