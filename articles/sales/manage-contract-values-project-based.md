---
title: Darbs ar projekta līguma rindām
description: Šajā tēmā ir sniegta informācija par projekta līguma rindām.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2072692296308a08756ec3e0f381c792745dd3e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011515"
---
# <a name="work-with-projectbased-contract-lines"></a>Darbs ar projekta līguma rindām

Projekta līguma rindas risinājumā Dynamics 365 Project Operations ir izstrādātas, lai ietvertu budžeta un norēķinu līgumus noteiktiem projekta darba komponentiem saistībā ar dalību. Līguma rinda, kuras pamatā ir projekts, tiek paplašināta projekta aplēsēm un norēķinu scenārijiem, izmantojot tālāk norādītos jēdzienus.

- Rēķinu izrakstīšanas metode
- Projektu un uzdevumu kartēšana
- Iekļautās transakciju klases
- Nepārsniedzamais ierobežojums
- Iekasēšanas iestatīšana
- Novērtējumi, izmantojot līgumu rindu informāciju
- Līguma rindas klients

Tālāk minētie lauki ir iekļauti līguma rindu cilnē **Vispārīgi**. Šie lauki palīdz iestatīt detalizētu, no jauna veidotu aprēķinu un rēķinu izrakstīšanas kārtību atbilstoši projekta darbam.

| Lauks | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| **Nosaukums** | Līguma rindas nosaukums, kas identificē līguma diskrēto komponentu, kas tiek novērtēts. No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošās projekta piedāvājuma rindas vērtības. | Šī lauka vērtība tiek kopēta uz to projekta rēķina rindu, kura tiek izveidota no šīs līguma rindas, kad tiek izveidots rēķins. |
| **Rēķinu izrakstīšanas metode** | No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošā piedāvājuma rindas lauka. Tā ir opciju kopa, kas pārstāv divus galvenos līguma modeļus, ko atbalsta Project Operations:</br>- **Fiksēta cena**</br>- **Laiks un materiāls** | Par pamatu izmantojot atsauces līguma rindas norēķinu metodi, tiek veikta faktiskā darbība. Ja līguma rindai, kurai ir atsauce uz faktisko, ir iestatīts laiks un materiālu norēķinu metode, tiek izveidots izmaksu un rēķinā neiekļauto pārdošanas darījumu faktiskais ieraksts. Ja līguma rindai, kurai ir atsauce uz faktisko, ir fiksētas cenas norēķinu metode, tiek izveidota tikai izmaksu faktiskā summa. |
| **Project** | Izmantojiet šo lauku, lai norādītu projektu, kas tiks izmantots, lai nodrošinātu darbu šajā piesaistē. | Šī lauka vērtība tiks izmantota savienojumā ar laukiem **Iekļautie uzdevumi** un **Iekļautās transakciju klases**, lai atrisinātu līguma rindas atsauci faktiskajā vai novērtējuma rindas ierakstā. |
| **Iekļaut laiku** | Karodziņš norāda, vai šajā līguma rindā ir iekļautas laika transakcijas vai darba izmaksas par atlasīto projektu. Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas laika transakcijas vai darba izmaksas. Vērtība **Jā** norāda, ka tās tiks iekļautas. | Šī lauka vērtība tiks izmantota savienojumā ar projektu, lai atrisinātu līguma rindas atsauci faktiskajā vai novērtējuma rindas ierakstā. |
| **Iekļaut izdevumus** | Karodziņš norāda, vai šajā līguma rindā tiks iekļautas izdevumu izmaksas par atlasīto projektu. Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas izdevumu izmaksas. Vērtība **Jā** norāda, ka tās tiks iekļautas. | Šī lauka vērtība tiks izmantota savienojumā ar projektu, lai atrisinātu līguma rindas atsauci faktiskajā vai novērtējuma rindas ierakstā. |
| **Iekļaut maksu** | Karodziņš norāda, vai šajā līguma rindā tiks iekļautas papildmaksas par atlasīto projektu. Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas papildmaksas. Vērtība **Jā** norāda, ka tās tiks iekļautas. | Šī lauka vērtība tiks izmantota savienojumā ar projektu, lai atrisinātu līguma rindas atsauci faktiskajā vai novērtējuma rindas ierakstā. |
| **Līgumā paredzētā summa** | Fiksētas cenas līguma rindā šī ir vienošanās par vērtību, par kuru klientam tiks izrakstīts rēķins attiecībā uz visiem ar šo līguma rindu saistītajiem darba komponentiem. Laika un materiāla līguma rindā šī summa ir aprēķināta vērtība, par kuru klientam tiks izrakstīts rēķins attiecībā uz visiem ar šo līguma rindu saistītajiem darba komponentiem. No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošā piedāvājuma rindas lauka. Ja projektā, kuras pamatā ir līguma rinda, ir rindu informācija, šis lauks ir slēgts rediģēšanai, un tas tiek apkopots no līguma rindas informācijas summas. | Ja līguma rindai ir rindas informācija, šo vērtību var modificēt, mainot summas rindu informācijā. Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai par periodiskajiem norēķinu atskaites punktiem ģenerētu summu pirms nodokļu nomaksas. |
| **Aprēķinātais nodoklis** | Lietotājs var rediģēt šo lauku, lai ievadītu prognozējamo nodokļu summu līguma rindā. Ja projektā, kuras pamatā ir līguma rinda, ir rindu informācija, šis lauks ir slēgts rediģēšanai, un tas tiek apkopots no līguma rindas informācijas nodokļu summas. | Ja līguma rindai ir rindas informācija, šo vērtību var modificēt, mainot nodokļu summas rindu informācijā. Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai par periodiskajiem norēķinu atskaites punktiem ģenerētu nodokļus. |
| **Līgumā paredzētā summa pēc nodokļa atskaitīšanas** | Līguma rindas summa pēc nodokļa atskaitīšanas. Šis lauks ir tikai lasāms un aprēķināts kā **Līgumā paredzētā summa + nodoklis**. | Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai ģenerētu periodisko norēķinu atskaites punktus. |
| **Nepārsniedzamais ierobežojums** | Lietotājs var rediģēt šo lauku, un tas ir pieejams tikai projekta līguma rindās, kurās ir laika un materiālu norēķinu metode. | Lietotājs var rediģēt šo lauku. Kad uz faktisko laiku vai materiāliem attiecas šī līguma rinda, faktiskais laiks un materiāli norāda faktisko summu attiecībā pret nepārsniedzamo limitu līguma rindā pēc tam, kad ir veikta uzskaite par jau iztērētajām un piešķirtajām summām. |
| **Klienta budžets** | Ja līgums tika izveidots no piedāvājuma, šis lauks ir rediģējams un ir nokopēts no atbilstošā piedāvājuma rindas lauka. | Šis lauks tiek izmantots tikai informācijai, un tam nav pakārtotas nozīmes. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Validācijas kārtula projekta līguma rindu cilnē Vispārīgi norādītajām opcijām

