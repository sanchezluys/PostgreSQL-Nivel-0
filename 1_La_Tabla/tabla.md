## 📃 Primer Pilar La Tabla

<img src="1_La_Tabla/tabla_1.webp" alt="tabla"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

### 📘 La tabla - Datos

<img src="1_La_Tabla/t_1.gif" alt="tabla 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 🎛️ La tabla - Workbench

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

### 🔢 Tipo de Dato

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🔢 Datos Numéricos</strong>:
  - INT: Para números enteros (id, cantidad, edad)
  - DECIMAL(10,2): Para valores monetarios (precio, salario)
  - TINYINT(1): Para booleanos (es_activo, tiene_stock)
  - FLOAT: Para números decimales sin precisión exacta
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>📝 Datos de Texto</strong>:
  - VARCHAR(50): Textos cortos variables (nombre, email)
  - CHAR(10): Textos fijos (código_postal)
  - TEXT: Textos largos (descripcion, contenido)
  - ENUM: Valores predefinidos (estado, tipo)
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>📅 Datos de Fecha/Hora</strong>:
  - DATE: Solo fecha (fecha_nacimiento)
  - TIME: Solo hora (hora_entrada)
  - DATETIME: Fecha y hora (fecha_creacion)
  - TIMESTAMP: Marcas temporales (ultima_actualizacion)
</p>

<p class="fragment" data-fragment-index="4" style="text-align: left;">
  4. <strong>🎯 Datos Especiales</strong>:
  - BLOB: Datos binarios (imagen, archivo)
  - JSON: Datos en formato JSON (configuracion)
  - GEOMETRY: Datos geográficos (ubicacion)
  - UUID: Identificadores únicos (token)
</p>

---

### 🔑 PK - Llave primaria

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🔑 Estructura Básica PK</strong>:
  - Nombre: id o id_[tabla]
  - Tipo: INT o BIGINT
  - Propiedades: NOT NULL + AUTO_INCREMENT
  - Ejemplo: id INT NOT NULL AUTO_INCREMENT PRIMARY KEY
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>📋 Tipos Comunes de PK</strong>:
  - Numérica autoincremental: id INT (más común)
  - UUID: id CHAR(36)
  - Compuesta: (codigo_pais, dni)
  - Natural: numero_documento VARCHAR(20)
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Siempre usar NOT NULL
  - Preferir AUTO_INCREMENT
  - Evitar PKs compuestas si es posible
  - Indexar automáticamente (MySQL lo hace)
  - Considerar el crecimiento de datos
</p>

---

### ❗ NN - No Nulo

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>❗ Cuándo usar NOT NULL</strong>:
  - Campos obligatorios (nombre, email)
  - Llaves primarias (id)
  - Campos de fechas importantes (fecha_creacion)
  - Campos de estado (estado_pedido)
  - Cantidades y precios (precio_total)
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>⚠️ Cuándo permitir NULL</strong>:
  - Campos opcionales (segundo_nombre)
  - Fechas futuras (fecha_cancelacion)
  - Campos que pueden no aplicar (fecha_baja)
  - Datos complementarios (observaciones)
  - Referencias opcionales (supervisor_id)
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>💡 Mejores Prácticas</strong>:
  - Usar valores por defecto cuando sea posible
  - Documentar por qué se permite NULL
  - Considerar el impacto en consultas
  - Evitar NULL en campos de cálculos
  - Preferir NOT NULL para mejor rendimiento
</p>

---

### 🎯 UQ - Valor Unico

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar UNIQUE</strong>:
  - Correo electrónico (email)
  - Número de documento (dni, rut)
  - Nombre de usuario (username)
  - Códigos de producto (sku, codigo_barras)
  - Número de serie (serial_number)
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Tipos de UNIQUE</strong>:
  - Simple (una columna):
    <code>
    email VARCHAR(100) UNIQUE
    </code>
  - Compuesto (múltiples columnas):
    <code>
    UNIQUE KEY (codigo_pais, numero_documento)
    </code>
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Combinar con NOT NULL si el campo es obligatorio
  - Considerar índices para mejor rendimiento
  - Validar mayúsculas/minúsculas
  - Evaluar si realmente necesita ser único
  - Planear la gestión de duplicados
</p>

---

### 🔄 B - Columna Binaria

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar BINARY</strong>:
  - Contraseñas o hashes de contraseñas
  - Identificadores únicos (UUID en binario)
  - Tokens de autenticación
  - Archivos binarios pequeños
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Tipos de BINARY</strong>:
  - Longitud fija:
    <code>
    token BINARY(16)
    </code>
  - Longitud variable:
    <code>
    hash_password VARBINARY(64)
    </code>
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Definir la longitud exacta para optimizar espacio
  - Combinar con NOT NULL si es obligatorio
  - Asegurar que los datos sean compatibles con almacenamiento binario
  - Considerar índices para búsqueda rápida
</p>

---

### ⚡ UN - Sin signo

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar UNSIGNED</strong>:
  - Valores que nunca serán negativos (ej.: cantidades, edades, identificadores)
  - Columnas que necesitan maximizar el rango positivo (ej.: ID de usuarios, contadores)
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Tipos de UNSIGNED</strong>:
  - Enteros:
    <code>
    edad TINYINT UNSIGNED
    </code>
  - IDs o claves foráneas:
    <code>
    usuario_id INT UNSIGNED
    </code>
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Usar `UNSIGNED` solo cuando se está seguro de que el valor no será negativo
  - Considerar `UNSIGNED` en columnas de identificadores para maximizar el rango positivo
  - Revisar si la aplicación soporta el rango extendido de `UNSIGNED`
