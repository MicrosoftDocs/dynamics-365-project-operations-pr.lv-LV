---
title: Projekta grafika API izmantošana ar Power Automate
description: Šajā rakstā ir sniegts plūsmas paraugs, kas izmanto lietojumprogrammu interfeisus Project schedule (PROJECT schedule lietojumprogrammu interfeisus (API).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404459"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projekta grafika API izmantošana ar Power Automate

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Šajā rakstā ir aprakstīta plūsmas paraugs, kurā parādīts, kā izveidot pilnīgu projekta plānu, izmantojot Microsoft Power Automate, kā izveidot operāciju kopu un kā atjaunināt entītiju. Piemērā ir parādīts, kā izveidot projektu, projekta grupas dalībnieku, operāciju kopas, projekta uzdevumus un resursu piešķires. Šajā rakstā ir arī paskaidrots, kā atjaunināt entītiju un izpildīt operāciju kopu.

Šis ir pilns to darbību saraksts, kas ir dokumentētas šī raksta parauga plūsmā:

1. [Trigera PowerApps izveide](#1)
2. [Projekta izveidošana](#2)
3. [Mainīgā inicializēšana komandas dalībniekam](#3)
4. [Vispārīga darba grupas dalībnieka izveide](#4)
5. [Operāciju kopas izveide](#5)
6. [Projekta kausa izveide](#6)
7. [Mainīgā inicializēšana saites statusam](#7)
8. [Mainīgo inicializēt uzdevumu skaitam](#8)
9. [Mainīgā inicializēšana projekta uzdevuma ID](#9)
10. [Dariet līdz](#10)
11. [Projekta uzdevuma iestatīšana](#11)
12. [Projekta uzdevuma izveide](#12)
13. [Resursu piešķiršanas izveide](#13)
14. [Mainīgā lieluma pazemināšana](#14)
15. [Projekta uzdevuma pārdēvēšana](#15)
16. [Operāciju kopas palaišana](#16)

## <a name="assumptions"></a>Pieņēmumi

Šajā rakstā tiek pieņemts, ka jums ir pamatzināšanas par Dataverse platformu, mākoņa plūsmām un projekta grafika lietojumprogrammu programmēšanas interfeisu (Project Schedule Application Programming Interface — API). Papildinformāciju [skatiet šī raksta sadaļā Atsauces](#references).

## <a name="create-a-flow"></a>Plūsmas izveide

### <a name="select-an-environment"></a>Atlasiet vidi

Jūs varat izveidot Power Automate plūsmu savā vidē.

1. Dodieties uz <https://flow.microsoft.com> un izmantojiet administratora akreditācijas datus, lai pieteiktos.
2. Augšējā labajā stūrī atlasiet **Vides**.
3. Sarakstā atlasiet vidi, kurā Dynamics 365 Project Operations ir instalēta.

### <a name="create-a-solution"></a>Risinājuma izveide

Veiciet šīs darbības, lai izveidotu [uz risinājumu balstītu plūsmu](/power-automate/overview-solution-flows). Izveidojot uz risinājumu balstītu plūsmu, varat vieglāk eksportēt plūsmu, lai to vēlāk izmantotu.

1. Navigācijas rūtī atlasiet **Risinājumi**.
2. **Lapā Risinājumi** atlasiet **Jauns risinājums**.
3. **Dialoglodziņā Jauns risinājums** iestatiet nepieciešamos laukus un pēc tam atlasiet **Izveidot**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1. darbība: izveidojiet trigeri PowerApps

1. **Lapā Risinājumi** atlasiet izveidoto risinājumu un pēc tam atlasiet **Jauns**.
2. Kreisajā rūtī atlasiet **Cloud flows** \> **Automation** \> **Cloud flow** \> **Instant.**
3. **Laukā Plūsmas nosaukums** ievadiet **Schedule API Demo Flow**.
4. **Sarakstā Izvēlieties, kā aktivizēt šo plūsmu** atlasiet **Power Apps**. Kad izveidojat trigeri Power Apps, loģika ir atkarīga no jums kā autora. Šajā rakstā atstājiet ievades parametrus tukšus testēšanas nolūkos.
5. Atlasiet **Izveidot**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. darbība: Izveidot projektu

Veiciet šīs darbības, lai izveidotu projekta paraugu.

1. Izveidotajā plūsmā atlasiet **Jauns solis**.

    ![Jaunas darbības pievienošana.](media/newstep.png)

2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **veikt nesaistītās darbības**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.

    ![Operācijas izvēle.](media/chooseactiontab.png)

3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.

![Soļa pārdēvēšana.](media/renamestep.png)

4. Pārdēvējiet darbību **Izveidot projektu**.
5. **Laukā Darbības nosaukums** atlasiet **msdyn\_ CreateProjectV1**.
6. Zem tēmas lauka msdyn **atlasiet \_ Pievienot dinamisko saturu**.**·**
7. **Cilnes Izteiksme** laukā Funkcija ievadiet **Projekta nosaukums - utcNow()**.
8. Atlasiet **Labi**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3. solis: Inicializējiet mainīgo komandas dalībniekam

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet soli **Init komandas dalībnieks**.
5. **Laukā Nosaukums** ievadiet **TeamMemberAction**.
6. **Laukā Tips** atlasiet **Virkne**.
7. **Laukā Vērtība** ievadiet **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4. darbība: izveidojiet vispārēju komandas dalībnieku

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **veikt nesaistītās darbības**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot grupas dalībnieku**.
5. **Laukā Darbības nosaukums** dialoglodziņā Dinamiskais **saturs** atlasiet **TeamMemberAction**.
6. **Laukā Darbības parametri** ievadiet šādu parametru informāciju.

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

    - **\@\@ odata.type** — entītijas nosaukums. Piemēram, ievadiet **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** - projekta grupas ID primārā atslēga. Vērtība ir vispārēji unikāla identifikatora (Globally Unique Identifier — GUID) izteiksme.   ID tiek ģenerēts no izteiksmes cilnes.

    - **msdyn\_ project\@ odata.bind** – Piederošā projekta ID. Vērtība būs dinamisks saturs, kas nāk no soļa "Izveidot projektu" atbildes. Pārliecinieties, vai esat ievadījis pilnu ceļu un starp iekavām pievienojis dinamisku saturu. Ir nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ vārds** – Komandas dalībnieka vārds. Piemēram, ievadiet **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5. darbība: izveidojiet operāciju kopu

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **veikt nesaistītās darbības**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot darbību kopu**.
5. **Laukā Darbības nosaukums** atlasiet **pielāgoto darbību msdyn\_ CreateOperationSetV1** Dataverse.
6. **Laukā Apraksts** ievadiet **ScheduleAPIDemoOperationSet**.
7. **Laukā Projekts** ievadiet **/msdyn\_ projekti(**.
8. Dialoglodziņā Dinamiskais **saturs** atlasiet **msdyn\_ CreateProjectV1Response ProjectId**.
9. **Laukā Projekts** ievadiet **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6. darbība: izveidojiet projekta kausu

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **pievienot jaunu rindu**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot kausu**.
5. **Laukā Tabulas nosaukums** atlasiet **Projektu kausi**.
6. Laukā **Nosaukums** ievadiet **ScheduleAPIDemoBucket1**.
7. **Laukā Projekts** dialoglodziņā Dinamiskais saturs **atlasiet \_ msdyn** CreateProjectV1Response **ProjectId**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7. darbība: inicializēt mainīgo saites statusam

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Init linkstatus**.
5. **Laukā Nosaukums** ievadiet **linkstatus**.
6. **Laukā Tips** atlasiet **Vesels skaitlis**.
7. **Laukā Vērtība** ievadiet **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8. solis: Inicializējiet mainīgo uzdevumu skaitam

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet soli **Init uzdevumu** skaits.
5. Laukā **Nosaukums** ievadiet **uzdevumu** skaitu.
6. **Laukā Tips** atlasiet **Vesels skaitlis**.
7. Laukā **Vērtība** ievadiet **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9. solis: inicializējiet mainīgo projekta uzdevuma ID

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Init ProjectTaskID**.
5. Laukā **Nosaukums** ievadiet **uzdevumu** skaitu.
6. **Laukā Tips** atlasiet **Virkne**.
7. **Laukā Vērtība** izteiksmju veidotājā ievadiet **guid().**

## <a name="step-10-do-until"></a><a id="10"></a> 10. solis: dariet līdz

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **darīt** līdz. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Iestatiet pirmo vērtību nosacījuma priekšrakstā uz **uzdevumu** mainīgo skaitu no dialoglodziņa **Dinamiskais saturs**.
4. Iestatiet nosacījumu, lai tas būtu **mazāks par vienādu ar**.
5. Iestatiet otro vērtību nosacījuma priekšrakstā uz **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11. darbība: projekta uzdevuma iestatīšana

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **iestatīt mainīgo**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Iestatīt projekta uzdevumu**.
5. **Laukā Nosaukums** atlasiet **msdyn\_ projecttaskid**.
6. **Laukā Vērtība** izteiksmju veidotājā ievadiet **guid().**

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. darbība: izveidojiet projekta uzdevumu

Veiciet šīs darbības, lai izveidotu projekta uzdevumu, kuram ir unikāls ID, kas pieder pašreizējam projektam un jūsu izveidotajam projekta spainim.

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **veikt nesaistītās darbības**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot projekta uzdevumu**.
5. **Laukā Darbības nosaukums** atlasiet **msdyn\_ PssCreateV1**.
6. Laukā Entītija **ievadiet** šādu parametru informāciju.

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

    - **\@\@ odata.type** — entītijas nosaukums. Piemēram, ievadiet **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – Uzdevuma unikālais ID. Vērtība jāiestata uz dinamisku mainīgo no **msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – Piederošā projekta ID. Vērtība būs dinamisks saturs, kas nāk no soļa "Izveidot projektu" atbildes. Pārliecinieties, vai esat ievadījis pilnu ceļu un starp iekavām pievienojis dinamisku saturu. Ir nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ subject** – Jebkurš uzdevuma nosaukums.
    - **msdyn\_ projectbucket\@ odata.bind** - projekta kauss, kurā ir uzdevumi. Vērtība būs dinamisks saturs, kas nāk no soļa "Izveidot kausu" atbildes. Pārliecinieties, vai esat ievadījis pilnu ceļu un starp iekavām pievienojis dinamisku saturu. Ir nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ start** – Dinamisks saturs sākuma datumam. Piemēram, rītdiena tiks attēlota kā **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduledstart** – Plānotais sākuma datums. Piemēram, rītdiena tiks attēlota kā **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** - Plānotais beigu datums. Atlasiet datumu nākotnē. Piemēram, norādiet **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** - saites statuss. Piemēram, ievadiet **"192350000"**.

7. **Laukā OperationSetId** dialoglodziņā Dinamiskais saturs **atlasiet \_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. darbība: resursu piešķiršanas izveide

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **veikt nesaistītās darbības**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot uzdevumu**.
5. **Laukā Darbības nosaukums** atlasiet **msdyn\_ PssCreateV1**.
6. Laukā Entītija **ievadiet** šādu parametru informāciju.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. **Laukā OperationSetId** dialoglodziņā Dinamiskais saturs **atlasiet \_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14. solis: mainīgā lieluma pazemināšana

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **decrement mainīgo**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Laukā **Nosaukums** atlasiet **uzdevumu** skaitu.
4. Laukā **Vērtība** ievadiet **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15. darbība: projekta uzdevuma pārdēvēšana

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **veikt nesaistītās darbības**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Projekta uzdevuma** pārdēvēšana.
5. **Laukā Darbības nosaukums** atlasiet **msdyn\_ PssUpdateV1**.
6. Laukā Entītija **ievadiet** šādu parametru informāciju.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **Laukā OperationSetId** dialoglodziņā Dinamiskais saturs **atlasiet \_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16. solis: palaidiet operāciju kopu

1. Plūsmā atlasiet **Jauns solis**.
2. Dialoglodziņa **Operācijas** izvēle meklēšanas laukā ievadiet **veikt nesaistītās darbības**. Pēc tam **cilnē Darbības** atlasiet darbību rezultātu sarakstā.
3. Darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pārdēvēt**.
4. Pārdēvējiet darbību **Izpildes operāciju kopa**.
5. **Laukā Darbības nosaukums** atlasiet **msdyn\_ ExecuteOperationSetV1**.
6. Laukā OperationSetId **dialoglodziņā Dinamīda saturs** atlasiet **msdyn\_ CreateOperationSetV1Response OperationSetId** **.**

## <a name="references"></a>Atsauces

- [Pārskats par to, kā integrēt plūsmas ar Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām](schedule-api-preview.md)
- [Pārskats par mākoņa plūsmām - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pārskats par plūsmām, kas saistītas ar risinājumiem - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
