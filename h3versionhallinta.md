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

Aloitetaan teemällä uusi kansio 'squid':
![image](https://user-images.githubusercontent.com/103587811/168426937-ad05f878-85b7-4e0b-9f5e-7025bfb39320.png)

Squid on avoimen lähdekoodin proxy server (välityspalvelin?), jolla voi kikkailla kaiken näköistä. Ajattelin hyödyntää tätä myöhemmin H7 -loppuprojektissa:

Luodaan tilafunktio:
![image](https://user-images.githubusercontent.com/103587811/168427021-8c05af05-3e66-4351-92e7-991c3b768f09.png)

Ja ajetaan:
![image](https://user-images.githubusercontent.com/103587811/168427077-59ff9cf9-4b86-4fde-9ae4-790db0c89c53.png)

Testataan vielä onko idempotentti:

![image](https://user-images.githubusercontent.com/103587811/168427084-f1d18eb2-e270-4e51-b0e6-519f4a9faa99.png)

Lisätään vielä service.running -funktio, joka määrittää, että squid käynnistyy, mikäli se ei ole käynnissä.
![image](https://user-images.githubusercontent.com/103587811/168427262-4e3bba22-466d-4607-85b6-9e8878dadb41.png)

Ja vielä viimeinen testi:
![image](https://user-images.githubusercontent.com/103587811/168427541-2350337d-d6b8-48df-ae48-513d8c1ef23f.png)

Näyttäisi toimivan, tästä on hyvä jatkaa.






**f) Vapaaehtoinen: Laita srv/salt/ gittiin. Tee uusi moduli. Kloonaa varastosi toiselle koneelle (tai poista srv/salt ja palauta se kloonaamalla) ja jatka sillä.**

**e) Vapaaehtoinen: Omaa koiranruokaa. Säädä jotain käyttämääsi konetta Saltilla.**


Lähteet:

Tero Karvinen - Configuration management systems 2022
https://terokarvinen.com/2021/configuration-management-systems-2022-spring/

Tero Karvinen - Publish Your Project with GitHub
https://terokarvinen.com/2016/publish-your-project-with-github/?fromSearch=git

CommonMark
https://commonmark.org/help/

Salt Stack docs
https://salt-zh.readthedocs.io/en/latest/ref/states/all/salt.states.service.html

Squid Proxy installation:
www.squid-cache.org

