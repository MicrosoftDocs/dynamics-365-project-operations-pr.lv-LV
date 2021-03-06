---
title: Projekta piedāvājuma pamata koncepti
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu izmantošanu Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896290"
---
# <a name="project-quote-key-concepts"></a>Projekta piedāvājuma pamata koncepti

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_


Tālāk minēti galvenie jēdzieni, kas jāzina, pirms sākat lietot projekta piedāvājumus risinājumā Dynamics 365 Project Operations.

## <a name="contracting-unit"></a>Līgumslēdzēja vienība

Līgumslēdzēja vienība pārstāv struktūrvienību vai praksi, kurai pieder projekta nodrošinājums. Katrai līgumslēdzējai vienībai var iestatīt resursu izmaksas. Norādot resursu izmaksas resursam līgumslēdzēja vienībā, varat arī iestatīt dažādas izmaksu likmes resursiem, no kā šī līgumslēdzēja vienība aizņemas, vai cita veida struktūrvienības vai prakses uzņēmumā. Tās sauc par pārsūtīšanas cenām, resursu aizņēmumiem vai apmaiņas cenām. Kad iestatāt resursu aizņēmumu izmaksas no citām struktūrvienībām, varat arī izvēlēties iestatīt šīs izmaksu likmes aizdodošās struktūrvienības valūtā.

## <a name="cost-currency"></a>Izmaksu valūta

Izmaksu valūta risinājumā Project Operations ir valūta, kurā tiek ziņotas izmaksas. Šī valūta ir atvasināta no valūtas, kas ir piesaistīta laukam **Līgumslēdzēja vienība** piedāvājumā, līgumā un projektā. Izmaksas var reģistrēt jebkurā valūtā attiecībā pret projektu. Taču tiek veikta valūtas konvertēšana no valūtas, kurā tika ierakstītas izmaksas, uz projekta izmaksu valūtu.

CDS platformā valūtas kursam nevar būt spēkā esamības datuma, tāpēc laika gaitā ekrānā redzamās summas var mainīties, atjauninot valūtas maiņas kursus. Tomēr datubāzē ierakstītās izmaksas paliek nemainīgas, jo summas tiek glabātas valūtā, kādā tās radušās.

## <a name="sales-currency"></a>Pārdošanas valūta

Pārdošanas valūta risinājumā Project Operations ir valūta, kādā tiek reģistrētas un parādītas prognozētās un faktiskās pārdošanas summas. Tā ir arī valūta, kurā klientam tiek izrakstīts rēķins par darījumu. Projekta piedāvājumā pārdošanas valūtas noklusējuma vērtība tiek ņemta no klienta vai uzņēmuma ieraksta, un to var mainīt, kad tiek izveidots piedāvājums. Pēc tam, kad piedāvājums ir saglabāts, pārdošanas valūtu nevar mainīt. Produktu un projektu cenrāžu noklusējums tiek iestatīts, pamatojoties uz piedāvājuma pārdošanas valūtu.

Atšķirībā no izmaksām pārdošanas vērtības var reģistrēt tikai pārdošanas valūtā.

## <a name="billing-method"></a>Rēķinu izrakstīšanas metode

Projektiem parasti ir fiksēta maksa un uz patēriņu balstīti līgumu modeļi. Tas ir parādīts risinājumā Project Operations kā **Rēķinu izrakstīšanas metode**, un tai ir divas vērtības — laiks un materiāli un fiksēta cena.

- **Laiks un materiāli:** šis ir uz patēriņu balstīts līguma modelis, kurā visām radītajām izmaksām ir atbilstoši ieņēmumi. Aprēķinot vai radot vairāk izmaksu, palielinās arī aplēstais un faktiskais pārdošanas apjoms. Varat norādīt nepārsniedzamos ierobežojumus to piedāvājumu rindās, kam ir šī norēķinu metode. Tādējādi tiek iestatīta maksimālā robežvērtība faktiskajiem ieņēmumiem. Nepārsniedzamie ierobežojumi neietekmē prognozējamos ieņēmumus.
- **Fiksēta cena:** šis ir fiksētas maksas līguma modelis, kas norāda, ka pārdošanas vērtības ir neatkarīgas no izmaksām, kas radušās. Pārdošanas vērtība ir fiksēta un nemainās, aplēšot vai radot vairāk izmaksu.

