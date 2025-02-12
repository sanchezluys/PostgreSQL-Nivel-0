#### 🌐 Vistas, Eventos, Funciones, Procedimientos y Triggers

<img src="img/herr_avan/herramientas.jpg" alt="vistas"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;">

---

#### 📊 Vistas

Las **vistas** son tablas virtuales que permiten visualizar datos sin duplicarlos. Muy útil para querys recurrentes

<img src="img/herr_avan/vistas_1.png" alt="vistas"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;">

---

#### ⏳ Eventos

Los **eventos** son acciones programadas en MySQL que ocurren automáticamente en intervalos definidos o en un momento específico.

<img src="img/herr_avan/eventos.webp" alt="eventos"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Funciones

Las **funciones** permiten realizar cálculos y transformaciones en los datos de manera modular. Pueden recibir varios argumentos y devuelven un valor **siempre**

<img src="img/herr_avan/funcion.jpeg" alt="funcion"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🌀 Procedimientos

Los **procedimientos almacenados** permiten ejecutar un conjunto de instrucciones en MySQL. No devuelven ningún valor.

<img src="img/herr_avan/procedimiento.png" alt="procedimiento"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔁 Triggers

Los **triggers** son acciones automáticas que se ejecutan cuando ocurre un evento en una tabla (como una inserción o actualización). El flujo de un trigger es el siguiente:

<img src="img/herr_avan/trigger.jpg" alt="trigger"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔗 Conclusión

En resumen, estos componentes permiten a MySQL gestionar datos de manera automatizada, modular y eficiente. Utiliza herramientas para mejorar el rendimiento de tus bases de datos. 🚀

<img src="img/herr_avan/conclusion.jpg" alt="conclusion"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

#### 📊 Entendiendo las Vistas

<img src="img/herr_avan/v_1.png" alt="vista 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 📊 Partes de las Vistas

<img src="img/herr_avan/v_2.png" alt="vista 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 📊 Código Ejemplo para una Vista

```sql

CREATE 
        ALGORITHM = UNDEFINED 
        DEFINER = `credicel_profesor`@`%` 
        SQL SECURITY DEFINER
VIEW    `lista` AS
        SELECT 
            `Dpto`.`departamento` AS `DEPARTAMENTO`,
            `Mcipio`.`municipio` AS `MUNICIPIOS`
        FROM
            (`departamentos` `Dpto`
            JOIN `municipios` `Mcipio` 
                ON (`Dpto`.`id_departamento` = `Mcipio`.`departamento_id`))

```

===

#### 🛠️ Entendiendo las Funciones

<img src="img/herr_avan/f/f_1.png" alt="Funcion 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Partes de las Funciones

<img src="img/herr_avan/f/f_2.png" alt="funcion 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🛠️ Código Básico Ejemplo para una Función

```sql

DELIMITER $$

CREATE FUNCTION nombre_completo(nombre VARCHAR(50), apellido VARCHAR(50))
RETURNS VARCHAR(101)
DETERMINISTIC
BEGIN
    RETURN CONCAT(nombre, ' ', apellido);
END $$

DELIMITER ;

```

---

#### 🛠️ Código Intermedio Ejemplo para una Función

```sql

DELIMITER $$

CREATE FUNCTION format_full_name(first_name VARCHAR(50), 
                                middle_name VARCHAR(50), 
                                last_name VARCHAR(50))
RETURNS VARCHAR(151)
DETERMINISTIC
BEGIN
    DECLARE full_name VARCHAR(151);
    
    -- Inicializa full_name como una cadena vacía
    SET full_name = '';
    
    -- Si el primer nombre no es nulo, agregarlo
    IF first_name IS NOT NULL THEN
        SET full_name = first_name;
    END IF;
    
    -- Si el segundo nombre no es nulo, agregarlo con un espacio
    IF middle_name IS NOT NULL THEN
        SET full_name = CONCAT(full_name, ' ', middle_name);
    END IF;
    
    -- Si el apellido no es nulo, agregarlo con un espacio
    IF last_name IS NOT NULL THEN
        SET full_name = CONCAT(full_name, ' ', last_name);
    END IF;
    
    -- Retorna el nombre completo, eliminando espacios en blanco adicionales
    RETURN TRIM(full_name);
END $$

DELIMITER ;


```

===

#### 🌀 Entendiendo los Procedimientos

<img src="img/herr_avan/p/p_1.png" alt="procedimiento 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🌀 Partes de los Procedimientos

<img src="img/herr_avan/p/p_2.png" alt="procedimiento 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🌀 Código Básico Ejemplo para un Procedimiento

