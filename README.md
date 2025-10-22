# ProyectoConsumodeCafeI-MartinezEstela

# 📊 Análisis de Gastos en Café ☕

Este proyecto analiza los patrones y hábitos de consumo de café en Argentina a partir de un dataset de Kaggle adaptado con datos locales. En los últimos años, el país ha experimentado un crecimiento notable en la cultura cafetera, impulsado por la aparición de cafés de especialidad, la expansión del consumo fuera del hogar y la diversificación de los formatos de preparación.

El objetivo principal del análisis es comprender cómo evolucionan las preferencias de los consumidores argentinos, qué factores influyen en sus decisiones de compra y cómo las nuevas tendencias están moldeando el mercado del café.

---

## 📂 Contenido
- `DATA SET CAFE.csv` → Dataset utilizado para el análisis.
- `analisis_cafe.ipynb` → Notebook con el código del análisis y los gráficos.
- `README.md` → Este archivo de documentación.

---

## 🔍 Análisis realizado
1. **Limpieza de datos**
   - Corrección de nombres de columnas.
   - Imputación de valores faltantes en la variable *Profesion* con la moda.
   - Análisis exploratorio (EDA): estudio de las variables clave (frecuencia, tipo, lugar, horario, profesión, promociones).
   - Se eliminaron duplicados y outliers
     
 2.**Variables Generadas**
   
   -Cantidad: número de unidades vendidas.
   -Ventas: precio * cantidad.
   -Clima: aleatorio entre calor, frío, nublado, lluvia y templado.
   -Ubicación: barrios de la ciudad.
   -Promo: descuentos asociados según medio de pago.
   -Hora y DiaSemana: para análisis temporal.
   -BebidaPremium: variable indicadora para bebidas premium como Latte, Cappuccino y Espresso.
   -Interacciones: Precio_TipoTienda, Promo_Cantidad.

3. **Visualizaciones**
   - 📈 **Evolución temporal del gasto diario** (con línea de media).
   - 📊 **Precio promedio por medio de pago** (con línea de media general).
   - 🥧 **Distribución del gasto por tipo de tienda** (gráfico de torta).
   -     **Heatmaps de correlación entre variables.**
   - 📦 **Gráficos de cajas (boxplots)** para comparar el precio según:
     - Medio de pago
     - Tipo de tienda
     - Momento del día
     - Día de la semana
     - Profesión

4.**Modelos Predictivos**
  -OLS (Regresión Lineal Simple y Múltiple)
  -Variables: Precio, Cantidad, Tipo de Café, Ubicación, DiaSemana, Clima, Promociones.
  -Log-transformación de Ventas para reducir sesgo.
  -Modelos simples explican ~10-13% de la variabilidad.
  -Modelo avanzado con interacciones y variables categóricas codificadas logra R² ~0.94.
  -Variables más influyentes: Precio, Cantidad, Tipo de Tienda, Ubicación y Bebidas Premium.

  **Análisis de Residuos**
  -Residuales centrados en cero, dispersión uniforme.
  -Algunos outliers en ventas extremas.
  -Validación de supuestos de homocedasticidad y normalidad.

 5.**Feature Selection**
 -Selección de variables mediante métodos estadísticos (SelectKBest, f_regression).
 -Importancia de variables evaluada con Random Forest.
 -Proceso de Machine Learning
 -Preparación de datos: limpieza, imputación, codificación, normalización.
  
  **División en Train/Test/Validation.**
  -Entrenamiento de modelos de regresión lineal y Random Forest.
  -Evaluación con métricas: R², RMSE.

  **Visualización de resultados y predicciones.**
  -Métricas del Modelo Final
  -R²: 0.94
  -Predicciones muy cercanas a ventas reales.
  -Gráficos muestran buena alineación entre predicciones y valores observados.

  **Conclusiones**
  -Las ventas están determinadas por Precio, Cantidad, Tipo de Tienda, Ubicación y Promociones.
  -Las bebidas premium y ubicaciones como Belgrano tienen un impacto positivo significativo.
  -Las promociones tienen un efecto menor pero deben aplicarse estratégicamente.
  -El modelo avanzado es útil para planificación estratégica, gestión de inventario y campañas de marketing.

  **Recomendaciones**
  -Optimizar precios según tipo de tienda.
  -Promociones estratégicas según medio de pago.
  -Invertir en ubicaciones de alto rendimiento.
  -Monitorear ventas extremas y actualizar el modelo periódicament

## 🛠️ Tecnologías utilizadas
- Python 3.x  
- Pandas  
- Numpy  
- Matplotlib  
- Seaborn  
- Plotly (para gráficos interactivos)
- statsmodels
- scikit-learn 

---


   
