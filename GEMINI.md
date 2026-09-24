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
