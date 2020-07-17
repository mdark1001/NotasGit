# Notas de GIT (Guía Rápida)

**Nota:** Recuerda tener instalado git

```bash
$ sudo apt install git-all
```



### Comandos de Git

- |                      Comando                       | Descripción                                                  | Opciones                                                     |
  | :------------------------------------------------: | ------------------------------------------------------------ | ------------------------------------------------------------ |
  |                   `$ git init `                    | Iniciar un repositorio de git, se crea internamente la carpeta **.git/** |                                                              |
  |                    `$ git add`                     | Agregar archivos  locales y hacer **track** de los archivos, y lo mandamos a **Staging** | Podemos  agregar un archivo en paricular indicando por nombre del archivo o un **.** (punto) agrega todos los archivos |
  | `$ git commit -m "Mensaje descriptivo del commit"` | Confirma los archivos  una vez agregados (`git add`) y lo mandamos al repositorio **Local. ** |                                                              |
  |                   `$ git status`                   | Revisa el estatus del repositorio, idica si existen cambios sin confirmar, archivos sin tack |                                                              |
  |                    `$ git log`                     | Muestra el historial de cambios del repositorio o de un archivos<br />Por ejemplo `$ git log file.txt` |                                                              |
  |        `$ git diff ID_COMMIT_1 ID_COMMIT_2`        | Muestra las diferencias entre dos commits a partir de la clave generada.<br />Ejemplo: `$ git diff 31c549e32f585b8c9ef1f67496a7522bf8d4b30f 011a7c55eb1aae26002f2c74a1fdba703c0c1e55 ` |                                                              |
  |                    `$ git rm `                     | Elimina un archivo del arbol de directorios                  |                                                              |
  |                `$ git rm --cached`                 | Elimina los archivos del área de *Staging*, lo mantiene en disco local |                                                              |
  |                 `$ git rm --force`                 | Elimina los archivos de Git y del disco<br />**Nota: Es posible recuperarlo, se mantiene en el historial de cambios** |                                                              |
  |                   `$ git reset`                    | Permite *viajar en el tiempo, sin la opción de regresar*  <br /> | Este comando es **muy peligroso** y debemos usarlo solo en caso de emergencia. Recuerda que debemos usar alguna de estas dos opciones: <br />`$ git reset --soft`<br />`$ git reset --hard ` |


### Comando Git con repositorio remoto

------

Clonar un repositorio 

```bash
$ git clone **url_del_repositorio**
```

Descargar cambios del repositorio,  de *master*

```bash
$ git pull  origin master
```

Subir cambios locales a *master*

```bash
 $ git push -u origin master
```

Agregar un origen remoto 

```bash
$ git remote add origin **url_del_repositorio**
```

Ver los origenes del reposiotorio 

```bash
$ git remote -v 
```



### Uso de ramas en git 

------

Crear una rama a partir de master:

```bash
$ git branch  otra_rama
```

Cambiar a otra  rama 

```bash
$ git checkout -b otra_rama
```

Uniendo ramas 

```bash
# Crear un nuevo commit en la rama master combinando
# los cambios de la rama otra_rama:
$ git checkout master
$ git merge otra_rama

# Crear un nuevo commit en la rama otra_rama combinando
# los cambios de cualquier otra_rama_2:
$ git checkout otra_rama
$ git merge otra_rama_2
```



### Utilidades

------

Mostrar el log en forma gráfica.

```bash
$ git log --all --graph --decorate --oneline
```

Crear un **Tag**

```bash
$ git tag -a v0.1 -m "Mensaje descriptivo de la versión"
# Enviar a github
$ git push origin --tags
```

Ver el listado de tags

```bash
$ git show-ref --tags
```

Eliminar un tag

```bash
$ git tag -d NOMBRE_TAG 
# Eliminar en github
$ git push origin :refs/tags/NOMBRE_TAG
```

Crear un **alias** para un comando en git

```bash
$ git  config --global alias.$NOMBRE_ALIAS "COMANDO QUE SE EJECUTA"
# POR EJEMPLO, saber el total de commits por usuario sin contar los merges 
$ git config --global alias.stats "shortlog -sn --no-merges"
# Después ejecutar como:
$ git stats
 
```



Consultar información desde la terminal

```bash
$ git $COMANDO --help 
```

