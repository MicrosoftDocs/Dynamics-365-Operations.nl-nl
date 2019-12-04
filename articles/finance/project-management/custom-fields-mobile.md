---
title: Aangepaste velden voor de app Microsoft Dynamics 365 Project Timesheet implementeren in iOS en Android
description: Dit onderwerp bevat algemene patronen voor het gebruik van extensies voor het implementeren van aangepaste velden.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: c0c578ca44919671b67daeea51a9ec7687f755c9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773640"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="e73f3-103">Aangepaste velden voor de app Microsoft Dynamics 365 Project Timesheet implementeren in iOS en Android</span><span class="sxs-lookup"><span data-stu-id="e73f3-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e73f3-104">Dit onderwerp bevat algemene patronen voor het gebruik van extensies voor het implementeren van aangepaste velden.</span><span class="sxs-lookup"><span data-stu-id="e73f3-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="e73f3-105">De volgende onderwerpen zijn opgenomen:</span><span class="sxs-lookup"><span data-stu-id="e73f3-105">The following topics are covered:</span></span>

- <span data-ttu-id="e73f3-106">De verschillende gegevenstypen die door het raamwerk voor aangepaste velden worden ondersteund</span><span class="sxs-lookup"><span data-stu-id="e73f3-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="e73f3-107">Alleen-lezen- of bewerkbare velden weergeven in urenstaatinvoer en door de gebruiker opgegeven waarden opslaan in de database</span><span class="sxs-lookup"><span data-stu-id="e73f3-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="e73f3-108">Alleen-lezenvelden weergeven in de roosterkoptekst</span><span class="sxs-lookup"><span data-stu-id="e73f3-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="e73f3-109">Andere aangepaste bedrijfslogica integreren integreren om standaardwaarden in velden in te voeren en extra validatie uit te voeren</span><span class="sxs-lookup"><span data-stu-id="e73f3-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="e73f3-110">Doelgroep</span><span class="sxs-lookup"><span data-stu-id="e73f3-110">Audience</span></span>

