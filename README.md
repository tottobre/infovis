# De Gymrat a correr una maratón: cuerpo y hábitos

> **Trabajo Práctico:** Visualización de Datos Personales  
> **Carrera:** Maestría en Ciencia de Datos (MCD) / Especialización en Ciencia de Datos (ECD) — ITBA  
> **Materia:** Visualización de la Información  
> **Profesor:** Ariel Aizemberg  
> **🚀 Presentación en vivo del TP:** [https://tottobre.github.io/infovis/presentacion.html](https://tottobre.github.io/infovis/presentacion.html)  
> **🌐 Ejercicios de clase:** [https://tottobre.github.io/infovis/](https://tottobre.github.io/infovis/)

---

## 🎯 Motivación y Narrativa

Durante años mantuve una rutina estricta de gimnasio enfocada en el entrenamiento de fuerza y la hipertrofia muscular. Sin embargo, a principios de 2024 encaré un objetivo opuesto: preparar y completar los 42.195 km de la **Maratón de Buenos Aires**.

Este proyecto no aborda la maratón únicamente como un logro deportivo, sino como una **transformación de hábitos y biometría documentada paso a paso**. A lo largo de 9 meses se registraron más de 500 sesiones, telemetría cardíaca continua y mediciones antropométricas clínicas para responder cómo el cuerpo y los tiempos personales debieron adaptarse para cruzar la meta.

---

## 📊 Matriz de Visualizaciones y Herramientas

Cumpliendo con la consigna de la cátedra, cada visualización está encabezada por una **pregunta disparadora**, respeta la taxonomía de escalas de medición (NOIR) y la justificación cromática:

| Diapositiva | Herramienta | Pregunta Disparadora | Tipo de Gráfico | Variables y Escalas (NOIR) |
|---|---|---|---|---|
| **Slide 01** | **Datawrapper** | *¿A qué hora y qué días entrenaba normalmente?* | Matrix Heatmap | Días de semana (Ordinal), Franja horaria (Intervalo), Frecuencia de accesos (Razón - Paleta secuencial). |
| **Slide 02** | **Flourish Studio** | *¿Cómo el running fue ganándole terreno a todo lo demás?* | Bar Chart Race | Meses (Intervalo/Tiempo), Disciplinas deportivas (Nominal - Paleta cualitativa), Horas acumuladas (Razón). |
| **Slide 03** | **Flourish Studio** | *¿Qué disciplina demanda mayor exigencia cardiovascular y gasto calórico?* | Scatter Multivariable | Duración en minutos (Razón - Eje X), FC Pico en bpm (Razón - Eje Y), Calorías quemadas (Razón - Tamaño de burbuja), Disciplina (Nominal - Color). |
| **Slide 04** | **Tableau Public** | *¿Cómo varió la masa muscular según el tipo y volumen de entrenamiento?* | Dashboard Interactivo | Horas mensuales por disciplina (Razón), Masa muscular en kg (Razón), Fechas (Intervalo temporal). |
| **Slide 05** | **Datawrapper** | *¿Cómo impactó la preparación en mi masa muscular y grasa corporal?* | Small Multiples Line Chart | Controles antropométricos temporales (Intervalo), Masa muscular en kg y Masa grasa en kg (Razón con escalas independientes). |
| **Slide 06** | **RAWGraphs** | *¿Cómo cambió la intensidad del esfuerzo mes a mes?* | Timeline de Zonas Cardíacas (SVG Interactivo) | Meses de preparación (Intervalo), Kilómetros acumulados (Razón), Zonas cardíacas 1 a 5 (Ordinal con codificación de color por nivel de esfuerzo). |
| **Slide 07** | **HTML / CSS** | *El balance: ¿Valió la pena el esfuerzo?* | Tabla Comparativa, Conclusiones y Cierre | Comparación Antes (Mayo) vs Después (Septiembre), aprendizajes y registro fotográfico finisher con medalla. |

---

## 📁 Linaje y Estructura de Datos

Para garantizar la reproducibilidad y transparencia científica exigida por la cátedra, los datos se encuentran estructurados en directorios dedicados:

```
infovis/
├── index.html                           # Ejercicios prácticos de clase (GitHub Pages root)
├── presentacion.html                    # Presentación interactiva completa del TP de Datos Personales
├── rawgraphs_zonas_final.svg            # Gráfico vectorial interactivo de zonas cardíacas
├── assets/
│   └── tomas_maraton_42k.jpg            # Fotografía finisher oficial con medalla
├── data/
│   ├── raw/                             # Fuentes originales sin modificar
│   │   ├── garmin_Activities_original.csv   # Telemetría de 75 actividades de running (Garmin Connect)
│   │   ├── reporte_accesos_sportclub.xlsx   # 537 accesos por molinete RFID y reservas de boxes
│   │   ├── antropometria_historica.csv      # 10 controles con antropometrista ISAK 1 (calibre Harpenden)
│   │   ├── nike_activities.csv              # Registros históricos Nike Run Club
│   │   ├── nike_activities_raw.json         # Payload JSON original de Nike
│   │   └── xiaomi_zepp_export.zip           # Exportación cruda de pulsera inteligente
│   └── processed/                       # Datasets curados y limpios para cada herramienta
│       ├── heatmap_horarios_raw.csv         # Matriz 7 días x 16 franjas horarias
│       ├── heatmap_horarios_transpuesto.csv # Dataset para Datawrapper Heatmap
│       ├── flourish_bar_chart_race_*.csv    # Series mensuales para Flourish
│       ├── tableau_sesiones_completas.csv   # Dataset maestro para Tableau Public
│       ├── datawrapper_small_multiples_*.csv# Series de masa muscular y grasa
│       └── rawgraphs_*.csv                  # Tablas de fondos y zonas cardíacas
└── README.md
```

---

## 🛠️ Herramientas Empleadas

- **Visualización No-Code / Interactiva:** Datawrapper, Flourish Studio, Tableau Public, RAWGraphs.
- **Wrangling y Curaduría de Datos:** Python 3 (Pandas) para estandarización de fechas, limpieza de valores atípicos y unión de tablas.
- **Edición y Optimización Gráfica:** Inkscape / SVG manipulable para anotaciones directas y corrección tipográfica.
- **Alojamiento y Despliegue:** GitHub Pages con arquitectura responsive (compatible con proyector de aula, escritorio y móvil).