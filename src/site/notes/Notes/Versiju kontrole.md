---
{"dg-publish":true,"permalink":"/notes/versiju-kontrole/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"section":"[[Notes/8. Pulciņa nodarbība]]","tags":["note"],"created":"2026-10-13","cssclasses":null}}
---

[[Notes/8. Pulciņa nodarbība\|Atpakaļ]]

---
# [Uzliec lādēties!](https://desktop.github.com/download/)

# Kas ir versiju kontrole?
## Definīcijas
### Versiju pārvaldības sistēma
> **Versiju pārvaldības sistēma** (VPS) ir programmatūras rīks, kas palīdz organizēt kādas mainīgas informācijas vienības evolucionāru attīstību. Kā informācijas vienība var būt programmatūras [pirmkods](https://lv.wikipedia.org/wiki/Pirmkods "Pirmkods"), elektroniski dokumenti, grāmatas. 

> VPS tiek uzglabātas dažādas dokumentu versijas. Ja ir nepieciešamība, var atgriezties pie agrākām versijām. 

> VPS visbiežāk pielieto darbam komandā, kad vairāki izstrādātāji var rediģēt vienu un to pašu dokumentu.

### Repozitorijs
> **Repozitorijs** ([angļu](https://lv.wikipedia.org/wiki/Angļu_valoda "Angļu valoda"): _repository_) ir vieta, kur tiek glabāts un pārvaldīts [programmatūras](https://lv.wikipedia.org/wiki/Programmatūra "Programmatūra") kods, faili vai cita veida dati, kas saistīti ar projekta izstrādi. Tas parasti tiek izmantots [versiju kontroles sistēmās](https://lv.wikipedia.org/wiki/Versiju_kontroles_sistēma "Versiju kontroles sistēma"), lai saglabātu visu izmaiņu vēsturi un ļautu komandai strādāt pie viena projekta vienlaikus.

> Izmantojot versiju kontroli, ir iespējams atgriezties pie jebkuras iepriekšējās faila versijas, pārskatīt izmaiņas un saprast, kurš tās veicis. Repozitoriji atbalsta darbu ar dažādām projekta versijām, izveidojot atzaru jeb _branch_. 
> Tas ir noderīgi, ja ir vēlme testēt jaunas funkcijas, nebojājot galveno projekta versiju. Katrs, kas klonē repozitoriju no servera, saņem pilnu tā kopiju, ieskaitot visu failu vēsturi un atzarus. Ja divi cilvēki vienlaikus veic izmaiņas vienā failā, versiju kontrole palīdz atrisināt konfliktus, apvienojot izmaiņas vai izvēloties prioritāru versiju.

> Repozitoriji, piemēram, _[GitHub](https://lv.wikipedia.org/wiki/GitHub "GitHub")_, ir veicinājuši milzīgu atvērtā koda projektu izplatību. Izstrādātāji no visas pasaules var sadarboties, izmantojot vienu un to pašu koda bāzi.

### Git
_**Git**_ ir [sadalīta versiju kontroles sistēma](https://lv.wikipedia.org/wiki/Sadalīta_versiju_kontroles_sistēma?action=edit&redlink=1 "Sadalīta versiju kontroles sistēma (vēl nav uzrakstīts)") ar uzsvaru uz ātrdarbību. _Git_ sākotnēji izplānoja un izstrādāja [Līnuss Tūrvaldss](https://lv.wikipedia.org/wiki/Līnuss_Tūrvaldss "Līnuss Tūrvaldss") [_Linux_ kodola](https://lv.wikipedia.org/wiki/Linux_kodols "Linux kodols") izstrādei. Katrs _Git_ jeb repozitorijs ietver pilnu izmaiņu vēsturi un nodrošina vadības iespējas, neatkarīgi no tīkla savienojuma pieejamības vai centrālā servera.

### GitHub
_**GitHub**_ ir tīmeklī balstīts *GIT* repozitoriju mitināšanas (*hosting*) pakalpojums.

_GitHub_ [[Notes/Versiju kontrole#Repozitorijs\|repozitoriji]] var būt publiski pieejami vai privāti, taču daudzas funkcionalitātes ir ierobežotas privāti uzturot repozitoriju.

$$
Git ≠ GitHub
$$
## Ko izmanto spēļu izstrādē?
### [[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|AAA]] spēles
<a href="https://www.perforce.com/products/p4" style="display: inline-block; border: 1px solid var(--background-modifier-border); padding: 8px; border-radius: 8px; text-align: center; text-decoration: none; color: inherit; max-width: 500px;"><strong style="display: block; margin-bottom: 5px; font-size: 0.9em; line-height: 1.2;">Perforce P4: Version Control that Scales With Your Team</strong><img src="https://www.perforce.com/sites/default/files/image-social-share-default.jpg" style="width: 100%; border-radius: 4px; display: block; margin: 0 auto;"></a>
### [[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|Indie]] spēlēs
[GitLab](https://about.gitlab.com/), [GitHub](https://github.com/), [Gitea](https://about.gitea.com/).

## Kāpēc izmantot versiju kontroli?
### Saistība ar tvērumu
> Jo lielāks projekts, jo lielāka nepieciešamība ieviest versiju kontroli

$$
NeedForGit ≡ ProjectScope
$$
### Programmējot vienam
Dažkārt, kad veic izmaiņas, saproti, ka tomēr izdarīji kautko labāk vecākā faila versijā. Bez versiju kontroles, viss ir zaudēts. Ar Git, vari apskatīt visas vecās faila versijas un atrast koda fragmentu, kuru vajadzēja atstāt.

### Programmējot komandā
Versiju kontrole ir vienīgais veids kā strādāt kopā. Pieņemsim, ka divatā strādājot, abi programmētāji ir mainījuši vienu un to pašu funkciju. Ar Git, būtu pieejama vecā versija, un katra programmētāja izmaiņas, šādi, koda apvienošana ir visvienkāršākā. Bez versiju kontroles, ir zaudēta vecā versija, un eksistē tikai pēdējā modificētā funkcija.
## Kā izmantot Git?
### Git
Lai saprastu galvenās funkcijas, noder šis špikeris:
![downloadgram.org_639782681_18565978420047114_2407949020572382972_n.jpg](/img/user/Attachments/downloadgram.org_639782681_18565978420047114_2407949020572382972_n.jpg)
### GitHub
1. Ej uz https://github.com/ un uztaisi profilu (ja tāds vēl nav)
2. Uzsāc jaunu *Godot* projektu, iespējojot `version control metadata`
    ![Pasted image 20261013142209.png](/img/user/Attachments/Pasted%20image%2020261013142209.png)
3. Atver instalēto [GitHub Desktop](https://desktop.github.com/download/) aplikāciju
4. Ieej savā profilā
5. Atver izveidotā *Godot* projekta mapi izmantojot aplikācijas `New repository` funkciju zem **File** vai izmanto `Ctrl + N`
6. Ievadi datus un `Local path` norādi izveidotā **Godot** projekta lokāciju, `Name` norādi **Godot** projekta nosaukumu.
   ![Pasted image 20261013142647.png](/img/user/Attachments/Pasted%20image%2020261013142647.png)
7. Tagad, veicot izmaiņas **Godot** projektā, redzamas veiktās izmaiņas aplikācijā. Izveido vienu mezglu, un paskaties vai tas uzrādās pie izmaiņām.
  ![Pasted image 20261013143155.png](/img/user/Attachments/Pasted%20image%2020261013143155.png)
8. Tagad, mums ir lokāla versiju kontrole. Lai publicētu šo projektu un pataisītu to globāli pieejamu ikvienam, spied **Publish repository**, pēc tam izvēlies nosaukumu un izslēds `Keep this code private`.
   ![Pasted image 20261013143614.png](/img/user/Attachments/Pasted%20image%2020261013143614.png)
9. Tagad šis repozitorijs ir publicēts internetā!
   ![Pasted image 20261013143826.png](/img/user/Attachments/Pasted%20image%2020261013143826.png)
