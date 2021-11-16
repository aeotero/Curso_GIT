# Curso_Python
Hice este pequeño readme para que puedan probar el clonar repositorios.

Tambien, ya que estamos, tener un mache de los comandos de git.

De la nube a Wollok (para un repositorio nuevo)

# 1. Ubicarse en la carpeta en la que se va a trabajar
Una vez ubicado en esa carpeta, abrir una ventana de terminal (o consola).
Todos los comandos de git se hacen desde la consola.

# 2. Ingresar a GitHub
Ir a la página de GitHub (https://github.com) y hacer "Sign in".

# 3. Encontrar el repositorio a descargar
Ir a la página de Programación con Objetos 1, 
sección Cursada (https://obj1-unahur.github.io/Cursada)

# 4. Descargar el repositorio
git clone https://github.com/wollok/multipepita.git
cd multipepita 

# 5. Configurar el usuario
git config user.name "Juana Pérez"
git config user.email "jperex@wollok.org"

# 6. Importar el proyecto a Wollok
Archivo -> Open Project from File System

De Wollok a la nube

# 1. Registrar los cambios
git add .
git commit -m "Agregados métodos volar y comer a Pepita"

# 2. Subir los cambios al servidor
git push origin master

De la nube a Wollok (para un repositorio existente)

# 1. Ubicarse en la carpeta en la carpeta del proyecto.
Una vez ubicado en esa carpeta, abrir una ventana de terminal (o consola).
Todos los comandos de git se hacen desde la consola.

# 2. Descargar los cambios de GitHub.
git pull origin master

# 3. Si hay conflictos, resolverlos y después commitear. 
# En este caso no se usa la opción `-m` para el commit, 
# porque Git ya escribe el mensaje.
git add .
git commit

# 4. Subir los cambios.
git push origin master

Explicación detallada
De la nube a Wollok - paso a paso
1. Ingresar a GitHub

Lo primero que debemos hacer es ingresar a GitHub con el usuario y contraseña que tengamos registrado.
2. Encontrar el repositorio a descargar

A continuación abrimos la página de nuestra materia y nos dirigimos a la solapa Cursada en donde encontraremos los ejercicios semanales que nos permitirán acceder a la URL que vamos a descargar.

Presionado en el link Clonar el Ejercicio que corresponda, nos dirige a la página del repositorio que queremos descargar.
3. Descargar el repositorio

Dentro del repositorio debemos copiar el link que aparece arriba a la derecha:

Una vez obtenido ese link, abriremos una consola y utilizaremos el comando git clone para bajar el repositorio a nuestra compu. Por ejemplo, para bajar este repositorio haríamos lo siguiente:

git clone https://github.com/wollok/multipepita.git

Finalizado este comando, tendremos el repositorio completo en una carpeta con su nombre, en este caso multipepita. Todos los pasos que siguen asumen que estás dentro de la carpeta nueva, eso en este caso se logra ejecutando:

cd multipepita

4. Configurar el usuario

Git es un sistema de control de versiones, y está pensado para que varias personas contribuyan al mismo repositorio. Por esto, cada cambio que se registra está asociado a un usuario y antes de comenzar a trabajar debemos "decirle a Git quiénes somos".

Esto se puede hacer por cada repositorio (recomendado para computadoras compartidas) o para todo el sistema (más cómodo si trabajamos con compu propia). En esta guía elegimos hacerlo de la primera forma porque es como vamos a trabajar en el aula:

git config user.name "Juana Pérez"
git config user.email "jperex@wollok.org"

Es importante que el mail coincida con el que tenés registrado en GitHub, porque eso será lo que la plataforma utilizará para relacionar tus commits con tu usuario.

Si quisieras configurarlo de manera global, basta con agregar el flag --global a los comandos anteriores:

git config --global user.name "Juana Pérez"
git config --global user.email "jperex@wollok.org"

5. Importar el proyecto a Wollok

Para comenzar a trabajar en nuestro código debemos importar el proyecto descargado. Para logar esto, primero abrimos Wollok, vamos al menú Archivo y luego al sub-menu Open Project from File System. Y en el cuadro de dialogo que se abre debemos selecionar la carpeta que hemos descargado. En nuestro ejemplo, la carpeta es multipepita.

Ya tenemos nuestro proyecto listo para comenzar a trabajar en nuestro código.
De Wollok a la nube - paso a paso
1. Registrar los cambios

Cada vez que "termines algo" (un método, una funcionalidad, un test, etc), es buena idea registrar esos cambios, haciendo lo que en git se denomina commit. Un commit es básicamente una serie de cambios acompañado por un mensaje que explica qué fue lo que se hizo, podríamos pensarlo como una pequeña versión de nuestro programa.

Algunos ejemplos de mensajes de commit:

    Terminada vista de estudiantes.
    Creado modelo de artistas.
    Corregido error al guardar una nueva yerba.

Para hacer un commit, hay que indicarle a git qué cambios vamos a incluir y luego hacer el commit, especificando el mensaje. Esto se logra con los siguientes comandos:

git add .
git commit -m "Agregados métodos volar y comer a Pepita"

Con eso, los cambios quedarán registrados (aún dentro de nuestra compu) y el repositorio listo para seguir trabajando.
2. Subir los cambios al servidor

De vez en cuando (típicamente antes de irte o de dejar de trabajar) tenés que subir tus commits al servidor. Esto tiene dos objetivos: por un lado, tener un respaldo de tu trabajo y por otro ponerlo a disposición para que las personas que trabajan con vos puedan verlo.

Esto se consigue con un comando es muy sencillo, que sube todos los commits nuevos al servidor:

git push origin master

A continuación, te pedirá que ingreses tu usuario y luego tu password (ojo, que el password no aparece mientras lo escribís). Si pusiste todo bien, deberías ver algo como esto:

Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 460 bytes | 0 bytes/s, done.
Total 3 (delta 2), reused 0 (delta 0)
To git@github.com:wollok/multipepita.git
   c037f15..8d218e2  master -> master