<span data-ttu-id="e73f3-111">Dit onderwerp is bedoeld voor ontwikkel aars die hun aangepaste velden integreren in app Microsoft Dynamics 365 Project Timesheet die beschikbaar is voor Apple IOS en Google Android.</span><span class="sxs-lookup"><span data-stu-id="e73f3-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="e73f3-112">De veronderstelling is dat lezers vertrouwd zijn met X++-ontwikkeling en de functionaliteit voor projecturenstaten.</span><span class="sxs-lookup"><span data-stu-id="e73f3-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="e73f3-113">Gegevenscontract – TSTimesheetCustomField X++-klasse</span><span class="sxs-lookup"><span data-stu-id="e73f3-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="e73f3-114">De klasse **TSTimesheetCustomField** is de X++-gegevenscontractklasse die staat voor informatie over een aangepast veld voor urenstaatfunctionaliteit.</span><span class="sxs-lookup"><span data-stu-id="e73f3-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="e73f3-115">Lijsten met de aangepaste veldobjecten worden zowel in het TSTimesheetDetails-gegevenscontract als in het TSTimesheetEntry-gegevenscontract doorgegeven om aangepaste velden in de mobiele app weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="e73f3-116">**TSTimesheetDetails** - Het roosterkoptekstcontract.</span><span class="sxs-lookup"><span data-stu-id="e73f3-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="e73f3-117">**TSTimesheetEntry** - Het urenstaattransactiecontract.</span><span class="sxs-lookup"><span data-stu-id="e73f3-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="e73f3-118">Groepen van deze objecten met dezelfde projectgegevens en waarde voor **timesheetLineRecId** vormen een regel.</span><span class="sxs-lookup"><span data-stu-id="e73f3-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="e73f3-119">fieldBaseType (typen)</span><span class="sxs-lookup"><span data-stu-id="e73f3-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="e73f3-120">De eigenschap **FieldBaseType** van het object **TsTimesheetCustom** bepaalt welk type veld wordt weergegeven in de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="e73f3-121">De volgende waarden voor **Typen** worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="e73f3-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="e73f3-122">Waarden voor typen</span><span class="sxs-lookup"><span data-stu-id="e73f3-122">Types value</span></span> | <span data-ttu-id="e73f3-123">Type</span><span class="sxs-lookup"><span data-stu-id="e73f3-123">Type</span></span>              | <span data-ttu-id="e73f3-124">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e73f3-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="e73f3-125">0</span><span class="sxs-lookup"><span data-stu-id="e73f3-125">0</span></span>           | <span data-ttu-id="e73f3-126">Tekenreeks (en vaste tekst)</span><span class="sxs-lookup"><span data-stu-id="e73f3-126">String (and Enum)</span></span> | <span data-ttu-id="e73f3-127">Het veld wordt weergegeven als een tekstveld.</span><span class="sxs-lookup"><span data-stu-id="e73f3-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="e73f3-128">1</span><span class="sxs-lookup"><span data-stu-id="e73f3-128">1</span></span>           | <span data-ttu-id="e73f3-129">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="e73f3-129">Integer</span></span>           | <span data-ttu-id="e73f3-130">De waarde wordt weer gegeven als een getal zonder decimalen.</span><span class="sxs-lookup"><span data-stu-id="e73f3-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="e73f3-131">2</span><span class="sxs-lookup"><span data-stu-id="e73f3-131">2</span></span>           | <span data-ttu-id="e73f3-132">Real-modus</span><span class="sxs-lookup"><span data-stu-id="e73f3-132">Real</span></span>              | <span data-ttu-id="e73f3-133">De waarde wordt weergegeven als een getal met decimalen.</span><span class="sxs-lookup"><span data-stu-id="e73f3-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="e73f3-134">Als u de echte waarde wilt weergeven als een valuta in de app, gebruikt u de eigenschap **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="e73f3-135">U kunt de eigenschap **numberOfDecimals** gebruiken om het aantal decimalen in te stellen dat wordt weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="e73f3-136">3</span><span class="sxs-lookup"><span data-stu-id="e73f3-136">3</span></span>           | <span data-ttu-id="e73f3-137">Datum</span><span class="sxs-lookup"><span data-stu-id="e73f3-137">Date</span></span>              | <span data-ttu-id="e73f3-138">Datumnotaties worden bepaald door de instelling **Datum-, tijd- en getalnotatie** van de gebruiker die is opgegeven onder **Voorkeuren voor taal en land/regio** in **Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="e73f3-139">4</span><span class="sxs-lookup"><span data-stu-id="e73f3-139">4</span></span>           | <span data-ttu-id="e73f3-140">Booleaans</span><span class="sxs-lookup"><span data-stu-id="e73f3-140">Boolean</span></span>           | |
| <span data-ttu-id="e73f3-141">15</span><span class="sxs-lookup"><span data-stu-id="e73f3-141">15</span></span>          | <span data-ttu-id="e73f3-142">GUID</span><span class="sxs-lookup"><span data-stu-id="e73f3-142">GUID</span></span>              | |
| <span data-ttu-id="e73f3-143">16</span><span class="sxs-lookup"><span data-stu-id="e73f3-143">16</span></span>          | <span data-ttu-id="e73f3-144">Int64</span><span class="sxs-lookup"><span data-stu-id="e73f3-144">Int64</span></span>             | |

