**io.js 2015 Február 13-i bejegyzés**

Szó lesz többek között a 29, különböző nyelven működő csoportjainkkról, 1.2.0 release-ről, és még sok minden másról. 

**io.js támogatás elérhető már…**

* [Postmark](http://www.google.com/url?q=http%3A%2F%2Fblog.postmarkapp.com%2Fpost%2F110829734198%2Fits-official-were-getting-cozy-with-node-js&sa=D&sntz=1&usg=AFQjCNEOW8WRfuK896Cc77GDiE6Ap4DNXA)

* [node-serialport](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fvoodootikigod%2Fnode-serialport%2Fissues%2F439&sa=D&sntz=1&usg=AFQjCNETU24uk0pum_geBcYbKa6EmWQJXA)

* [Microsoft Azure](http://www.google.com/url?q=http%3A%2F%2Fazure.microsoft.com%2Fen-us%2Fdocumentation%2Farticles%2Fweb-sites-nodejs-iojs%2F&sa=D&sntz=1&usg=AFQjCNHGw9YvP_ZWImfk64a4qdT63VGylg)

**GitHub-on már meghaladtuk a 10.000-res …………………….??**

Február 13-án, elértük a célunkat s átléptük a 10.000 -res …………………………………??? határt GitHub-on. 

Természetesen ezt csak a mögöttünk álló hatalmas támgatásnak köszönhetjük, amit a JavaScript közösség biztostani tud. Köszönjük mindenkinek a segtséget!!!!

**io.js 1.2.0 release**

* **stream**: [Egyszerűbb stream szerkesztés](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Freadable-stream%2Fissues%2F102&sa=D&sntz=1&usg=AFQjCNFKNLzMqrM5Ix1ZXuWSnOEJX4Ei6w).
* **dns**: lookup() [now supports an ‘all’ boolean option, default to false but when turned on will cause the method to return an array of all resolved names for an address](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fpull%2F744&sa=D&sntz=1&usg=AFQjCNGXM0lAz9jOOCN_f7QvySBHBwqIHw).
* **assert**: Remove prototype property comparison in [deepEqual()](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fpull%2F636&sa=D&sntz=1&usg=AFQjCNGcQM34_-TsHWPW63ZJ1O_oJfq63Q) introduced a deepStrictEqual() method to mirror [deepEqual()](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fpull%2F639&sa=D&sntz=1&usg=AFQjCNESFRODORTjvXkzGVmXJu44A2IRVg) but performs strict equality checks on primitives.
* **tracing**: [Add LTTng (Linux Trace Toolkit Next Generation) when compiled with the —with-lttng option. Trace points match those available for DTrace and ETW](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fio.js%2Fpull%2F702&sa=D&sntz=1&usg=AFQjCNHQfN3Z-WvsUmhsoQcQm1uNHqdzWA).
* **docs**: Sok az frissités a dokumentációban, lásd a commit-okat ; új [Errors page](https://www.google.com/url?q=https%3A%2F%2Fiojs.org%2Fapi%2Ferrors.html&sa=D&sntz=1&usg=AFQjCNHzEqvLiG19-mobBNpr5T52C2wfvg) discussing JavaScript errors, V8 specifikációk, és io.js specifikus hibák.
* **npm** frissités 2.5.1 -re
* **libuv** frissités 1.4.0, -re lásd libuv [ChangeLog](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Flibuv%2Flibuv%2Fblob%2Fv1.x%2FChangeLog&sa=D&sntz=1&usg=AFQjCNF2i5H9Jl5mwm5a9MTkW-RKdV9eIQ)
* **Új társak csatlakoztak a csapathoz**: Aleksey Smolenchuk ([@lxe](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Flxe&sa=D&sntz=1&usg=AFQjCNHrczPUb1fhdGs6IiYcKA04Ovqo7A)) és Shigeki Ohtsu ([@shigeki](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fshigeki&sa=D&sntz=1&usg=AFQjCNHEMExmtixmukjEwK_i8RmSF5fyoQ))

**Megkezdődtek a nemzetközi csoportok szerveződései is**

Lásd az eredeti [Medium]( https://www.google.com/url?q=https%3A%2F%2Fmedium.com%2F%40mikeal%2Fhow-io-js-built-a-146-person-27-language-localization-effort-in-one-day-65e5b1c49a62&sa=D&sntz=1&usg=AFQjCNEOO7zfmuqUgLr9qrd0ypRORlyb_g) cikket.

* Új kontributorok bukkantak fel, s közösségek szerveződnek, saját nyelven
* A csapatok regisztráltan vannak jelen Twitteren s minden más releváns közösségi fórumon 
* Minden csapat a saját tempójában tud dolgozni, közösséget éptve, túllépve a sablonos, fordtói szerepkörökön,

**Érdekes statisztika**

* Első nap 146 -an jelentkeztek támogatóként (jelen pillanatban pedig meghaladjuk a 160 főt)
* 27, különböző nyelvű csoport lett regisztrálva az első nap (mára pedig meghaladtuk a 29-et)
Csoportjaink

* [iojs-bn](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fiojs-bn&sa=D&sntz=1&usg=AFQjCNGtvWdrdgB5Hr8-7JBiZGXKYEtjkQ) bengáli csoport

* [iojs-cn](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fiojs-cn&sa=D&sntz=1&usg=AFQjCNEMV5-XQDVpG62GdqkVgkypRdNrXA) kinai csoport 

* [iojs-cs](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fiojs-cs&sa=D&sntz=1&usg=AFQjCNHlocJU5S-orAJQyFPrsX1VL0WAUA) cseh csoport

* [iojs-da](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fiojs-da&sa=D&sntz=1&usg=AFQjCNHIUV7ABGMxZDLEbb08iIKFpHeVlA) dán csoport

* [iojs-de](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fiojs-de&sa=D&sntz=1&usg=AFQjCNF0Zrt_9iqHhSDtcLqN36au53zUmA) német csoport

* [iojs-el](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fiojs-el&sa=D&sntz=1&usg=AFQjCNH41HSNAzSQEVxSx6rxzRnA6-w-Cg) görög csoport

* [iojs-es](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fiojs-es&sa=D&sntz=1&usg=AFQjCNE_Ep5g54XUlbgV4tJsWLoo_4T9Hg) spanyol csoport

* [iojs-fa](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fiojs-fa&sa=D&sntz=1&usg=AFQjCNGnH1R1G8XDAKCr-7PTSImtMlR2vA) perzsa csoport

* [iojs-fi](https://github.com/iojs/iojs-fi) finn csoport

*  [iojs-fr](https://github.com/iojs/iojs-fr) francia csoport

* [iojs-he](https://github.com/iojs/iojs-he) héber csoport

* [iojs-hi](https://github.com/iojs/iojs-hi) hindi csoport

* [iojs-hu](https://github.com/iojs/iojs-hu) magyar csoport

* [iojs-id](https://github.com/iojs/iojs-id) indonéziai csoport

* [iojs-it](https://github.com/iojs/iojs-it) olasz csoport

* [iojs-ja](https://github.com/iojs/iojs-ja) japán csoport

* [iojs-ka](https://github.com/iojs/iojs-ka) grúz csoport

* [iojs-ko](https://github.com/iojs/iojs-ko) koreai csoport

* [iojs-mk](https://github.com/iojs/iojs-mk) macedón csoport

* [iojs-nl](https://github.com/iojs/iojs-nl) holland csoport

* [iojs-no](https://github.com/iojs/iojs-no) norvég csoport

* [iojs-pl](https://github.com/iojs/iojs-pl) lengyel csoport

* [iojs-pt](https://github.com/iojs/iojs-pt) portugál csoport

* [iojs-ro](https://github.com/iojs/iojs-ro) román csoport

* [iojs-ru](https://github.com/iojs/iojs-ru) orosz csoport

* [iojs-sv](https://github.com/iojs/iojs-sv) svéd csoport

* [iojs-tr](https://github.com/iojs/iojs-tr) török csoport

* [iojs-tw](https://github.com/iojs/iojs-tw) tajvani csoport

* [iojs-uk](https://github.com/iojs/iojs-uk) ukrán csoport

**io.js és node.js**

Lásd az eredeti [Medium](https://www.google.com/url?q=https%3A%2F%2Fmedium.com%2F%40iojs%2Fio-js-and-a-node-js-foundation-4e14699fb7be&sa=D&sntz=1&usg=AFQjCNERAE8Aj-loVu0vD6ox9uOfYsGI9A) cikket.

* Scott Hammond, a Joyent CEO-ja, megemlítette, hogy szívesen venné ha az io.js-t visszavezetnék node.js -be.

**Pár hónap alatt az io.js…**

* 23 aktiv alaptagra növelte a csapatát
* Rengeteg onműködő csoport alakult
* 29, különböző nyelvű csoportja van a világ számos területén
* Több kontributor van a project-ben, mint történte során a node.js-nek 
* Az erős support-nak, és a kivételes közösségnek köszönhetően magas minőségűek és gyorsak release-k 

Mindezt szivesen magunk mögött hagyjuk, de nem akarjuk feláldozni a fejlődést és a önállőságot ami idáig juttatott minket.

**A jövő**

* Megbeszélések a node.js közösségel folyamatban vannak.
* Ha egyszer megegyezünk egy közös irányban az io.js-t illetően, arról mindenféleképpen értesülni fogtok GitHub -on. Ennek az iránynak az elfogadásában mindenki kiveheti a szerepét, mivel egy nyitott szavazással lesz eldöntve a következő lépés.

Nem fogunk megváltozni.

**Amivel segiteni tudsz minket**

* Folyamatosan küldj pull request-eket io.js -szel kapcsolatban
* Csatlakozz a [27 különböző nyelven dolgozó csoportunk egyikéhez](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fwebsite%2Fissues%2F125&sa=D&sntz=1&usg=AFQjCNF-pgq55qCCaMQ_ddooBd2SLXqJhw)
* Dolgozz velünk a különböző io.js csoportokban ([streams](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Freadable-stream&sa=D&sntz=1&usg=AFQjCNEwG2qLNS-zSKnh8mX6oL2lodw0pg), [website](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fwebsite&sa=D&sntz=1&usg=AFQjCNFo_qfRgQn2n7QeFrSqRfQDk3OLyg), [evangelism](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fwebsite%2Flabels%2Fevangelism&sa=D&sntz=1&usg=AFQjCNG1bDRjAzwsFFSUsyW6do1t3tYqdQ),[tracing](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Ftracing-wg&sa=D&sntz=1&usg=AFQjCNEBuewrstHcB_lgMMz6__oc2q1nZQ), [build](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Fbuild&sa=D&sntz=1&usg=AFQjCNF-aUDkwv1lZVmFlUGFLxmz7t-e0A),[roadmap](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fiojs%2Froadmap&sa=D&sntz=1&usg=AFQjCNGo1y1UiHc_5CmdL8JOUsAnLiGoXg)) és
* Alkalmazásaidban továbbra is használj io.js -t 

