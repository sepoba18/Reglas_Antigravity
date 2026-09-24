# Guía Rápida de Git y GitHub CLI (`gh`)

Esta guía explica de forma clara y sin tecnicismos complejos para qué sirven los comandos esenciales de Git y cómo crear repositorios directamente desde la terminal.

---

## 1. La metáfora para entender Git

Imagina que estás preparando un paquete para enviar por encomienda:

1. **Tu carpeta de trabajo:** Es tu mesa de trabajo con archivos.
2. **`git add .`:** Tomas todos los archivos modificados y los metes dentro de la caja (preparar el paquete).
3. **`git commit -m "mensaje"`:** Cierras la caja con cinta y le pegas una etiqueta que dice qué contiene (guardar una versión en tu PC).
4. **`git push`:** Llevas la caja a la sucursal de envíos y la mandas a la nube de GitHub (subir los cambios).
5. **`git pull`:** Vas a la sucursal a retirar las cajas nuevas que se enviaron desde tu otro computador (bajar los cambios).

---

## 2. Los comandos del día a día

### Para subir tus cambios (al terminar o cambiarte de PC):
```bash
git add .
git commit -m "descripción de lo que hiciste"
git push
```

### Para descargar los cambios (cuando llegas al otro PC):
```bash
git pull
```

### Para ver si tienes cambios pendientes o si todo está al día:
```bash
git status
```

---

## 3. Crear un repositorio en GitHub sin abrir la web

Para crear un repositorio directamente desde la terminal usamos la herramienta **GitHub CLI (`gh`)**.

### Paso a paso desde una carpeta nueva de proyecto:

1. **Iniciar el proyecto con Git en tu PC:**
   ```bash
   git init -b main
   ```

2. **Preparar y guardar tu primer commit:**
   ```bash
   git add .
   git commit -m "feat: commit inicial del proyecto"
   ```

3. **Crear el repositorio en GitHub y subirlo de una sola vez:**
   * **Si lo quieres Privado (solo tú lo ves):**
     ```bash
     gh repo create nombre-de-tu-proyecto --private --source=. --remote=origin --push
     ```
   * **Si lo quieres Público (cualquiera lo puede ver):**
     ```bash
     gh repo create nombre-de-tu-proyecto --public --source=. --remote=origin --push
     ```

### ¿Qué significa cada parte de ese comando?
* `gh repo create`: Comando para crear el repositorio en tu cuenta de GitHub.
* `nombre-de-tu-proyecto`: El nombre que tendrá en GitHub.
* `--private` / `--public`: Define la visibilidad.
* `--source=.`: Le dice que use la carpeta actual (`.`) como el contenido del repositorio.
* `--remote=origin`: Configura el enlace remoto automáticamente con el nombre estándar `origin`.
* `--push`: Sube tus archivos inmediatamente tras crearlo.

---

## 4. Clonar un repositorio existente en tu otro PC

Cuando ya creaste el repositorio y te sientas en el otro computador por primera vez:

```bash
git clone https://github.com/sepoba18/nombre-de-tu-proyecto.git
```
*(Luego solo usas `git pull` y `git push` en el día a día).*
