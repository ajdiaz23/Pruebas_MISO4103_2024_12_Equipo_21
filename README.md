# Miembros del equipo

| Nombre            | Correo                           |
| ----------------- | -------------------------------- |
| Axl Díaz          | aj.diaz23@uniandes.edu.co        |
| Diego Jaramillo   | df.jaramilloa1@uniandes.edu.co   |
| Nicolas Ibarra    | n.ibarra@uniandes.edu.co         |
| Andrés Rentería   | af.renteria2@uniandes.edu.co     |
| ----------------- | -------------------------------- |

# Instrucciones para la instalación y ejecución de las pruebas con Cypress

Luego de haber clonado el repositorio: https://github.com/ajdiaz23/Pruebas_MISO4103_2024_12_Equipo_21.git,
abra una terminal y ejecute los siguientes comandos:

- npm init -y
- npm install -g cypress

Si no se ha instalado correctamente cypress y sus respectivos plugins es necesario implementar los siguientes comandos:

- npm install faker
- npm install -D cypress-log-to-output
- npm install -D cypress-plugin-tab
- npm install neat-csv
- npm install --save-dev webpack-node-modules-polyfill

Si con el anterior comando no se instala faker para probar todas las pruebas, pruebe con el siguiente comando:

- npm install cypress --save-dev
- npm install @faker-js/faker --save-dev

Por ultimo,  para ejecutar las pruebas debe acceder a la carpeta "cypress" y luego en la terminal escribir el comando:
- cd cypress
- cypress run --headless

Para ejecutar cypress con interfaz realice los siguientes pasos:

- cd .\cypress
- root\cypress> cypress open
- clic en "Add project", escoger la carpeta "cypress" que esta dentro de la primera carpeta "cypress"
- Dar clic en la seccion o cuadro que menciona "e2e Testing"
- Dar clic en la seccion o boton que menciona "Start E2E Testing in Chrome"
- se abrira una ventana donde estaran varias carpetas dentro de la carpeta "cypress/e2e"
    (Nota: Cada carpeta tiene secciones por los 4 integrantes con los respectivos escenarios creados)
    - 3.42.9 -> escenarios con pruebas en cypress por cada integrante de la version 3.42.9 de GHOST
    - 5.82.2 -> escenarios con pruebas en cypress por cada integrante de la version 5.82.2 de GHOST
    - data-generation -> seccionado por carpetas de cada integrante con las pruebas de data pool seccionado con a-priori, pseudo-random y random. (Aqui se encuentran los 120 escenarios de pruebas)
- escoger y realizar la prueba por cada escenario de cada integrante dando clic en el archivo con extension ".cy.js". 

A continuación un link para poder realizarlo con una parte gráfica para correr las pruebas en cypress:
- https://uniandes-my.sharepoint.com/:v:/g/personal/n_ibarra_uniandes_edu_co/EbYxunneqPtJtKPWMpj_W44BzGwMFg3C-4QR2ojCErCZIg?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=iTaBog  
---

# Instrucciones para la instalación y ejecución de las pruebas con kraken

Luego de haber clonado el repositorio: https://github.com/ajdiaz23/Pruebas_MISO4103_2024_12_Equipo_21.git,
abra una terminal y ejecute los siguientes comandos en este orden:

- npm init -y
- npm install kraken-node
- npm install android-platform-tools
- npm install appium
- npx kraken-node gen

y para ejecutar use:

- npx kraken-node run

Por motivos de lo que parece ser un bug, debe probarse cada archivo por separado. Todos los archivos de prueba están ubicados en la carpeta:
.kraken\features\web\support\featuresToTest\

Para que las pruebas puedan correr sin problema se recomienda tener un único archivo de prueba en la carpeta:
.kraken\features\web\support\
y lanzar la prueba.

Luego intercambiar los archivos con los que están ubicados en la carpeta ..\featuresToTest\ y ejecutar cada vez y por separado.
De esta manera se logra evitar correr todos los archivos al tiempo y generar errores en las pruebas por falta de capacidad de procesamiento.
