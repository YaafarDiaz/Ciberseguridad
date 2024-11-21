[![LDAPSearch](https://coffeebeantech.com/wp-content/uploads/2019/06/COFFEE-BEAN-Site-Products-Icon-LDAP.png "Nmap")](https://coffeebeantech.com/wp-content/uploads/2019/06/COFFEE-BEAN-Site-Products-Icon-LDAP.png "LDAPSearch")  
# LDAPSearch 
Se utiliza para realizar consultas a un servidor LDAP (Lightweight Directory Access Protocol). LDAP es un protocolo utilizado para acceder a servicios de directorio, que son bases de datos estructuradas que almacenan información, como usuarios, grupos, y otros recursos de una red o de una infraestructura.   

## Sintaxis básica de un comando ldapsearch:  

                `ldapsearch -x -H ldap://<servidor_ldap> -b 'DC=Dominio,DC=Sub-dominio'`  

- **-x:** Usa una autenticación simple (en lugar de SASL).

- **-H:** Dirección del servidor LDAP.

- **-b:** Nombre distinguido base o (DN) sobre el cual se realiza la busqueda.
