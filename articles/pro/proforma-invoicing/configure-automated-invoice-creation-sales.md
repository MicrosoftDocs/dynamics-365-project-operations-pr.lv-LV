---
title: Automātiskas rēķina izveides iestatīšana
description: Šajā tēmā ir sniegta informācija par proformas rēķinu automātiskās izveides iestatīšanu un konfigurēšanu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1cce457fbc04ba9d3890d73439e6e7fd3db44d84a4498d5dc68ed82d362158b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997525"
---
# <a name="set-up-automatic-invoice-creation"></a>Automātiskas rēķina izveides iestatīšana 
 
_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_

Varat konfigurēt automātiskas rēķina izveides programmā Dynamics 365 Project Operations. Sistēma izveido melnraksta proforma rēķinu, pamatojoties uz rēķina grafiku katram projekta līgumam un līguma rindai. Rēķinu grafiki tiek konfigurēti līguma rindas līmenī. Katrai līguma rindai var noteikt atsevišķu rēķina grafiku vai vienu un to pašu rēķina grafiku var iekļaut ikvienā līguma rindā.

Kad izveidojat rēķinu, sistēma vienmēr katram projekta līgumam izveido vismaz vienu rēķinu. Dažos gadījumos var būt izveidoti vairāki rēķini. Piemēram, ja līgumam ir vairāki klienti, tiek izveidots tāds pats rēķinu skaits kā to klientu skaits, kuriem attiecīgajā projekta līgumā ir rēķinā iekļaujami darījumi.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Informācija par to, kā darījumi tiek iekļauti rēķinā 

Dažreiz katra projekta līguma rinda nosaka atsevišķu rēķina grafiku. Piemēram, ieviešanas pakalpojumiem, kas paredzēti Adatum līgumam, ir šādas līguma rindas:

- Prototipa darbs, kas ir fiksēta cena ar diviem manuāli izveidotiem atskaites punktiem.
- Ieviešanas darbs, kurā ir iekļauts laiks un par ko reizi divās nedēļās pirmdienā tiks izrakstīts rēķins.
- Radušies izdevumi, kas jāapmaksā katru mēnesi katra mēneša pirmajā pirmdienā.

Rēķina grafiki, kas definēti katrā no šiem diviem rindas elementiem, izskatīsies, kā redzams tabulā.

| Līguma rinda | Rēķina izpildes datums | Transakcijas pēdējais datums | Atskaites punkta datums | Atskaites punkta summa |
| --- | --- | --- | --- | --- |
| Prototipa darbs | 5. oktobris, pirmdiena | - | 5. oktobris, pirmdiena | 5000 USD |
| - | 3. novembris, otrdiena | - | 3. novembris, otrdiena | 12,000 USD |
| Ieviešanas darbs | 5. oktobris, pirmdiena | 4. oktobris, svētdiena | - | - |
| - | 19. oktobris, pirmdiena | 18. oktobris, svētdiena | - | - |
| - | 2. novembris, pirmdiena | 1. novembris, svētdiena | - | - |
| - | 16. novembris, pirmdiena | 15. novembris, svētdiena | - | - |
| Radušies izdevumi | 5. oktobris, pirmdiena | 4. oktobris, svētdiena | - | - |
| - | 2. novembris, pirmdiena | 1. novembris, svētdiena | - | - |

Šajā piemērā, kad tiek izpildīta automātiskā rēķinu izveide:

- **4. oktobris vai jebkura diena pirms tā**: šim līgumam netiek ģenerēts rēķins, jo tabula **Rēķina grafiks** katrai no šīm līguma rindām neizsauc 4. oktobri, svētdienu kā rēķina izpildes datumu.
- **5. oktobris, pirmdiena**: viens rēķins tiek ģenerēts:

    - Prototipa darbs, kas ietver atskaites punktu, ja tas ir atzīmēts kā **Gatavs rēķina izrakstīšanai**.
    - Ieviešanas darbs, kurā ir iekļauti visi laika darījumi, kas izveidoti pirms darījuma pabeigšanas datuma 4. oktobrī, svētdienā, kas ir atzīmēts kā **Gatavs rēķina izrakstīšanai**.
    - Radušies izdevumi, kuros ir iekļauti visi izdevumu darījumi, kas izveidoti pirms darījuma pabeigšanas datuma 4. oktobrī, svētdienā, kas ir atzīmēts kā **Gatavs rēķina izrakstīšanai**.
  
