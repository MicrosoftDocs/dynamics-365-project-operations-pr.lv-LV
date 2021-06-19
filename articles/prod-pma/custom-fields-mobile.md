---
title: Pielāgoto lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajā programmā operētājsistēmā iOS un Android
description: Šajā tēmā ir sniegti biežākie veidi, kā lietot paplašinājumus, lai ieviestu pielāgotus laukus.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003050"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="ddf16-103">Pielāgoto lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajā programmā operētājsistēmā iOS un Android</span><span class="sxs-lookup"><span data-stu-id="ddf16-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddf16-104">Šajā tēmā ir sniegti biežākie veidi, kā lietot paplašinājumus, lai ieviestu pielāgotus laukus.</span><span class="sxs-lookup"><span data-stu-id="ddf16-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="ddf16-105">Ir ietvertas tālāk norādītās tēmas.</span><span class="sxs-lookup"><span data-stu-id="ddf16-105">The following topics are covered:</span></span>

- <span data-ttu-id="ddf16-106">Dažādie datu tipi, kurus atbalsta pielāgotā lauku struktūra</span><span class="sxs-lookup"><span data-stu-id="ddf16-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="ddf16-107">Kā laika uzskaites tabulās parādīt tikai lasāmus vai rediģējamus ierakstus un saglabāt lietotāja sniegtās vērtības atpakaļ datu bāzē</span><span class="sxs-lookup"><span data-stu-id="ddf16-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="ddf16-108">Kā rādīt tikai lasāmus laukus laika uzskaites tabulas galvenē</span><span class="sxs-lookup"><span data-stu-id="ddf16-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="ddf16-109">Kā integrēt citu pielāgoto biznesa loģiku, lai laukos ievadītu noklusējuma vērtības un veiktu papildu validāciju</span><span class="sxs-lookup"><span data-stu-id="ddf16-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="ddf16-110">Auditorija</span><span class="sxs-lookup"><span data-stu-id="ddf16-110">Audience</span></span>

