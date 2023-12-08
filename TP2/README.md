# Estructura del TP2:

- Jupyter notebooks: son 6 en total, van del N1 hasta el N6, los partimos así para segmentar mejor el trabajo. Se deja un detalle abajo de qué contiene cada uno (este mismo también está presente apenas abrir el notebook en la sección "Resumen")
- joblib_serializations.zip: archivo comprimido que contiene las serializaciones de joblib de todos los modelos entrenados en los notebooks, cada uno tiene un submit asociado. Al cargar el joblib de un modelo se puede acceder al modelo mediante el get de "model". No sé incluyó en el repo porque pesa mucho para Github, por lo que se puede descargar mediante [este link a Google Drive](https://drive.google.com/file/d/1tEOJQ_truTyccymD5UQJ9lvRGixuGzWS/view?usp=sharing) (requiere cuenta FIUBA). Hay 18 modelos en total y un índice de las muestras lemmatizadas (explorado en el N4)
- submits.zip: archivo comprimido que contiene todos los submits del modelo al que hace referencia
- datasets (carpeta): contiene los datasets
- imgs (carpeta): contiene imágenes que están en los notebooks de redes neuronales

### 7506R_TP2_GRUPO16_ENTREGA_N1:

En esta notebook se exploran los siguientes modelos:
- Un modelo Naive Bayes default con count vectorizer
- Un modelo Naive Bayes con optimización de hiperparámetros bayesiana del modelo y del vectorizer (count vectorizer + tfidf transformer)
- Un modelo Random Forest con optimización de hiperparámetros bayesiana del modelo y del vectorizer (count vectorizer + tfidf transformer)
- Un modelo XGBoost con optimización de hiperparámetros bayesiana del modelo y del vectorizer (count vectorizer + tfidf transformer)

### 7506R_TP2_GRUPO16_ENTREGA_N2:

En esta notebook se exploran las siguientes variantes de modelos Naive Bayes con optimización de hiperparámetros bayesiana para el modelo y para el vectorizer (count vectorizer y el tfidf):
- Usando unigramas y bigramas
- Usando sólo bigramas
- Usando bigramas y trigramas
- Usando sólo trigramas

### 7506R_TP2_GRUPO16_ENTREGA_N3:

En esta notebook se explora el uso del modelo KNN con el vectorizer (count vectorizer más tfidf transformer)

### 7506R_TP2_GRUPO16_ENTREGA_N4:

En esta notebook exploramos el uso de un modelo Naives Bayes con optimización de hiperparámetros del modelo y el vectorizer (count vectorizer más tfidf transformer). Además, tomamos como un hiperparámetro más de la optimización a la elección entre algunos stemmers y un lemmatizador, probando así la efectividad de los mismos para esta arquitectura.

### 7506R_TP2_GRUPO16_ENTREGA_N5:

En esta notebook se exploran los siguientes modelos:

- Un modelo perceptrón multicapa con input de un vectorizer (count vectorizer + tfidf transformer) de unigramas
- Un modelo perceptrón multicapa con input de un vectorizer (count vectorizer + tfidf transformer) de bigramas
- Un modelo perceptrón multicapa con input de un vectorizer (count vectorizer + tfidf transformer) de unigramas y bigramas
- Un modelo perceptrón multicapa con dropout y regularización L2 con input de un vectorizer (count vectorizer + tfidf transformer) de unigramas y bigramas
- Un modelo red neuronal de deep learning con input de un vectorizer (count vectorizer + tfidf transformer) de unigramas y bigramas

### 7506R_TP2_GRUPO16_ENTREGA_N6:

En esta notebook exploramos el uso de un modelo de ensamble híbrido de tipo stacking, donde los estimadores base pre-entrenados son el mejor Naive Bayes, Perceptrón Multicapa y Random Forest que obtuvimos a lo largo de las notebooks, el metamodelo es una regresión logística.