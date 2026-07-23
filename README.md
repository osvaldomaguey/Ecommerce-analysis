# 📊 Prueba de hipótesis, análisis A/B para tienda de E-commerce

## 🇪🇦 Español

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
Este proyecto sigue un flujo estructurado de análisis dividido en 6 etapas principales:

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

### 🗂 Producto Final
Un reporte inferencial que contiene:

✅ Validación de hipótesis (Test A/B)
  ○ Relación entre gasto promedio y landing page
  ○ Relación entre tasa de conversión y landing page
  ○ Relación
✅ Evidencia visual
✅ Implicaciones de negocio accionables

### 📊 Resultado del Análisis
- El gasto promedio en la página B es mayor al de la A en $3.28 y es estadísticamente significativo (p value = 0.0000)
- La tasa de conversión es mayor en la página B en comparación con la página A en un 0.0338% y es estadísticamente significativa. (p value = 0.0000)
- La tasa de conversión por canal de tráfico es muy similar en cualquiera de los 4 canales, la variación va desde 0.1% a 1.2% y dicha diferencia es estadísticamente significativa (p value = 0.0341)
- No hay evidencia estadística de que el tipo de usuario influya en la conversión (p value = 0.47). La conversion por tipo de usuario fue: para nuevos es 14.35% y para recurrentes es de 14.09%

### **🖋 Conclusiones y recomendaciones**
● Antes de escalar la versión B, proyectar el impacto financiero anual para determinar si la mejora justifica el cambio.
● Diseñar una nueva iteración del experimento con modificaciones más diferenciadas que puedan generar un incremento más relevante en ingresos.
● Priorizar el análisis de rentabilidad por canal de tráfico (costo vs ingreso generado) antes de considerar redistribuciones presupuestales.
● Explorar optimizaciones dentro de cada canal en lugar de modificar la estrategia global de adquisición.
● Calcular CAC y LTV a 30 dias que permita vislumbrar el costo beneficio de cualquier cambio.
● Experimentar segmentar por otras variables del cliente

#### **🚨 Limitaciones del Estudio**

1. Las pruebas identifican diferencias, pero no determinan qué elemento específico generó el cambio en comportamiento.
2. Significancia estadística no implica relevancia económica. Es decir, aunque las diferencias analizadas son estadísticamente significativas, su impacto en ingresos es limitado, lo que reduce su relevancia estratégica.
3. El análisis se enfocó en conversión inmediata y gasto promedio. No se incluyeron métricas como:Retención, recompra, valor de vida del cliente (LTV), y percepción de marca.
4. Variables externas no controladas: Factores como estacionalidad, calidad del tráfico, tipo de productos, barreras de conversión o cambios en el mercado podrían influir en el comportamiento del usuario.