- **6. oktobris vai jebkura diena pirms 19. oktobra**: šim līgumam netiek ģenerēts rēķins, jo tabula **Rēķina grafiks** katrai no šīm līguma rindām neizsauc 6. oktobri vai jebkuru datumu pirms 19. oktobra kā rēķina izpildes datumu.
- **19. oktobris, pirmdiena**: viens rēķins tiek izveidots no ieviešanas darba, kurā ir iekļauti visi laika darījumi, kas izveidoti pirms darījuma pabeigšanas datuma 18. oktobrī, svētdienā, kas ir atzīmēts kā **Gatavs rēķina izrakstīšanai**.
- **2. novembris, pirmdiena**: viens rēķins tiek ģenerēts:

    - Ieviešanas darbs, kurā ir iekļauti visi laika darījumi, kas izveidoti pirms darījuma pabeigšanas datuma 1. novembrī, svētdienā, kas ir atzīmēts kā **Gatavs rēķina izrakstīšanai**.
    - Radušies izdevumi, kuros ir iekļauti visi izdevumu darījumi, kas izveidoti pirms darījuma pabeigšanas datuma 1. novembrī, svētdienā, kas ir atzīmēts kā **Gatavs rēķina izrakstīšanai**.

- **3. novembris, otrdiena**: viens rēķins tiek ģenerēts prototipa darbam, kas ietver 12000 USD atskaites punktu, ja tas ir atzīmēts kā **Gatavs rēķina izrakstīšanai**.

## <a name="configure-automatic-invoicing"></a>Automātiskās rēķinu izrakstīšanas konfigurēšana

Veiciet tālāk norādītās darbības, lai konfigurētu automātisko rēķina izpildi.

1. Sadaļā **Project Operations** atveriet **Iestatījumi** > **Periodisku rēķinu iestatīšana**.
2. Izveidojiet lielapjoma darbu un nosauciet to **Project Operations rēķinu izveide**. Lielapjoma darba nosaukumā jābūt iekļautiem vārdiem “rēķinu izveide”.
3. Laukā **Darba tips** atlasiet vienumu **Nav**. Pēc noklusējuma lauki **Biežuma aizkave** un **Aktīvs** ir iestatīti uz **Jā**.
4. Atlasiet **Palaist darbplūsmu**. Dialoglodziņā **Meklēt ierakstu** redzēsiet trīs darbplūsmas.

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Atlasiet vienumu **ProcessRunCaller** un pēc tam **Pievienot**.
6. Nākamajā dialoglodziņā atlasiet **Labi**. Darbplūsma **Miegs** seko darbplūsmai **Apstrādāt**. 

> [!NOTE]
> 5. darbībā varat arī atlasīt **ProcessRunner**. Pēc tam, kad atlasā **Labi** **Apstrādāt** darbplūsmai seko **Miegs** darbplūsma.

**ProcessRunCaller** un **ProcessRunner** darbplūsmas veido rēķinus. **ProcessRunCaller** izsauc **ProcessRunner**. **ProcessRunner** ir darbplūsma, kas faktiski izveido rēķinus. Darbplūsma darbojas caur visām līguma rindām, kurām ir jāizveido rēķini, un izveido rēķinu šīm rindām. Lai noteiktu līguma rindas, kurām jāizveido rēķini, darbs tiek apskatīts līguma rindu rēķina izpildes datumos. Ja līguma rindām, kas attiecas uz vienu līgumu, ir vienāds rēķina izpildes datums, darījumi tiek apvienoti vienā rēķinā, kurā ir divas rēķina rindas. Ja nav nevienas transakcijas rēķinu izveidei, darbs izlaiž rēķina izveidošanu.

Kad **ProcessRunner** ir beidzis darboties, tas izsauc **ProcessRunCaller**, nodrošina beigu laiku un ir slēgts. **ProcessRunCaller** pēc tam sāk skaitīt laiku, kas darbojas 24 stundas no norādītā beigu laika. Taimera laika skaitīšanas beigās **ProcessRunCaller** tiek slēgts.

Lielapjoma izpildes darbs rēķinu izveidošanai ir kārtējais darbs. Ja šis pakešapstrādes process ir palaists vairākas reizes, tiek izveidoti vairāki darba gadījumi un var tikt izraisītas kļūdas. Tāpēc pakešapstrāde jāsāk tikai vienu reizi, un pēc tam tā ir jārestartē tikai tad, ja tā pārstāj darboties.

> [!NOTE]
> Project Operations lielapjomu rēķinu izveide darbojas vienīgi projekta līguma rindām, kuras ir konfigurējuši rēķinu grafiki. Līguma rindai ar fiksētu cenas aprēķina metodi jābūt konfigurētiem atskaites punktiem. Projekta līguma rindai ar laika un materiālu aprēķinu metodi ir jābūt iestatītam datuma bāzes rēķina grafikam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
