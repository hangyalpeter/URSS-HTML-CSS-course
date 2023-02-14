# URSS-HTML-CSS-basics

## Webfejlesztés alapjai

### Alapvető szoftverek, amire szükség lesz:
- Visual Studio Code (IDE): https://code.visualstudio.com/download
- Böngésző (Google Chrome): https://www.google.com/chrome/
- Git: https://git-scm.com/download/win

### Kiindulási pontok, tananyagok:
- MDN - https://developer.mozilla.org/en-US/docs/Learn/Front-end_web_developer
- W3SCHOOLS(HTML) - https://www.w3schools.com/html/default.asp
- W3SCHOOLS(CSS) - https://www.w3schools.com/css/default.asp
- CSS-TRICKS - https://css-tricks.com/

[HTML-CSS Introduction](https://slides.com/dmweb/html-css-i#/1)

### Hogyan működnek a weboldalak (forrás: https://academind.com/tutorials/how-the-web-works):



![how-do-webpages-work](https://res.cloudinary.com/academind-gmbh/image/upload/f_auto,q_auto:eco/dpr_2.0,w_400,c_limit,g_center/v1/academind.com/content/tutorials/how-the-web-works/how-the-web-works-big-picture)

### HTML alapok (HTML5)



A **HTML** (*HyperText Markup Langauge*) az alapvető építőköve a weboldalaknak. Ez határozza meg a tartalom szerkezetét. A HTML melletti technológiák általánosságban a weboldal megjelenését és viselkedését befolyásolják. (Hypertext => a weboldalak kapcsolódására, kapcsolatára utal)
A HTML megjelöli (= markup) a különböző tartalmakat (szövegeket, képeket, más tartalmakat), ezen megjelölések segítségével jeleníti meg a
böngésző a tartalmat. A HTML megjelölései különböző elemeket (element) tartalmaz. (pl.: ```<head>, <title>, <body>, <header>, <footer>, <article>, <section>, <p>, <div>, <span>, <img>, <nav>, <ul>, <ol>, <li>``` stb.) Egy HTML elemet *tagekkel* különböztetünk meg, ami az elem nevéből, és '<' és '>' karakterekből áll.

[HTML4 vs HTML5 - W3C (hivatalos - web szabványügyi testület)](https://www.w3.org/TR/html5-diff/)

A HTML-elemek **attribútumokkal** rendelkeznek; ezek olyan további értékek, amelyek az elemeket konfigurálják, vagy különböző módon módosítják viselkedésüket, hogy megfeleljenek a felhasználók által várt kritériumoknak. Ezek jellemzően mindig kulcs-érték párok,
és az értékeket ajánlás alapján mindin idézőjelbe érdemes tenni (pl.: ```<img src="img_girl.jpg">``` )

### CSS alapok

A CSS (Cascading Style Sheets) egy olyan nyelv, amely segítségével egy HTML dokumentum megjelenését tudjuk megfogalmazni. A CSS leírja, hogy
az adott elemek hogyan jelenjenek meg a böngészőben. Arra használjuk, hogy megadjuk az oldal elrendezését, betűtípusát, betűméretét, a színeket, 
háttereket, térközök beállítását stb.

3 lehetőségünk van stílusjellemzőket megadni: inline, internal, external 

Alap stílusjegyek: 
- background settings (color, image, size, position, repeat)
- text settings (font-size, color, font-family, font-weight, line-height, text-align, letter-spacing)
- sizing (absolute: px, cm, in, %, etc.  relative: em, rem, vh, vw, etc.)
- box-model (margin, padding, border)

**box-model**

![css-box-model](https://i0.wp.com/css-tricks.com/wp-content/uploads/2019/08/boxes-in-devtools.png?w=350&ssl=1)

[Bővebben a CSS box-modelről](https://css-tricks.com/the-css-box-model/)

### Szemantikus HTML elemek

A **szemantikus** HTML a weboldalon található tartalom jelentését erősíti, nem pedig egyszerűen a megjelenését. A szemantikus HTML-elemek olyan elemek, amelyek egyértelműen leírják a weboldal egy adott részének célját és tartalmát. A szemantikus elemek például a következők:

- ```<header>```: a dokumentum fejlécét tartalmazza, például a logót és a fő navigációt.
- ```<nav>```: a navigációs linkek tárolására szolgál.
- ```<main>```: egy dokumentum fő tartalmának meghatározására szolgál, amely csak az adott dokumentumra jellemző, kizárva a dokumentumok között ismétlődő tartalmakat, például a webhely fejléceit és lábléceit.
- ```<article>```: egy független, önálló tartalmi elem, például egy blogbejegyzés definiálására szolgál.
- ```<section>```: egy önálló tartalmi rész, például egy fejezet vagy bevezetés definiálására szolgál.
- ```<aside>```: a fő tartalomtól eltérő tartalom, például egy oldalsáv vagy egy kihúzott idézet definiálására szolgál.
- ```<footer>```: a dokumentum láblécének tartalmának meghatározására szolgál, például a szerzői jogi információk és a másodlagos navigáció.

A szemantikus elemek használata segít javítani a weboldalak hozzáférhetőségét és karbantarthatóságát, mivel megkönnyíti az oldal szerkezetének és tartalmának megértését mind az emberek, mind a gépek számára.

### Advanced CSS

#### Floating

A CSS **float** tulajdonsággal megadható, hogy egy elem hogyan 'lebegjen' a weblap elrendezésében. Ha egy elemet lebegőre (=float) állítunk, akkor az elemet kivesszük a dokumentum normál áramlásából, és a tartalmazó blokk bal vagy jobb oldalára helyezzük, lehetővé téve, hogy más elemek körülötte áramoljanak.

Ha például van egy kisebb elem (például egy kép), amelyet egy nagyobb szövegblokk jobb oldalán szeretne elhelyezni, akkor a 'float: right' tulajdonsággal elérheti ezt az elrendezést.

Fontos megjegyezni, hogy a lebegő elemek befolyásolhatják az oldal többi részének elrendezését, és clearfix technikákra lehet szükség ahhoz, hogy a lebegő elemeket a szülői konténerükön belül tartsák.

A float tulajdonság a bal és jobb mellett a none (az elem nem lebegtetése) és az inherit (a lebegő viselkedés átvétele a szülőelemtől) értéket is felveheti.

![css-floating](https://i0.wp.com/css-tricks.com/wp-content/uploads/2021/03/web-text-wrap.png?resize=540%2C270&ssl=1)

A 'clear' tulajdonsággal megadható, hogy az elem mely oldalain nem lebeghetnek a lebegő elemek. Segítségével szabályozható a lebegő elemek áramlása az oldalon, és megakadályozható, hogy a lebegő elemek átfedjenek más elemeket.

A clear tulajdonság a következő értékek egyikét veszi fel:

- none: Mindkét oldalon engedélyezi a lebegő elemeket.
- left: Megakadályozza a lebegő elemek lebegését a bal oldalon.
- right: Megakadályozza a lebegő elemeket a jobb oldalon.
- both: Megakadályozza a lebegő elemeket a bal és a jobb oldalon is.



#### Positioning

A **CSS pozicionálás** a HTML-elemek weblapon való elhelyezésének módszerére utal. A CSS position tulajdonság az elemhez használandó pozicionálási módszer típusának megadására szolgál. A 'position' tulajdonság öt értéket vehet fel:

- '**static**': ez az alapbeállítás, annyit jelent, hogy nincs hozzáadva semmilyen "mozgató" érték, vagyis úgy jelenik meg az oldalon az elem, ahogy azt a normal flowban elvárjuk. Csak akkor szoktuk használni, ha el akarjuk távolítani az akaratlan formázást az elemről, ekkor úgymond alaphelyezetbe állítjuk. 

- '**relative**': A relatív positioning annyit jelent, hogy az elem önmagában relatív. Ha nem adunk hozzá további attribútumokat, akkor nem fogja befolyásolni az elhelyezkedését (olyan, mintha static-ot kapott volna). Ha valamilyen irányba elmozdítjuk, akkor kimozdul a normal flow-ból. 
Ha parent elemben használjuk, akkor figyelni kell arra, hogy befolyásolja az absolute positionnel ellátott gyerek elemek pozícióját. 

- '**absolute**': Ha a position property absolute értéket kap, akkor alapértelmezetten nem változik meg az elem helyzete, de kikerül a normal html flow-ból (elrendezésből). A többi elem ezután nem veszi figyelembe. Az abszolút értéknek adhatunk további propertyket, amelyek befolyásolják az elhelyezkedését. Top-bottom-left-right irányba mozgathatjuk el, így állítható be a pozíciója. Ha ezeket az értékeket megkapja, akkor nincs már rá hatással a parent elem. 
Egy abszolút elem mindig megkeresi, hogy a parent elemek közül van-e relatív, vagy fixed pozíciójú. Ha talál, akkor ahhoz fog igazodni. Ha nem talál ilyet, akkor alapértelmezetten a bodyhoz igazodik. Különbözik a fixedtől abban, hogy nem lesz mindig ott a képernyőn, hanem elmozdul, ahogy legörgetünk.  

- '**fixed**': A fixed position relatíven igazodik a Viewporthoz, ami nem változik, ha az oldal lejjebb gördül. Ennek köszönhetően a Fixed elem ugyanott marad a képernyőn. Hasznos lehet olyan navbarok esetén, melyeket állandóan láttatni szeretnénk attól függetlenül, hogy a felhasználó az oldal melyik részét nézi épp.  Problémát okozhat a használata, ha pl. fixált elem eltakarja valamelyik alsó elemet az olvasó elől. 

- '**sticky**': a felhasználó görgetési pozíciója alapján kerül pozicionálásra. A "ragadós" elem a görgetési pozíciótól függően váltogatja a viselkedését relatív és fixed pozícionálás között. Az elem relatív pozícióban van, amíg egy adott eltolási pozíciót nem ér el a viewportban - ezután "ragad" a helyén (mint a fixed pozícióval rendelkező elemek). Leegyszerűsítve ez a tulajdonság egyesíti a relative és sticky tulajdonságokat.

![css-positioning](https://www.csssolid.com/images/csspositions/css-position-all.png)

#### Flexbox

A Flexbox egy CSS modul, amely segítségével különböző elemeket tudunk sorokba és oszlopokba rendezni.
Az elemeket ki tudjuk terjeszteni, nyújtani, vagy összeszűkíteni akár, hogy a kívánt elrendezést elérjük.

Sokáig a böngészők közötti kompatibilitást is támogató elrendezések kialakításához a floating és a positioning
tulajdonságokat lehetett használni, de ez a módszer elég nehézkes és kellemetlen és zavaró. (pl. egy blokk szintű
elem függőleges pozícionálása a szülőn belül, az összes gyerekelem azonos szélességet/magasságot vegyen fel egy 
szülőn belül stb.)

A flexbox alapelve, hogy a szülőelem képes legyen a gyerekelemeknek a szélességét és magasságát módosítani azért,
hogy megfelelően ki tudják tölteni a rendelkezésre álló helyet (főleg a reszponzivitás érdekében). Egy flex elem
kiterjeszti az elemeit a szabad helyekre vagy összeszűkíti azokat, hogy ne érjenek túl.

A Flexbox egy egydimenziós elrendezés, amely a gyakorlatban azt jelenti, hogy egyszerre egy dimenziót tudunk flexbox-szal
leírni: függőlegest vagy vízszintest - sort vagy oszlopot.

A Flexbox komponensek, kisebb egységek elrendezésére alkalmas leginkább, a Grid nagyobb méretű elrendezések 
kialakítására alkalmas.

* Flexbox basic properties

A display: flex tulajdonságot megadva a konténerünkre, az abban található elemek elrendezése flexbox elrendezés.
A block elemek egymás mellé rendeződnek, balról jobbra rendeződve (a fő tengely mentén).

https://res.cloudinary.com/practicaldev/image/fetch/s---3gDSFf1--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/fsln7je4ax7ft3er28hh.png
 
*flex-direction* *justify-content* *align-items* *flex-wrap* *flex-flow* *align-content* *gap* *order* 

https://www.freecodecamp.org/news/an-animated-guide-to-flexbox-d280cf6afc35/#.xdqa0my2e

* Flexbox advanced properties

*flex-grow* *flex-shrink* *flex-basis* *flex* *align-self*

https://www.freecodecamp.org/news/even-more-about-how-flexbox-works-explained-in-big-colorful-animated-gifs-a5a74812b053/