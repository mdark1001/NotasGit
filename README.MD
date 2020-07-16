# Notas de GIT (Guía Rápida)

**Nota:** Recuerda tener instalado git

`$ sudo apt install git-all `

### Comandos de Git

|                      Comando                       | Descripción                                                  | Opciones                                                     |
| :------------------------------------------------: | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                   `$ git init `                    | Iniciar un repositorio de git, se crea internamente la carpeta **.git/** |                                                              |
|                    `$ git add`                     | Agregar archivos  locales y hacer **track** de los archivos, y lo mandamos a **Staggin** | Podemos  agregar un archivo en paricular indicando por nombre del archivo o un **.** (punto) agrega todos los archivos |
| `$ git commit -m "Mensaje descriptivo del commit"` | Confirma los archivos  una vez agregados (`git add`) y lo mandamos al repositorio **Local. ** |                                                              |
|                   `$ git status`                   | Revisa el estatus del repositorio, idica si existen cambios sin confirmar, archivos sin tack |                                                              |
|                    `$ git log`                     | Muestra el historial de cambios del repositorio o de un archivos<br />Por ejemplo `$ git log file.txt` |                                                              |
|        `$ git diff ID_COMMIT_1 ID_COMMIT_2`        | Muestra las diferencias entre dos commits a partir de la clave generada.<br />Ejemplo: `$ git diff 31c549e32f585b8c9ef1f67496a7522bf8d4b30f 011a7c55eb1aae26002f2c74a1fdba703c0c1e55 ` |                                                              |
|                                                    |                                                              |                                                              |
|                                                    |                                                              |                                                              |

