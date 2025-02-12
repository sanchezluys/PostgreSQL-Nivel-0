### Group By en PostgreSQL

<img src="6_group_by/group_by.png" alt="todos los joins" style="height: 800px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Group By en PostgreSQL

- Sirve para agrupar datos que se repiten
- Se usa en conjunto con funciones de agregación (Count(), Sum(), Avg()..)

---

### ¿Cuándo Usarlo?

Cuando quieras agrupar datos similares y obtener resultados agregados por grupo, por ejemplo:

- Sumar ventas por mes.
- Contar empleados por departamento.
- Buscar la menor edad separados por sexo de un listado de clientes.

---

### Código Ejemplo

```sql
SELECT          columna1, 
                columna2, 
                FUNCION_AGREGADA(columna3)
FROM            tabla
GROUP BY        columna1, columna2;

-- ***************
-- Algunas Funciones de agregación
-- 1. Count()   -> cuenta registros
-- 2. Sum()     -> suma y acumula
-- 3. Avg()     -> busca el promedio
-- 4. Min()     -> busca el mínimo valor
-- 5. Max()     -> busca el máximo valor
```

---

### Funciones de Agregación en PostgreSQL 1/3

- **COUNT()** 📊: Cuenta el número de filas o valores no nulos.
- **SUM()** ➕: Suma los valores de una columna numérica.
- **AVG()** 🔢: Calcula el promedio de una columna numérica.
- **MIN()** 🔽: Encuentra el valor mínimo en una columna.
- **MAX()** 🔼: Encuentra el valor máximo en una columna.
- **STRING_AGG()** 📝: Concatena los valores de una columna de tipo texto en un solo string.

---

### Funciones de Agregación en PostgreSQL 2/3

- **ARRAY_AGG()** 🧳: Devuelve una matriz de todos los valores de una columna.
- **BOOL_AND()** ✅: Devuelve verdadero si todas las expresiones de tipo booleano son verdaderas.
- **BOOL_OR()** 🔘: Devuelve verdadero si alguna expresión de tipo booleano es verdadera.
- **VAR_POP()** 📉: Calcula la varianza de una población.
- **VAR_SAMP()** 📉🔬: Calcula la varianza de una muestra.
- **STDDEV_POP()** 📐: Calcula la desviación estándar de una población.

---

### Funciones de Agregación en PostgreSQL 3/3

- **STDDEV_SAMP()** 📏: Calcula la desviación estándar de una muestra.
- **REGR_SLOPE()** ↗️: Calcula la pendiente de la recta de regresión.
- **REGR_INTERCEPT()** ➖: Calcula la intersección de la recta de regresión.
- **REGR_R2()** 🔄: Calcula el coeficiente de determinación (R^2) de la regresión.
- **REGR_AVGX()** 🔀: Calcula el promedio de X en una regresión.
- **REGR_AVGY()** 🔀: Calcula el promedio de Y en una regresión.