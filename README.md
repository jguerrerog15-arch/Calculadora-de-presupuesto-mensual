#  Calculadora de Presupuesto Mensual

---

## Introducción, Finalidad y Objetivos del Proyecto

El presente documento combina la explicación de las herramientas de documentación esenciales con la especificación técnica del proyecto **"Calculadora de Presupuesto Mensual"**.

###  Finalidad y Propósito General

La Calculadora de Presupuesto Mensual es una herramienta digital práctica y eficiente diseñada para que los usuarios lleven un control detallado de sus finanzas. Su función principal es registrar **ingresos** y **gastos** para realizar los cálculos necesarios y obtener un **balance final** claro, fomentando la **educación financiera personal**.

### Evolución y Objetivos del Alcance

| Versión | Alcance Principal | Énfasis |
| :--- | :--- | :--- |
| **V1 (Inicial)** | Registro simple en memoria y cálculo inmediato del balance. | Sencillez y Fiabilidad, con cálculos menores a **1 segundo**. |
| **V2 (Mejorada)** | Análisis visual, edición de registros, historial y mayor usabilidad. | Robustez, visualización gráfica y **Responsividad para móviles**. |

---

##  Fundamentos del Lenguaje Markdown

### ¿Qué es Markdown y por qué se utiliza en proyectos de software?

**Markdown** es un **lenguaje de marcado ligero** diseñado para que la creación de documentación sea fácil de leer y escribir en formato de **texto plano**. Su objetivo es permitir la conversión sencilla y estructuralmente válida a HTML.

**Utilidad en Software:**
1.  **Legibilidad:** Su código fuente es muy legible, lo que simplifica la auditoría de la documentación.
2.  **Control de Versiones:** Al ser texto plano, herramientas como Git pueden rastrear y mostrar los cambios (**diffs**) de manera precisa.
3.  **Estándar:** Es el formato universal para documentación en plataformas de desarrollo como GitHub.

### Ejemplo Práctico de Uso de Markdown