<span data-ttu-id="ddf16-111">Šī tēma ir paredzēta izstrādātājiem, kuri integrē savus pielāgotos laukus Microsoft Dynamics 365 Project Timesheet mobilajā programmā, kas pieejama operētājsistēmām Apple iOS un Google Android.</span><span class="sxs-lookup"><span data-stu-id="ddf16-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="ddf16-112">Tiek pieņemts, ka lasītāji pārzina X++ izstrādi un projekta laika uzskaites tabulu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="ddf16-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="ddf16-113">Datu līgums — TSTimesheetCustomField X++ klase</span><span class="sxs-lookup"><span data-stu-id="ddf16-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="ddf16-114">**TSTimesheetCustomField** klase ir X++ datu līguma klase, kas atspoguļo informāciju par pielāgotu laika uzskaites tabulas funkcionalitātes lauku.</span><span class="sxs-lookup"><span data-stu-id="ddf16-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="ddf16-115">Pielāgoto lauku objektu saraksti tiek nodoti gan TSTimesheetDetails datu līgumam, gan TSTimesheetEntry datu līgumam, lai rādītu pielāgotos laukus mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="ddf16-116">**TSTimesheetDetails** — laika uzskaites tabulas galvenes līgums.</span><span class="sxs-lookup"><span data-stu-id="ddf16-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="ddf16-117">**TSTimesheetEntry** — laika uzskaites tabulas transakcijas līgums.</span><span class="sxs-lookup"><span data-stu-id="ddf16-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="ddf16-118">Šo objektu grupas, kurām ir vienāda projekta informācija un **timesheetLineRecId** vērtība, veido rindu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="ddf16-119">fieldBaseType (Types)</span><span class="sxs-lookup"><span data-stu-id="ddf16-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="ddf16-120">Rekvizīts **FieldBaseType** objektā **TsTimesheetCustom** nosaka tā lauka veidu, kas tiek parādīts programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="ddf16-121">Tiek atbalstītas tālāk norādītās **Types** vērtības.</span><span class="sxs-lookup"><span data-stu-id="ddf16-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="ddf16-122">Types vērtība</span><span class="sxs-lookup"><span data-stu-id="ddf16-122">Types value</span></span> | <span data-ttu-id="ddf16-123">Veids</span><span class="sxs-lookup"><span data-stu-id="ddf16-123">Type</span></span>              | <span data-ttu-id="ddf16-124">Piezīmes</span><span class="sxs-lookup"><span data-stu-id="ddf16-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="ddf16-125">0</span><span class="sxs-lookup"><span data-stu-id="ddf16-125">0</span></span>           | <span data-ttu-id="ddf16-126">Virkne (un uzskaitījums)</span><span class="sxs-lookup"><span data-stu-id="ddf16-126">String (and Enum)</span></span> | <span data-ttu-id="ddf16-127">Lauks tiek parādīts kā teksta lauks.</span><span class="sxs-lookup"><span data-stu-id="ddf16-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="ddf16-128">1</span><span class="sxs-lookup"><span data-stu-id="ddf16-128">1</span></span>           | <span data-ttu-id="ddf16-129">Integer</span><span class="sxs-lookup"><span data-stu-id="ddf16-129">Integer</span></span>           | <span data-ttu-id="ddf16-130">Šī vērtība tiek parādīta kā skaitlis bez decimāldaļām.</span><span class="sxs-lookup"><span data-stu-id="ddf16-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="ddf16-131">2</span><span class="sxs-lookup"><span data-stu-id="ddf16-131">2</span></span>           | <span data-ttu-id="ddf16-132">Real</span><span class="sxs-lookup"><span data-stu-id="ddf16-132">Real</span></span>              | <span data-ttu-id="ddf16-133">Šī vērtība tiek parādīta kā skaitlis ar decimāldaļām.</span><span class="sxs-lookup"><span data-stu-id="ddf16-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="ddf16-134">Lai programmā parādītu faktisko vērtību kā valūtu, izmantojiet rekvizītu **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="ddf16-135">Varat izmantot rekvizītu **numberOfDecimals**, lai iestatītu parādāmo decimāldaļu skaitu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="ddf16-136">3</span><span class="sxs-lookup"><span data-stu-id="ddf16-136">3</span></span>           | <span data-ttu-id="ddf16-137">Datums</span><span class="sxs-lookup"><span data-stu-id="ddf16-137">Date</span></span>              | <span data-ttu-id="ddf16-138">Datuma formātus nosaka lietotāja iestatījums **Datuma, laika un ciparu formāts**, kas ir norādīts iestatījumos **Valodas un valsts/reģiona reference** sadaļā **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="ddf16-139">4</span><span class="sxs-lookup"><span data-stu-id="ddf16-139">4</span></span>           | <span data-ttu-id="ddf16-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="ddf16-140">Boolean</span></span>           | |
| <span data-ttu-id="ddf16-141">15</span><span class="sxs-lookup"><span data-stu-id="ddf16-141">15</span></span>          | <span data-ttu-id="ddf16-142">GUID</span><span class="sxs-lookup"><span data-stu-id="ddf16-142">GUID</span></span>              | |
| <span data-ttu-id="ddf16-143">16</span><span class="sxs-lookup"><span data-stu-id="ddf16-143">16</span></span>          | <span data-ttu-id="ddf16-144">Int64</span><span class="sxs-lookup"><span data-stu-id="ddf16-144">Int64</span></span>             | |

