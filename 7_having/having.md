### Having

<img src="7_having/having.png" alt="todos los joins" style="height: 800px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Having

- Se utiliza para filtrar los resultados de las funciones de agregación (similar a **WHERE**, pero **HAVING** opera después de la agregación).
- Las **funciones de agregación** son, por ejemplo, `COUNT()`, `SUM()`, `AVG()`, etc.
- Es muy común su uso con **GROUP BY**, pero no es obligatorio que sea así.
- ⚠️ Debe usarse en conjunto con **Las Funciones de Agregación**.

---

### ¿Cuándo Usarlo?

Por ejemplo, si quieres contar la cantidad de ventas por producto, pero solo mostrar los productos que tienen más de 100 ventas:

- Cuando necesites aplicar condiciones sobre los resultados de las funciones de agregación.
- Útil para filtrar grupos basados en resultados agregados, que no podrías filtrar con **WHERE**.

---

### Having en PostgreSQL

<img src="7_having/sql-having.png" alt="todos los joins" style="height: 800px; margin: 0 auto 4rem auto; background: white; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Código Ejemplo

```sql
SELECT      producto, 
            COUNT(*) AS total_ventas
FROM        ventas
GROUP BY    producto
HAVING      total_ventas > 100;

-- ***************
-- Algunas Funciones de Agregación en PostgreSQL:
-- 1. COUNT()   -> cuenta registros
-- 2. SUM()     -> suma y acumula
-- 3. AVG()     -> busca el promedio
-- 4. MIN()     -> busca el mínimo valor
-- 5. MAX()     -> busca el máximo valor
```