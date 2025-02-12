### 🐹 Consultas SQL Básica

<img src="3_SQL_Consultas/s_1.png" alt="consulta basica 1" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🐹 Consultas SQL Básica 2

<img src="3_SQL_Consultas/s_2.png" alt="consulta basica 2" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🏷️ Consultas SQL Intermedia

<img src="3_SQL_Consultas/s_3.png" alt="consulta intermedia" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🎁 Consultas SQL Avanzada

<img src="3_SQL_Consultas/s_4.png" alt="consulta avanzada" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

### SELECT 📚

- **Título:** Navegando por tus Datos con `SELECT`
- **Subtítulo:** La clave para recuperar información en MySQL 🗝️

---

### * / COLUMNAS 📜

- Todas las columnas `SELECT *`
- Seleccionando las columnas `SELECT col1, col2, col3`

---

### Alias en las Columnas 🐔

- Seleccionando las columnas `SELECT col1 as id, col2 as nombre, col3 as edad`

===

### FROM 📍

- Seleccionando las tablas con `FROM tabla1`
- Se pueden seleccionar varias tablas `FROM tabla1, tabla2`

---

### Alias en las Tablas 📚

- Usando el alias `FROM tabla1 as t1, tabla2 as t2`

===

### LIMIT 👋

- **`LIMIT`**: Restringe el número de filas que se devuelven en el conjunto de resultados.
- **Propósito**: Controlar la cantidad de datos retornados, optimizando el rendimiento y la legibilidad.

---

### Limit normal y con offset 📈

- Limit normal `SELECT * FROM tabla1 LIMIT 2`
- Limit con offset `SELECT * FROM tabla2 LIMIT 3,2`

===

### ORDER BY 📝

- **`ORDER BY`**: Ordena el conjunto de resultados según una o más columnas especificadas.
- **Propósito**: Presentar los datos de manera lógica y fácil de analizar.

---

### ORDER BY ASCENDENTE Y DESCENDENTE ⚠️

- Ascendente `SELECT * FROM tabla1 ORDER BY col1 ASC`
- Descendente `SELECT * FROM tabla1 ORDER BY col1 DESC`

---

### ORDER BY MULTICOLUMNAS 🗃️

- Se puede aplicar a varias columnas 
- Ejemplo `SELECT * FROM tabla1 ORDER BY col1 ASC, col2 DESC`

===

### CONSULTA INTERMEDIA - WHERE 👀

- **`SELECT * FROM TABLA WHERE ID>10 ORDER BY ID ASC LIMIT 5`**: Filtrar y Ordenar Datos.
- **Propósito**: Obtener solo los datos que cumplan con condiciones especificas.

---

### FILTROS EN MYSQL - WHERE + = 🐬

- Igualdad `=`
- Filtra registros donde una columna tiene un valor específico.

```sql
-- Seleccionar productos con un precio igual a 100
SELECT * FROM productos WHERE precio = 100;
```

---

### FILTROS EN MYSQL - WHERE + != ✅

- Diferente `<>`, `!=`
- Filtra registros donde una columna tiene un valor distinto.

```sql
-- Seleccionar productos que no pertenezcan a la categoría 'Electrónica'.
SELECT * FROM productos WHERE categoria <> 'Electrónica';
```

---

### FILTROS EN MYSQL - WHERE + >,< 🐶

- Mayor o menor que `>`, `<`, `<=`, `>=`
- Filtra registros donde una columna tiene un valor mayor o menor que.

```sql
SELECT * FROM productos WHERE costo >= 15;
```

---

### FILTROS EN MYSQL - WHERE + BETWEEN 🧲

- Rango de valores
- Filtra registros dentro de un rango definido

```sql
-- Seleccionar productos con precio entre 50 y 100.
SELECT * FROM productos WHERE precio BETWEEN 50 AND 100;
```

---

### FILTROS EN MYSQL - WHERE + IN 🚀

- Lista de valores
- Filtra registros dentro de un rango definido

```sql
-- Filtrar productos que pertenezcan a 'Electrónica', 'Ropa' o 'Juguetes'.
SELECT * FROM productos WHERE categoria IN ('Electrónica', 'Ropa', 'Juguetes');
```

---

### FILTROS EN MYSQL - WHERE + LIKE 🔑

