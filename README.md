## Preliminares
Para realizar las prácticas debes tener instalado en el equipo o servidor de pruebas:
  - Docker
  - Python

#### Instalación de Ansible

        pip install ansible

### Construcción de la imagen personalizada
Ingresa a la carpeta 'Dockerfile' y sigue los pasos indicados.

### Documentacion de lo que se hizo en la migracion


Estos playbooks requieren Ansible 1.2.
Estos playbooks están destinados a ser una guía de referencia y de inicio para la construcción
playbooks de ejercicios Ansible. Estos manuales fueron probados en CentOS 6.x por lo que recomendamos
que utilice CentOS o RHEL para probar estos módulos.

Esta stack LAMP puede estar en un solo nodo o en varios nodos. El archivo de inventario
'hosts' define los nodos en los que se deben configurar las stack.

        [webservers]
        localhost

        [dbservers]
        bensible

Aquí el servidor web sería configurado en el host local y el dbserver en un servidor llamado "bensible". La stack  se puede implementar mediante el siguiente comando:

        ansible-playbook -i hosts site.yml

Una vez hecho esto, puede comprobar los resultados consultando http://localhost/index.php.
Debería ver una página de prueba simple y una lista de bases de datos
servidor de base de datos.
