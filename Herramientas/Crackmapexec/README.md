[![Crackmapexec](https://www.kali.org/tools/crackmapexec/images/crackmapexec-logo.svg "Crackmapexec")](https://www.kali.org/tools/crackmapexec/images/crackmapexec-logo.svg "Crackmapexec")  
# Crackmapexec (CME)
CrackMapExec o CME es una herramienta diseñada para la post-explotación, su principal característica es que permite hacer movimientos laterales dentro una red local. Pero también tiene muchas opciones de uso, ya que usa módulos y funcionalidades externas.  

## Protocolos y métodos utilizados:

### SMB (Server Message Block):  
Principalmente se comunica a través de SMB, que es utilizado para compartir archivos e impresoras en redes Windows.  
### NetSession y NetShare:  
Usados para gestionar sesiones y recursos compartidos.  

## Opciones:  

- **-smb (Server Message Block):** Protocolo utilizado para compartir archivos e impresoras en redes Windows.  
- **-RDP (Remote Desktop Protocol):** Usado para acceder de forma remota a escritorios de Windows.  
- **-WinRM (Windows Remote Management):** Protocolo usado para ejecutar comandos remotos en Windows de manera similar a SSH en sistemas Linux.  
- **-LDAP (Lightweight Directory Access Protocol):** Protocolo para acceder a directorios de red como Active Directory.  
- **-HTTP/HTTPS:** Usado para interactuar con servicios web, como servidores web o interfaces de administración remota.  
- **-DNS:** Usado para interactuar con servidores DNS.  

        `crackmapexec <protocolo> <objetivo> <opciones>`  

- **-d:** Especifica el dominio cuando estás realizando pruebas de penetración en una red Windows. 
**Ejemplo:**  
        `crackmapexec smb <objetivo> -d <dominio>`  

- **-u:** Especifica el usuario  
**Ejemplo:**  
        `crackmapexec smb <objetivo> -d <dominio> -u <usuario>`  

- **-p:** Especifica la contrasena  
**Ejemplo:**  
        `crackmapexec smb <objetivo> -d <dominio> -u <usuario> -p <contrasena>` 

- **--shares:** se utiliza para enumerar los recursos compartidos (shares) en una máquina remota que tiene el protocolo SMB (Server Message Block) habilitado.  
**Ejemplo:**  
        `crackmapexec smb <objetivo> -d <dominio> -u <usuario> -p <contrasena> --shares` 

- **--users:** se utiliza para enumerar los usuarios en una máquina remota dentro de una red que tiene habilitado el protocolo SMB (Server Message Block).  
**Ejemplo:**  
        `crackmapexec smb <objetivo> -d <dominio> -u <usuario> -p <contrasena> --users`  

- **-rid-brute:** se utiliza para realizar un ataque de fuerza bruta con el objetivo de descifrar la clave de cifrado utilizada por el archivo de hibernación de Windows (hiberfil.sys) o la clave de arranque de Windows (BootKey).  
**Ejemplo:**  
        `crackmapexec smb <objetivo> -d <dominio> -u <usuario> -p <contrasena> --rid-brute` 