- <span data-ttu-id="ddf16-145">Ja rekvizīts **stringOptions** nav norādīts objektā **TSTimesheetCustomField**, lietotājam tiek nodrošināts brīva teksta lauks.</span><span class="sxs-lookup"><span data-stu-id="ddf16-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="ddf16-146">Rekvizītu **stringLength** var izmantot, lai iestatītu maksimālo virknes garumu, ko lietotāji var ievadīt.</span><span class="sxs-lookup"><span data-stu-id="ddf16-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="ddf16-147">Ja rekvizīts **stringOptions** ir norādīts objektā **TSTimesheetCustomField**, šie saraksta elementi ir vienīgās vērtības, ko lietotāji var atlasīt, izmantojot opciju pogas (radiopogas).</span><span class="sxs-lookup"><span data-stu-id="ddf16-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="ddf16-148">Šajā gadījumā virknes lauks var darboties kā uzskaitījuma vērtība lietotāja ieraksta vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="ddf16-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="ddf16-149">Lai vērtību saglabātu datu bāzē kā uzskaitījumu, manuāli kartējiet virknes vērtību atpakaļ uz uzskaitījuma vērtību, pirms to saglabājat datu bāzē, izmantojot komandu ķēdi (piemēru skatiet sadaļā “Komandu ķēdes izmantošana TSTimesheetEntryService klasē, lai saglabātu laika uzskaites tabulas ierakstu no programmas atpakaļ datu bāzē” tālāk šajā tēmā).</span><span class="sxs-lookup"><span data-stu-id="ddf16-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="ddf16-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="ddf16-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="ddf16-151">Šo rekvizītu var izmantot, lai formatētu reālas vērtības kā valūtu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="ddf16-152">Šī pieeja ir piemērojama tikai tad, ja **fieldBaseType** vērtība ir **Real**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="ddf16-153">**TSCustomFieldExtendedType:None** — formatējums netiek lietots.</span><span class="sxs-lookup"><span data-stu-id="ddf16-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="ddf16-154">**TSCustomFieldExtendedType::Currency** — vērtības formatēšana valūtā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="ddf16-155">Ja valūtas formatēšana ir aktīva, lauku **stringValue** var lietot, lai nodotu valūtas kodu, kas jārāda programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="ddf16-156">Šī vērtība ir tikai lasāma.</span><span class="sxs-lookup"><span data-stu-id="ddf16-156">The value is a read-only value.</span></span>

    <span data-ttu-id="ddf16-157">Lauks **realValue** satur naudas summu, kas jāsaglabā datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="ddf16-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="ddf16-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="ddf16-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="ddf16-159">Šo rekvizītu var izmantot, lai norādītu, kur programmā jārāda pielāgotais lauks.</span><span class="sxs-lookup"><span data-stu-id="ddf16-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="ddf16-160">**TSCustomFieldSection::Header** — lauks tiks parādīts programmas sadaļā **Skatīt detalizētu informāciju**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="ddf16-161">Šie vienmēr ir tikai lasāmie lauki.</span><span class="sxs-lookup"><span data-stu-id="ddf16-161">These fields are always read-only.</span></span>
- <span data-ttu-id="ddf16-162">**TSCustomFieldSection::Line** — lauks tiks parādīts pēc visiem iebūvētajiem rindu laukiem laika uzskaites tabulas ierakstos.</span><span class="sxs-lookup"><span data-stu-id="ddf16-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="ddf16-163">Šie lauki var būt rediģējami vai tikai lasāmi.</span><span class="sxs-lookup"><span data-stu-id="ddf16-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="ddf16-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="ddf16-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="ddf16-165">Šis rekvizīts identificē lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="ddf16-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="ddf16-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="ddf16-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="ddf16-167">Šis rekvizīts identificē lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="ddf16-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="ddf16-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="ddf16-168">isEditable (NoYes)</span></span>

<span data-ttu-id="ddf16-169">Iestatiet šo rekvizītu uz **Yes**, lai norādītu, ka lauku laika uzskaites tabulas ierakstu sadaļā lietotāji var rediģēt.</span><span class="sxs-lookup"><span data-stu-id="ddf16-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="ddf16-170">Iestatiet rekvizītu uz **No**, lai padarītu lauku tikai lasāmu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="ddf16-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="ddf16-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="ddf16-172">Iestatiet šo rekvizītu uz **Yes**, lai norādītu, ka laukam laika uzskaites tabulas ierakstu sadaļā jābūt obligātam.</span><span class="sxs-lookup"><span data-stu-id="ddf16-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="ddf16-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="ddf16-173">label (str)</span></span>

<span data-ttu-id="ddf16-174">Šajā rekvizītā ir norādīta etiķete, kas tiek parādīta blakus laukam programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="ddf16-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="ddf16-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="ddf16-176">Šis rekvizīts ir lietojams tikai tad, ja **fieldBaseType** ir iestatīts uz **String**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="ddf16-177">Ja **stringOptions** ir iestatīts, virkņu vērtības, kas ir pieejamas atlasei, izmantojot opciju pogas (radiopogas), tiek norādītas pēc virknēm sarakstā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="ddf16-178">Ja nav nevienas virknes, ir atļauts brīvā teksta ieraksts (piemēru skatiet sadaļā “Komandu ķēdes izmantošana TSTimesheetEntryService klasē, lai saglabātu laika uzskaites tabulas ierakstu no programmas atpakaļ datu bāzē” tālāk šajā tēmā).</span><span class="sxs-lookup"><span data-stu-id="ddf16-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="ddf16-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="ddf16-179">stringLength (int)</span></span>

