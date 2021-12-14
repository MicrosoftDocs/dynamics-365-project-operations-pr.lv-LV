---
title: Projektu plānošanas žurnāli
description: Šajā tēmā ir sniegta informācija un paraugi, kas palīdzēs izmantot projektu plānošanas žurnālus, lai izsekotu kļūmes, kas saistītas ar projektu plānošanas servisu un projektu plānošanas API.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877514"
---
# <a name="project-scheduling-logs"></a>Projektu plānošanas žurnāli

_**Attiecas uz:** projekta operācijas uz resursiem/nekrātiem scenārijiem, Lite izvietošana - darījums ar proforma rēķinu izrakstīšanu_, Projekts _tīmeklim_

Microsoft Dynamics 365 Project Operations izmanto [Project tīmeklim](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kā primāro plānošanas programmu. Tā vietā, lai izmantotu standarta Microsoft Dataverse tīmekļa lietojumprogrammu programmēšanas interfeisus (API), projekta operācijas izmanto jaunās projektu plānošanas API, lai izveidotu, atjauninātu un dzēstu projekta uzdevumus, resursu piešķires, uzdevumu atkarības, projektu kopas un projekta grupu dalībniekus. Tomēr, veidojot, atjauninot vai dzēšot operācijas programmiski tiek palaistas darba sadalījuma struktūras (WBS) entītijām, var rasties kļūdas. Lai izsekotu šīm kļūdām un operāciju vēsturei, ir ieviesti divi jauni administratīvie žurnāli: **Operāciju kopa un Projektu plānošanas pakalpojums** **(PSS)**. Lai piekļūtu šiem žurnāliem, dodieties uz **Iestatījumu** \> **grafika integrācija**.

Nākamajā attēlā ir parādīts datu modelis projektu plānošanas žurnāliem.

![Datu modelis projektu plānošanas žurnāliem.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Operāciju kopas žurnāls

Operāciju kopas žurnāls izseko tādas operāciju kopas izpildi, kas tiek izmantota, lai palaistu vienu vai daudzas izveides, atjaunināšanas vai dzēšanas operācijas projektu, projekta uzdevumu, resursu piešķirju, uzdevumu atkarīgo, projektu grupu vai projekta grupas dalībnieku paketē. Lauks **Operācija statusā** parāda operāciju kopas vispārējo statusu. Detalizēta informācija par operāciju kopu lietderīgo slodzi tiek fiksēta saistītajos operāciju kopas detaļu ierakstos.

### <a name="operation-set"></a>Operāciju kopa

Šajā tabulā ir parādīti lauki, kas saistīti ar **entītiju Operāciju** kopa.

| Shēmas nosaukums            | Apraksts                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datums/laiks, kad operāciju kopa tika pabeigta vai neizdevās.                                                | CompletedOn            |
| msdyn_correlationid   | **Pieprasījuma correlationId** vērtība.                                                                  | CorrelationId          |
| msdyn_description     | Operāciju kopas apraksts.                                                                        | Apraksts            |
| msdyn_executedon      | Ieraksta izpildes datums/laiks.                                                                       | Kad izpildīja            |
| msdyn_operationsetId  | Entītiju instanču unikālais identifikators.                                                                   | OperationSet           |
| msdyn_Project         | Projekts, kas saistīts ar operāciju kopu.                                                            | Project                |
| msdyn_projectid       | **Pieprasījuma projectId** vērtība.                                                                      | ProjectId (novecojis) |
| msdyn_projectName     | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_PSSErrorLog     | Ar operāciju kopu saistītā projektu plānošanas pakalpojuma kļūdu žurnāla unikālais identifikators. | PSS kļūdu žurnāls          |
| msdyn_PSSErrorLogName | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_status          | Operāciju kopas statuss.                                                                             | Statuss                 |
| msdyn_statusName      | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_useraadid       | Tā lietotāja Azure Active Directory (Azure AD) objekta ID, kuram pieder pieprasījums.                     | UserAADID              |

### <a name="operation-set-detail"></a>Operāciju kopas detaļas

Šajā tabulā ir parādīti lauki, kas saistīti ar **entītiju Operāciju kopas** detaļas.

| Shēmas nosaukums                 | Apraksts                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Pieprasījuma serializētie Dataverse lauki.                                            | CdsPayload            |
| msdyn_entityname           | Pieprasījuma entītijas nosaukums.                                                     | EntityName            |
| msdyn_httpverb             | Pieprasījuma metode.                                                                         | HTTP darbības vārds (novecojis) |
| msdyn_httpverbName         | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_operationset         | Tās operācijas kopas unikālais identifikators, kurai pieder ieraksts.                      | OperationSet          |
| msdyn_operationsetdetailId | Entītiju instanču unikālais identifikators.                                                  | OperationSet detalizētā informācija   |
| msdyn_operationsetName     | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_operationtype        | Operāciju kopas detaļas darbības tips.                                             | OperationType         |
| msdyn_operationtypeName    | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_psspayload           | Pieprasījuma serializētie projektu plānošanas pakalpojuma lauki.                           | PssPayload            |
| msdyn_recordid             | Pieprasījuma ieraksta identifikators.                                                       | Ieraksta ID             |
| msdyn_requestnumber        | Automātiski ģenerēts numurs, kas identificē pasūtījumu, kurā tika saņemti pieprasījumi. | Pieprasījuma numurs        |

## <a name="project-scheduling-service-error-logs"></a>Projektu plānošanas pakalpojuma kļūdu žurnāli

Projekta plānošanas pakalpojuma kļūdu žurnāli tver kļūmes, kas rodas, kad projekta plānošanas pakalpojums mēģina **saglabāšanas** vai **atvēršanas** operāciju. Ir trīs atbalstīti scenāriji, kuros šie žurnāli tiek ģenerēti:

- Lietotāja iniciētas darbības kritiski neizdodas (piemēram, uzdevumu nevar izveidot trūkstošo privilēģiju dēļ).
- Projekta plānošanas pakalpojums nevar programmiski izveidot, atjaunināt, dzēst vai veikt citu kaskadēšanas operāciju entītijā.
- Lietotājs rodas kļūdas, ja ierakstu neizdodas atvērt (piemēram, atverot projektu vai atjauninot grupas dalībnieka informāciju).

### <a name="project-scheduling-service-log"></a>Projektu plānošanas pakalpojumu žurnāls

Šajā tabulā ir parādīti lauki, kas ir iekļauti projektu plānošanas pakalpojumu žurnālā.

| Shēmas nosaukums          | Apraksts                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Izņēmuma izsaukuma steks.                                               | Izsaukuma steks     |
| msdyn_correlationid | Kļūdas korelācijas ID.                                               | CorrelationId  |
| msdyn_errorcode     | Lauks, kas tiek izmantots Dataverse kļūdas koda vai HTTP kļūdas koda glabāšanai. | Kļūdas kods     |
| msdyn_HelpLink      | Saite uz publisko palīdzības dokumentāciju.                                       | Palīdzības saite      |
| msdyn_log           | Žurnāls no projekta plānošanas pakalpojuma.                                   | Žurnāls            |
| msdyn_project       | Projekts, kas saistīts ar kļūdu žurnālu.                             | Project        |
| msdyn_projectName   | Projekta nosaukums, ja operācijas kopas lietderīgā slodze tiks saglabāta. | Nav piemērojams |
| msdyn_psserrorlogId | Entītiju instanču unikālais identifikators.                                     | PSS kļūdu žurnāls  |
| msdyn_SessionId     | Projekta sesijas ID.                                                        | Sesijas ID     |

## <a name="error-log-cleanup"></a>Kļūdu žurnāla tīrīšana

Pēc noklusējuma gan Project Scheduling Service kļūdu žurnālus, gan operāciju kopas žurnālu var iztīrīt ik pēc 90 dienām. Visi ieraksti, kas ir vecāki par 90 dienām, tiks dzēsti. Tomēr, mainot msdyn_StateOperationSetAge lauka vērtību **lapā** Projekta **parametri**, administratori var pielāgot tīrīšanas diapazonu tā, lai tas būtu no 1 līdz 120 dienām. Ir pieejamas vairākas šīs vērtības mainīšanas metodes:

- Pielāgojiet **entītiju Project** Parameter, izveidojot pielāgotu lapu un pievienojot lauku **Novecojušo operāciju kopas** vecums.
- Izmantojiet klienta kodu, kas izmanto [WebApi programmatūras izstrādes komplektu (SDK).](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord)
- Izmantojiet pakalpojuma SDK kodu, kas izmanto Xrm SDK **updateRecord** metodi (klienta API atsauce) modeļa vadītās programmās. Power Apps ietver metodi updateRecord aprakstu un atbalstītos **parametrus**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
