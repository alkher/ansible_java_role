****
JAVA
****

Instalación de `JAVA`_ en servidores LiNUX.

**********
Requisitos
**********

Sistemas operativos soportados:

	- CentOS 7 

*********
Variables
*********

::

	---
	# defaults file for java
	jdk_java: [] # Java a instalar: "open", la que viene con la paqueteria u "oracle" para instalar la versión de oracle (se pasa como parámetro).
	# JDK ORACLE
	jdk_version: 1.8.0_51 # Versión de JDK si jdk_java es oracle
	jdk_file: jdk-8u51-linux-x64.rpm # Nombre del fichero si jdk_java es oracle
	jdk_url: http://download.oracle.com/otn-pub/java/jdk/8u51-b16/jdk-8u51-linux-x64.rpm # URL de descarga si jdk_java es oracle
	jdk_download_path: /tmp # Directorio de descarga si jdk_java es oracle
	# JDK OPEN
	centos_openjdk: java-1.8.0-openjdk # Paquete para CentOS 

************
Dependencias
************

N/A

*******************
Ejemplo de playbook
*******************

::

    - hosts: servidores
      roles:
         - { role: alkher.java, jdk_java:open }

********
Licencia
********

BSD

*****
Autor
*****

Andoni Alcalde
- @alkher
- http://zenway.es
- alcher [at] zenway [dot] es


.. _JAVA: http://java.com/es/about/whatis_java.jsp