<span data-ttu-id="ddf16-180">Šajā rekvizītā ir norādīts virknes lauka maksimālais garums.</span><span class="sxs-lookup"><span data-stu-id="ddf16-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="ddf16-181">Tas ir lietojams tikai tad, ja **fieldBaseType** ir iestatīts uz **String**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="ddf16-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="ddf16-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="ddf16-183">Šis rekvizīts norāda decimāldaļu skaitu, kas tiek rādīts reālo skaitļu laukam.</span><span class="sxs-lookup"><span data-stu-id="ddf16-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="ddf16-184">Tas ir lietojams tikai tad, ja **fieldBaseType** ir iestatīts uz **Real**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="ddf16-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="ddf16-185">orderSequence (int)</span></span>

<span data-ttu-id="ddf16-186">Šis rekvizīts nosaka secību, kādā pielāgotie lauki tiek rādīti programmā, ja ir norādīti vairāki pielāgotie lauki.</span><span class="sxs-lookup"><span data-stu-id="ddf16-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="ddf16-187">Lauki, kuros ir mazāki skaitļi, tiek parādīti vispirms.</span><span class="sxs-lookup"><span data-stu-id="ddf16-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="ddf16-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="ddf16-188">booleanValue (boolean)</span></span>

<span data-ttu-id="ddf16-189">**Boolean** veida laukiem šis rekvizīts nodod lauka Būla vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="ddf16-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="ddf16-190">guidValue (guid)</span></span>

<span data-ttu-id="ddf16-191">**GUID** veida laukiem šis rekvizīts nodod lauka vispārēji unikālā identifikatora (GUID) vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="ddf16-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="ddf16-192">int64Value (int64)</span></span>

<span data-ttu-id="ddf16-193">**Int64** veida laukiem šis rekvizīts nodod lauka Int64 vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="ddf16-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="ddf16-194">intValue (int)</span></span>

<span data-ttu-id="ddf16-195">**Int** veida laukiem šis rekvizīts nodod lauka Int vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="ddf16-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="ddf16-196">realValue (real)</span></span>

<span data-ttu-id="ddf16-197">**Real** veida laukiem šis rekvizīts nodod lauka reālo vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="ddf16-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="ddf16-198">stringValue (str)</span></span>

<span data-ttu-id="ddf16-199">**String** veida laukiem šis rekvizīts nodod lauka virknes vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="ddf16-200">Tas tiek izmantots arī **Real** veida laukiem, kas formatēti kā valūta.</span><span class="sxs-lookup"><span data-stu-id="ddf16-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="ddf16-201">Šiem laukiem rekvizīts tiek izmantots, lai nodotu valūtas kodu programmai.</span><span class="sxs-lookup"><span data-stu-id="ddf16-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="ddf16-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="ddf16-202">dateValue (date)</span></span>

<span data-ttu-id="ddf16-203">**Date** veida laukiem šis rekvizīts nodod lauka datuma vērtību starp serveri un programmu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="ddf16-204">Pielāgota lauka rādīšana un saglabāšana laika uzskaites tabulas ierakstu sadaļā</span><span class="sxs-lookup"><span data-stu-id="ddf16-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="ddf16-205">Tālāk ir redzams izveidotās laika uzskaites tabulas ieraksta ekrānuzņēmums mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="ddf16-206">Tajā ir redzami iebūvētie lauki un pielāgots lauks sadaļā “Laika ieraksts”, kura nosaukums ir “Testa virkne”, un uzskaitījuma vērtība “Otrā opcija” jau ir iestatīta.</span><span class="sxs-lookup"><span data-stu-id="ddf16-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Testa virknes pielāgotais lauks programmā](media/timesheet-entry.jpg)



