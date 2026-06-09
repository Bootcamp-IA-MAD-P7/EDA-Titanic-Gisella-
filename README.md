📘 README — Análisis Exploratorio de Datos (EDA) del Titanic
   Objetivo del Proyecto
El objetivo de este análisis es identificar qué factores influyeron en la supervivencia de los pasajeros del Titanic. Se estudian variables como sexo, edad, clase social, tamaño de familia y precio del ticket, para responder preguntas como:

¿Las mujeres tuvieron mayor probabilidad de sobrevivir?
¿Los niños fueron priorizados?
¿La clase social influyó en la supervivencia?
¿Viajar solo o en familia afectó las probabilidades?

🧠 Parte 1: Investigación Teórica
1. ¿Qué es el EDA y cuál es su propósito?
El EDA (Exploratory Data Analysis) es el proceso de explorar, limpiar y comprender un conjunto de datos antes de aplicar modelos. Sirve para detectar patrones, identificar errores o valores faltantes, entender relaciones entre variables y formular hipótesis.

2. Tipos de datos en un EDA
Numéricos: continuos (edad), discretos (número de hijos)
Categóricos: nominales (sexo), ordinales (clase social)
Fechas / tiempo
Booleanos (0/1)
3. Diferencia entre análisis univariado, bivariado y multivariado
Univariado: analiza una sola variable
Bivariado: analiza dos variables
Multivariado: analiza varias variables a la vez
4. ¿Qué es la estadística descriptiva?
Es un conjunto de medidas que resumen los datos:

Media, mediana, moda
Rango, varianza, desviación estándar
Percentiles
Tablas y gráficos
5. ¿Qué es la limpieza de datos?
Incluye:

Manejo de valores nulos
Eliminación de duplicados
Detección y tratamiento de outliers
Corrección de tipos de datos
Normalización o estandarización
6. Papel de pandas, matplotlib y seaborn
pandas: manipulación y limpieza de datos
matplotlib: gráficos base
seaborn: gráficos estadísticos más avanzados y estéticos
7. ¿Qué es una matriz de correlación?
Es una tabla que muestra la relación entre variables numéricas.
Valores cercanos a:

1: correlación positiva fuerte
-1: correlación negativa fuerte
0: sin relación
8. ¿Qué son los outliers y cómo se detectan?
Son valores extremos que se alejan del resto.
Métodos:

Boxplot
IQR (Q1 − 1.5·IQR, Q3 + 1.5·IQR)
Z-score
9. ¿Qué es hypothesis testing?
Es un método estadístico para evaluar hipótesis mediante un p-valor.
Sirve para:

Comparar grupos
Ver si una diferencia es significativa
Apoyar conclusiones del EDA
🧪 Parte 2: Resumen del EDA Práctico (Titanic)
1. Carga y exploración inicial
Se cargó el dataset desde Kaggle usando kagglehub.
Se revisaron:
primeras filas (head)
dimensiones (shape)
tipos de datos (info)
columnas disponibles
2. Estadística descriptiva
Se analizaron variables numéricas (describe).
Se revisaron variables categóricas (describe(include='object')).
Se detectaron valores extremos en la variable Fare.
3. Limpieza de datos
Se eliminaron columnas irrelevantes: PassengerId, Name, Ticket, Cabin.

Se imputó:

Age con la mediana
Embarked con la moda
Se eliminaron filas con valores faltantes restantes.

Se renombraron columnas para mayor claridad.

4. Análisis univariado
Distribución de supervivencia (Survived)

Distribución por sexo (Sex)

Histograma de edades (Age)

Boxplot de tarifas (Fare)

5. Análisis bivariado
Sexo vs supervivencia: las mujeres sobrevivieron más.
Clase vs supervivencia: primera clase tuvo mayor supervivencia.
Edad vs supervivencia: los niños tuvieron ventaja.
Fare vs supervivencia: tarifas más altas se relacionan con mayor supervivencia.
6. Análisis multivariado
Se generó una matriz de correlación para identificar relaciones entre variables numéricas.
Se creó un heatmap para visualizar las correlaciones de forma más clara.
Se utilizó un pairplot para observar patrones entre múltiples variables simultáneamente.
7. Feature Engineering
Se crearon nuevas variables para enriquecer el análisis:

Family_Size: tamaño de la familia (Siblings_Spouses + Parents_Children + 1)
Is_Alone: indica si el pasajero viajaba solo (1) o acompañado (0)
Age_Group: clasificación de edades en grupos (Child, Teenager, Young Adult, Adult, Senior)
Estas nuevas variables permitieron identificar patrones adicionales relacionados con la supervivencia.

8. Conclusiones principales
Las mujeres tuvieron mayor probabilidad de sobrevivir.
Los pasajeros de primera clase sobrevivieron más.
Los niños tuvieron ventaja frente a los adultos.
Viajar solo redujo la supervivencia.
El precio del ticket se relaciona con la supervivencia: tarifas más altas → mayor probabilidad de sobrevivir.
📁 Archivos entregados
README.md (este documento)
EDA_Titanic.ipynb (Google Colab con todo el análisis)
🎉 Proyecto completado
Este proyecto presenta un análisis exploratorio de datos (EDA) del Titanic utilizando Python, Google Colab y visualizaciones estadísticas. El objetivo fue comprender qué factores influyeron en la supervivencia de los pasajeros y desarrollar habilidades fundamentales de análisis de datos.
