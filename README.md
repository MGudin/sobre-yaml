# sobre-yaml

La idea es crear un script que lea un archivo en formato csv y los transforme
a yaml y json.

El formato del archivo csv es:
provincia;ciudad;escuela;nivel

Se debe crear un script que cree un archivo csv de ejemplo con el formato mencionado.

## Generador

El script que genera el archivo se es [csv\_generator](./csv_generator).

El script recibe dos argumentos:

| short | long | descripcion |
| --- | --- | --- |
| -l LINES | --lines LINES | Cantidad de lineas a generar.(por defecto 5) |
| -o OUTPUT | --output OUTPUT | Nombre del archivo a generar. Si no se recibe se imprime en pantalla |
| -h | --help | Muestra mensaje de ayuda |

## Parseador

El script que parsea el archivo .csv y genera yaml|json es [csv\_converter](./csv_converter).

El script recibe dos argumentos:

| short | long | descripcion |
| --- | --- | --- |
|     |  | POSICIONAL(json o yaml).  Si no se recibe imprime por defecto json |
| -i INPUT  | --input INPUT | nombre de archivo para leer |
| -h  | --help | Muestra mensaje de ayuda |

Internamente crea un diccionario con las lineas leidas y dicho diccionario es pasado a una funcion
parseadora segun se reciba json o yaml como parametro.

