#### 🧲 Ejercicios de Creación de Tablas en PostgreSQL 1 🧲

- A continuación, se presentan 10 ejercicios para practicar la creación de tablas en PostgreSQL.  
- En cada ejercicio, define las columnas, tipos de datos y clave primaria adecuados según el contexto. Son tablas **independientes**.

---

#### 🌐 Ejercicio 1: Tabla de Redes Sociales  

Crea una tabla llamada `redes_sociales` para almacenar información sobre las redes sociales que usa esta generación y su nivel de popularidad.

#### 📦 Ejercicio 2: Tabla de Productos 

Crea una tabla llamada `productos` que almacene información sobre los productos disponibles en el inventario.

#### 💵 Ejercicio 3: Tabla de Vehículos  

Crea una tabla llamada `vehiculos` para almacenar los registros de los vehículos de un concesionario.

---

#### 🎮 Ejercicio 4: Tabla de Videojuegos 

Crea una tabla llamada `videojuegos` que contenga información sobre los videojuegos más populares y sus características principales.

#### 🚚 Ejercicio 5: Tabla de Proveedores  

Crea una tabla llamada `proveedores` que contenga información sobre los proveedores de una tienda o empresa.

#### 🛠️ Ejercicio 6: Tabla de Repuestos  

Crea una tabla llamada `repuestos` para almacenar los repuestos de motos de un local de servicio técnico para motos.

---

#### 📱 Ejercicio 7: Tabla de Influencers  

Crea una tabla llamada `influencers` para almacenar datos sobre influencers populares, sus plataformas principales y la cantidad de seguidores.

#### 🏥 Ejercicio 8: Tabla de Pacientes  

Crea una tabla llamada `pacientes` para almacenar los datos de los pacientes de una clínica.

#### 📱 Ejercicio 9: Tabla de Celulares  

Crea una tabla llamada `celulares` para almacenar los datos de los celulares de una tienda de celulares.

---

#### 🎓 Ejercicio 10: Tabla de Cursos  
Crea una tabla llamada `cursos` para almacenar información de los cursos ofrecidos en una plataforma educativa.

> **ℹ️ Instrucciones**: En cada ejercicio, piensa cuidadosamente qué columnas se requieren y elige los tipos de datos adecuados. Asegúrate de definir una clave primaria para cada tabla.

---

#### 🛠️ Ejercicios de Creación de Tablas en PostgreSQL para el Área Industrial 🛠️

- A continuación, se presentan 10 ejercicios para practicar la creación de tablas en PostgreSQL orientados al ámbito industrial.  
- En cada ejercicio, define las columnas, tipos de datos y clave primaria adecuados según el contexto.  
- Las tablas son **independientes** y se debe configurar cada columna en cuanto a si debe ser `NOT NULL`, `UNIQUE`, `SERIAL`, etc.

---

#### 🏭 Ejercicio 1: Tabla de Máquinas y Equipos  

Crea una tabla llamada `maquinas_equipos` que almacene información sobre las máquinas utilizadas en una planta industrial.  
Incluye `nombre_equipo`, `codigo`, `tipo`, `fecha_instalacion`, `estado` y `ubicacion`.

#### 🧰 Ejercicio 2: Tabla de Mantenimiento Preventivo  

Crea una tabla llamada `mantenimiento_preventivo` para llevar registro de los mantenimientos programados.  
Define columnas para `equipo_id`, `fecha_mantenimiento`, `tipo_mantenimiento`, `encargado` y `comentarios`.

#### 📦 Ejercicio 3: Tabla de Inventario de Materias Primas  

Crea una tabla llamada `inventario_materias_primas` para almacenar información sobre las materias primas en el inventario.  
Incluye `material`, `codigo`, `cantidad_disponible`, `unidad_medida`, `fecha_ultima_actualizacion` y `proveedor`.

---

#### 🚧 Ejercicio 4: Tabla de Seguridad Industrial  

Crea una tabla llamada `seguridad_industrial` para registrar los incidentes de seguridad en la planta.  
Incluye `tipo_incidente`, `fecha`, `ubicacion`, `descripcion`, `causas` y `medidas_correctivas`.

#### 🚚 Ejercicio 5: Tabla de Proveedores Industriales  

Crea una tabla llamada `proveedores_industriales` que contenga información sobre los proveedores que suministran maquinaria y materiales.  
Incluye `nombre_proveedor`, `codigo_proveedor`, `contacto`, `telefono`, `direccion` y `pais`.

#### 🧪 Ejercicio 6: Tabla de Productos Químicos  

Crea una tabla llamada `productos_quimicos` para gestionar el inventario de productos químicos.  
Define columnas como `nombre_producto`, `codigo_producto`, `cantidad_almacenada`, `unidad`, `fecha_expiracion` y `riesgo`.

---

#### 🛡️ Ejercicio 7: Tabla de Equipos de Protección Personal (EPP)  

Crea una tabla llamada `equipos_proteccion_personal` para registrar la información de los equipos de protección personal entregados a los empleados.  
Incluye `tipo_epp`, `codigo_epp`, `fecha_entrega`, `empleado` y `estado`.

#### 🏗️ Ejercicio 8: Tabla de Proyectos Industriales 

