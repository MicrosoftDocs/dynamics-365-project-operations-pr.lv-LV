---
title: Iestatīt darba rēķinu likmes
description: Šajā rakstā ir sniegta informācija par to, kā iestatīt darba norēķinu likmes risinājumā Project Operations.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ad83e899030be480baed95597e1ccfc0e560e24
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924347"
---
# <a name="set-up-labor-bill-rates"></a>Iestatīt darba rēķinu likmes

_ **Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem

Katram cenrādim ir lomu cenu kopa vai darba likmes, kas ir spēkā kontekstam un datumu efektivitātei, kas iekļauta cenrāža galvenē. Rēķinu kursus laika intervālam programmā Dynamics 365 Project Operations var iestatīt tikai vienā valūtā, kas ir valūta cenrāža galvenē.

1. Lai pārdošanas cenrādim iestatītu darbaspēka rēķinu cenas, atveriet **Pārdošana** > **Klienti** > **Cenrāži** un atlasiet  **Jauns**, lai izveidotu jaunu cenrādi. 
2. Cilnes **Lomas cenas** apakšrežģī atlasiet **Jauna lomas cena**. 
3. Rūtī **Ātrā izveide** ievadiet lomu un organizācijas vienību kombināciju, kurai ir jāiestata rēķina likme.

   Tālāk sniegtajā tabulā ir iekļauti lauki cilnē **Vispārīgi** un **Ātrā izveide** rūts ar lomu cenu rindu, kas ir jāpatur prātā, veidojot pārdošanas cenas sarakstā norādītās lomas.

    | Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
    | --- | --- | --- | --- |
    | Loma | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Atlasiet lomu, kurai iestatāt rēķina likmi. | Loma ienākošajā tāmē vai faktiskajos datos tiks saskaņota ar šo rindu, lai noklusētu rēķina likmi. |
    | Resursu uzņēmums | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Atlasiet uzņēmumu vai juridisku personu, no kuras ir loma. Piemēram, izstrādātājs no Fabrikam India vai izstrādātājs no Fabrikam USA. | Ienākošās aplēses vai faktiskās resursu veidošanas uzņēmums tiks saskaņots ar šo rindu, lai noklusētu lomas rēķina likmi. |
    | Resursu vienība | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Atlasiet organizācijas vienību vai uzņēmuma nodaļu, no kuras ir loma. Piemēram, izstrādātājs no Fabrikam India Robotics nodaļas vai izstrādātājs no Fabrikam USA programmatūras nodaļas. | Ienākošās aplēses vai faktiskās resursu veidošanas vienība tiks saskaņota ar šo rindu, lai noklusētu lomas rēķina likmi. |
    | Cenrādis | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Iestatiet rēķina likmi lomu resursu veidošanas uzņēmumam un resursu piešķiršanas vienību kombinācijai. Piemēram, izstrādātājam no Fabrikam India ir rēķina kurss 100 ASV dolāru vai izstrādātājam no Fabrikam USA ir rēķina likme 150 ASV dolāru. | Šī ir noklusētā rēķina likme ienākošā novērtējuma vienības cenai vai laika darbības klases faktiskajai rindai. |
    | Valūta | Cilne **Vispārīgi** un rūts **Ātrā izveide**| Pēc noklusējuma valūtas vērtība tiek iegūta no valūtas, kas atrodas pārdošanas cenu saraksta galvenē. Pārdošanas cenrādī valūtu nevar ignorēt. | Šī valūta ir noklusētā valūta vienības cenā ienākošajai faktiskajai pārdošanas rindai laika darbības klasē. |
    | Vienības grafiks | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Šis vienības plāns pēc noklusējuma ir Laiks, un to nevar mainīt Lomas cenas entītijā, jo tas tiek izmantots, lai izteiktu likmes pēc laika vienībām. | Šim laukam nav lejupstraumes ietekmes. |
    | Vienība | Cilne **Vispārīgi** un rūts **Ātrā izveide** | Vienības vērtība tiek iegūta no lauka **Laika vienība**, kas atrodas pārdošanas cenu saraksta galvenē. Tomēr šo vērtību var ignorēt. Piemēram, izstrādātājs no Fabrikam India maksā 1000 ASV dolāru par **Indijas dienu**. IIzstrādātājam no Fabrikam USA ir rēķina likme 1500 ASV dolāru par **ASV dienu**. | Ja ienākošās aplēses vai faktiskās rindas noklusējums ir vienības cena, sistēma izmanto vienību sistēmu un konvertēšanu bāzes vienībās, lai aprēķinātu vienības cenu. Piemēram, tāme ir 10 **India Days** ērts darbs izstrādātājam no Indijas, un vienība “Indijas diena” tiek definēta kā 10 stundas. Ja tiek noteikta novērtējuma rinda, programma aprēķina vienības cenu aprēķinā kā 1000 ASV dolāru/10 stundas = 100 ASV dolāru stundā. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Pāradresācijas cenu noteikšana vai rēķinu likmes iestatīšana resursiem no citām organizācijas vienībām vai daļām 

Uz projektiem balstītie uzņēmumi bieži izmanto dažādu juridisku personu darbiniekus un dažādas juridiskās personas, lai strādātu pie projektiem. Projektus var īstenot no noteiktas juridiskas personas un nodaļas, bet darbinieki vai konsultanti, kas strādā ar projektiem, var būt no tās pašas juridiskās personas un nodaļas vai no citas. Projektā var iekļaut arī personu kombināciju no dažādām juridiskām personām un struktūrvienībām. Risinājumā Project Operations juridiskā persona, kurai pieder projekta piegāde, ir **Uzņēmuma īpašnieks**, un struktūrvienība, kurai pieder piegāde, ir **Līgumslēdzēja vienība**. Visas citas juridiskās personas, kas nodrošina resursus, ir **Resursu uzņēmumi**, un nodaļas, kas nodrošina resursus, ir **Resursu struktūrvienības**. Ņemot vērā darba izmaksu atšķirības dažādos ģeogrāfiskos apgabalos un darba tirgos visā pasaulē, arī darba samaksas likmes dažādos ģeogrāfiskos apgabalos tiek noteiktas atšķirīgi.

Piemēram, izstrādātājs no Fabrikam India Robotics nodaļas, kas strādā pie ASV projekta, izmaksā 100 ASV dolāru stundā. Piemēram, izstrādātājs no Fabrikam US Robotics nodaļas, kas strādā pie ASV projekta, izmaksā 150 ASV dolāru stundā. 

### <a name="example-set-up-a-bill-rate"></a>Piemērs: rēķina likmes iestatīšana 

1. Izveidojiet pārdošanas cenrāža nosaukumu *Fabrikam US rēķinu likmes* un iestatiet datu efektivitāti.
2. Pārdošanas cenrādī ievadiet šādu likmes informāciju:

    | Loma | Resursu uzņēmums | Resursu vienība | Rēķina likme |
    | --- | --- | --- | --- |
    | Izstrādātājiem | Fabrikam India | Fabrikam India - Robotics | USD 100 |
    | Izstrādātājiem | Fabrikam Philippines | Fabrikam Philippines - Robotics | 90 ASV dolāru |
    | Izstrādātājiem | Fabrikam US | Fabrikam US - Robotics | 150 ASV dolāru |

3. Pievienojiet pārdošanas cenas sarakstu, ar **Fabrikam US rēķinu likmēm** projekta līguma cenrādim vai noteiktam uzņēmumam.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
