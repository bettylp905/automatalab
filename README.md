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

## 💬 Prompts utilizados

### Prompt inicial (Rol, Tarea, Contexto, Restricciones)

```
PEGA AQUÍ EL PROMPT EXACTO QUE USASTE EN GEMINI
```



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
