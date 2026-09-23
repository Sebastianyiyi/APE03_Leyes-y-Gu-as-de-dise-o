# 📋 Informe de Evaluación y Rediseño de Interfaz - Sistema GITT

Este repositorio contiene el informe y la documentación del proceso de evaluación, rediseño y validación de usabilidad centrado en el usuario para el módulo de Configuración (**Condiciones** y **Estados**) del sistema de Gestión de Inventario de Talleres Tecnológicos (GITT). 

El proyecto aplica de forma rigurosa las **Leyes de Gestalt** y los lineamientos de Usabilidad e Interacción Humano-Computador establecidos por la norma **ISO 9241-210 / ISO 9241-11**.

---

## 👥 Integrantes del Proyecto
* **Acaro Ibujés Pedro Sebastián**
* **González Álvarez Vladimir Humberto**
* **Mora Beltrán Santiago Sebastian**
* **Vinces Cueva Boris Yussef**

---

## 🎯 Objetivos

### Objetivo General
* Utilizar las leyes de Gestalt en un diseño de interfaz de usuario.

### Objetivos Específicos
1. Identificar las deficiencias perceptuales en la interfaz actual del sistema mediante el análisis de la disposición espacial y gráfica de sus elementos.
2. Reestructurar la presentación de datos en tablas y formularios aplicando los principios de proximidad, continuidad y figura-fondo para reducir la carga visual.
3. Estandarizar la retroalimentación visual y el contraste de los componentes interactivos para garantizar una navegación intuitiva y orientada a la tarea.

---

## 🛠️ Desarrollo por Fases

### 🔹 Fase 1: Ficha de Diseño Conceptual
Se definió el concepto central de **"Libertad"**, el cual se traduce en brindar al usuario el control total sobre sus acciones dentro del sistema sin riesgo de pérdida de datos. Se estructuraron 5 garantías de diseño:
* **Punto de partida único:** Toda operación nace del listado principal.
* **Salida siempre visible:** Uso de migas de pan y botones "Cancelar" explícitos.
* **Filtro reversible:** Búsquedas anulables en un solo clic.
* **Acciones destructivas rechazables:** Confirmación obligatoria previa a eliminar.
* **Retroalimentación constante:** Mensajes de estado y éxito al finalizar procesos.

Se fundamentó el ordenamiento de los elementos aplicando la **Ley de Continuidad de Gestalt**, asegurando alineaciones en ejes verticales y horizontales constantes para generar un patrón de recorrido visual en "Z".

---

### 🔹 Fase 2: Prototipado de Alta Fidelidad
Se diseñaron componentes estandarizados replicados en ambos apartados para reducir la curva de aprendizaje:
* **Listados:** Tablas estructuradas con alineación vertical estricta, insignias de estado (*badges*) y paginación inferior.
* **Formularios:** Organización a dos columnas (panel explicativo a la izquierda y campos de entrada alineados a la derecha).
* **Prevención de errores:** Inclusión de contadores de caracteres (0/25 y 0/250) e interruptores gráficos.

---

### 🔹 Fase 3: Evaluación de la Percepción y Carga Cognitiva

Pese a que el sistema web es funcional, la interfaz evaluada presentó falencias críticas en UX/UI:

* **Redundancia de Información (Carga Cognitiva):** Formularios con hasta 4 niveles de instrucciones y títulos duplicados, generando fatiga visual y violando la norma ISO 9241-11.
* **Ley de Proximidad y Continuidad:** Separación excesiva entre los datos del registro y sus íconos de acción en las tablas, forzando la vista y elevando el riesgo de selecciones erróneas.
* **Ley de Figura-Fondo y Contraste:** El menú lateral activo presentó un contraste deficiente (1.3:1), dificultando ubicar la sección actual de un vistazo.
* **Retroalimentación Distante:** Notificaciones flotantes de éxito desplegadas en la esquina inferior derecha, alejadas del foco de atención principal ubicado al centro de la pantalla.
* **Distractores Visuales (Ruido):** Presencia de caracteres residuales (`;`) flotando en el área inferior del lienzo.

---

### 🔹 Fase 4: Validación y Mejora Iterativa (ISO 9241-210)
Se realizó un estudio de usabilidad con **10 usuarios representativos** (Responsables de taller, Docentes y Estudiantes) organizados en dos iteraciones de prueba.

#### Métricas y Evolución de Resultados:
| Indicador Global | Sistema Actual (Base) | Prototipo It. 1 | Prototipo Mejorado (It. 2) | Criterio Aceptación |
| :--- | :---: | :---: | :---: | :---: |
| **Tasa de Éxito Global** | 70% | 90% | **97.5%** | ≥ 90% |
| **Tiempo Total Tareas** | 262 s | 175 s | **135 s** | ≤ 170 s |
| **Errores por Usuario** | 0.55 | 0.23 | **0.05** | ≤ 0.2 |
| **Satisfacción (SUS)** | 55.5 | 75.0 | **83.5** | ≥ 80 |
| **Carga Cognitiva (NASA-RTLX)** | 46 | 31 | **22** | ≤ 30 |

#### Principales Refinamientos Aplicados:
1. **M-01 (Buscador):** Se agregó botón de limpieza `×` e interacción con la tecla `Esc`.
2. **M-02 (Acciones de Fila):** Se ampliaron las áreas de clic a 40 × 40 px (Ley de Fitts) y se añadieron *tooltips* descriptivos.
3. **M-03 (Notificaciones):** La retroalimentación de éxito se reubicó de manera anclada justo sobre la tabla de datos.
4. **M-08 (Figura-Fondo):** Se añadió una barra de acento `#E05A50` en el ítem activo del menú para alcanzar un contraste accesible de 5.1:1.

---

## 📈 Conclusiones

1. La práctica demostró que la aplicación de las Leyes de Gestalt es una herramienta diagnóstica esencial para identificar problemas de usabilidad que van más allá del funcionamiento técnico, evidenciando que la correcta organización visual de los elementos incide directamente en la reducción de la carga cognitiva.
2. Se corroboró de manera empírica cómo el incumplimiento de los lineamientos de eficiencia y satisfacción de la norma ISO 9241-210 en un entorno real afecta la fluidez del operador, reafirmando que el diseño centrado en el usuario debe ser un eje transversal en el desarrollo y no un complemento estético.
3. El análisis permitió comprender que anomalías perceptuales aparentemente menores, como la falta de continuidad en una tabla o un contraste deficiente, exigen un esfuerzo consciente por parte del cerebro para ser procesadas, lo que resalta la necesidad de mantener un rigor analítico meticuloso al evaluar interfaces gráficas.

---

## 💡 Recomendaciones

1. Se recomienda integrar evaluaciones heurísticas basadas en los principios de Gestalt de forma iterativa durante el ciclo de vida del desarrollo de software, permitiendo detectar y corregir problemas de percepción antes de que el sistema llegue a la fase de producción.
2. Es aconsejable fomentar el uso de guías de estilo o sistemas de diseño (*Design Systems*) estandarizados que provean componentes con jerarquías visuales, contrastes y agrupaciones predefinidas, mitigando así el riesgo de introducir errores de proximidad o redundancia.
3. Se sugiere extender este tipo de metodologías de análisis práctico hacia otros entornos digitales, como aplicaciones móviles o cuadros de mando (*dashboards*) complejos, con el fin de afianzar las competencias diagnósticas frente a diferentes paradigmas de interacción y flujos de trabajo.
