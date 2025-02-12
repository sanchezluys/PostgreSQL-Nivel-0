### JOIN en PostgreSQL 🔗

<img src="5_Join/todos_join.png" alt="todos los joins" style="height: 800px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Uso de JOIN en PostgreSQL 🔗 

En PostgreSQL, los `JOIN` se utilizan para combinar filas de dos o más tablas basadas en una condición común. Existen varios tipos de `JOIN`:

- `INNER JOIN`
- `LEFT JOIN`
- `RIGHT JOIN`
- `FULL JOIN`
- `CROSS JOIN`

---

#### 🔹 INNER JOIN

Devuelve solo las filas que tienen coincidencias en ambas tablas.

<img src="5_Join/inner_join.png" alt="diagrama er" style="height: 600px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
INNER JOIN departamentos ON empleados.departamento_id = departamentos.id;
```

---

#### 🔹 LEFT JOIN (LEFT OUTER JOIN)

Devuelve todas las filas de la tabla izquierda y las coincidencias de la tabla derecha. Si no hay coincidencia, devuelve NULL.

<img src="5_Join/left_join.png" alt="diagrama er" style="height: 600px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
LEFT JOIN departamentos ON empleados.departamento_id = departamentos.id;
```

---

#### 🔹 RIGHT JOIN (RIGHT OUTER JOIN)

Devuelve todas las filas de la tabla derecha y las coincidencias de la tabla izquierda. Si no hay coincidencia, devuelve NULL.

<img src="5_Join/right_join.png" alt="diagrama er" style="height: 600px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
RIGHT JOIN departamentos ON empleados.departamento_id = departamentos.id;
```

---

#### 🔹 FULL JOIN (FULL OUTER JOIN)

Devuelve todas las filas cuando hay una coincidencia en una de las tablas. Si no hay coincidencia, devuelve NULL.

<img src="5_Join/full_join.png" alt="diagrama er" style="height: 600px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

```sql 
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
FULL JOIN departamentos ON empleados.departamento_id = departamentos.id;
```

---

#### 🔹 CROSS JOIN

Devuelve el producto cartesiano de las filas de las tablas involucradas.

<img src="5_Join/cross_join.png" alt="diagrama er" style="height: 600px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

```sql
SELECT empleados.nombre, departamentos.nombre AS departamento
FROM empleados
CROSS JOIN departamentos;
```