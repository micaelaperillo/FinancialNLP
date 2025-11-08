# Sentiment Analysis for the Financial Market

## Descripción del Proyecto

Este proyecto realiza análisis de sentimiento en textos financieros utilizando el **Financial Phrase Bank dataset** de la Universidad de Aalto. El objetivo es clasificar oraciones de noticias financieras en tres categorías de sentimiento: **Positivo**, **Neutral** y **Negativo**, desde la perspectiva de un inversor.

### Dataset

El proyecto utiliza el **Financial Phrase Bank v.1.0**, que contiene aproximadamente 4,840 oraciones anotadas manualmente por 16 expertos con conocimientos en mercados financieros. El dataset ofrece 4 niveles de acuerdo entre anotadores:

- `Sentences_AllAgree.txt`: Oraciones con 100% de acuerdo
- `Sentences_75Agree.txt`: Oraciones con más del 75% de acuerdo
- `Sentences_66Agree.txt`: Oraciones con más del 66% de acuerdo
- `Sentences_50Agree.txt`: Oraciones con más del 50% de acuerdo

**Formato del dataset**: `sentence@sentiment` (separado por "@")

**Referencia**: Malo, P., Sinha, A., Takala, P., Korhonen, P. and Wallenius, J. (2013): "Good debt or bad debt: Detecting semantic orientations in economic texts." Journal of the American Society for Information Science and Technology.

## Contenido del Proyecto

### Análisis Exploratorio de Datos (EDA)

El notebook [exploratory_analysis.ipynb](exploratory_analysis.ipynb) contiene:

- **Preprocesamiento de datos**: Limpieza, normalización de fechas y eliminación de duplicados
- **Análisis temporal**: Evolución de noticias por mes
- **Distribución de sentimientos**: Frecuencia de sentimientos (Negativo, Neutral, Positivo)
- **Niveles de impacto**: Análisis de Low, Medium y High impact
- **Análisis cruzado**: Relación entre sentimiento y nivel de impacto
- **Visualizaciones**: Gráficos de barras y análisis estadísticos

## Requisitos

- Python 3.7+
- Jupyter Notebook o JupyterLab

### Dependencias

Las librerías necesarias están en [requirements.txt](requirements.txt):

```
matplotlib
pandas
seaborn
```

## Instalación y Ejecución

### 1. Clonar el repositorio

```bash
git clone <url-del-repositorio>
cd FinancialNLP
```

### 2. Crear un entorno virtual (recomendado)

```bash
python -m venv venv

# En macOS/Linux:
source venv/bin/activate

# En Windows:
venv\Scripts\activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Ejecutar el análisis exploratorio

```bash
jupyter notebook exploratory_analysis.ipynb
```

O si usas JupyterLab:

```bash
jupyter lab exploratory_analysis.ipynb
```

### 5. Ejecutar el notebook

Una vez abierto el notebook, puedes ejecutar todas las celdas secuencialmente usando:
- **Run All**: Menu → Cell → Run All
- O ejecutar celda por celda con `Shift + Enter`

## Estructura del Proyecto

```
FinancialNLP/
│
├── dataset/                          # Directorio con los datos
│   ├── Sentences_50Agree.txt         # Dataset con 50% acuerdo
│   ├── Sentences_66Agree.txt         # Dataset con 66% acuerdo
│   ├── Sentences_75Agree.txt         # Dataset con 75% acuerdo
│   ├── Sentences_AllAgree.txt        # Dataset con 100% acuerdo
│   ├── README.txt                    # Documentación del dataset
│   └── License.txt                   # Licencia del dataset
│
├── exploratory_analysis.ipynb        # Notebook de análisis exploratorio
├── requirements.txt                  # Dependencias del proyecto
└── README.md                         # Este archivo
```

## Resultados del Análisis

El análisis exploratorio revela:

- **Rango temporal**: Febrero 2025 - Agosto 2025
- **Distribución de sentimientos** (aproximada):
  - Negativo: 32.2%
  - Neutral: 31.4%
  - Positivo: 30.7%
- **Niveles de impacto**:
  - Medium: 34.4%
  - Low: 33.7%
  - High: 31.9%

## Licencia

El dataset Financial Phrase Bank está sujeto a su propia licencia. Para uso académico, citar la publicación original. Para uso comercial, contactar a los autores del dataset.

## Contacto

Para preguntas sobre el dataset original:
- Pekka Malo: pekka.malo@aalto.fi
- Ankur Sinha: ankur.sinha@aalto.fi