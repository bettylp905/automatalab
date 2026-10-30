# 🤖 AutómataLab

Simulador interactivo de **autómatas finitos** (DFA y NFA). Escribes una cadena y ves, paso a paso, cómo el autómata recorre sus estados hasta aceptarla o rechazarla.

🌐 **Sitio publicado:** https://TU-USUARIO.github.io/automatalab/
📦 **Repositorio:** https://github.com/TU-USUARIO/automatalab

> Proyecto final · Curso *Introducción a la IA y Vibecoding* · Tecnolochicas TC PRO

---

## 🎯 ¿De qué trata?

Aprender teoría de autómatas solo con dibujos en el pizarrón es difícil. **AutómataLab** convierte esos dibujos en algo que se puede probar:

- Diagrama de estados animado (estado actual en rosa, transición usada resaltada).
- Cinta de entrada que marca el símbolo que se está leyendo.
- Tabla de transiciones δ con la celda activa resaltada.
- Bitácora paso a paso (incluye conjuntos de estados para NFA).
- Botones: **Paso**, **Atrás**, **Auto**, **Resultado** y **Reiniciar**.
- 5 autómatas de ejemplo + editor para **crear el tuyo**.
- Modo claro / oscuro.

## 🧪 Cómo usarlo

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

## 🛠️ Herramientas

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

### Refinamientos

1. `PEGA AQUÍ EL PROMPT DE REFINAMIENTO 1`
2. `PEGA AQUÍ EL PROMPT DE REFINAMIENTO 2`
3. `PEGA AQUÍ EL PROMPT DE REFINAMIENTO 3`

## 🐞 Errores encontrados y cómo se corrigieron

| # | Qué pasó | Causa técnica | Cómo se corrigió |
|---|---|---|---|
| 1 | `DESCRIBE EL ERROR` | `EXPLICA POR QUÉ OCURRIÓ` | `QUÉ LE PEDISTE A GEMINI` |
| 2 | | | |

## 📁 Estructura

```
automatalab/
├── index.html   # Sitio completo (HTML, CSS y JS)
└── README.md
```

## 🚀 Publicación

Publicado con **GitHub Pages** desde la rama `main`, carpeta raíz.

## 💜 Aprendizaje personal

`ESCRIBE AQUÍ 2 O 3 FRASES SOBRE LO QUE APRENDISTE (vibecoding, prompts, autómatas...)`
