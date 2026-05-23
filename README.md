# Solemne2
## 1. Información del Proyecto

### Descripción objetiva
El proyecto es un sistema visual dinámico programado en p5.js que genera una malla o matriz interactiva de elementos geométricos abstractos. 
En la pantalla se ve una cuadrícula regular de formas (círculos y cuadrados) en alto contraste (blanco, negro y rojo). Los elementos reaccionan continuamente modificando su forma, tamaño, posición y color a medida que el usuario mueve el mouse.
* **Inputs utilizados:** Posición continua del mouse (`mouseX`, `mouseY`) y evento de clic (`mousePressed`).
* **Outputs generados:** Transformaciones geométricas, variaciones de grosor de línea, distorsiones por proximidad, vibración aleatoria de las formas y cambios en la paleta de colores.

## 2. Descripción Conceptual
### Idea central del proyecto
El proyecto explora la transición entre el orden geométrico estático y el caos orgánico reactivo mediante el movimiento del mouse. Busca que el espectador experimente una sensación de distorsión óptica a través de una pantalla digital.
### Corriente o referente de diseño con el que dialoga
**Op Art (Arte Óptico)** y el **Arte Cinético**. 
* **Referentes: Se toman como referencia las estructuras geométricas repetitivas de **Victor Vasarely** y los efectos de vibración de líneas de **Bridget Riley**. 
* **Principio de diseño explorado:** El principio de **Ritmo y Variación**. No se copia una imagen fija de estos artistas, sino que se traduce su *lógica de diseño* (el contraste, la repetición geométrica y la ilusión de movimiento) en un algoritmo computacional reactivo donde el usuario es el motor de la vibración de la obra.

## 3. Input/Output y Sistema

Reglas que gobiernan el sistema
1.  Regla de Espaciado: El lienzo se divide matemáticamente en una cuadrícula simétrica de 15x15 elementos.
2.  Regla de Proximidad: Cada celda calcula constantemente su distancia física respecto al cursor.
3.  Regla de Comportamiento Cinético: Si la distancia es menor a 100 píxeles, la forma muta de un círculo a un cuadrado, reduce su tamaño y activa una vibración aleatoria (`random`).
4.  Regla de Grosor: El grosor del trazo de todo el sistema se calcula proporcionalmente (`map`) a la coordenada X del mouse.
5.  Regla de Color: Si el mouse cruza el eje central horizontal (mitad de pantalla), el color del trazo cambia automáticamente de blanco a rojo mediante un condicional.

Explicación del sistema de interactividad
¿Qué datos entran? Las coordenadas de posición $X$ e $Y$ del mouse en tiempo real.
¿Cómo se procesan y transforman? A través de la función `dist()`, el sistema calcula la cercanía del cursor a cada elemento. Mediante la función `map()`, el movimiento lineal del mouse se transforma en un rango controlado para el grosor de las líneas y la escala de las figuras.
¿Qué respuesta visual producen? Una onda de distorsión visual y "vibración" que sigue la trayectoria del cursor, rompiendo la cuadrícula rígida inicial.

<img width="1200" height="1200" alt="E27DNL2XMAMK11M" src="https://github.com/user-attachments/assets/6a5390f3-d637-4b57-89b5-04f8b158fceb" />
<img width="400" height="398" alt="blaze-1-1962" src="https://github.com/user-attachments/assets/27ed491b-7d28-44b7-9ec2-9d599df4ac8e" />

##LINK##
https://editor.p5js.org/luna.queulo/sketches/0N5h2w_ll
