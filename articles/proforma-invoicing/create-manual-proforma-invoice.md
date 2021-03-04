---
title: Izveidot manuālu pro formas rēķinu
description: Šajā tēmā ir sniegta informācija par pro formas rēķina izveidi.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d3c84664f1b0701db17f0c05654e0c99bb6c640
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128067"
---
# <a name="create-a-manual-proforma-invoice"></a>Izveidot manuālu pro formas rēķinu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Rēķinu izveide ir noderīga, jo tie projektu vadītājiem sniedz otro apstiprinājuma līmeni pirms rēķinu izveides klientiem. Pirmais apstiprināšanas līmenis tiek pabeigts, kad tiek apstiprināti projekta darba grupas dalībnieku iesniegtie laika un izdevumu ieraksti.

Dynamics 365 Project Operations nav izveidota, lai ģenerētu uz klientiem vērstus rēķinus tālāk norādīto iemeslu dēļ.

- Tajā nav iekļauta informācija par nodokļiem.
- Tā nevar pārvērst citas valūtas uz rēķina valūtu, izmantojot pareizi konfigurētus valūtas kursus.
- Nevar pareizi formatēt rēķinus, lai tos varētu izdrukāt.

Tā vietā varat izmantot finanšu vai grāmatvedības sistēmu, lai izveidotu uz klientiem vērstus rēķinus, kuri izmanto informāciju no ģenerētajiem rēķina priekšlikumiem.

## <a name="creating-project-invoices"></a>Projektu rēķinu izveide

Projekta rēķinus var izveidot pa vienam vai arī lielapjomā. Tos varat izveidot manuāli, vai arī var konfigurēt tā, lai tie tiktu ģenerēti automātikā palaišanā.

### <a name="manually-create-project-invoices"></a>Manuāla projektu rēķinu izveide 

Saraksta lapā **Projekta līgumi** varat izveidot projekta rēķinus atsevišķi katram projekta līgumam, kā arī var izveidot lielapjoma rēķinus vairākiem projekta līgumiem.

Veiciet šīs darbības, lai izveidotu rēķinu konkrētam projekta līgumam.

- Saraksta lapā **Projekta līgumi** atveriet projekta līgumu un pēc tam atlasiet **Izveidot rēķinu**.

    Rēķins tiek ģenerēts visām atlasītā projekta līguma transakcijām, kuru statuss ir **Gatavs rēķinam**. Šīs transakcijas ietver laiku, izdevumus, atskaites punktus un produktu līguma rindas.

Lai izveidotu lielapjoma rēķinus, veiciet tālāk norādītās darbības.

1. Sarakstu lapā **Projekta līgumi** atlasiet vienu vai vairākus projekta līgumus, kuriem jāizveido rēķins, un pēc tam atlasiet **Izveidot projekta rēķinus**.

    Brīdinājuma ziņojums informē par to, ka pirms rēķinu izveidošanas var būt aizkave. Tiek parādīts arī process.

2. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

    Rēķins tiek ģenerēts visām līguma rindas transakcijām, kuru statuss ir **Gatavs rēķinam**. Šīs transakcijas ietver laiku, izdevumus, atskaites punktus un produktu līguma rindas.

3. Lai skatītu ģenerētos rēķinus, dodieties uz **Pārdošana** \> **Maksas noteikšana** \> **Rēķini**. Katram projekta līgumam tiks parādīts viens rēķins.

### <a name="set-up-automated-creation-of-project-invoices"></a>Projektu rēķinu automātiskas izveides iestatīšana 

Veiciet tālāk norādītās darbības, lai konfigurētu automātisko rēķina izpildi.

1. Dodieties uz **Iestatījumi** \> **Lielapjoma darbi**.
2. Izveidojiet lielapjoma darbu un nosauciet to **Project Operations rēķinu izveide**. Lielapjoma darbu nosaukumā ir jāiekļauj termins “Rēķinu izveide”.
3. Laukā **Darba tips** atlasiet vienumu **Nav**. **Pēc noklusējuma** Biežuma aizkave **Aktīvs** opcijas ir iestatītas uz **Jā.**
4. Atlasiet **Palaist darbplūsmu**. Dialoglodziņā **Meklēt ierakstu** redzēsiet trīs darbplūsmas.

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Atlasiet vienumu **ProcessRunCaller** un pēc tam **Pievienot**.
6. Nākamajā dialoglodziņā atlasiet **Labi**. Darbplūsma **Miegs** seko darbplūsmai **Apstrādāt**.

    5. darbībā varat arī atlasīt **ProcessRunner**. Pēc tam, kad atlasā **Labi** **Apstrādāt** darbplūsmai seko **Miegs** darbplūsma.

**ProcessRunCaller** un **ProcessRunner** darbplūsmas veido rēķinus. **ProcessRunCaller** izsauc **ProcessRunner**. **ProcessRunner** ir darbplūsma, kas faktiski izveido rēķinus. Tā darbojas caur visām līguma rindām, kurām ir jāizveido rēķini, un izveido rēķinu šīm rindām. Lai noteiktu līguma rindas, kurām jāizveido rēķini, darbs tiek apskatīts līguma rindu rēķina izpildes datumos. Ja līguma rindām, kas attiecas uz vienu līgumu, ir vienāds rēķina izpildes datums, darījumi tiek apvienoti vienā rēķinā, kurā ir divas rēķina rindas. Ja nav nevienas transakcijas rēķinu izveidei, darbs izlaiž rēķina veidošanu.

