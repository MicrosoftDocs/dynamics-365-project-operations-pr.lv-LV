---
title: Projekta grafika žurnāli
description: Šajā tēmā ir sniegta informācija un paraugi, kas palīdzēs izmantot projektu plānošanas žurnālus, lai izsekotu kļūmes, kas saistītas ar projektu plānošanas pakalpojumu un projektu plānošanas API.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589527"
---
# <a name="project-scheduling-logs"></a>Projekta grafika žurnāli

_**Attiecas uz:** Projekta operācijas resursu/neuzkrātiem scenārijiem, Lite izvietošana - darījums ar proformas rēķiniem_, _Projekts tīmeklim_

Microsoft Dynamics 365 Project Operations izmanto [Web programmu Project](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kā primāro plānošanas programmu. Tā vietā, lai izmantotu standarta Microsoft Dataverse tīmekļa lietojumprogrammu programmēšanas interfeisus (API), projekta operācijas izmanto jaunās projektu plānošanas API, lai izveidotu, atjauninātu un dzēstu projekta uzdevumus, resursu piešķires, uzdevumu atkarības, projektu grupas un projektu grupu dalībniekus. Tomēr, ja darba sadalījuma struktūras (WBS) entītijām tiek programmatiski palaistas izveides, atjaunināšanas vai dzēšanas operācijas, var rasties kļūdas. Lai izsekotu šīs kļūdas un operāciju vēsturi, ir ieviesti divi jauni administratīvie žurnāli: **Operāciju kopa** un **Projektu plānošanas pakalpojums (PSS)**. Lai piekļūtu šiem žurnāliem, dodieties uz **Iestatījumu** \> **grafika integrācija.**

Šajā attēlā parādīts projektu plānošanas žurnālu datu modelis.

![Projektu plānošanas žurnālu datu modelis.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Operāciju kopas žurnāls

Operāciju kopas žurnāls izseko operāciju kopas izpildi, kas tiek izmantota, lai palaistu vienu vai vairākas izveides, atjaunināšanas vai dzēšanas operācijas paketē projektiem, projekta uzdevumiem, resursu piešķirēm, uzdevumu atkarībām, projektu grupām vai projekta grupas dalībniekiem. Laukā **Operācija statusā** ir norādīts operāciju kopas vispārējais statuss. Detalizēta informācija par operāciju kopas derīgo kravu tiek uztverta saistītajos operāciju kopas detalizētās informācijas ierakstos.

### <a name="operation-set"></a>Operāciju kopa

Šajā tabulā parādīti lauki, kas ir saistīti ar entītiju Operāciju **kopa**.

| Shēmas nosaukums            | Apraksts                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Operācijas kopas pabeigšanas vai neizdevās datums/laiks.                                                | CompletedOn            |
| msdyn_correlationid   | Pieprasījuma **korelācijas Id** vērtība.                                                                  | CorrelationId          |
| msdyn_description     | Operāciju kopas apraksts.                                                                        | Apraksts            |
| msdyn_executedon      | Ieraksta izpildes datums/laiks.                                                                       | Izpildes laiks            |
| msdyn_operationsetId  | Entītiju instanču unikālais identifikators.                                                                   | OperationSet           |
| msdyn_Project         | Projekts, kas ir saistīts ar operāciju kopu.                                                            | Project                |
| msdyn_projectid       | Pieprasījuma **projectId** vērtība.                                                                      | ProjectId (novecojis) |
| msdyn_projectName     | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_PSSErrorLog     | Ar operāciju kopu saistītā projektu plānošanas pakalpojuma kļūdu žurnāla unikālais identifikators. | PSS kļūdu žurnāls          |
| msdyn_PSSErrorLogName | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_status          | Operāciju kopas statuss.                                                                             | Statuss                 |
| msdyn_statusName      | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_useraadid       | Tā Azure Active Directory lietotāja (Azure AD) objekta ID, kuram pieder pieprasījums.                     | UserAADID              |

### <a name="operation-set-detail"></a>Operāciju kopas detalizētā informācija

Šajā tabulā ir parādīti lauki, kas ir saistīti ar entītiju Operāciju **kopas detaļas**.

| Shēmas nosaukums                 | Apraksts                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Pieprasījuma serializētie Dataverse lauki.                                            | CdsPayload            |
| msdyn_entityname           | Pieprasījuma entītijas nosaukums.                                                     | EntityName            |
| msdyn_httpverb             | Pieprasījuma metode.                                                                         | HTTP darbības vārds (novecojis) |
| msdyn_httpverbName         | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_operationset         | Tās operācijas kopas unikālais identifikators, kurai pieder ieraksts.                      | OperationSet          |
| msdyn_operationsetdetailId | Entītiju instanču unikālais identifikators.                                                  | OperationSet detalizētā informācija   |
| msdyn_operationsetName     | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_operationtype        | Operācijas kopas detalizētās informācijas operācijas tips.                                             | OperationType         |
| msdyn_operationtypeName    | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_psspayload           | Pieprasījuma serializētie projektu plānošanas pakalpojuma lauki.                           | PssPayload            |
| msdyn_recordid             | Pieprasījuma ieraksta identifikators.                                                       | Ieraksta ID             |
| msdyn_requestnumber        | Automātiski ģenerēts numurs, kas identificē pasūtījumu, kurā tika saņemti pieprasījumi. | Pieprasījuma numurs        |

## <a name="project-scheduling-service-error-logs"></a>Projektu plānošanas pakalpojuma kļūdu žurnāli

Projekta plānošanas pakalpojuma kļūda reģistrē tveršanas kļūmes, kas rodas, kad projektu plānošanas pakalpojums izmēģina saglabāšanas **vai** atvēršanas **operāciju**. Ir trīs atbalstīti scenāriji, kuros tiek ģenerēti šie žurnāli:

- Lietotāja iniciētās darbības kritiski neizdodas (piemēram, piešķiri nevar izveidot trūkstošo atļauju dēļ).
- Projektu plānošanas pakalpojums entītijai nevar programmatiski izveidot, atjaunināt, dzēst vai veikt nevienu citu kaskadētu operāciju.
- Ja neizdodas atvērt ierakstu, lietotājam rodas kļūdas (piemēram, atverot projektu vai atjauninot grupas dalībnieka informāciju).

### <a name="project-scheduling-service-log"></a>Projektu plānošanas pakalpojumu žurnāls

Šajā tabulā ir parādīti lauki, kas iekļauti projektu plānošanas pakalpojumu žurnālā.

| Shēmas nosaukums          | Apraksts                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Izņēmuma izsaukuma steks.                                               | Izsaukuma steks     |
| msdyn_correlationid | Kļūdas korelācijas ID.                                               | CorrelationId  |
| msdyn_errorcode     | Lauks, kas tiek izmantots, lai saglabātu Dataverse kļūdas kodu vai HTTP kļūdas kodu. | Kļūdas kods     |
| msdyn_HelpLink      | Saite uz publiskās palīdzības dokumentāciju.                                       | Palīdzības saite      |
| msdyn_log           | Žurnālu no projekta plānošanas pakalpojuma.                                   | Žurnāls            |
| msdyn_project       | Projekts, kas ir saistīts ar kļūdu žurnālu.                             | Project        |
| msdyn_projectName   | Projekta nosaukums, ja operāciju kopas lietderīgā slodze tiks saglabāta. | Nav piemērojams |
| msdyn_psserrorlogId | Entītiju instanču unikālais identifikators.                                     | PSS kļūdu žurnāls  |
| msdyn_SessionId     | Projekta sesijas ID.                                                        | Sesijas ID     |

## <a name="error-log-cleanup"></a>Kļūdu žurnāla tīrīšana

Pēc noklusējuma gan projektu plānošanas pakalpojuma kļūdu žurnālus, gan operāciju kopas žurnālu var iztīrīt ik pēc 90 dienām. Visi ieraksti, kas ir vecāki par 90 dienām, tiks dzēsti. Tomēr, mainot msdyn_StateOperationSetAge **lauka** vērtību **lapā Projekta parametri**, administratori var pielāgot tīrīšanas diapazonu tā, lai tas būtu no 1 līdz 120 dienām. Ir pieejamas vairākas metodes šīs vērtības mainīšanai:

- Pielāgojiet entītiju **Projekta parametrs**, izveidojot pielāgotu lapu un pievienojot **lauku Novecojušu operāciju kopas vecums**.
- Izmantojiet klienta kodu, kas izmanto WebApi programmatūras [izstrādes komplektu (SDK).](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord)
- Izmantojiet pakalpojuma SDK kodu, kas modeļa vadītajās programmās izmanto metodi Xrm SDK **updateRecord** (klienta API atsauce). Power Apps ietver updateRecord **metodes aprakstu un atbalstītos** parametrus.

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
