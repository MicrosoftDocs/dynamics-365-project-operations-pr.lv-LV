---
title: Personiskie izdevumi izdevumu atskaitē
description: Šajā tēmā ir paskaidrotas divas metodes, kā apstrādāt darba ņēmēja personiskos izdevumus risinājumā Microsoft Dynamics 365 Finance.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 355e47054c20b32193c9819844c41c03cadf7fad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005440"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="495bc-103">Personiskie izdevumi izdevumu atskaitē</span><span class="sxs-lookup"><span data-stu-id="495bc-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="495bc-104">Komandējumu laikā darba ņēmēji dažreiz var izmantot korporatīvo kredītkarti, lai apmaksātu personīgos izdevumus.</span><span class="sxs-lookup"><span data-stu-id="495bc-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="495bc-105">Ja nedefinējat personīgo izdevumu apstrādes procesu, izdevumu atskaišu apstiprināšanas process var tikt traucēts, ja darba ņēmēji iesniedz detalizētas izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="495bc-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="495bc-106">Darba ņēmēja izdevumus var apstrādāt ar divām metodēm.</span><span class="sxs-lookup"><span data-stu-id="495bc-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="495bc-107">**Apmaksā darbinieks** — jūsu organizācija neapmaksā personiskos izdevumus, kas parādās uzņēmuma kredītkartes rēķinā.</span><span class="sxs-lookup"><span data-stu-id="495bc-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="495bc-108">Tā vietā tiek izveidota atskaite, kurā tiek rādīti personiskie izdevumi kopā ar korporatīvajiem izdevumiem, kas tika apmaksāti ar uzņēmuma kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="495bc-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="495bc-109">**Apmaksā uzņēmums** — jūsu organizācija apmaksā visu uzņēmuma kredītkartes rēķinu un pēc tam no darba ņēmēja konta debetē personiskos izdevumus.</span><span class="sxs-lookup"><span data-stu-id="495bc-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="495bc-110">Lapā **Izdevumu pārvaldības parametri** varat atlasīt metodi, ko organizācija izmanto.</span><span class="sxs-lookup"><span data-stu-id="495bc-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]