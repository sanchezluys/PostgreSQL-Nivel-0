#### 🌐 Vistas, Eventos, Funciones, Procedimientos y Triggers

<img src="8_herramientas_avanzadas/herramientas.jpg" alt="vistas"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;">

---

#### 📊 Vistas

Las **vistas** son tablas virtuales que permiten visualizar datos sin duplicarlos. Son muy útiles para consultas recurrentes, ya que simplifican la complejidad de las consultas al abstraer la lógica subyacente y permiten acceder a datos específicos de forma rápida y eficiente.

<img src="8_herramientas_avanzadas/vistas_0.png" alt="vistas" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;">


---

#### ⏳ Eventos

Los **eventos** son acciones programadas en **PostgreSQL** que permiten ejecutar tareas automáticamente en intervalos definidos o en momentos específicos. Estos eventos son útiles para realizar tareas periódicas, como mantenimiento de la base de datos o actualizaciones automáticas.

<img src="8_herramientas_avanzadas/eventos.webp" alt="eventos" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">


---

#### 🛠️ Funciones

Las **funciones** en **PostgreSQL** permiten realizar cálculos y transformaciones en los datos de manera modular. Pueden recibir varios argumentos y siempre devuelven un valor, lo que las hace útiles para encapsular lógica y reutilizarla en varias partes de las consultas.

<img src="8_herramientas_avanzadas/funcion.jpeg" alt="funcion" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">


---

#### 🌀 Procedimientos

Los **procedimientos almacenados** en **PostgreSQL** permiten ejecutar un conjunto de instrucciones en la base de datos. A diferencia de las funciones, los procedimientos no devuelven un valor, sino que realizan acciones como actualizaciones, inserciones o eliminaciones, entre otras operaciones.

<img src="8_herramientas_avanzadas/procedimiento.png" alt="procedimiento" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔁 Triggers

Los **triggers** en **PostgreSQL** son acciones automáticas que se ejecutan cuando ocurre un evento específico en una tabla (como una inserción, actualización o eliminación). Los triggers permiten responder a cambios en los datos de manera eficiente, sin necesidad de intervención manual.

<img src="8_herramientas_avanzadas/trigger_0.png" alt="trigger" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

#### 📊 Entendiendo las Vistas

<img src="8_herramientas_avanzadas/vistas_1.png" alt="vista 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 📊 Partes de las Vistas

<img src="8_herramientas_avanzadas/vistas_2.png" alt="vista 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 📊 Código Ejemplo para una Vista

```sql
CREATE VIEW lista AS
    SELECT 
        Dpto.departamento AS DEPARTAMENTO,
        Mcipio.municipio AS MUNICIPIOS
    FROM
        departamentos Dpto
    JOIN municipios Mcipio 
        ON Dpto.id_departamento = Mcipio.departamento_id;
```

===

#### 🛠️ Entendiendo las Funciones

<img src="8_herramientas_avanzadas/funcion_1.png" alt="Funcion 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Partes de las Funciones

<img src="8_herramientas_avanzadas/funcion_2.png" alt="funcion 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Código Básico Ejemplo para una Función

```sql
CREATE FUNCTION nombre_completo(nombre VARCHAR(50), apellido VARCHAR(50))
RETURNS VARCHAR(101)
LANGUAGE plpgsql
AS $$
BEGIN
    RETURN nombre || ' ' || apellido;
END;
$$;
```

---

#### 🛠️ Código Intermedio Ejemplo para una Función

```sql
CREATE FUNCTION format_full_name(first_name VARCHAR(50), 
                                middle_name VARCHAR(50), 
                                last_name VARCHAR(50))
RETURNS VARCHAR(151)
LANGUAGE plpgsql
AS $$
DECLARE
    full_name VARCHAR(151);
BEGIN
    -- Inicializa full_name como una cadena vacía
    full_name := '';

    -- Si el primer nombre no es nulo, agregarlo
    IF first_name IS NOT NULL THEN
        full_name := first_name;
    END IF;

    -- Si el segundo nombre no es nulo, agregarlo con un espacio
    IF middle_name IS NOT NULL THEN
        full_name := full_name || ' ' || middle_name;
    END IF;

    -- Si el apellido no es nulo, agregarlo con un espacio
    IF last_name IS NOT NULL THEN
        full_name := full_name || ' ' || last_name;
    END IF;

    -- Retorna el nombre completo, eliminando espacios en blanco adicionales
    RETURN TRIM(full_name);
END;
$$;
```

===

#### 🌀 Entendiendo los Procedimientos

<img src="8_herramientas_avanzadas/procedimiento_1.png" alt="procedimiento 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🌀 Partes de los Procedimientos