- Coincidencia de patrones
- Filtra registros basándose en patrones.
- %: Coincide con cualquier cantidad de caracteres.
- _: Coincide con un solo carácter.

```sql
-- Seleccionar productos cuyo nombre comience con 'Cam'.
SELECT * FROM productos WHERE nombre LIKE 'Cam%';
```

---

### FILTROS EN POSTGRESQL - WHERE + ILIKE 🔑

- Coincidencia de patrones sin distinción entre mayúsculas y minúsculas.
- Filtra registros basándose en patrones.
- `%`: Coincide con cualquier cantidad de caracteres.
- `_`: Coincide con un solo carácter.

```sql
-- Seleccionar productos cuyo nombre comience con 'Cam' (sin distinguir mayúsculas).
SELECT * FROM productos WHERE nombre ILIKE 'Cam%';
```

---

### FILTROS EN MYSQL - WHERE + IS NULL / IS NOT NULL 🤘

- Valores nulos
- `IS NULL`: Filtra registros con valores nulos.
- `IS NOT NULL`: Filtra registros con valores no nulos.

```sql
-- Seleccionar productos sin descripción
SELECT * FROM productos WHERE descripcion IS NULL;
```

---

### LOGICAS BINARIAS - WHERE + AND / OR  🐶

- **`AND`**: Es verdadero solo si todas las condiciones son verdadero
- **`OR`**: Es verdadero si alguna de las condiciones es verdadero

```sql
-- Seleccionar productos con precio mayor a 50 y categoría 'Electrónica'
SELECT * FROM productos WHERE precio > 50 AND categoria = 'Electrónica';
```

---

### LOGICAS BINARIAS - WHERE + NOT ⚠️

- Negación
- Invierte el resultado de una condición

```sql
-- Seleccionar productos que no pertenezcan a la categoría 'Electrónica'.
SELECT * FROM productos WHERE NOT categoria = 'Electrónica';

--Seleccionar productos cuyo nombre no comience con 'Cam'.
SELECT * FROM productos WHERE NOT nombre LIKE 'Cam%';

-- Seleccionar productos cuyo precio no esté entre 50 y 100.
SELECT * FROM productos WHERE NOT precio BETWEEN 50 AND 100;
```

---

### FILTROS EN POSTGRESQL - WHERE + REGEXP 🦊

- Filtra registros basados en patrones más complejos.
- `~` → Coincide con una expresión regular (sensible a mayúsculas).
- `~*` → Coincide con una expresión regular (insensible a mayúsculas).

```sql
-- Seleccionar productos cuyo nombre empiece con 'Cam' o 'Zap'
SELECT * FROM productos WHERE nombre ~ '^(Cam|Zap)';
```

===

### USO DE FUNCIONES 🧑‍🎄

<img src="3_SQL_Consultas/fun_2.jpg" alt="funciones" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### USO DE FUNCIONES 2 🧑‍🎄

<img src="3_SQL_Consultas/fun_1.png" alt="funciones2" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### TIPOS DE FUNCIONES 📊 🧠  

- **Numéricas**: `ABS()`, `CEIL()`, `FLOOR()`, `ROUND()` 🧮  
- **Manipulación** de cadenas: `CONCAT()`, `LOWER()`, `UPPER()`, `STRING_AGG()` 📝  
- **Fechas** y Horas: `NOW()`, `CURRENT_DATE`, `TO_CHAR()`, `AGE()` 🕰️  
- **Lógicas** y Condicionales: `CASE WHEN`, `COALESCE()`, `NULLIF()` 🤔  

> 📌 **Nota:** PostgreSQL no tiene `CONCAT_WS()`, pero `STRING_AGG()` puede usarse en agregaciones. Tampoco tiene `IF()`, por lo que se usa `CASE WHEN`. `CURDATE()` se reemplaza por `CURRENT_DATE`.

---

### Funciones Numéricas 🧙‍♂️

Las funciones numéricas en PostgreSQL nos permiten realizar operaciones matemáticas básicas y avanzadas. Algunas de las más comunes son:

- `ABS(x)`: Devuelve el valor absoluto de un número.
- `CEIL(x)`: Devuelve el siguiente entero más grande que el número dado.
- `FLOOR(x)`: Devuelve el entero más grande que es menor o igual que el número dado.
- `ROUND(x, d)`: Redondea un número al número de decimales especificado. Si no se especifica `d`, se redondea al entero más cercano.

