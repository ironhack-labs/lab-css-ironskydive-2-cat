![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Exercici guiat - IronSkydive 🎨 - estil (CSS)

<br/>

## Introducció

A hores d'ara, t'has familiaritzat amb les Fulles d'Estil a Cascada (CSS), i saps com

- orientar elements usant etiquetes, classes o ids,
- treballar amb les propietats de la font i el text,
- afegir colors al text i al fons.

Recorda obrir el **CodePen** que vas crear al principi de l'exercici per fer-ne les diferents iteracions.

Anem allà.

<br/>

## IDs

En primer lloc, afegiràs quatre ids, un per cada `<section>` que hagis definit. De dalt a baix, els ids han de ser

- `información general`
- `estructura`
- `equipo`
- `horario`

Això ens ajudarà a identificar les diferents seccions. Això també va crear alguna cosa anomenat [enllaços interns](http://www.yourhtmlsource.com/text/internallinks.html) . Què passa ara si es fa clic als enllaços `<nav>`a la part superior de la pàgina? Es desplaça automàticament cap avall a la secció! :white_check_mark:

<br/>

## Configuració general per a tota la pàgina

Bé, comencem a fer servir la pestanya CSS dins del teu projecte de CodePen. Començarem configurant tota la pàgina perquè utilitzi la regla següent (copieu el fragment al principi de la pestanya CSS):

```css
html,
body {
  margin: 0;
  padding: 0;
}
```

Això eliminarà el `margin` i el `padding` de tots els elements, o en llenguatge senzill, els posarà a `0` . Per què fem això? Estem fent això per restablir alguns estils que el vostre navegador aplica automàticament als elements, coneguts com a _estils per defecte del navegador_ .

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_603c70d5d3664d3cd0d7829c6b0367cb.png)

<br/>

:thought \_balloon: No et preocupis pel que són les propietats `margin` i `padding` ara mateix, les discutirem en un moment.

<br/>

## Font i text

### font-family

Per a tot el lloc web d'IronSkydive, utilitzarem una font anomenada `Roboto` . Pots trobar-la a `https://fonts.google.com/` , el repositori de Google que acull un gran nombre de fonts. Normalment has de passar per un procés per incrustar una d'aquestes fonts al teu lloc, però nosaltres ho hem simplificat per a tu.

Al principi de la pestanya CSS del teu CodePen, copia la següent línia:

```css
@import url('https://fonts.googleapis.com/css?family=Roboto+Condensed:700|Roboto:100,300,700');
```

Encara no passa res. Només afegeix una referència a dues fonts diferents:

- `Roboto` , amb pesos de 100, 300 i 700.
- `Roboto Condensed` , amb un pes de 700.

Vostè utilitzarà tots dos al vostre lloc web. Així que canviarem la font per a tot el document. Tot el document ha de tenir el text formatat de la següent manera:

- font: `Roboto` .
- mida: `10px` .
- alçada de línia: `3.5em` .
- pes: `300` .

Recorda: podem apuntar als elements sobre els quals volem aplicar alguns estils usant la classe o l'id o el _nom de l'etiqueta_ .Pots fer servir l'etiqueta `body` i afegir aquestes propietats CSS respectives. Un cop definida la font per al document, canviarem el comportament de les capçaleres.

Si utilitzeu les capçaleres de l'1 al 5, utilitzeu un _multiselector_ que els seleccionarà tots. Dins aquest selector, estableix la font com a `Roboto Condensed` . Modificarem la mida de les capçaleres en un altre selector ja que cadascun tindrà una mida diferent.

```css
/* CSS multiselector example */

h1,
h2,
h3,
h4,
h5,
h6 {
  /*  define font-family here  */
}
```

El resultat hauria de ser una cosa així:

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_8772412e132f34f5246213a371f16ea5.png)

<br/>

### Propietats del text

Ara mateix totes les fonts tenen la mateixa mida, canviarem. En primer lloc, estilitzarem les capçaleres incloent les següents propietats:

