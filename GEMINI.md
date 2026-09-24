# Reglas del Proyecto

## Idioma
- Responde siempre en español (Chile).

## Entorno
- Sistema operativo: Windows 11
- Python: 3.12
- IDE: Antigravity IDE

## Preferencias de código
- No uses type hints en Python.
- Agrega docstrings en español solo a funciones que no sean obvias por su nombre.
- Prefiere f-strings sobre .format() o concatenación.

## Comportamiento
- No borres archivos sin confirmación.
- Explica brevemente los cambios que hagas.
- Si hay un error, muestra el error completo antes de proponer la solución.

## Seguridad y Restricciones de Archivos (Capa B)
- Está estrictamente prohibido ejecutar comandos de eliminación de archivos o carpetas (`Remove-Item`, `del`, `rm`, `rmdir`, `rd`, `git clean`, `git reset --hard`, etc.) sin autorización previa y explícita del usuario en el chat.
- Prohibido sobrescribir o vaciar destructivamente archivos existentes sin confirmación expresa.
- Si alguna tarea requiere eliminar, limpiar o descartar archivos o cambios, debes pausar, explicar detalladamente qué archivos se verían afectados y esperar la confirmación del usuario antes de ejecutar cualquier acción.


## Sincronización y Traspaso de Equipos (Laptop <-> PC Escritorio)
- Cuando el usuario indique que cambiará de equipo (ej. "me paso al PC", "voy al notebook", "guarda el avance", "traspaso"):
  1. **Actualizar estado**: Crear o actualizar un archivo `CURRENT_TASK.md` en la raíz del proyecto activo resumiendo:
     - Tareas completadas en la sesión actual.
     - Tareas y pasos específicos pendientes.
     - Archivos y funciones modificadas recientemente.
     - Pruebas, errores pendientes o comandos por ejecutar.
  2. **Commit y Push en Git**:
     - Realizar commit con formato: `wip: traspaso de equipo - [breve descripción]`.
     - Subir los cambios con `git push` a la rama de trabajo.
- Al retomar en el otro computador (ej. tras hacer `git pull` o cuando el usuario diga "continuemos" o "retomamos"):
  - Leer automáticamente `CURRENT_TASK.md` si existe en el proyecto.
  - Informar al usuario brevemente del estado anterior y proponer inmediatamente los siguientes pasos para continuar.

## Documentos e Integración con Google Drive
- Carpeta base sincronizada: `G:\Mi unidad\Antigravity_Docs\` (o la unidad de Google Drive correspondiente).
- Al generar informes, análisis, presentaciones o documentos que no sean código:
  - Usar `.docx` (formato compatible nativo con Google Docs) o `.pptx` (Google Slides) según corresponda.
  - Guardar directamente en `G:\Mi unidad\Antigravity_Docs\` para sincronización automática en la nube.
  - Esto permite consultarlos y editarlos directamente en Google Docs/Slides y en Gemini web (`gemini.google.com`) mediante `@Google Drive`.
- **Estilo y formato obligatorio para informes (.docx):**
  - Mantener un estilo sobrio, formal y limpio, idéntico al estándar de los informes de Google Docs y ámbito universitario (USS).
  - Prohibido agregar adornos estéticos excesivos: sin cajas de colores, sin fondos celestes/azules, sin sombras ni líneas divisorias cromáticas.
  - Tipografía: Fuente Arial en todo el documento.
  - Color de texto: Estrictamente negro (#000000) o automático. Cero fuentes en azul o colores decorativos.
  - Jerarquía de tamaños:
    - Título principal: Arial 18 pt, Negrita, Negro.
    - Encabezados principales (H1): Arial 14 pt, Negrita, Negro.
    - Subtítulos / Subsecciones (H2): Arial 12 pt, Negrita, Negro.
    - Cuerpo de texto: Arial 11 pt, Regular, Negro, interlineado 1.15, espaciado posterior 6 pt.
  - Código o comandos: Consolas 10 pt, negro, con sangría simple.
  - Tablas: Bordes sencillos negros o grises delgados, encabezado en negrita, fondo blanco o neutro, sin rellenos llamativos.


