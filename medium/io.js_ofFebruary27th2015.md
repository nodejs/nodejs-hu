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