- <span data-ttu-id="e73f3-145">Als de eigenschap **stringOptions** niet wordt opgegeven voor het object **TSTimesheetCustomField**, wordt er een vrije-tekstveld beschikbaar voor de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="e73f3-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="e73f3-146">De eigenschap **stringLength** kan worden gebruikt om de maximale tekenreekslengte in te stellen die gebruikers kunnen invoeren.</span><span class="sxs-lookup"><span data-stu-id="e73f3-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="e73f3-147">Als de eigenschap **stringOptions** is opgegeven voor het object **TSTimesheetCustomField**, zijn deze elementen de enige waarden die gebruikers kunnen selecteren met behulp van keuzerondjes.</span><span class="sxs-lookup"><span data-stu-id="e73f3-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="e73f3-148">In dit geval kan het tekenreeksveld fungeren als een opsommingswaarde voor gebruikersinvoer.</span><span class="sxs-lookup"><span data-stu-id="e73f3-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="e73f3-149">Als u de waarde als een opsommingswaarde in de database wilt opslaan, wijst u de tekenreekswaarde weer handmatig toe aan de opsommingswaarde voordat u opslaat naar de database opslaat met behulp van de opdrachtstructuur (zie Opdrachtstructuur voor de klasse TSTimesheetEntryService gebruiken om een urenstaatvermelding uit de app weer op te slaan in de database verderop in dit onderwerp voor een voorbeeld).</span><span class="sxs-lookup"><span data-stu-id="e73f3-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="e73f3-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="e73f3-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="e73f3-151">Met deze eigenschap kunt u echte waarden opmaken als valuta.</span><span class="sxs-lookup"><span data-stu-id="e73f3-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="e73f3-152">Dit kan alleen als **fieldBaseType** is ingesteld op **Werkelijk**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="e73f3-153">**TSCustomFieldExtendedType:None** – Er wordt geen opmaak toegepast.</span><span class="sxs-lookup"><span data-stu-id="e73f3-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="e73f3-154">**TSCustomFieldExtendedType::Valuta** – De waarde wordt opgemaakt als valuta.</span><span class="sxs-lookup"><span data-stu-id="e73f3-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="e73f3-155">Wanneer valuta-opmaak actief is, kan het veld **stringValue** worden gebruikt om de valutacode door te geven die in de app moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="e73f3-156">De waarde is een alleen-lezenwaarde.</span><span class="sxs-lookup"><span data-stu-id="e73f3-156">The value is a read-only value.</span></span>

    <span data-ttu-id="e73f3-157">Het veld **realValue** bevat het bedrag dat moet worden opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="e73f3-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="e73f3-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="e73f3-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="e73f3-159">U kunt deze eigenschap gebruiken om op te geven waar het aangepaste veld moet worden weergegeven in de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="e73f3-160">**TSCustomFieldSection::Koptekst** – Het veld wordt weergegeven in de sectie **Meer details weergeven** in de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="e73f3-161">Deze velden zijn altijd alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="e73f3-161">These fields are always read-only.</span></span>
- <span data-ttu-id="e73f3-162">**TSCustomFieldSection::Regel** –Het veld wordt weergegeven na alle kant-en-klare regelvelden in urenstaatinvoer.</span><span class="sxs-lookup"><span data-stu-id="e73f3-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="e73f3-163">Deze velden kunnen bewerkbaar of alleen-lezen zijn.</span><span class="sxs-lookup"><span data-stu-id="e73f3-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="e73f3-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="e73f3-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="e73f3-165">Met deze eigenschap wordt het veld aangegeven wanneer waarden uit de app worden opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="e73f3-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="e73f3-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="e73f3-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="e73f3-167">Met deze eigenschap wordt het veld aangegeven wanneer waarden uit de app worden opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="e73f3-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="e73f3-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="e73f3-168">isEditable (NoYes)</span></span>

<span data-ttu-id="e73f3-169">Stel deze eigenschap in op **Ja** om op te geven dat het veld in de sectie voor het invoeren van urenstaten moet kunnen worden bewerkt door gebruikers.</span><span class="sxs-lookup"><span data-stu-id="e73f3-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="e73f3-170">Stel de eigenschap in op **Nee** als u het veld alleen-lezen wilt maken.</span><span class="sxs-lookup"><span data-stu-id="e73f3-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="e73f3-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="e73f3-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="e73f3-172">Stel deze eigenschap in op **Ja** om op te geven dat het veld in de sectie voor het invoeren van urenstaten verplicht is.</span><span class="sxs-lookup"><span data-stu-id="e73f3-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="e73f3-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="e73f3-173">label (str)</span></span>

