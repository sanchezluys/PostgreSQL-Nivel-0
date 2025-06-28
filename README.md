## PostgreSQL-Nivel-0

Este repositorio contiene un curso educativo completo de PostgreSQL nivel básico, implementado como una plataforma de presentaciones interactivas usando Reveal.js. [1](#0-0) 

### 🎯 Objetivos del Curso

El curso está diseñado para enseñar los fundamentos de PostgreSQL a través de objetivos específicos: [2](#0-1) 

- **🗄️ Bases de datos Relacionales**: Comprender la estructura de datos en tablas relacionadas
- **📊 Tablas**: Crear y gestionar tablas de forma eficiente  
- **🔗 Relaciones entre tablas**: Establecer relaciones mediante claves primarias y foráneas
- **🛠️ CRUD**: Realizar operaciones básicas (Crear, Leer, Actualizar, Eliminar)
- **🔍 Consultas SQL**: Ejecutar consultas para recuperar y manipular datos
- **🚀 Publicar en GitHub**: Desarrollar y publicar una base de datos en GitHub

### 📋 Requisitos del Sistema

Para utilizar esta plataforma educativa necesitas: [3](#0-2) 

- **💻 Computadora**: Equipo adecuado para desarrollo y gestión de bases de datos
- **🌐 Conexión a Internet**: Para colaboración y acceso a recursos en la nube
- **☁️ Servidor PostgreSQL**: Instancia de PostgreSQL en la nube
- **💻 pgAdmin**: Herramienta de gestión de bases de datos
- **🌐 GitHub**: Para versionado y colaboración de proyectos
- **🧑‍🤝‍🧑 Trabajo en equipo**: Colaboración activa con otros desarrolladores
- **⚙️ Metodologías ágiles**: Uso de Scrum o Kanban

### 🚀 Instalación y Configuración

#### PostgreSQL y pgAdmin

1. **Descargar PostgreSQL**: Obtén la versión más reciente desde el sitio oficial. PostgreSQL es completamente gratuito y de código abierto. [4](#0-3) 

2. **Instalar pgAdmin**: Descarga desde `https://www.pgadmin.org/download/` y sigue las instrucciones de instalación. [5](#0-4) 

3. **Configurar conexión**: [6](#0-5) 
   - **Host**: `tu-host.com / IP`
   - **Puerto**: `5432` (por defecto)
   - **Usuario**: `tu_usuario`
   - **Contraseña**: `tu_clave_secreta`
   - **Base de datos**: `tu_base_de_datos`

### 📚 Estructura del Curso

El curso está organizado en módulos progresivos:

#### Módulos Principales

1. **0_Introduccion** - Conceptos fundamentales de proyectos IT y requisitos [7](#0-6) 
2. **1_La_Tabla** - Diseño de tablas y tipos de datos [8](#0-7) 
3. **3_SQL_Consultas** - Consultas SQL y funciones [9](#0-8) 
4. **4_Relaciones** - Relaciones entre tablas (1:1, 1:M, M:M) [10](#0-9) 
5. **8_herramientas_avanzadas** - Vistas, funciones, procedimientos y triggers [11](#0-10) 

#### Ejercicios Prácticos

- **100_Talleres** - Configuración de herramientas y talleres prácticos [12](#0-11) 
- **101_Tablas_Ejercicios** - Ejercicios de creación de tablas para diferentes sectores [13](#0-12) 

### 🛠️ Características Técnicas

#### Plataforma de Presentación

El curso utiliza **Reveal.js** como framework de presentación con características avanzadas: [14](#0-13) 

- **Plugin Anything**: Para contenido interactivo y elementos HTML personalizados
- **Plugin Seminar**: Para colaboración en tiempo real y sistema de Q&A
- **Chart.js**: Para visualizaciones de datos
- **Chalkboard**: Para anotaciones interactivas

#### Convenciones de Código

El curso enseña las mejores prácticas de nomenclatura: [15](#0-14) 

- **snake_case**: Para nombres de columnas (`fecha_nacimiento`)
- **Descriptivo y conciso**: Nombres claros (`correo_electronico`)
- **Patrones consistentes**: Prefijos y sufijos estándar (`id_usuario`, `categoria_id`)

### 📊 Conceptos PostgreSQL Cubiertos

#### Tipos de Datos

- **Numéricos**: `INTEGER`, `NUMERIC(10,2)`, `BIGINT` [16](#0-15) 
- **Texto**: `VARCHAR(50)`, `CHAR(10)`, `TEXT` [17](#0-16) 
- **Fecha/Hora**: `DATE`, `TIMESTAMP`, `TIMESTAMPTZ` [18](#0-17) 
- **Especiales**: `JSONB`, `BYTEA`, `GEOGRAPHY` [19](#0-18) 

#### Funciones SQL

El curso cubre diferentes categorías de funciones PostgreSQL: [20](#0-19) 

- **Numéricas**: `ABS()`, `CEIL()`, `FLOOR()`, `ROUND()`
- **Cadenas**: `CONCAT()`, `LOWER()`, `UPPER()`, `STRING_AGG()`
- **Fechas**: `NOW()`, `CURRENT_DATE`, `TO_CHAR()`
- **Lógicas**: `CASE WHEN`, `COALESCE()`, `NULLIF()`

### 🎓 Cómo Usar Este Repositorio

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/sanchezluys/PostgreSQL-Nivel-0.git
   ```

2. **Abrir las presentaciones**: Navega a `index.html` en tu navegador web

3. **Seguir el orden de módulos**: Comienza con `0_Introduccion` y progresa secuencialmente

4. **Practicar con ejercicios**: Utiliza los talleres en `100_Talleres` y `101_Tablas_Ejercicios`

5. **Configurar PostgreSQL**: Sigue las instrucciones en el módulo de talleres para configurar tu entorno

### 🤝 Contribuciones

Este es un proyecto educativo diseñado para aprendizaje colaborativo usando metodologías ágiles y GitHub para versionado. [21](#0-20) 

### 📄 Licencia

PostgreSQL es un sistema de gestión de bases de datos completamente gratuito y de código abierto. [22](#0-21) 

---

**Autor**: Luis Sánchez  
**Repositorio**: [PostgreSQL-Nivel-0](https://github.com/sanchezluys/PostgreSQL-Nivel-0)

[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/sanchezluys/PostgreSQL-Nivel-0)