# Prácticas para aprender git

1. Abrir una terminal integrada de Git (desde la carpeta del proyecto)
2. Tipear git init
3. En la terminal podemos tipear ls (para listar) y -la(para mostrar los archivos ocultos en la terminal)
4. la "U" en los archivos significa "untracked" o no rastreados, no están sincronizados.
5. Si tipeamos en alguno de esos archivos "git add nombre-de-archivo", la "U" cambia por "A". Si aparece una "M", significa "modificado", o "modifier"
6. Con "git add .", todos los archivos del directorio pasan a la condición "A".
7. Con "git commit -m "" " agregamos un comentario
8. Con "git push -u origin master", empujamos la rama master
9. Al tipear "pwd" me muestra el directorio donde estoy ubicado
10. Para crearse una carpeta donde guardar las claves públicas y privadas, nos trasladamos a la carpeta ".ssh" (si no existe, la creamos con "mkdir .ssh"), una vez allí pegamos 'ssh-keygen -t ed25519 -C "your_email@example.com"', con lo que procederemos a crear la clave (se siguen los pasos).
11. Con el comando "cat nombre de archivo" abrimos un archivo (lo usaremos para abrir la el archivo de la llave pública).
12. Debemos copiar la dirección SSH del repositorio en git para establecer la conexión. El comando para establecer la conexión sería: 'git remote add origin git@github.com:gabrielbaute/taller-de-git.git' (con esta última dirección para nuestro caso). De esta forma vinculamos el repositorio en github con el repositorio en la PC.
13. Así, podemos ejecutar el comando indicado en (8).
14. Con 'git remote -v' se visualizan los repositorios vinculados, y con "git remote rm" y agregando la categoria (como origin) se borran los accesos a esos repositorios y se puede volver a crear uno nuevo.
15. Para clonar un proyecto, se emplea el comando 'git clone dirección-ssh', con lo que lograríamos tener una copia (desde la terminal) en la carpeta que hemos escogido para ella.
16. Para crear una rama, una vez clonado el proyecto, se tipea 'git checkout -b nomre-de-la-rama', lo que hara switch hacia la nueva rama.
17. Con 'git checkout nombre-de-la-rama', nos desplazaremos hacia la rama especificada.
18. git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
(formato para la presentación del log, usar siempre este código)
19. git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
(creación de un alias para el código ubicado en el punto 18, de esta forma se usa solo el comando 'git lg', en vez de 'git log', y muestra el log contenido en el punto 18)
20. Para salir de la terminal cuando consultamos el log del proyecto, presionamos la tecla 'q'.
21. Cuando se realiza un cambio en el repositorio (con git push), se procura hacer en la rama en que se está trabajando y no en la rama master (que habitualmente se bloquea), por lo que el comando en este caso para subir modificaciones sería 'git push -u origin nombre-de-la-rama'.