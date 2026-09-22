---
{"dg-publish":true,"permalink":"/notes/par-spelu-izstradi/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"section":"[[Notes/1. Pulciņa nodarbība]]","tags":["note"],"created":"2026-09-14","cssclasses":null}}
---

[[Notes/1. Pulciņa nodarbība\|Atpakaļ]]

---
# Māksla + zinātne = spēļu izstrāde
## Kāpēc veidot datorspēles?
### Spēles veido, lai:
#### Mākslinieciski izpaustos
Spēļu izstrāde ir interaktīvs multimedijs, kas apvieno gandrīz visus radošos elementus, ko mēs mīlam citur:
- **Vizuālā māksla** (kā gleznās, dizainā un filmās)
- **Stāstniecība un scenāriji** (kā grāmatās)
- **Mūzika un skaņu dizains**
- **Lietotāja saskarne un interaktivitāte** (kā mājaslapās un lietotnēs)

Klāt arī nāk viss, kas veidojas šo elementu kombināciju dēļ, piemēram: 
- **Mūzika** + **stāstniecība** = emocionāls mirklis 
- **Skaņu dizains** + **vizuālā māksla** + **interaktivitāte** = patīkami lietojama izvēlne vai interfeiss
#### Iemācitos ko jaunu
Spēļu izstrāde ir ideāla vide, lai **eksperimentētu**,
Tā ir nemitīga **problēmu risināšana**.
##### Veidojot spēles, tu esi:
- **Fiziķis:** 
  Tev jāsaprot gravitācija, berze un paātrinājums, lai tēlu lēciens, bumbas atsitiens vai mašīnas vadāmība šķistu reālistiska.

- **Matemātiķis:** 
  Tu izmanto ģeometriju un vektorus, lai aprēķinātu lodes lidojuma trajektoriju, ienaidnieka redzeslauku vai varoņa kustības ātrumu.

- **Arhitekts un telpu plānotājs:** 
  Tu būvē virtuālās pasaules, veidojot līmeņu dizainu (_level design_), kur katram šķērslim un telpai ir savs mērķis, lai spēlētājs neapmaldītos, bet arī negarlaikotos.

- **Skaņu inženieris un komponists:** 
  Tu vāc, apstrādā vai komponē audio elementus. Soļu krakšķi, fona mūzika un saskarnes klikšķi ir tas, kas spēlei piedod atmosfēru un *dzīvību*. 
  Skaņai var arī būt prakstisks pielietojums - Tas ir viegli saskatāms spēlējot *Counter Strike 2* bez austiņām. 
  Spēlē *Overwatch*, ir iespējams atšķirt katru varoni pēc to soļošanas skaņām.

- **Režisors un rakstnieks:** 
  Tu izvēlies kameras skata punktus, raksti dialogu, veido tēlus ar personalitāti, modelē viņus un domā par to, cik informāciju sniegt spēlētājam, lai veicinātu intrigu.
  Prasmes, kuras noder stāstu veidošanai datorspēlēs līdzinās *Dungeons & Dragons* galvenā (*Dungeon Master*) prasmēm. Mācēt paredzēt, ko spelētājs gribētu darīt un veidot dinamisku stāstu, kas ir bāzēts spēlētāja veiktajās izvēlēs.

- **Psihologs:** 
  Tev jāsaprot cilvēka prāts - kas spēlētājam sagādā prieku, kā viņu apbalvot par pūlēm un kā sabalansēt spēles grūtību/sarežģītību, tā lai būtu izaicinoši, bet ne kaitinoši vai pārmērīgi sodoši.

- **Mārketinga speciālists:** 
  Spēle pati sevi nepārdos. Tev jāveido piesaistoši treileri un ekrānuzņēmumi, jākomunicē ar spēlētāju kopienu _Discord_ vai sociālajos tīklos un jāizdomā stratēģija, kā tavai spēlei izcelties _Steam_ vai _Itch.io_ platformās starp tūkstošiem citu.

- Protams, arī **Programmētājs:** 
  Tu pārvērt vizuālās un dizaina idejas reālā, strādājošā produktā. Veidojot spēles, tu praktiski (nevis sausā teorijā) apgūsti galvenās programmēšanas prasmes, kā piemēram:
	- **Datu tipus (_Data types_):** Kā pareizi glabāt spēlētāja vārdu (teksts), dzīvības punktus (vesels skaitlis) vai pārvietošanās ātrumu (daļskaitlis).
	- **Objektorientēto programmēšanu (OOP):** Tu saproti klases un objektus. Piemēram, tu uzraksti vienu "Ienaidnieka" klasi ar tās uzvedību, un tad spēlē ģenerē simtiem unikālu ienaidnieku, mantojot šīs īpašības.
	- **Atmiņas pārvaldību un optimizāciju:** Kad tava spēle nestrādā dēļ _Out of Memory_ (OOM) kļūdas, tu ātri iemācies, kāpēc nedrīkst ielādēt 4K tekstūras vai radīt jaunus objektus katrā datora kadrā, bet gan, ka tie ir jāpārstrādā (_Object pooling_).

#### Pelnītu naudu
Spēļu industrija šobrīd ir lielāka, nekā filmu un mūzikas industrijas kopā! 

- **Spēļu industrijas aptuvenā vērtība gadā:** $$ $184,000,000,000$$
- **Filmu Industrijas aptuvenā vērtība gadā:** $$ $34,000,000,000$$
- **Mūzikas industrijas aptuvenā vērtība gadā:** $$ $28,000,000,000$$
Tas var sākties kā interesants hobijs, bet pāraugt ienesīgā amatā lielā uzņēmumā (*[[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|AAA]]*) vai pat personīgajā biznesā, veidojot neatkarīgās (_indie_) spēles.
Pateicoties jaudīgiem un bezmaksas rīkiem (*Godot* būdams viens no tiem), šobrīd ir **visu laiku labākais brīdis** neatkarīgo (_indie_) spēļu izstrādei, taču vienlaikus ir arī **grūtāk, kā jebkad** tikt pamanītam un gūt peļņu.

**Priekšrocības: izstrāde un rīki**

- **Plaša pieejamība:** publiski pieejami spēļu dziņi, mācību video un viedā programmatūra padara spēles radīšanu vienkāršāku, kā jebkad.

- **Zems ienākšanas slieksnis:** individuāli izstrādātāji mūsdienās spēj radīt to, kam agrāk bija nepieciešama vesela studija un milzīgs finansējums.

- **Nišas auditorija:** spēlētāji aktīvi meklē unikālu un nestandarta spēļu pieredzi.

**Trūkumi: konkurence un pārdošana**

- **Tirgus pārsātinājums:** katru gadu _Steam_ platformā tiek publicētas desmitiem tūkstošu spēļu, tāpēc izcelties ir milzīgs izaicinājums.

- **Augstas prasības:** spēlētāji sagaida noslīpētas spēles bez kļūdām un ir gatavi rakstīt negatīvas atsauksmes pat par vissīkākajiem trūkumiem.

- **Finansiālais risks:** finansiāli panākumi joprojām ir retums, un, uztverot _indie_ spēļu izstrādi kā vieglu naudas avotu, nāksies vilties. 

Tomēr, neatkarīgiem izstrādātājiem ir viena galvenā priekšrocība pār *[[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|AAA]]* izstrādātājiem - **izmaksas ir mikroskopiskas**, salīdzinot ar uzņēmumiem, kas sadarbojas ar izdevējiem un uztur tūkstošiem kvalificētus cilvēkus.
Izveidojot spēli, kas neredz dienasgaismu, nekas īsti netiek zaudēts (vismaz 100 eiro, jo tik izmaksā publicējot spēli *Steam*). 
Un, ja tā tomēr redz dienasgaismu, Latvijas ekonomikā nopelnītā nauda ir daudz.

Jebkurš laiks ir piemērots, lai sāktu savu gaitu šajā nozarē, ja spēj saprātīgi **pārvaldīt riskus** un saglabā **reālistisku skatījumu** uz spēles apjomu. 
Publicējot spēli, vispirms izveido savu auditoriju un uzkrāj ievērojamu *Steam* vēlmju saraksta (_wishlist_) bāzi, un tikai tad apsver pamatdarba pamešanu.
#### Tērētu laiku
Spēļu izstrāde aizņem ārkārtīgi ilgu laiku. 
##### Laika formula
Lai izvērtētu projekta tvērumu, noder sekojošā formula: 
$$(T_{plānotais} \times 2) \xrightarrow{\style{font-family: 'Times New Roman', serif;}{\text{Nākamā mērvienība}}}T_{reālais}$$

Ja uzsākot projektu, šķiet ka tas aizņems **2 nedēļas**: 
$$T_{plānotais} = 2ned$$

Tad patiesībā, izmantojot formulu:
$$(2ned \times 2) \xrightarrow{\style{font-family: 'Times New Roman', serif;}{\text{Nākamā mērvienība}}} 4mēn$$

Redzam, ka projekta izstrāde patiesībā aizņems **4 mēnešus** 
$$2ned \xrightarrow{\text{formula}} 4mēn$$

##### Projekta plānošana
Lielā laika mēroga dēļ, projekta plānošanas prasmes ir ļoti noderīgas. Izstrādājot datorspēles, iemācīsies:
- Noteikt sasniedzamu projekta tvērumu
- Dokumentēt projektu un produktu
- Pielietot projekta plānošanas rīkus
- Ievietot komentārus programmas kodā
- Strādāt ar komandu
	- Pārvaldīt cilvēkresursus
	- Izmantot GitHub ar vairākiem līdzstrādniekiem (*contributors*)
- Pabeigt projektus un tos uzturēt

#### Izbaudītu procesu
Gala rezultāts ir svarīgs, taču ceļš līdz tam sniedz milzīgu prieku. 
Manuprāt, spēļu izstrāde ir **visinteresantākais** veids kā iemācīties programmēt, jo ir uzreiz jūtams veiktais darbs, un programmēšanas labās prakses neievērošana ir ārkārtīgi viegli izjūtama kad viss brūk un neiet.
Redzēt, kā sevis veidots tēls atdzīvojas un projekta sākumā tukšais ekrāns lēnām tiek aizpildīts ar manuāli radītām entītijām pārspēj visu citu. 
Cerams, ka šis pulciņš spēs radīt to sajūtu kādā citā.

### Kāpēc TU gribi veidot datorspēles?
#### Atbildi uz jautājumiem:
##### 1. Vai ceri ar to pelnīt naudu?
##### 2. Vai gribi lai tava spēle izceļās un gūst popularitāti?
##### 3. Vai vēlies veidot savu sapņu spēli vai mazus projektus? Ar ko tu sāktu?
##### 4. No kurām spēļu izstrādes daļām (piem. skaņas efekti, 3D modelēšana) noteikti gribi izvairīties?
##### 5. Vai labāk gribi būt *[[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|AAA]]* vai *indie* izstrādātājs?
## Kāpēc spēlēt datorspēles?
### **Uzdevums:** Atlasi galvenās īpašības:
#### 1. Izvēlies 1 spēli
#### 2. Izraksti visas īpašības šajā spēlē, kas, tavuprāt padara to aizraujošu (piem. animācijas, skaņas efekti)
#### 3. Sanumurē īpašības pēc to svarīguma tavas spēlēšanas baudas veicināšanai
#### 4. Atbildi uz jautājumiem:
##### 1. Vai izrakstītās galvenās īpašības tev bieži ir galvenās arī citās spēlēs?
##### 2. Vai gribētu nodarboties ar izrakstīto galveno īpašību veidošanu savās spēlēs?
##### 3. Kāpēc izrakstītās vismazāk svarīgās īpašības tavuprāt nav svarīgas? Vai tās ir māzāk svarīgas tieši tavā skatījumā vai spēles identitātē?

### Galveno īpašību noteikšana
#### Kā domāt kā spēļu dizainerim

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/clippings/game-maker-s-toolkit-how-to-think-like-a-game-designer/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




<a href="https://www.youtube.com/watch?v=iIOIT3dCy5w">
  <div style="border: 1px solid var(--background-modifier-border); padding: 10px; border-radius: 8px; text-align: center;">
    <strong style="display: block; margin-bottom: 8px;">How To Think Like A Game Designer</strong>
    <img src="https://www.youtube.com/img/desktop/yt_1200.png" style="width: 100%; border-radius: 4px;">
  </div>
</a>

</div></div>


Spēļu mehānikas bieži tiek mantotas un "nošpikotas", taču, bieži vien, šīs mehānikas ir labas tieši pārējās spēles kontekstā.
### [[Notes/MDA framework\|MDA framework]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/notes/mda-framework/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




# Materiāls
<iframe src="/img/user/Attachments/MDA_A_Formal_Approach_to_Game_Design_and_Game_Rese.pdf" width="100%" height="900px" title="MDA_A_Formal_Approach_to_Game_Design_and_Game_Rese.pdf" style="border:1px solid #ccc;"></iframe>

# MDA (Mechanics-Dynamics-Aesthetics)
## Definīcija
**MDA** ir spēļu dizaina un analīzes ietvars, kas sadala spēli trīs savstarpēji saistītos slāņos, lai izskaidrotu, kā spēles noteikumi ietekmē spēlētāja pieredzi.
Ietvaru 2004. gadā publicēja Robins Hunike (*Robin Hunicke*), Marks Leblāns (*Marc LeBlanc*) un Roberts Zubeks (*Robert Zubek*)

## Trīs MDA komponentes

- **Mehānika (Mechanics):** Tiešie spēles noteikumi, kodi, dati, cipari un darbības, ko spēlētājs var veikt (piemēram, cik daudz patronu ir ierocim vai cik augstu tēls var uzlēkt).

- **Dinamika (Dynamics):** Reāllaika uzvedība un sistēmas, kas rodas, kad spēlētājs mijiedarbojas ar mehāniku (piemēram, ienaidnieku slēpšanās vai agresīva uzbrukuma taktika).

- **Estētika (Aesthetics):** Emocionālā reakcija un **baudījums**, ko spēlētājs izjūt spēles laikā (piemēram, izaicinājums, atklāšanas prieks vai sasprindzinājums).

## Dizaineru un spēlētāju pretējais skatījums

- **Dizaineri** skatās uz spēli no apakšas uz augšu: viņi raksta **mehāniku**, kas rada **dinamiku**, kas savukārt izraisa **estētiku**.

- **Spēlētāji** pieredzi uztver no augšas uz apakšu: viņi vispirms izjūt **estētiku** (emocijas), tad pamana **dinamiku** un tikai tad apzinās pašas **mehānikas** noteikumus.

![Pasted image 20260917142418.png](/img/user/Attachments/Pasted%20image%2020260917142418.png)

## Astoņi estētikas veidi

MDA ietvars definē astoņas spēlētāju **baudījuma** kategorijas, aizstājot vispārējo vārdu "jautrība":

- **Sajūtas (Sensation):** Maņu baudījums (skaņas, vizuālais noformējums).
- **Fantāzija (Fantasy):** Izlikšanās citā pasaulē.
- **Stāsts (Narrative):** Piedalīšanās drāmā vai sižetā.
- **Izaicinājums (Challenge):** Grūtību pārvarēšana.
- **Kolektīvs (Fellowship):** Sociālā mijiedarbība un komandas darbs.
- **Atklāšana (Discovery):** Teritoriju un noslēpumu izpēte.
- **Pašizpausme (Expression):** Radošums un individuālais stils.
- **Pakļaušanās (Submission):** Hobijs, rutīna vai relaksācija.


</div></div>


Ne vienmēr mehānikās jautrība ir galvenais. Dažkārt likt spēlētājam justies **neērti**, atbilst dizainera vajadzībām vairāk. 
Kad gribi kautko pievienot, jautā:
- Vai šis **atbilst** manas spēles idejai? 
- Kā šis liktu **justies** spēlētājam? 
- Vai es gribu lai spēlētājs tā jūtās **šajā brīdī**?
- Vai mehānika **iederās** starp pārējām spēles funkcijām?
### [[Notes/Core Loop\|Core Loop]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/notes/core-loop/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




---
# Video materiāls

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/clippings/andrew-chambers-you-re-making-game-development-too-hard/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




<a href="https://www.youtube.com/watch?v=kJyvnMFYTQw">
  <div style="border: 1px solid var(--background-modifier-border); padding: 10px; border-radius: 8px; text-align: center;">
    <strong style="display: block; margin-bottom: 8px;">You're Making Game Development Too Hard</strong>
    <img src="https://i.ytimg.com/vi/kJyvnMFYTQw/maxresdefault.jpg" style="width: 100%; border-radius: 4px;">
  </div>
</a>

</div></div>


---

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/clippings/roblox-learn-what-s-a-core-loop-on-roblox/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




<a href="https://www.youtube.com/watch?v=gkFKF9A-snY">
  <div style="border: 1px solid var(--background-modifier-border); padding: 10px; border-radius: 8px; text-align: center;">
    <strong style="display: block; margin-bottom: 8px;">What's a core loop on Roblox?</strong>
    <img src="https://i.ytimg.com/vi/gkFKF9A-snY/maxresdefault.jpg" style="width: 100%; border-radius: 4px;">
  </div>
</a>


</div></div>


---
# Definīcija
**Core Loop** jeb **Core Gameplay Loop** jeb **Pamata Cikls** ir spēles bāze.
Tas ir baudāmu darību cikls, kuru spēlētājs atkārtoti pilda, to var darīt atkal un atkal ar nelielām variācijām, **nenogurstot**. Tajā parasti ietilpst visas spēles mehānikas, vai to pildot spēlētājam ir pieejamas visas spēles mehānikas. 
# Piemērs
**MMORPG** gadījumā, tas būtu:
- Izpildīt misiju
- Iegūt atlīdzību
- Iegūt jaunas spējas / uzlabot savu tēlu
- Doties grūtākā misijā

![Pasted image 20260917150735.png](/img/user/Attachments/Pasted%20image%2020260917150735.png)

Parasti, ciklā ir kāda sarežģīta darbība, atalgojums par to, kuru iztērējot, iegūstam mazu variāciju atkal pildot darbību un turpinot ciklu. 

</div></div>



### Analizē iepriekš izvēlēto spēli
#### Izveido tās **Core Loop**
#### Izvēlies vieno no tās mehānikām un apraksti tās **MDA framework**