<img src="8_herramientas_avanzadas/procedimiento_2.png" alt="procedimiento 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🌀 Código Básico Ejemplo para un Procedimiento

```sql
CREATE OR REPLACE PROCEDURE insertarCliente(
    p_nombre VARCHAR(50),
    p_email VARCHAR(50),
    p_telefono VARCHAR(15)
)
LANGUAGE plpgsql
AS $$
BEGIN
    -- Insertar un nuevo cliente en la tabla "clientes"
    INSERT INTO clientes (nombre, email, telefono)
    VALUES (p_nombre, p_email, p_telefono);
END;
$$;
```

---

#### 🌀 Código Intermedio Ejemplo para un Procedimiento

```sql
CREATE OR REPLACE PROCEDURE actualizarOInsertarCliente(
    p_id INT,
    p_nombre VARCHAR(50),
    p_email VARCHAR(50),
    p_telefono VARCHAR(15)
)
LANGUAGE plpgsql
AS $$
DECLARE
    cliente_existe INT DEFAULT 0;
BEGIN
    -- Verificar si el cliente ya existe
    SELECT COUNT(*) INTO cliente_existe
    FROM clientes
    WHERE id = p_id;

    IF cliente_existe > 0 THEN
        -- Actualizar la información del cliente existente
        UPDATE clientes
        SET nombre = p_nombre, email = p_email, telefono = p_telefono
        WHERE id = p_id;
        RAISE NOTICE 'Cliente actualizado';
    ELSE
        -- Insertar un nuevo cliente
        INSERT INTO clientes (nombre, email, telefono)
        VALUES (p_nombre, p_email, p_telefono);
        RAISE NOTICE 'Cliente insertado';
    END IF;
END;
$$;
```

===

#### 🔁 Entendiendo los Triggers o Disparadores

<img src="8_herramientas_avanzadas/trigger_1.png" alt="procedimiento 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔁 Partes de los Trigger

<img src="8_herramientas_avanzadas/trigger_2.png" alt="procedimiento 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔁 Código Básico Ejemplo para un Trigger

```sql
-- Asumiendo la existencia de estas 2 tablas
-- cada vez que un salario sea modificado notificarlo en la tabla auditoria_empleados

CREATE TABLE empleados (
    id SERIAL PRIMARY KEY,
    nombre VARCHAR(100),
    salario DECIMAL(10, 2)
);

CREATE TABLE auditoria_empleados (
    id SERIAL PRIMARY KEY,
    empleado_id INT,
    viejo_salario DECIMAL(10, 2),
    nuevo_salario DECIMAL(10, 2),
    fecha_modificacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Trigger:

CREATE OR REPLACE FUNCTION after_salario_update_fn() 
RETURNS TRIGGER AS $$
BEGIN
    IF OLD.salario != NEW.salario THEN
        INSERT INTO auditoria_empleados (empleado_id, viejo_salario, nuevo_salario)
        VALUES (OLD.id, OLD.salario, NEW.salario);
    END IF;
    RETURN NEW;
END;
$$ LANGUAGE plpgsql;

CREATE TRIGGER after_salario_update
AFTER UPDATE ON empleados
FOR EACH ROW
EXECUTE FUNCTION after_salario_update_fn();
```

---

#### 🔁 Código Intermedio Ejemplo para un Trigger

```sql
-- Queremos asegurarnos de que ningún empleado reciba un aumento de salario mayor al 50% en una sola actualización.
-- Si el aumento es mayor al 50%, el trigger revertirá el cambio y lanzará un error.
-- También registrará cualquier cambio válido en la tabla auditoria_empleados.

CREATE OR REPLACE FUNCTION before_salario_update_fn() 
RETURNS TRIGGER AS $$
DECLARE 
    salario_aumento DECIMAL(10, 2);
BEGIN
    -- Calcular el porcentaje de aumento
    salario_aumento := (NEW.salario - OLD.salario) / OLD.salario * 100;

    -- Verificar si el aumento es mayor al 50%
    IF salario_aumento > 50 THEN
        -- Lanzar un error para evitar el aumento
        RAISE EXCEPTION 'El aumento no puede ser mayor al 50% del salario anterior';
    ELSE
        -- Registrar los cambios válidos en la auditoría
        INSERT INTO auditoria_empleados (empleado_id, viejo_salario, nuevo_salario)
        VALUES (OLD.id, OLD.salario, NEW.salario);
    END IF;
    RETURN NEW;
END;
$$ LANGUAGE plpgsql;

CREATE TRIGGER before_salario_update
BEFORE UPDATE ON empleados
FOR EACH ROW
EXECUTE FUNCTION before_salario_update_fn();
```