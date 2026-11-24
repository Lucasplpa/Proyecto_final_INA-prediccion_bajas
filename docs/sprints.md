# Registro de Sprints

Seguimiento del trabajo según Scrum: Sprint Planning → Daily → Sprint Review → Sprint Retrospective.
Tablero de seguimiento: **Trello** (enlace en el README).

---

## Sprint 1 – Semanas 1 y 2

### Sprint Planning
- **Objetivo:** tener un modelo entrenado y evaluado con variables éticamente aceptables.
- **Sprint Backlog:** HU01, HU02, HU03, HU04, HU05, HU06, HU07 (20 puntos).

### Daily (resumen)
| Pregunta | Respuesta |
|---|---|
| ¿Qué hice desde la última reunión? | Planificación: problema, objetivos, alcance, roles y backlog. |
| ¿Qué haré hoy? | Obtener el dataset, análisis exploratorio, preparar datos y entrenar el modelo. |
| ¿Hay impedimentos? | Definir qué variables usar: hay diferencia de criterio entre PO y Científico de Datos (ver conflicto). |

### Conflicto y su gestión
| | |
|---|---|
| **Situación** | El Product Owner propuso incluir edad, género y estado civil porque "seguramente influyen en las bajas". El Científico de Datos se opuso por riesgo de discriminación. |
| **Tipo de conflicto** | De tarea (sobre el contenido del trabajo). |
| **Mediación** | El Scrum Master facilitó una reunión breve: escuchar ambas posiciones, separar el problema de las personas y buscar intereses comunes. |
| **Estrategia** | Colaboración (gana-gana): el interés común es detectar bajas **y** que el modelo sea justo. Se acordó decidir con evidencia. |
| **Evidencia** | Se entrenó el modelo con y sin esas variables (anexo del notebook). Con ellas la exactitud sube de 75,5% a 77,6%, pero detecta **menos** bajas (32 vs. 35 de 47). |
| **Acuerdo** | Excluir `Age`, `Gender` y `MaritalStatus`: no mejoran el objetivo del proyecto (detectar bajas) y agregan riesgo de discriminación. |
| **Documentación** | Decisión registrada en el notebook, en este archivo y en [`etica.md`](etica.md). |

### Sprint Review
| Historia | Estado | Resultado |
|---|---|---|
| HU01 | Hecho | Tasa de bajas: 16,1% (237 de 1.470). |
| HU02 | Hecho | Dataset sin datos faltantes, 35 columnas. |
| HU03 | Hecho | Con horas extra la tasa de bajas es 30,5% vs. 10,4% sin horas extra. |
| HU04 | Hecho | 1.176 registros de entrenamiento y 294 de prueba, normalizados. |
| HU05 | Hecho | Red neuronal 16-8-1 (Keras) entrenada y guardada. |
| HU06 | Hecho | Exactitud 75,5%; detecta 35 de 47 bajas reales (recall 74%). |
| HU07 | Hecho | Variables sensibles excluidas. |

**Incremento:** modelo funcional que estima la probabilidad de baja de un empleado.

### Sprint Retrospective
| ¿Qué salió bien? | ¿Qué mejorar? | Acción |
|---|---|---|
| El backlog priorizado permitió enfocarse en lo importante. | La exactitud sola era engañosa por el desbalance. | Evaluar siempre con matriz de confusión y recall. |
| El conflicto se resolvió con datos y quedó documentado. | El modelo genera muchas falsas alarmas (60). | Comunicarlo en el informe de ética y en la presentación. |

---

## Sprint 2 – Semanas 3 y 4

### Sprint Planning
- **Objetivo:** entregar el proyecto documentado y la presentación final.
- **Sprint Backlog:** HU08, HU09, HU10 (8 puntos).

### Daily (resumen)
| Pregunta | Respuesta |
|---|---|
| ¿Qué hice desde la última reunión? | Modelo entrenado y evaluado (Sprint 1 cerrado). |
| ¿Qué haré hoy? | Informe de ética, README y presentación. |
| ¿Hay impedimentos? | Ninguno. |

### Sprint Review
| Historia | Estado | Resultado |
|---|---|---|
| HU08 | Hecho | Informe de ética en `docs/etica.md`. |
| HU09 | Hecho | README completo; cambios integrados a `main` mediante Pull Request. |
| HU10 | Hecho | Presentación final en Canva ([ver presentación](https://canva.link/r8wamuazr03loi7)). |

**Incremento:** proyecto completo, documentado y listo para presentar.

### Sprint Retrospective
| ¿Qué salió bien? | ¿Qué mejorar? | Acción |
|---|---|---|
| Trello y GitHub dieron visibilidad del avance (transparencia). | La documentación se concentró al final del proyecto. | Documentar cada historia apenas se termina. |
| Trabajar en una rama y unir con Pull Request ordenó los cambios. | — | Mantener el flujo rama → Pull Request → `main`. |
