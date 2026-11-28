# SEJK
Proyecto de Taller de Ing. Electrónica.

Integrantes:

Mahia Alejandra Vanegas Parrado

Julián González Cuellar

# S.E.J.K. — Sistema de Estudio Julick

## Descripción del proyecto

S.E.J.K. (Sistema de Estudio Julick) es un proyecto desarrollado en la Universidad Nacional de Colombia, sede Bogotá, orientado a mejorar los métodos de estudio, la concentración, la memoria y el aprendizaje autónomo de los estudiantes universitarios.

El proyecto se encuentra relacionado con el Objetivo de Desarrollo Sostenible 4 (ODS 4): Educación de calidad. Su fundamento teórico se basa en técnicas de aprendizaje y memorización propuestas por Ramón Campayo y Jaime García Serrano.

## Implementaciones del proyecto

Durante el desarrollo del proyecto se conservaron las dos implementaciones propuestas:

- **Aplicación informática:** desarrollada mediante MIT App Inventor, incorpora herramientas y ejercicios orientados al fortalecimiento de la memoria, la concentración y los hábitos de estudio.
- **Dispositivo electrónico con pantalla táctil:** desarrollado mediante una pantalla con microcontrolador ESP32 integrado, programada utilizando Arduino IDE.

Ambas implementaciones cuentan con herramientas educativas complementadas mediante videos explicativos y animaciones disponibles en el canal de YouTube MateJULICK.

## Implementación electrónica del LED

Como parte del desarrollo electrónico del dispositivo, se planteó la incorporación de un LED externo que complementara el ejercicio de memoria y concentración disponible en la pantalla táctil.

Mediante la modificación del código original de la ESP32, se logró controlar la intensidad luminosa del LED utilizando una señal PWM generada por el GPIO 22.

La intensidad luminosa del LED aumenta y disminuye de manera sincronizada con el tamaño de la esfera presentada durante el ejercicio de concentración.

Las pruebas realizadas mediante una protoboard permitieron comprobar satisfactoriamente el funcionamiento del circuito y su sincronización con la interfaz gráfica.

Asimismo, se conservaron las funcionalidades originales del dispositivo, incorporando el control del LED sin eliminar los ejercicios ni las herramientas previamente desarrolladas.

El dispositivo puede utilizarse tanto con el módulo LED conectado como sin él, sin necesidad de modificar nuevamente su programación.

## Diseño de la PCB

Para consolidar la implementación electrónica, se desarrolló una placa de circuito impreso (PCB) mediante KiCad 10.0.8.

La PCB funciona como un módulo de expansión externo conectado a la ESP32 mediante dos conexiones: PWM y GND.

El diseño incorpora los siguientes componentes:

- Una resistencia de 330 Ω.
- Un LED de 5 mm.
- Un conector de dos pines con separación de 2,54 mm.

El diseño utiliza pistas de cobre en una sola cara, con el objetivo de simplificar el proceso de fabricación y reducir sus costos.

Se realizaron las comprobaciones de reglas eléctricas (ERC), reglas de diseño (DRC) y correspondencia entre el esquema eléctrico y la PCB, obteniendo resultados sin errores ni advertencias en las comprobaciones ejecutadas.

También se generaron los archivos Gerber y de taladrado necesarios para solicitar la fabricación física de la placa.

## Programación y configuración de Arduino IDE

Para la programación de la pantalla táctil y la incorporación del control PWM del LED se utilizó la siguiente configuración:

| Parámetro | Configuración |
|---|---|
| Entorno de desarrollo | Arduino IDE 2.3.11 |
| Placa | ESP32 Dev Module |
| ESP32 Core | 3.3.12 |
| Velocidad de carga | 115200 baudios |
| Frecuencia de CPU | 240 MHz |
| Modo de memoria Flash | DIO |
| Frecuencia de memoria Flash | 40 MHz |
| Tamaño de memoria Flash | 4 MB |
| PSRAM | Desactivada |
| Pin de control del LED | GPIO 22 |
| Librería gráfica | TFT_eSPI |
| Librería táctil | XPT2046_Touchscreen |

