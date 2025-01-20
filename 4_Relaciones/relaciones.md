### 🧑‍🤝‍🧑 Relaciones

<img src="4_Relaciones/rel_1.jpg" alt="relaciones" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### 📊 Diagrama Entidad Relación

<img src="4_Relaciones/erd_1.webp" alt="diagrama er" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

### Tipos de Relaciones

- 🔗 Relación uno a uno
- 🔄 Relación uno a muchos
- 🔀 Relación muchos a muchos

---

### 1️⃣:1️⃣ Relación Uno a Uno

- 🏷️ Una entidad A se asocia con una sola entidad B
- 🔗 Cada registro de A tiene un solo registro correspondiente en B
- 🧑‍🤝‍🧑 Ejemplo: Un cliente tiene una sola cuenta bancaria
- 🚪 Se usa cuando una entidad tiene una relación directa y exclusiva con otra
- 🔒 Asegura integridad referencial en la base de datos

---

### 1️⃣:🧑‍🤝‍🧑 Relación Uno a Muchos

- 🏷️ Una entidad A se asocia con múltiples registros en la entidad B
- 🔗 Cada registro de A puede estar vinculado a varios registros de B
- 🧑‍🤝‍🧑 Ejemplo: Un autor puede escribir varios libros
- 🔄 La entidad B tiene una clave foránea que hace referencia a la entidad A
- 🔒 Garantiza la integridad referencial entre ambas entidades
- 🛠️ Comúnmente usada en bases de datos para modelar relaciones jerárquica

---

### 🧑‍🤝‍🧑🧑‍🤝‍🧑 Relación M:M Muchos a Muchos

- 🔗 Varias entidades A se pueden asociar con varias entidades B
- 🏷️ Cada registro de A puede estar relacionado con varios registros de B y viceversa
- 🧑‍🤝‍🧑 Ejemplo: Estudiantes pueden estar inscritos en varios cursos y un curso puede tener varios estudiantes
- ➕ Requiere una tabla intermedia (de relación) para gestionar las asociaciones
- 🔄 La tabla intermedia contiene claves foráneas que apuntan a ambas entidades
- 📊 Ideal para modelar relaciones complejas en bases de datos

===

### Relación 1:1 1️⃣

<img src="4_Relaciones/rel_1a1_1.png" alt="uno a uno" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo 1: Persona Pasaporte 🏠

<img src="4_Relaciones/per_pas_1.png" alt="persona pasaporte" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo 2: Usuario - Cuenta Bancaria 🐶

<img src="4_Relaciones/us_cuenta_1.png" alt="persona cuenta bancaria" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo 3: Usuario - Licencia de Conducir ⛱️

<img src="4_Relaciones/rel_1a1_3.png" alt="persona cuenta bancaria" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

### Relación 1:M 🛠️

<img src="4_Relaciones/rel_1am_1.png" alt="uno a muchos" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo: 1 **Clientes y Direcciones 🏠**

<img src="4_Relaciones/rel_1_m_1.png" alt="uno a muchos 1" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo: 2 **Artículos y categorías 🏷️**

<img src="4_Relaciones/rel_1_m_2.png" alt="uno a muchos 2" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo: 3 **Proveedores y Productos 🏭➡️🛒**

<img src="4_Relaciones/rel_1_m_3.png" alt="uno a muchos 3" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

===

### Relación M:M 🧑‍🤝‍🧑

<img src="4_Relaciones/rel_mam_1.png" alt="muchos a muchos" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo 1: Vehículos y Repuestos 🛒

<img src="4_Relaciones/rel_m_m_1.png" alt="muchos a muchos" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo 2: Películas y Actores ⛱️

<img src="4_Relaciones/rel_m_m_2.png" alt="muchos a muchos" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">

---

### Ejemplo 3: Proyectos y Empleados 🧑‍🤝‍🧑

<img src="4_Relaciones/rel_m_m_3.png" alt="muchos a muchos" style="height: 600px; margin: 0 auto 4rem auto; background: transparent; box-shadow: 0 0 10px 10px rgb(150, 156, 238); border-radius: 20px;" class="demo-logo">
