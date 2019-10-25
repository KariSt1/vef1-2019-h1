# Hópverkefni 1 í vefforritun 1
---
__Hópur 25, meðlimir:__
  * Fannar Skúli Birgisson
  * Gunnar Páll Júlíusson
  * Kári Steinn Aðalsteinsson
---
## Uppsetning á verkefni:
Til að keyra verkefnið:

```sh
npm install
npm run dev
```
Ef villa kemur við keyrslu þarf mögulega að installa eftirfarandi:
```sh
npm install @primer/css
```

Til að linta verkefni:

```sh
npm run lint-scss
```
---
## Lýsing á verkefni:
Verkefnið snérist um að hanna vefsíðu fyrir netverslun fyrirtækisins Prílihúsið.
Vefsíðunni er skipt niður í nokkrar undirsíður: 
  * Forsíða, html skjal fyrir hana er `index.html` og er staðsett í rót verkefnis.
  * Vörur, html skjal fyrir hana er `products.html` undir `pages/`.
  * Námskeið, html skjal fyrir hana er `course.html` undir `pages/`.
  * Starfsfólk, html skjal fyrir hana er `staff.html` undir `pages/`.
  * Karfa, html skjal fyrir hana er `cart.html` undir `pages/`.

Í `styles.scss` skránni sem staðsett er í rót verkefnisins eru grunnupplýsingar skráðar fyrir og inniheldur einnig import fyrir allar hinar scss skránnar sem gerðar voru.
Við skiptum ýmsum elementum síðunnar niður í sér scss skrár sem staðsettar eru undir `scss` möppunni:
  * Í `config.scss` eru skilgreindar grunnstærðir og föll sem notuð eru í verkefninu.
  * Fyrir allar síðurnar var notaður sami haus og fótur og fyrir hausinn eru tvær skrár, í fyrsta lagi
`header.scss` sem nær utan um allan hausinn og síðan `menu.scss` sem hefur hlekki yfir á allar undirsíður
verkefisins. Fyrir fótinn var gerð `footer.scss` skrá.
  * Fyrir `index.html` var gerð `home.scss` skrá ásamt `button.scss` skrá sem einnig var notuð á öðrum stöðum.
  * Fyrir `products.html` var gerð `products.scss` skrá ásamt `product.scss` skrá sem einnig var notuð á öðrum stöðum.
  * Fyrir `course.html` var gerð `course.scss` skrá ásamt `form.scss` skrá sem einnig var notuð á öðrum stöðum.
Hér var einnig notast við `button.scss` skránna aftur.
  * Fyrir `staff.html` var gerð `staff.scss` skrá.
  * Fyrir `cart.html` var gerð `cart.scss` skrá ásamt því að hún notar aftur `product.scss`, `form.scss` og `button.scss` skrárnar.

Í `img` möppunni eru allar myndir sem notaðar voru í verkefninu.

Í `package.json` skránni eru skilgreind script sem nota má til að keyra verkefnið ásamt því að hin ýmsu dependancies eru skilgreind. Í `node_modules` skránni eru pakkarnir sem notaðir eru til að keyra verkefnið staðsettir.

---
# Upprunaleg verkefnalýsing:
---
# Hópverkefni 1

Verkefnið felst í því að smíða vef eftir forskrift.

Gefnar eru [fyrirmyndir](utlit/) í `500px`, `800px` og `1500px` með grind ásamt `1500px` án grindar og yfirliti yfir virkni vefs í `utlit/video.mp4`.

## Síður

Gögn fyrir síður eru í viðeigandi textaskrám (t.d. forsida.txt) undir `efni/`. Myndir fyrir síður eru gefnar undir `img/`. Afrita þarf öll gögn á milli síðna, ekki er krafa um að setja upp sameiginlegan haus/fót á síðum með einhverju kerfi eða forritun.

Efni síðu skal ekki vera breiðara en `1200px`. Litir í haus og fæti skulu fylla út í allt lárétt pláss.

Síður hafa allar sama haus og sama fót. Vöruflokkar í fæti skulu allir vísa á `pages/products.html`. Námskeið í fæti skulu vís á `pages/course.html`

Grunn leturstærð er 16px og fylgja allar aðrar leturgerðir eftirfarandi skala: `12 14 16 18 21 24 36 48 60`.

Litapalletta fyrir vef er `#000000`, `#fffcf2`, `#ff5000` og `#00b7ff`.

Letur fyrir meginmál er Open Sans eða helvetica, arial eða sans-serif letur.
Letur fyrir fyrirsagnir er Oswald, Verdana eða serif letur.

Flest allt er sett upp í 12 dálka grind með `20px` gutter.

