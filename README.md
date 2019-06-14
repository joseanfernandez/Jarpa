# Jarpa

Jarpa consta de 3 proyectos:
### [Jarpa Security](https://github.com/joseanfernandez/jarpa-security)
Aplicación móvil.

[APK](https://github.com/joseanfernandez/Jarpa/raw/master/Jarpa.apk)


#### Pages y modales
Si estás autenticado:
* home: Contiene el menú tipo tabs principal que incluye list y generator.
  - settings: Modal accesible desde list y generator para modificar contraseña de acceso y datos de usuario.
* list: Lista de cuentas creadas.
  - edit: Modal accesible desde list para editar cuentas.
* generator: Crea cuentas, ya sea con contraseña generada aleatoriamente o introducidad por el usuario.
* 


Si no estás autenticado:
* login
  - register
  - forgot-password

#### Pipes
* filter: Filtro de búsqueda de cuentas en list.

#### Modelos
* account
* statistic
* user

### Servicios
* auth
  - Autenticación de Firebase: 
    * signInWithEmailAndPassword
    * signOut
    * sendPasswordResetEmail
    * updatePassword
    * createUserWithEmailAndPassword
  - Auto Sign Out
* ed
  - Encriptación
  - Desencriptación
* server
  - Peticiones http al servidor para:
    * Crear usuarios, cuentas y estadísticas.
    * Actualizar usuarios y cuentas.
    * Borrar cuentas.
    * Leer usuarios y cuentas.
* toast
  - Servicio para mostrar toast de diferentes colores con mensaje personalizado.

### [Jarpa Admin](https://github.com/joseanfernandez/jarpa-admin)
Página de administración, donde podemos ver estadísticas de usuarios y contraseñas, además de gestionar los estados de los usuarios.

[https://jarpa.joseanfernandez.com](https://jarpa.joseanfernandez.com)

### [Jarpa Engine](https://github.com/joseanfernandez/jarpa-engine)
Motor de toda la aplicación.






