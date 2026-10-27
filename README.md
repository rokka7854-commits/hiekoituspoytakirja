# Hiekoituspöytäkirja

Suomenkielinen PWA: pysyvät tarkastuskohteet, kierroskohtaiset hiekoitushavainnot, Suomen ajassa näkyvät havaintoajat, valinnainen kuva, tarkastajan nimi ja koko kierroksen allekirjoitus. Ei palvelinpuolta eikä ulkoisia riippuvuuksia.

## Käyttö
1. Lisää kohteet. Valitse kullekin Hiekoitettu / Ei hiekoitettu. Aika tulee automaattisesti; sitä voi korjata. Lisää kuva halutessasi.
2. Kirjoita tarkastajan nimi ja allekirjoita kierros.
3. Luo PDF. Tarkista esikatselu ja tallenna tai jaa tiedosto.
4. Aloita uusi kierros. Vahvistettu tyhjennys säilyttää vain kohteet. Raportin luominen tai jakaminen ei koskaan tyhjennä tietoja.

Valikosta saa JSON-varmuuskopion, palautuksen ja tyhjennyksen. Tiedot ovat vain nykyisen selaimen IndexedDB-tallennuksessa. Muut laitteet tai eri verkko-osoitteet eivät näe niitä. Varmuuskopio sisältää myös kuvat ja allekirjoituksen. Varmuuskopion palautus korvaa nykyiset tiedot vahvistuksen jälkeen. Sovellus ei arkistoi vanhoja raportteja. PDF on paikallisesti tuotettu kuvapohjainen tiedosto, joten tekstiä ei voi valita tai hakea; ääkköset näkyvät selaimen fontilla. Aikaleima perustuu laitteen kelloon, ei varmennettuun aikapalveluun. Syksyn kahdesti esiintyvä käsin syötetty kellonaika tulkitaan talviajan mukaan.

## Asennus ja offline
Julkaise HTTPS-osoitteessa. Android: selaimen valikko → Asenna sovellus. iPhone: Safari → Jaa → Lisää Koti-valikkoon. Offline toimii ensimmäisen onnistuneen verkkolatauksen ja service workerin asennuksen jälkeen. Pelkkä HTML-tiedosto paikallisesti avattuna ei tue PWA-asennusta. Testaa varsinainen PDF-jakaminen omalla puhelimella.

## GitHub Pages
Kopioi dist-kansion sisältö uuden repositorion juureen. Lisää myös tämä README. Valitse Settings → Pages → Deploy from a branch → main / (root). Kaikki polut ovat suhteellisia, myös repositorion alihakemistossa. Sovellus: https://rokka7854-commits.github.io/hiekoituspoytakirja/

## Kehitys
Buildless HTML/CSS/JavaScript; ei asennettavia riippuvuuksia. `dist/index.html` sisältää sovelluksen. Service workerin välimuistiversio päivitetään julkaistaessa muuttunut sovellus. Tarkastajan piirretty allekirjoitus on kuittaus, ei vahva sähköinen allekirjoitus.
