# Design Tokens Repository
Este repositorio es la fuente única de verdad de nuestro sistema de diseño. Aquí encontrarás los valores de color, tipografía, espaciado y otros estilos exportados directamente desde Figma a través de una automatización de Supernova.io.

## ¿Dónde están los archivos?
Toda la salida de diseño se encuentra en la carpeta /tokens, organizada por tecnología para que cada equipo use lo que necesite:

- /tokens/css: Variables nativas de CSS para proyectos web estándar.

- /tokens/json: Los datos puros en formato JSON. Ideal si usas herramientas como Style Dictionary para transformar estos tokens a otros formatos (Android, iOS, etc.).

- /tokens/tailwind: Configuración lista para copiar en proyectos que usen Tailwind CSS.

_Nota para Devs: Si se necesitaran nuevas exportaciones, pueden solicitarlas al equipo de diseño._

## ¿Cómo se actualiza esto?
Se ha configurado un flujo automático para que el repositorio siempre esté al día:

Cambio en Figma: Cuando se modifica un token en las librerías de Figma y se publica, Supernova detecta el cambio automáticamente a partir del evento _Source updated_.

Generación de archivos: Supernova traduce esos cambios a los archivos de código en la carpeta /tokens.

Aviso en GitHub (Pull Request): Supernova abrirá automáticamente un Pull Request.

_Nota para Devs: El equipo responsable de validar los tokens recibira una notificación, podrá revisar qué valores cambiaron y decidir cuándo integrar (merge) esos cambios en su código._

## Notas para el equipo de desarrollo
No editar manualmente: Por favor, no modifiquen los archivos dentro de /. Cualquier cambio manual se perderá la próxima vez que yo actualice Figma.

Nomenclatura: Los nombres de las variables se generan automáticamente. Si necesitan un formato de nombre diferente, avísenme para ajustar la configuración en Supernova.
