### 🗃️ Tipos de Datos en PostgreSQL

<img src="2_Tipos_de_Datos/d_2.jpg" alt="tabla 2" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔢 1. Datos Numéricos

- **Enteros**: Almacenan números enteros sin decimales.  
    - Ejemplos: `SMALLINT`, `INTEGER`, `BIGINT`  
    - **Uso**: Para contar elementos o definir cantidades exactas como `edad`, `cantidad`.

- **Decimales y Flotantes**: Para números con decimales, útil cuando se necesita precisión.  
    - Ejemplos: `REAL`, `DOUBLE PRECISION`, `NUMERIC`  
    - **Uso**: Valores como `precio`, `porcentaje`, `puntuación`.  
    - `NUMERIC` permite definir precisión y escala exacta (ej: `NUMERIC(10,2)`).

---

#### ✍️ 2. Datos de Texto

- **Texto Corto y Variable**: Para almacenar texto de longitud fija o variable.  
    - Ejemplos: `CHAR(n)`, `VARCHAR(n)`  
    - **Uso**: Nombres, apellidos, títulos. `VARCHAR` es más flexible, `CHAR` es útil si siempre se espera una longitud fija.

- **Texto Largo**:  
    - Ejemplo: `TEXT`  
    - **Uso**: Para contenido extenso como descripciones, mensajes o artículos.  
    - No hay límite práctico en la longitud del texto.

---

#### 📅 3. Tipos de Datos de Fecha y Hora

- **Fecha**: Solo la fecha (año, mes, día).  
    - Ejemplo: `DATE`  
    - **Uso**: Fecha de nacimiento, eventos, vencimientos.

- **Hora**: Solo hora (hora, minuto, segundo).  
    - Ejemplo: `TIME`  
    - **Uso**: Horarios, duración de eventos.

- **Fecha y Hora Combinadas**:  
    - Ejemplos: `TIMESTAMP`, `TIMESTAMPTZ` (con zona horaria)  
    - **Uso**: Fechas exactas como `fecha_creación`, `última_actualización`.

---

#### 🧩 4. Tipos de Datos Especiales

- **Enumeraciones (Enum)**: Conjunto predefinido de valores.  
    - Se definen con `CREATE TYPE estado AS ENUM ('activo', 'inactivo');`  
    - **Uso**: Estados, roles, categorías.

- **Datos JSON**: Para almacenar objetos JSON.  
    - Ejemplos: `JSON`, `JSONB`  
    - **Uso**: Estructuras flexibles como preferencias de usuario, configuración dinámica.  
    - `JSONB` permite búsquedas y consultas más eficientes.

- **Datos Binarios**:  
    - Ejemplo: `BYTEA`  
    - **Uso**: Almacenar imágenes, archivos, documentos binarios.

---

### Dato vacío, con valor y nulo (NULL)

<img src="3_SQL_Consultas/dato_null_1.png" alt="motores" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">