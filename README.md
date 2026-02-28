# 🛒 Análisis de Ventas y Segmentación de Clientes — Online Retail I (UCI)

## 🎯 Contexto del Negocio
Una empresa de comercio electrónico del Reino Unido especializada en productos de regalo busca optimizar su desempeño comercial mediante el entendimiento profundo de su base de clientes. En un entorno transaccional masivo, es vital diferenciar a los clientes de alto valor de aquellos esporádicos para personalizar las estrategias de marketing y evitar la fuga de ingresos.

## 🚀 Objetivo del Proyecto
Analizar más de 500,000 transacciones reales para identificar tendencias de ventas, patrones de comportamiento de compra y concentración de revenue, aplicando segmentación RFM para generar insights accionables orientados a retención, reactivación y optimización comercial.

## 📊 Alcance del Análisis
- **Datos:** 541,909 registros transaccionales reales (dic 2010 — dic 2011)
- **Limpieza:** Tratamiento de 135,080 nulos en `CustomerID`, eliminación de duplicados, separación de cancelaciones y filtrado de valores no plausibles en `Quantity` y `UnitPrice`
- **Granularidad:** Análisis a nivel de factura (`InvoiceNo`) y producto (`StockCode`)
- **Temporalidad:** Evaluación de tendencias históricas mensuales para detectar estacionalidad

## 💡 Principales Insights
- **Concentración de revenue:** El 26% de los clientes (1,129 de 4,338) genera el 80% del revenue total — validación del Principio de Pareto sobre la base de clientes
- **Estacionalidad marcada:** Noviembre y octubre concentran los picos más altos de revenue (£1.5M y £1.15M respectivamente), asociados a temporada alta de regalos
- **Dependencia geográfica:** United Kingdom concentra la mayoría del revenue (£9M), con Netherlands, EIRE y Germany como mercados internacionales líderes
- **Productos estrella:** Los productos de mayor revenue no coinciden con los de mayor volumen — DOTCOM POSTAGE lidera en ingresos mientras PAPER CRAFT, LITTLE BIRDIE lidera en unidades vendidas

## 🛠️ Enfoque Analítico
- **Preprocesamiento:** Separación de datasets por propósito (negocio, clientes, productos), tratamiento diferenciado de nulos y cancelaciones
- **Análisis Descriptivo:** Tendencias generales de venta, volumen y revenue mensual
- **Análisis 80/20:** Concentración de revenue por cliente y por producto
- **Segmentación RFM:** Segmentación ejecutada sobre clientes identificados evaluando Recency, Frequency y Monetary con scoring por cuantiles

## 📈 Métricas de Negocio
- **Revenue Total:** £10,642,110 GBP sobre ventas válidas
- **Transacciones únicas:** 19,960 facturas
- **Clientes identificados:** 4,338 clientes únicos
- **Average Order Value (AOV):** £533 GBP
- **Average Revenue per Customer:** £2,453 GBP
- **Tasa de cancelación:** 1.72% del total de registros

## 🧠 Impacto en Decisiones de Negocio
- **Retención:** El segmento de alto valor (26% de clientes) concentra el 80% del revenue — una caída en este grupo tiene impacto directo y significativo en los ingresos totales
- **Gestión de Stock:** Estacionalidad identificada permite anticipar demanda de Q4 desde agosto, evitando quiebres de stock en temporada alta
- **Marketing Dirigido:** Segmentación RFM permite diferenciar estrategias por segmento — retención para clientes de alto valor, reactivación para clientes en riesgo y conversión para clientes potenciales

## 💻 Tecnologías y Herramientas
- **Lenguaje:** Python
- **Librerías:** Pandas, NumPy, Matplotlib, Seaborn
- **Entorno:** Jupyter Notebook

## 📂 Estructura del Repositorio
```
├── data/
│   └── online_retail.csv          # Dataset (no incluido por tamaño)
├── notebook/
│   └── online_retail.ipynb        # Notebook principal del análisis
├── README.md                      # Documentación del proyecto
├── requirements.txt               # Dependencias necesarias
└── .gitignore                     # Archivos excluidos
```

## ▶️ Cómo Ejecutar el Proyecto
1. Clonar el repositorio: `git clone https://github.com/DiegoTascon94/online-retail-analysis.git`
2. Descargar el dataset desde [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail) y colocarlo en `/data`
3. Instalar dependencias: `pip install -r requirements.txt`
4. Abrir el análisis: navegar a `/notebook` y ejecutar `online_retail.ipynb`

## 📝 Conclusiones
Este proyecto demuestra que los datos transaccionales crudos pueden transformarse en una hoja de ruta estratégica. La combinación de limpieza rigurosa, análisis exploratorio y segmentación RFM permite identificar con precisión los segmentos críticos del negocio — desde los clientes de alto valor que sostienen el revenue hasta los patrones estacionales que definen la planificación comercial.

## 🔮 Próximos Pasos / Mejoras Futuras
- **Market Basket Analysis:** Implementar algoritmos de asociación (Apriori o FP-Growth) para descubrir productos que se compran juntos y optimizar el cross-selling
- **Modelo predictivo de churn:** Clasificar clientes en riesgo antes de que migren a segmento perdido, basándose en su perfil RFM
- **Expansión del análisis:** Replicar metodología sobre el dataset Online Retail II (2009-2011) con stack completo Python + SQL Server + Power BI
