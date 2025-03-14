## Plantilla per iniciar maquetes

Creat amb:

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

Amb '{ {' inserim text, sigui del propi html o des de un .yml

Amb '{ { >' inserim el contingut d'un .html

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

### Organització dels partials

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

1. Tenim un .yml (site.yml) amb el nom del site
2. Ara hi afegim aquest text al html

## Layouts

Plantilles html per organitzar el contingut segons ens convingui

_Layout modificat:

En aquest cas, hi hem afegit un header i un footer.

També, en el body, afegim una class que indicarem dintre de les pàgines_

## Pages

Posem un nom descriptiu del contingut (Ex: home.html)

_Al principi indiquem quin Layout volem utilitzar, el nom que sortirà en title i la class que afegim al body (Així modifiquem alguns aspectes del layout)

Després afegim l'estructura del html i afegim els HTMLs que tindrà la pàgina (Es carrega dins del {body} del layout)_

## Partials

### Blocks

Anomenem cada block en relacio a la pàgina on es pinta (Ex: block-home-01.html)

En un block afegim els components que formaran aquest

### Organisms

Nom en relació al que conte (Ex: or__3columnes.html)

Organitzem la forma en què es veuran els elements (Per exemple en columnes)

### Molecules

Nom descriptiu component (Ex: mo__article.html)

Sovint el reutilitzem, per això és important utilitzar els .yml del directori 'data' per modificar-lo 

### Atoms

Nom descriptiu del l'element (Ex: at__titol.html)

En aquest cas li diem que el text del títol serà el nom del site que abans em posat al .yml



## Plugins

* [gulp-imagemin](https://github.com/sindresorhus/gulp-imagemin)

* [posthtml-lorem](https://github.com/jonathantneal/posthtml-lorem)
* [posthtml-bem](https://github.com/rajdee/posthtml-bem)
* [posthtml-alt-always](https://github.com/ismamz/posthtml-alt-always)

* [sanitize.css (Reset)](https://github.com/csstools/sanitize.css)
* [gulp-postcss](https://github.com/postcss/gulp-postcss)
* [gulp-cssnano](https://github.com/ben-eb/gulp-cssnano)
* [gulp-sourcemaps](https://github.com/gulp-sourcemaps/gulp-sourcemaps)

* [precss](https://github.com/jonathantneal/precss)
* [postcss-scss](https://github.com/postcss/postcss-scss)
* [postcss-preset-env](https://preset-env.cssdb.org/)
* [postcss-utilities](https://ismamz.github.io/postcss-utilities/)
* [css-mqpacker](https://github.com/hail2u/node-css-mqpacker)
* [postcss-discard-duplicates](https://github.com/ben-eb/postcss-discard-duplicates)
* [postcss-uncss](https://github.com/uncss/postcss-uncss)
* [postcss-extend](https://github.com/travco/postcss-extend)
* [lost](https://github.com/peterramsing/lost)
* [postcss-pxtorem](https://github.com/cuth/postcss-pxtorem)

* [jshint](http://jshint.com/)
* [gulp-jshint](https://github.com/spalger/gulp-jshint)
* [gulp-uglify](https://github.com/terinjokes/gulp-uglify)
* [gulp-babel](https://github.com/babel/gulp-babel)
* [babel-preset-env](https://github.com/babel/babel-preset-env)
* [babel-core](https://github.com/babel/gulp-babel/issues/124)
* [just-detect-adblock](https://github.com/wmcmurray/just-detect-adblock)

## LICENSE

MIT License

Copyright (c) 2018 Jordi Rué

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