Ejemplo:

```sql
SELECT 
    ABS(-10.5) AS valor_absoluto,
    CEIL(3.14) AS techo,
    FLOOR(3.14) AS piso,
    ROUND(3.14159, 2) AS redondeado;
```

---

### Funciones de Manipulación de Cadenas 📝

Las funciones de manipulación de cadenas en PostgreSQL nos permiten trabajar con texto. Algunas de las más útiles son:

- `CONCAT(str1, str2, ...)`: Concatena dos o más cadenas de texto.
- `LOWER(str)`: Convierte una cadena de texto a minúsculas.
- `UPPER(str)`: Convierte una cadena de texto a mayúsculas.
- `STRING_AGG(expression, delimiter)`: Concatena valores agrupados con un delimitador.

Ejemplo:

```sql
SELECT
    CONCAT('Hola', ', ', 'mundo') AS concatenado,
    STRING_AGG('Curso' || ' de ' || 'SQL', ' - ') AS concatenado_con_separador,
    LOWER('SQL es GENIAL') AS texto_a_minusculas;
```

---

### Funciones de Fecha y Hora 🕰️

Las funciones de fecha y hora en PostgreSQL nos permiten trabajar con información temporal. Algunas de las más comunes son:

- `NOW()`: Devuelve la fecha y hora actual.
- `CURRENT_DATE`: Devuelve la fecha actual.
- `TO_CHAR(date, format)`: Formatea una fecha según un patrón especificado.

Ejemplo:

```sql
SELECT
    NOW() AS fecha_y_hora_actual,
    CURRENT_DATE AS fecha_actual,
    TO_CHAR(NOW(), 'DD/MM/YYYY') AS formato_personalizado;
```

---

### Funciones Lógicas y Condicionales 🤔 1/2

Las funciones lógicas y condicionales en SQL nos permiten realizar operaciones basadas en condiciones. Algunas de las más útiles en PostgreSQL son:

- `CASE WHEN condition THEN value ELSE other_value END`: Evalúa una serie de condiciones y devuelve un valor correspondiente.
- `COALESCE(value1, value2, ...)`: Devuelve el primer valor no nulo de la lista.
- `NULLIF(value1, value2)`: Devuelve `NULL` si ambos valores son iguales; de lo contrario, devuelve `value1`.

---

### Funciones Lógicas y Condicionales 🤔 2/2

Ejemplo:

```sql
SELECT
    CASE 
        WHEN 10 > 5 THEN 'Verdadero'
        ELSE 'Falso'
    END AS resultado_case,
    CASE 
        WHEN 3 > 1 THEN 'Mayor'
        WHEN 3 < 1 THEN 'Menor'
        ELSE 'Igual'
    END AS resultado_case_multiple,
    COALESCE(NULL, 'Valor por defecto', 'Otro valor') AS resultado_coalesce,
    NULLIF(5, 5) AS resultado_nullif;
```
> No existe el IF en las columnas

===

### Uso de Variables

<img src="3_SQL_Consultas/var_1.png" alt="variables" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Creando Variables con `WITH` en PostgreSQL 🤔

- Las variables se pueden declarar temporalmente utilizando una **CTE (Common Table Expression)** con la cláusula `WITH`.
- Se pueden definir múltiples "variables" a la vez dentro de la misma cláusula `WITH`.

Ejemplo:

```sql
WITH 
    var1 AS (SELECT 1),
    var2 AS (SELECT 'LUIS'),
    var3 AS (SELECT TRUE),
    var4 AS (SELECT '2024-05-12'::DATE)
SELECT * FROM var1, var2, var3, var4;
```

---

### Utilidad de las variables en PostgreSQL 🤔 1/2 

- 🚀 **Mejora el rendimiento de las consultas**: Almacena resultados intermedios en variables para evitar cálculos repetidos.
- 🧩 **Facilita operaciones complejas**: Permite almacenar y manipular datos durante la ejecución de funciones o procedimientos almacenados.
- 🔄 **Reutilización de valores**: Reduce la necesidad de repetir expresiones complejas en una consulta.
- 🔧 **Control de flujo en funciones y procedimientos**: Usar variables dentro de bloques `PL/pgSQL` para estructurar el flujo de operaciones.

---

### Utilidad de las variables en PostgreSQL 🤔 2/2

