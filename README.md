# Reglas_Antigravity

Estructura de proyecto sincronizada para **Google Antigravity** entre Laptop y PC de Escritorio.

## Estructura
```text
Reglas_Antigravity/
├── .git/
├── .gitignore                    # Ignora archivos temporales y secretos
├── GEMINI.md                     # Reglas del proyecto y protocolo de traspaso
├── CURRENT_TASK.md               # Archivo de traspaso de contexto entre PCs
├── README.md
└── .agents/
    └── skills/                   # Skills compartidas del proyecto
        └── mi-skill/
            └── SKILL.md
```

## Flujo de Trabajo entre Computadores
1. **En la Laptop:**
   - Trabajar normalmente en el proyecto.
   - Al terminar o cambiar de computador, indicar:
     > *"Me paso al PC de escritorio, guarda el avance"*
   - Antigravity actualizará `CURRENT_TASK.md` y hará `git push`.
2. **En el PC de Escritorio:**
   - Descargar los cambios:
     ```bash
     git pull
     ```
   - Indicar a Antigravity:
     > *"Continuemos"*
   - El agente leerá `CURRENT_TASK.md` y continuará sin perder el contexto.
