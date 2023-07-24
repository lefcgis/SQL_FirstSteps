# SQL: Primeros pasos👨‍💻💊

![wallpaper](images/mysql.jpg)

<br />
<br />

<h1>💊¿Qué es SQL? 💊</h1>

<b>**SQL**</b> es el Lenguaje Estructuado de Consultas. Es usado para almacenar y administrar datos a través de un sistema de bases de datos relacionales (**RDBMS**)


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
**SET Columna 1= Valor1,**<br />
      Columna 2= Valor2,...<br />
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