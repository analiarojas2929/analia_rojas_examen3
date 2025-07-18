# 🩺 Análisis Predictivo del Dataset de Diabetes
## Proyecto de Machine Learning Avanzado

**Autor:** Analia Rojas  
**Fecha:** Julio 2025  
**Curso:** Machine Learning Avanzado  

---

## 📋 Descripción del Proyecto

Este proyecto implementa un análisis exhaustivo y modelado predictivo del **Pima Indians Diabetes Dataset** utilizando técnicas avanzadas de machine learning. El objetivo es predecir la presencia de diabetes en pacientes basándose en indicadores médicos, aplicando metodologías profesionales de ciencia de datos.

## 🎯 Objetivos

- **Objetivo Principal:** Desarrollar modelos predictivos robustos para detectar diabetes
- **Objetivos Técnicos:**
  - Implementar pipelines de preprocessing modernos
  - Aplicar técnicas avanzadas de manejo de outliers
  - Optimizar hiperparámetros con validación cruzada
  - Comparar modelos de ensemble (Random Forest vs XGBoost)
  - Asegurar reproducibilidad y calidad del código

## 📊 Dataset

**Fuente:** Pima Indians Diabetes Database (Kaggle)  
**Tamaño:** 768 observaciones, 9 variables  
**Tipo:** Clasificación binaria (0: No diabetes, 1: Diabetes)

### Variables del Dataset:
- `Pregnancies`: Número de embarazos
- `Glucose`: Concentración de glucosa en plasma
- `BloodPressure`: Presión arterial diastólica (mm Hg)
- `SkinThickness`: Grosor del pliegue cutáneo del tríceps (mm)
- `Insulin`: Insulina sérica de 2 horas (mu U/ml)
- `BMI`: Índice de masa corporal (peso en kg/(altura en m)²)
- `DiabetesPedigreeFunction`: Función de pedigrí de diabetes
- `Age`: Edad (años)
- `Outcome`: Variable objetivo (0 o 1)

## 🛠️ Tecnologías y Librerías

### Librerías Core
- **pandas** - Manipulación de datos
- **numpy** - Computación numérica
- **scikit-learn** - Machine learning

### Preprocesamiento Avanzado
- **ColumnTransformer** - Transformaciones diferenciadas por columnas
- **Pipeline** - Flujos de trabajo reproducibles
- **StandardScaler** - Normalización estándar
- **RobustScaler** - Escalamiento robusto para outliers

### Modelos de Machine Learning
- **RandomForestClassifier** - Modelo de ensemble basado en árboles
- **XGBClassifier** - Gradient boosting extremo

### Optimización y Evaluación
- **RandomizedSearchCV** - Búsqueda aleatoria de hiperparámetros
- **StratifiedKFold** - Validación cruzada estratificada
- **classification_report** - Métricas comprehensivas

### Visualización
- **matplotlib** - Gráficos base
- **seaborn** - Visualizaciones estadísticas avanzadas

## 🔧 Metodología Implementada

### 1. **Análisis Exploratorio de Datos (EDA)**
- Estadísticas descriptivas detalladas
- Análisis de distribuciones y asimetría
- Detección de valores faltantes y duplicados
- Matriz de correlaciones
- Visualizaciones profesionales

### 2. **Ingeniería de Características Avanzada**
- **Detección de Outliers:**
  - Método IQR (Rango Intercuartílico)
  - Método Z-score (puntuaciones estándar)
  - Análisis visual con boxplots
- **Tratamiento de Outliers:**
  - Clipping conservador (percentiles 5-95)
  - Preservación de información médica relevante

### 3. **Preprocessing Moderno**
- **ColumnTransformer** para tratamiento diferenciado:
  - Variables normales: StandardScaler
  - Variables con outliers: RobustScaler + OutlierClipper
- **Pipelines completos** para reproducibilidad
- Separación estratificada train/test (80/20)

### 4. **Modelado y Optimización**
- **Random Forest:**
  - Optimización de n_estimators, max_depth, min_samples_split
  - Validación cruzada estratificada 5-fold
- **XGBoost:**
  - Optimización de learning_rate, max_depth, n_estimators
  - Regularización L1/L2 (reg_alpha, reg_lambda)

### 5. **Evaluación Comprehensiva**
- **Métricas Múltiples:** Accuracy, Precision, Recall, F1-Score, ROC-AUC
- **Matrices de Confusión** detalladas
- **Curvas ROC** comparativas
- **Análisis de Importancia** de características

## 📈 Resultados Principales

### Rendimiento de Modelos Optimizados

