# Web de Yeite

La página de la banda: **https://yeite-banda.netlify.app**

Es un solo `index.html` con las fotos y el video al lado. No hay nada que compilar: lo que ves en tu compu es lo que publica Netlify.

Para un cambio chico desde el navegador, sin instalar nada, seguí [LEEME.md](LEEME.md). Esta guía es para trabajar desde tu compu y ver los cambios antes de subirlos. Si te trabás en algún paso, pasale este archivo a tu asistente de IA y contale qué querés hacer.

## Qué necesitás

Solo **git**. En la Terminal escribí `git --version`. Si no lo tenés, la Mac te ofrece instalar las "herramientas de línea de comandos": aceptá. Eso también trae Python, que sirve para ver la web en tu compu. No hace falta nada más.

Para subir cambios necesitás una cuenta de GitHub con permiso en este repo (pedíselo a Eze o a Mati).

## Bajar el repo (una sola vez)

```
git clone https://github.com/yeite-banda/yeite-web.git
cd yeite-web
```

## Antes de cada cambio

Traé lo último y abrí una rama con un nombre que diga qué vas a hacer:

```
git checkout main
git pull
git checkout -b fecha-22-11
```

## Ver la web en tu compu

Desde la carpeta `yeite-web`, usá lo que ya tengas instalado:

- Si tenés **Node**: `npx serve` y abrí http://localhost:3000
- Si no: `python3 -m http.server 8000` y abrí http://localhost:8000

Editá `index.html`, guardá y recargá el navegador. Para apagar el servidor, Ctrl+C en la Terminal.

Si editás con TextEdit, primero en **TextEdit → Ajustes** activá la opción de abrir los HTML como código y desactivá las comillas tipográficas. Si no, rompe la página.

Antes de subir, revisá:

- **Celular:** achicá la ventana del navegador a ancho de teléfono. Que nada quede cortado ni se salga de las tarjetas de fechas.
- **Modo oscuro:** la web cambia de colores con el modo oscuro del sistema. Probala en **Configuración del Sistema → Apariencia → Oscuro**.
- **Links:** que los botones de entradas e Instagram abran donde tienen que abrir.

## Subir el cambio

La rama `main` está protegida: los cambios entran por un *pull request*. Mirá qué cambió con `git status`, agregá solo lo que tocaste y subí la rama:

```
git add index.html
git commit -m "agrego fecha 22/11"
git push -u origin fecha-22-11
```

La primera vez git te pide usuario y contraseña de GitHub:

- Si ya tenés **gh** instalado, corré `gh auth login` antes del push y no te pide nada.
- Si no, como contraseña va un *token*. Crealo en https://github.com/settings/tokens/new tildando solo `public_repo`. La Mac lo guarda y no te lo vuelve a pedir.

El push te muestra un link para crear el pull request. Abrilo, tocá **Create pull request** y después **Merge pull request** → **Confirm merge**. En un minuto Netlify actualiza la web.

Para dejar todo listo para el próximo cambio:

```
git checkout main
git pull
```

## Si algo sale mal

Si la web publicada se rompió, en el pull request que la rompió tocá **Revert** y mergeá el pull request nuevo que se crea. O avisale a Eze o a Mati.
