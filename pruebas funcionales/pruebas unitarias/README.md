# Pruebas unitarias
En este paquete, hay casos de prueba para algunos de métodos de las clases "Ticket", "UserBankAccount", "User", "Holiday", "Contrat" y "ProductBatch" de Dolibarr. Estas pruebas se encuentran codificadas en el framework [PHPUnit](https://phpunit.de/index.html). Las técnicas utilizadas para el diseño de los casos de prueba fueron: cobertura de condición/decisión, cobertura de sentencia, cobertura de ramas y cobertura de condición, la documentación asociada a los diseños de casos de prueba está disponible [en este archivo](https://docs.google.com/spreadsheets/d/1H-yZdWvDW8vkOjY2Z713mLw6MODfCmK2/edit?usp=sharing&ouid=100049882241117173391&rtpof=true&sd=true). Con estos casos de prueba se logra más de un 90% de cobertura de sentencia en las clases y métodos seleccionados.


## ¿Cómo ejecutar las pruebas?
1. Clone el código fuente de Dolibarr.
```bash
git clone https://github.com/Dolibarr/dolibarr.git
```
2. Instale **PHPUnit** siguiendo la [guía oficial](https://docs.phpunit.de/en/13.0/installation.html).
3. Mueva la carpeta "tests" dentro del directorio que se creó al clonar el repositorio de Dolibarr.
```bash
mv ./tests ./<carpeta-codigo-dolibarr>
```
5. Ejecute las pruebas utilizando uno de los siguientes comandos
```bash
phpunit                           # Ejecutar todos los tests
phpunit <nombre-archivo>.php      # Ejecutar los tests de un archivo en especifico
phpunit --coverage                # Ejecutar todos los tests guardando el reporte de cobertura de código
```

**Nota:** Al ejecutar las pruebas con reporte de cobertura se creará una carpeta con el reporte de cobertura de código como una página HTML.
