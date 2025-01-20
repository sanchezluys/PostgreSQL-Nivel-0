### 🗃️ Tipos de Datos en MySQL

<img src="2_Tipos_de_Datos/d_2.jpg" alt="tabla 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔢 1. Datos Numéricos

- **Enteros**: Almacenan números enteros sin decimales. 
    - Ejemplos: `INT`, `SMALLINT`, `BIGINT`
    - **Uso**: Ideal para contar elementos o definir cantidades exactas, como `edad` o `cantidad`.

- **Decimales y Flotantes**: Almacenan números con decimales, útiles para valores que requieren precisión.
    - Ejemplos: `FLOAT`, `DOUBLE`, `DECIMAL`
    - **Uso**: Para valores con decimales, como `precio` o `puntuación`.

---

#### ✍️ 2. Datos de Texto

- **Cadenas de Texto Corto**: Para almacenar texto breve.
    - Ejemplos: `CHAR`, `VARCHAR`
    - **Uso**: Nombres, apellidos, títulos. `VARCHAR` permite longitud variable y es más flexible que `CHAR`.

- **Cadenas de Texto Largo**: Para almacenar texto extenso, como descripciones o comentarios.
    - Ejemplos: `TEXT`, `MEDIUMTEXT`, `LONGTEXT`
    - **Uso**: Para contenido largo como descripciones de productos, mensajes o artículos.

---

#### 📅 3. Tipos de Datos de Fecha y Hora

- **Fecha**: Almacena solo la fecha (año, mes, día).
    - Ejemplo: `DATE`
    - **Uso**: Fechas de nacimiento, fechas de eventos.

- **Hora**: Almacena solo la hora (horas, minutos, segundos).
    - Ejemplo: `TIME`
    - **Uso**: Horarios específicos, como la hora de apertura o cierre.

- **Fecha y Hora Combinadas**: Almacena fecha y hora juntas.
    - Ejemplos: `DATETIME`, `TIMESTAMP`
      - **Uso**: Para eventos en tiempo específico, como `fecha_creación` o `fecha_modificación`.

---

#### 🧩 4. Tipos de Datos Especiales

- **Enumeraciones**: Valores predefinidos de selección única o múltiple.
    - Ejemplos: `ENUM`, `SET`
    - **Uso**: Estados (`activo`, `inactivo`), etiquetas múltiples (`promoción`, `exclusivo`).

- **Datos JSON**: Almacena estructuras complejas de datos en formato JSON.
    - Ejemplo: `JSON`
    - **Uso**: Ideal para almacenar datos flexibles y anidados, como configuraciones o preferencias del usuario.

- **Datos Binarios**: Almacena datos en formato binario.
    - Ejemplos: `BLOB`, `BINARY`
    - **Uso**: Imágenes, archivos, y otros datos multimedia.