## ▶ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:
[Google Colab](https://colab.research.google.com/drive/11FUTZyapwP7IhT1vJ2ic0Ws2U6vZiCG0?usp=sharing)

## 📘 Cómo reproducir el análisis

1. Abre `notebooks/Version_Student_Proyecto_Landing_Experiment.ipynb`
2. Ejecuta las celdas en orden
3. El notebook carga automáticamente el dataset desde `/data/`

# 📊 Hypothesis Testing & A/B Analysis for E-commerce Store

## 🇬🇧 English

## 🎯 Project Description
A hypothesis testing analysis was conducted for an e-commerce store. They implemented a change to their landing page and wanted to evaluate whether this modification increased their customer conversion rate. The analysis was carried out across 6 stages: Data quality check, comparing average spending per user (A/B pages), comparing conversion rates between web versions, examining the relationship between user type and conversion, generating data visualizations, and communicating insights to stakeholders.

## 🔍 Research Question
Which landing page version is most advantageous for the business? Taking into account conversion rate, average spending, behavior across traffic channels, and user type.

## 📋 Objectives
- Perform thorough data cleaning to ensure data validity for subsequent analyses.
- Determine which page version yields higher user spending and drives more conversions.
- Detect whether a relationship exists between user type and conversion rate.
- Create data visualizations that clearly communicate key findings.
- Translate research findings into actionable business insights for stakeholders.

## 🗂️ Dataset
Source: landing_experiment.csv  
Size: 40,000 customer records

## **Analyzed Variables**

| Variable | Type | Description |
| ---- | ---- | ---- |
| landing | Categorical | Page version shown to the user |
| gasto | Numerical | Amount spent by the user (0 if no conversion occurred) |
| converted | Binary | Indicates whether the user converted |
| traffic_source | Categorical | Acquisition channel through which the user arrived |
| user_type | Categorical | User category based on prior activity history |

## 🛠️ Methodology
Data cleaning.  
Independent samples T-Test with homoscedasticity assumption verified via Levene’s test.  
Z-Test for proportions.  
Chi-Square Test of Independence.  
Tools Used: pandas, scipy.stats, matplotlib, seaborn

## 🔄 Analysis Stages
This project follows a structured analytical workflow divided into 6 main stages:

| Stage | Description | Expected Outcome |
| :--- | :--- | :--- |
| 1. Initial Data Exploration | Load and explore the dataset | Understand data structure, columns, data types, and key metrics |
| 2. Average User Spending | Levene’s test and T-Test | Does the experimental version generate higher user spending? |
| 3. Conversion Rate Across Web Versions | Z-Test for proportions | Does the experimental version achieve a higher conversion rate? |
| 4. User Type vs. Conversion Relationship | Chi-Square test | Which user category proves most profitable for the business? |
| 5. Data Visualization | Create visualizations of results | Clear, illustrative charts depicting analytical findings |
| 6. Delivering Stakeholder Insights | Evidence-based recommendations | Equip stakeholders with actionable information for business decision-making |

### 🎯 Analytical Focus
Nature: Inferential statistical analysis with hypothesis testing to compare landing page versions A and B  
Target Variables: converted (conversion rate) and gasto (revenue)  
Relationship Types Analyzed: Group comparisons, binary variables, and associations between categorical variables

### 🗂 Final Product
An inferential report featuring:
✅ Hypothesis validation (A/B Testing)
  ○ Relationship between average spending and landing page version
  ○ Relationship between conversion rate and landing page version
  ○ Categorical associations
✅ Visual evidence
✅ Actionable business implications

### 📊 Key Findings
- Average spending on Page B is $3.28 higher than on Page A, showing statistical significance (p-value = 0.0000).
- The conversion rate is higher on Page B compared to Page A by 0.0338%, which is statistically significant (p-value = 0.0000).
- Conversion rates across acquisition channels are remarkably similar across all 4 channels, with variations ranging from 0.1% to 1.2%, and this difference is statistically significant (p-value = 0.0341).
- There is no statistical evidence that user type influences conversion (p-value = 0.47). Conversion by user type was 14.35% for new users and 14.09% for returning users.

### **🖋 Conclusions & Recommendations**
● Before scaling Version B, project the annual financial impact to determine if the performance lift justifies implementation costs.
● Design a new experimental iteration with more distinct design modifications capable of driving a more substantial revenue increase.
● Prioritize profitability analysis by acquisition channel (Cost vs. Generated Revenue) prior to reallocating marketing budgets.
● Explore channel-level optimizations rather than altering the global acquisition strategy.
● Calculate CAC (Customer Acquisition Cost) and 30-day LTV (Customer Lifetime Value) to evaluate the true cost-benefit ratio of any future changes.
● Experiment with audience segmentation using additional customer demographic or behavioral variables.

#### **🚨 Study Limitations**
1. While statistical tests identify significant differences, they do not pinpoint which specific design element drove the behavioral change.
2. Statistical significance does not equal economic relevance. That is, although the observed differences are statistically significant, their net impact on revenue is modest, limiting strategic impact.
3. The scope was restricted to immediate conversion and average spending, excluding key metrics such as retention, repeat purchases, long-term Customer Lifetime Value (LTV), and brand perception.
4. Uncontrolled external variables: Factors such as seasonality, traffic quality, product catalog variations, checkout friction, or market shifts could influence user behavior.

## ▶ How to open the notebook in Google Colab
Click on the following button:  
[Google Colab](https://colab.research.google.com/drive/11FUTZyapwP7IhT1vJ2ic0Ws2U6vZiCG0?usp=sharing)

## 📘 How to reproduce the analysis
1. Open `notebooks/Version_Student_Proyecto_Landing_Experiment.ipynb`
2. Execute the cells in sequential order
3. The notebook automatically loads the dataset from `/data/`
