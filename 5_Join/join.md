### Uso de JOIN en PostgreSQL 🔗

En PostgreSQL, los `JOIN` se utilizan para combinar filas de dos o más tablas basadas en una condición común. Existen varios tipos de `JOIN`:

- `INNER JOIN`
- `LEFT JOIN`
- `RIGHT JOIN`
- `FULL JOIN`
- `CROSS JOIN`
- `SELF JOIN`
- `NATURAL JOIN`

---

#### 🔹 INNER JOIN
Devuelve solo las filas que tienen coincidencias en ambas tablas.

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
INNER JOIN departamentos ON empleados.departamento_id = departamentos.id;
```

---

#### 🔹 LEFT JOIN (LEFT OUTER JOIN)

Devuelve todas las filas de la tabla izquierda y las coincidencias de la tabla derecha. Si no hay coincidencia, devuelve NULL.

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
LEFT JOIN departamentos ON empleados.departamento_id = departamentos.id;
```

---

#### 🔹 RIGHT JOIN (RIGHT OUTER JOIN)

Devuelve todas las filas de la tabla derecha y las coincidencias de la tabla izquierda. Si no hay coincidencia, devuelve NULL.

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
RIGHT JOIN departamentos ON empleados.departamento_id = departamentos.id;
```

---

#### 🔹 FULL JOIN (FULL OUTER JOIN)

Devuelve todas las filas cuando hay una coincidencia en una de las tablas. Si no hay coincidencia, devuelve NULL.

```sql 
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
FULL JOIN departamentos ON empleados.departamento_id = departamentos.id;
```

---

#### 🔹 CROSS JOIN

Devuelve el producto cartesiano de las filas de las tablas involucradas.

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
CROSS JOIN departamentos;
```

---

#### 🔹 SELF JOIN

Se utiliza para hacer referencia a la misma tabla.

```sql
SELECT e1.nombre, e2.nombre AS jefe
FROM empleados e1
LEFT JOIN empleados e2 ON e1.jefe_id = e2.id;
```

---

#### 🔹 NATURAL JOIN

Devuelve las filas que tienen valores coincidentes en las columnas con el mismo nombre en ambas tablas.

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
NATURAL JOIN departamentos;
```