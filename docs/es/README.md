# Bievenido a la localización de MDN en español 

Puedes comenzar en la siguiente [guía de contribución](https://developer.mozilla.org/es/docs/MDN/Contribute)

## Pasos para configurar el entorno local

> Puedes ver: https://youtu.be/pFeW0vUYbkg

## Pasos para abrir un Pull Request
### Desde tu computadora
> Crear rama, hacer commit, crear pull request, esperar revisiones.
> * Acceder a GitHub: https://github.com/login/
> * Ir a https://github.com/mdn/translated-content
> * ![Screenshot 2022-03-01 at 17-13-20 mdn translated-content All translated MDN content in raw form](https://user-images.githubusercontent.com/13079269/156264660-afcba14a-14a0-4c66-9a33-c1e2ad41737b.png) hacer Fork al repositorio en nuestra cuenta de GitHub.
> * Clonar el repositorio de nuestra cuenta de GitHub `git clone git@github.com:TU_USUARIO/translated-content.git`
> * `cd translated-content` #Entrar al directorio
> * `git checkout -b patch-error-on-123-issue` #Crear rama para trabajar
> * Hacer nuestros cambios
> * `git add files/es/archivo.md` #Agregamos los arachivos modificados
> * `git rm files/es/archivo.html` #Removemos los archivos eliminados
> * `git commit -m "Corregido el error 123 [es]"` #Hacemos commit con una descripción de lo realizado y agregamos `[es]`
> * `git push -u origin patch-error-on-123-issue` #Subimos nuestra rama a nuestro repositorio
> * Ir a nuestro repositorio https://github.com/TU_USUARIO/translated-content y solicitar el Pull Request

A continuación puedes ver un ejemplo en video: https://youtu.be/pFeW0vUYbkg

## Pasos para traducir un documento

Ejemplificaremos el proceso a realizar cuando se desea traducir el contenido de una página.
Ejemplo:

Digamos que desea traducir el contenido de la página que se observa en esta dirección.
    ![image](https://user-images.githubusercontent.com/7331511/152851642-5dea4df9-f771-4323-bc13-b238dec511ef.png)
1. Buscar la [versión original (en inglés)](https://github.com/mdn/content/tree/main/files/en-us) del documento que desea traducir.
    Debería buscar en el repositorio [en inglés (mdn/content)](https://github.com/mdn/content) el archivo correspondiente al documento, en este caso la dirección sería [`files/en-us/web/javascript/reference/global_objects/array/index.md`](https://github.com/mdn/content/blob/main/files/en-us/web/javascript/reference/global_objects/array/index.md)

2. Buscar la [versión en español](https://github.com/mdn/translated-content/blob/main/files/es/) del [documento](https://github.com/mdn/translated-content/blob/main/files/es/web/javascript/reference/global_objects/array/index.html) que desea traducir. En este caso la dirección seria [`files/es/web/javascript/reference/global_objects/array/index.{html|md}`](https://github.com/mdn/translated-content/blob/main/files/es/web/javascript/reference/global_objects/array/index.html)

    > NOTA:
    > - Si el archivo no existe, deberá crearlo en formato `Markdown` imitando la ruta que tiene la versión en inglés. 
    >
    > - Es posible que el archivo en la versión en español se encuentre en formato `HTML`, en cuyo caso tendrá que reemplazarlo por el formato `Markdown`.

3. Utilizar el texto y formato en inglés como guía para traducir al español. 


## Convención en traducciones

La comunidad de español sugiere utilizar las siguientes convenciones al traducir el contenido.

<details>
  <summary>Traducciones recomendadas</summary>

| Término original                | Traducción                     |
| ------------------------------- | ------------------------------ |
| Event listener                  | Detector de eventos            |
| Event handler                   | Manejador de eventos           |
| See also                        | Véase también                  |
| Browser compatibility           | Compatibilidad con navegadores |
| HTML Content o HTML             | HTML                           |
| JavaScript Content o JavaScript | JavaScript                     |
| Warning | Advertencia |

</details>

Actualmente trabajando en: https://github.com/mdn/translated-content/issues/6562

Charla con nosotros:

Telegram: https://t.me/+Dr6qKQCAepw4MjFj

Matrix: https://chat.mozilla.org/#/room/#mdn-l10n-es:mozilla.org

<details>
  <summary><h2>Enlaces relevantes</h2></summary>

Documentación por prioridad.
https://developer.mozilla.org/en-US/docs/MDN/Contribute/Documentation_priorities 

Proyecto `ES` en GitHub
https://github.com/mdn/translated-content/projects/7

Telegram link
https://t.me/+Dr6qKQCAepw4MjFj

Matrix link
https://chat.mozilla.org/#/room/!cIEBGoIHFpsXNeVUwp:mozilla.org

Grupo en community
https://community.mozilla.org/en/groups/mdn-localizacion-espanol/

Los `tags` no se usan para las traducciones de la documentación,  borremoslo.
https://github.com/mdn/translated-content/pull/4058#discussion_r802298455

Tutorial para crear el ambiente de desarrollo para MDN
https://www.youtube.com/watch?v=pFeW0vUYbkg

Guía de markdown
https://developer.mozilla.org/en-US/docs/MDN/Contribute/Markdown_in_MDN
</details>

Más información [aqui](https://github.com/mdn/translated-content/discussions/4029)