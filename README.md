# Ejercicio 1 - Sistema de Áreas y Empleados (Spark + SQL2o)

## 📌 Objetivo
Este ejercicio forma parte de la **Sección III** del trabajo práctico de Spark, cuyo objetivo es **manejar la persistencia de objetos** utilizando la librería [SQL2o](https://www.sql2o.org).  
SQL2o permite realizar un **mapeo Objeto-Relacional (ORM)** de forma simple, facilitando la conversión de datos entre objetos Java y registros en una base de datos.

En este ejercicio se implementa un sistema que gestiona:
- **Áreas** de una empresa
- **Empleados** asociados a cada área

Se utiliza el patrón **MVC** (sin Velocity) para estructurar el código.

---

## 🛠 Herramientas y Requisitos
- **Java**
- **Spark Java**
- **SQL2o**
- **MySQL** (o cualquier otro motor de base de datos compatible)
- Haber completado las **Partes I y II** del TP de Spark.
- Entorno de desarrollo configurado según las indicaciones previas del TP.

---

## 🗄 Modelo de Base de Datos

### Tablas
**AREA**
| Campo   | Tipo      | Descripción                      |
|---------|-----------|----------------------------------|
| codigo  | PK, int   | Identificador único del área      |
| nombre  | varchar   | Nombre del área                  |
| director| varchar   | Director del área                |

**EMPLEADO**
| Campo     | Tipo      | Descripción                              |
|-----------|-----------|------------------------------------------|
| nombre    | PK, varchar | Nombre del empleado                    |
| categoria | varchar   | Categoría laboral del empleado           |
| dedicacion| varchar   | Dedicación (por ejemplo, tiempo completo)|
| codigo    | FK, int   | Área en la que trabaja (referencia a AREA)|

---

## 📋 Funcionalidades Implementadas
1. **Retornar todas las áreas**  
2. **Retornar todas las áreas con un director específico**  
3. **Buscar todos los empleados con determinada dedicación (`YY`)**  
4. **Buscar todas las áreas que tengan empleados**  
5. **Buscar todos los empleados que trabajen en un área específica**

---

## 🚀 Ejecución
1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/usuario/nombre-repo.git