Kārtula: projekts un noteikta transakciju klase var būt iekļauta tikai vienā līguma projekta līguma rindā.

| Līgums | Līguma rinda | Project | Iekļaut laiku | Iekļaut izdevumus | Iekļaut maksu | Derīgs/nav derīgs | Iemesls                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Jā          | Jā             | Jā         | Nav derīgs       | Pārkāpj kārtulu. Laiks, izdevumi un maksas projektam P1 ir iekļautas abās līguma rindās, CL1 un CL2.                                                                                       |
| C1       | CL2           | P1      | Jā          | Jā             | Jā         | Nav derīgs       | Pārkāpj kārtulu. Laiks, izdevumi un maksas projektam P1 ir iekļautas abās līguma rindās, CL1 un CL2.                                                                                       |
| C1       | CL1           | P1      | Jā          | No              | Jā         | Nav derīgs       | Pārkāpj kārtulu. Laiks un maksas projektam P1 ir iekļautas abās līguma rindās, CL1 un CL2.                                                                                                   |
| C1       | CL2           | P1      | Jā          | Jā             | Jā         | Nav derīgs       | Pārkāpj kārtulu. Laiks un maksas projektam P1 ir iekļautas abās līguma rindās, CL1 un CL2.                                                                                                   |
| C1       | CL1           | P1      | Jā          | No              | Jā         | Derīgs           | Projekta P1 laiks un maksas ir iekļautas CL1. Izdevumi P1 projektā ir ietverti rindā CL2. </br>   Nav pārklāšanās tam, kas tiek iekļauts katrā līguma rindā un tādējādi ir derīgs.  |
| C1       | CL2           | P1      | No           | Jā             | No          | Derīgs           | Projekta P1 laiks un maksas ir iekļautas CL1. Izdevumi P1 projektā ir ietverti rindā CL2. </br>   Nav pārklāšanās tam, kas tiek iekļauts katrā līguma rindā un tādējādi ir derīgs.  |
| C1       | CL1           | P1      | Jā          | Jā             | Jā         | Nav derīgs       | Pārkāpj kārtulu. Laiks, izdevumi un maksas projektam P1 ir iekļautas divu līgumu rindās.                                                                                               |
| CL2      | CL2           | P1      | Jā          | Jā             | Jā         | Nav derīgs       | Pārkāpj kārtulu. Laiks, izdevumi un maksas projektam P1 ir iekļautas divu līgumu rindās.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]