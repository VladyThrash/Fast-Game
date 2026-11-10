# 🎮 Fast-Game

Un juego interactivo construido con HTML, CSS y JavaScript. Este proyecto sirve como práctica principal para aprender el flujo de trabajo básico en **Git y GitHub**.

🚀 **[¡Juega la versión en vivo aquí!](https://vladythrash.github.io/Fast-Game/)**

---

## 📝 Descripción

Fast-Game es un proyecto de código abierto diseñado para aprender y practicar el control de versiones. Durante su desarrollo, aplicamos conceptos clave como:
* Inicialización de repositorios locales y conexión a remotos.
* Creación de `commits` atómicos y descriptivos.
* Uso de `git push` para sincronizar con GitHub.
* Manejo de ramas (`branches`) para agregar nuevas características de forma segura.
* Despliegue gratuito utilizando **GitHub Pages**.

## 🛠️ Tecnologías Utilizadas

* **HTML5:** Estructura del juego.
* **CSS3:** Estilos, animaciones y diseño responsivo.
* **JavaScript (Vanilla):** Lógica del juego e interactividad.
* **Git & GitHub:** Control de versiones y alojamiento.

## 🔀 Lección: Flujo de Integración de Ramas y Resolución de Conflictos

Integrar ramas (**merge**) consiste en unir el trabajo desarrollado en un entorno aislado de vuelta a la rama principal (`main`). A continuación se detallan los tres escenarios de integración utilizados en el curso.

---

### 1. Pull Request desde GitHub

Utilizamos un **Pull Request (PR)** en la plataforma web para revisar e integrar la rama `feature/estilos-neon`.

1. En la interfaz de GitHub, creamos el PR seleccionando `feature/estilos-neon` hacia `main` y confirmamos la fusión haciendo clic en **Merge pull request**.
2. Dado que el cambio ocurrió en la nube, nos movemos a la rama principal en nuestra computadora con `git checkout main` y descargamos la versión actualizada ejecutando `git pull origin main`.

---

### 2. Merge Local desde la Terminal

Para fusionar la rama `feature/dificultad` realizaremos la integración directamente desde la terminal de comandos.

1. Confirmamos que estamos posicionados en la rama receptora ejecutando `git branch` (la rama activa estará marcada con un asterisco `* main`).
2. Absorbemos los cambios de la rama de dificultad corriendo el comando `git merge feature/dificultad`.
3. Finalmente, como la fusión ocurrió en nuestro equipo local, subimos la rama principal actualizada a GitHub con `git push origin main`.

---

### 3. Resolución de Conflictos (Merge Conflict)

Al intentar integrar la rama `bugfix/game-over` se provocará un conflicto intencional porque modificó la misma línea de código en `script.js` que la rama anterior.

1. Estando en la rama `main`, iniciamos la fusión ejecutando `git merge bugfix/game-over`. La terminal arrojará el mensaje de error `CONFLICT (content): Merge conflict in script.js`.
2. Abrimos `script.js` en el editor de código para revisar la estructura del conflicto demarcada por Git:

```javascript
<<<<<<< HEAD
setInterval(cicloJuego, 15);
=======
let intervaloJuego = setInterval(cicloJuego, 30);
>>>>>>> bugfix/game-over
```

## ⚙️ Instalación y Uso Local

Para correr este proyecto en tu propia computadora, sigue estos pasos desde tu terminal:

1. **Clona el repositorio:**
   ```bash
   git clone https://github.com/VladyThrash/Fast-Game.git
