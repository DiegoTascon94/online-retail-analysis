# 🛒 Análisis de Ventas y Segmentación de Clientes: Online Retail

## 🎯 Contexto del Negocio
Una empresa de comercio electrónico busca optimizar su desempeño comercial mediante el entendimiento profundo de su base de clientes. En un entorno transaccional masivo, es vital diferenciar a los clientes de alto valor de aquellos esporádicos para personalizar las estrategias de marketing y evitar la fuga de ingresos.

## 🚀 Objetivo del Proyecto
Analizar datos transaccionales de ventas para identificar tendencias y patrones de comportamiento, aplicando una **segmentación estratégica** que permita generar insights accionables para la optimización del negocio.

## 📊 Alcance del Análisis
* **Limpieza de Datos:** Tratamiento de valores nulos en `CustomerID` y gestión de registros negativos correspondientes a cancelaciones o devoluciones.
* **Granularidad:** Análisis a nivel de factura (`InvoiceNo`) y producto (`StockCode`).
* **Temporalidad:** Evaluación de tendencias históricas para detectar picos de demanda estacional.

## 💡 Principales Insights (EDA)
* **Comportamiento de Compra:** Identificación de los productos con mayor rotación y su impacto en el ticket promedio.
* **Anomalías Transaccionales:** Detección de patrones de devoluciones que afectan la rentabilidad neta por cliente.
* **Concentración de Mercado:** Análisis de ventas por regiones, identificando los mercados con mayor lealtad.

## 🛠️ Enfoque Analítico
* **Análisis Descriptivo:** Para comprender las tendencias generales de venta y volumen.
* **Segmentación RFM (Propuesto):** Evaluación de clientes basada en la Recencia de su última compra, la Frecuencia de sus pedidos y el valor Monetario total aportado.

## 📈 Métricas de Negocio
* **Ingreso Total (Gross Revenue):** Calculado tras la depuración de transacciones fallidas.
* **Volumen de Ventas:** Identificación de los SKUs estrella de la operación.
* **Retención Inicial:** Análisis de la recurrencia de los clientes identificados.

## 🧠 Impacto en Decisiones de Negocio
* **Fidelización:** Priorizar estrategias comerciales en clientes recurrentes identificados como "VIP" o "Campeones".
* **Gestión de Stock:** Priorizar productos con mejor desempeño logístico y comercial.
* **Marketing Dirigido:** Utilizar los patrones identificados para reducir el costo de adquisición de clientes.

## 💻 Tecnologías y Herramientas
* **Lenguaje:** Python
* **Librerías:** Pandas, NumPy, Matplotlib, Seaborn.
* **Entorno:** Jupyter Notebook.

## 📂 Estructura del Repositorio
```text
├── data/
│   └── online_retail.csv       # Dataset (Nota: No incluido por tamaño/privacidad)
├── notebook/
│   └── online_retail.ipynb     # Notebook principal del análisis
├── README.md                   # Documentación del proyecto
├── requirements.txt            # Dependencias necesarias
└── .gitignore                  # Archivos excluidos
```
## 📝 Conclusiones
Este proyecto demuestra que los datos transaccionales crudos pueden transformarse en una hoja de ruta estratégica. Al separar el ruido de las devoluciones y centrarse en el comportamiento real del cliente, el negocio puede actuar de manera proactiva, optimizando tanto el inventario como la relación con el consumidor final.

## 🔮 Próximos Pasos / Mejoras Futuras
* **Market Basket Analysis:** Implementar algoritmos de asociación (como Apriori o FP-Growth) para descubrir qué productos se compran juntos frecuentemente y optimizar el *cross-selling*.
* **Dashboard Interactivo:** Conectar estos hallazgos a una herramienta de BI (Power BI o Tableau) para un monitoreo de KPIs en tiempo real.