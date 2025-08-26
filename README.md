# 🕵️‍♂️ Enron Person of Interest Identifier

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python) 
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikit-learn) 
![Status](https://img.shields.io/badge/Status-Completed-brightgreen) 
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Project Introduction
En el año 2000, **Enron** era una de las mayores empresas en Estados Unidos. Para 2002, colapsó en bancarrota debido a un fraude corporativo masivo.  
Como resultado de la investigación federal, salió a la luz un gran volumen de información que normalmente sería confidencial: decenas de miles de correos electrónicos y datos financieros de los principales ejecutivos.

En este proyecto actuamos como **detectives de datos**, construyendo un **identificador de personas de interés (POI)** a partir de los datos financieros y de correos electrónicos publicados tras el escándalo.  
Las POI incluyen individuos que fueron acusados, llegaron a acuerdos legales o declararon a cambio de inmunidad judicial.

---

## 🎯 Objective
El objetivo es desarrollar un modelo de **Machine Learning** capaz de predecir si un individuo es una **Persona de Interés (POI)** basándose en:
- Características financieras 💵  
- Características de correos electrónicos 📧  
- Etiquetas de POI (booleanas) ⚖️  

---

## 💻 Resources Needed
Para trabajar con este proyecto necesitas:
- **Python 3.x**  
- **Scikit-learn**  
- Dataset y código inicial (incluido en el directorio `final_project`)  

Archivos principales:
- `poi_id.py` → código base para construir el identificador POI  
- `final_project_dataset.pkl` → dataset con características financieras, emails y etiquetas  
- `tester.py` → script usado para validar el rendimiento de tu modelo  
- `emails_by_address/` → colección de archivos de texto con correos (útil para ingeniería de nuevas features)  

---

## ⚙️ Features
El dataset contiene tres tipos de características:  

- **Financieras**  
  `['salary', 'deferral_payments', 'total_payments', 'loan_advances', 'bonus', 
  'restricted_stock_deferred', 'deferred_income', 'total_stock_value', 'expenses', 
  'exercised_stock_options', 'other', 'long_term_incentive', 'restricted_stock', 'director_fees']`

- **Correos electrónicos**  
  `['to_messages', 'email_address', 'from_poi_to_this_person', 'from_messages', 
  'from_this_person_to_poi', 'shared_receipt_with_poi']`

- **Etiqueta POI**  
  `['poi']` → valor booleano (1 si es POI, 0 en caso contrario)  

---

## 🚀 Steps to Success
1. **Carga de datos**: usar el código base para leer el dataset.  
2. **Selección e ingeniería de características**:  
   - Crear nuevas variables combinando o transformando las existentes.  
   - Normalizar y escalar las features según corresponda.  
3. **Entrenamiento del modelo**:  
   - Probar distintos algoritmos (Decision Trees, Random Forests, SVM, etc.).  
   - Ajustar hiperparámetros con `GridSearchCV` o `RandomizedSearchCV`.  
4. **Evaluación**:  
   - Usar `tester.py` para validar el rendimiento.  
   - Métricas: precisión, recall, F1-score.  
5. **Entrega final**:  
   - `poi_id.py` con el modelo entrenado.  
   - Dataset modificado (`my_dataset`).  
   - Lista de características utilizadas (`my_feature_list`).  

---

## 🙌 Pep Talk
Este proyecto es más desafiante que los anteriores:  
- El dataset es **real y desordenado**.  
- Los puntos de datos son limitados.  

No te desanimes: trabajar con datos imperfectos es parte del día a día de un **Data Scientist**.  
Piensa estratégicamente, experimenta con nuevas ideas y recuerda: ¡**sí puedes lograrlo**! 💪

---

## 📊 Expected Outcome
Un modelo de Machine Learning que identifique **Personas de Interés en el caso Enron**, con resultados consistentes y justificables en métricas de clasificación.  

---

## 📂 Project Structure
final_project/
│── poi_id.py
│── final_project_dataset.pkl
│── tester.py
│── emails_by_address/
│── README.md ← este archivo