<span data-ttu-id="ddf16-208">Tālāk ir redzams mobilās programmas ekrānuzņēmums, kur lietotājs atlasa vienu no uzskaitījuma opcijām, kas pieejamas pielāgotajam laukam “Testa virkne”.</span><span class="sxs-lookup"><span data-stu-id="ddf16-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="ddf16-209">Šīs divas opcijas ir “Pirmais variants” un “Otrā opcija”, kas tiek rādītas kā radiopogas.</span><span class="sxs-lookup"><span data-stu-id="ddf16-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="ddf16-210">Pašlaik ir atlasīta otrā opcija.</span><span class="sxs-lookup"><span data-stu-id="ddf16-210">The second option is currently selected.</span></span>

![Opciju pogas (radiopogas), kas paredzētas testa virknes pielāgotajam laukam](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="ddf16-212">TSTimesheetLine tabulas paplašināšana, lai tai būtu pielāgotais lauks</span><span class="sxs-lookup"><span data-stu-id="ddf16-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="ddf16-213">Tipiskos scenārijos ir iespējams, ka dati, kas paredzēti pielāgotajam laukam laika uzskaites tabulas ierakstu sadaļā, tiks saglabāti tabulā TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="ddf16-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="ddf16-214">Taču var izmantot arī citas tabulas, ja datus var izgūt, pamatojoties uz nodrošinātu TSTimesheetTrans ierakstu vai ja tiem nav konkrēta ieraksta konteksta (piemēram, ja lauks ir iestatīts kā tikai lasāms projekta parametros).</span><span class="sxs-lookup"><span data-stu-id="ddf16-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="ddf16-215">Ņemiet vērā, ka pielāgotajiem laukiem nav nepieciešami nekādi datu bāzes dublējuma ieraksti.</span><span class="sxs-lookup"><span data-stu-id="ddf16-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="ddf16-216">Tos var dinamiski ģenerēt, izmantojot X++ loģiku.</span><span class="sxs-lookup"><span data-stu-id="ddf16-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="ddf16-217">Šī pieeja var būt noderīga tikai lasāmos scenārijos (dinamiski ģenerētu pielāgoto lauku vērtību piemēru skatiet sadaļā “Komandu ķēdes izmantošana TSTimesheetDetails klasē, buildCustomFieldListForHeader metode, lai ievadītu laika uzskaites tabulas detaļas”).</span><span class="sxs-lookup"><span data-stu-id="ddf16-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="ddf16-218">Zemāk ir Visual Studio ekrānuzņēmums ar programmas objektu koku.</span><span class="sxs-lookup"><span data-stu-id="ddf16-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="ddf16-219">Tajā ir redzams TSTimesheetLine tabulas paplašinājums ar TestLineString lauku, kas pievienots kā pielāgots lauks.</span><span class="sxs-lookup"><span data-stu-id="ddf16-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Rindas virkne](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="ddf16-221">Komandu ķēdes izmantošana buildCustomFieldList metodei TSTimesheetSettings klasē, lai parādītu lauku laika uzskaites tabulas ierakstu sadaļā</span><span class="sxs-lookup"><span data-stu-id="ddf16-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="ddf16-222">Šis kods kontrolē lauka rādīšanas iestatījumus programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="ddf16-223">Piemēram, tas kontrolē lauka tipu, etiķeti, to, vai lauks ir obligāts, kā arī to, kurā sadaļā šis lauks tiek rādīts.</span><span class="sxs-lookup"><span data-stu-id="ddf16-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="ddf16-224">Nākamajā piemērā i parādīts virknes lauks laika ierakstos.</span><span class="sxs-lookup"><span data-stu-id="ddf16-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="ddf16-225">Šim laukam ir divas opcijas, **Pirmā opcija** un **Otrā opcija**, kas pieejamas, izmantojot opciju pogas (radiopogas).</span><span class="sxs-lookup"><span data-stu-id="ddf16-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="ddf16-226">Programmas lauks ir saistīts ar lauku **TestLineString**, kas tiek pievienots tabulai TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="ddf16-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="ddf16-227">Ņemiet vērā, ka varat izmantot **TSTimesheetCustomField::newFromMetatdata()** metodi, lai vienkāršotu pielāgoto lauku rekvizītu inicializēšanu: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** un **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="ddf16-228">Šos parametrus var iestatīt arī manuāli.</span><span class="sxs-lookup"><span data-stu-id="ddf16-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="ddf16-229">Komandu ķēdes izmantošana buildCustomFieldListForEntry metodei TSTimesheetEntry klasē, lai ievadītu vērtības laika uzskaites tabulas ierakstā</span><span class="sxs-lookup"><span data-stu-id="ddf16-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="ddf16-230">Metode **BuildCustomFieldListForEntry** tiek izmantota, lai ievadītu vērtības saglabātajās laika uzskaites tabulas rindās mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="ddf16-231">Kā parametrs tiek ņemts TSTimesheetTrans ieraksts.</span><span class="sxs-lookup"><span data-stu-id="ddf16-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="ddf16-232">Šī ieraksta laukus var izmantot, lai programmā ievadītu pielāgotā lauka vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddf16-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="ddf16-233">Komandu ķēdes izmantošana TSTimesheetEntryService klasē, lai saglabātu laika uzskaites tabulas ierakstu no programmas atpakaļ datu bāzē</span><span class="sxs-lookup"><span data-stu-id="ddf16-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="ddf16-234">Lai saglabātu pielāgotu lauku datu bāzē tipiska lietojuma veidā, ir jāpaplašina vairākas metodes:</span><span class="sxs-lookup"><span data-stu-id="ddf16-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="ddf16-235">Metode **timesheetLineNeedsUpdating** tiek izmantota, lai noteiktu, vai lietotājs programmā ir mainījis rindas ierakstu un vai tas ir jāsaglabā datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="ddf16-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="ddf16-236">Ja veiktspēja nerada bažas, šo metodi var vienkāršot, lai tā vienmēr atgrieztu **true**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="ddf16-237">Metodes **populateTimesheetLineFromEntryDuringCreate** un **populateTimesheetLineFromEntryDuringUpdate** var paplašināt tā, lai tās TSTimesheetLine datu bāzes ierakstā ievadītu vērtības no nodrošinātā TSTimesheetEntry datu līguma ieraksta.</span><span class="sxs-lookup"><span data-stu-id="ddf16-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="ddf16-238">Turpmāk norādītajā piemērā pievērsiet uzmanību tam, kā datu bāzes lauka un ieraksta lauka kartēšana tiek veikta manuāli, izmantojot X++ kodu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="ddf16-239">Metodi **populateTimesheetWeekFromEntry** var paplašināt arī tad, ja pielāgoto lauku, kas ir kartēts uz **TSTimesheetEntry** objektu, nepieciešams rakstīt atpakaļ uz TSTimesheetLineweek datu bāzes tabulu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="ddf16-240">Šajā piemērā tiek saglabāta **firstOption** vai **secondOption** vērtība, ko lietotājs atlasa datu bāzē kā neapstrādātu virknes vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddf16-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="ddf16-241">Ja datu bāzes lauks ir **Enum** veida lauks, šīs vērtības var manuāli kartēt uz uzskaitījuma vērtību un pēc tam saglabāt datu bāzes tabulas uzskaitījuma laukā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="ddf16-242">Pielāgota lauka rādīšana laika uzskaites tabulas galvenes sadaļā</span><span class="sxs-lookup"><span data-stu-id="ddf16-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="ddf16-243">Tālāk ir redzams ekrānuzņēmums, kurā mobilās programmas lietotājs skata laika uzskaites tabulu.</span><span class="sxs-lookup"><span data-stu-id="ddf16-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="ddf16-244">Augšējā labējā stūrī ir atlasīta poga “Papildinformācija”, lai parādītu opciju “Skatīt papildinformāciju”.</span><span class="sxs-lookup"><span data-stu-id="ddf16-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Detalizētas informācijas skatīšanas komanda](media/show-more.png)

<span data-ttu-id="ddf16-246">Tālāk ir redzams ekrānuzņēmums, kurā mobilajā programmā redzama laika uzskaites tabulas sadaļa “Vairāk”.</span><span class="sxs-lookup"><span data-stu-id="ddf16-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="ddf16-247">Pielāgots lauks, ko dēvē par “Šīs laika uzskaites tabulas izmantošanas biežums (aprēķinātais pielāgotais lauks), ir pievienots laika uzskaites tabulas galvenes sadaļai.</span><span class="sxs-lookup"><span data-stu-id="ddf16-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="ddf16-248">Pielāgotajā laukā ir iestatīta tikai lasāma vērtība “0,667”.</span><span class="sxs-lookup"><span data-stu-id="ddf16-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Papildu sadaļa](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="ddf16-250">TSTimesheetTable tabulas paplašināšana, lai tai būtu pielāgotais lauks</span><span class="sxs-lookup"><span data-stu-id="ddf16-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="ddf16-251">Tipiskos scenārijos ir iespējams, ka dati, kas paredzēti pielāgotajam laukam laika uzskaites tabulas galvenes sadaļā, tiks ņemti no tabulas TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="ddf16-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="ddf16-252">Taču var izmantot arī citas tabulas, ja datus var izgūt, pamatojoties uz nodrošinātu TSTimesheetTable ierakstu vai ja tiem nav konkrēta ieraksta konteksta (piemēram, ja lauks ir iestatīts kā tikai lasāms projekta parametros).</span><span class="sxs-lookup"><span data-stu-id="ddf16-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="ddf16-253">Ņemiet vērā, ka pielāgotajiem laukiem nav nepieciešami nekādi datu bāzes dublējuma ieraksti.</span><span class="sxs-lookup"><span data-stu-id="ddf16-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="ddf16-254">Tos var dinamiski ģenerēt, izmantojot X++ loģiku.</span><span class="sxs-lookup"><span data-stu-id="ddf16-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="ddf16-255">Tālāk parādīts piemērs, kas demonstrē šādu pieeju.</span><span class="sxs-lookup"><span data-stu-id="ddf16-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="ddf16-256">Galvenes sadaļas lauki programmā vienmēr ir tikai lasāmi.</span><span class="sxs-lookup"><span data-stu-id="ddf16-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="ddf16-257">Komandu ķēdes izmantošana buildCustomFieldList metodei TSTimesheetSettings klasē, lai parādītu lauku galvenes sadaļā</span><span class="sxs-lookup"><span data-stu-id="ddf16-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="ddf16-258">Šis kods kontrolē lauka rādīšanas iestatījumus programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="ddf16-259">Piemēram, tas kontrolē lauka tipu, etiķeti, to, vai lauks ir obligāts, kā arī to, kurā sadaļā šis lauks tiek rādīts.</span><span class="sxs-lookup"><span data-stu-id="ddf16-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="ddf16-260">Nākamajā piemērā ir parādīta aprēķinātā vērtība programmas galvenes sadaļā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="ddf16-261">Komandu ķēdes izmantošana buildCustomFieldListForHeader metodei TSTimesheetDetails klasē, lai ievadītu laika uzskaites tabulas detaļas</span><span class="sxs-lookup"><span data-stu-id="ddf16-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="ddf16-262">Metode **buildCustomFieldListForHeader** metode tiek izmantota, lai ievadītu laika uzskaites tabulas galvenes detaļas mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="ddf16-263">Kā parametrs tiek ņemts TSTimesheetTable ieraksts.</span><span class="sxs-lookup"><span data-stu-id="ddf16-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="ddf16-264">Šī ieraksta laukus var izmantot, lai programmā ievadītu pielāgotā lauka vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddf16-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="ddf16-265">Nākamajā piemērā netiek lasītas nekādas vērtības no datu bāzes.</span><span class="sxs-lookup"><span data-stu-id="ddf16-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="ddf16-266">Tā vietā tiek izmantota X++ loģika, lai ģenerētu aprēķināto vērtību, kas pēc tam tiek parādīta programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="ddf16-267">Citas konfigurēšanas/paplašināšanas iespējas</span><span class="sxs-lookup"><span data-stu-id="ddf16-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="ddf16-268">Papildu validācijas pievienošana programmai</span><span class="sxs-lookup"><span data-stu-id="ddf16-268">Adding additional validation for the app</span></span>

<span data-ttu-id="ddf16-269">Esošā laika uzskaites tabulas funkcionalitātes loģika datu bāzes līmenī joprojām darbosies kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="ddf16-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="ddf16-270">Lai pārtrauktu saglabāšanas vai iesniegšanas operāciju pabeigšanu un parādītu konkrētu kļūdas ziņojumu, varat pievienot kodam **throw error("message to user")**, izmantojot komandu paplašinājuma ķēdi.</span><span class="sxs-lookup"><span data-stu-id="ddf16-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="ddf16-271">Tālāk norādīti trīs noderīgi paplašināmo metožu piemēri.</span><span class="sxs-lookup"><span data-stu-id="ddf16-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="ddf16-272">Ja **validateWrite** tabulā TSTimesheetLine atgriež **false** laika uzskaites rindas saglabāšanas operācijas laikā, mobilajā programmā tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="ddf16-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="ddf16-273">Ja **validateSubmit** tabulā TSTimesheetTable atgriež **false** laika uzskaites rindas iesniegšanas laikā programmā, lietotājam tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="ddf16-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="ddf16-274">Loģika, kas aizpilda laukus (piemēram, **Rindas rekvizīts**), metodes **insert** laikā tabulā TSTimesheetLine joprojām darbosies.</span><span class="sxs-lookup"><span data-stu-id="ddf16-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="ddf16-275">Iebūvēto lauku paslēpšana un atzīmēšana kā tikai lasāmus, izmantojot konfigurēšanu</span><span class="sxs-lookup"><span data-stu-id="ddf16-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="ddf16-276">Izmantojot projekta parametrus, iebūvētos laukus var padarīt tikai lasāmus vai paslēptus mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="ddf16-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="ddf16-277">Iestatiet opcijas sadaļā **Mobilās laika uzskaites tabulas** cilnē **Laika uzskaites tabula**, kas atrodas lapā **Projekta pārvaldības un grāmatvedības parametri**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projekta parametri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="ddf16-279">To darbību mainīšana, kas pieejamas atlasei, izmantojot paplašinājumus</span><span class="sxs-lookup"><span data-stu-id="ddf16-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="ddf16-280">Darbības, kas ir pieejamas projekta atlasei, tiek aizpildītas, izmantojot metodes **getActivitiesForProject()** un **getActivityQuery()** klasē **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="ddf16-281">Varat izmantot komandu ķēdi, lai mainītu šo uzvedību atbilstoši jūsu biznesa scenārijam attiecībā uz darbībām, kas ir pieejamas atlasīšanai noteiktam projektam.</span><span class="sxs-lookup"><span data-stu-id="ddf16-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="ddf16-282">Noklusējuma projekta kategorijas ievadīšana laika uzskaites tabulas ierakstos</span><span class="sxs-lookup"><span data-stu-id="ddf16-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="ddf16-283">Noklusējuma projekta kategorijas ieraksts laika uzskaites tabulas ierakstos notiek trīs līmeņos.</span><span class="sxs-lookup"><span data-stu-id="ddf16-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="ddf16-284">Varat izmantot komandu ķēdi, lai izvērstu uzvedību jebkurā vai visos šajos līmeņos un panāktu nepieciešamo uzvedību.</span><span class="sxs-lookup"><span data-stu-id="ddf16-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="ddf16-285">Tiek izmantota tālāk norādītā hierarhija.</span><span class="sxs-lookup"><span data-stu-id="ddf16-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="ddf16-286">Programma mēģina ievietot noklusējuma kategoriju no projekta resursa.</span><span class="sxs-lookup"><span data-stu-id="ddf16-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="ddf16-287">Šī noklusējuma kategorija ir iestatīta metodēs **getCurrentUserResource** un **getDelegatedResourcesForCurrentUser** klasē **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="ddf16-288">Ja noklusējuma kategorija netiek nodrošināta projekta resursu līmenī, programma mēģina to izgūt no projekta darbības.</span><span class="sxs-lookup"><span data-stu-id="ddf16-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="ddf16-289">Šī noklusējuma kategorija ir iestatīta metodē **getActivitiesForProject** klasē **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="ddf16-290">Ja noklusējuma kategorija netiek nodrošināta projekta aktivitātes līmenī, noklusējuma kategorija tiek izgūta no projekta parametriem.</span><span class="sxs-lookup"><span data-stu-id="ddf16-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="ddf16-291">Šī noklusējuma kategorija ir iestatīta metodē **getProjectDetailsbyRule** klasē **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="ddf16-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]