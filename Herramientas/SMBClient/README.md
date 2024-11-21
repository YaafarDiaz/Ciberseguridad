 # SMBClient (Cliente Samba)
herramienta de línea de comandos utilizada para acceder a recursos compartidos en redes locales utilizando el protocolo SMB (Server Message Block). Este protocolo es ampliamente utilizado para compartir archivos, impresoras y otros recursos en redes Windows, aunque también es compatible con otros sistemas operativos como Linux y macOS.  

## Funciones principales:

### Acceso a recursos compartidos:  
Permite acceder a carpetas y archivos en servidores que utilicen SMB para compartir sus recursos, como en sistemas Windows o servidores Linux que usan Samba.  

### Transferencia de archivos:  
Puede utilizarse para copiar archivos hacia y desde un recurso compartido, usando comandos similares a los de FTP, como get, put, mget, mput, entre otros.  

### Exploración de recursos:  
Permite listar los recursos compartidos en un servidor remoto con el comando -L, lo cual muestra todas las carpetas y recursos disponibles.  

### Interacción con servidores Windows:  
Permite ejecutar comandos de administración y transferencia de archivos en entornos Windows.  


## Opciones:

- **-U:** Especifica el usuario.  

        smbclient -U <usuario> <objetivo>  

- **-L:** Lista los recursos compartidos en el servidor.  

        smbclient -U <usuario> -L <objetivo>  