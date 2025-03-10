


Readme E13hash
E13hash.py
Descripción
E13hash.py es un script en Python diseñado para crear una línea base de integridad del sistema de archivos utilizando PowerShell. Genera un conjunto de hashes de los archivos en una carpeta específica y los almacena en un archivo binario para su posterior análisis.

Características
Validación de rutas: Verifica si la ruta ingresada existe y es accesible.

Obtención de hashes: Ejecuta HashAcquire.ps1 en PowerShell para calcular los hashes de los archivos.

Almacenamiento estructurado: Guarda los hashes en un diccionario y los serializa en un archivo con pickle.

Configuración flexible: Utiliza un archivo config.txt para definir las rutas de entrada y salida.

Requisitos
Python 3.x

PowerShell habilitado en el sistema

Archivo config.txt con los siguientes parámetros en la sección [ARGUMENTS]:

[ARGUMENTS]
baseline = ruta/del/archivo_de_salida.pkl
Path = ruta/de/la/carpeta_a_analizar
tmp = ruta/del/archivo_temporal.txt
Script HashAcquire.ps1 en la misma ubicación del script Python.

Instrucciones de uso
Asegúrate de tener instalado Python 3.x y PowerShell habilitado.

Crea y configura el archivo config.txt con las rutas necesarias.

Abre una terminal o consola de comandos.

Ejecuta el script con:

python E13hash.py
El script generará una línea base de integridad y la guardará en el archivo definido en baseline.

Notas adicionales
Si el archivo config.txt no está correctamente configurado, el script no podrá ejecutarse.

Para verificar la integridad del sistema en el futuro, puedes comparar los hashes generados con una nueva ejecución del script.

Asegúrate de que HashAcquire.ps1 esté en la misma carpeta o proporciona su ruta absoluta en el código si es necesario.

