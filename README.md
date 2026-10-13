# Aplicación del Aprendizaje por Refuerzo en la Gestión y Optimización del Rendimiento Deportivo en Béisbol y Fútbol

**Universidad de Oriente — Facultad de Ingeniería en Telecomunicaciones, Informática y Biomédica**
**Carrera: Ingeniería Informática — Período 2026-2027**

Proyecto experimental que utiliza el algoritmo **Q-Learning** (Aprendizaje por Refuerzo) para seleccionar acciones relacionadas con la intensidad del entrenamiento y la recuperación de atletas de béisbol y fútbol, a partir de estados construidos con variables de fatiga, rendimiento y carga de entrenamiento.

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `Aprendizaje por Refuerzo.md` | Informe completo del proyecto: definición de datos, planteamiento del problema, objetivos, modelo del entorno, configuración experimental, resultados y su interpretación |
| `img/` | Imágenes del informe: logo UDO, diagrama de la interacción agente-entorno y gráfica de evolución de la recompensa |
| `Notebook_Q_Learning.ipynb` | Notebook de Google Colab con todo el código: carga de datos, discretización de estados, entrenamiento Q-Learning y generación de resultados |
| `ElevatorPitch.m4a` | Audio del elevator pitch del proyecto |

## Recursos y enlaces

* **Notebook en Google Colab:** [https://colab.research.google.com/drive/1fWz5IFy-Vba0ngmd4NKluw8_AJ6hVNoq](https://colab.research.google.com/drive/1fWz5IFy-Vba0ngmd4NKluw8_AJ6hVNoq)
* **Dataset de béisbol (Athlete Injury and Performance Dataset, Kaggle):** [https://www.kaggle.com/datasets/ziya07/athlete-injury-and-performance-dataset](https://www.kaggle.com/datasets/ziya07/athlete-injury-and-performance-dataset)
* **Dataset de fútbol (SoccerMon, Zenodo):** [https://zenodo.org/records/10033832](https://zenodo.org/records/10033832)

## Resultados principales

Entrenamiento con 500 episodios, 20 pasos por episodio, α = 0,10, γ = 0,90, ε = 0,20 y semilla 42:

| Deporte | Registros | Recompensa media | Recompensa últimos 50 | Recompensa máxima |
|---|---:|---:|---:|---:|
| Béisbol | 200 | -11,2780 | -9,4827 | 8,0515 |
| Fútbol | 16 983 | -0,4094 | -0,4288 | 17,4253 |

La interpretación detallada de estos resultados (por qué la recompensa media es negativa, la tendencia de aprendizaje observada y el efecto de la exploración épsilon-greedy) se encuentra en el informe `Aprendizaje por Refuerzo.md`, sección *Resultados obtenidos y su interpretación*.

## Cómo ejecutar

1. Abrir `Notebook_Q_Learning.ipynb` en Google Colab (o localmente con Jupyter).
2. Cargar los datasets en las rutas que indica el notebook:
   * Béisbol: `/content/beisbol_dataset/collegiate_athlete_injury_dataset.csv`
   * Fútbol: carpeta `/content/soccer_subjective/subjective/` con las subcarpetas `wellness`, `training-load`, `game-performance` e `injury`
3. Ejecutar todas las celdas. El notebook imprime el resumen por deporte, guarda `resultados_IA_deportes.csv` y dibuja la gráfica de evolución de la recompensa.

## Integrantes

* Alejandro Manuel Tamayo Morales
* Francis Alejandro Liranza Liranza
* Rolando Javier Vila Rodríguez
