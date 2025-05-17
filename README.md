# **Data Science Final**

## **Problema a Resolver**
### El objetivo de este proyecto es construir un modelo de **clasificación binaria** que prediga si una persona ha sufrido alguna **enfermedad cardíaca o ataque al corazón**, basándonos en indicadores de salud, estilo de vida y características socioeconómicas.  
Este tipo de predicción puede apoyar programas preventivos de salud pública al identificar a personas en alto riesgo.

## **Dataset**

- **Nombre**: Heart Disease Health Indicators (BRFSS 2015)
- **Fuente**: [CDC - Behavioral Risk Factor Surveillance System (BRFSS)](https://www.cdc.gov/brfss/)
- **Versión procesada (la que se utilizó)**: [Kaggle Dataset - Alex Teboul](https://www.kaggle.com/datasets/alexteboul/heart-disease-health-indicators-dataset)
- **Observaciones**: 253,680 registros
- **Variables**: 22 columnas totales (21 features + 1 target)
- **Target**: HeartDiseaseorAttack
- Clases: 1 = sí ha tenido enfermedad cardíaca o ataque; 0 = no ha tenido enfermedad cardíaca o ataque

## **Modelo Final**

### Target: `HeartDiseaseorAttack`

- `0` → No ha tenido enfermedad cardíaca  
- `1` → Sí ha tenido enfermedad cardíaca (infarto, angina, ataque)

---

### Features utilizadas (21 variables)

- `HighBP` – Alta presión arterial  
- `HighChol` – Colesterol alto  
- `CholCheck` – Chequeo de colesterol reciente  
- `BMI` – Índice de masa corporal  
- `Smoker` – Fuma regularmente  
- `Stroke` – Ha tenido un derrame  
- `Diabetes` – Diagnóstico de diabetes  
- `PhysActivity` – Actividad física en el último mes  
- `Fruits` – Consume frutas regularmente  
- `Veggies` – Consume vegetales regularmente  
- `HvyAlcoholConsump` – Consumo excesivo de alcohol  
- `AnyHealthcare` – Tiene acceso a servicios de salud  
- `NoDocbcCost` – No pudo ver a un doctor por costo  
- `GenHlth` – Salud general autoevaluada  
- `MentHlth` – Días con salud mental deficiente  
- `PhysHlth` – Días con salud física deficiente  
- `DiffWalk` – Dificultad para caminar  
- `Sex` – Sexo (0 = mujer, 1 = hombre)  
- `Age` – Rango de edad  
- `Education` – Nivel educativo  
- `Income` – Nivel de ingresos


  ###  Métricas de Evaluación – Modelo Final 

| Métrica     | Valor       |
|-------------|-------------|
| Accuracy    | 0.7526      |
| Precision   | 0.2471      |
| Recall      | 0.7949      |
| ROC AUC     | 0.8485      |
| KS Score    | 0.5446      |

### Matriz de Confusión

|                        | Predicción No Enfermedad | Predicción Enfermedad |
|------------------------|--------------------------|------------------------|
| **Real No Enfermedad** | 51,577 (TN)              | 17,359 (FP)            |
| **Real Enfermedad**    | 1,470 (FN)               | 5,698 (TP)             |

- **TN (51,577)**: Casos sanos correctamente identificados  
- **FP (17,359)**: Casos sanos etiquetados como enfermos (falsas alarmas)  
- **FN (1,470)**: Pacientes enfermos no detectados (casos perdidos)  
- **TP (5,698)**: Pacientes enfermos correctamente detectados  
