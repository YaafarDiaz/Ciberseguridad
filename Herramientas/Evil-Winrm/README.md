[![Evil-winrm](https://www.kali.org/tools/evil-winrm/images/evil-winrm-logo.svg "Evil-winrm")](https://www.kali.org/tools/evil-winrm/images/evil-winrm-logo.svg "Evil-winrm")  
# Evil-Winrm  
La herramienta evil-winrm es un script de PowerShell que se utiliza para realizar ataques de Remote Windows Management (WMF) a sistemas Windows a través de la implementación de la funcionalidad Windows Remote Management (WinRM). WinRM es un servicio que permite a los administradores de sistemas gestionar de manera remota las máquinas Windows.  

## Opciones:

- **-S, --ssl:** Habilitar SSL
- **-c, --pub-key:** PUBLIC_KEY_PATH Ruta local al certificado de clave pública
- **-k, --priv-key:** PRIVATE_KEY_PATH Ruta local al certificado de clave privada
- **-r, --realm DOMINIO:** Autenticación Kerberos, también debe configurarse en el archivo /etc/krb5.conf usando este formato -> CONTOSO.COM = { kdc = fooserver.contoso.com }
- **-s, --scripts PS_SCRIPTS_PATH:** Ruta local de scripts de PowerShell
- **--spn SPN_PREFIX:** Prefijo SPN para autenticación Kerberos (HTTP predeterminado)
- **-e, --executables EXES_PATH:** Ruta local de ejecutables de C#
- **-i, --ip IP:** Nombre o dirección IP del host remoto. FQDN para autenticación Kerberos (obligatorio)
- **-U, --url URL:** Punto final de URL remoto (predeterminado /wsman)
- **-u, --user USER:** Nombre de usuario (obligatorio si no se utiliza Kerberos)
- **-p, --password PASS:** Contraseña
- **-H, --hash HASH:** NTHash
- **-P, --port PORT:** Puerto de host remoto (predeterminado 5985)
- **-V, --version:** Mostrar versión
- **-n, --no-colors:** Deshabilitar colores
- **-N, --no-rpath:** Deshabilitar la finalización de ruta remota
- **-l, --log:** Registrar la sesión WinRM

## Ejemplo:

        evil-winrm -u <usuario> -p <contrasena> -i <objetivo> 
