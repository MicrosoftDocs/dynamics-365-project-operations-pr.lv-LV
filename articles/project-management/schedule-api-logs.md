---
title: Projekta grafika žurnāli
description: Šajā rakstā ir sniegta informācija un paraugi, kas palīdzēs jums izmantot Project Scheduling žurnālus, lai izsekotu ar projektu plānošanas pakalpojumu un projektu plānošanas API saistītām kļūmēm.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923704"
---
# <a name="project-scheduling-logs"></a>Projekta grafika žurnāli

_**Attiecas uz:** Project Operations resursu balstītiem / krājumu nebalstītiem scenārijiem, Lite izvietošana — darījums ar proformas rēķinu izrakstīšanu_ _Project for the Web_

Microsoft Dynamics 365 Project Operations izmanto [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kā galveno plānošanas programmu. Tā vietā, lai lietotu standarta Microsoft Dataverse tīmekļa programmu programmēšanas saskarnes (API), Project Operations izmanto jaunu projektu plānošanas API, lai izveidotu, jauninātu un dzēstu projektu uzdevumus, resursu piešķīrumus, uzdevumu atkarības, projektu intervālus un projekta darba grupas dalībniekus. Taču, ja izveides, jaunināšanas vai dzēšanas darbības tiek programmiski palaistas darba sadalījuma struktūras (WBS) entitījās, var rasties kļūdas. Lai izsekotu šīm kļūdām un darbību vēsturei, ir ieviesti divi jauni administratīvie žurnāli: **Darbību kopa** un **Projekta plānošanas pakalpojums (PSS)**. Lai piekļūtu šiem žurnāliem, dodieties uz **Iestatījumi** \>**Plānotāja integrācija**.

Attēlā tālāk parādīts projektu plānošanas žurnālu datu modelis.

![Projektu plānošanas žurnālu datu modelis.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Darbību kopas žurnāls

Darbību kopas žurnāls izsekot darbību kopas izpildei, kas tiek izmantota, lai palaistu vienu vai vairākas izveides, jaunināšanas vai dzēšanas darbības projektu partijā, projekta uzdevumos, resursu piešķīrumos, uzdevumu atkarībās, projektu intervālos vai projekta darba grupas dalībniekiem. Laukā **Darbības statuss** tiek rādīts darbību kopas vispārējais statuss. Darbību kopas slodzes informācija tiek tverta attiecīgajos Operāciju kopas informācijas ierakstos.

### <a name="operation-set"></a>Darbību kopa

Tabulā tālāk parādīti lauki, kas ir saistīti ar entitīju **Darbību kopa**.

| Shēmas nosaukums            | Apraksts                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datums/laiks, kad darbību kopa tika pabeigta vai tās pabeigšana neizdevās.                                                | CompletedOn            |
| msdyn_correlationid   | Pieprasījuma **correlationId** vērtība.                                                                  | CorrelationId          |
| msdyn_description     | Darbību kopas apraksts.                                                                        | Apraksts            |
| msdyn_executedon      | Ieraksta palaišanas datums/laiks.                                                                       | Izpildes laiks            |
| msdyn_operationsetId  | Entitījas instanču unikālais identifikators.                                                                   | OperationSet           |
| msdyn_Project         | Ar darbību kopu saistītais projekts.                                                            | Project                |
| msdyn_projectid       | Pieprasījuma **projectId** vērtība.                                                                      | ProjectId (novecojis) |
| msdyn_projectName     | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_PSSErrorLog     | Project Scheduling Service kļūdu žurnāla unikālais identifikators, kas ir saistīts ar darbību kopu. | PSS kļūdu žurnāls          |
| msdyn_PSSErrorLogName | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_status          | Darbību kopas statuss.                                                                             | Statuss                 |
| msdyn_statusName      | Nav lietojams.                                                                                              | Nav piemērojams         |
| msdyn_useraadid       | Azure Active Directory (Azure AD) objekta ID lietotājam, kam pieder pieprasījums.                     | UserAADID              |

### <a name="operation-set-detail"></a>Darbību kopas informācija

Tabulā tālāk parādīti lauki, kas ir saistīti ar entitīju **Darbību kopas informācija**.

| Shēmas nosaukums                 | Apraksts                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serializēti Dataverse lauki pieprasījumam.                                            | CdsPayload            |
| msdyn_entityname           | Entītijas nosaukums šim pieprasījumam.                                                     | EntityName            |
| msdyn_httpverb             | Pieprasījuma metode.                                                                         | HTTP darbības vārds (novecojis) |
| msdyn_httpverbName         | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_operationset         | Tās darbību kopas unikālais identifikators, kam pieder šis ieraksts.                      | OperationSet          |
| msdyn_operationsetdetailId | Entitījas instanču unikālais identifikators.                                                  | OperationSet detalizētā informācija   |
| msdyn_operationsetName     | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_operationtype        | Darbību kopas detalizētās informācijas darbības tips.                                             | OperationType         |
| msdyn_operationtypeName    | Nav lietojams.                                                                             | Nav piemērojams        |
| msdyn_psspayload           | Pieprasījumam serializētie projektu plānošanas pakalpojuma lauki.                           | PssPayload            |
| msdyn_recordid             | Pieprasījuma ieraksta identifikators.                                                       | Ieraksta ID             |
| msdyn_requestnumber        | Automātiski ģenerēts numurs, ko izmanto, lai identificētu pasūtījumu, kurā pieprasījumi tiek saņemti | Pieprasījuma numurs        |

## <a name="project-scheduling-service-error-logs"></a>Project Scheduling Service kļūdu žurnāli

Project Scheduling Service kļūdu žurnālos tiek tvertas kļūdas, kas radušās, Project Scheduling Service mēģinot **Saglabāt** vai **Atvērt** darbību. Šie žurnāli tiek izveidoti trijos atbalstītos scenārijos:

- Neizdodas lietotāja ierosinātas darbības (piemēram, nav iespējams piešķirt uzdevumu, jo trūkst privilēģiju).
- Project Scheduling Service nevar programmiski izveidot, jaunināt, dzēst entitīju vai veikt citas kaskadēšanas darbības.
- Lietotājam rodas kļūdas, ja nevar atvērt ierakstu (piemēram, ja ir atvērts projekts vai ir atjaunināta informācija par darba grupas dalībnieku).

### <a name="project-scheduling-service-log"></a>Project Scheduling Service žurnāls

Tabulā parādīti lauki, kas iekļauti Project Scheduling Service žurnālā.

| Shēmas nosaukums          | Apraksts                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Izņēmuma izsaukuma steks.                                               | Izsaukuma steks     |
| msdyn_correlationid | Kļūdas korelācijas ID.                                               | CorrelationId  |
| msdyn_errorcode     | Lauks, kas tiek izmantots Dataverse kļūdas koda vai HTTP kļūdas koda glabāšanas nolūkam. | Kļūdas kods     |
| msdyn_HelpLink      | Publiskās palīdzības dokumentācijas saite.                                       | Palīdzības saite      |
| msdyn_log           | Žurnāls no Project Scheduling Service.                                   | Žurnāls            |
| msdyn_project       | Ar kļūdu žurnālu saistīts projekts.                             | Project        |
| msdyn_projectName   | Projekta nosaukums, ja darbību kopas slodze tiek saglabāta. | Nav piemērojams |
| msdyn_psserrorlogId | Entitījas instanču unikālais identifikators.                                     | PSS kļūdu žurnāls  |
| msdyn_SessionId     | Projekta sesijas ID.                                                        | Sesijas ID     |

## <a name="error-log-cleanup"></a>Kļūdu žurnāla notīrīšana

Pēc noklusējuma gan Project Scheduling Service kļūdu žurnālus, gan operāciju kopas žurnālu var notīrīt ik pēc 90 dienām. Ieraksti, kas ir vecāki par 90 dienām, tiks dzēsti. Taču mainot lauka **msdyn_StateOperationSetAge** vērtību lapā **Projekta parametri**, administratori var regulēt tīrīšanas diapazonu, lai tas būtu no 1 līdz 120 dienām. Šīs vērtības mainīšanai ir pieejamas vairākas metodes:

- Pielāgojiet entitīju **Projekta parametrs**, izveidojot pielāgotu lapu un pievienojot lauku **Novecojušās darbību kopas vecums**.
- Izmantojiet klienta kodu, kas lieto [WebApi programmatūŗas izstrādes komplektu (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Izmantojiet Pakalpojuma SDK kodu, kas lieto Xrm SDK metodi **updateRecord** (klienta API atsauce) modeļa vadītās programmās. Power Apps ietver metodes **updateRecord** aprakstu un atbalstītos parametrus.

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
