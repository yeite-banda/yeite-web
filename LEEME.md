# Web de Yeite

La página está publicada en **https://yeite-banda.netlify.app**.
Cada vez que se guarda un cambio acá en GitHub, Netlify la actualiza sola en un minuto.

## Cómo cambiar algo (sin instalar nada)

1. Entrá a este repositorio y tocá `index.html`.
2. Tocá el lápiz ✏️ (arriba a la derecha del archivo).
3. Buscá el texto con Cmd+F (Ctrl+F en Windows), cambialo y nada más.
4. Tocá el botón verde **Commit changes**, escribí qué cambiaste (ej. "agrego fecha 22/11") y elegí **Create a new branch for this commit and start a pull request**. Confirmá con **Propose changes**.
5. En la pantalla que sigue tocá **Create pull request**, y después **Merge pull request** → **Confirm merge**. (La rama `main` está protegida: los cambios entran siempre por un pull request, no hace falta que nadie lo apruebe.)
6. Esperá un minuto y recargá la web.

## Lo más común

**Una fecha nueva:** en `index.html` buscá `<article class="fecha">`. Copiá un bloque entero, desde `<article class="fecha">` hasta `</article>`, pegalo abajo y cambiá día, mes, lugar y texto.
- Si todavía no hay entradas: `<span class="pronto">Entradas muy pronto vía link</span>`
- Si hay link: `<a class="btn solid" href="LINK-DE-ENTRADAS" target="_blank" rel="noopener">Entradas</a>`

**Una fecha que ya pasó:** borrá su bloque `<article>...</article>` de "Próximas fechas" y sumala en "Dónde tocamos" (buscá `Dónde tocamos`) con una línea así:
`<dt>22/11/2026</dt><dd>Ituzaingó</dd>`

**Cambiar una foto:** subí la foto nueva con el MISMO nombre (ej. `mati.jpg`) con **Add file → Upload files**. Reemplaza a la anterior.

## Para no romper nada
- Cambiá solo el texto que está entre `>` y `<`. No borres los `<` `>` ni las comillas.
- Si algo se rompe: tocá el archivo → **History** → abrí la versión anterior y volvé a guardarla, o avisale a Eze.
