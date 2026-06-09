# Repositorio oficial de Tokens para el DS del Gobierno de Morelos
Este repositorio es la fuente única de verdad de nuestro sistema de diseño. Aquí encontrarás los valores de color, tipografía, espaciado y otros estilos exportados directamente desde Figma a través de una automatización de Supernova.io.

## ¿Dónde están los archivos?
Toda la salida de diseño se encuentra en la carpeta /tokens, organizada por tecnología para que cada equipo use lo que necesite:

- /tokens/css: Variables nativas de CSS para proyectos web estándar.

- /tokens/json: Los datos puros en formato JSON. Ideal si usas herramientas como Style Dictionary para transformar estos tokens a otros formatos (Android, iOS, etc.).

- /tokens/tailwind: Configuración lista para copiar en proyectos que usen Tailwind CSS.

_Nota para Devs: Si se necesitaran nuevas exportaciones, pueden solicitarlas al equipo de diseño._

## Instalación rápida para proyectos web

La forma más simple de consumir los tokens CSS es vía CDN, sin instalar nada:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/morelosdesign/morelos-ds@main/tokens/css/index.css">
```

Luego aplica las clases de tema en tu elemento `<body>`:

```html
<body class="theme-light theme-desktop">
```

### Clases de tema disponibles

| Categoría | Clase | Descripción |
|-----------|-------|-------------|
| Color | `theme-light` | Paleta clara (default) |
| Color | `theme-dark` | Paleta oscura |
| Color | `theme-high-contrast` | Alto contraste (accesibilidad) |
| Color | `theme-gray-scale` | Escala de grises |
| Tamaños | `theme-desktop` | Tipografía y espaciado para desktop |
| Tamaños | `theme-mobile` | Tipografía y espaciado para mobile |

### ⚠️ Aviso importante sobre `@main`

El enlace de arriba apunta siempre a la última versión del repositorio. Esto significa:

- Los tokens se actualizan automáticamente cuando el equipo de diseño hace un merge.
- Si se renombra o elimina un token, **tu página puede verse afectada sin previo aviso**.

Esto es aceptable durante la fase activa de construcción del DS. Cuando el sistema esté estable, se publicarán versiones etiquetadas (`@v1.0.0`) para que cada proyecto pueda actualizar de forma controlada.

## ¿Cómo se actualiza esto?
Se ha configurado un flujo automático para que el repositorio siempre esté al día:

Cambio en Figma: Cuando se modifica un token en las librerías de Figma y se publica, Supernova detecta el cambio automáticamente a partir del evento _Source updated_.

Generación de archivos: Supernova traduce esos cambios a los archivos de código en la carpeta /tokens.

Aviso en GitHub (Pull Request): Supernova abrirá automáticamente un Pull Request.

_Nota para Devs: El equipo responsable de validar los tokens recibira una notificación, podrá revisar qué valores cambiaron y decidir cuándo integrar (merge) esos cambios en su código._

## Notas para el equipo de desarrollo
No editar manualmente: Por favor, no modifiquen los archivos dentro de /. Cualquier cambio manual se perderá la próxima vez que yo actualice Figma.

Nomenclatura: Los nombres de las variables se generan automáticamente. Si necesitan un formato de nombre diferente, avísenme para ajustar la configuración en Supernova.

## Estado del Sistema (Fase de Implementación)
Este repositorio está en proceso de construcción durante este año. Para que la integración sea lo más fluida posible, ten en cuenta lo siguiente:

Evolución constante: Como estamos en una fase activa de diseño, es probable que veas ajustes en nombres de tokens o en la organización de archivos. Todo será notificado con previo aviso.

La comunicación es clave: Si ves algo que no te cuadra, algún nombre confuso o crees que la estructura podría ser mejor para tu flujo de trabajo, avísanos directamente.
