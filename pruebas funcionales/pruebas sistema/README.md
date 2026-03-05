# Pruebas de sistema
En este paquete, hay casos de prueba para los módulos de "facturación", "tickets" y "MRP" de Dolibarr. Estas pruebas se encuentran codificadas en el framework [Playwright](https://playwright.dev/) en su versión de **Python**.
Las técnicas utilizadas para el diseño de los casos de prueba fueron: particiones de equivalencia y rablas de decisión, la documentación asociada está disponible en [este archivo](https://docs.google.com/spreadsheets/d/1vwR9MOoKY_qYQYv3sNeQtmdAnCmDssLD/edit?usp=sharing&ouid=100049882241117173391&rtpof=true&sd=true).

## Requisitos
1. Debe tener instalado Dolibarr en el sistema que probará. Para ver la guía de descarga e instalación [consulte la guía oficial](https://www.dolibarr.org/downloads.php). Se recomienda utilizar la versión de disponible en [Dockerhub](https://hub.docker.com/r/dolibarr/dolibarr).
2. Cada funcionalidad cuenta con requisitos especificos, por lo que revise la [matriz de requerimientos de prueba](https://docs.google.com/spreadsheets/d/1sry7gnjY14pm4QPmz99Gs4jLONDJm4PO/edit?usp=sharing&ouid=100049882241117173391&rtpof=true&sd=true) antes de ejecutar algún script.

## ¿Cómo ejecutar las pruebas?
1. Instale Playwright en su entorno de Python con el comando:
```
pip install -r requirements.txt
```
2. Configure las variables de entorno como se muestra en el archivo `.env.example`. Recuerde que el usuario **debe tener acceso** a los módulos que haga referencia cada prueba y permisos para realizar las operaciones CRUD.
3. Asegurese de que las precondiciones de cada caso de prueba se cumplan dentro de la aplicación.
4. Ejecute las pruebas con uno de los siguientes comandos:
```
pytest ./tests                     # Ejecute todas las pruebas
pytest ./tests/test_<nombre>.py    # Para ejecutar únicamente las pruebas de un archivo.
```

**Nota:** Cuando un test falle, se guardará una captura de pantalla en la carpeta `./screenshots` y el nombre de archivo corresponderá al test fallido.
