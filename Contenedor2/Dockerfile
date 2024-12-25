# Última versión de Ubuntu
FROM ubuntu:latest

# Actualiza ubuntu e instala proftpd
RUN apt-get update \
    && apt install -y proftpd-mod-crypto


RUN useradd deaw -m -d /srv/deaw/ --password "$user_password" -s /sbin/nologin

#Copia desde local todos los archivos necesarios
COPY proftpd.conf /etc/proftpd/proftpd.conf
COPY tls.conf /etc/proftpd/tls.conf
COPY modules.conf /etc/proftpd/modules.conf
COPY proftpd.key /etc/ssl/private/
COPY proftpd.crt /etc/ssl/certs/
COPY Recursos_Contenedor_2 /srv/deaw

# Expone los puertos 20 y 21 para que proftpd en el contenedor funcione
EXPOSE 20 21