| Encapçalat | Propietats                                                   |
| ---------- | ------------------------------------------------------------ |
| `<h1>`     | Mida:`9em` <br/> Alinear:`center` <br/> Transformar:`uppercase` |
| `<h2>`     | Mida:`5em` <br/> Alinear:`center` <br/> Transformar:`uppercase` |
| `<h3>`     | Mida:`4.2em` <br/> Alinear:`center` <br/> [ Alçada de la línia](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) :`1em` |
| `<h4>`     | Mida:`1.5em` <br/> [ Espai entre lletres](https://developer.mozilla.org/en/docs/Web/CSS/letter-spacing) :`0.4px` <br/> [ Alçada de línia](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) :`1em` |
| `<h5>`     | Mida`1.2em` <br/> [ Alçada de línia](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) :`1em` |

Un cop aplicats aquests estils a les diferents capçaleres que tenim, `<h1>` i `<h2>`necessiten més espai entre elles. Afegirem més espai establint la propietat d'alçada de línia `<h2>`de `line-height` a `4em` .

Ja heu especificat tots els estils de text que necessiteu tenir al vostre lloc web.

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_b0f5f1c39886cbe09c75630ca7706c2a.png)

<br/>

Genial, ara afegirem alguns colors al nostre lloc web.

<br/>

## Colors

<br/>

Anteriorment, vostè va utilitzar les propietats de text CSS per canviar l'aparença del lloc web, afegint una font i mides personalitzades, depenent de l'etiqueta. Ara és el moment de donar-li una mica de color!

Quan estàs desenvolupant un lloc web, és una bona pràctica tenir en compte una taula amb els diferents colors que utilitzaràs. En aquest cas, la taula és:

| Color     | RGB            | Resultat                                                     |
| --------- | -------------- | ------------------------------------------------------------ |
| Blau      | `67, 163, 230` | <div style="background:rgb(67, 163, 230);height:20px;margin:0 auto;width:20px"/></div> |
| Blau fosc | `25, 33, 41`   | <div style="background:rgb(25, 33, 41);height:20px;margin:0 auto;width:20px"/></div> |
| Text      | `0, 0, 0`      | <div style="background:rgb(0, 0, 0);height:20px;margin:0 auto;width:20px"/></div> |

Aquesta taula us ajudarà a comunicar-vos amb el vostre equip de disseny UX/UI. Quan et diguin que apliquis el `dark blue` com a color de fons, sabràs immediatament de quin color es tracta.

Descriurem un a un els canvis que has d'aplicar sobre les diferents seccions que definim a la primera iteració d'aquest exercici. Recorda el disseny que hem creat:

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_8f778c8cd703db596d5bb22dae089716.jpg)

<br/>

Obre CodePen al teu navegador, i comencem!

<br/>

### Nav

<br/>

L'objectiu final de la barra de navegació és el següent:

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_065124c74d928a12e32e446b759968e3.png)

<br/>

Comencem per afegir el color. Afegeix el `dark blue` com a color de fons.

És una bona pràctica utilitzar selectors de classe en lloc de fer servir selectors d'etiquetes HTML per definir estils. Què passa si apliques un estil a l'etiqueta `nav` i en el futur la canvies a `header` ? Perdries tots els estils, i els canviaries un a un al CSS.

Crea un selector a la fitxa CSS anomenat `.nav-bar` , i assigna l'estil descrit anteriorment. Després, assigneu la classe a l'etiqueta `nav` al vostre HTML.

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_320885335d288348997362c44aa6f6b0.png)

<br/>

Ja funciona... més o menys. Hem d'establir el color dels enllaços en blanc i si intentes establir la propietat `color: white` dins de la classe `.nav-bar` , no funcionarà perquè les paraules/enllaços estan embolicades dins una etiqueta `a` .

Podem anar a la direcció de la creació d'una nova classe i adjuntar la classe a cada element `li` dins de`<nav>`, o podem anar **DRY** (Don't Repeat Yourself) i evitar la creació d'una classe més, però en lloc de això, la referència dels elements que volem orientar a través de la classe existent `.nav-bar` .

