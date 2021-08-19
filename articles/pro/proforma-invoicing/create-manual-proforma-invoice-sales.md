---
title: Pro forma projekta rēķini
description: Šajā tēmā ir sniegta informācija par proformas projekta rēķiniem programmā Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3d02728ce682781eb8816e0c2239cf62f88adfa8c5d2a0aab280be053c2a5ae6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992935"
---
# <a name="proforma-project-pnvoices"></a>Pro forma projekta rēķini

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Pro forma projektu rēķinu izveide projektu vadītājiem sniedz otro apstiprinājuma līmeni pirms rēķinu izveides klientiem. Pirmais apstiprināšanas līmenis tiek pabeigts, kad tiek apstiprināti projekta darba grupas dalībnieku iesniegtie laika, izdevumu un materiālu ieraksti.

Dynamics 365 Project Operations Lite izvietošana nav izstrādāta, lai ģenerētu klientiem paredzētus rēķinus. Šajā sarakstā ir parādīts, kāpēc rēķinus nevar ģenerēt.

- Nav iekļauta informācija par nodokļiem.
- Nevar konvertēt citas valūtas rēķina valūtā.
- Nevar pareizi formatēt rēķinus drukāšanai.

Tā vietā varat izmantot finanšu vai grāmatvedības sistēmu, lai izveidotu klientiem paredzētus rēķinus, kuri izmanto informāciju no rēķina priekšlikumiem.

## <a name="creating-project-invoices"></a>Projektu rēķinu izveide

Projekta rēķinus var izveidot pa vienam vai arī lielapjomā. Tos varat izveidot manuāli, vai arī var konfigurēt tā, lai tie tiktu ģenerēti automātikā palaišanā.

### <a name="manually-create-project-invoices"></a>Manuāla projektu rēķinu izveide 

Saraksta lapā **Projekta līgumi** varat izveidot projekta rēķinus atsevišķi katram projekta līgumam, kā arī var izveidot lielapjoma rēķinus vairākiem projekta līgumiem.

   - Lai izveodotu rēķinu konkrētam projekta līgumam, sarakstu lapā **Projekta līgumi** atveriet projekta līgumu un atlasiet **Izveidot rēķinu**.

   Rēķins tiek ģenerēts visām atlasītā projekta līguma transakcijām, kuru statuss ir **Gatavs rēķinam**. Šīs transakcijas ietver laika, izmaksu, materiālu, atskaites punktu, produktu līguma rindas un citas rēķinos neietvertas pārdošanas žurnala rindas, kuras, iespējams, ir apstiprinātas.

Rēķinu lielapjoma izveide

1. Sarakstu lapā **Projekta līgumi** atlasiet vienu vai vairākus projekta līgumus, kuriem jāizveido rēķins, un pēc tam atlasiet **Izveidot projekta rēķinus**.
2. Brīdinājuma ziņojums informē par to, ka pirms rēķinu izveidošanas var būt aizkave. Tiek parādīts arī process. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

   Rēķins tiek ģenerēts visām līguma rindas transakcijām, kuru statuss ir **Gatavs rēķinam**. Šīs transakcijas ietver laika, izmaksu, materiālu, atskaites punktu, produktu līguma rindas un citas rēķinos neietvertas pārdošanas žurnala rindas, kuras, iespējams, ir apstiprinātas.

3. Lai skatītu ģenerētos rēķinus, dodieties uz **Pārdošana** \> **Norēķini** \> **Rēķini**. Katram projekta līgumam tiks parādīts viens rēķins.

### <a name="set-up-automated-creation-of-project-invoices"></a>Projektu rēķinu automātiskas izveides iestatīšana 

Veiciet tālāk norādītās darbības, lai konfigurētu automātisko rēķina izpildi.

1. Dodieties uz **Iestatījumi** \> **Lielapjoma darbi**.
2. Izveidojiet lielapjoma darbu un nosauciet to **Project Operations rēķinu izveide**. Lielapjoma darbu nosaukumā ir jāiekļauj termins “Rēķinu izveide”.
3. Laukā **Darba tips** atlasiet vienumu **Nav**. **Pēc noklusējuma** Biežuma aizkave **Aktīvs** opcijas ir iestatītas uz **Jā.**
4. Atlasiet **Palaist darbplūsmu**. Dialoglodziņā **Meklēt ierakstu** redzēsiet talāk minētās darbplūsmas.

    - ProcessRunCaller
    - Procesu palaidējs
    - Atjaunināt lomu lietojumu

5. Atlasiet vienumu **ProcessRunCaller** un pēc tam **Pievienot**.
6. Nākamajā dialoglodziņā atlasiet **Labi**. Darbplūsma **Miegs** seko darbplūsmai **Apstrādāt**.

    5. darbībā varat arī atlasīt **ProcessRunner**. Pēc tam, kad atlasā **Labi** **Apstrādāt** darbplūsmai seko **Miegs** darbplūsma.

**ProcessRunCaller** un **ProcessRunner** darbplūsmas veido rēķinus. **ProcessRunCaller** izsauc **ProcessRunner**. **ProcessRunner** ir darbplūsma, kas izveido rēķinus. Šī darbplūsma iet cauri visām līguma rindām, kurām ir jāizveido rēķini, un izveido rēķinus šīm rindām. Lai noteiktu līguma rindas, kurām jāizveido rēķini, darbplūsma apskata līguma rindu rēķina izpildes datumus. Ja līguma rindām, kas attiecas uz vienu līgumu, ir vienāds rēķina izpildes datums, darījumi tiek apvienoti vienā rēķinā, kurā ir divas rēķina rindas. Ja nav nevienas transakcijas rēķinu izveidei, rēķini netiek izveidoti.

