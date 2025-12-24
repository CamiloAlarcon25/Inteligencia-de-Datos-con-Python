# Inteligencia de Datos con Python: Limpieza, Análisis y Reportabilidad Automatizada
## 1. Contexto y Objetivos
En entornos empresariales, los datos suelen venir con errores de digitación, nombres duplicados o formatos inconsistentes. El objetivo de este proyecto fue crear un script robusto en Python capaz de procesar archivos de ventas, corregir inconsistencias mediante algoritmos de similitud de texto, realizar análisis estadísticos y generar un reporte ejecutivo en PDF de forma 100% automática.
## 2. Tecnologías y Librerías
•	Python (Core): Lenguaje principal para la lógica del negocio.

•	Pandas: Para la manipulación de estructuras de datos (DataFrames).

•	TheFuzz (FuzzyWuzzy): Para la aplicación de algoritmos de Lógica Difusa (Levenshtein Distance).

•	Matplotlib: Para la generación de visualizaciones estadísticas.

•	FPDF: Para la creación y maquetación del informe final en formato PDF.
## 3. Desafíos Técnicos y Soluciones
### A. Limpieza con Lógica Difusa (El mayor valor agregado)
El script enfrenta el problema de nombres de empresas escritos de distintas formas (ej: "Apple Inc" vs "Apple").

•	Solución: Implementé una función que utiliza fuzz.token_sort_ratio para comparar cadenas de texto. El sistema identifica automáticamente la coincidencia más cercana en una lista maestra de vendedores y estandariza el nombre si la similitud supera el 80%, asegurando que los datos financieros sean exactos.
### B. Procesamiento de Datos (Data Wrangling)

•	Se realizó una limpieza profunda: conversión a minúsculas, eliminación de espacios en blanco y unión de tablas (Merge) para consolidar la información de ventas con la de los vendedores.

•	Se realizaron agrupaciones (groupby) para calcular métricas críticas: ventas totales por empresa y rendimiento por vendedor.
### C. Visualización y Automatización de Salida

•	Gráficos Dinámicos: El script genera automáticamente gráficos de barras que comparan el desempeño de las ventas, guardándolos como archivos .png para su posterior uso.

•	Generador de PDF: En lugar de crear un informe manual, el script utiliza la librería FPDF para construir un documento PDF que incluye:

o	Títulos y encabezados.

o	Tablas de datos procesados.

o	Inserción de los gráficos generados previamente.
## 4. Impacto del Proyecto
Este proyecto demuestra la capacidad de sustituir horas de trabajo manual en Excel por un script de pocos segundos que garantiza:

1.	Integridad Total: No hay errores humanos en la corrección de nombres.

2.	Repetibilidad: El script puede procesar nuevos datos cada mes con un solo clic.

3.	Profesionalismo: Entrega un producto final (PDF) listo para ser enviado a gerencia.

