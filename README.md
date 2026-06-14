# DataMind — Analista de Datos IA

DataMind es una aplicación web de una sola página (SPA) que funciona como un **panel de análisis de datos asistido por IA**, totalmente en el navegador. Permite cargar archivos de datos, explorarlos, visualizarlos, consultarlos con SQL, ejecutar código en una consola Python/R simulada y conversar con un asistente que genera estadísticas, consultas y recomendaciones a partir del dataset cargado.

Todo el procesamiento ocurre **del lado del cliente**: no hay backend, base de datos ni servidor. El archivo `index.html` contiene la interfaz, los estilos y toda la lógica de la aplicación.

## ✨ Características principales

- **Dashboard interactivo**: KPIs automáticos (total de filas, columnas, valores nulos, columnas numéricas) y gráficos de distribución, tipos de columna y correlación generados al instante tras cargar un archivo.
- **Tabla de datos**: visualización tabular con búsqueda, ordenamiento por columnas y exportación a CSV.
- **Estadísticas descriptivas**: cálculo de media, mediana, desviación estándar, mínimos, máximos y otros estadísticos para cada variable numérica.
- **Módulo de visualización**: creación de gráficos (barras, líneas, dispersión, pastel, dona, radar, área polar, burbuja) con selección de ejes, agregaciones, paletas de color y exportación a PNG.
- **Editor SQL**: motor de consultas SQL ligero implementado en JavaScript, capaz de interpretar `SELECT`, `WHERE`, `GROUP BY`, `ORDER BY` y `LIMIT` sobre los datos cargados, con vista del esquema y exportación de resultados.
- **Consola Python/R (simulada)**: editor de código con salida simulada para patrones comunes de pandas/estadística (`df.shape`, `df.describe()`, `df.head()`, `df.isnull().sum()`, etc.), útil como espacio de práctica y referencia.
- **Chat con Analista IA**: chatbot basado en reglas que responde preguntas sobre el dataset cargado (resúmenes ejecutivos, detección de valores nulos, detección de anomalías/outliers, recomendaciones de visualización, generación de consultas SQL, código Python para regresión, etc.).
- **Carga de archivos múltiple**: soporte para `.xlsx`, `.xls`, `.csv`, `.json`, `.pdf`, `.docx`, `.doc` y `.txt`, mediante arrastrar y soltar o selección manual.
- **Exportación**: descarga de los datos (o de los resultados de una consulta) en formato CSV.
- **Diseño dark UI** propio, con tipografías personalizadas y un sistema de variables CSS para theming.

## 🛠️ Stack tecnológico

| Capa | Tecnología |
|---|---|
| Estructura / Maquetado | HTML5 |
| Estilos | CSS3 (vanilla, variables CSS personalizadas, layout con Flexbox/Grid) |
| Lógica e interactividad | JavaScript (vanilla, sin frameworks) |
| Gráficos | [Chart.js](https://www.chartjs.org/) |
| Parseo de CSV | [PapaParse](https://www.papaparse.com/) |
| Lectura de Excel | [SheetJS (xlsx)](https://sheetjs.com/) |
| Tipografías | Google Fonts — Syne, Inter, DM Mono |

No requiere `package.json`, gestor de paquetes ni proceso de build: todas las dependencias se cargan vía CDN (cdnjs / Google Fonts).

## 🚀 Cómo usarlo

1. Clona o descarga este repositorio.
2. Abre el archivo `index.html` directamente en tu navegador (no requiere servidor).
3. Carga un archivo de datos (`.xlsx`, `.csv`, `.json`, etc.) desde el panel lateral, arrastrándolo o haciendo clic en la zona de carga.
4. Explora el **Dashboard**, la **Tabla de Datos**, las **Estadísticas** y la **Visualización**.
5. Usa el **Editor SQL** o la **Consola Python/R** para consultas y análisis adicionales.
6. Habla con el **Chat Analista IA** para obtener interpretaciones, sugerencias y código a partir de tu dataset.

## 📁 Estructura del proyecto

```
.
└── index.html   # Aplicación completa (HTML + CSS + JS)
```

## ⚠️ Notas y limitaciones

- El **Editor SQL** es un parser propio con soporte limitado (consultas `SELECT` simples), no un motor SQL completo.
- La **Consola Python/R** simula la salida de patrones de código comunes; no ejecuta código real.
- El **Chat Analista IA** es un sistema basado en reglas/heurísticas sobre el dataset cargado, no realiza llamadas a un modelo de lenguaje externo.
- Al ser una aplicación 100% client-side, los archivos cargados nunca salen del navegador del usuario.

## 📄 Licencia

Añade aquí la licencia que quieras usar para el proyecto (por ejemplo, MIT).
