# Trabajo Práctico Integrador - Computación Aplicada

## Integrantes

* Ariel Butrón
* Matías Gonzalez Groba
* Lucio Silva Cubitto
* Agustín Santiñaque

## Resumen

Servidor Debian 12 configurado con:

* SSH mediante autenticación por clave pública.
* Apache + PHP.
* MariaDB.
* Almacenamiento adicional con particiones dedicadas.
* Sistema de backup automatizado.
* Tareas programadas mediante cron.

## Descripción

* En el presente trabajo práctico se realizó la implementación y configuración integral de un servidor basado en Debian GNU/Linux 12, utilizando la máquina virtual provista.

* Como primera etapa, se efectuó la recuperación y reconfiguración de la cuenta de administrador (root), estableciendo una nueva contraseña y configurando el hostname del sistema como TPServer. Posteriormente, se actualizó completamente el sistema operativo a Debian 12, garantizando la utilización de una plataforma actualizada y segura.

* En relación con los servicios requeridos, se instaló y configuró el servicio SSH, habilitando el acceso remoto del usuario root mediante autenticación basada en claves pública y privada. Asimismo, se implementó un servidor web Apache HTTP Server con soporte para PHP, permitiendo la publicación y ejecución de aplicaciones web. Complementariamente, se instaló y configuró MariaDB como motor de base de datos, importando correctamente el script SQL suministrado y verificando su funcionamiento mediante la aplicación web provista.

* Respecto de la conectividad, se configuró la interfaz de red con direccionamiento IP estático, definiendo explícitamente los parámetros de dirección IP, máscara de red y puerta de enlace predeterminada. Esto permitió garantizar la accesibilidad permanente del servidor desde otros equipos de la misma red.

* En materia de almacenamiento, se incorporó un disco virtual adicional de 10 GB, sobre el cual se crearon dos particiones independientes destinadas a los directorios /www_dir y /backup_dir. Ambas particiones fueron formateadas, montadas y configuradas para su montaje automático durante el arranque del sistema mediante el archivo /etc/fstab. Adicionalmente, se reconfiguró Apache para utilizar /www_dir como directorio raíz de publicación del sitio web.

* Como mecanismo de respaldo, se desarrolló un script denominado backup_full.sh, capaz de generar copias de seguridad comprimidas en formato tar.gz, incorporando la fecha de ejecución al nombre del archivo generado. El script incluye validaciones de parámetros, existencia de directorios y disponibilidad de los sistemas de archivos involucrados. Finalmente, se automatizó su ejecución mediante tareas programadas con cron, permitiendo la generación periódica de respaldos de los directorios definidos por la consigna.

* Por último, se generaron y comprimieron los directorios solicitados para la entrega, incluyendo la partición del directorio /var en múltiples archivos para facilitar su almacenamiento y publicación en un repositorio GitHub.

* Como resultado, se obtuvo un servidor Linux completamente funcional, con servicios de acceso remoto, servidor web, base de datos, almacenamiento persistente y mecanismos automatizados de respaldo.