Kad **ProcessRunner** ir beidzis darboties, tas izsauc **ProcessRunCaller**, nodrošina beigu laiku un ir slēgts. **ProcessRunCaller** pēc tam sāk skaitīt laiku, kas darbojas 24 stundas no norādītā beigu laika. Taimera laika skaitīšanas beigās **ProcessRunCaller** tiek slēgts.

Lielapjoma izpildes darbs rēķinu izveidošanai ir kārtējais darbs. Ja šis pakešapstrādes process ir palaists vairākas reizes, tiek izveidoti vairāki darba gadījumi un var tikt izraisītas kļūdas. Lai novērstu šo problēmu, sāciet pakešapstrādi tikai vienu reizi, un restartējiet to tikai tad, ja tā pārstāj darboties.

> [!NOTE]
> Lielapjomu rēķinu izveide darbojas vienīgi projekta līguma rindām, kuras ir konfigurējuši rēķinu grafiki. Līguma rindai ar fiksētu cenas aprēķina metodi jābūt konfigurētiem atskaites punktiem. Projekta līguma rindai ar laika un materiālu aprēķinu metodi ir jābūt iestatītam datuma bāzes rēķina grafikam. Tas pats attiecas uz līguma rindu, kuras pamatā ir projekts.      
 
### <a name="edit-a-draft-invoice"></a>Melnraksta rēķina rediģēšana

Izveidojot projekta rēķina melnrakstu, visi nepārdoto pārdošanas transakciju ieraksti, kas tika izveidoti, kad tika apstiprināti laika un izdevumu ieraksti, tiek iekļauti rēķinā. Varat veikt tālāk norādītos pielāgojumus, kamēr rēķins vēl nav iekļauts melnraksta stadijā.

- Dzēsiet vai rediģējiet informāciju par rēķina rindu.
- Rediģējiet un pielāgojiet daudzuma un norēķinu tipu.
- Precīzi pievienojiet laiku, izdevumus, materiālus un maksas kā rēķina transakcijas. Šo līdzekli var izmantot, ja rēķina rinda ir kartēta uz līguma rindu, kas ļauj veikt šīs transakciju klases.

Atlasiet vienumu **Apstiprināt**, lai apstiprinātu rēķinu. Šī ir vienvirziena darbība. Atlasot **Apstiprināt**, rēķins kļūst par tikai lasāmu un tiek izveidotas rēķinā ietvertās pārdošanas faktiskās vērtība no katras rēķina rindas detalizētās vērtības katrā rēķina rindā. Ja rēķina rindas informācija attiecas uz rēķinā neietvertu pārdošanas faktisko vērtību, rēķinā neietvertā pārdošanas faktiskā vērtība tiek atsaukta. Jebkura rēķina rindas detalizēta informācija, kas izveidota laika, izmaksu vai materiālu lietojuma ieraksta laikā, attiecas uz rēķinā neietverto pārdošanas faktisko vērtību. Virsgrāmatas integrācijas sistēmas var izmantot šo atsaukšanu, lai grāmatvedības vajadzībām mainītu nepabeigto projekta darbu (WIP).

### <a name="correct-a-confirmed-invoice"></a>Apstiprināta rēķina labošana

Apstiprinātos rēķinus var rediģēt. Kad esat izlabojis apstiprinātu rēķinu, tiek izveidots jauns melnraksta labojošais rēķins. Tā kā tiek pieņemts, ka vēlaties atsaukt visas transakcijas un daudzumus no sākotnējā rēķina, šis labotais rēķins ietver visas darbības no sākotnējā rēķina un visi tajā ietvertie daudzumi ir nulle.

Ja transakcijām nav nepieciešama labošana, tās var noņemt no melnraksta labojošā rēķina. Ja vēlaties atsaukt vai atgriezt tikai daļēju daudzumu, var rediģēt rindas informācijas lauku **Daudzums**. Ja atverat rēķina rindas informāciju, varat redzēt sākotnējo rēķina apjomu. Pašreizējo rēķina daudzumu var rediģēt, lai tas būtu mazāks vai lielāks par sākotnējo rēķina apjomu.

Kad apstiprināsit laboto rēķinu, sākotnējais izmaksātais pārdošanas apjoms tiek apgriezts un tiek izveidots jauns rēķins par pārdošanu. Ja daudzums tika samazināts, starpība izveidos jaunu rēķinā neietvertu pārdošanas faktisko vērtību. Piemēram, ja sākotnējais apmaksātais pārdošanas apjoms ir astoņas stundas un labojošā rēķina rindu informācijai ir samazināts daudzums uz sešām stundām, sākotnējā izmaksu rinda tiek atsaukta un tiek izveidotas divas jaunas faktiskās vērtības.

- Rēķins par pārdošanu ir fiksētas sešas stundas.
- Neiekasēts pārdošanas apjoms atlikušajām divām stundām. Šo transakciju var izrakstīt vēlāk vai atzīmēt kā nepiemērojamu atkarībā no vienošanās ar klientu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
