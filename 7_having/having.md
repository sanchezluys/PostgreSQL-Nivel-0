## Having

- Se utiliza para filtrar los resultados de las funciones de agregación (similar a WHERE, pero HAVING opera después de la agregación).
- Las **funciones de agregación** son por ejemplo Count(), Sum(), Avg(), etc 
- Es muy común su uso con **Group By** pero no es obligatorio que sea así
- ⚠️ Debe usarse en conjunto con **Las Funciones de Agregación**

---

## ¿Cuándo Usarlo?

Por ejemplo, si quieres contar la cantidad de ventas por producto, pero solo mostrar los productos que tienen más de 100 ventas

- Cuando necesites aplicar condiciones sobre los resultados de las funciones de agregación.
- Útil para filtrar grupos basados en resultados agregados, que no podrías filtrar con WHERE.

---

## Código Ejemplo

```sql
SELECT      producto, 
            COUNT(*) AS total_ventas
FROM        ventas
GROUP BY    producto
HAVING      total_ventas > 100;

-- ***************
-- Algunas Funciones de agregación
-- 1. Count()   -> cuenta registros
-- 2. Sum()     -> suma y acumula
-- 3. Avg()     -> busca el promedio
-- 4. Min()     -> busca el mínimo valor
-- 5. Max()     -> busca el máximo valor

```
