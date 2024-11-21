# Nmap (Network Mapper)  
Herramienta de código abierto utilizada para la exploración y auditoría de redes. Fue diseñada para descubrir hosts y servicios en una red, así como para realizar anál>

## Opciones:

- **-p: ** Se utiliza para especificar los puertos que se desean escanear.  
**Ejemplo:**  
                `nmap -p 80,443,22 <objetivo>`  
                `nmap -p- <objetivo> (Escanea todos los puertos disponibles '65 535')`  

- **-sS:** Envía paquetes SYN al destino para verificar si el puerto está abierto, pero no completa la conexión TCP. Es conocido como un "Escaneo sigiloso" porque no establece una conexion completa.  
**Ejemplo:**  
                `nmap -sS <objetivo>`  

- **--open :** se utiliza para filtrar y mostrar solo los puertos que están abiertos en el objetivo, es decir, aquellos puertos en los que se ha detectado actividad.  
**Ejemplo:**  
                `nmap --open <objetivo>`  

- **--min-rate :** Es útil cuando se quiere acelerar un escaneo, forzando a Nmap a enviar paquetes a una tasa más alta.  
**Ejemplo:**  
                `nmap --min-rate <cantidad> <objetivo>`  

- **-vvv :** Es el nivel más alto de verbosidad. Muestra información muy detallada sobre cada paso del escaneo, como la configuración de las opciones, los paquetes que se están enviando y recibiendo, los puertos escaneados, y otras estadísticas internas del proceso.  
**Ejemplo:**  
                `nmap -vvv <objetivo>`  

- **-Pn :** Se utiliza para desactivar el descubrimiento de hosts antes de realizar el escaneo de puertos.  Normalmente, Nmap intenta realizar una determinación de si el host está activo (es decir, si responde a un ping o alguna otra forma de verificación) antes de proceder con el escaneo de puertos. Esto ayuda a evitar escanear máquinas que están apagadas o inaccesibles, lo que ahorra tiempo y recursos.  
**Ejemplo:**  
                `nmap -Pn <objetivo>`  

- **-oG :** Se utiliza para guardar los resultados de un escaneo en un formato "grepable" (que se puede procesar fácilmente con herramientas como grep, awk o sed en la línea de comandos).  
**Ejemplo:**  
                `nmap -oG <nombre_archivo> <objetivo>`  

- **-sC :** Ejecuta un conjunto de scripts de detección predefinidos, conocidos como los Nmap Scripting Engine (NSE). Esta opción activa una serie de scripts que Nmap ejecuta automáticamente durante el escaneo, lo que permite realizar tareas avanzadas de detección, como la identificación de servicios, la detección de vulnerabilidades, la recopilación de información adicional y más.  
**Ejemplo:**  
                `nmap -sC <objetivo>`  

- **-sV :** Realiza un escaneo de versiones de servicios. Con esta opción, Nmap intenta identificar las versiones exactas de los servicios que están escuchando en los puertos abiertos de un host o red.  
**Ejemplo:**  
                `nmap -sV <objetivo>`  

- **-oN :** Guarda los resultados de un escaneo en un archivo de salida en formato normal (legible por humanos). Este formato es el formato predeterminado de Nmap, es decir, el mismo que verías si no redirigieras la salida a un archivo.  
**Ejemplo:**  
                `nmap -oN <nombre_archivo> <objetivo>`  
