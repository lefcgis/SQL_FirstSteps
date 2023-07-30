# SQL: Primeros pasos👨‍💻💊

![wallpaper](images/mysql.jpg)

<br />

<h1>💊¿Qué es SQL? 💊</h1>

<b>SQL</b> es el Lenguaje Estructuado de Consultas. Es usado para almacenar y administrar datos a través de un sistema de bases de datos relacionales (**RDBMS**).<br />
<br />
PostgreSQL, MySQL, SQLite, Oracle, SQL Server, entre otros son algunas de las tecnologías qe utilizan este lenguaje.<br />
<br />
<br />
_Lucho Ferrer_ 👨‍💻
*****************************************************************************************************************

<h1>💊 Comandos 💊</h1>

<h2>🌱SELECT</h2>
<b>Extrae</b> información desde una base de datos. La data resultante es almacenada en una tabla de resultados llamada Conjunto de resultados (result - set).<br />
<br />

**SELECT Columna 1, Columna 2,...**<br />
**FROM nombre_tabla**<br />
<br />
Columna 1 y Columna 2 son los nombres de los campos de la tabla desde donde quieres seleccionar los datos. Si deseas seleccionar todos los campos disponibles en la tabla, utiiza la siguiente sintaxis.<br />

Por ejemplo:<br />
**SELECT * FROM nombre_tabla**
*****************************************************************************************************************
<h2>🌱ORDER BY</h2>
<b>Ordena</b>los resultados de una consulta en un orden específico.<br />
<br />

Por ejemplo:<br />
**SELECT * FROM nombres**<br />
**ORDER BY edad ASC**
*****************************************************************************************************************
<h2>🌱GROUP BY</h2>
<b>Agrupa</b> filas similares en conjunto, basándose en una o más columnas.<br />
Se coloca luego de la función WHERE y se especifican las columnas por las que se desea agrupar.<br />
<br />

Por ejemplo:<br />
**SELECT carreras, COUNT (carreras)**<br />
**FROM nombres GROUP BY "category"**
*****************************************************************************************************************
<h2>🌱WHERE</h2>
<b>Filtra</b>los resultados de una consulta. Se coloca luego del comando SELECT.<br />
<br />

Por ejemplo:<br />

**SELECT * FROM clientes**<br />
**WHERE edad>20**
*****************************************************************************************************************
<h2>🌱 UPDATE</h2>
Es utilizado para <b>modificar</b> registros existentes en una tabla.<br />
<br />

**UPDATE nombre_tabla**<br />
**SET columna 1= valor 1,**<br />
      columna 2= valor 2,...<br />
**WHERE Condición;**<br />
<br />
Por ejemplo:<br />

**UPDATE cliente_db**<br />
**SET nomb_client = 'Lucho F.'**<br />
      **distrito = 'Villa El Salvarock'**<br />
*****************************************************************************************************************
<h2>🌱 DELETE</h2>
Es utilizada para <b>eliminar</b> registros existentes en una tabla.<br />
<br />

**DELETE FROM nombre_tabla**<br />
**WHERE Condición;**<br />
<br />
Por ejemplo:<br />

**DELETE FROM cliente_db**<br />
**WHERE nomb_client = 'Lucho F.';**<br />
*****************************************************************************************************************
<h2>🌱 INSERT INTO</h2>
Se utiliza para <b>insertar(agregar) nuevos registros</b> en una tabla. Se puede escribir la función de dos maneras:<br />
<br />

1. Especificando las columnas y valores que serán insertados<br />
**INSERT INTO nombre_tabla**<br />
**(columna 1, columna 2, columna 3,...)**<br />
**VALUES(valor 1, valor 2, valor 3,...) ;**<br />
2. No especificando las columnas que serán insertados<br />
**INSERT INTO nombre_tabla**<br />
**VALUES(valor 1, valor 2, valor 3,...) ;**<br />

Por ejemplo:<br />

**INSERT INTO cliente_db (nomb_client, nomb_contact, direcc, distrito, pais)**<br />
**VALUES('Ricardo Belmont', 'Augusto Ferrando', 'Av. Manco Capac 1260', 'La Victoria', 'Perú') ;**<br />
*****************************************************************************************************************
<h2>🌱 CREATE DATABASE</h2>
Es usada para <b>crear</b> una nueva base de datos SQL.<br />
<br />

Por ejemplo:<br />

**CREATE DATABASE comida_db**;
*****************************************************************************************************************
<h2>🌱 ALTER TABLE</h2>
Es utilizada para <b>añadir,borrar o modificar columnas</b> en una tabla existente.<br />
También es usada para añadir y borrar varias restricciones en una tabla existente.<br />
<br />

Por ejemplo:<br />

1. **ALTER TABLE** - **ADD COLUMN**<br />
**ALTER TABLE clientes**<br />
**ADD email VARCHAR (255)**<br />

2. **ALTER TABLE** - **DROP COLUMN**<br />
**ALTER TABLE clientes**<br />
**DROP COLUMN email ;**<br />

***************************************************************************************************************
<h2>🌱 CREATE TABLE</h2>

Es utilizada para <b>crear</b> una nueva tabla en una base de datos.<br />

Por ejemplo:<br />
<br />
**CREATE TABLE Personas(<br />
      person_id INT,<br />
      apellidos VARCHAR(255),<br />
      nombres VARCHAR(100),<br />
      direcc VARCHAR(255),<br />
      distr VARCHAR(100)<br />
  );**
*****************************************************************************************************************
<h2>🌱 DROP TABLE</h2>
Se utiliza para <b>borrar una tabla existente</b> en una base de datos.<br />
<br />

Por ejemplo:<br />

**DROP TABLE mascotas;**
*****************************************************************************************************************
<h2>🌱 CREATE INDEX</h2>
Se utiliza para <b>crear índices</b> en una tabla. Permite recuperar datos desde otra base de datos, de manera más rápida y eficiente.<br />
<br />

Por ejemplo:<br />

**CREATE INDEX idx_apellidos**<br />
**ON personas(apellidos_nombres);**
*****************************************************************************************************************
<h2>🌱 DROP INDEX</h2>
Se utiliza para <b>borrar índices</b> en una tabla.<br />
<br />

Por ejemplo:<br />

**ALTER TABLE edades**<br />
**DROP INDEX index_nombres;**
*****************************************************************************************************************
<h2>🌱 JOIN</h2>
Permite <b>recuperar información</b> relacionada de varias tablas.<br />
INNER JOIN, LEFT JOIN entre otros, son algunos de los tipos de JOIN, cada uno con su lógica.<br />
<br />

Por ejemplo:<br />

**SELECT clients.names,**<br />
**pedidos.fecha FROM clients**<br />
**INNER JOIN pedidos on clients.id**<br />
**= pedidos.cliente_id**<br />
*****************************************************************************************************************