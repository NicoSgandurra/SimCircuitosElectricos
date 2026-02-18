# Deployment Hub - Instrucciones

Este directorio contiene la página principal (`index.html`) que actúa como un "Hub" para acceder a todos los simuladores del repositorio.

## Cómo Usar Localmente
1. Abre el archivo `index.html` en tu navegador web.
2. Navega a los diferentes simuladores usando las tarjetas.
3. El tema (claro/oscuro) se guardará en tu navegador.

## Cómo Desplegar en GitHub Pages
Para que este Hub funcione correctamente en GitHub Pages:

1. Asegúrate de que este repositorio esté subido a GitHub.
2. Ve a la configuración del repositorio en GitHub -> **Settings** -> **Pages**.
3. En **Source**, selecciona la rama (ej. `main` o `master`).
4. (Opcional) Si quieres que el Hub sea la página principal del repositorio, mueve el contenido de `Deployment/index.html` a la raíz del repositorio o configura GitHub Pages para publicar desde la carpeta que elijas (si GitHub lo permite, aunque usualmente es Root o Docs).
   - **Recomendación**: La forma más fácil es dejar esto aquí y acceder vía: `https://<usuario>.github.io/<repo>/Deployment/`
   
   Si prefieres acceder directamente desde la raíz (`https://<usuario>.github.io/<repo>/`), deberías mover este `index.html` a la carpeta raíz del repositorio y ajustar los enlaces (quitando el `../` al inicio de cada enlace).

## Estructura
El `index.html` utiliza enlaces relativos (`../Carpeta/Archivo.html`) para navegar a los simuladores que se encuentran en las carpetas hermanas.
