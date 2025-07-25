## 📃 Primer Pilar La Tabla

<img src="1_La_Tabla/tabla_1.webp" alt="tabla"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

### 📘 La tabla - Datos

<img src="1_La_Tabla/t_1.gif" alt="tabla 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🎛️ La tabla - PgAdmin

<img src="1_La_Tabla/t_2.png" alt="tabla 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 👽 Encabezado de la tabla

<img src="1_La_Tabla/t_3.png" alt="tabla 3"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🔩 Columnas

<img src="1_La_Tabla/t_4.png" alt="tabla 4"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 📝 Nombre de la columna

<p class="fragment" data-fragment-index="1" style="text-align: left;">
1. <strong>📝 Usar snake_case</strong>: Escribe todos los nombres en minúsculas usando guiones bajos para separar palabras. Por ejemplo:
- fecha_nacimiento (✅ correcto)
- fechaNacimiento (❌ incorrecto)
- FECHA_NACIMIENTO (❌ incorrecto)
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🎯 Ser descriptivo y conciso</strong>: Usa nombres que indiquen claramente el propósito de la columna:
  - correo_electronico (✅ correcto)
  - mail (❌ incorrecto)
  - email_usuario_sistema (❌ demasiado largo)
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>📋 Seguir patrones establecidos</strong>: Mantén consistencia en los prefijos y sufijos:
  - id_usuario (✅ para claves primarias)
  - categoria_id (✅ para claves foráneas)
  - es_activo (✅ para booleanos)
  - fecha_creacion (✅ para timestamps)
</p>

---

### 🔢 Tipos de Datos 1/2

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🔢 Datos Numéricos</strong>:
  - INTEGER: números enteros (id, cantidad, edad).
  - NUMERIC(10,2): valores monetarios o con precisión exacta (precio, salario).
  - SMALLINT: números enteros pequeños (edades).
  - REAL: números decimales sin precisión exacta.
  - BIGINT: números enteros grandes (transacciones, conteos masivos).
</p>
<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>📝 Datos de Texto</strong>:
  - VARCHAR(50): Textos cortos con longitud variable (nombre, email).
  - CHAR(10): Textos longitud fija (código_postal).
  - TEXT: Textos largos o ilimitados (descripción, contenido).
  - ENUM: Valores predefinidos (estado, tipo) mediante dominios o tipos personalizados en PostgreSQL.
</p>

---

### 🔢 Tipos de Datos 2/2

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>📅 Datos de Fecha/Hora</strong>:
  - DATE: fecha (fecha_nacimiento).
  - TIME: hora (hora_entrada).
  - TIMESTAMP: Fecha y hora sin zona horaria (fecha_creacion).
  - TIMESTAMPTZ: Fecha y hora con zona horaria (ultima_actualizacion).
</p>
<p class="fragment" data-fragment-index="4" style="text-align: left;">
  4. <strong>🎯 Datos Especiales</strong>:
  - BYTEA: Datos binarios (imagen, archivo).
  - JSON/JSONB: Datos formato JSON, JSONB optimizado para consultas (configuración).
  - GEOGRAPHY/GEOMETRY: Datos geoespaciales mediante extensiones como PostGIS (ubicación).
  - UUID: Identificadores únicos universales (token).
  - ARRAY: Datos en formato de lista o conjunto (etiquetas, preferencias).
</p>

---

### 🔑 PK - Llave Primaria 1/2

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🔑 Estructura Básica de PK</strong>:
  - Nombre: id o id_[tabla].
  - Tipo: INTEGER o BIGINT.
  - Propiedades: NOT NULL + GENERATED ALWAYS AS IDENTITY.
  - Ejemplo: 
    <code>
    id SERIAL PRIMARY KEY
    </code>
    O bien, usando la opción recomendada:
    <code>
    id INTEGER GENERATED ALWAYS AS IDENTITY PRIMARY KEY
    id INTEGER GENERATED ALWAYS AS IDENTITY (START WITH 100 INCREMENT BY 10 MINVALUE 100 MAXVALUE 1000 CACHE 5)
    </code>
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>📋 Tipos Comunes de PK</strong>:
  - Numérica autoincremental: id INTEGER GENERATED BY DEFAULT AS IDENTITY (más común).
  - UUID: id UUID DEFAULT gen_random_uuid().
  - Compuesta: (codigo_pais, dni).
  - Natural: numero_documento VARCHAR(20) (evitar si no es necesario).
