# Usa la ultima imagen oficial de Ubuntu 22.04 como base
FROM ubuntu:22.04

#Establecer los parametros de las variable de entorno
ENV MYSQL_USER=usuarioDockerfile MYSQL_PASSWORD=passwordDockerfile MYSQL_DATABASE=baseDeDatosDockerfile

#Instalar mysql-server
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y mysql-server

# Copiar ficheros
COPY my.cnf /etc/mysql/conf.d/
COPY script.sh /usr/local/bin/

# Otorgar permisos de escritura al fichero script.sh copiado en el paso anterior
RUN chmod +x /usr/local/bin/script.sh

# Exponer el puerto 3306
EXPOSE 3306

# Ejecutar al arrancar el script.sh
CMD ["/usr/local/bin/script.sh"]