# Última versión de Ubuntu
FROM ubuntu:latest

# Actualiza ubuntu e instala proftpd
RUN apt-get update \
    && apt-get -y install proftpd

#Copia desde local el fichero con la configuración de proftpd y la carpeta que se pide en el enunciado 
COPY proftpd.conf /etc/proftpd/proftpd.conf
COPY Recursos-Contenedor-1 /srv/ftp

# Expone los puertos 20 y 21 para que proftpd en el contenedor funcione
EXPOSE 20 21