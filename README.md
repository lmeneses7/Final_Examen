## Supuestos del PCA y su verificación

### 1. Linealidad

PCA asume que las variables tienen *relaciones lineales entre sí*. Esto significa que las combinaciones lineales de las variables originales pueden explicar la varianza en los datos.

En este caso:

- Las variables seleccionadas (estatura, peso, educacion, edad, etc.) son numéricas y tienen relaciones lineales entre sí.
- La *matriz de correlación* generada previamente muestra coeficientes de correlación positivos y negativos, lo cual confirma que existen relaciones lineales.

---

### 2. Datos numéricos

PCA solo trabaja con *datos numéricos*. Las variables categóricas deben transformarse antes de aplicar PCA.

En este caso:

- La columna genero fue transformada a valores binarios:
   - Masculino = 1, Femenino = 0.
- La columna etnia fue codificada numéricamente:
   - Blanco = 1, Other = 0, Afroamericano = 3, Latino = 4.

Por lo tanto, todas las columnas utilizadas en el análisis PCA son numéricas.

---

### 3. Varianza máxima

PCA busca capturar la *máxima varianza* en los datos, por lo que es importante que las variables sean *escaladas* a la misma escala.

En este caso:

- Se utilizó StandardScaler para escalar las variables antes de aplicar PCA.
- El escalamiento asegura que todas las variables tengan *media 0* y *desviación estándar 1*, eliminando la influencia de las unidades o magnitudes originales.

El escalamiento previo garantiza que la varianza capturada por PCA no se vea afectada por las diferencias en la escala de las variables.

---

### 4. Independencia de componentes

PCA genera *componentes principales ortogonales, es decir, linealmente **independientes* entre sí. Cada componente captura información única de los datos.

En este caso:

- Los componentes principales PC1 y PC2 tienen varianzas explicadas *separadas*:
   - PC1 explica el *25.63%* de la varianza total.
   - PC2 explica el *18.60%* de la varianza total.
- La independencia entre componentes está garantizada por la naturaleza misma del algoritmo PCA.

---

### 5. Escalamiento

El *escalamiento* de las variables es un requisito fundamental para PCA, ya que permite que todas las variables tengan la *misma importancia* en el análisis.

En este caso:

- Se aplicó StandardScaler para realizar el escalamiento previo a PCA.
- El resultado muestra que los datos están *centrados en 0* y tienen una *desviación estándar de 1*, cumpliendo con el requisito de escalamiento.

---
