#  AutómataLab

Simulador interactivo de **autómatas finitos** (DFA y NFA). Escribes una cadena y ves, paso a paso, cómo el autómata recorre sus estados hasta aceptarla o rechazarla.

 Sitio publicado: https://bettylp905.github.io/automatalab/
Repositorio:** https://github.com/bettylp905/automatalab

> Proyecto final · Curso Introducción a la IA y Vibecoding · Tecnolochicas TC PRO

---

##  ¿De qué trata?

Aprender teoría de autómatas solo con dibujos en el pizarrón es difícil. AutómataLab convierte esos dibujos en algo que se puede probar:

- Diagrama de estados animado (estado actual en rosa, transición usada resaltada).
- Cinta de entrada que marca el símbolo que se está leyendo.
- Tabla de transiciones δ con la celda activa resaltada.
- Bitácora paso a paso (incluye conjuntos de estados para NFA).
- Botones: **Paso**, **Atrás**, **Auto**, **Resultado** y **Reiniciar**.
- 5 autómatas de ejemplo + editor para **crear el tuyo**.
- Modo claro / oscuro.

##  Cómo usarlo

1. Elige un autómata de la lista.
2. Escribe una cadena (por ejemplo `1101`).
3. Pulsa **Paso** para avanzar uno a uno, **Auto** para verlo animado o **Resultado** para ir al final.

### Crear tu propio autómata

Usa este formato en el cuadro de texto y pulsa **Cargar mi autómata**:

```
inicial: q0
finales: q2
q0,a,q1
q1,b,q2
```

Cada línea de transición es `origen,símbolo,destino`. Si repites origen y símbolo con destinos distintos, obtienes un autómata no determinista.

##  Herramientas

| Herramienta | Uso |
|---|---|
| **Gemini** | Generación y mejora del código mediante prompts |
| HTML + CSS + JavaScript | Sitio en un solo archivo, sin librerías externas |
| SVG | Dibujo del diagrama de estados |
| GitHub + GitHub Pages | Repositorio y publicación |

##  Prompts utilizados

### Prompt inicial (Rol, Tarea, Contexto, Restricciones)


ROL: Actúa como un desarrollador web front-end experto en HTML, CSS y JavaScript puro, y con conocimientos sólidos de teoría de autómatas y lenguajes formales.
TAREA: Construye un sitio web interactivo de una sola página llamado "AutómataLab" que simule autómatas finitos (DFA y NFA). El usuario escribe una cadena y el sitio muestra paso a paso cómo se recorren los estados hasta aceptar o rechazar la cadena.
CONTEXTO: El público son estudiantes de la Licenciatura en Tecnologías y Sistemas de la Información que cursan Teoría de Autómatas y Lenguajes Formales. El sitio debe ser didáctico, muy visual y colorido (morado, rosa y cian), y debe poder demostrarse en vivo en un pitch de 2 minutos.
RESTRICCIONES: 1) Todo en un solo archivo index.html, sin librerías externas, compatible con GitHub Pages. 2) Diagrama de estados en SVG con el estado actual resaltado, doble círculo para estados de aceptación y flecha de entrada en el estado inicial. 3) Cinta de entrada que marque el símbolo leído. 4) Botones funcionales: Paso, Atrás, Auto, Resultado y Reiniciar. 5) Tabla de transiciones y bitácora de pasos. 6) Al menos 4 autómatas de ejemplo (termina en 01, cantidad par de 0s, contiene "aba", ab*c). 7) Un cuadro para que el usuario cree su propio autómata. 8) Botón de modo oscuro y diseño responsivo para celular. 9) Código comentado en español.


Refnamientos
Refinamiento 1 · No determinismo
Agrega soporte para autómatas no deterministas (NFA): si hay varias transiciones posibles, resalta todos los estados activos a la vez. Incluye un ejemplo NFA que acepte cadenas que terminan en "ab".
Refinamiento 2 · Validación
Si el usuario escribe símbolos que no están en el alfabeto del autómata, muestra una advertencia en rojo debajo del campo y rechaza la cadena. Muestra también un mensaje claro de ACEPTADA o RECHAZADA al final.
Refinamiento 3 · Diseño y claridad
Mejora el diseño para celular, agrega una bitácora que diga "Leo X → {estados}" en cada paso y resalta en la tabla de transiciones la celda que se usó. Comenta el código en español.




##  Errores encontrados y cómo se corrigieron

| # | Qué pasó | Causa técnica | Cómo se corrigió |
|---|---|---|---|
| 1 |La flecha de entrada se encima con el estado inicial. | Ambos elementos se dibujaban en la misma dirección. | Se le pidió a la IA ajustar las coordenadas y la curva del vector.|
| 2 |Los botones no respondían al dar clic. |El script intentaba leer los elementos antes de que el navegador los dibujara. | Se envolvió la lógica en la función de inicialización.|

##  Estructura

```
automatalab/
├── index.html   # Sitio completo (HTML, CSS y JS)
└── README.md
```

##  Publicación

Publicado con **GitHub Pages** desde la rama `main`, carpeta raíz.

##  Aprendizaje personal

"Aprendí que usar herramientas de IA no es solo pedir código, sino saber estructurar los requerimientos e interpretar los errores. Diseñar las visualizaciones paso a paso me ayudó a reforzar por completo la lógica de las transiciones en los autómatas."
