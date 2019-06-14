# Jarpa

Jarpa consta de 3 proyectos:
### [Jarpa Security](https://github.com/joseanfernandez/jarpa-security) 
Aplicación móvil que nos permite tener todas nuestras contraseñas seguras bajo una única contraseña.
Con un solo click podrás copiar la contraseña al portapapeles sin necesidad de ver esa contraseña.

[APK](https://github.com/joseanfernandez/Jarpa/raw/master/Jarpa.apk)

### Estructura
#### Pages y modales
Si estás autenticado:
* home: Contiene el menú tipo tabs principal que incluye list y generator.
  - settings: Modal accesible desde list y generator para modificar contraseña de acceso y datos de usuario.
* list: Lista de cuentas creadas.
  - edit: Modal accesible desde list para editar cuentas.
* generator: Crea cuentas, ya sea con contraseña generada aleatoriamente o introducidad por el usuario.


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


### Estructura
#### Charts
* area:  Contraseñas aleatorias vs propias de usuario por semana.
* gauge: Total de usuarios en la aplicación (Frente a objetivo marcado).
* line: Cantidad de usuarios registrados por semana.
* pie: Total de contraseñas aleatorias vs propias de usuario.
#### Componentes
Si estás autenticado:
* navbar: Presente en toda la aplicación.
* dashboard: Contiene las cuatro gráficas: area, gauge, line y pie.
* users: Tabla de usuarios con su datos y estado.

Si no estás autenticado:
* login

#### Guards
* auth: Guard para securizar las rutas.

### Servicios
* auth
  - Autenticación de Firebase: 
    * signInWithEmailAndPassword
    * signOut
* info
  - Servicio para mostrar snackbar de diferentes colores con mensaje personalizado.
* server
  - Peticiones http al servidor para:
    * Actualizar usuarios.
    * Leer usuarios y estadísticas.

[https://jarpa.joseanfernandez.com](https://jarpa.joseanfernandez.com)

### [Jarpa Engine](https://github.com/joseanfernandez/jarpa-engine)
Motor de toda la aplicación.


### Estructura
#### Componentes
Cada componente tiene su propio router y funciones.
* accounts
* statistics
* user

#### Modelos
* accounts
* statistics
* user

### Translate
Traductor para mandar al front el contenido de las gráficas traducidos.



