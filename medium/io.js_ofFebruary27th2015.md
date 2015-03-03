**io.js 2015 Február 27-i blog bejegyzés**

ARMv8, C++ Streams, 1.4.1 release, egyeztetési javaslatok s más hirek.

**io.js 1.4.1 Release**

Megjegyzés: Az 1.4.0 as verzió munka alatt állt de végül nem lett kiadva. 
libuv hibát fedeztünk fel, igy a folyamatot megszaktottunk s zavar elkerülése érdekében továbbléptunk az 1.4.1 -es verzióhoz. 

**Notable changes**

* **process / promises**: Az ’unhandledRejection’ event is now emitted on process whenever a Promise is rejected and no error handler is attached to the Promise within a turn of the event loop. A ‘rejectionHandled’ event is now emitted whenever a Promise was rejected and an error handler was attached to it later than after an event loop turn. [#758](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fpull%2F758&sa=D&sntz=1&usg=AFQjCNGrDsFkeWhkGJZSFWXgR2VezqDaGA) (Petka Antonov)
* **streams**: you can now use regular streams as an underlying socket for tls.connect() [#926](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fpull%2F926&sa=D&sntz=1&usg=AFQjCNHyImaayqtgEJ9BWLuSIBMEhbbdVA) (Fedor Indutny)
* **http**: A new ‘abort’ event emitted when a http.ClientRequest is aborted by the client. [#945](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fpull%2F945&sa=D&sntz=1&usg=AFQjCNGLuclBExooJFY2h3CkzrU-RRdUNg) (Evan Lucas)
* **V8**: Upgrade V8 to 4.1.0.21. Includes an embargoed fix, details should be available when embargo is lifted. A breaking ABI change has been held back from this upgrade, possibly to be included when io.js merges V8 4.2. See [#952](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fpull%2F952&sa=D&sntz=1&usg=AFQjCNHsYmLv-88p3W1SGOzIjBVr2czeLw) for discussion.
* **npm**: Upgrade npm to 2.6.0. Includes features to support the new registry and to prepare for npm@3. See [npm CHANGELOG.md](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fnpm%2Fnpm%2Fblob%2Fmaster%2FCHANGELOG.md%23v260-2015-02-12&sa=D&sntz=1&usg=AFQjCNHrI-F3UjduRZsYVUHWyjxgvOS7xA) for details. Summary:
* [**#5068**](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fnpm%2Fnpm%2Fissues%2F5068&sa=D&sntz=1&usg=AFQjCNEcepwnF10IfJnx_7XMNT8IxlGJKA) Add new logout command, and make it do something useful on both bearer-based and basic-based authed clients. [#6565](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fnpm%2Fnpm%2Fissues%2F6565&sa=D&sntz=1&usg=AFQjCNHzgjyXQFCTCakjSvFA7oRDzvnbaQ) Warn that peerDependency behavior is changing and add a note to the docs. [#7171](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fnpm%2Fnpm%2Fissues%2F7171&sa=D&sntz=1&usg=AFQjCNFWEjQLSUsXBV6p34n3DV6xMUUc7w) Warn that engineStrict in package.json will be going away in the next major version of npm (coming soon!)
* **libuv**: Upgrade to 1.4.2. See [libuv ChangeLog](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Flibuv%2Flibuv%2Fblob%2Fv1.x%2FChangeLog&sa=D&sntz=1&usg=AFQjCNF2i5H9Jl5mwm5a9MTkW-RKdV9eIQ) for details of fixes.

**Az ARM support-ot ajánlott az io.js nek ARMv8 -on**

Az ARM kapcsolatba lépett Rod Vagg-gal az io.js Build Working Group vezetőjével, és segtséget ajánlott fel a projecthez. Partnereikkel jó úton haladnak, hogy megalkossanak egy életképes ARMv8 server paltform-ot, ami tökéletes párost alkothatna egy gyors szerver-oldali JavaScript-tel.

Mióta a mobil-gyártó cégek használják az ARMv8-at, a V8 újabb verzióinak is jobb support-ja van. A V8 kulcsszerepet játszik az Android életében, s az io.js tökéletesen illeszkedhet a support követésében, és még közreműködhet az új kapcsolatok kialakitásában is a V8 csapattal.  

Rod az io.js project-et is beleértve kezdete óta támogatja az ARM szerepét kiegészitve az IoT-vel, hobby project-ekkel és a szerver oldali alkalmazásokkal. Példának okáért a Raspberry Pi release-nél ARMv6 build-eket hasunálunk és ARMv7 -et más népszerű termékeknél(beleértve az Online Labs ARM alapúcloud platrform-ját is, aki szintén biztositotta segitő szándékáról az io.js -t).  Ennek egy logikus kiterjesztése az ARMv8, de szintén izgalmas lehetőségek rejlenek a szerver oldali applikációkban is, különös tekintettel gondolunk itt az új 64-bit támogatásra. 

A csapat a engedélyeztetés folyamatában van az ARMv8 Server Cluster integráció illetően az io.js CI platform integrációval, aminek végül egy ARMv8 release -hez kellene vezetnie.

**Közösségi hirek**

* **[Egyeztetesi javaslat](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fissues%2F978&sa=D&sntz=1&usg=AFQjCNFOzJhQjoxhNT6dEqWkxPorR_FAhw)**: Az io.js projectet illetően tervet késztünk, amit elfogunk juttatni a Node Foundation -hoz. Ezért, minden a közösségtől érkező vélemenyt nagyon fontosnak tartunk ebben a korai fázisban, igy kérünk titeket, hogy adjatok teret a szavatoknak.

* **New internal C++ Streams API**: A heten [új C++ Stream API](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fcommit%2Fb9686233fc0be679d7ba1262b611711629ee334e&sa=D&sntz=1&usg=AFQjCNEPX_bRZxtSut1p1cIXOHFy8bCtQw) érkezett, ami segit az egyik TLS stream -et wrappolni egy másikba.

* **io.js Roadmap**: Ime a legújabb [Roadmap](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fblob%2Fv1.x%2FROADMAP.md&sa=D&sntz=1&usg=AFQjCNHOdPnRo8spNnU12bdSxun4oha2pA) az io.js jövőbeni terveit illetően. Helyet kap a stabilitás kérdését érintő szabályzat, valamint az azonnali teendők köre a project egészét érintve.

* **Roadmap slide-sor elkészült és fordtásra kész**: [Az io.js roadmap bemutató slide sorok véglegesek](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Froadmap%2Fissues%2F18&sa=D&sntz=1&usg=AFQjCNGHQtuHfkXLcZ1XUq98P_hMFlwNFw) és forditásra készek. Ha bárki úgy érzi, hogy készen áll egy prezentációra a saját közössége előtt, akkor jelezze ezt felénk bátran s segiteni fogunk az előkészületekben.

* **Microsoft io.js How-To for Azure Websites**: [A Microsoft kiadta az Azure platform -hoz tartozó oktató anyagot](http://www.google.com/url?q=http%3A%2F%2Fazure.microsoft.com%2Fen-us%2Fdocumentation%2Farticles%2Fweb-sites-nodejs-iojs%2F&sa=D&sntz=1&usg=AFQjCNHGw9YvP_ZWImfk64a4qdT63VGylg), ami segiti az io.js használatának elsajátitását az Azure platform-on. 

* **Floobits io.js -t használ**:  [A Floobits áttért io.js -re](https://news.floobits.com/2015/02/23/on-moving-to-io.js/), részben mert frusztráló volt számukra a node.js release ciklusainak lassúsága, beleértve a több ES6 feature -t a harmony flag szükségessége nélkül, illetve a nagyobb fejlődés hiányat a 0.10..0 és a 0.12.0 közt.

* **Anand Mani Sankar’s Node.js vs io.js: Mi oka a fork -nak?!?**: [Anand, irt egy többnyire objektiv véleményt az io.js eddigi történéseiről](http://www.google.com/url?q=http%3A%2F%2Fanandmanisankar.com%2Fposts%2Fnodejs-iojs-why-the-fork%2F%23.VO82hE60PVw.twitter&sa=D&sntz=1&usg=AFQjCNFIXWcCll74aHXBZeiUf1QolsGZ5w) és a jövőben célokról. Kifejezetten érdekes és ajánlott olvasmány mindenkinek aki nem elkötekezett az io.js irányában. 

* **iojs-jp - új japán io.js blog**: A japán io.js csoport egy létrehozott egy, saját nyelvű [allokált io.js -t érintő blogot](http://www.google.com/url?q=http%3A%2F%2Fblog.iojs.jp%2F&sa=D&sntz=1&usg=AFQjCNH2MvG-JqduDayGLYmWfc6p8qMLnA), annak érdekében, hogy még jobban tudják terjeszteni a közösség hirét.

* **iojs-cn - új kinai io.js blog**: Hasonlóan a japán io.js blog-oldalhoz, ez a csoport is [felállitott egy saját nyelvű oldalt](http://www.google.com/url?q=http%3A%2F%2Fcn.iojs.org%2F&sa=D&sntz=1&usg=AFQjCNH8xlZ0XzKsD7CrzbroHU5SV14PHQ), ahol a megtekinthetőek a hirek és az újdonságok az io.js-t illetően. 

* **[Roadmap slide-sor review](https://www.youtube.com/watch?v=etI_UD4wXlo)** - Áttekintésre került az io.js roadmap bemutató mielőtt szabadon szabadon lesz használható a csoportok által, ez rendkivül fontos volt abból a szempontból, hogy a project üzenete találkozzon az elvárásokkal.

**io.js támogatás elérhető**

* **[Wallby.js](http://www.google.com/url?q=http%3A%2F%2Fwallabyjs.com%2F&sa=D&sntz=1&usg=AFQjCNEMz30psv0ejZpAaJkvrrJwbe2gCQ)**, ez a testing JavaScript library elérte az 1.0 verziót és az io.js támogatottságot.

* **[jsdom](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Ftmpvar%2Fjsdom&sa=D&sntz=1&usg=AFQjCNH_Dit-bvVWStAIV-xoMEYeBchS0A)**, a WHATWG DOM és HTML standard -ek megvalósitója, elérte 4.0.0 verziót, ami az io.js elvárásoknak is eleget tesz.

* **[give](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fmmalecki%2Fgive&sa=D&sntz=1&usg=AFQjCNEtnJZKP-zG_mY8KEpoxnF2xVZbRA)** megalkotója nemrég közölte egy [tweet-ben](https://www.google.com/url?q=https%3A%2F%2Ftwitter.com%2Fmaciejmalecki%2Fstatus%2F569629100215816192&sa=D&sntz=1&usg=AFQjCNHzGZxe4YSrI2Q9ZLRRLTILrE95rQ), hogy az újabb give verziók io.js támogatással működnek majd. A give, egy git alapú node.js/io.js verzió követeő rendszer.

* A **Firebase Realtime Kliens**, a hivatalos web/node.js JavaScript kliens Firebase hez, nemrég közölte egy [tweet-ben](https://www.google.com/url?q=https%3A%2F%2Ftwitter.com%2FFirebaseRelease%2Fstatus%2F570000737343647744&sa=D&sntz=1&usg=AFQjCNHDLhmcl20SZuUBPZs_Kc9qCgvfSQ), hogy io.js támogatást biztosit a [2.2.1 verzióhoz](https://www.google.com/url?q=https%3A%2F%2Fwww.firebase.com%2Fdocs%2Fweb%2Fchangelog.html%23section-realtime-client&sa=D&sntz=1&usg=AFQjCNFcjv7E698eXaHV7nfRDSZKbUdTVw). 

* A continuous integrations szolgáltatást biztosito **Semaphore** egy [tweet -ben](https://www.google.com/url?q=https%3A%2F%2Ftwitter.com%2Fsemaphoreapp%2Fstatus%2F570987355005431809&sa=D&sntz=1&usg=AFQjCNFEsTUf27A6m0xU8eUcjPfMQyiJdg) jelezte a [2015 Február 24-i frissitést követően](https://www.google.com/url?q=https%3A%2F%2Fsemaphoreapp.com%2Fblog%2F2015%2F02%2F17%2Fplatform-update-on-february-24th.html%3Futm_source%3Dtwitter%26utm_medium%3Dsocial%26utm_content%3Dplatform_update_launch%26utm_campaign%3Dplatformupdate&sa=D&sntz=1&usg=AFQjCNHNa2lUgZaypv-7JPoHUBoBYPLVSQ) io.js támogatást biztositanak. 