Kad **ProcessRunner** ir beidzis darboties, tas izsauc **ProcessRunCaller**, nodrošina beigu laiku un ir slēgts. **ProcessRunCaller** pēc tam sāk skaitīt laiku, kas darbojas 24 stundas no norādītā beigu laika. Taimera laika skaitīšanas beigās **ProcessRunCaller** tiek slēgts.

Lielapjoma izpildes darbs rēķinu izveidošanai ir kārtējais darbs. Ja šis pakešapstrādes process ir palaists vairākas reizes, tiek izveidoti vairāki darba gadījumi un var tikt izraisītas kļūdas. Tāpēc pakešapstrāde jāsāk tikai vienu reizi, un tā ir jārestartē tikai tad, ja tā pārstāj darboties.

> [!NOTE]
> Lielapjomu rēķinu izveide darbojas vienīgi projekta līguma rindām, kuras ir konfigurējuši rēķinu grafiki. Līguma rindai ar fiksētu cenas aprēķina metodi jābūt konfigurētiem atskaites punktiem. Projekta līguma rindai ar laika un materiālu aprēķinu metodi ir jābūt iestatītam datuma bāzes rēķina grafikam. Tas pats attiecas uz līguma rindu, kuras pamatā ir projekts.      
 
### <a name="edit-a-draft-invoice"></a>Melnraksta rēķina rediģēšana

Izveidojot projekta rēķina melnrakstu, visi nepārdoto pārdošanas transakciju ieraksti, kas tika izveidoti, kad tika apstiprināti laika un izdevumu ieraksti, tiek iekļauti rēķinā. Varat veikt tālāk norādītos pielāgojumus, kamēr rēķins vēl nav iekļauts melnraksta stadijā.

- Dzēsiet vai rediģējiet informāciju par rēķina rindu.
- Rediģējiet un pielāgojiet daudzuma un norēķinu tipu.
- Precīzi pievienojiet laiku, izdevumus un maksas kā rēķina transakcijas. Šo līdzekli var izmantot, ja rēķina rinda ir kartēta uz līguma rindu, kas ļauj veikt šīs transakciju klases.

Atlasiet vienumu **Apstiprināt**, lai apstiprinātu rēķinu. Apstiprinājuma darbība ir vienvirziena darbība. Kad atlasāt **Apstiprināt**, sistēma padara rēķinu par tikai lasāmu un izveido izrakstīto pārdošanas darījumu no katras rēķina rindas detalizētās vērtības katrā rēķina rindā. Ja rēķina rindas informācija attiecas uz nepārdotu pārdošanas apjomu faktisko, sistēma arī apvērš nepārdoto pārdošanas darījumu faktisko. (Jebkura rēķina rindas informācija, kas izveidota no laika vai izdevumu ieraksta, atsaucas uz nepārdotu pārdošanas darījumu.) Galvenās virsgrāmatas ieviešanas sistēmas var izmantot šo apvērsi, lai nepabeigtu projekta darbu (NP) grāmatvedības vajadzībām.

### <a name="correct-a-confirmed-invoice"></a>Apstiprināta rēķina labošana

Apstiprinātos rēķinus var rediģēt (labot). Kad esat izlabojis apstiprinātu rēķinu, tiek izveidots jauns melnraksta labojošais rēķins. Tā kā tiek pieņemts, ka vēlaties atsaukt visas transakcijas un daudzumus no sākotnējā rēķina, šis labojošais rēķins ietver visas darbības no sākotnējā rēķina un visi tajā ietvertie daudzumi ir 0 (nulle).

Ja transakcijām nav nepieciešama labošana, tās var noņemt no melnraksta labojošā rēķina. Ja vēlaties atsaukt vai atgriezt tikai daļēju daudzumu, var rediģēt rindas informācijas lauku **Daudzums**. Ja atverat rēķina rindas informāciju, varat redzēt sākotnējo rēķina apjomu. Pašreizējo rēķina daudzumu var rediģēt, lai tas būtu mazāks vai lielāks par sākotnējo rēķina apjomu.

Kad apstiprināsit laboto rēķinu, sākotnējais izmaksātais pārdošanas apjoms tiek apgriezts un tiek izveidots jauns rēķins par pārdošanu. Ja daudzums tika samazināts, starpība izraisīs jaunu nemaksātu pārdošanas darījumu. Piemēram, ja sākotnējais apmaksātais pārdošanas apjoms ir astoņas stundas un labojošā rēķina rindu informācijai ir samazināts daudzums uz sešām stundām, sākotnējā izmaksu rinda tiek atgriezta un tiek izveidoti divi jauni reālie dati.

- Rēķins par pārdošanu ir fiksētas sešas stundas.
- Neiekasēts pārdošanas apjoms atlikušajām divām stundām. Šo transakciju var izrakstīt vēlāk vai atzīmēt kā nepiemērojamu atkarībā no vienošanās ar klientu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]