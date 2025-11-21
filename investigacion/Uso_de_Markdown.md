## ¿Qué es Markdown?

**Markdown** es un **lenguaje de marcado ligero** cuyo principal objetivo es permitir a las personas escribir en un formato de **texto plano** fácil de leer y escribir, para luego convertirlo de manera sencilla a HTML o a otros formatos.

Markdown se basa en convenciones de formato que ya se usaban en el correo electrónico. Por ejemplo, al rodear una palabra con asteriscos (`*palabra*`), se indica que debe estar en **cursiva**.

### Por qué se utiliza en proyectos de software

Markdown es el estándar *de facto* para la documentación en el desarrollo de software por estas razones:

  * **Legibilidad del Código Fuente:** A diferencia de lenguajes como HTML, el texto fuente de Markdown es muy legible y limpio, incluso antes de ser renderizado.
  * **Sencillez y Rapidez:** Su sintaxis mínima se aprende en minutos, lo que agiliza la creación de documentación esencial como archivos **README**, wikis y *changelogs*.
  * **Control de Versiones:** Al ser texto plano, sistemas como Git pueden rastrear y mostrar los cambios (**diffs**) de manera precisa y eficiente, facilitando la colaboración.
  * **Estándar de la Industria:** Es compatible con la mayoría de las plataformas de desarrollo y comunidades técnicas (GitHub, GitLab, Stack Overflow, etc.).

-----

##  Ejemplo Práctico de Uso de Markdown

El siguiente código muestra la sintaxis de Markdown para los elementos más comunes:

````markdown
# Título Principal del Proyecto (H1)
##  Módulo de Requerimientos (H2)

Este es un párrafo de texto normal que introduce la idea.
Se usa **doble asterisco** para el énfasis fuerte (Negrita).
Se usa *un solo asterisco* para el énfasis suave (Cursiva).

### Lista de Tareas Pendientes (H3)

* [ ] Configurar el entorno de desarrollo.
* [x] Definir los requerimientos funcionales.
* [ ] Implementar la función de registro.

### Enlaces y Código

Para ir al sitio web de Markdown, haz clic en [este enlace](https://daringfireball.net/projects/markdown/).

El nombre de la función es `calcularBalance()` (código en línea).

```python
# Bloque de código Python
def calcular_area(radio):
    return 3.14 * radio**2
````

### Tabla de Prioridades

| Funcionalidad | Prioridad | Estado |
| :--- | :---: | ---: |
| Registro de usuario | Alta | correcto|
| Recuperación de contraseña | Media | proceso |
| Cierre de sesión | Alta | correcto|

```

---

## 🔗 Ventajas de utilizar Markdown en combinación con GitHub

GitHub y Markdown son una combinación poderosa que optimiza la gestión de proyectos y la colaboración.

* **Visualización Automática (README.md):** GitHub renderiza automáticamente cualquier archivo llamado `README.md` como la página principal del repositorio. Esto proporciona una **tarjeta de presentación** profesional e informativa del proyecto, con instrucciones claras y directas. 
* **Colaboración Estructurada:** Los desarrolladores utilizan Markdown para describir *Issues* (errores) y *Pull Requests* (solicitudes de cambio). El formato permite usar **listas de tareas** y **bloques de código** para garantizar que la comunicación sea clara y concisa, reduciendo ambigüedades.
* **Historial de Documentación (Git):** Dado que la documentación (READMEs, Wikis) está escrita en texto plano, Git puede rastrear los cambios con granularidad. Si se introduce un error en la documentación, es fácil ver el *diff* (la diferencia) y **revertir** el cambio.
* **Uso en la Interfaz:** Markdown se utiliza en toda la interfaz de GitHub: en los **comentarios** de *commits*, en la descripción de los **lanzamientos** (*Releases*) y en el **Wiki** del proyecto, asegurando un formato de documentación consistente y simple en todos los ámbitos.
```