Crea una tabla llamada `proyectos_industriales` para almacenar información sobre los proyectos en curso en la planta.  
Define campos como `nombre_proyecto`, `codigo_proyecto`, `fecha_inicio`, `fecha_fin_estimada`, `estado` y `presupuesto`.

#### 🔧 Ejercicio 9: Tabla de Herramientas  

Crea una tabla llamada `herramientas` para llevar el control de las herramientas utilizadas en la planta.  
Define columnas para `nombre_herramienta`, `codigo_herramienta`, `cantidad_disponible`, `ubicacion` y `estado`.

---

#### 📊 Ejercicio 10: Tabla de Producción Diaria  
Crea una tabla llamada `produccion_diaria` para almacenar los datos de producción de cada día.  
Incluye `fecha`, `turno`, `cantidad_producida`, `equipo`, `operador` y `comentarios`.

> **ℹ️ Instrucciones**: En cada ejercicio, selecciona los tipos de datos adecuados y define una clave primaria para cada tabla.  
> Considera el uso de restricciones como `UNIQUE` en campos que requieren valores únicos, como `codigo_proveedor` o `codigo_equipo`.

---

#### 👞 Ejercicios de Creación de Tablas en PostgreSQL para el Área de Zapaterías 👞

- A continuación, se presentan 10 ejercicios para practicar la creación de tablas en PostgreSQL enfocadas en el mundo de las zapaterías,  
  cubriendo aspectos como la gestión de inventario, producción, proveedores y diseños de calzado.  
- Cada tabla es **independiente** y se debe configurar cada columna en cuanto a si debe ser `NOT NULL`, `UNIQUE`, `SERIAL`, etc.

---

#### 🛍️ Ejercicio 1: Tabla de Tienda de Zapatos  

Crea una tabla llamada `tienda_zapatos` para almacenar información sobre los diferentes modelos de zapatos disponibles en una tienda.  
Incluye `nombre_modelo`, `codigo_producto`, `talla`, `color`, `precio`, `cantidad_disponible` y `categoria` (ej: deportivo, casual, formal).

#### 🏭 Ejercicio 2: Tabla de Producción de Fábrica 

Crea una tabla llamada `produccion_fabrica` que lleve el registro de la producción diaria en una fábrica de zapatos.  
Define columnas para `fecha_produccion`, `modelo`, `cantidad_producida`, `linea_produccion` y `supervisor`.

#### 🧵 Ejercicio 3: Tabla de Materiales  

Crea una tabla llamada `materiales` para gestionar el inventario de materiales utilizados en la fabricación de zapatos.  
Incluye `nombre_material`, `codigo_material`, `cantidad_disponible`, `unidad_medida`, `proveedor` y `fecha_ultima_actualizacion`.

---

#### 👟 Ejercicio 4: Tabla de Diseños de Calzado  

Crea una tabla llamada `disenos_calzado` para almacenar información sobre los diferentes diseños de calzado.  
Define columnas para `nombre_diseno`, `codigo_diseno`, `tipo_calzado`, `materiales_usados`, `disenador` y `fecha_creacion`.

#### 📦 Ejercicio 5: Tabla de Proveedores de Materiales  

Crea una tabla llamada `proveedores_materiales` que contenga información sobre los proveedores de materiales para la producción de zapatos.  
Incluye `nombre_proveedor`, `codigo_proveedor`, `contacto`, `telefono`, `direccion` y `pais_origen`.

#### 🛠️ Ejercicio 6: Tabla de Control de Calidad  

Crea una tabla llamada `control_calidad` para registrar los detalles de las inspecciones de calidad en la producción de calzado.  
Define columnas como `fecha_inspeccion`, `modelo_inspeccionado`, `resultado`, `defectos_detectados` y `inspector`.

---

#### 👔 Ejercicio 7: Tabla de Empleados de Producción  

Crea una tabla llamada `empleados_produccion` para almacenar información sobre los empleados que trabajan en la producción de la fábrica.  
Incluye `nombre_empleado`, `codigo_empleado`, `puesto`, `linea_produccion_asignada`, `fecha_ingreso` y `turno`.

#### 🛒 Ejercicio 8: Tabla de Pedidos de Clientes  

Crea una tabla llamada `pedidos_clientes` para registrar los pedidos realizados por clientes en la tienda de zapatos.  
Incluye `numero_pedido`, `cliente_id`, `fecha_pedido`, `modelo_solicitado`, `cantidad` y `estado_pedido`.

#### 💼 Ejercicio 9: Tabla de Marcas de Zapatos  

Crea una tabla llamada `marcas_zapatos` para gestionar las diferentes marcas de zapatos que maneja la tienda.  
Define columnas para `nombre_marca`, `codigo_marca`, `pais_origen`, `anio_fundacion` y `descripcion`.

---

#### 📈 Ejercicio 10: Tabla de Ventas Mensuales  

Crea una tabla llamada `ventas_mensuales` para almacenar el registro de ventas mensuales de la tienda.  
Incluye `mes`, `anio`, `cantidad_vendida`, `ingresos_totales`, `modelo_mas_vendido` y `empleado_ventas_top`.

> **ℹ️ Instrucciones**: En cada ejercicio, elige los tipos de datos adecuados y define una clave primaria para cada tabla.

> Considera el uso de restricciones como `UNIQUE` en campos que requieran valores únicos, como `codigo_material` o `numero_pedido`.