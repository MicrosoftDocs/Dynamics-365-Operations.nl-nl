---
title: Een configuratie ontwerpen voor het genereren van documenten in Excel-indeling
description: Dit onderwerp bevat informatie over het ontwerpen van een ER-indeling (Elektronische rapportage) voor het invullen van een Excel-sjabloon en het genereren van uitgaande Excel-documenten.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375808"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="47c65-103">Een configuratie ontwerpen voor het genereren van documenten in Excel-indeling</span><span class="sxs-lookup"><span data-stu-id="47c65-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="47c65-104">U kunt een [ER](general-electronic-reporting.md)-indelingsconfiguratie ontwerpen met een ER-[indelingsonderdeel](general-electronic-reporting.md#FormatComponentOutbound) dat u kunt configureren om een uitgaand document in een Microsoft Excel-werkmapindeling te genereren.</span><span class="sxs-lookup"><span data-stu-id="47c65-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="47c65-105">Hiervoor moeten specifieke ER-indelingsonderdelen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="47c65-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="47c65-106">Volg de stappen in het onderwerp [Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](tasks/er-design-reports-openxml-2016-11.md) voor meer informatie over deze functie.</span><span class="sxs-lookup"><span data-stu-id="47c65-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="47c65-107">Een nieuwe ER-indeling toevoegen</span><span class="sxs-lookup"><span data-stu-id="47c65-107">Add a new ER format</span></span>

<span data-ttu-id="47c65-108">Wanneer u een nieuwe ER-indelingsconfiguratie toevoegt om een uitgaand document in een Excel-werkmapindeling te genereren, moet u de waarde **Excel** voor het kenmerk **Type indeling** van de indeling selecteren of het kenmerk **Type indeling** leeg laten.</span><span class="sxs-lookup"><span data-stu-id="47c65-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="47c65-109">Als u **Excel** selecteert, kunt u de indeling zo configureren dat een uitgaand document alleen in de Excel-indeling wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="47c65-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="47c65-110">Als u het kenmerk leeg laat, kunt u de indeling configureren om een uitgaand document te genereren in elke indeling die wordt ondersteund door het ER-raamwerk.</span><span class="sxs-lookup"><span data-stu-id="47c65-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="47c65-111">Als u het ER-indelingsonderdeel van de configuratie wilt configureren, selecteert u **Ontwerper** in het actievenster en opent u het ER-indelingsonderdeel in de ER Operations-ontwerper.</span><span class="sxs-lookup"><span data-stu-id="47c65-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Pagina Configuraties](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="47c65-113">Excel-bestandsonderdeel</span><span class="sxs-lookup"><span data-stu-id="47c65-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="47c65-114">Handmatige invoer</span><span class="sxs-lookup"><span data-stu-id="47c65-114">Manual entry</span></span>

<span data-ttu-id="47c65-115">U moet een onderdeel **Excel\\Bestand** toevoegen aan de geconfigureerde ER-indeling om een uitgaand document in Excel-indeling te genereren.</span><span class="sxs-lookup"><span data-stu-id="47c65-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Onderdeel Excel\Bestand](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="47c65-117">Als u de indeling van het uitgaande document wilt opgeven, voegt u een Excel-werkmap met de extensie .xlsx toe aan het onderdeel **Excel\\Bestand** als sjabloon voor uitgaande documenten.</span><span class="sxs-lookup"><span data-stu-id="47c65-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="47c65-118">Wanneer u handmatig een sjabloon toevoegt, moet u een [documenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) gebruiken dat in de [ER-parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) voor dat doel is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="47c65-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Een bijlage toevoegen aan het onderdeel Excel\Bestand](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="47c65-120">Als u wilt opgeven hoe de toegevoegde sjabloon wordt ingevuld wanneer u de geconfigureerde ER-indeling uitvoert, moet u geneste onderdelen **Werkblad**, **Bereik** en **Cel** toevoegen aan het onderdeel **Excel\\Bestand**.</span><span class="sxs-lookup"><span data-stu-id="47c65-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="47c65-121">Elk genest onderdeel moet worden gekoppeld aan een benoemd Excel-item.</span><span class="sxs-lookup"><span data-stu-id="47c65-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="47c65-122">Sjabloonimport</span><span class="sxs-lookup"><span data-stu-id="47c65-122">Template import</span></span>

<span data-ttu-id="47c65-123">U kunt **Importeren uit Excel** selecteren op het tabblad **Importeren** van het actievenster om een nieuwe sjabloon te importeren in een lege ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="47c65-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="47c65-124">In dit voorbeeld wordt automatisch een onderdeel **Excel\\Bestand** gemaakt en de geïmporteerde sjabloon wordt hieraan toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="47c65-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="47c65-125">Alle vereiste ER-onderdelen worden ook automatisch gemaakt, op basis van de lijst met Excel-artikelen die worden ontdekt.</span><span class="sxs-lookup"><span data-stu-id="47c65-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Importeren uit Excel selecteren](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="47c65-127">Als u het optionele element **Werkblad** wilt maken in de bewerkbare ER-indeling, stelt u de optie **Indelingselement Excel-werkblad maken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="47c65-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="47c65-128">Het onderdeel Werkblad</span><span class="sxs-lookup"><span data-stu-id="47c65-128">Sheet component</span></span>

<span data-ttu-id="47c65-129">Het onderdeel **Werkblad** geeft een werkblad aan van de bijgevoegde Excel-werkmap die moet worden ingevuld.</span><span class="sxs-lookup"><span data-stu-id="47c65-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="47c65-130">De naam van het werkblad in een Excel-sjabloon wordt gedefinieerd in het eigenschap **Werkblad** van dit onderdeel.</span><span class="sxs-lookup"><span data-stu-id="47c65-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="47c65-131">Dit onderdeel is optioneel voor Excel-werkmappen die één werkblad bevatten.</span><span class="sxs-lookup"><span data-stu-id="47c65-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="47c65-132">Op het tabblad **Toewijzing** van de ER Operations-ontwerper kunt u de eigenschap **Ingeschakeld** voor een onderdeel **Werkblad** configureren om op te geven of het onderdeel in een gegenereerd document moet worden geplaatst:</span><span class="sxs-lookup"><span data-stu-id="47c65-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="47c65-133">Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Waar** te retourneren tijdens runtime, of als er helemaal geen expressie is geconfigureerd, wordt het betreffende werkblad in het gegenereerde document geplaatst.</span><span class="sxs-lookup"><span data-stu-id="47c65-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="47c65-134">Als een expressie van de eigenschap **Ingeschakeld** is ingesteld om **Onwaar** te retourneren tijdens runtime, bevat het gegenereerde document geen werkblad.</span><span class="sxs-lookup"><span data-stu-id="47c65-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Voorbeeld van een onderdeel Werkblad](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="47c65-136">Het onderdeel Bereik</span><span class="sxs-lookup"><span data-stu-id="47c65-136">Range component</span></span>

<span data-ttu-id="47c65-137">Het onderdeel **Bereik** geeft een Excel-bereik aan dat moet worden beheerd door dit ER-onderdeel.</span><span class="sxs-lookup"><span data-stu-id="47c65-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="47c65-138">De naam van het bereik wordt gedefinieerd in het eigenschap **Excel-bereik** van dit onderdeel.</span><span class="sxs-lookup"><span data-stu-id="47c65-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="47c65-139">De eigenschap **Replicatierichting** geeft aan of en hoe het bereik wordt herhaald in een gegenereerd document:</span><span class="sxs-lookup"><span data-stu-id="47c65-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="47c65-140">Als de eigenschap **Replicatierichting** is ingesteld op **Geen replicatie**, wordt het betreffende Excel-bereik niet herhaald in het gegenereerde document.</span><span class="sxs-lookup"><span data-stu-id="47c65-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="47c65-141">Als de eigenschap **Replicatierichting** is ingesteld op **Verticaal**, wordt het betreffende Excel-bereik herhaald in het gegenereerde document.</span><span class="sxs-lookup"><span data-stu-id="47c65-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="47c65-142">Elk gerepliceerd bereik wordt onder het oorspronkelijke bereik in een Excel-sjabloon geplaatst.</span><span class="sxs-lookup"><span data-stu-id="47c65-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="47c65-143">Het aantal herhalingen wordt gedefinieerd door het aantal records in een gegevensbron van het type **Recordlijst** dat is gekoppeld aan dit ER-onderdeel.</span><span class="sxs-lookup"><span data-stu-id="47c65-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="47c65-144">Als de eigenschap **Replicatierichting** is ingesteld op **Horizontaal**, wordt het betreffende Excel-bereik herhaald in het gegenereerde document.</span><span class="sxs-lookup"><span data-stu-id="47c65-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="47c65-145">Elk gerepliceerd bereik wordt rechts van het oorspronkelijke bereik in een Excel-sjabloon geplaatst.</span><span class="sxs-lookup"><span data-stu-id="47c65-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="47c65-146">Het aantal herhalingen wordt gedefinieerd door het aantal records in een gegevensbron van het type **Recordlijst** dat is gekoppeld aan dit ER-onderdeel.</span><span class="sxs-lookup"><span data-stu-id="47c65-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="47c65-147">Als u meer wilt weten over horizontale replicatie, volgt u de stappen in [Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="47c65-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="47c65-148">Het onderdeel **Bereik** kan andere geneste ER-onderdelen bevatten die worden gebruikt om waarden op te geven in de toepasselijke benoemde Excel-bereiken.</span><span class="sxs-lookup"><span data-stu-id="47c65-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="47c65-149">Als een deel van de groep **Tekst** wordt gebruikt om waarden in te voeren, wordt de waarde in een Excel-bereik ingevoerd als tekstwaarde.</span><span class="sxs-lookup"><span data-stu-id="47c65-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="47c65-150">Gebruik dit patroon om ingevoerde waarden op te maken op basis van de landinstelling die in de toepassing is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="47c65-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="47c65-151">Als het onderdeel **Cel** van de groep **Excel** wordt gebruikt om waarden in te voeren, wordt de waarde in een Excel-bereik ingevoerd als een waarde van het gegevens type dat wordt gedefinieerd door de binding van dat onderdeel **Cel** (bijvoorbeeld **Tekenreeks**, **Werkelijk** of **Geheel getal**).</span><span class="sxs-lookup"><span data-stu-id="47c65-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="47c65-152">Gebruik dit patroon om de ingevoerde waarden in de Excel-toepassing op te maken op basis van de landinstelling van de lokale computer waarop het uitgaande document wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="47c65-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="47c65-153">Op het tabblad **Toewijzing** van de ER Operations-ontwerper kunt u de eigenschap **Ingeschakeld** voor een onderdeel **Bereik** configureren om op te geven of het onderdeel in een gegenereerd document moet worden geplaatst:</span><span class="sxs-lookup"><span data-stu-id="47c65-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="47c65-154">Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Waar** te retourneren tijdens runtime, of als er helemaal geen expressie is geconfigureerd, wordt het betreffende bereik in het gegenereerde document ingevuld.</span><span class="sxs-lookup"><span data-stu-id="47c65-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="47c65-155">Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Onwaar** te retourneren tijdens runtime en als dit bereik niet alle rijen of kolommen vertegenwoordigt, wordt het betreffende bereik niet in het gegenereerde document ingevuld.</span><span class="sxs-lookup"><span data-stu-id="47c65-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="47c65-156">Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Onwaar** te retourneren tijdens runtime en als dit bereik alle rijen of kolommen vertegenwoordigt, bevat het gegenereerde document die rijen en kolommen als verborgen rijen en kolommen.</span><span class="sxs-lookup"><span data-stu-id="47c65-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="47c65-157">Het onderdeel Cel</span><span class="sxs-lookup"><span data-stu-id="47c65-157">Cell component</span></span>

<span data-ttu-id="47c65-158">Het onderdeel **Cel** wordt gebruikt om benoemde cellen, vormen en figuren in Excel in te vullen.</span><span class="sxs-lookup"><span data-stu-id="47c65-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="47c65-159">Als u een benoemd Excel-object wilt aanduiden dat moet worden ingevuld door een ER-onderdeel **Cel**, moet u de naam van dat object opgeven in de eigenschap **Excel-bereik** van het onderdeel **Cel**.</span><span class="sxs-lookup"><span data-stu-id="47c65-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="47c65-160">Op het tabblad **Toewijzing** van de ER Operations-ontwerper kunt u de eigenschap **Ingeschakeld** voor een onderdeel **Cel** configureren om op te geven of het object in een gegenereerd document moet worden ingevuld:</span><span class="sxs-lookup"><span data-stu-id="47c65-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="47c65-161">Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Waar** te retourneren tijdens runtime, of als er helemaal geen expressie is geconfigureerd, wordt het betreffende object in het gegenereerde document ingevuld.</span><span class="sxs-lookup"><span data-stu-id="47c65-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="47c65-162">De binding van dit onderdeel **Cel** geeft een waarde aan die in het betreffende object wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="47c65-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="47c65-163">Als een expressie van de eigenschap **Ingeschakeld** is ingesteld om **Onwaar** te retourneren tijdens runtime, wordt het betreffende object niet ingevuld in het gegenereerde document.</span><span class="sxs-lookup"><span data-stu-id="47c65-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="47c65-164">Wanneer een onderdeel **Cel** is geconfigureerd om een waarde in een cel in te voeren, kan deze worden gekoppeld aan een gegevensbron waarmee de waarde van een primitief gegevenstype wordt geretourneerd (bijvoorbeeld **Tekenreeks**, **Werkelijk** of **Geheel getal**).</span><span class="sxs-lookup"><span data-stu-id="47c65-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="47c65-165">In dit geval wordt de waarde in de cel ingevoerd als waarde van hetzelfde gegevenstype.</span><span class="sxs-lookup"><span data-stu-id="47c65-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="47c65-166">Wanneer een onderdeel **Cel** is geconfigureerd om een waarde in een Excel-vorm in te voeren, kan deze worden gekoppeld aan een gegevensbron waarmee een waarde van een primitief gegevenstype wordt geretourneerd (bijvoorbeeld **Tekenreeks**, **Werkelijk** of **Geheel getal**).</span><span class="sxs-lookup"><span data-stu-id="47c65-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="47c65-167">In dit geval wordt de waarde in de Excel-vorm ingevoerd als de tekst van die vorm.</span><span class="sxs-lookup"><span data-stu-id="47c65-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="47c65-168">Voor waarden van andere gegevenstypen dan **Tekenreeks** wordt de conversie naar tekst automatisch uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="47c65-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="47c65-169">U kunt een onderdeel **Cel** zo configureren dat alleen een vorm wordt ingevuld wanneer een eigenschap voor vormtekst wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="47c65-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="47c65-170">Wanneer een onderdeel **Cel** is geconfigureerd om een waarde in een Excel-afbeelding cel in te voeren, kan deze worden gekoppeld aan een gegevensbron waarmee een waarde van het gegevenstype **Container** wordt geretourneerd die staat voor een afbeelding in binaire indeling.</span><span class="sxs-lookup"><span data-stu-id="47c65-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="47c65-171">In dit geval wordt de waarde in de Excel-afbeelding als een afbeelding ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="47c65-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="47c65-172">Elke Excel-afbeelding en -vorm wordt als verankerd aan de linkerbovenhoek van een bepaalde Excel-cel of een bepaald bereik beschouwd.</span><span class="sxs-lookup"><span data-stu-id="47c65-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="47c65-173">Als u een Excel-afbeelding of -vorm wilt repliceren, moet u de cel of het bereik waaraan deze is verankerd, configureren als een gerepliceerde cel of een gerepliceerd bereik.</span><span class="sxs-lookup"><span data-stu-id="47c65-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="47c65-174">Zie [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md) voor meer informatie over het insluiten van afbeeldingen en vormen.</span><span class="sxs-lookup"><span data-stu-id="47c65-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="47c65-175">Het onderdeel Pagina-einde</span><span class="sxs-lookup"><span data-stu-id="47c65-175">Page break component</span></span>

<span data-ttu-id="47c65-176">Het onderdeel **Pagina-einde** zorgt ervoor dat er een nieuwe pagina wordt gestart in Excel.</span><span class="sxs-lookup"><span data-stu-id="47c65-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="47c65-177">Dit onderdeel is niet vereist als u de standaardpaginering van Excel wilt gebruiken, maar u moet deze functie gebruiken wanneer u wilt dat Excel uw ER-indeling volgt om de paginering te structureren.</span><span class="sxs-lookup"><span data-stu-id="47c65-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="47c65-178">Een toegevoegde ER-indeling bewerken</span><span class="sxs-lookup"><span data-stu-id="47c65-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="47c65-179">Een sjabloon bewerken</span><span class="sxs-lookup"><span data-stu-id="47c65-179">Update a template</span></span>

<span data-ttu-id="47c65-180">U kunt **Bijwerken vanuit Excel** selecteren op het tabblad **Importeren** van het actievenster om een bijgewerkte sjabloon te importeren in een bewerkbare ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="47c65-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="47c65-181">Tijdens dit proces wordt een sjabloon van het geselecteerde onderdeel **Excel\\Bestand** vervangen door een nieuwe sjabloon.</span><span class="sxs-lookup"><span data-stu-id="47c65-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="47c65-182">De inhoud van de bewerkbare ER-indeling wordt gesynchroniseerd met de inhoud van de bijgewerkte ER-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="47c65-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="47c65-183">Er wordt automatisch een nieuw ER-indelingsonderdeel gemaakt voor elke Excel-naam als het ER-indelingsonderdeel niet wordt gevonden in de bewerkbare indeling.</span><span class="sxs-lookup"><span data-stu-id="47c65-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="47c65-184">Elk ER-indelingsonderdeel wordt verwijderd uit de bewerkbare ER-indeling als de geschikte Excel-naam niet wordt gevonden.</span><span class="sxs-lookup"><span data-stu-id="47c65-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="47c65-185">Als u het optionele element **Werkblad** wilt maken in de bewerkbare ER-indeling, stelt u de optie **Indelingselement Excel-werkblad maken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="47c65-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="47c65-186">Als de bewerkbare ER-indeling oorspronkelijk elementen van het type **Werkblad** bevatte, wordt u aangeraden de optie **Indelingselement Excel-werkblad maken** op **Ja** in te stellen wanneer u een bijgewerkte sjabloon importeert.</span><span class="sxs-lookup"><span data-stu-id="47c65-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="47c65-187">Anders worden alle geneste elementen van het oorspronkelijke element **Werkblad** helemaal opnieuw gemaakt.</span><span class="sxs-lookup"><span data-stu-id="47c65-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="47c65-188">Alle bindingen van de opnieuw gemaakte indelingselementen gaan in dat geval verloren in de bijgewerkte ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="47c65-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![De optie Indelingselement Excel-werkblad maken in het dialoogvenster Bijwerken vanuit Excel](./media/er-excel-format-update-template.png)

<span data-ttu-id="47c65-190">Volg de stappen in de [Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen](modify-electronic-reporting-format-reapply-excel-template.md) voor meer informatie over deze functie.</span><span class="sxs-lookup"><span data-stu-id="47c65-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="47c65-191">Een ER-indeling valideren</span><span class="sxs-lookup"><span data-stu-id="47c65-191">Validate an ER format</span></span>

<span data-ttu-id="47c65-192">Wanneer u een ER-indeling valideert die kan worden bewerkt, wordt een consistentiecontrole uitgevoerd om er zeker van te zijn dat de Excel-naam aanwezig is in de Excel-sjabloon die momenteel wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="47c65-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="47c65-193">U wordt op de hoogte gebracht van eventuele inconsistenties.</span><span class="sxs-lookup"><span data-stu-id="47c65-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="47c65-194">Voor sommige inconsistenties wordt de optie voor het automatisch oplossen van problemen aangeboden.</span><span class="sxs-lookup"><span data-stu-id="47c65-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Foutbericht over validatie](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="47c65-196">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="47c65-196">Additional resources</span></span>

[<span data-ttu-id="47c65-197">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="47c65-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="47c65-198">Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling</span><span class="sxs-lookup"><span data-stu-id="47c65-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="47c65-199">Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen</span><span class="sxs-lookup"><span data-stu-id="47c65-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="47c65-200">Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen</span><span class="sxs-lookup"><span data-stu-id="47c65-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="47c65-201">Afbeeldingen en vormen insluiten in documenten die u genereert met ER</span><span class="sxs-lookup"><span data-stu-id="47c65-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="47c65-202">Elektronische rapportage (ER) configureren om gegevens op te halen in Power BI</span><span class="sxs-lookup"><span data-stu-id="47c65-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)