# ansible-go
Using go with ansible and minikube WIP
Basado en el siguiente articulo
https://medium.com/@adilsonbna/ansible-k8s-for-the-laziest-person-part-2-a0fea80c490c

El siguiente codigo busca automatizar la instalación de un entorno de minikube local
para que un desarrollador pueda probar de forma rapida y comoda sus imagenes dockerizadas,
se utiliza Centos 7 como sistema operativo base.

Pre requisitos manuales para que el codigo funcione:
-- El servidor debe poseer como requerimientos minimos 2 Procesadores (Virtuales), 2GB de Ram y 20 GB de espacio disponible
-- Se debe instalar git en el servidor.
-- Se debe instalar ansible en el servidor
-- Clonar el repositorio

Los procesos automatizados actualmente son los siguientes:

1) Crear un usuario llamado minikube y entregar permisos de super usuario (sudo).
2) Instalar Pip3.
3) Remover antiguas versiones de docker instaladas previamente
4) Instalar docker-ce
5) Instalar docker-compose
6) Instalar version pip de ansible para instalar paquetes de python 
7) Instalar Openshift
8) Iniciar servicio docker
9) Instalar Minidocker
10) Iniciar Minidocker
11) Verificar si imagen existe, sino crearla.
12 Crear un recurso de kubernetes para la imagen
13) Crear un servicio de kubernetes para la imagen
14) Exponer servicio en el host.
15) Testear la conexion a la imagen en minikube

Aun faltan procesos como la instalación de kubectl, para que el usuario pueda manejar de forma manual el cluster.

Se corregirá la logica para usar un solo usuario en todo el proceso, generando asi tambien los archivos necesarios para manejar las variables
correspondientes.