```sql

DELIMITER $$

CREATE PROCEDURE insertarCliente(
    IN p_nombre VARCHAR(50),
    IN p_email VARCHAR(50),
    IN p_telefono VARCHAR(15)
)
BEGIN
    -- Insertar un nuevo cliente en la tabla "clientes"
    INSERT INTO clientes (nombre, email, telefono)
    VALUES (p_nombre, p_email, p_telefono);
END$$

DELIMITER ;

```

---

#### 🌀 Código Intermedio Ejemplo para una los Procedimientos

```sql

DELIMITER $$

CREATE PROCEDURE actualizarOInsertarCliente(
    IN p_id INT,
    IN p_nombre VARCHAR(50),
    IN p_email VARCHAR(50),
    IN p_telefono VARCHAR(15)
)
BEGIN
    DECLARE cliente_existe INT DEFAULT 0;

    -- Verificar si el cliente ya existe
    SELECT COUNT(*) INTO cliente_existe
    FROM clientes
    WHERE id = p_id;

    IF cliente_existe > 0 THEN
        -- Actualizar la información del cliente existente
        UPDATE clientes
        SET nombre = p_nombre, email = p_email, telefono = p_telefono
        WHERE id = p_id;
        SELECT 'Cliente actualizado' AS mensaje;
    ELSE
        -- Insertar un nuevo cliente
        INSERT INTO clientes (nombre, email, telefono)
        VALUES (p_nombre, p_email, p_telefono);
        SELECT 'Cliente insertado' AS mensaje;
    END IF;
END$$

DELIMITER ;

```

===

#### 🔁 Entendiendo los Triggers o Disparadores

<img src="img/herr_avan/trigg/trigg_1.png" alt="procedimiento 1"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔁 Partes de los Trigger

<img src="img/herr_avan/trigg/trigg_2.png" alt="procedimiento 2"	style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

#### 🔁 Código Básico Ejemplo para un Trigger

```sql
-- Asumiendo la existencia de estas 2 tablas
-- cada vez que un salario sea modificado notificarlo en la tabla auditoria_empleados

CREATE TABLE empleados (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(100),
    salario DECIMAL(10, 2)
);

CREATE TABLE auditoria_empleados (
    id INT PRIMARY KEY AUTO_INCREMENT,
    empleado_id INT,
    viejo_salario DECIMAL(10, 2),
    nuevo_salario DECIMAL(10, 2),
    fecha_modificacion TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Trigger:

DELIMITER $$

CREATE TRIGGER after_salario_update
AFTER UPDATE ON empleados
FOR EACH ROW
BEGIN
    IF OLD.salario != NEW.salario THEN
        INSERT INTO auditoria_empleados (empleado_id, viejo_salario, nuevo_salario)
        VALUES (OLD.id, OLD.salario, NEW.salario);
    END IF;
END$$

DELIMITER ;
```

---

#### 🔁 Código Intermedio Ejemplo para un Trigger

```sql
-- Queremos asegurarnos de que ningún empleado reciba un aumento de salario mayor al 50% en una sola actualización.
-- Si el aumento es mayor al 50%, el trigger revertirá el cambio y lanzará un error.
-- También registrará cualquier cambio válido en la tabla auditoria_empleados.

DELIMITER $$

CREATE TRIGGER before_salario_update
BEFORE UPDATE ON empleados
FOR EACH ROW
BEGIN
    DECLARE salario_aumento DECIMAL(10, 2);
    
    -- Calcular el porcentaje de aumento
    SET salario_aumento = (NEW.salario - OLD.salario) / OLD.salario * 100;

    -- Verificar si el aumento es mayor al 50%
    IF salario_aumento > 50 THEN
        -- Lanzar un error para evitar el aumento
        SIGNAL SQLSTATE '45000' 
        SET MESSAGE_TEXT = 'El aumento no puede ser mayor al 50% del salario anterior';
    ELSE
        -- Registrar los cambios válidos en la auditoría
        INSERT INTO auditoria_empleados (empleado_id, viejo_salario, nuevo_salario)
        VALUES (OLD.id, OLD.salario, NEW.salario);
    END IF;
END$$

DELIMITER ;
```

---

### Verificando Diagrama de Flujo

<div class="slides">
    <section>
        <div class="mermaid">
            flowchart TD
                A[Start] --> B{Is it?};
                B -- Yes --> C[OK];
                C --> D[Rethink];
                D --> B;
                B -- No --> E[End];
        </div>
    </section>
</div>