</p>

---

### 🕹️ ZF - Relleno con ceros - Zero Fill

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar ZEROFILL</strong>:
  - Números que necesitan formato de longitud fija con ceros a la izquierda (ej.: códigos de productos, números de cuenta)
  - Identificadores donde el formato visual es importante, pero no el valor en sí
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Tipos de ZEROFILL</strong>:
  - Entero con relleno de ceros:
    <code>
    codigo_producto INT ZEROFILL
    </code>
  - Longitud fija:
    <code>
    numero_cuenta INT(8) ZEROFILL
    </code>
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Utilizar `ZEROFILL` cuando se requiera formato visual uniforme
  - No combinar con `UNSIGNED` ya que `ZEROFILL` lo aplica automáticamente
  - Evaluar si el valor de longitud fija es necesario para propósitos visuales
</p>

---

### 📞 AI - Auto incremental

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar AUTO_INCREMENT</strong>:
  - Identificadores únicos de registros (ej.: ID de usuarios, pedidos, productos)
  - Claves primarias que deben incrementarse automáticamente para cada nuevo registro
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Tipos de AUTO_INCREMENT</strong>:
  - Entero estándar:
    <code>
    id INT AUTO_INCREMENT
    </code>
  - Entero sin signo para maximizar el rango:
    <code>
    id INT UNSIGNED AUTO_INCREMENT
    </code>
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Definir `AUTO_INCREMENT` en una clave primaria o índice único
  - Usar `UNSIGNED` si el valor no será negativo para ampliar el rango positivo
  - Evitar `AUTO_INCREMENT` en columnas que puedan necesitar valores personalizados
  - Configurar un valor de inicio o incremento si es necesario con `AUTO_INCREMENT = valor_inicial`
</p>

---

### 🏷️ G - Columna Generada

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar COLUMNAS GENERADAS</strong>:
  - Campos derivados de otros valores en la misma fila (ej.: edad a partir de fecha de nacimiento, total con impuestos)
  - Cálculos o concatenaciones que se necesitan frecuentemente pero no deberían almacenarse manualmente
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Tipos de COLUMNAS GENERADAS</strong>:
  - Generadas almacenadas (valor calculado y almacenado):
    <code>
    total_con_impuesto DECIMAL(10,2) GENERATED ALWAYS AS (precio * 1.19) STORED
    </code>
  - Generadas virtuales (calculado cada vez que se consulta):
    <code>
    nombre_completo VARCHAR(255) GENERATED ALWAYS AS (CONCAT(nombre, ' ', apellido)) VIRTUAL
    </code>
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Usar `STORED` para valores calculados que se consultan frecuentemente y mejoran el rendimiento
  - Usar `VIRTUAL` cuando el cálculo es ocasional para ahorrar espacio de almacenamiento
  - Asegurar que las columnas fuente existan y estén correctamente tipificadas
  - Verificar que las columnas generadas estén optimizadas y no afecten el rendimiento en tablas grandes
</p>

---

### 📉 Default/Expression Expresión o valor por defecto

<p class="fragment" data-fragment-index="1" style="text-align: left;">
  1. <strong>🎯 Cuándo usar DEFAULT o EXPRESSIONS</strong>:
  - Establecer valores automáticos si el usuario no proporciona uno (ej.: fecha de creación, estatus inicial)
  - Columnas que requieren valores iniciales que pueden depender de funciones o expresiones (ej.: timestamp actual)
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
  2. <strong>🔄 Tipos de DEFAULT o EXPRESSIONS</strong>:
  - Valor por defecto simple:
<code>
estado VARCHAR(20) DEFAULT 'pendiente'
</code>
  - Expresión de función para valor dinámico:
    <code>
    fecha_creacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    </code>
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
  3. <strong>⚡ Mejores Prácticas</strong>:
  - Usar `DEFAULT` en columnas que pueden o deben tener un valor inicial común
  - Utilizar funciones en `DEFAULT` para valores dinámicos (ej.: `CURRENT_TIMESTAMP` para fechas)
  - Asegurar que las columnas con `DEFAULT` reflejen el comportamiento esperado para evitar problemas de consistencia
  - Revisar si la base de datos soporta expresiones en `DEFAULT` para columnas calculadas
</p>

===

### 📉 Tablas Dependientes e Independientes en MySQL

<img src="1_La_Tabla/t_5.jpg" alt="tabla 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### Ejemplos de Tablas Independientes

1. **🧑‍💼 Tabla `clientes`**
   - Almacena información básica de los clientes, como su nombre, correo electrónico y teléfono, sin depender de otras tablas.

2. **📦 Tabla `productos`**
   - Contiene información sobre los productos disponibles, como nombre, precio y categoría. No depende de ninguna otra tabla.

3. **🏢 Tabla `departamentos`**
   - Define los departamentos dentro de una empresa (por ejemplo, ventas, recursos humanos), con datos que no dependen de otras tablas.

---

#### Ejemplos de Tablas Dependientes

1. **🛒 Tabla `pedidos`**
   - Depende de la tabla `clientes` para asociar cada pedido a un cliente específico, permitiendo un registro organizado de las compras de cada cliente.

2. **📋 Tabla `detalles_pedido`**
   - Depende de la tabla `pedidos` y almacena los productos de cada pedido, asociando los productos comprados con un pedido en particular.

3. **👷 Tabla `empleados`**
   - Depende de la tabla `departamentos` para indicar en qué departamento trabaja cada empleado, creando una relación de dependencia entre empleados y departamentos.
