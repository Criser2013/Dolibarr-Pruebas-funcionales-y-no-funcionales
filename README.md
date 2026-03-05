# Pruebas Dolibarr v.20.0.4
Este repositorio contiene casos de prueba funcionales y no funcionales sobre la aplicación Dolibarr en su versión **20.0.4**. En este evaluan diferentes factores de calidad.

## Requisitos
El requisitos principal es tener instalado y ejecución la aplicación Dolibarr. Dependiendo del tipo de prueba a ejecutar, habrán requisitos especificos como tener usuarios con acceso 
a ciertos módulos de la aplicación. También deberá tener instalado el software correspondiente a las pruebas que desee ejecutar, por ejemplo para la pruebas funcionales se requiere Python 
y para las unitarias PHP.

## Pruebas funcionales
En este factor de calidad se evaluaron **pruebas del sistema (E2E)** y **pruebas unitarias** sobre algunas funcionalidades y componentes de la aplicación. Los scripts e instrucciones
de ejecución pueden ser encontrados en la carpeta respectiva a cada tipo de prueba, al igual que la documentación sobre diseño de los mismos.  
En este apartado se utilizaron los frameworks:
- Playwright.
- PHPUnit.

## Pruebas no funcionales
Se realizaron pruebas de accesibilidad y pruebas de volumen, para esto se utilizó Google Lighthouse y Apache JMeter. La documentación sobre los casos de prueba y técnicas utilizadas 
se especifica en el archivo `README` de la carpeta respectiva.
