# Pruebas no funcionales
En este paquete, se encuentra un conjunto de pruebas sobre factores de calidad no funcionales de la aplicación Dolibarr. Se efectuaron pruebas de volumen y accesibilidad.

## Requisitos
1. Debe tener instalado Dolibarr en el sistema que probará. Para ver la guía de descarga e instalación [consulte la guía oficial](https://www.dolibarr.org/downloads.php). Se recomienda utilizar la versión de disponible en [Dockerhub](https://hub.docker.com/r/dolibarr/dolibarr). Para las pruebas de volumen puede hacerlo sobre la instancia demo alojada en la página de Dolibarr.
2. Cada caso de prueba cuenta con requisitos especificos, por lo que revise la [matriz de requerimientos de prueba]([https://docs.google.com/spreadsheets/d/1sry7gnjY14pm4QPmz99Gs4jLONDJm4PO/edit?usp=sharing&ouid=100049882241117173391&rtpof=true&sd=true](https://docs.google.com/spreadsheets/d/1sOB86MA264QKfCVnAbBri_xDcddwlCuZdmUi33O-lvI/edit?usp=sharing)) antes de ejecutar algún script.

## Pruebas de accesibilidad
Se utilizó la técnica de "evaluación heurística" sobre los factores de "comprensibilidad" y "perceptibilidad" utilizando las siguientes [listas de chequeo](https://docs.google.com/spreadsheets/d/1pBMLBvfRXDneVNNI5CIHShEPqeq38AAz_FQkNaA5Tic/edit?usp=sharing). 
Este instrumento está basado en el estándar **WCAG 2.2**. Para validar el cumplimiento de las listas de chequeó se utilizó **Google Lighthouse**.  
Las pruebas deben ser ejecutadas manualmente utilizando la extensión de Lighthouse o la versión de las DevTools (para navegadores basados en Chromium) una vez esté en la página.  
Esto generá un reporte que puede ser exportado como archivo HTML.

## Pruebas de volumen
Se creó un script utilizando la herramienta **Apache JMeter** (archivo `Pruebas de carga - volumen.jmx`). En este se establecen 
los casos de prueba [aquí definidos](https://docs.google.com/spreadsheets/d/1sOB86MA264QKfCVnAbBri_xDcddwlCuZdmUi33O-lvI/edit?gid=1895327524#gid=1895327524). 
Tenga en cuenta que lo ideal sería ejecutar estas pruebas sobre el entorno de producción, no obstante puede simularse utilizando la distribución de Docker
de Dolibarr.

**Importante:** Las instrucciones para obtener la cookie de sesión con las credenciales para acceder a la aplicación se encuentran dentro del archivo.
