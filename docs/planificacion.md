# Planificación del proyecto

**Proyecto:** Predicción de bajas voluntarias de empleados
**Empresa (simulada):** TechNova S.A. – Gerencia de Capital Humano
**Duración:** 4 semanas (2 sprints de 2 semanas)

---

## 1. Problema

La empresa registra una tasa de bajas voluntarias del **16%**. Hoy Recursos Humanos se entera cuando el empleado ya presentó la renuncia, sin margen para actuar.

| Pregunta | Respuesta |
|---|---|
| ¿Qué problema tiene la empresa? | Pierde empleados sin anticiparlo. |
| ¿A quién afecta? | A los equipos que quedan con vacantes, a RRHH y a los líderes. |
| ¿Por qué es importante? | Cada baja implica costos de búsqueda, capacitación y pérdida de conocimiento. |
| ¿Cómo ayuda la Ciencia de Datos? | Un modelo puede estimar qué empleados tienen mayor probabilidad de irse para priorizar conversaciones de retención. |

## 2. Objetivos

**Objetivo general:** desarrollar un prototipo de Red Neuronal Artificial que estime la probabilidad de baja voluntaria de un empleado.

**Objetivos específicos:**
1. Analizar los datos históricos de empleados e identificar variables asociadas a las bajas.
2. Preparar los datos para el entrenamiento (codificación, división y normalización).
3. Entrenar y evaluar el modelo, buscando detectar al menos el **70%** de las bajas reales (recall) en los datos de prueba.
4. Documentar el proyecto y sus implicancias éticas.

## 3. Alcance

| Incluye | No incluye |
|---|---|
| Análisis exploratorio del dataset | Uso de datos reales de empleados |
| Preparación de datos | Implementación productiva / despliegue en la nube |
| Entrenamiento y evaluación del modelo | Integración con el sistema de RRHH |
| Informe de ética | Tablero de visualización (queda en el backlog) |
| Documentación y presentación | Acciones de retención sobre personas |

## 4. Recursos

| Tipo | Detalle |
|---|---|
| Humanos | Equipo simulado (ver punto 5) |
| Tecnológicos | Python, Jupyter, pandas, scikit-learn, TensorFlow/Keras, matplotlib, Git/GitHub, Trello, Canva |
| Información | Dataset público *IBM HR Analytics Employee Attrition* (1.470 registros, datos ficticios) |
| Tiempo | 4 semanas (2 sprints de 2 semanas) |
| Económicos | Sin costo: herramientas gratuitas |

## 5. Roles del equipo

> El trabajo es individual. El autor asume como rol principal el de **Scrum Master** (facilita el proceso, los eventos y la gestión de conflictos); los demás roles son simulados y también los ejecuta el autor, separando en cada tarea la responsabilidad de cada rol.

| Rol Scrum | Rol técnico | Responsabilidad |
|---|---|---|
| Product Owner | Gerente de Capital Humano (cliente) | Define y prioriza el backlog, acepta los entregables. |
| Scrum Master **(autor)** | Líder del proyecto | Facilita los eventos, remueve impedimentos, cuida el proceso. |
| Equipo de desarrollo | Ingeniero de Datos | Obtiene, valida y organiza los datos. |
| Equipo de desarrollo | Científico de Datos | Prepara los datos, entrena y evalúa el modelo. |
| Equipo de desarrollo | Analista BI / Datos | Análisis exploratorio, gráficos y comunicación de resultados. |

## 6. Product Backlog

Prioridad: **Alta / Media / Baja**. Estimación en puntos de historia (1, 2, 3, 5).

| ID | Historia de usuario | Prioridad | Puntos | Sprint |
|---|---|---|---|---|
| HU01 | Como **Gerente de RRHH** quiero conocer la tasa de bajas actual para dimensionar el problema. | Alta | 2 | 1 |
| HU02 | Como **Ingeniero de Datos** quiero obtener y validar el dataset (faltantes, tipos) para trabajar con datos confiables. | Alta | 2 | 1 |
| HU03 | Como **Analista** quiero identificar las variables asociadas a las bajas para orientar el modelo. | Alta | 3 | 1 |
| HU04 | Como **Científico de Datos** quiero preparar los datos (codificación, división, normalización) para entrenar el modelo. | Alta | 3 | 1 |
| HU05 | Como **Gerente de RRHH** quiero un modelo que estime la probabilidad de baja de cada empleado para priorizar conversaciones. | Alta | 5 | 1 |
| HU06 | Como **Gerente de RRHH** quiero saber qué tan confiable es el modelo para decidir cómo usarlo. | Alta | 3 | 1 |
| HU07 | Como **equipo** queremos definir qué variables no se usan por razones éticas para evitar discriminación. | Alta | 2 | 1 |
| HU08 | Como **Gerente de RRHH** quiero un informe de ética que indique cómo usar el modelo de forma responsable. | Alta | 2 | 2 |
| HU09 | Como **equipo** queremos documentar el proyecto en GitHub para que cualquiera pueda entenderlo y ejecutarlo. | Media | 3 | 2 |
| HU10 | Como **Product Owner** quiero una presentación ejecutiva para mostrar los resultados al comité. | Alta | 3 | 2 |
| HU11 | Como **Gerente de RRHH** quiero un tablero de visualización con el riesgo por área. | Baja | 5 | — |
| HU12 | Como **Gerente de RRHH** quiero integrar el modelo al sistema de RRHH. | Baja | 5 | — |

HU11 y HU12 quedan en el backlog para una próxima etapa (fuera de alcance).

## 7. Sprint Planning

| Sprint | Duración | Objetivo del sprint | Historias | Puntos |
|---|---|---|---|---|
| Sprint 1 | Semanas 1 y 2 | Tener un modelo entrenado y evaluado con variables éticamente aceptables. | HU01 a HU07 | 20 |
| Sprint 2 | Semanas 3 y 4 | Entregar el proyecto documentado y la presentación final. | HU08 a HU10 | 8 |

**Cronograma**

| Semana | Actividad |
|---|---|
| 1 | Definición del problema, obtención y análisis exploratorio de los datos (HU01–HU03). |
| 2 | Preparación de datos, entrenamiento y evaluación del modelo, decisión ética de variables (HU04–HU07). |
| 3 | Informe de ética y documentación en GitHub (HU08–HU09). |
| 4 | Presentación final (HU10). |

El detalle de cada sprint está en [`sprints.md`](sprints.md).

## 8. Riesgos

| Riesgo | Mitigación |
|---|---|
| Datos desbalanceados (pocas bajas) | Usar pesos por clase y evaluar con recall, no solo con exactitud. |
| Sesgo / discriminación del modelo | Excluir variables sensibles (ver [`etica.md`](etica.md)). |
| Retraso en actividades | Priorizar historias de valor alto; dejar HU11 y HU12 fuera del alcance. |
| Resultados poco precisos | Comunicar las limitaciones; el modelo es de apoyo, no de decisión. |
| Problemas de instalación de librerías | Documentar versiones en `requirements.txt`. |

## 9. Entregables

1. Documento de planificación (este archivo).
2. Dataset documentado (`data/`).
3. Notebook con el modelo (`notebooks/prediccion_bajas.ipynb`) y modelo guardado (`modelo_bajas_entrenado.keras`).
4. Registro de sprints, conflicto y retrospectivas (`docs/sprints.md`).
5. Informe de ética (`docs/etica.md`).
6. README del repositorio.
7. Tablero de Trello.
8. Presentación final en Canva ([ver presentación](https://canva.link/r8wamuazr03loi7)).
