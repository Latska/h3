# h3 Versionhallinta

 **z) Lue ja tiivistä artikkeli muutamalla ranskalaisella viivalla. Tässä z-alakohdassa ei tarvitse siis tehdä testejä tietokoneella.**
 
 **Commonmark contributors: Markdown Reference (huomaa ainakin otsikot risuaidoilla, kappalejako tyhjällä rivillä, sisennys (tab) koodia, lista, linkki, kuva.**
 
 * Markdown on helppo keino muotoilla tekstiä, jotta se näyttää hyvältä kaikilla laitteilla. Se ei tee mitään ylimääräistä, kuten muuta kirjasinkokoa, vaan pelkät olennaiset asiat.
 * Hyviä esimerkkejä markdownista:
 - *Italic* * *<- kursivoitu teksti
 - **bold** ** **<- lihavoitu teksti
 - # Heading #<- 1. otsikko
 - ## Heading ##<- 2. otsikko
 - [Link](http://google.com) [Link]<- Linkki
 - ![Image](https://commonmark.org/help/images/favicon.png) ![Image]<- Kuva
 - `-/*` <- Lista
 - `Inline codings` <- inline code 
 
 


**a) MarkDown. Tee tämän tehtävän raportti MarkDownina. Helpointa on tehdä raportti GitHub-varastoon, jolloin md-päätteiset tiedostot muotoillaan automaattisesti. Tyhjä rivi tekee kappalejaon, risuaita ‘#’ tekee otsikon, sisennys merkitsee koodinpätkän.**

Aluksi teemme uuden repositoryn Githubiin:
![Image](https://i.imgur.com/MOCU1VN.png)
"kloonataan" äsken luotu repository Githubista (Linkin saa Code -valikosta)
~$ git clone git@github.com:Latska/h3.git

Liikutaan kloonattuun arkistoon:
~$ cd h3/cd 

Tehdään tämä kyseinen raportti MarkDownina:
~$ sudo nano h3versionhallinta.md 
![Image](https://i.imgur.com/eLLkIN1.png)




**b) Pull first. Tee useita muutoksia git-varastoosi. Tee muutama muutos, jossa yksi commit koskee useampaa tiedostoa. Anna hyvä kuvaukset (commit message), yksi englanninkielinen lause imperatiivissa (määräysmuodossa) "Add top level menu to Foobar synchronizer"**

**b) Kaikki kirjataan. Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.**

**c) Huppis! Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset --hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.**

**d) Formula. Tee uusi salt-tila (formula, moduli, infraa koodina). (Eli uusi tiedosto esim. /srv/salt/terontila/init.sls). Voit tehdä ihan yksinkertaisen parin funktion (pkg, file...) tilan, tai edistyneemmin asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman. Käytä tarvittaessa ‘find -printf “%T+ %p\n”|sort’ löytääksesi uudet asetustiedostot.**

**f) Vapaaehtoinen: Laita srv/salt/ gittiin. Tee uusi moduli. Kloonaa varastosi toiselle koneelle (tai poista srv/salt ja palauta se kloonaamalla) ja jatka sillä.**

**e) Vapaaehtoinen: Omaa koiranruokaa. Säädä jotain käyttämääsi konetta Saltilla.**

