# MCDI504 – Machine Learning I
## Avance del Proyecto · Fase 1: Definición y orientación de la situación

**Grupo:** GRUPO N°1
**Integrantes:**

- Pablo Ignacio Balbontín Constenla @pabbalbontin-maker
- Melany Esmeralda Reyes Leiva @melanyreyesy
- Ingeborg Andrea Muñoz Carnot @dark452
- Mario Alejandro López Pulgar @malp2203

**Docente:** David Ruete Zuniña
**Fecha:** 8 de agosto de 2026

---

## 1. Descripción del proyecto

Este repositorio contiene la Fase 1 de un proyecto ABP de Machine Learning. La fase **no desarrolla modelamiento**: establece la definición analítica del problema, caracteriza los datos disponibles y justifica la selección del enfoque de aprendizaje, en el marco del proceso KDD.

**Caso.** La Red Nacional de Monitoreo de Biodiversidad (RNMB) registra mediciones morfométricas de ejemplares en campañas de terreno. La determinación de especie está a cargo de un equipo reducido de especialistas, y el crecimiento del volumen de registros (tras incorporar voluntarios a las campañas) generó un rezago de observaciones medidas pero sin determinar. Un registro sin especie es un dato inutilizable: no ingresa a los análisis de distribución de la red.

**Problema analítico.** Determinar si las mediciones morfométricas que las brigadas ya registran de forma rutinaria permiten asignar la especie de forma automática, aprovechando el histórico de registros ya determinados por especialistas.

**Enfoque seleccionado.** Aprendizaje supervisado - clasificación multiclase.

| Elemento | Definición |
|---|---|
| Variable objetivo | `Species` — categórica nominal, 3 clases |
| Variables de entrada | 4 numéricas continuas (medidas de sépalo y pétalo, en cm) |
| Observaciones | 150, con 150 registros no nulos en las 5 columnas |
| Balance de clases | La clase más frecuente registra 50 de 150 observaciones |
| Dataset | Iris (Fisher, 1936), vía `sklearn.datasets.load_iris()` |

---

## 2. Estructura del repositorio

```
MCDI504_GRUPO1/
├── docs/                           # Carpeta para futuros documentos  
├── notebooks/
│   └── F1_Definicion.ipynb         # Notebook Ejecutable
├── figures/                        # Figuras del informe
├── requirements.txt
└── README.md
```

Las figuras 2 a 4 son las salidas gráficas del notebook, exportadas para su inclusión en el informe.
La figura 1 (diagrama KDD) es de elaboración propia.

---

## 3. Reproducir el análisis

```bash
pip install -r requirements.txt
jupyter notebook notebooks/F1_Definicion.ipynb
```

El notebook se ejecuta de principio a fin sin intervención manual y conserva todas sus salidas.
También puede abrirse directamente en Google Colab.