<span data-ttu-id="e73f3-174">Met deze eigenschap wordt het label opgegeven dat naast het vel wordt weergegeven in de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="e73f3-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="e73f3-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="e73f3-176">Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="e73f3-177">Als **stringOptions** is ingesteld, wordt op basis van de tekenreeksen in de lijst bepaald welke tekenreekswaarden beschikbaar zijn voor selectie via keuzerondjes.</span><span class="sxs-lookup"><span data-stu-id="e73f3-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="e73f3-178">Als er geen tekenreeksen zijn opgegeven, is vrije-tekstinvoer toegestaan in het tekenreeksveld (zie Opdrachtstructuur voor de klasse TSTimesheetEntryService gebruiken om een urenstaatvermelding uit de app weer op te slaan in de database verderop in dit onderwerp voor een voorbeeld).</span><span class="sxs-lookup"><span data-stu-id="e73f3-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="e73f3-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="e73f3-179">stringLength (int)</span></span>

<span data-ttu-id="e73f3-180">Met deze eigenschap geeft u de maximumlengte voor een tekenreeksveld op.</span><span class="sxs-lookup"><span data-stu-id="e73f3-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="e73f3-181">Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="e73f3-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="e73f3-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="e73f3-183">Met deze eigenschap geeft u het aantal decimalen op dat voor een werkelijk veld wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="e73f3-184">Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **Werkelijk**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="e73f3-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="e73f3-185">orderSequence (int)</span></span>

<span data-ttu-id="e73f3-186">Deze eigenschap bepaalt de volgorde waarin de aangepaste velden in de app worden weergegeven wanneer meerdere aangepaste velden worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="e73f3-187">Velden met een lagere waarde worden als eerste weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="e73f3-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="e73f3-188">booleanValue (boolean)</span></span>

<span data-ttu-id="e73f3-189">Voor velden van het type **Booleaans** geeft deze eigenschap de Booleaanse waarde van het veld tussen de server en de app door.</span><span class="sxs-lookup"><span data-stu-id="e73f3-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="e73f3-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="e73f3-190">guidValue (guid)</span></span>

<span data-ttu-id="e73f3-191">Voor velden van het type **GUID** geeft deze eigenschap de GUID-waarde van het veld tussen de server en de app door.</span><span class="sxs-lookup"><span data-stu-id="e73f3-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="e73f3-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="e73f3-192">int64Value (int64)</span></span>

<span data-ttu-id="e73f3-193">Voor velden van het type **Int64** geeft deze eigenschap de int64-waarde van het veld tussen de server en de app door.</span><span class="sxs-lookup"><span data-stu-id="e73f3-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="e73f3-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="e73f3-194">intValue (int)</span></span>

<span data-ttu-id="e73f3-195">Voor velden van het type **Int** geeft deze eigenschap de int-waarde van het veld tussen de server en de app door.</span><span class="sxs-lookup"><span data-stu-id="e73f3-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="e73f3-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="e73f3-196">realValue (real)</span></span>

<span data-ttu-id="e73f3-197">Voor velden van het type **Werkelijk** geeft deze eigenschap de werkelijke waarde van het veld tussen de server en de app door.</span><span class="sxs-lookup"><span data-stu-id="e73f3-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="e73f3-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="e73f3-198">stringValue (str)</span></span>

<span data-ttu-id="e73f3-199">Voor velden van het type **Tekenreeks** geeft deze eigenschap de tekenreekswaarde van het veld tussen de server en de app door.</span><span class="sxs-lookup"><span data-stu-id="e73f3-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="e73f3-200">Deze eigenschap wordt ook gebruikt voor velden van het type **Werkelijk** die zijn opgemaakt als valuta.</span><span class="sxs-lookup"><span data-stu-id="e73f3-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="e73f3-201">Voor deze velden wordt de eigenschap gebruikt om de valutacode door te geven aan de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="e73f3-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="e73f3-202">dateValue (date)</span></span>

