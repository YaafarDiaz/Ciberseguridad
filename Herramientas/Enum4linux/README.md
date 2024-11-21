 # Enum4Linux (enumeración protocolo SMB)
Herramienta de código abierto que se utiliza principalmente para realizar enumeración (recopilación de información) sobre sistemas que ejecutan el protocolo SMB (Server Message Block), típicamente sistemas Windows o servidores Linux que utilizan Samba.   

## Opciones:
- **-U:**  obtener lista de usuarios
- **-M:**  obtener lista de máquinas*
- **-S:**  obtener lista de recursos compartidos
- **-P:**  obtener información de política de contraseñas
- **-G:**  obtener lista de miembros y grupos
- **-d:**  ser detallado, se aplica a -U y -S
- **-u:**  user especificar nombre de usuario a utilizar (predeterminado "")
- **-p:**  pass especificar contraseña a utilizar (predeterminado "")
- **-a:** Realizar todas las enumeraciones simples (-U -S -G -P -r -o -n -i).
- **-r:** Enumera usuarios mediante ciclos de RID
- **-R:** range Rangos de RID a enumerar (predeterminado: 500-550,1000-1050, implica -r)
- **-K:** n Sigue buscando RID hasta que n RID consecutivos no correspondan a
- **-s:** Adivinación por fuerza bruta de archivos para nombres de recursos compartidos
- **-k:** user Usuario(s) que existen en el sistema remoto (predeterminado: administrador, invitado, krbtgt, administradores de dominio, raíz, bin, ninguno)
- **-o:** Obtener información del sistema operativo
- **-i:** Obtener información de la impresora
- **-w:** wrkg Especificar el grupo de trabajo manualmente (normalmente se encuentra automáticamente)
- **-n:** Realizar un nmblookup (similar a nbtstat)
- **-v:** Verbose. Muestra todos los comandos que se están ejecutando (net, rpcclient, etc.)
- **-A:** Agresivo. Escribir comprobaciones en recursos compartidos, etc.


## Ejemplo:

        enum4linux -a -u <usuario> -p <contrasena> <objetico> 