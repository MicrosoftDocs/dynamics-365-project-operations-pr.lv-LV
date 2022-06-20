---
title: Izdevumu pārvaldības integrācija
description: Šajā rakstā sniegta informācija par izdevumu pārskata integrāciju projektu operācijās, izmantojot divējādu rakstīšanu.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c64c318dc1915a9a87b6ae3c6b8a2aa6d3c9cd36
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924623"
---
# <a name="expense-management-integration"></a>Izdevumu pārvaldības integrācija

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā ir sniegta informācija par izdevumu pārskatu integrāciju projektu operāciju [pilnajā izdevumu izvietošanā](../expense/expense-overview.md), izmantojot divkāršu rakstīšanu.

## <a name="expense-categories"></a>Izdevumu kategorijas

Pilnā izdevumu izvietošanā izdevumu kategorijas tiek izveidotas un uzturētas finanšu un operāciju programmās. Lai izveidotu jaunu izdevumu kategoriju, veiciet tālāk uzskaitītās darbības.

1. Risinājumā Microsoft Dataverse izveidojiet kategoriju **Transakcija**. Duālās rakstīšanas integrācija sinhronizēs šo darbību kategoriju ar finanšu un operāciju programmām. Papildinformāciju skatiet sadaļā [Projekta kategoriju konfigurēšana](/dynamics365/project-operations/project-accounting/configure-project-categories) un [Project Operations iestatīšanas un konfigurēšanas datu integrācija](resource-dual-write-setup-integration.md). Šīs integrācijas rezultātā sistēma izveido četrus koplietojamu kategoriju ierakstus finanšu un operāciju programmās.
2. Risinājumā Finance dodieties uz **Izdevumu pārvaldība** > **Iestatīšana** > **Kopīgotās kategorijas** un atlasiet kategoriju ar transakcijas klasi **Izdevumi**. Parametru **Var izmantot izdevumos** iestatiet kā **Patiess** un definējiet izmantojamo izdevumu tipu.
3. Izmantojot šo kopīgotās kategorijas ierakstu, izveidojiet jaunu izdevumu kategoriju, dodoties uz **Izdevumu pārvaldība** > **Iestatīšana** > **Izdevumu kategorijas** un atlasiet vienumu **Jauns**. Kad ieraksts ir saglabāts, duālā rakstīšana izmanto tabulas karti **Project Operations integrācijas projekta izdevumu kategorijas eksporta entītija (msdyn\_expensecategories)**, lai sinhronizētu šo ierakstu ar Dataverse.

  ![Izdevumu kategoriju integrācija.](./media/DW6ExpenseCategories.png)

Izdevumu kategorijas finanšu un operāciju programmās ir specifiskas uzņēmumam vai juridiskai personai. Programmā Dataverse ir atsevišķi, atbilstošajai juridiskajai personai specifiski ieraksti. Aprēķinot izdevumus, projektu vadītājs nevar atlasīt izdevumu kategorijas, kas tika izveidotas projektam, kura īpašnieks ir cits uzņēmums, nevis tas uzņēmums, kuram pieder projekts, pie kura tiek strādāts. 

## <a name="expense-reports"></a>Izdevumu atskaites

Izdevumu pārskati tiek izveidoti un apstiprināti finanšu un operāciju programmās. Papildinformāciju skatiet sadaļā [Izdevumu atskaišu izveide un apstrāde risinājumā Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Pēc tam, kad izdevumu atskaiti ir apstiprinājis projekta vadītājs, tā tiek grāmatota virsgrāmatā. Programmā Project Operations ar projektiem saistītās izdevumu atskaišu rindas tiek grāmatotas, izmantojot īpašas grāmatošanas kārtulas.

  - Ar projektiem saistītās izmaksas (tostarp neatgūstamie nodokļi) netiek nekavējoties grāmatotas projekta izmaksu kontā virsgrāmatā, bet tiek grāmatotas izdevumu integrācijas kontā. Šis konts tiek konfigurēts sadaļas **Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Projekta pārvaldības un uzskaites parametri** cilnē **Project Operations on Dynamics 365 Customer engagement**.
  - Duālā rakstīšana veic sinhronizāciju ar Dataverse, izmantojot tabulas karti **Project Operations integrācijas projekta izdevumu eksporta entītija (msdyn\_expenses)**.
  - Izdevumu atskaites grāmatošanas laikā nodokļu apakšgrāmata, piegādātāju apakšgrāmata un citi finanšu reģistri tiek ierakstīti atbilstoši piemērojamībai.

  ![Izdevumu atskaišu integrācija.](./media/DW6ExpenseReports.png)

Kad Dataverse entītijā **Izdevumi** tiek ierakstīts ieraksts, sistēma aktivizē automatizētu ieraksta apstiprināšanas procesu. Ja nepieciešams, automatizēto apstiprināšanas statusu var pārskatīt risinājumā Dataverse, dodoties uz **Papildu iestatījumi** > **Sistēma** > **Sistēmas uzdevumi**. Pēc apstiprinājuma pabeigšanas entītijā **Faktiskie dati** tiek izveidoti izdevumu transakcijas klases ieraksti.

Ar izdevumiem saistītie faktiskie dati pēc tam tiek apstrādāti, izmantojot duālās rakstīšanas tabulas karti **Project Operations integrācijas faktiskie dati (msdyn\_actuals)**. Papildinformāciju skatiet sadaļā [Projekta aprēķini un faktisko dati](resource-dual-write-estimates-actuals.md).

Periodiskais process **Importēt no izstādīšanas** Project Operations integrācijas žurnālā izveido ar izdevumu atskaiti saistītas žurnāla rindas. Nobīdes konts pēc noklusējuma tiek mainīts uz izdevumu integrācijas kontu. Integrācijas žurnāla grāmatošanas laikā tiek notīrīta izdevumu transakcijas konta bilance, un izdevumu summa tiek pārvietota uz projekta izmaksu kontu. Sistēma arī izveido projekta apakšgrāmatas transakcijas lejupstraumes rēķinu izrakstīšanas un ieņēmumu atpazīšanas nolūkiem.