Öll bil eru hálft, heilt, tvöfalt eða þrefalt margfeldi af gutter. Hægt er að nota reglustiku tól (t.d. http://www.arulerforwindows.com/ eða http://www.pascal.com/software/freeruler/) til að finna nákvæmar stærðir en mestu skiptir að lausn svipi til en sé ekki nákvæmlega eins og fyrirmynd.

Allar hreyfingar gerast á `200ms` með `ease-in-out` hröðunarfalli.

Ekki þarf að útfæra neina virkni fyrir takka eða form.

## Hópavinna

Verkefnið skal unnið í hóp með þremur einstaklingum. Skráning í hópa fer fram í [Google sheets](https://docs.google.com/spreadsheets/d/1GwC9OvnpGHIkuX7ArRG7UQ-JV74b_pomegGXOWF1od0/edit?usp=sharing)

Notast skal við Git og GitHub. Engar zip skrár með kóða ættu að ganga á milli í hópavinnu, heldur á að „committa“ allan kóða og vinna gegnum Git.

## Lýsing á verkefni

`README.md` skrá skal vera í rót verkefnis og innihalda:

* Upplýsingar um hvernig keyra skuli verkefnið
* Lýsingu á uppsetningu verkefnis, hvernig því er skipt í möppur, hvernig CSS er skipulagt og fleira sem á við
* Upplýsingar um alla sem unnu verkefnið
* Leyfilegt er að halda eftir þessari verkefnalýsingu en hún skal þá koma _á eftir_ ykkar lýsingu

## Tæki og tól

Setja skal upp Sass og stylelint fyrir verkefnið. Gefin er `styles.scss` skrá með grunn upplýsingum.

Gefin er `.stylelintrc` skrá sem segir til um hvernig lint fyrir `scss` skrár skuli háttað.

Í `.gitignore` er `styles.css` hunsað sem þýðir að það verður _ekki_ checkað inn. Það er gert vegna þess að það er búið til af sass út frá `styles.scss`

## Gefnar skrár

Eftirfarandi er sett upp í verkefni:

* `.stylelintrc` með upplýsingum um hvernig stylelint eigi að haga sér. Setja þarf upp `stylelint-config-primer` pakkann
* `.gitignore` sem hunsar algengar skrár, [sjá nánar](https://help.github.com/ignore-files/)
* `.gitattributes` sem kemur í veg fyrir ósamræmi sem geta komið upp þegar unnið er á milli stýrikerfa
* `.editorconfig` sem samræmir notkun á tabs og spaces, bilum [og fleira](https://editorconfig.org/)
* `index.html` með vísun í `styles.css` og `grid.css` ásamt tómum skrám fyrir `products.html`, `staff.html`, `course.html` og `cart.html` undir `pages/`, halda skal þessu skipulagi
* `grid.css` til að sjá grid sem fyrirmynd er unnin eftir

Setja þarf upp `package.json` og sækja viðeigandi pakka til að tæki og tól sem verkefnið á að nýta virki.

## Mat

* 10% - `README` eftir forskrift, tæki og tól uppsett
* 20% – Snyrtilegt, gilt (skv. stylelint) CSS/Sass, gilt og aðgengilegt HTML
* 30% – Almennt útlit
* 8% – Forsíða
* 8% – Vörur síða
* 8% – Námskeið síða
* 8% – Starfsfólk síða
* 8% – Karfa síða

## Sett fyrir

Verkefni sett fyrir í fyrirlestri mánudaginn 7. október 2019.

## Skil

Einn aðili úr hóp skal skila fyrir hönd allra og skila skal undir „Verkefni og hlutaprófa“ á Uglu í seinasta lagi fyrir lok dags föstudaginn 25. október 2019.

Skil skulu innihalda:

* Nöfn allra í hóp ásamt notendanafni
* Slóð á GitHub repo fyrir verkefni, og öllum dæmatímakennurum skal hafa verið boðið í repo ([sjá leiðbeiningar](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/)). Notendanöfn þeirra eru `anz1e`, `gunnnnii`, `magdadianaa`, `OlafurjonHI` og `Wolfcoder13` .
* Slóð á verkefnið keyrandi á vefnum.

## Einkunn

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 3,5% hvert, samtals 28% af lokaeinkunn.

Sett verða fyrir tvö stærri verkefni þar sem hvort um sig gildir 11%, samtals 22% af lokaeinkunn.

## Myndir

Myndir frá:

* [Innkaupakörfu fengin á iconfinder](https://www.iconfinder.com/icons/216460/cart_icon)
* [Aðrar myndir fengnar frá Unsplash](https://unsplash.com/photos/N4QTBfNQ8Nk)