</p>

---

### 🔑 PK - Llave Primaria 2/2

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Siempre usar NOT NULL en las columnas de la llave primaria.
  - Preferir GENERATED AS IDENTITY en lugar de SERIAL (más moderno y estandarizado).
  - Evitar PKs compuestas si es posible (dificultan índices y consultas).
  - PostgreSQL automáticamente indexa las PKs.
  - Evaluar el crecimiento de los datos para seleccionar el tipo de columna adecuado (por ejemplo, usar BIGINT si se esperan grandes volúmenes de datos).
</p>

---

### ❗ NN - No Nulo 1/2

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>❗ Cuándo usar NOT NULL</strong>:
  - Campos obligatorios: como nombre o email, que siempre deben tener un valor.
  - Llaves primarias: como id, que requieren ser únicas y no nulas.
  - Campos de fechas importantes: como fecha_creacion, necesarios para el seguimiento.
  - Campos de estado: como estado_pedido, que determinan el flujo de datos.
  - Cantidades y precios: como precio_total, fundamentales en cálculos.
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>⚠️ Cuándo permitir NULL</strong>:
  - Campos opcionales: como segundo_nombre, que no todos los registros llenan.
  - Fechas futuras: como fecha_cancelacion, que depende de eventos posteriores.
  - Campos que pueden no aplicar: como fecha_baja, para empleados activos.
  - Datos complementarios: como observaciones, útiles pero no esenciales.
  - Referencias opcionales: como supervisor_id, cuando no todos tienen un supervisor.
</p>

---

### ❗ NN - No Nulo 2/2

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>💡 Mejores Prácticas</strong>:
  - Usar valores por defecto: para evitar nulos innecesarios, por ejemplo:
    <code>
    estado_pedido VARCHAR(20) NOT NULL DEFAULT 'pendiente'
    </code>
  - Documentar por qué se permite NULL: para mantener claridad en el diseño.
  - Considerar el impacto en consultas: usar IS NULL o IS NOT NULL puede ser costoso en ciertas circunstancias.
  - Evitar NULL en campos de cálculos: manejar valores predeterminados para evitar resultados inesperados.
  - Preferir NOT NULL para mejor rendimiento: facilita índices y optimiza consultas.
</p>

---

### 🎯 UQ - Valor Único 1/2

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar UNIQUE</strong>:
  - Correo electrónico: (email) para garantizar que cada usuario tenga un email único.
  - Número de documento: (dni, rut) para identificar personas de manera única.
  - Nombre de usuario: (username) en sistemas de autenticación.
  - Códigos de producto: (sku, codigo_barras) para evitar duplicados en inventarios.
  - Número de serie: (serial_number) en equipos o productos manufacturados.
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Tipos de UNIQUE</strong>:
  - Simple (una columna):
    <code>
    email VARCHAR(100) UNIQUE
    </code>
  - Compuesto (múltiples columnas):
    <code>
    UNIQUE (codigo_pais, numero_documento)
    </code>
    Esto se define a nivel de tabla:
    <code>
    CREATE TABLE usuarios (
        id SERIAL PRIMARY KEY,
        codigo_pais VARCHAR(5),
        numero_documento VARCHAR(20),
        UNIQUE (codigo_pais, numero_documento)
    );
    </code>
</p>

---

### 🎯 UQ - Valor Único 2/2

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Combinar con NOT NULL si el campo es obligatorio para evitar valores nulos únicos.
  - Considerar índices automáticamente creados por las restricciones UNIQUE.
  - Validar mayúsculas/minúsculas si aplica, usando operadores como `LOWER()` en las consultas:
   <code>
    email VARCHAR(100) UNIQUE,
    CHECK (email = LOWER(email))
    </code>
  - Evaluar necesidad real de unicidad para evitar restricciones innecesarias que puedan afectar el rendimiento.
</p>

---