<span data-ttu-id="e73f3-203">Voor velden van het type **Datum** geeft deze eigenschap de datumwaarde van het veld tussen de server en de app door.</span><span class="sxs-lookup"><span data-stu-id="e73f3-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="e73f3-204">Een aangepast veld weergeven en opslaan in de sectie voor de invoer van urenstaten</span><span class="sxs-lookup"><span data-stu-id="e73f3-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="e73f3-205">Hieronder vindt u een schermopname van de mobiele app tijdens het maken van urenstaatinvoer.</span><span class="sxs-lookup"><span data-stu-id="e73f3-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="e73f3-206">U ziet de kant-en-klare velden en een aangepast veld in de sectie Tijdinvoer met de naam Testtekenreeks en als opsommingswaarde Tweede optie.</span><span class="sxs-lookup"><span data-stu-id="e73f3-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Aangepast veld Testtekenreeks in de app](media/timesheet-entry.jpg)



<span data-ttu-id="e73f3-208">Hieronder ziet u een schermopname van de mobiele app van de gebruiker die een van de beschikbare opsommingsopties voor het aangepaste veld Testtekenreeks selecteert.</span><span class="sxs-lookup"><span data-stu-id="e73f3-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="e73f3-209">De twee opties zijn Eerste optie en Tweede optie, weergegeven als keuzerondjes.</span><span class="sxs-lookup"><span data-stu-id="e73f3-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="e73f3-210">De tweede optie is momenteel geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e73f3-210">The second option is currently selected.</span></span>

