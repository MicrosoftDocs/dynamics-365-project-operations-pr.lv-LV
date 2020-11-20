---
title: Labotie rēķini
description: Šajā tēmā ir sniegta informācija par labotiem rēķiniem.
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
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122397"
---
# <a name="corrected-invoices"></a><span data-ttu-id="9f788-103">Labotie rēķini</span><span class="sxs-lookup"><span data-stu-id="9f788-103">Corrected invoices</span></span>

<span data-ttu-id="9f788-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="9f788-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9f788-105">Apstiprinātos rēķinus var rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9f788-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="9f788-106">Rediģējot apstiprinātu rēķinu, tiek izveidots labotā rēķina melnraksts.</span><span class="sxs-lookup"><span data-stu-id="9f788-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="9f788-107">Tā kā tiek pieņemts, ka vēlaties atsaukt visas transakcijas un daudzumus no sākotnējā rēķina, šis labotais rēķins ietver visas darbības no sākotnējā rēķina un visi tajā ietvertie daudzumi ir nulle (0).</span><span class="sxs-lookup"><span data-stu-id="9f788-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="9f788-108">Ja transakcijām nav nepieciešama labošana, tās var noņemt no melnraksta labojošā rēķina.</span><span class="sxs-lookup"><span data-stu-id="9f788-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="9f788-109">Lai atsauktu vai atgrieztu tikai daļēju daudzumu, var rediģēt rindas informācijas lauku Daudzums.</span><span class="sxs-lookup"><span data-stu-id="9f788-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="9f788-110">Ja atverat rēķina rindas informāciju, varat redzēt sākotnējo rēķina apjomu.</span><span class="sxs-lookup"><span data-stu-id="9f788-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="9f788-111">Pašreizējo rēķina daudzumu var rediģēt, lai tas būtu mazāks vai lielāks par sākotnējo rēķina apjomu.</span><span class="sxs-lookup"><span data-stu-id="9f788-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="9f788-112">Kad apstiprināsit laboto rēķinu, sākotnējais izmaksātais pārdošanas apjoms tiek apgriezts un tiek izveidots jauns rēķins par pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="9f788-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="9f788-113">Ja daudzums tika samazināts, starpība izraisīs jaunu nemaksātu pārdošanas darījumu.</span><span class="sxs-lookup"><span data-stu-id="9f788-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="9f788-114">Piemēram, ja sākotnējais apmaksātais pārdošanas apjoms ir astoņas stundas un labotā rēķina rindu informācijai ir samazināts daudzums uz sešām stundām, sākotnējā izmaksu rinda tiek atgriezta un tiek izveidoti divi jauni reālie dati.</span><span class="sxs-lookup"><span data-stu-id="9f788-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="9f788-115">Rēķins par pārdošanu ir fiksētas sešas stundas.</span><span class="sxs-lookup"><span data-stu-id="9f788-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="9f788-116">Neiekasēts pārdošanas apjoms atlikušajām divām stundām.</span><span class="sxs-lookup"><span data-stu-id="9f788-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="9f788-117">Šo transakciju var izrakstīt vēlāk vai atzīmēt kā nepiemērojamu atkarībā no vienošanās ar klientu.</span><span class="sxs-lookup"><span data-stu-id="9f788-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