| Modelo | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|----------|-----------|--------|----------|---------|
| Random Forest | 82.47% | 78.18% | 72.34% | 75.14% | 0.8854 |
| XGBoost | 83.77% | 80.85% | 74.47% | 77.53% | 0.8932 |

### Características Más Importantes
1. **Glucose** - Concentración de glucosa (factor principal)
2. **BMI** - Índice de masa corporal
3. **Age** - Edad del paciente
4. **DiabetesPedigreeFunction** - Factor hereditario
5. **Pregnancies** - Historial reproductivo

## 🏆 Técnicas Avanzadas Implementadas

### ✅ **Manejo Profesional de Outliers**
- Detección con múltiples métodos (IQR + Z-score)
- Clipping conservador para preservar información médica
- Transformadores personalizados reutilizables

### ✅ **Pipelines Modernos**
- ColumnTransformer para preprocessing diferenciado
- Flujos completos desde datos crudos hasta predicciones
- Reproducibilidad garantizada

### ✅ **Optimización Inteligente**
- RandomizedSearchCV para eficiencia computacional
- Validación cruzada estratificada
- Búsqueda en espacios de hiperparámetros amplios

### ✅ **Evaluación Robusta**
- Múltiples métricas para análisis completo
- Validación cruzada para estimaciones confiables
- Análisis de interpretabilidad del modelo

## 📁 Estructura del Proyecto

```
analia_rojas_examen3/
├── README.md                                           # Este archivo
├── diabetes.csv                                        # Dataset original
├── analia_rojas_examen3_diabetes_analysis.ipynb       # Notebook principal
└── outputs/                                           # (Generado automáticamente)
    ├── visualizations/                                # Gráficos generados
    └── models/                                        # Modelos entrenados
```

## 🚀 Instrucciones de Uso

### Requisitos Previos
```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
```

### Ejecución
1. **Clonar/Descargar** el proyecto
2. **Abrir** `analia_rojas_examen3_diabetes_analysis.ipynb` en Jupyter/VS Code
3. **Ejecutar todas las celdas** secuencialmente
4. **Revisar** resultados y visualizaciones generadas

### Reproducibilidad
- Todas las semillas aleatorias están fijadas (`random_state=42`)
- El notebook se ejecuta de inicio a fin sin errores
- Los resultados son determinísticos y reproducibles

## 🎓 Consideraciones Éticas y Médicas

### **Responsabilidad Médica**
- Este modelo es para fines **educativos y de investigación**
- **NO debe usarse** para diagnósticos médicos reales
- Las decisiones médicas requieren evaluación profesional

### **Sesgos y Limitaciones**
- Dataset específico de mujeres Pima Indians
- Posibles sesgos demográficos y genéticos
- Necesidad de validación en poblaciones diversas

### **Privacidad y Seguridad**
- Datos anonimizados y de dominio público
- Cumplimiento con estándares de privacidad médica
- Uso responsable de información de salud

## 📊 Innovaciones Técnicas

### **OutlierClipper Personalizado**
Transformador custom que implementa clipping conservador basado en percentiles, preservando información médica relevante mientras mitiga el impacto de valores extremos.

### **Estrategia de Preprocessing Diferenciado**
Uso de ColumnTransformer para aplicar diferentes estrategias de escalamiento según las características de distribución de cada variable.

### **Optimización Eficiente**
RandomizedSearchCV con 100 iteraciones y validación cruzada estratificada para encontrar configuraciones óptimas en tiempo razonable.

## 🔮 Trabajo Futuro

### **Mejoras Técnicas**
- Implementar ensemble stacking
- Explorar redes neuronales (MLPClassifier)
- Aplicar técnicas de selección de características avanzadas

### **Validación Clínica**
- Validación en datasets adicionales
- Análisis de fairness entre grupos demográficos
- Estudio de calibración de probabilidades

### **Despliegue**
- API REST para predicciones
- Interfaz web interactiva
- Pipeline de MLOps para reentrenamiento

## 📞 Contacto

**Analia Rojas**  
Estudiante de Machine Learning Avanzado  
Proyecto Académico - Julio 2025

---

## 📄 Licencia

Este proyecto es de uso académico y educativo. Los datos utilizados son de dominio público (Kaggle).

---

## 🙏 Agradecimientos

- **UCI Machine Learning Repository** por el dataset
- **Kaggle Community** por la distribución de datos
- **Scikit-learn Team** por las herramientas de ML
- **XGBoost Developers** por el algoritmo de gradient boosting

---

*"La ciencia de datos aplicada a la salud tiene el potencial de salvar vidas, pero debe practicarse con responsabilidad y rigor científico."*
