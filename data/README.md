# Datasets: Visualización de Datos Personales (InfoVis ECD.2026.B)

Este directorio contiene los datasets crudos y consolidados del trabajo práctico personal de **Tomas Ottobre**.

## Estructura de Archivos

| Archivo | Filas | Variables | Descripción |
|---|---|---|---|
| `antropometria_historica.csv` | 10 | 30 | Evaluaciones antropométricas clínicas (certificación ISAK 1) realizadas entre mayo de 2024 y agosto de 2026. Incluye peso, talla, IMC, 8 pliegues cutáneos (tríceps, subescapular, bíceps, cresta ilíaca, supraespinal, abdominal, muslo anterior, pantorrilla medial), perímetros musculares, composición corporal (% grasa, masa magra) y coordenadas de la Somatocarta de Heath-Carter (X, Y). |
| `actividades_consolidadas.csv` | 175 | 13 | Registro unificado y deduplicado de entrenamientos aeróbicos y de fuerza provenientes de **Garmin Connect** y **Nike Run Club**. Contiene fecha, tipo de actividad (Running, Natación, Ciclismo, Fuerza, Cinta), distancia en km, duración en minutos, calorías, frecuencia cardíaca media, ritmo y asignación al período antropométrico correspondiente. |
| `master_antropometria_periodos.csv` | 9 | 26 | Dataset analítico consolidado por intervalo entre controles antropométricos consecutivos. Cruza la carga real de entrenamiento (km de running, metros de natación, sesiones) con la respuesta morfológica del cuerpo ($\Delta$ masa magra en kg, $\Delta$ grasa %, $\Delta$ sumatoria de pliegues en mm y desplazamiento en la Somatocarta). |

*Nota: Datasets consolidados provisoriamente para la entrega del prototipo (Clase 5). Sujetos a eventual incorporación de registros de ingresos a gimnasio (SportClub).*