![Keuzerondjes voor het aangepaste veld Testtekenreeks](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="e73f3-212">De tabel TSTimesheetLine uitbreiden met een aangepast veld</span><span class="sxs-lookup"><span data-stu-id="e73f3-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="e73f3-213">In de meeste scenario's worden de gegevens voor een aangepast veld in de sectie voor het invoeren van urenstaten opgeslagen in de tabel TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="e73f3-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="e73f3-214">Er kunnen echter andere tabellen worden gebruikt als de gegevens kunnen worden opgehaald op basis van een TSTimesheetTrans-record die wordt geleverd of als er geen specifieke recordcontext is (bijvoorbeeld als het veld is ingesteld als alleen-lezen in de projectparameters).</span><span class="sxs-lookup"><span data-stu-id="e73f3-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="e73f3-215">Houd er rekening mee dat aangepaste velden geen back-ups van databaserecords hoeven te hebben.</span><span class="sxs-lookup"><span data-stu-id="e73f3-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="e73f3-216">Deze kunnen dynamisch worden gegenereerd op basis van X + +-logica.</span><span class="sxs-lookup"><span data-stu-id="e73f3-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="e73f3-217">Deze benadering kan handig zijn in alleen-lezenscenario's (zie Opdrachtstructuur van de methode buildCustomFieldListForHeader in de klasse TSTimesheetDetailsmethode gebruiken om details van urenstaten in te vullen voor een voorbeeld van dynamisch gegenereerde waarden van aangepaste velden.)</span><span class="sxs-lookup"><span data-stu-id="e73f3-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="e73f3-218">Hieronder ziet u een schermopname uit Visual Studio van de Application Object Tree.</span><span class="sxs-lookup"><span data-stu-id="e73f3-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="e73f3-219">Het bevat een uitbreiding van de tabel TSTimesheetLine, waarbij het veld TestLineString als een aangepast veld is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e73f3-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Regeltekenreeks](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="e73f3-221">Opdrachtstructuur voor de methode buildCustomFieldList van de klasse TSTimesheetSettings gebruiken om een veld weer te geven in de sectie voor het invoeren van urenstaten</span><span class="sxs-lookup"><span data-stu-id="e73f3-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="e73f3-222">Met deze code bepaalt u de weergave-instellingen voor het veld in de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="e73f3-223">U bepaalt bijvoorbeeld het type veld, het label, of het veld verplicht is en in welke sectie het veld voorkomt.</span><span class="sxs-lookup"><span data-stu-id="e73f3-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="e73f3-224">In het volgende voorbeeld wordt een tekenreeksveld voor tijdsinvoeren weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="e73f3-225">Dit veld heeft twee opties, **Eerste optie** en **Tweede optie**, die beschikbaar zijn via keuzerondjes.</span><span class="sxs-lookup"><span data-stu-id="e73f3-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="e73f3-226">Het veld in de app is gekoppeld aan het veld **TestLineString** dat aan de tabel TSTimesheetLine is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e73f3-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="e73f3-227">U kunt de methode **TSTimesheetCustomField::newFromMetatdata()** gebruiken om de initialisatie van de eigenschappen van aangepaste velden te vereenvoudigen: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** en **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="e73f3-228">U kunt deze parameters ook handmatig instellen, zoals u wilt.</span><span class="sxs-lookup"><span data-stu-id="e73f3-228">You can also set these parameters manually, as you prefer.</span></span>

```
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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="e73f3-229">Opdrachtstructuur voor de methode buildCustomFieldListForEntry van de klasse TSTimesheetEntry gebruiken om waarden in te voeren in een urenstaatboeking</span><span class="sxs-lookup"><span data-stu-id="e73f3-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="e73f3-230">De methode **buildCustomFieldListForEntry** wordt gebruikt om waarden in te voeren op de opgeslagen urenstaatregels in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="e73f3-231">Een TSTimesheetTrans-record wordt als parameter gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e73f3-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="e73f3-232">Velden uit deze record kunnen worden gebruikt om de waarde voor het aangepaste veld in de app in te vullen.</span><span class="sxs-lookup"><span data-stu-id="e73f3-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="e73f3-233">Opdrachtstructuur voor de klasse TSTimesheetEntryService gebruiken om een urenstaatvermelding uit de app weer op te slaan in de database</span><span class="sxs-lookup"><span data-stu-id="e73f3-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="e73f3-234">Als u een aangepast veld op de normale wijze weer in de database wilt opslaan, moet u meerdere methoden uitbreiden:</span><span class="sxs-lookup"><span data-stu-id="e73f3-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="e73f3-235">De methode **timesheetLineNeedsUpdating** wordt gebruikt om te bepalen of de regelrecord door de gebruiker in de app is gewijzigd en moet worden opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="e73f3-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="e73f3-236">Als prestaties geen probleem zijn, kan deze methode worden vereenvoudigd zodat altijd **waar**wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e73f3-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="e73f3-237">De methoden **populateTimesheetLineFromEntryDuringCreate** en **populateTimesheetLineFromEntryDuringUpdate** kunnen worden uitgebreid zodat hiermee waarden in de TSTimesheetLine-databaserecord worden ingevoerd vanuit de TSTimesheetEntry-gegevenscontractrecord.</span><span class="sxs-lookup"><span data-stu-id="e73f3-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="e73f3-238">In het volgende voorbeeld ziet u hoe de toewijzing tussen het databaseveld en het invoerveld handmatig wordt uitgevoerd via X + +-code.</span><span class="sxs-lookup"><span data-stu-id="e73f3-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="e73f3-239">De methode **populateTimesheetWeekFromEntry** kan ook worden uitgebreid als het aangepaste veld dat aan het object **TSTimesheetEntry** is toegewezen, moet worden teruggeschreven naar de TSTimesheetLineweek-databasetabel.</span><span class="sxs-lookup"><span data-stu-id="e73f3-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="e73f3-240">In het volgende voorbeeld wordt de door de gebruiker geselecteerde waarde **firstOption** of **secondOption** als onbewerkte tekenreekswaarde opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="e73f3-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="e73f3-241">Als het databaseveld een veld van het type **Opsomming** is, kunnen deze waarden handmatig worden toegewezen aan een opsommingswaarde en vervolgens worden opgeslagen in een opsommingsveld in de databasetabel.</span><span class="sxs-lookup"><span data-stu-id="e73f3-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="e73f3-242">Een aangepast veld weergeven in de sectie voor de roosterkoptekst</span><span class="sxs-lookup"><span data-stu-id="e73f3-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="e73f3-243">Hieronder vindt u een schermopname van de mobiele app van een gebruiker die een urenstaat weergeeft.</span><span class="sxs-lookup"><span data-stu-id="e73f3-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="e73f3-244">De knop Meer informatie is geselecteerd in de rechterbovenhoek om de optie Meer details weergeven weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Opdracht Meer details weergeven](media/show-more.png)

<span data-ttu-id="e73f3-246">Hieronder vindt u een schermopname van de mobiele app met de sectie Meer van een urenstaat.</span><span class="sxs-lookup"><span data-stu-id="e73f3-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="e73f3-247">Een aangepast veld met de naam Verbruikspercentage van deze urenstaat (berekend aangepast veld) is toegevoegd aan de koptekstsectie van de urenstaat.</span><span class="sxs-lookup"><span data-stu-id="e73f3-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="e73f3-248">Een alleen-lezenwaarde van 0,667 is ingesteld voor het aangepaste veld.</span><span class="sxs-lookup"><span data-stu-id="e73f3-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sectie Meer](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="e73f3-250">De tabel TSTimesheetTable uitbreiden met een aangepast veld</span><span class="sxs-lookup"><span data-stu-id="e73f3-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="e73f3-251">In de meeste scenario's worden de gegevens voor een aangepast veld in de koptekstsectie uit de tabel TSTimesheetHeader gehaald.</span><span class="sxs-lookup"><span data-stu-id="e73f3-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="e73f3-252">Er kunnen echter andere tabellen worden gebruikt als de gegevens kunnen worden opgehaald op basis van een TSTimesheetTable-record die wordt geleverd of als er geen specifieke recordcontext is (bijvoorbeeld als het veld is ingesteld als alleen-lezen in de projectparameters).</span><span class="sxs-lookup"><span data-stu-id="e73f3-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="e73f3-253">Houd er rekening mee dat aangepaste velden geen back-ups van databaserecords hoeven te hebben.</span><span class="sxs-lookup"><span data-stu-id="e73f3-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="e73f3-254">Deze kunnen dynamisch worden gegenereerd op basis van X + +-logica.</span><span class="sxs-lookup"><span data-stu-id="e73f3-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="e73f3-255">Het volgende voorbeeld wordt deze benadering weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="e73f3-256">Velden in de koptekstsectie zijn altijd alleen-lezen in de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="e73f3-257">Opdrachtstructuur voor de methode buildCustomFieldList van de klasse TSTimesheetSettings gebruiken om een veld weer te geven in de koptekstsectie</span><span class="sxs-lookup"><span data-stu-id="e73f3-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="e73f3-258">Met deze code bepaalt u de weergave-instellingen voor het veld in de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="e73f3-259">U bepaalt bijvoorbeeld het type veld, het label, of het veld verplicht is en in welke sectie het veld voorkomt.</span><span class="sxs-lookup"><span data-stu-id="e73f3-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="e73f3-260">In het volgende voorbeeld wordt een berekende waarde in de koptekstsectie van de app weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e73f3-260">The following example shows a computed value in the header section in the app.</span></span>

```
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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="e73f3-261">Opdrachtstructuur voor de methode buildCustomFieldListForHeader van de klasse TSTimesheetDetails gebruiken om details van urenstaten in te vullen</span><span class="sxs-lookup"><span data-stu-id="e73f3-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="e73f3-262">De methode **buildCustomFieldListForHeader** wordt gebruikt om koptekstdetails voor urenstaten in te vullen in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="e73f3-263">Een TSTimesheetTable-record wordt als parameter gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e73f3-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="e73f3-264">Velden uit deze record kunnen worden gebruikt om de waarde voor het aangepaste veld in de app in te vullen.</span><span class="sxs-lookup"><span data-stu-id="e73f3-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="e73f3-265">In het volgende voorbeeld worden geen waarden gelezen uit de database.</span><span class="sxs-lookup"><span data-stu-id="e73f3-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="e73f3-266">In plaats daarvan wordt X + +-logica gebruikt om een berekende waarde te genereren die vervolgens wordt weergegeven in de app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="e73f3-267">Overige mogelijkheden voor configuratie/uitbreidbaarheid</span><span class="sxs-lookup"><span data-stu-id="e73f3-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="e73f3-268">Aanvullende validatie voor de app toevoegen</span><span class="sxs-lookup"><span data-stu-id="e73f3-268">Adding additional validation for the app</span></span>

<span data-ttu-id="e73f3-269">Bestaande logica voor urenstaatfunctionaliteit op databaseniveau werkt nog steeds zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="e73f3-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="e73f3-270">Als u het voltooien van bewerkingen voor opslaan of indienen wilt onderbreken en een specifiek foutbericht wilt weergeven, kunt u **throw error("message to user")** aan de code toevoegen door een opdrachtstructuur uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="e73f3-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="e73f3-271">Hier volgen drie voorbeelden van handige uitbreidbare methoden:</span><span class="sxs-lookup"><span data-stu-id="e73f3-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="e73f3-272">Als **validateWrite** voor de tabel TSTimesheetLine **onwaar** retourneert tijdens het opslaan voor een urenstaatregel, wordt een foutbericht weergegeven in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="e73f3-273">Als **validateSubmit** voor de tabel TSTimesheetTable **onwaar** retourneert tijdens het indienen van de urenstaat in de app, wordt een foutbericht weergegeven voor de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="e73f3-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="e73f3-274">De logica waarmee velden worden ingevuld (bijvoorbeeld **Regeleigenschap**) tijdens de methode **invoegen** in de tabel TSTimesheetLine wordt nog steeds uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e73f3-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="e73f3-275">Standaardvelden verbergen en als alleen-lezen markeren via configuratie</span><span class="sxs-lookup"><span data-stu-id="e73f3-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="e73f3-276">Vanuit de projectparameters kunt u standaardvelden alleen-lezen maken of verbergen in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="e73f3-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="e73f3-277">Stel de opties in de sectie **Mobiele urenstaten** op het tabblad **Urenstaat** van de pagina **Projectbeheer- en boekhoudingsparameters** in.</span><span class="sxs-lookup"><span data-stu-id="e73f3-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projectparameters](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="e73f3-279">De beschikbare activiteiten voor selectie via uitbreidingen wijzigen</span><span class="sxs-lookup"><span data-stu-id="e73f3-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="e73f3-280">De activiteiten die beschikbaar zijn voor selectie voor een project, worden gevuld via de methoden **getActivitiesForProject()** en **getActivityQuery()** in de klasse **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="e73f3-281">U kunt een reeks opdrachten gebruiken om dit gedrag aan te passen aan uw bedrijfsscenario voor de activiteiten die kunnen worden geselecteerd voor een specifiek project.</span><span class="sxs-lookup"><span data-stu-id="e73f3-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="e73f3-282">Een standaardprojectcategorie invoeren voor urenstaatvermeldingen</span><span class="sxs-lookup"><span data-stu-id="e73f3-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="e73f3-283">Het invoeren van een standaardprojectcategorie voor urenstaatvermeldingen vindt plaats op drie niveaus.</span><span class="sxs-lookup"><span data-stu-id="e73f3-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="e73f3-284">U kunt een reeks opdrachten gebruiken om het gedrag op een of meer van deze niveaus uit te breiden om het gewenste gedrag te krijgen.</span><span class="sxs-lookup"><span data-stu-id="e73f3-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="e73f3-285">De volgende hiërarchie wordt hierbij gebruikt:</span><span class="sxs-lookup"><span data-stu-id="e73f3-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="e73f3-286">De app probeert de standaardcategorie uit de projectresource te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="e73f3-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="e73f3-287">Deze standaardcategorie wordt ingesteld in de methoden **getCurrentUserResource** en **getDelegatedResourcesForCurrentUser** in de klasse **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="e73f3-288">Als de standaardcategorie niet is opgegeven op het niveau van de projectresource, probeert de app deze te halen uit de projectactiviteit.</span><span class="sxs-lookup"><span data-stu-id="e73f3-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="e73f3-289">Deze standaardcategorie wordt ingesteld in de methode **getActivitiesForProject** in de klasse **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="e73f3-290">Als de standaardcategorie niet is opgegeven op het niveau van de projectactiviteit, wordt de standaardcategorie uit de projectparameters gehaald.</span><span class="sxs-lookup"><span data-stu-id="e73f3-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="e73f3-291">Deze standaardcategorie wordt ingesteld in de methode **getProjectDetailsbyRule** in de klasse **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="e73f3-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
