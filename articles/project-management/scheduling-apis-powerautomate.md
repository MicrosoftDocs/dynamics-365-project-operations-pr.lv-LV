---
title: Projekta grafika API izmantošana ar Power Automate
description: Šī tēma nodrošina parauga plūsmu, kas izmanto projekta grafika lietojumprogrammu interfeisus (API).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597715"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projekta grafika API izmantošana ar Power Automate

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Šajā tēmā ir aprakstīta plūsmas paraugs, kas parāda, kā izveidot pilnu projekta plānu, izmantojot Microsoft Power Automate, kā izveidot operāciju kopu un kā atjaunināt entītiju. Piemērs parāda, kā izveidot projektu, projekta grupas dalībnieku, operāciju kopas, projekta uzdevumus un resursu piešķires. Šajā tēmā ir arī paskaidrots, kā atjaunināt entītiju un izpildīt operāciju kopu.

Tālāk ir sniegts pilnīgs to darbību saraksts, kas ir dokumentētas parauga plūsmā šajā tēmā:

1. [Trigera PowerApps izveide](#1)
2. [Projekta izveidošana](#2)
3. [Grupas dalībnieka mainīgā inicializēšana](#3)
4. [Vispārīga grupas dalībnieka izveide](#4)
5. [Operāciju kopas izveide](#5)
6. [Izveidot projekta grupu](#6)
7. [Saites statusa mainīgā inicializēšana](#7)
8. [Inicializēt mainīgo uzdevumu skaitam](#8)
9. [Inicializēt projekta uzdevuma ID mainīgo](#9)
10. [Dariet, līdz](#10)
11. [Iestatīt projekta uzdevumu](#11)
12. [Izveidot projekta uzdevumu](#12)
13. [Izveidot resursu piešķiri](#13)
14. [Mainīgā atsaistīšana](#14)
15. [Projekta uzdevuma pārdēvēšana](#15)
16. [Operāciju kopas palaišana](#16)

## <a name="assumptions"></a>Pieņēmumi

Šajā tēmā tiek pieņemts, ka jums ir pamatzināšanas par Dataverse platformu, mākoņa plūsmām un projekta grafika lietojumprogrammu programmēšanas interfeisu (API). Papildinformāciju skatiet tālāk šīs tēmas [sadaļā Atsauces](#references).

## <a name="create-a-flow"></a>Plūsmas izveide

### <a name="select-an-environment"></a>Atlasiet vidi

Jūs varat izveidot Power Automate plūsmu savā vidē.

1. Dodieties uz <https://flow.microsoft.com> un izmantojiet administratora akreditācijas datus, lai pieteiktos.
2. Augšējā labajā stūrī atlasiet **Vide**.
3. Sarakstā atlasiet vidi, kurā Dynamics 365 Project Operations tā ir instalēta.

### <a name="create-a-solution"></a>Risinājuma izveide

Veiciet tālāk norādītās darbības, lai izveidotu plūsmu [, kas](/power-automate/overview-solution-flows) apzinās risinājumu. Izveidojot plūsmu, kas apzinās risinājumu, varat vieglāk eksportēt plūsmu, lai to izmantotu vēlāk.

1. Navigācijas rūtī atlasiet **Risinājumi**.
2. **Lapā Risinājumi** atlasiet **Jauns risinājums**.
3. Dialoglodziņā **Jauns risinājums** iestatiet nepieciešamos laukus un pēc tam atlasiet **Izveidot**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1. darbība: izveidojiet trigeri PowerApps

1. **Lapā Risinājumi** atlasiet izveidoto risinājumu un pēc tam atlasiet **Jauns**.
2. Kreisajā rūtī atlasiet **Cloud flows** \> **Automation** \> **Cloud flow** \> **Instant.**
3. Laukā **Plūsmas nosaukums** ievadiet **Schedule API Demo Flow**.
4. **Sarakstā Izvēlieties, kā aktivizēt šo plūsmas plūsmu** atlasiet **Power Apps**. Veidojot trigeri Power Apps, loģika ir atkarīga no jums kā autora. Šajā tēmā testēšanas nolūkos atstājiet ievades parametrus tukšus.
5. Atlasiet **Izveidot**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. darbība: Izveidot projektu

Veiciet šīs darbības, lai izveidotu projekta paraugu.

1. Izveidotajā plūsmā atlasiet **Jauns solis**.

    ![Jauna soļa pievienošana.](media/newstep.png)

2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **Veikt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.

    ![Operācijas atlasīšana.](media/chooseactiontab.png)

3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.

![Soļa pārdēvēšana.](media/renamestep.png)

4. Pārdēvējiet darbību **Izveidot projektu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_ CreateProjectV1**.
6. Msdyn tēmas **\_ laukā atlasiet** Pievienot dinamisko saturu **.**
7. **Cilnes Izteiksme** laukā Funkcija ievadiet **Projekta nosaukums - utcNow()**.
8. Atlasiet **Labi**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3. darbība: grupas dalībnieka mainīgā inicializēšana

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Init grupas dalībnieks**.
5. Laukā **Nosaukums** ievadiet **TeamMemberAction**.
6. Laukā **Tips** atlasiet **Virkne**.
7. Laukā **Vērtība** ievadiet **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4. darbība: izveidojiet vispārēju grupas dalībnieku

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **Veikt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot grupas dalībnieku**.
5. Laukam **Darbības nosaukums** dialoglodziņā Dinamiskais **saturs** atlasiet **TeamMemberAction**.
6. Laukā **Darbības parametri** ievadiet šādu informāciju par parametru.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Šeit ir parametru skaidrojums:

    - **\@\@ odata.type** – entītijas nosaukums. Piemēram, ievadiet **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – projekta komandas ID primārā atslēga. Vērtība ir globāli unikāla identifikatora (GUID) izteiksme.   ID tiek ģenerēts no izteiksmes cilnes.

    - **msdyn\_ project\@ odata.bind** – Projekta ID īpašnieka projektam. Vērtība būs dinamisks saturs, kas nāk no soļa "Izveidot projektu" atbildes. Pārliecinieties, vai ievadāt pilnu ceļu un starp iekavām pievienojat dinamisku saturu. Nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ vārds** — komandas dalībnieka vārds. Piemēram, ievadiet **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5. darbība: operāciju kopas izveide

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **Veikt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **izveidot operāciju kopu**.
5. Laukā **Darbības nosaukums** atlasiet pielāgoto **darbību msdyn\_ CreateOperationSetV1** Dataverse.
6. Laukā **Apraksts** ievadiet **ScheduleAPIDemoOperationSet**.
7. Laukā **Projekts** ievadiet **/msdyn\_ projects(**.
8. Dialoglodziņā Dinamiskais **saturs** atlasiet **msdyn\_ CreateProjectV1Response ProjectId**.
9. Laukā **Projekts** ievadiet **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6. darbība: izveidojiet projekta spaini

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **pievienot jaunu rindu**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot kausu**.
5. Laukā **Tabulas nosaukums** atlasiet **Projektu kausi**.
6. Laukā **Nosaukums** ievadiet **ScheduleAPIDemoBucket1**.
7. Laukam Projekts dialoglodziņā **Dinamiskais** saturs **atlasiet \_ msdyn** CreateProjectV1Response ProjectId **.**

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7. darbība: inicializējiet saites statusa mainīgo

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Init linkstatus**.
5. Laukā **Nosaukums** ievadiet **linkstatus**.
6. Laukā **Tips** atlasiet **Vesels skaitlis**.
7. Laukā **Vērtība** ievadiet **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8. darbība: inicializējiet mainīgo uzdevumu skaitam

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Init Uzdevumu** skaits.
5. Laukā **Nosaukums** ievadiet **uzdevumu** skaitu.
6. Laukā **Tips** atlasiet **Vesels skaitlis**.
7. Laukā **Vērtība** ievadiet **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9. darbība: projekta uzdevuma ID mainīgā inicializēšana

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Init ProjectTaskID**.
5. Laukā **Nosaukums** ievadiet **uzdevumu** skaitu.
6. Laukā **Tips** atlasiet **Virkne**.
7. Laukam **Vērtība** ievadiet **GUID()** izteiksmju veidotājā.

## <a name="step-10-do-until"></a><a id="10"></a> 10. darbība: veiciet līdz

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet darīt **līdz**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Iestatiet pirmo vērtību nosacījuma priekšrakstā uz **uzdevumu** skaita mainīgo no dialoglodziņa Dinamiskais **saturs**.
4. Iestatiet nosacījumu mazāku par **vienādu**.
5. Iestatiet otro vērtību nosacījuma priekšrakstā uz **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11. darbība: iestatiet projekta uzdevumu

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **iestatīto mainīgo**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Jaunajā solī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Iestatīt projekta uzdevumu**.
5. Laukā **Nosaukums** atlasiet **msdyn\_ projecttaskid**.
6. Laukam **Vērtība** ievadiet **GUID()** izteiksmju veidotājā.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. darbība: izveidojiet projekta uzdevumu

Veiciet šīs darbības, lai izveidotu projekta uzdevumu ar unikālu ID, kas pieder pašreizējam projektam un izveidotajam projekta grupai.

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **Veikt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot projekta uzdevumu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_ PssCreateV1**.
6. Laukā **Entītija** ievadiet šādu parametru informāciju.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Šeit ir parametru skaidrojums:

    - **\@\@ odata.type** – entītijas nosaukums. Piemēram, ievadiet **"Microsoft.Dynamics.CRM.msdyn\_ projecttaset"**.
    - **msdyn\_ projecttaskid** – uzdevuma unikālais ID. Vērtība jāiestata uz dinamisku mainīgo no **msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – Projekta ID īpašnieka projektam. Vērtība būs dinamisks saturs, kas nāk no soļa "Izveidot projektu" atbildes. Pārliecinieties, vai ievadāt pilnu ceļu un starp iekavām pievienojat dinamisku saturu. Nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ tēma** — jebkurš uzdevuma nosaukums.
    - **msdyn\_ projectbucket\@ odata.bind** – Projekta spainis, kurā ir uzdevumi. Vērtība būs dinamisks saturs, kas nāk no soļa "Izveidot kausu" atbildes. Pārliecinieties, vai ievadāt pilnu ceļu un starp iekavām pievienojat dinamisku saturu. Nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ sākums** — dinamisks saturs sākuma datumam. Piemēram, rītdiena tiks attēlota kā **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduledstart** – plānotais sākuma datums. Piemēram, rītdiena tiks attēlota kā **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** — plānotais beigu datums. Atlasiet datumu nākotnē. Piemēram, norādiet **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – saites statuss. Piemēram, ievadiet **"192350000"**.

7. **Laukam OperationSetId** dialoglodziņā **Dinamiskais saturs\_ atlasiet** msdyn **CreateOperationSetV1Response**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. darbība: izveidojiet resursu piešķiri

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **Veikt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot piešķiri**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_ PssCreateV1**.
6. Laukā **Entītija** ievadiet šādu parametru informāciju.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. **Laukam OperationSetId** dialoglodziņā **Dinamiskais saturs\_ atlasiet** msdyn **CreateOperationSetV1Response**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14. darbība: mainīgā atmešana

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **samazināšanas mainīgo**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Laukā **Nosaukums** atlasiet **uzdevumu** skaitu.
4. Laukā **Vērtība** ievadiet **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15. darbība: pārdēvējiet projekta uzdevumu

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **Veikt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Pārdēvēt projekta uzdevumu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_ PssUpdateV1**.
6. Laukā **Entītija** ievadiet šādu parametru informāciju.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **Laukam OperationSetId** dialoglodziņā **Dinamiskais saturs\_ atlasiet** msdyn **CreateOperationSetV1Response**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16. darbība: darbību kopas palaišana

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **Veikt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet operāciju rezultātu sarakstā.
3. Darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **izpildes operāciju kopu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_ ExecuteOperationSetV1**.
6. **Laukam OperationSetId** dialoglodziņā **Dinamīda saturs\_ atlasiet** msdyn **CreateOperationSetV1Response OperationSetId**.

## <a name="references"></a>Atsauces

- [Pārskats par to, kā integrēt plūsmas ar Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām](schedule-api-preview.md)
- [Pārskats par mākoņu plūsmām - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pārskats par plūsmām, kas apzinās risinājumus - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