- 📚 **Mayor legibilidad y mantenimiento**: Hace el código más limpio y fácil de seguir.
- ⚠️ **Evita errores de repetición**: Previene errores de lógica relacionados con la repetición de cálculos.
- ⚡ **Optimización de subconsultas**: Almacena resultados intermedios en variables para optimizar consultas con subconsultas o cálculos complejos.

---

### Dato vacío, con valor y nulo (NULL)

<img src="3_SQL_Consultas/dato_null_1.png" alt="motores" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

### Tipos de almacenamiento en PostgreSQL

- 🛠️ **PostgreSQL con MVCC**: Manejo avanzado de transacciones, alto rendimiento y concurrencia.
- 📦 **TOAST**: Almacenamiento eficiente para grandes objetos, como texto y datos binarios.
- 💾 **HASH**: Índice optimizado para búsquedas rápidas de igualdad.
- 📄 **JSONB**: Almacenamiento eficiente y consultas de datos JSON con soporte completo de índices.
- 🗄️ **BRIN**: Índices para datos con alta correlación, optimizando el espacio y el rendimiento en grandes conjuntos de datos.  

---

### 🚀 Características clave de PostgreSQL 🐘  

PostgreSQL es un sistema de gestión de bases de datos relacional avanzado, diseñado para ofrecer alto rendimiento, escalabilidad y cumplimiento con ACID. No utiliza motores de almacenamiento separados como MySQL, sino que incorpora todas sus funcionalidades de manera nativa.  

Algunas de sus características clave incluyen:  

- **MVCC (Multi-Version Concurrency Control)**: Manejo eficiente de transacciones sin bloqueos.  
- **JSONB y XML**: Soporte para almacenamiento y consulta de datos semiestructurados.  
- **Índices avanzados**: B-Tree, GIN, BRIN y Hash para optimización de consultas.  

---

### ⚙️ Características principales en PostgreSQL  

| Característica               | 🐘 **PostgreSQL**               |
|------------------------------|--------------------------------|
| **Soporte para transacciones** | ✅ Sí (ACID-compliant, MVCC)  |
| **Bloqueo de registros**       | ✅ Nivel de fila (MVCC)      |
| **Velocidad de lectura**       | 🚀 Alta con índices avanzados (B-Tree, GIN, BRIN) |
| **Integridad referencial**     | ✅ Soporte completo con claves foráneas |
| **Consumo de memoria**         | 🧠 Optimizado con TOAST y compresión |
| **Recuperación tras fallos**   | ✅ WAL (Write-Ahead Logging) para recuperación confiable |

---

### 📊 Comparación en profundidad  

#### 🌟 **Ventajas de PostgreSQL en transacciones**  
1. 🔒 **Integridad de datos**: Soporte completo para **claves foráneas**, reglas de **cascada** y **constraints avanzadas**.  
2. 📈 **Alto rendimiento en transacciones**: Implementación de **MVCC** (Multi-Version Concurrency Control) para transacciones concurrentes sin bloqueos.  
3. 🛡️ **Recuperación confiable**: Sistema de **WAL (Write-Ahead Logging)** para recuperación ante fallos y consistencia de datos.  

---

#### ⚡ **Ventajas de PostgreSQL para lectura intensiva**  
1. 🚀 **Consultas optimizadas**: Uso de **índices avanzados** (B-Tree, GIN, BRIN) para acelerar lecturas.  
2. 📁 **Almacenamiento eficiente**: Soporte para **TOAST** y **JSONB**, reduciendo el consumo de espacio.  
3. 🛠️ **Ideal para analítica y reporting**: Soporte para **Materialized Views** y **paralelización de consultas**.  

---

### 📂 Casos de uso en PostgreSQL

| Proyecto                               | Recomendación               |
|---------------------------------------|----------------------------|
| 🛒 **Sistema de e-commerce**           | **PostgreSQL con MVCC**: Soporte transaccional y concurrencia eficiente. |
| 📚 **Sistema de biblioteca**           | **PostgreSQL con FK y índices**: Integridad referencial y optimización de consultas. |
| 📊 **Generación de reportes simples**  | **Materialized Views o JSONB**: Almacenamiento eficiente y consultas rápidas. |
| 📄 **Blogs o sitios web estáticos**    | **PostgreSQL con JSONB**: Manejo flexible de contenido y almacenamiento eficiente. |