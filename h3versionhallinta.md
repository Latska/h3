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

~/h3$ sudo nano h3versionhallinta.md 

![Image](https://i.imgur.com/eLLkIN1.png)

Lisätään raporttitiedosto "alueelle":

~/h3$ git add h3versionhallinta.md 

Commit -komennolla ns. vahvistetaan/kerrotaan tehdyt muutokset
~/h3$ git commit

![Image](https://i.imgur.com/3tsCYpD.png)

Pull & push -komennoilla saadaan vietyä muutokset repositoryyn:

~/h3$ git pull

~/h3$ git push\
Counting objects: 3, done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 298 bytes | 33.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:Latska/h3.git
   7696b3a..6d27ca4  main -> main



**b) Pull first. Tee useita muutoksia git-varastoosi. Tee muutama muutos, jossa yksi commit koskee useampaa tiedostoa. Anna hyvä kuvaukset (commit message), yksi englanninkielinen lause imperatiivissa (määräysmuodossa) "Add top level menu to Foobar synchronizer"**

Tehdään muutoksia varastoon (lisätään parit tiedostot) 

![image](https://user-images.githubusercontent.com/103587811/164225585-a3e9432f-8be7-4657-bcf5-6ba5d7de3672.png)

~/h3$ git add README.md 

~/h3$ git add h3ipsum.md 

~/h3$ git add h3testings.md 


Commit message:

![image](https://user-images.githubusercontent.com/103587811/164225842-b8470efb-a07f-4034-aa60-642e0c2bf025.png)

Pull&push:

~/h3$ git pull

~/h3$ git push


**b) Kaikki kirjataan. Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.**

Git log-komennolla saadaan näkyviin tehtyjen muutosten "historia":

![image](https://user-images.githubusercontent.com/103587811/164227184-2af853b2-e72e-4c1a-8b00-670212ecfad2.png)

git diff cached checks

Git blame-komento kertoo, että kuka on muutoksen tehnyt ja milloin:
![image](https://user-images.githubusercontent.com/103587811/164229473-0f322641-dac9-48cc-b68d-5968a5fa09fc.png)





**c) Huppis! Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset --hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.**

Tehdään tyhmiä muutoksia tähän kyseiseen raporttiin:\
~/h3$ nano h3versionhallinta.md\ 
~/h3$ git add h3versionhallinta.md\
Tarkistetaan, että muutokset ovat menneet läpi:\
~/h3$ nano h3versionhallinta.md\
Tuhotaan tyhmät muutokset resetillä:\
~/h3$ git reset --hard\
HEAD is now at e6ee3d9 Update h3versionhallinta.md\
Ja varmistetaan vielä, että muutokset on tuhottu:
~/h3$ nano h3versionhallinta.md \


**d) Formula. Tee uusi salt-tila (formula, moduli, infraa koodina). (Eli uusi tiedosto esim. /srv/salt/terontila/init.sls). Voit tehdä ihan yksinkertaisen parin funktion (pkg, file...) tilan, tai edistyneemmin asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman. Käytä tarvittaessa ‘find -printf “%T+ %p\n”|sort’ löytääksesi uudet asetustiedostot.**

**f) Vapaaehtoinen: Laita srv/salt/ gittiin. Tee uusi moduli. Kloonaa varastosi toiselle koneelle (tai poista srv/salt ja palauta se kloonaamalla) ja jatka sillä.**

**e) Vapaaehtoinen: Omaa koiranruokaa. Säädä jotain käyttämääsi konetta Saltilla.**

