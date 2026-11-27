# SEJK
Proyecto de Taller de Ing. Electrónica.

Integrantes:

Mahia Alejandra Vanegas Parrado

Julián González Cuellar

David Santiago Farfán
  
S.E.J.K. – Sistema de Estudio Julick

Descripción del proyecto:

S.E.J.K. (Sistema de Estudio Julick) es un proyecto desarrollado en el marco de la asignatura de Introducción a la Ingeniería Electrónica de la Universidad Nacional de Colombia, sede Bogotá. Su propósito es proporcionar herramientas que contribuyan al fortalecimiento de la memoria, la concentración y los métodos de estudio de los estudiantes universitarios.

El proyecto se encuentra relacionado con el Objetivo de Desarrollo Sostenible 4 (ODS 4): Educación de calidad, y se compone de dos implementaciones principales:

- Una aplicación móvil con ejercicios interactivos y herramientas de estudio.
- Un dispositivo electrónico autónomo con pantalla táctil, basado en un microcontrolador ESP32.

Ambas implementaciones buscan facilitar el acceso a diferentes técnicas de aprendizaje y promover el estudio autónomo.

Primera implementación: aplicación móvil

La aplicación móvil fue desarrollada mediante MIT App Inventor, una plataforma que permite la creación de aplicaciones mediante programación por bloques. Adicionalmente, se incorporaron recursos desarrollados en HTML para ampliar las funcionalidades y personalizar diferentes apartados del programa.

La aplicación cuenta con herramientas orientadas al entrenamiento de la memoria, la concentración, la lectura fotográfica, la elaboración de resúmenes y la administración del tiempo mediante la técnica Pomodoro.

El proceso de desarrollo se encuentra documentado en los archivos PDF disponibles en este repositorio:

- S.E.J.K. semana 2.pdf: diseño inicial del programa, organización de sus apartados y planteamiento de sus funcionalidades.
- S.E.J.K. semana 3.pdf y documentos posteriores:** avances relacionados con la programación, implementación y desarrollo de las herramientas propuestas.

Segunda implementación: dispositivo electrónico con pantalla táctil

La segunda implementación consiste en un dispositivo electrónico desarrollado mediante el módulo ESP32-2432S028, el cual integra un microcontrolador ESP32, una pantalla TFT táctil de 2,8 pulgadas con resolución de 240 × 320 píxeles y un controlador táctil XPT2046.

La programación del dispositivo se realizó en lenguaje C++ mediante Arduino IDE, utilizando las librerías TFT_eSPI y XPT2046_Touchscreen para gestionar la interfaz gráfica y la interacción táctil.

El dispositivo cuenta con una interfaz propia que permite acceder a diferentes ejercicios de memoria y herramientas de estudio sin depender de una computadora para su ejecución, aunque requiere una fuente de alimentación.

 Implementación electrónica adicional: 

Como complemento del dispositivo, se desarrolló un circuito externo compuesto por un LED y una resistencia de 330 Ω, conectado al GPIO 22 del ESP32.

Mediante la modulación por ancho de pulso (PWM), se controla progresivamente la intensidad luminosa del LED, sincronizándola con el crecimiento y la disminución de una figura circular presentada en uno de los ejercicios de memoria y concentración.

Esta implementación permite complementar el estímulo visual generado por la pantalla mediante un componente electrónico externo.

El circuito posee un diseño modular, lo que permite utilizar el dispositivo con o sin el LED conectado, sin necesidad de modificar nuevamente su programación.

## Código fuente y archivos de desarrollo

En el archivo comprimido **SEJK_GitHub.zip**, disponible en este repositorio, se encuentran los archivos necesarios para reproducir la programación del prototipo electrónico.

Su contenido se encuentra organizado de la siguiente manera:

| Carpeta | Descripción |
|---|---|
| SEJK_LED | Código fuente del dispositivo y recursos gráficos. |
| Configuracion_TFT | Archivos de configuración de la pantalla TFT. |
| Librerias | Librerías utilizadas durante el desarrollo. |
| Configuracion_Arduino | Parámetros de configuración y compilación del ESP32. |
| Firmware | Archivos binarios generados mediante la compilación del programa. |

### Especificaciones técnicas

- Microcontrolador: ESP32.
- Módulo: ESP32-2432S028.
- Controlador de pantalla configurado: ST7789.
- Resolución: 240 × 320 píxeles.
- Controlador táctil: XPT2046.
- Entorno de desarrollo: Arduino IDE 2.3.11.
- Paquete ESP32: versión 3.3.12.
- Lenguaje de programación: C++.
- Memoria flash: 4 MB.
- Frecuencia del procesador: 240 MHz.
- Frecuencia de la memoria flash: 40 MHz.
- Modo de memoria flash: DIO.
- Salida PWM para el LED: GPIO 22.
- Resistencia de protección del LED: 330 Ω.

La publicación de estos archivos busca facilitar la reproducción, modificación y ampliación del proyecto, así como permitir el desarrollo de futuras versiones de S.E.J.K.
