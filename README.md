# SQL_training
Ejercicios bases de datos
Para la entrega de la tarea únicamente se solicitará las consultas necesarias para realizar los ejercicios solicitados. No obstante, se recomiendo realizar las 
consultas directamente sobre nuestra cuenta de Snowflake para poder comprobar los resultados.
Nota: Es posible que tu cuenta de Snowflake haya quedado inactiva, si esto hubiera ocurrido pedes crear una nueva cuenta de prueba con un email diferente al que 
usaste para crearla primera cuenta.

Ejercicio 1
A continuación, vamos a realizar las siguientes consultas y para ello vamos a necesitar los archivos incluidos en el comprimido operaciones_ucm.zip disponibles 
en la plataforma del máster:
- Crear una base de datos con el nombre tarea_ucm.
- Crear un esquema de base de datos con el nombre operaciones_ucm.
- Creamos las tres tablas correspondientes a los 3 archivos: orders, refunds y merchants.
Recuerda seleccionar el tipo de dato más adecuado para cada uno de los campos de las tres tablas.
- Opcional: Si estamos realizando los ejercicios sobre Snowflake, rellenamos las tablas a partir de los datos incluidos en los archivos *.csv.

Ejercicio 2
A partir de las tablas incluidas en la base de datos tarea_ucm, vamos a realizar las siguientes consultas:
1. Realizamos una consulta donde obtengamos por país y estado de operación, el total de operaciones y su importe promedio. La consulta debe cumplir las
siguientes condiciones:
a. Operaciones posteriores al 01-07-2015.
b. Operaciones realizadas en Francia, Portugal y España.
c. Operaciones con un valor mayor de 100 € y menor de 1500€. Ordenamos los resultados por el promedio del importe de manera descendente.
2. Realizamos una consulta donde obtengamos los 3 países con el mayor número de operaciones, el total de operaciones, la operación con un valor máximo y la
operación con el valor mínimo para cada país. La consulta debe cumplir las siguientes condiciones:
a. Excluimos aquellas operaciones con el estado “Delinquent” y “Cancelled”.
b. Operaciones con un valor mayor de 100 €.

Ejercicio 3
A partir de las tablas incluidas en la base de datos tarea_ucm vamos a realizar las siguientes consultas:
1. Realizamos una consulta donde obtengamos, por país y comercio, el total de operaciones, su valor promedio y el total de devoluciones. La consulta debe cumplir
las siguientes condiciones:
a. Se debe mostrar el nombre y el id del comercio.
b. Comercios con más de 10 ventas.
c. Comercios de Marruecos, Italia, España y Portugal.
d. Creamos un campo que identifique si el comercio acepta o no devoluciones. Si no acepta (total de devoluciones es igual a cero) el campo debe contener el valor
“No” y si sí lo acepta (total de devoluciones es mayor que cero) el campo debe contener el valor “Sí”. Llamaremos al campo “acepta_devoluciones”. Ordenamos los
resultados por el total de operaciones de manera ascendente.
3. Realizamos una consulta donde vamos a traer todos los campos de las tablas operaciones y comercios. De la tabla devoluciones vamos a traer el conteo de devoluciones
por operación y la suma del valor de las devoluciones. Una vez tengamos la consulta anterior, creamos una vista con el nombre orders_view dentro del esquema tarea_ucm
con esta consulta. 
Nota: La tabla refunds contiene más de una devolución por operación por lo que para hacer el cruce es muy importante que agrupemos las devoluciones
