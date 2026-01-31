# Horas de Estudio - Análisis Predictivo del Rendimiento Académico

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Machine%20Learning-yellow.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)

## Descripción del Proyecto

Este proyecto implementa un **modelo de Machine Learning** para predecir el rendimiento académico de estudiantes basándose en las horas de estudio invertidas. Utiliza técnicas de **regresión lineal simple** y **regresión polinómica** para encontrar el mejor ajuste que explique la relación entre estas dos variables.

El análisis se realiza sobre un **dataset sintético masivo** de entre 75,000 y 100,000 registros, simulando escenarios realistas del impacto del esfuerzo académico en las calificaciones finales.

## Objetivos

1. **Generar un dataset sintético** que simule la relación entre horas de estudio y notas de examen
2. **Modelar la relación** utilizando diferentes enfoques de regresión
3. **Comparar modelos** desde regresión lineal simple hasta polinómicas de grado 6
4. **Identificar el modelo óptimo** que mejor prediga el rendimiento académico
5. **Visualizar resultados** mediante gráficas comparativas

## Estructura del Proyecto

```
Horas-de-estudio/
│
├── Horas_de_estudio_GuzmanWilliam.ipynb   # Notebook principal con todo el análisis
└── README.md                               # Este archivo
```

## Metodología

### 1️⃣ Generación del Dataset

El dataset se construye con dos variables principales:

- **Variable Independiente (X)**: `hores_estudi` - Horas dedicadas al estudio (valores enteros)
- **Variable Dependiente (Y)**: `nota_final` - Calificación del examen (escala 0-10 con 2 decimales)

**Características del dataset:**
- Volumen: 75,000 - 100,000 registros
- Distribución estratificada en 3 grupos de estudio con diferentes rangos de horas
- Notas generadas con distribución normal y desviación estándar controlada

### 2️⃣ Modelos Implementados

#### Regresión Lineal Simple
- Modelo base que identifica tendencia lineal
- Ecuación: `y = mx + b`
- Evaluación mediante coeficiente R²

#### Regresión Polinómica (Grados 2-6)
- Modelos de mayor complejidad para capturar relaciones no lineales
- Evaluación comparativa de R² para cada grado
- Identificación del punto óptimo evitando overfitting

### 3️⃣ Visualización de Datos

El proyecto incluye múltiples visualizaciones:
-  Scatter plots de datos originales
-  Histogramas de distribución de horas y notas
-  Curvas de regresión superpuestas a datos reales
-  Comparativas entre diferentes grados polinómicos

## Tecnologías Utilizadas

| Tecnología | Propósito |
|-----------|-----------|
| **Python 3.x** | Lenguaje de programación principal |
| **Jupyter Notebook** | Entorno de desarrollo interactivo |
| **NumPy** | Operaciones numéricas y generación de datos |
| **Pandas** | Manipulación y análisis de datos |
| **Matplotlib** | Visualización de datos |
| **scikit-learn** | Algoritmos de Machine Learning |

## Cómo Usar Este Proyecto

### Requisitos Previos

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

### Ejecución

1. **Clonar el repositorio:**
```bash
git clone https://github.com/williamG7/Horas-de-estudio.git
cd Horas-de-estudio
```

2. **Abrir el notebook:**
```bash
jupyter notebook Horas_de_estudio_GuzmanWilliam.ipynb
```

3. **Ejecutar las celdas secuencialmente** desde el principio para:
   - Generar el dataset
   - Entrenar los modelos
   - Visualizar resultados
   - Comparar predicciones

> ⚠️ **Nota:** Debido a la generación aleatoria de datos, es posible que necesites re-ejecutar la celda de generación de muestras si los grupos de estudio no cuadran perfectamente.

##  Resultados Esperados

El análisis permite:

✅ Identificar el **modelo con mejor R²** (coeficiente de determinación)  
✅ Visualizar cómo las **regresiones polinómicas capturan mejor** la complejidad de los datos  
✅ Entender el **punto de rendimientos decrecientes** en el estudio  
✅ Predecir notas futuras basadas en horas de estudio planificadas

## Ejemplo de Uso del Modelo

Una vez entrenado el modelo, puedes predecir notas para nuevas horas de estudio:

```python
# Ejemplo conceptual
horas_nuevas = [[5], [10], [15]]
predicciones = modelo_polinomico.predict(horas_nuevas)
print(f"Predicción para 5 horas: {predicciones[0]:.2f}")
```

## Contexto Académico

Este proyecto fue desarrollado originalmente en **Google Colab** como parte de un trabajo académico de análisis de datos y Machine Learning.

## Autor

**William Guzmán**

- GitHub: [@williamG7](https://github.com/williamG7)
- Proyecto: [Horas-de-estudio](https://github.com/williamG7/Horas-de-estudio)

## Licencia

Este proyecto es de código abierto y está disponible para uso educativo y de investigación.

---

⭐ Si te ha resultado útil este proyecto, ¡considera darle una estrella! ⭐