| Elemento | Código Markdown |
| :--- | :--- |
| **Encabezado principal** | `# Título de Documentación` |
| **Lista ordenada** | `1. Primer paso\n2. Segundo paso` |
| **Énfasis (Negrita)** | `El saldo es **crítico**` |
| **Bloque de código** | \`\`\`js\nconst saldo = ingresos - gastos;\n\`\`\` |
| **Enlace** | `[Ver Repositorio](https://github.com/proyecto)` |

### Ventajas de utilizar Markdown en combinación con GitHub

* **Página de Inicio:** GitHub renderiza automáticamente el archivo `README.md`, actuando como la tarjeta de presentación del proyecto.
* **Flujo de Trabajo:** Se utiliza en la descripción de *Issues* y *Pull Requests* para estructurar la comunicación (ej. usando listas de tareas `- [ ]`).
* **Trazabilidad:** El Control de Versiones garantiza que todos los cambios en la documentación (Mantenimiento Adaptativo o Evolutivo) sean claros y reversibles.

---

## Requerimientos Funcionales y No Funcionales – Versión 1

### Requerimientos Funcionales (V1)
| Descripción | Prioridad | Justificación |
| :--- | :--- | :--- |
| Permitir al usuario ingresar el monto total de ingresos mensuales. | Alta | Fundamental para el cálculo del balance. |
| Registrar y clasificar gastos mensuales por categorías. | Alta | Permite análisis detallado del presupuesto. |
| Calcular automáticamente el balance mensual (ingresos – gastos). | Alta | Núcleo funcional del sistema. |
| Mostrar un resumen con total de ingresos, total de gastos y balance resultante. | Media | Mejora comprensión y transparencia del resultado. |
| Permitir limpiar los datos ingresados para iniciar un nuevo cálculo. | Media | Facilita la usabilidad y continuidad de uso. |

### Requerimientos No Funcionales (V1)
| Descripción | Categoría | Prioridad |
| :--- | :--- | :--- |
| La interfaz debe ser simple y clara. | Usabilidad | Alta |
| El tiempo de cálculo no debe superar **1 segundo** (según DRS). | Rendimiento | Alta |
| Los datos deberán mantenerse en memoria hasta que el usuario decida reiniciar o cerrar. | Fiabilidad | Media |
| Debe funcionar en cualquier navegador actual. | Portabilidad | Media |

---

##  Requerimientos Funcionales y No Funcionales – Versión Mejorada (V2)

### Requerimientos Funcionales (V2)
1.  **Registrar gastos** con categoría, descripción y monto (RF1).
2.  **Editar y eliminar** gastos registrados (RF2).
3.  **Calcular porcentaje** de gasto por categoría (RF3).
4.  Generar **gráfico circular** de distribución de gastos (RF4).
5.  Mantener historial de gastos durante la sesión (RF5).
6.  Incluir **validación de campos** (Mejora).
7.  **Mejorar la organización** del resumen (Mejora).

### Requerimientos No Funcionales (V2)
* **Responsividad para móviles** (RNF1).
* Código modular para **fácil mantenimiento** (RNF2).
* Interfaz legible y amigable (RNF3).
* **Rendimiento:** Gráficos generados en menos de **2 segundos**.
* **Seguridad:** Almacenamiento de contraseñas con cifrado (para futura persistencia de datos).

---

## Plan de Pruebas: Casos Críticos

Las pruebas unitarias y de validación aseguran la conformidad del producto con los criterios definidos, garantizando la precisión de los cálculos financieros.

| Caso de Prueba | Objetivo | Entrada | Resultado Esperado |
| :--- | :--- | :--- | :--- |
| **CP01 (Cálculo)** | Verificar cálculo del saldo. | Ingreso $500, Gasto $100 | Saldo = $400 |
| **CP02 (Validación)** | Validar errores por campos vacíos. | Gasto sin monto | "El monto es obligatorio" |
| **CP03 (Porcentaje)** | Calcular porcentaje de gastos. | Ingreso $1000, Gastos $250 | 25% |

---

##  Plan de Mantenimiento de Software

El plan de mantenimiento tiene como objetivo asegurar la estabilidad, vigencia y crecimiento del sistema.

| Tipo de Mantenimiento | Descripción y Enfoque | Justificación Principal |
| :--- | :--- | :--- |
| **Correctivo** | Corrección inmediata de errores en cálculos o fallos en el registro/edición de gastos. | Es esencial para la **Fiabilidad**. Asegura que el núcleo funcional se ejecute sin errores. |
| **Adaptativo** | Ajustes para operar con nuevas resoluciones, sistemas operativos o librerías obsoletas. | Protege la inversión de software contra la **obsolescencia tecnológica** (Vigencia Tecnológica). |
| **Perfectivo** | Mejoras en el rendimiento (ej. velocidad de cálculo de porcentajes) y optimización de la interfaz (Usabilidad). | Mejora la experiencia del usuario y extiende el ciclo de vida útil del sistema. |
| **Evolutivo** | Adición de nuevas funcionalidades (ej. exportación a PDF o soporte de múltiples monedas). | Proporciona el marco para el **crecimiento**, añadiendo funciones futuras excluidas inicialmente. |

---

##  Reflexión sobre el Control de Versiones (Git)

El Control de Versiones (VCS) es la columna vertebral de la **confianza** y **estabilidad** del proyecto.

### 1. Protección y Mantenimiento Correctivo
El VCS permite **auditar la precisión** de la lógica financiera. Si se introduce un *bug* en el cálculo del balance, el VCS permite identificar **qué** línea cambió y realizar un **Rollback** a un estado estable anterior en segundos, minimizando la interrupción (Gestión del Riesgo y **Fiabilidad**).

### 2. Soporte al Crecimiento y Evolución
* **Bifurcación (*Branching*):** Es fundamental para el **Mantenimiento Evolutivo**. El desarrollo de la **persistencia de datos** (pasar de "en memoria" a almacenamiento local) se haría en una rama dedicada (`feature/almacenamiento-local`) sin riesgo de estropear la calculadora básica.
* **Aislamiento Crítico:** Permite aislar los ajustes de optimización de código (Mantenimiento Perfectivo) en ramas pequeñas para mejorar el **Rendimiento** (Alta) sin afectar el código principal.

### 3. Colaboración y Trazabilidad
El VCS facilita la **coordinación de la usabilidad** y el cálculo. Los *commits* se pueden enlazar a tareas del Plan de Pruebas, documentando el progreso y las decisiones de diseño a lo largo del tiempo.
```