```css
.nav-bar a {
  /*  styles to be added here    */
}
```

<!-- Let's create another class, called `nav-bar-item`, and -->

Canvia el `color` a _blanc_ , el `text-decoration` a _none_ i el `font-size` a `2em` per obtenir el resultat desitjat.

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_e03b2f8983da0df77b6e88f973cfc0c5.png)

<br/>

A les següents iteracions, completaràs el menú. Estàs llest per passar a la secció següent.

<br/>

### Encapçalat

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_e80b0ee85c8f2fb8126befe68b152ab2.png)

<br/>

No tinguis por. És més fàcil del que sembla. En primer lloc, has destablir la imatge de [fons](https://developer.mozilla.org/en/docs/Web/CSS/background-image?v=control) . Les propietats de la imatge de fons són

- **url:** `https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/ironhack-skydive-background.jpg.`
- **posició:** `0 0` .
- **repetir** : `no-repeat`
- **mida** : `cover` .

Recorda que has de crear una classe, en aquest cas `header` , i assignar-la a l'etiqueta `header` al teu HTML per utilitzar aquest estil. Ara, només cal establir lalçada de la `header` a `650px` .

El següent pas és canviar el color de `h2` a blanc, i després afegir una ombra de [`texto`](https://developer.mozilla.org/en/docs/Web/CSS/text-shadow) . La propietat `text-shadow` ha de tenir com a valor `#020819 8px -20px 9px` .

Per acabar aquesta secció, canvieu la mida de la font de la cita. Poseu-lo a `2.5em` . Crea una classe de `quote` per fer això, i afegeix la classe a l'etiqueta `aside` a l'HTML.

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_c03f57b39ea0d76161156d6e58d91307.png)

<br/>

### Secció 1

En una de les iteracions anteriors, vas afegir un _id_ `general-information` a aquesta secció. El nostre objectiu final per a aquesta secció és:

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_505f90aabf6c0d4e03b4216c07c615f8.png)

<br/>

Crear un selector de classe `dark-background` , que apliqui les propietats següents

