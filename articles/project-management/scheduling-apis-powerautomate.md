---
title: Projekta grafika API izmantošana ar Power Automate
description: Šajā rakstā ir sniegts plūsmas paraugs, kurā izmantotas projekta grafika programmas programmēšanas saskarnes (API).
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

Šajā rakstā ir aprakstīts plūsmas paraugs, kurā parādīts, kā izveidot pilnīgu projekta plānu, izmantojot Microsoft Power Automate, kā izveidot darbību kopu un kā atjaunināt entītiju. Piemērā tiek parādīts, kā izveidot projektu, projekta darba grupas dalībnieku, darbību kopas, projekta uzdevumus un resursu piešķīrumus. Šajā rakstā arī izskaidrots, kā atjaunināt entītiju un izpildīt darbību kopu.

Tālāk ir sniegts pilns darbību saraksts, kas šajā rakstā ir dokumentētas parauga plūsmā.

1. [PowerApps trigera izveidošana](#1)
2. [Projekta izveidošana](#2)
3. [Darba grupas dalībnieka mainīgā inicializēšana](#3)
4. [Vispārēja darba grupas dalībnieka izveide](#4)
5. [Darbību kopas izveide](#5)
6. [Projekta intervāla izveide](#6)
7. [Saites statusa mainīgā inicializēšana](#7)
8. [Uzdevumu skaita mainīgā inicializēšana](#8)
9. [Projekta uzdevuma ID mainīgā inicializēšana](#9)
10. [Paveikt līdz](#10)
11. [Projekta uzdevuma iestatīšana](#11)
12. [Projekta uzdevuma izveidošana](#12)
13. [Resursu piešķīruma izveidošana](#13)
14. [Mainīgā samazināšana](#14)
15. [Projekta uzdevuma pārdēvēšana](#15)
16. [Darbību kopas palaišana](#16)

## <a name="assumptions"></a>Pieņēmumi

Šajā rakstā tiek pieņemts, ka jums ir pamatzināšanas par Dataverse platformu, mākoņa plūsmām un projekta grafika programmas programmēšanas saskarni (API). Papildinformāciju skatiet šī raksta sadaļā [Atsauces](#references).

## <a name="create-a-flow"></a>Plūsmas izveide

### <a name="select-an-environment"></a>Atlasiet vidi

Savā vidē varat izveidot Power Automate plūsmu.

1. Pārejiet uz <https://flow.microsoft.com> un izmantojiet savus administratora akreditācijas datus, lai pieteiktos.
2. Augšējā labējā stūrī atlasiet **Vides**.
3. Sarakstā atlasiet vidi, kurā instalēta programma Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Risinājuma izveide

Izpildiet šīs darbības, lai izveidotu [par risinājumu informētu plūsmu](/power-automate/overview-solution-flows). Izveidojot par risinājumu informētu plūsmu, varat plūsmu vieglāk eksportēt, lai to izmantotu vēlāk.

1. Navigācijas rūtī atlasiet vienumu **Risinājumi**.
2. Lapā **Risinājumi** atlasiet **Jauns risinājums**.
3. Dialoglodziņā **Jauns risinājums** iestatiet obligātos laukus un pēc tam atlasiet **Izveidot**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>1. darbība: PowerApps trigera izveidošana

1. Lapā **Risinājumi** atlasiet izveidoto risinājumu un pēc tam atlasiet **Jauns**.
2. Kreisajā rūtī atlasiet **Mākoņa plūsmas** \> **Automatizācija** \> **Mākoņa plūsma** \> **Tūlītēja**.
3. Laukā **Plūsmas nosaukums** ievadiet **Plānota API demonstrācijas plūsma**.
4. Sarakstā **Izvēlieties, kā izraisīt šo plūsmu** atlasiet **Power Apps**. Veidojot aktivizēšanas Power Apps kārtulu, loģiku nosakāt jūs kā autors. Šajā rakstā ievades parametrus testēšanas nolūkos atstājiet tukšus.
5. Atlasiet **Izveidot**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. darbība: Izveidot projektu

Lai izveidotu parauga projektu, izpildiet tālāk aprakstītās darbības.

1. Izveidotajā plūsmā atlasiet **Jauna darbība**.

    ![Jaunas darbības pievienošana](media/newstep.png)

2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **izpildīt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.

    ![Darbības atlasīšana.](media/chooseactiontab.png)

3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.

![Darbības pārdēvēšana.](media/renamestep.png)

4. Pārdēvējiet darbību **Izveidot projektu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_CreateButtonV1**.
6. Laukā **msdyn\_subject** atlasiet **Pievienot dinamisku saturu**.
7. Cilnes **Izteiksme** funkciju laukā ievadiet **Projekta nosaukums - utcNow()**.
8. Atlasiet **Labi**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>3. darbība. Darba grupas dalībnieka mainīgā inicializēšana

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Inicializēt darba grupas dalībnieku**.
5. Laukā **Nosaukums** ievadiet **TeamMemberAction**.
6. Laukā **Tips** atlasiet **Virkne**.
7. Laukā **Vērtība** ievadiet **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>4. darbība. Vispārēja darba grupas dalībnieka izveide

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **izpildīt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot darba grupas dalībnieku**.
5. Laukam **Darbības nosaukums** atlasiet **TeamMemberAction** dialoglodziņā **Dinamiskais saturs**.
6. Laukā **Darbības parametri** ievadiet tālāk norādīto informāciju par parametru.

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

    - **\@\@odata.type** — entītijas nosaukums. Piemēram, ievadiet **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** — projekta darba grupas ID primārā atslēga. Šī vērtība ir vispārēji unikālā identifikatora (GUID) izteiksme.   ID tiek ģenerēts no izteiksmes cilnes.

    - **msdyn\_project\@odata.bind** — atbildīgā projekta ID. Šī vērtība ir dinamisks saturs, kas tiek veidots no darbības “Izveidot projektu” atbildes. Pārliecinieties, vai ir ievadīts pilnais ceļš un pievienots dinamisks saturs iekavās. Ir nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** — darba grupas dalībnieka vārds. Piemēram, ievadiet **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>5. darbība. Darbību kopas izveide

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **izpildīt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot darbību kopu**.
5. Laukā **Darbības nosaukums** atlasiet pielāgoto darbību **msdyn\_CreateOperationSetV1** Dataverse.
6. Laukā **Apraksts** ievadiet **ScheduleAPIDemoOperationSet**.
7. Laukā **Projekts** ievadiet **/msdyn\_projects(**.
8. Dialoglodziņā **Dinamiskais saturs** atlasiet **msdyn\_CreateProjectV1Response ProjectId**.
9. Laukā **Projekts** ievadiet **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6. darbība. Projekta intervāla izveide

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **pievienot jaunu rindu**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot intervālu**.
5. Laukā **Tabulas nosaukums** atlasiet **Projekta intervāli**.
6. Laukā **Nosaukums** ievadiet **ScheduleAPIDemoBucket1**.
7. Laukā **Projekts** atlasiet **msdyn\_CreateProjectV1Response ProjectId** dialoglodziņā **Dinamiskais saturs**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>7. darbība. Saites statusa mainīgā inicializēšana

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Init linkstatus**.
5. Laukā **Nosaukums** ievadiet **linkstatus**.
6. Laukā **Tips** atlasiet **Vesels skaitlis**.
7. Laukā **Vērtība** ierakstiet **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>8. darbība. Uzdevumu skaita mainīgā inicializēšana

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Inicializēt uzdevumu skaitu**.
5. Laukā **Nosaukums** ievadiet **uzdevumu skaits**.
6. Laukā **Tips** atlasiet **Vesels skaitlis**.
7. Laukā **Vērtība** ierakstiet **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>9. darbība. Projekta uzdevuma ID mainīgā inicializēšana

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **inicializēt mainīgo**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Init ProjectTaskID**.
5. Laukā **Nosaukums** ievadiet **uzdevumu skaits**.
6. Laukā **Tips** atlasiet **Virkne**.
7. Lauka **Vērtība** izteiksmes veidotājā ievadiet **guid()**.

## <a name="step-10-do-until"></a><a id="10"></a>10. darbība. Paveikt līdz

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **paveikt līdz**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Nosacījuma priekšrakstā pirmo vērtību iestatiet uz mainīgo **uzdevumu skaits** no dialoglodziņa **Dinamiskais saturs** dialoglodziņa.
4. Iestatiet nosacījumu uz **mazāks par vai vienāds ar**.
5. Iestatiet otro vērtību nosacījuma priekšrakstā uz **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>11. darbība. Projekta uzdevuma iestatīšana

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **iestatīt mainīgo**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Jaunajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Iestatīt projekta uzdevumu**.
5. Laukā **Nosaukums** atlasiet **msdyn\_projecttaskid**.
6. Lauka **Vērtība** izteiksmes veidotājā ievadiet **guid()**.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12. darbība: Projekta uzdevuma izveidošana

Veiciet šīs darbības, lai izveidotu projekta uzdevumu ar unikālu ID, kas pieder pašreizējam projektam un projekta intervālam, ko izveidojāt.

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **izpildīt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Šajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot projekta uzdevumu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_PssCreateV1**.
6. Laukā **Entītija** ievadiet sekojošo parametru informāciju.

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

    - **\@\@odata.type** — entītijas nosaukums. Piemēram, ievadiet **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** — uzdevuma unikālais ID. Šī vērtība jāiestata uz dinamisku mainīgo no **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** — atbildīgā projekta ID. Šī vērtība ir dinamisks saturs, kas tiek veidots no darbības “Izveidot projektu” atbildes. Pārliecinieties, vai ir ievadīts pilnais ceļš un pievienots dinamisks saturs iekavās. Ir nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** — jebkurš uzdevuma nosaukums.
    - **msdyn\_projectbucket\@odata.bind** — projekta intervāls, kurā iekļauti uzdevumi. Šī vērtība ir dinamisks saturs, kas tiek veidots no darbības “Izveidot intervālu” atbildes. Pārliecinieties, vai ir ievadīts pilnais ceļš un pievienots dinamisks saturs iekavās. Ir nepieciešamas pēdiņas. Piemēram, ievadiet **"/msdyn\_projectbuckets(PIEVIENOJIET DINAMISKO SATURU)"**.
    - **msdyn\_start** — sākuma datuma dinamiskais saturs. Piemēram, rītdiena tiks parādīta kā **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** — ieplānotais sākšanas datums. Piemēram, rītdiena tiks parādīta kā **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** — ieplānotais beigu datums. Atlasiet datumu nākotnē. Piemēram, norādiet **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** — saites statuss. Piemēram, ievadiet **"192350000"**.

7. Laukā **OperationSetId** atlasiet **msdyn\_CreateOperationSetV1Response** dialoglodziņā **Dinamiskais saturs**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>13. darbība. Resursa piešķīruma izveide

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **izpildīt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Šajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Izveidot piešķīrumu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_PssCreateV1**.
6. Laukā **Entītija** ievadiet sekojošo parametru informāciju.

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

7. Laukā **OperationSetId** atlasiet **msdyn\_CreateOperationSetV1Response** dialoglodziņā **Dinamiskais saturs**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>14. darbība. Mainīgā samazināšana

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **samazināt mainīgo**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Laukā **Nosaukums** atlasiet **uzdevumu skaits**.
4. Laukā **Vērtība** ierakstiet **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15. darbība. Projekta uzdevuma pārdēvēšana

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **izpildīt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Šajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Pārdēvēt projekta uzdevumu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_PssUpdateV1**.
6. Laukā **Entītija** ievadiet sekojošo parametru informāciju.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Laukā **OperationSetId** atlasiet **msdyn\_CreateOperationSetV1Response** dialoglodziņā **Dinamiskais saturs**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>16. darbība. Darbību kopas palaišana

1. Plūsmā atlasiet **Jauna darbība**.
2. Dialoglodziņa **Darbības izvēle** meklēšanas laukā ievadiet **izpildīt nesaistītu darbību**. Pēc tam cilnē **Darbības** atlasiet darbību no rezultātu saraksta.
3. Šajā darbībā atlasiet daudzpunkti (**...**) un pēc tam atlasiet vienumu **Pārdēvēt**.
4. Pārdēvējiet darbību **Izpildīt darbību kopu**.
5. Laukā **Darbības nosaukums** atlasiet **msdyn\_ExecuteOperationSetV1**.
6. Laukā **OperationSetId** atlasiet **msdyn\_CreateOperationSetV1Response OperationSetId** dialoglodziņā **Dinamiskais saturs**.

## <a name="references"></a>Atsauces

- [Pārskats par plūsmu integrēšanu ar Dataverse — Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām](schedule-api-preview.md)
- [Pārskats par mākoņa plūsmām — Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pārskats: par risinājumu informētas plūsmas — Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
