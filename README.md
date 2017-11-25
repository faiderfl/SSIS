Microsoft SQL Server Integration Services: ETL, Data migration.

Guia:

ETL básica de homicidios:

1- Descargar la base de datos de homicidios de la siguiente ruta:
https://drive.google.com/drive/folders/0Byq3EWPvHOPpS3l6aTdvMEpHbUE

O la encontrada en este repositorio en el archivo de nombre: Homicidios 2003-2016 24112016
Y copiarlo en una ruta que sea de facil acceso.

2. Clonar el repositorio con la solucion HomicidiosInicial y probar en Visual Studio 2015.

3. Crear un base de datos con el nombre que se desee, en el caso de este ejercicio se usó como nombre Homicidios.

4. Ejecutar el proyecto de Homicidios y verificar que los datos se hayan migrado correctamente del archivo de Excel hasta la tabla de Homicidos en la base de datos. 


Esta parte tendrá un origen en excel, una transformación de ordenamiento y un destino en SQL Server.

-----------------------------------------------------------------
Evitar datos duplicados:

5.Generar una transformación de multicast para los demas procesos.
6. Utilizar un lookup y un conversor de datos para evitar datos duplicados en la BD.

Homicidios por Genero:
7. Utilizar un conditional split por año con las sentencias:
    
    2003-2010:  [Año] >= 2003 && [Año] <= 2010
    2010-2016:  [Año] > 2010
   
Homicidios por Años:
 8. Utilizar un conditional split por año con las sentencias:
 
   SexoM: Sexo == "HOMBRE"
   SexoF: Sexo == "MUJER"

Creación de Jobs: 
9. Importar archivo al servidor de SSIS
10.Crear Job con el package.

