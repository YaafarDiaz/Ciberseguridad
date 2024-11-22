[![Gobuster](https://www.kali.org/tools/gobuster/images/gobuster-logo.svg "Gobuster")](https://www.kali.org/tools/gobuster/images/gobuster-logo.svg "Gobuster")  
# Gobuster  
Gobuster es una herramienta de penetration testing (pruebas de penetración) utilizada principalmente para realizar reconocimiento en aplicaciones web. Su función principal es enumerar directorios y archivos ocultos en un servidor web, aunque también se puede utilizar para enumerar subdominios. Gobuster trabaja de forma eficiente utilizando un enfoque basado en fuerza bruta.  

## Comandos disponibles:

- **completion** Genera el script de autocompletado para el shell especificado.  
- **dir -u** Utiliza el modo de enumeración de directorios/archivos.  
- **dns** Utiliza el modo de enumeración de subdominios DNS.
- **fuzz** Utiliza el modo de fuzzing. Reemplaza la palabra clave FUZZ en la URL, cabeceras y cuerpo de la solicitud.
- **gcs** Utiliza el modo de enumeración de buckets de Google Cloud Storage (GCS).
- **help** Muestra ayuda sobre cualquier comando.
- **s3** Utiliza el modo de enumeración de buckets de AWS S3.
- **tftp** Utiliza el modo de enumeración TFTP.
- **version** Muestra la versión actual.
- **vhost** Utiliza el modo de enumeración de VHOST (probablemente quieras usar la dirección IP como parámetro de URL).

## Flags:

**--debug** Habilita la salida de depuración.  
**--delay** duration Tiempo que cada hilo espera entre solicitudes (por ejemplo, 1500ms).  
**-h, --help** Muestra ayuda para Gobuster.  
**--no-color** Desactiva la salida de colores.  
**--no-error** No muestra errores.  
**-z, --no-progress** No muestra el progreso.  
**-o, --output string** Archivo de salida para escribir los resultados (por defecto es stdout).  
**-p, --pattern string** Archivo que contiene patrones de reemplazo.  
**-q, --quiet** No imprime el banner ni otros ruidos.  
**-t, --threads int** Número de hilos concurrentes (por defecto 10).  
**-v, --verbose** Salida detallada (errores).  
**-w, --wordlist string** Ruta al archivo de palabras. Usa - para utilizar la entrada estándar (STDIN).  
**--wordlist-offset int** Reanuda desde una posición dada en la lista de palabras (por defecto es 0).  

## Ejemplos:

- Enumerar directorios de servidor web.  

`gobuster dir -u <objetivo> -w <diccionario>`

- Enumerar subdominios.  

`gobuster dns -d example.com -w <diccionario>`

- Enumerar URLs mediante Fuzzing

`gobuster fuzz -u <objetivo>/FUZZ -w <diccionario>`