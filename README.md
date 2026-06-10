# 📊 Prueba de hipótesis, análisis A/B para tienda de E-commerce

## 🎯 Descripción del Proyecto

Se realizó un análisis de prueba de hipótesis para una tienda de e-comerce. Llevaron acabo un cambio en su landing page y querian saber si dicho cambio aumentaba la tasa de conversión de sus clientes. El analisis realizado se llevo a cabo en 6 etapas: Calidad de datos, comparar gasto promedio por usuario (página A/B), comparar la tasa de conversión entre las versiones web, revisar la relación entre el tipo de usuario y la conversión, elaborar visualizaciones, y comunicar los insights del análisis a stakeholders.

## 🔍 Pregunta de Investigación
¿Cuál versión de la landing page es más conveniente para el negocio? Considerando la tasa de conversión, el gasto promedio, el comportamiento por canal de tráfico y tipo de usuario.

## 📋 Objetivos
Realizar una limpieza adecuada de los datos para garantizar la validez de los mismos en los análisis posteriores.
Descubrir en que versión de la página los usuarios gastan más, así como cual genera más conversiones.
Detectar si existe alguna relación entre tipo de usuario y la conversión.
Elaborar visualizaciones que comuniquen de forma clara los hallazgos.
Transformar los resultados encontrados en insights accionables para los stakeholders.

## 🗂️ Dataset
Fuente: landing_experiment.csv
Tamaño: 40,000 registros de clientes

## **Variables Analizadas**
| Variable | Tipo | Descripción |
|---------|-------------|-------------------|
| landing	| Categórica | Versión de la página mostrada al usuario |
| gasto | Numérica |	Monto gastado por el usuario (0 si no convirtió) |
| converted | Binaria	| Indica si el usuario realizó una conversión |
| traffic_source	| Categórica	| Canal por el que llegó el usuario |
| user_type | Categórica | Tipo de usuario según historial previo |

## 🛠️ Metodología
Limpieza de datos.
Prueba T de muestras independientes con verificación del supuesto de homocedasticidad mediante la prueba de Levene.
Prueba Z para proporciones.
Prueba Chi-cuadrada
Herramientas Utilizadas: pandas, scipy.stats, matplotlib, seaborn

## 🔄 Etapas del Análisis
Este proyecto sigue un flujo estructurado de análisis dividido en 5 etapas principales:

| Etapa	 | Descripción | Resultado Esperado |
|---------|-------------|-------------------|
| 1. Exploración Inicial | Cargar y explorar el dataset | Entender estructura, columnas, tipos y métricas clave? |
| 2. Gasto promedio por usuario	| Prueba de levene y Prueba T |	¿La versión experimental genera mayor gasto por parte de los usuarios? |
| 3. Tasa de conversión entre las versiones web | Prueba Z para proporciones | ¿La versión experimental tiene mayor tada de conversión? | 
| 4. Relación entre el tipo de usuario y la conversión | Prueba Chi-cuadrada| ¿Qué tipo de usuario es mas redituable para el negocio? |
| 5. Visualización | Crear visualizaciones de los resultados |	Gráficos ilustrativos sobre los hallazgos |
| 6. Transmitir insights a Stakeholders | Recomendaciones basadas en evidencia | Que los stakeholders tengan la información suficiente para tomar decisiones de negocio |
 
### 🎯 Enfoque del Análisis
Naturaleza: Análisis inferencial con pruebas de hipótesis para comparar versiones A y B de landing page
Variable objetivo: converted (tasa de conversión) y gasto (revenue)
Tipo de relaciones analizadas: Comparación entre grupos, variables binarias y asociación entre variables categóricas

### 📊 Resultado Final
Un reporte de rentabilidad y retención que combina:

✅ Evidencia visual (Dashboard interactivo en PowerBI)
✅ Evidencia numérica (KPIs de performance)
✅ Análisis de funnel de conversión
✅ Retención por cohortes
✅ Validación de hipótesis (Test A/B)
✅ Implicaciones de negocio accionables

## ▶ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:
[Google Colab](https://colab.research.google.com/drive/1d5hEBvqIXTaKGqIwQrEE1zKKEPFnitgY?usp=sharing)

## 📘 Cómo reproducir el análisis

1. Abre `notebooks/Estudiante_Proyecto_Final.ipynb`
2. Ejecuta las celdas en orden
3. El notebook carga automáticamente el dataset desde `/data/`