## <a name="project-price-lists"></a>Projekta cenrāži

Projektu cenrāži ir cenrāži, kas tiek izmantoti cenu, nevis izmaksu likmju noklusējuma vērtību iestatīšanai laika, izdevumu un citos ar projektu saistītos komponentos. Var būt vairāki cenrāži, un katram no tiem var būt savs datums katram projekta piedāvājumam. Project Operations neatbalsta spēkā esamības datumu pārklāšanos projektu cenrāžos.

## <a name="product-price-lists"></a>Produktu cenrāži

Produktu cenrāži ir cenrāži, kas tiek izmantoti cenu, nevis izmaksu likmju noklusējuma vērtību iestatīšanai piedāvājuma produkta rindās. Katram piedāvājumam ir tikai viens produktu cenrādis.

## <a name="transaction-classes"></a>Transakciju klases

Project Operations atbalsta četru veidu transakciju klases:

- Laiks
- Izdevumi
- Materiāls
- Maksa

Izmaksu un pārdošanas vērtības var aprēķināt un radīt laika, izmaksu un materiālu transakciju klasēs. Maksa ir tikai ieņēmumu transakciju klase.

## <a name="work-entities-and-billing-entities"></a>Darba entītijas un norēķinu entītijas

Entītijas, kas atspoguļo darbu, ir Projekti un Uzdevumi. Entītijas, kas atspoguļo norēķinus, ir piedāvājuma rindas un līguma rindas. Varat saistīt dažādas darba entītijas ar norēķinu opcijām, saistot tās ar piedāvājuma vai līguma rindām.

## <a name="multi-customer-deals"></a>Vairāku klientu darījumi

Vairāku klientu darījumi rodas, ja rēķinā ir vairāk nekā viens klients. Tālāk ir norādīti visbiežāk sastopamie piemēri.

- **OEM uzņēmumi un to partneri:** partneri un tālākpārdevēji pārdod produktu ar pievienotās vērtības pakalpojumiem. Parasti tas ir scenārijs, kurā konkrēta darījuma laikā laikā ar klientu OEM piedāvā finansēt daļu projekta. 

- **Publiskā sektora projekti:** vairāki vietējās valdības departamenti vienojas par projekta finansēšanu, un tiem tiek izrakstīts rēķins atbilstoši iepriekš saskaņotam sadalījumam. Piemēram, skolas rajons un pilsēta vai vietējās pašvaldības departaments vienojas par peldbaseina būvniecības finansēšanu.

## <a name="invoice-schedules"></a>Rēķina izrakstīšanas grafiki

Rēķinu grafiki ir specifiski katrai piedāvājuma rindai un arī nav obligāti. Rēķinu grafiki ir izveidoti, pamatojoties uz noteiktiem sākuma un beigu datumiem un rēķina biežumu. Rēķinu grafiki tiek izmantoti līguma posmā, kad ir konfigurēts automātiskais rēķinu izveides process. Piedāvājuma posmā grafiki ir neobligāti. Ja rēķinu grafiki tiek izveidoti posmā **Piedāvājums**, tie tiek kopēti uz projekta līgumu, kas izveidots, kad projekta piedāvājums tiek iegūts.

## <a name="changes-from-dynamics-365-sales-quote"></a>Izmaiņas no Dynamics 365 Sales piedāvājuma:

Project Operations piedāvājumi ir izveidoti, izmantojot Dynamics 365 Sales piedāvājumus. Tomēr ir dažas būtiskas atšķirības funkcionalitātē, kas jāņem vērā.

- Darbības **Pārskatīt** un **Aktivizēt** netiek atbalstītas.
- Project Operations piedāvājumiem ir divi dažādi rindu tipi. Viens ir projektiem, bet otrs — produktiem.
- Project Operations piedāvājumiem ir savas veidlapas un lietotāja interfeisa elementi, biznesa kārtulas, biznesa loģika spraudņi, kā arī klienta puses skripti, kas atšķir tos no Sales piedāvājumiem.

Šo iemeslu dēļ nav ieteicams izmantot Sales piedāvājumu un Project Operations piedāvājumu pamīšus.