Aunque durante el proceso de desarrollo se realizaron pruebas con diferentes velocidades de carga, finalmente se utilizó satisfactoriamente una velocidad de 115200 baudios.

Los archivos de programación, las librerías y sus configuraciones se encuentran disponibles en el repositorio para facilitar la reproducción del proyecto.

## Diagramas de cajas negras

Durante el desarrollo del proyecto se realizaron diferentes versiones del diagrama de cajas negras, con el propósito de representar la estructura y el funcionamiento general del sistema.

### Primera versión

En la primera versión se planteó una implementación en la cual la pantalla táctil se encontraba como un elemento externo al microcontrolador.

Esta versión corresponde a la propuesta inicial del sistema electrónico.

### Segunda versión

En la segunda versión se modificó la estructura del sistema debido a la selección de una pantalla táctil con microcontrolador ESP32 integrado.

Esta versión representa la arquitectura utilizada actualmente para el funcionamiento de la pantalla táctil.

### Tercera versión

Se plantea desarrollar una tercera versión del diagrama de cajas negras, incorporando la PCB de expansión y el LED controlado mediante PWM.

Esta actualización permitirá representar de manera más completa la implementación electrónica final del dispositivo.

## Contenido del repositorio

| Archivo o carpeta | Descripción |
|---|---|
| Proyecto taller de electrónica.pdf | Documento de requerimientos establecidos para el desarrollo del proyecto. |
| Primera versión de diagrama de cajas negras.jpg | Representación inicial del sistema, considerando una pantalla externa al microcontrolador. |
| Segunda versión de diagrama de cajas negras | Representación actualizada del sistema con pantalla y ESP32 integrados. |
| S.E.J.K semana 4.pdf | Bitácora del proceso de diseño, programación, pruebas e implementación electrónica desarrollado durante la cuarta semana. |
| SEJK_Configuración Arduino IDE.zip | Código fuente, librerías, archivos de configuración y recursos necesarios para programar la ESP32. |
| SEJK_KiCad | Carpeta que contiene los archivos originales y editables del proyecto electrónico desarrollado en KiCad. |
| SEJK_V1.0_Gerber.zip | Archivos Gerber y de taladrado necesarios para la fabricación física de la PCB. |
| SEJK_Esquema_Electrico.pdf | Esquema eléctrico del circuito exportado directamente desde KiCad. |
| SEJK_PCB_2D.png | Representación bidimensional de la PCB, mostrando las pistas, conexiones y distribución de los componentes. |
| SEJK_PCB_3D.png | Representación tridimensional de la apariencia prevista de la PCB ensamblada. |
| SEJK_BOM.csv | Lista de materiales necesarios para el ensamblaje de la PCB. |
| README.md | Documento general de presentación y descripción del proyecto. |

## Lista de materiales de la PCB

| Referencia | Componente | Especificación | Cantidad |
|---|---|---|---|
| R1 | Resistencia | 330 Ω | 1 |
| D1 | LED | 5 mm | 1 |
| J1 | Conector macho | 1×2 pines, separación de 2,54 mm | 1 |

## Conclusiones

El desarrollo de S.E.J.K. permitió integrar herramientas informáticas y electrónicas orientadas al fortalecimiento de los métodos de estudio.

Se logró conservar el funcionamiento de las dos implementaciones originales e incorporar una nueva funcionalidad electrónica mediante el control de la intensidad luminosa de un LED, sincronizado con uno de los ejercicios de concentración.

El diseño de la PCB representa un avance hacia la consolidación física del dispositivo, permitiendo sustituir las conexiones experimentales realizadas mediante protoboard por una implementación más compacta y organizada.

Los archivos disponibles en este repositorio permiten consultar, estudiar, reproducir y continuar desarrollando el proyecto S.E.J.K.

---

**S.E.J.K. V1.0 — Sistema de Estudio Julick**

Universidad Nacional de Colombia — Sede Bogotá

Ingeniería Electrónica — 2026
