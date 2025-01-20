## Group By

- Sirve para agrupar datos que se repiten
- Se usa en conjunto con funciones de agregación (Count(), Sum(), Avg()..)

---

## ¿Cuándo Usarlo?

Cuando quieras agrupar datos similares y obtener resultados agregados por grupo, por ejemplo:

- Sumar ventas por mes.
- Contar empleados por departamento.
- Buscar la menor edad separados por sexo de un listado de clientes.


---

## Código Ejemplo

```sql
SELECT          columna1, 
                columna2, 
                FUNCION_AGREGADA(columna3)
FROM            tabla
GROUP BY        columna1, columna2;

-- ***************
-- Algunas Funciones de agregación
-- 1. Count()   -> cuenta registros
-- 2. Sum()     -> suma y acumula
-- 3. Avg()     -> busca el promedio
-- 4. Min()     -> busca el mínimo valor
-- 5. Max()     -> busca el máximo valor
```
