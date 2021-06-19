---
title: Iestatīt darba rēķinu likmes — Lite
description: Šajā tēmā ir sniegta informācija par darba norēķinu likmju iestatīšanu risinājumā Project Operations.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 26c3743283dd9032e044071b3127a2885ad5ae49
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004270"
---
# <a name="set-up-labor-bill-rates---lite"></a>Iestatīt darba rēķinu likmes — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Katram cenrādim ir lomu cenu kopa vai darba likmes, kas ir spēkā kontekstam un datumu efektivitātei, kas iekļauta cenrāža galvenē. Rēķinu kursus laika intervālam programmā Dynamics 365 Project Operations var iestatīt tikai vienā valūtā, kas ir valūta cenrāža galvenē.

1. Lai pārdošanas cenrādim iestatītu darba laika likmes, izveidojiet cenrādi, pamatojoties uz cenrāža galveni. 
2. Cilnes **Lomas cenas** apakšrežģī atlasiet **+ Jauna lomas cena**. 
3. Rūtī **Ātrā izveide** ievadiet lomu un organizācijas vienību kombināciju, kurai ir jāiestata rēķina likme.

  Tālāk sniegtajā tabulā ir iekļauti lauki cilnē **Vispārīgi** un **Ātrā izveide** rūts ar lomu cenu rindu, kas ir jāpatur prātā, veidojot pārdošanas cenas sarakstā norādītās lomas.

  | Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
  | --- | --- | --- | --- |
  | Loma | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Atlasiet lomu, kurai iestatāt rēķina likmi. | Loma ienākošajā tāmē vai faktiskajos datos tiks saskaņota ar šo rindu, lai noklusētu rēķina likmi. |
  | Resursu vienība | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Atlasiet organizācijas vienību vai uzņēmuma nodaļu, no kuras ir loma. Piemēram, izstrādātājs no Fabrikam India Robotics nodaļas vai izstrādātājs no Fabrikam USA programmatūras nodaļas. | Ienākošās aplēses vai faktiskās resursu veidošanas vienība tiks saskaņota ar šo rindu, lai noklusētu lomas rēķina likmi. |
  | Cenrādis | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Iestatiet rēķina likmi lomu resursu veidošanas uzņēmumam un resursu piešķiršanas vienību kombinācijai. Piemēram, izstrādātājam no Fabrikam India ir rēķina kurss 100 ASV dolāru vai izstrādātājam no Fabrikam USA ir rēķina likme 150 ASV dolāru. | Šī ir noklusētā rēķina likme ienākošā novērtējuma vienības cenai vai laika darbības klases faktiskajai rindai. |
  | Valūta | Cilne **Vispārīgi** un rūts **Ātrā izveide**| Pēc noklusējuma valūtas vērtība tiek iegūta no valūtas, kas atrodas pārdošanas cenu saraksta galvenē. Pārdošanas cenrādī valūtu nevar ignorēt. | Šī valūta ir noklusētā valūta vienības cenā ienākošajai faktiskajai pārdošanas rindai laika darbības klasē. |
  | Vienības grafiks | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Šis vienības plāns pēc noklusējuma ir Laiks, un to nevar mainīt Lomas cenas entītijā, jo tas tiek izmantots, lai izteiktu likmes pēc laika vienībām. | Šim laukam nav lejupstraumes ietekmes. |
  | Vienība | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Vienības vērtība tiek iegūta no lauka **Laika vienība**, kas atrodas pārdošanas cenu saraksta galvenē. Tomēr šo vērtību var ignorēt. Piemēram, izstrādātājs no Fabrikam India maksā 1000 ASV dolāru par **Indijas dienu**. IIzstrādātājam no Fabrikam USA ir rēķina likme 1500 ASV dolāru par **ASV dienu**. | Ja ienākošās aplēses vai faktiskās rindas noklusējums ir vienības cena, sistēma izmanto vienību sistēmu un konvertēšanu bāzes vienībās, lai aprēķinātu vienības cenu. Piemēram, tāme ir 10 **India Days** ērts darbs izstrādātājam no Indijas, un vienība “Indijas diena” tiek definēta kā 10 stundas. Ja tiek noteikta novērtējuma rinda, programma aprēķina vienības cenu aprēķinā kā 1000 ASV dolāru/10 stundas = 100 ASV dolāru stundā. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Pāradresācijas cenu noteikšana vai rēķinu likmes iestatīšana resursiem no citām organizācijas vienībām vai daļām 

Uz projektu balstīti uzņēmumi, kas izmanto darbiniekus no dažādām uzņēmuma struktūrvienībām, lai strādātu pie projektiem. Projektus var izpildīt no vienas struktūrvienības, kamēr darbinieki vai konsultanti ir no vienas un tās pašas cita uzņēmuma nodaļas. Projektu varētu veidot arī personu apvienojums no dažādām struktūrvienībām. Risinājumā Project Operations uzņēmumam, kam pieder projekta piegāde, tiek dēvēta kā **Līgumslēdzēja vienība**. Visas pārējās struktūrvienības, kas nodrošina resursus, tiek sauktas kā **Resursu vienības**. Ņemot vērā darba izmaksu atšķirības dažādos ģeogrāfiskos apgabalos un darba tirgos visā pasaulē, arī darba samaksas likmes dažādos ģeogrāfiskos apgabalos tiek noteiktas atšķirīgi.

Piemēram, izstrādātājs no Fabrikam India, kas strādā pie ASV projekta, izmaksā 100 ASV dolāru stundā. Izstrādātājs no Fabrikam US, kas strādā pie ASV projekta, izmaksā 150 ASV dolāru stundā.

### <a name="example-set-up-a-bill-rate"></a>Piemērs: rēķina likmes iestatīšana

1. Izveidojiet pārdošanas cenrāža nosaukumu *Fabrikam US rēķinu likmes* un iestatiet datu efektivitāti.
2. Pārdošanas cenrādī ievadiet šādu likmes informāciju:

    | Loma | Organizācijas vienība | Rēķina likme |
    | --- | --- | --- |
    | Izstrādātājiem | Fabrikam India | USD 100 |
    | Izstrādātājiem | Fabrikam Philippines | 90 ASV dolāru |
    | Izstrādātājiem | Fabrikam US | 150 ASV dolāru |

3. Pievienojiet pārdošanas cenrādi **Fabrikam US rēķinu likmes** projekta līguma cenrādim vai noteiktam kontam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]