- color de fons: dark blue (vegeu la taula al principi d'aquesta iteració).
- color: blanc.

Un cop creada la classe al teu CSS, afegeix-la a la secció. Després d'aplicar la classe, pots veure que el text al és diminut, i no està centrat. Solucionarem aquest problema.

Primer, a cada paràgraf dins de la secció `general-information` , afegeix una classe de `text` .

<!-- Then create a multiple selector, that selects all the elements with a `.text` class inside the `#general-information` element. -->

Aquest selector ha de tenir les següents propietats CSS:

- Mida de la font: `2em` .
- Pes de la font: `100` .
- Alineació del text: `centro` .

Molt millor. Acabem aquesta secció afegint alguns estils als enllaços. Els enllaços es veuran com a botons, i tots els enllaços d'aquesta secció tindran la mateixa aparença. Això vol dir que has de crear una classe que apliqui les propietats CSS necessàries a un enllaç perquè s'assembli a un botó.

<br/>

:::info

:bulb : **Per què no fer servir un botó?** Consulta [aquesta resposta molt concisa de StackOverflow](https://stackoverflow.com/a/25350722/4624718) per conèixer una bona regla general

:::

<br/>

Crearem una classe `link-btn` amb les següents propietats:

- color de fons: blau (mireu la taula al principi d'aquesta iteració).
- color: blanc.
- font-family: `Roboto Condensed` .
- mida de la font: `2em` .
- [Espai entre lletres](https://developer.mozilla.org/en/docs/Web/CSS/letter-spacing) : `0.5px` .
- alineació del text: `center` .
- text-decoration: `none` .

Afegeix la classe als tres enllaços que tens a la secció.

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_7847968ca22bceb75dac295214859d36.png)

<br/>

Hmm... Sembla que necessitem una manera de reordenar els nostres elements i posar-los a certes posicions. Aquest serà l'objectiu d'una de les properes iteracions.

Passem a la següent secció.

### Secció 2

A la segona secció, hem afegit un id de `structure` . En aquesta secció, només cal configurar les propietats de mida de font i alineació.

<!-- You will also remove the `img` width property, and set it in the CSS. -->

Crea una classe `service-box` al CSS, amb les propietats següents:

- Mida de la font: `1.7em` .
- Alineació del text: `center` .

Assigna aquesta classe a cada `article` dins de la secció de `structure` .

Ara crea nous selectors múltiples per a totes les classes `img` , dins de la classe `service-box` .

:+1: Spoiler: Similar al que ja vas fer amb els enllaços a la navbar, aquí tindrem el següent:

```css
.service-box img {
  /*  styles to be added  */
}
```

Afegir una propietat dins per establir l'amplada d'aquestes imatges a `125px` .

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_85b85fdc98c951967b3554ee821cbfaa.png)

<br/>

### Secció 3

L'objectiu més important en escriure CSS de qualitat és crear classes que es puguin reutilitzar. En aquesta secció, tornem a tenir el blau fosc com a color de fons. Anteriorment heu creat una classe de fons fosc i ara afegeix aquesta classe a la secció de l'equip.

Ara, has de crear dues classes diferents - una per al text de la secció, i una altra per als noms dels membres de lequip. La primera classe, `section-text` , tindrà una mida de font de `1.9em` , i el text haurà d'estar alineat al `centro` .

D'altra banda, la classe `member-name` tindrà una mida de font de `1,` 5em, amb un pes de font de `700` . Afegeix la primera classe a la `p` a l'HTML, i la segona a totes les etiquetes `h4` .

Per evitar que les propietats sobrescriguin altres classes, creeu un selector múltiple per establir aquestes classes específicament dins de l'element id de l'equip:

```css
#team .section-text {
}

#team .member-name {
}
```

A més, ens ocuparem de les imatges d'aquesta secció. Com podem veure són súper grans. Fem servir selectors múltiples per apuntar a les etiquetes `img` dins de `#team` i establim el:

- width a 250px i
- height a 180px.

:+1: Spoiler:

```css
#team img {
  /* styles to be added here */
}
```

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_dbe16d63517310a82a988f9f13df4867.png)

<br/>

### Secció 4

_Aquí no hi ha res a fer... encara!_

### Peu de pàgina

De nou, tenim un fons fosc i un text blanc. Afegeix la classe de `dark-background` a l'etiqueta de `footer` a l'HTML. Crea una classe de `footer` i afegeix-la com a segona classe a l'etiqueta`<footer>`. Fes servir aquesta classe per centrar tot el text dins d'aquest element i per establir la mida de la font a `1.9em` .

:+1: Spoiler: Per afegir una segona classe, has de fer el següent:

```html
<!-- ... -->

<footer class="dark-background footer">
  <!-- ... -->
</footer>
```

Ara, creeu una nova classe - `address` , i assigneu-la a l'etiqueta HTML `address` . En aquesta classe, definir:

- estil de font: `normal` .
- mida de la font: `0.8em` .

Ja gairebé hem acabat. De la mateixa manera que hem seleccionat tots els enllaços dins de la barra de navegació (utilitzant un enfocament de selecció múltiple), aquí seleccionarem tots els enllaços dins del peu de pàgina i els seus estils:

- color: blau (mireu la taula al principi d'aquesta iteració).
- text-decoration: none.

Assigna aquesta classe a cada element dins la llista que tens al peu de pàgina.

:+1: Spoiler: La manera de fer-ho és la següent:

```css
.footer a {
  /* styles to be added here */
}
```

I un, l'última per a aquesta iteració és treure els punts de la llista que està mostrant els enllaços de les xarxes socials. Vostè pot apuntar a l'etiqueta `ul` dins del peu de pàgina i establir la propietat `list-style` a _cap_ . Així que aquí és!

<br/>

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_791457cbe452066c3123de22f4182eb8.png)

<br/><br/>

:heart: **Feliç codificació!**