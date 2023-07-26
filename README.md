# SQL: Primeros pasos👨‍💻💊

![wallpaper](images/mysql.jpg)

<br />

<h1>💊¿Qué es SQL? 💊</h1>

<b>**SQL**</b> es el Lenguaje Estructuado de Consultas. Es usado para almacenar y administrar datos a través de un sistema de bases de datos relacionales (**RDBMS**).<br />
<br />

<h1>💊 Comandos 💊</h1>

🌱 **SELECT**<br />
Extrae información desde una base de datos. La data resultante es almacenada en una tabla de resultados llamada Conjunto de resultados (result - set).<br />
<br />
**SELECT Columna 1, Columna 2,...**<br />
**FROM nombre_tabla**<br />
<br />
Columna 1 y Columna 2 son los nombres de los campos de la tabla desde donde quieres seleccionar los datos. Si deseas seleccionar todos los campos disponibles en la tabla, utiiza la siguiente sintaxis.<br />
<br />
**SELECT * FROM nombre_tabla**
*********************************************************************************************************************
🌱 **UPDATE**<br />
Utilizado para modificar registros existentes en una tabla.<br />
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
*********************************************************************************************************************
🌱 **DELETE**<br />
La función **DELETE** es utilizada para eliminar registros existentes en una tabla.<br />
<br />
**DELETE FROM nombre_tabla**<br />
**WHERE Condición;**<br />
<br />
Por ejemplo:<br />

**DELETE FROM cliente_db**<br />
**WHERE nomb_client = 'Lucho F.';**<br />
*********************************************************************************************************************
🌱 **INSERT INTO**<br />
**INSERT INTO** es una función que se utiliza para insertar(agregar) **nuevos registros** en una tabla. Se puede escribir la función INSERT INTO de dos maneras:<br />
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
*********************************************************************************************************************
🌱 **CREATE DATABASE**<br />
La función CREATE DATABASE es usada para crear una nueva base de datos SQL.**<br />

Por ejemplo:<br />

**CREATE DATABASE comida_db**;
*********************************************************************************************************************
🌱 **ALTER TABLE**<br />
La función ALTER TABLE es utilizada para añadir, borrar o modificar columnas en una tabla existente.<br />
También es usada para añadir y borrar varias restricciones en una tabla existente.<br />

Por ejemplo:<br />

1. **ALTER TABLE** - **ADD COLUMN**<br />
**ALTER TABLE clientes**<br />
**ADD email VARCHAR (255)**<br />

2. **ALTER TABLE** - **DROP COLUMN**<br />
**ALTER TABLE clientes**<br />
**DROP COLUMN email ;**<br />