### ⚡ UN - Sin signo (UNSIGNED) 1/2

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo simular UNSIGNED</strong>:
  - Valores que nunca serán negativos: cantidades, edades, identificadores.
  - Columnas que necesitan maximizar el rango positivo: como IDs de usuarios o contadores.
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Cómo manejar enteros positivos en PostgreSQL</strong>:
  - Enteros con restricciones CHECK:
    <code>
    edad SMALLINT CHECK (edad >= 0)
    </code>
  - IDs o claves foráneas:
    <code>
    usuario_id BIGINT CHECK (usuario_id >= 0)
    </code>
  - PostgreSQL no soporta directamente `UNSIGNED`, pero se puede limitar el rango de valores a través de una combinación de tipo de datos y restricciones.
</p>

---

### ⚡ UN - Sin signo (UNSIGNED) 2/2

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Usar restricciones CHECK para asegurar valores no negativos:
    <code>
    cantidad INTEGER CHECK (cantidad >= 0)
    </code>
  - Seleccionar tipos de datos adecuados según el rango esperado:
    - `SMALLINT`: -32,768 a 32,767.
    - `INTEGER`: -2,147,483,648 a 2,147,483,647.
    - `BIGINT`: -9,223,372,036,854,775,808 a 9,223,372,036,854,775,807.
  - Documentar las restricciones para evitar confusiones con usuarios o aplicaciones que esperan soporte nativo para `UNSIGNED`.
  - Evaluar si realmente necesitas maximizar el rango positivo y considerar el uso de `BIGINT` en lugar de `UNSIGNED` para grandes volúmenes de datos.
</p>

---

### 📞 AI - Auto incremental 1/2

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar AUTO_INCREMENT</strong>:
  - Identificadores únicos de registros: como IDs para usuarios, pedidos o productos.
  - Claves primarias que deben incrementarse automáticamente para cada nuevo registro.
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Cómo manejar AUTO_INCREMENT en PostgreSQL</strong>:
  - Usar el tipo de datos `SERIAL` para enteros autoincrementales:
    <code>
    id SERIAL PRIMARY KEY
    </code>
  - Para rangos mayores, usar `BIGSERIAL`:
    <code>
    id BIGSERIAL PRIMARY KEY
    </code>
  - Crear una secuencia manualmente si necesitas más control:
    <code>
    CREATE SEQUENCE id_sequence START WITH 1 INCREMENT BY 1;
    CREATE TABLE ejemplo (
        id INT DEFAULT nextval('id_sequence'),
        nombre TEXT
    );
    </code>
  - Configurar el valor inicial y el incremento de una secuencia:
    <code>
    ALTER SEQUENCE id_sequence RESTART WITH 100;
    </code>
</p>

---

### 📞 AI - Auto incremental 2/2

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Usar `SERIAL` o `BIGSERIAL` para la mayoría de los casos: simplifica la definición de columnas autoincrementales.
  - Definir la columna como clave primaria:
    <code>
    id SERIAL PRIMARY KEY
    </code>
  - Evitar el uso de autoincrementales para datos que necesitan personalización manual.
  - Gestionar las secuencias explícitamente si necesitas control avanzado, como reiniciar o modificar el valor inicial.
  - Considerar el uso de UUID si requieres identificadores únicos globales en lugar de valores numéricos secuenciales:
    <code>
    id UUID DEFAULT gen_random_uuid() PRIMARY KEY
    </code>
</p>

---

### 🏷️ G - Columna Generada 1/2

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar COLUMNAS GENERADAS</strong>:
  - Campos derivados de otros valores en la misma fila, como:
    - Edad calculada a partir de la fecha de nacimiento.
    - Totales con impuestos basados en precios.
  - Cálculos frecuentes o concatenaciones que no deberían almacenarse manualmente.
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Cómo manejar COLUMNAS GENERADAS en PostgreSQL</strong>:
  - Columna generada almacenada (STORED): su valor se calcula y almacena físicamente en la tabla.
    <code>
    CREATE TABLE productos (
        id SERIAL PRIMARY KEY,
        precio DECIMAL(10, 2) NOT NULL,
        total_con_impuesto DECIMAL(10, 2) GENERATED ALWAYS AS (precio * 1.19) STORED
    );
    </code>
  - Ejemplo con concatenación:
    <code>
    CREATE TABLE personas (
        id SERIAL PRIMARY KEY,
        nombre VARCHAR(50),
        apellido VARCHAR(50),
        nombre_completo VARCHAR(100) GENERATED ALWAYS AS (nombre || ' ' || apellido) STORED
    );
    </code>
