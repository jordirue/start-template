## Plantilla per iniciar maquetes

Framework creat amb:

**Yarn**
[https://yarnpkg.com/es-ES/](https://yarnpkg.com/es-ES/)

**Gulp**
[https://gulpjs.com/](https://gulpjs.com/)

**Postcss**
[https://postcss.org/](https://postcss.org/)

**Panini**
[https://foundation.zurb.com/sites/docs/panini.html](https://foundation.zurb.com/sites/docs/panini.html)

**Instal·lar:**
```markdown
yarn install
```

**Treballar-hi:**
```markdown
gulp dev
```

**Crear la maqueta final:**
```markdown
gulp
```

## HTML

La manera de construir els HTMLs és com les nines russes, tenim un tros de codi que conté un tros de codi que a la vegada conte un altre tros, etc.

Per crear el codi HTML, utilitza Panini de Zurb
Documentació: [https://github.com/zurb/panini](https://github.com/zurb/panini)

Amb 'doble {' inserim text, sigui del propi html o des de un .yml
```html
{+{ inserim text }+}
```
_**Si ho copies, elimina el símbol (+)**_

Amb 'doble { + >' inserim el contingut d'un .html
```html
{+{> inserim un .html}+}
```
_**Si ho copies, elimina el símbol (+)**_

### Organització dels htmls

Organitzem tots els arxius per construir els htmls de la següent manera:

**Data**
Fragments de text per reutilitzar

**Layouts**
Plantilles de pàgines html

**Pages**
El codi que s'incrusta en el { { body } } dels layouts

**Partials**
Parts de codi reutilitzables en qualsevol lloc que necessitem 

### Partials

Diferents parts de codi html per construir parts de les pagines

**Blocks**
El contingut de la pàgina s'estructura en diferents blocs (portada, galeries, ...), aquests estan formats per diferents organismes

**Organisms**
Un organisme es un grup de components html que units formen una part (bloc) de la pàgina (sidebar, llistat, ...)

**Molecules**
Components html, que units a d'altres, formen part d'un organisme (article, buscador, ...)

**Atoms**
Elements bàsics del codi, sols o conjuntament amb altres formen components (boto, títol de secció, ...)



## Data

Arxius .yml on tindrem text reutilitzable. Per exemple el text dels botons, dels títols, ...

Exemple del nom del site:

1. Tenim un .yml (site.yml) amb el nom del site:
```markdown
txt__nomsite:
  -
    text: Nom del site
```
2. Ara hi afegim aquest text al html:
```markdown
{+{#each site.txt__nomsite}+}
{+{ text }+}
{+{/each}+}
```
_**Si ho copies, elimina el símbol (+)**_

## Layouts
```markdown

```
## Pages
```markdown

```
## Partials
```markdown

```