</p>

---

### 🏷️ G - Columna Generada 2/2

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Usar columnas generadas almacenadas (`STORED`) para datos que se calculan con frecuencia y necesitan ser consultados rápidamente.
  - Validar las dependencias: las columnas de origen deben existir y tener el tipo de datos adecuado.
  - Evitar redundancia en datos almacenados si el cálculo es simple y puede realizarse dinámicamente en consultas.
  - No usar columnas generadas para cálculos que cambian frecuentemente, ya que requieren recalculación cada vez que se actualizan las columnas base.
  - Optimizar el rendimiento en tablas grandes asegurándote de que las expresiones generadas no sean complejas.
</p>

---

### 📉 Default o valor por defecto 1/2

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar DEFAULT o EXPRESSIONS</strong>:
  - Establecer valores automáticos cuando el usuario no proporciona uno, como:
    - Fecha de creación, estado inicial, etc.
  - Columnas que requieren valores iniciales que pueden depender de funciones o expresiones, como:
    - Obtener el timestamp actual.
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Cómo usar DEFAULT o EXPRESSIONS en PostgreSQL</strong>:
  - Valor por defecto simple: Asignar un valor fijo cuando no se proporciona un valor.
    <code>
    estado VARCHAR(20) DEFAULT 'pendiente'
    </code>
  - Expresión de función para valor dinámico: Usar funciones como `CURRENT_TIMESTAMP` para obtener un valor calculado automáticamente.
    <code>
    fecha_creacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    </code>
  - Otros ejemplos de expresiones:
    - Usar la fecha actual para la columna `fecha_baja`:
      <code>
      fecha_baja DATE DEFAULT CURRENT_DATE
      </code>
    - Usar una secuencia para el valor predeterminado de un ID:
      <code>
      id SERIAL PRIMARY KEY
      </code>
</p>

---

### 📉 Default o valor por defecto 2/2

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Usar `DEFAULT` en columnas que pueden o deben tener un valor inicial común, como estado o fechas de creación.
  - Utilizar funciones en `DEFAULT` para valores dinámicos que dependen de la fecha, hora, o valores generados por la base de datos (por ejemplo, `CURRENT_TIMESTAMP`).
  - Asegurar consistencia: Las columnas con `DEFAULT` deben tener un comportamiento esperado para evitar inconsistencias, especialmente cuando las filas se insertan sin valores específicos.
  - Revisar la compatibilidad de expresiones: PostgreSQL soporta expresiones complejas en `DEFAULT`, por lo que puedes usar operaciones, funciones y cálculos si es necesario.
</p>

===

### 📉 Tablas Dependientes e Independientes en PostgreSQL

<img src="1_La_Tabla/t_5.jpg" alt="tabla 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### Ejemplos de Tablas Independientes

1. 🧑‍💼 Tabla `clientes`
   - Almacena información básica de los clientes, como su nombre, correo electrónico y teléfono, sin depender de otras tablas.

2. 📦 Tabla `productos`
   - Contiene información sobre los productos disponibles, como nombre, precio y categoría. No depende de ninguna otra tabla.

3. 🏢 Tabla `departamentos`
   - Define los departamentos dentro de una empresa (por ejemplo, ventas, recursos humanos), con datos que no dependen de otras tablas.

---

#### Ejemplos de Tablas Dependientes

1. 🛒 Tabla `pedidos`
   - Depende de la tabla `clientes` para asociar cada pedido a un cliente específico, permitiendo un registro organizado de las compras de cada cliente.

2. 📋 Tabla `detalles_pedido`
   - Depende de la tabla `pedidos` y almacena los productos de cada pedido, asociando los productos comprados con un pedido en particular.

3. 👷 Tabla `empleados`
   - Depende de la tabla `departamentos` para indicar en qué departamento trabaja cada empleado, creando una relación de dependencia entre empleados y departamentos.