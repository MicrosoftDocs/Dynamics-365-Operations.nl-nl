---
title: Gegevensvelden in de belastingintegratie toevoegen met extensies
description: In dit onderwerp wordt uitgelegd hoe u X++-extensies gebruikt om gegevensvelden toe te voegen in de belastingintegratie.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8e3573f9c9971d4a5af33ece08b7e0b43f2e813a
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921160"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="21ef1-103">Gegevensvelden in de belastingintegratie toevoegen met extensies</span><span class="sxs-lookup"><span data-stu-id="21ef1-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="21ef1-104">In dit onderwerp wordt uitgelegd hoe u X++-extensies gebruikt om gegevensvelden toe te voegen in de belastingintegratie.</span><span class="sxs-lookup"><span data-stu-id="21ef1-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="21ef1-105">Deze velden kunnen worden uitgebreid tot het belastinggegevensmodel van de belastingservice en worden gebruikt om belastingcodes te bepalen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="21ef1-106">Zie [Gegevensvelden toevoegen in belastingconfiguraties](tax-service-add-data-fields-tax-configurations.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="21ef1-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="21ef1-107">Gegevensmodel</span><span class="sxs-lookup"><span data-stu-id="21ef1-107">Data model</span></span>

<span data-ttu-id="21ef1-108">De gegevens in het gegevensmodel worden vervoerd door objecten en geïmplementeerd door klassen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="21ef1-109">Hieronder volgt een overzicht van de belangrijke objecten:</span><span class="sxs-lookup"><span data-stu-id="21ef1-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="21ef1-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="21ef1-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="21ef1-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="21ef1-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="21ef1-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="21ef1-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="21ef1-113">In de volgende afbeelding ziet u de relaties tussen deze objecten.</span><span class="sxs-lookup"><span data-stu-id="21ef1-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="21ef1-114">[![Relatie van gegevensobjectmodel](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="21ef1-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="21ef1-115">Een object **Document** kan veel objecten van het type **Line** bevatten.</span><span class="sxs-lookup"><span data-stu-id="21ef1-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="21ef1-116">Elk object bevat metagegevens voor de belastingservice.</span><span class="sxs-lookup"><span data-stu-id="21ef1-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="21ef1-117">`TaxIntegrationDocumentObject` bevat `originAddress`-metagegevens, met informatie over het bronadres, en `includingTax`-metagegevens, waarmee wordt aangegeven of het regelbedrag btw bevat.</span><span class="sxs-lookup"><span data-stu-id="21ef1-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="21ef1-118">`TaxIntegrationLineObject` bevat `itemId`-, `quantity`- en `categoryId`-metagegevens.</span><span class="sxs-lookup"><span data-stu-id="21ef1-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="21ef1-119">`TaxIntegrationLineObject` implementeert ook **Charge**-objecten.</span><span class="sxs-lookup"><span data-stu-id="21ef1-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="21ef1-120">Integratiestroom</span><span class="sxs-lookup"><span data-stu-id="21ef1-120">Integration flow</span></span>

<span data-ttu-id="21ef1-121">De gegevens in de stroom worden gemanipuleerd door activiteiten.</span><span class="sxs-lookup"><span data-stu-id="21ef1-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="21ef1-122">Sleutelactiviteiten</span><span class="sxs-lookup"><span data-stu-id="21ef1-122">Key activities</span></span>

* <span data-ttu-id="21ef1-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="21ef1-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="21ef1-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="21ef1-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="21ef1-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="21ef1-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="21ef1-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="21ef1-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="21ef1-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="21ef1-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="21ef1-128">Activiteiten worden uitgevoerd in de volgende volgorde:</span><span class="sxs-lookup"><span data-stu-id="21ef1-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="21ef1-129">SettingRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-129">Setting Retrieval</span></span>
2. <span data-ttu-id="21ef1-130">DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-130">Data Retrieval</span></span>
3. <span data-ttu-id="21ef1-131">Calculation</span><span class="sxs-lookup"><span data-stu-id="21ef1-131">Calculation Service</span></span>
4. <span data-ttu-id="21ef1-132">CurrencyExchange</span><span class="sxs-lookup"><span data-stu-id="21ef1-132">Currency Exchange</span></span>
5. <span data-ttu-id="21ef1-133">DataPersistence</span><span class="sxs-lookup"><span data-stu-id="21ef1-133">Data Persistence</span></span>

<span data-ttu-id="21ef1-134">Breid **DataRetrieval** bijvoorbeeld eerder uit dan **Calculation**.</span><span class="sxs-lookup"><span data-stu-id="21ef1-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="21ef1-135">DataRetrieval-activiteiten</span><span class="sxs-lookup"><span data-stu-id="21ef1-135">Data Retrieval activities</span></span>

<span data-ttu-id="21ef1-136">Met **DataRetrieval**-activiteiten worden gegevens opgehaald uit de database.</span><span class="sxs-lookup"><span data-stu-id="21ef1-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="21ef1-137">Er zijn adapters voor verschillende transacties beschikbaar om gegevens uit verschillende transactietabellen op te halen:</span><span class="sxs-lookup"><span data-stu-id="21ef1-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="21ef1-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="21ef1-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="21ef1-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="21ef1-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="21ef1-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="21ef1-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="21ef1-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="21ef1-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="21ef1-145">In deze **DataRetrieval**-activiteiten worden gegevens van de database naar `TaxIntegrationDocumentObject` en `TaxIntegrationLineObject` gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="21ef1-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="21ef1-146">Omdat al deze activiteiten dezelfde abstracte sjabloonklasse uitbreiden, hebben ze gemeenschappelijke methoden.</span><span class="sxs-lookup"><span data-stu-id="21ef1-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="21ef1-147">Calculation-activiteiten</span><span class="sxs-lookup"><span data-stu-id="21ef1-147">Calculation Service activities</span></span>

<span data-ttu-id="21ef1-148">De **Calculation**-activiteit is de koppeling tussen de belastingservice en de belastingintegratie.</span><span class="sxs-lookup"><span data-stu-id="21ef1-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="21ef1-149">Deze activiteit is verantwoordelijk voor de volgende functies:</span><span class="sxs-lookup"><span data-stu-id="21ef1-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="21ef1-150">De aanvraag maken.</span><span class="sxs-lookup"><span data-stu-id="21ef1-150">Construct the request.</span></span>
2. <span data-ttu-id="21ef1-151">De aanvraag naar de belastingservice boeken.</span><span class="sxs-lookup"><span data-stu-id="21ef1-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="21ef1-152">Het antwoord van de belastingservice ontvangen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="21ef1-153">Het antwoord parseren.</span><span class="sxs-lookup"><span data-stu-id="21ef1-153">Parse the response.</span></span>

<span data-ttu-id="21ef1-154">Een gegevensveld dat u aan de aanvraag toevoegt, wordt samen met andere metagegevens geboekt.</span><span class="sxs-lookup"><span data-stu-id="21ef1-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="21ef1-155">Extensie-implementatie</span><span class="sxs-lookup"><span data-stu-id="21ef1-155">Extension implementation</span></span>

<span data-ttu-id="21ef1-156">In deze sectie vindt u gedetailleerde stappen waarin wordt uitgelegd hoe u de extensie implementeert.</span><span class="sxs-lookup"><span data-stu-id="21ef1-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="21ef1-157">De financiële dimensies **Kostenplaats** en **Project** worden als voorbeelden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="21ef1-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="21ef1-158">Stap 1.</span><span class="sxs-lookup"><span data-stu-id="21ef1-158">Step 1.</span></span> <span data-ttu-id="21ef1-159">De gegevensvariabele toevoegen in de objectklasse</span><span class="sxs-lookup"><span data-stu-id="21ef1-159">Add the data variable in the object class</span></span>

<span data-ttu-id="21ef1-160">De objectklasse bevat de gegevensvariabele en getter/setter-methoden voor de gegevens.</span><span class="sxs-lookup"><span data-stu-id="21ef1-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="21ef1-161">Voeg het gegevensveld toe aan `TaxIntegrationDocumentObject` of `TaxIntegrationLineObject`, afhankelijk van het niveau van het veld.</span><span class="sxs-lookup"><span data-stu-id="21ef1-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="21ef1-162">In het volgende voorbeeld wordt het regelniveau gebruikt en de bestandsnaam is `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="21ef1-163">Als het gegevensveld dat u toevoegt zich op documentniveau bevindt, wijzigt u de bestandsnaam in `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="21ef1-164">**Kostenplaats** en **Project** worden toegevoegd als privévariabelen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="21ef1-165">Maak getter- en settermethoden voor deze gegevensvelden om de gegevens te bewerken.</span><span class="sxs-lookup"><span data-stu-id="21ef1-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="21ef1-166">Stap 2.</span><span class="sxs-lookup"><span data-stu-id="21ef1-166">Step 2.</span></span> <span data-ttu-id="21ef1-167">Gegevens uit de database ophalen</span><span class="sxs-lookup"><span data-stu-id="21ef1-167">Retrieve data from the database</span></span>

<span data-ttu-id="21ef1-168">Geef de transactie op en breid de juiste adapterklassen uit om de gegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="21ef1-169">Voor een transactie **Inkooporder** moet u bijvoorbeeld `TaxIntegrationPurchTableDataRetrieval` en `TaxIntegrationVendInvoiceInfoTableDataRetrieval` uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="21ef1-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="21ef1-170">`TaxIntegrationPurchParmTableDataRetrieval` wordt overgenomen van `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="21ef1-171">Wijzig dit alleen als de logica van de tabellen `purchTable` en `purchParmTable` verschilt.</span><span class="sxs-lookup"><span data-stu-id="21ef1-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="21ef1-172">Als het gegevensveld voor alle transacties moet worden toegevoegd, breidt u alle `DataRetrieval`-klassen uit.</span><span class="sxs-lookup"><span data-stu-id="21ef1-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="21ef1-173">Omdat alle **DataRetrieval**-activiteiten dezelfde sjabloonklasse uitbreiden, zijn de klassestructuren, variabelen en methoden vergelijkbaar.</span><span class="sxs-lookup"><span data-stu-id="21ef1-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="21ef1-174">In het volgende voorbeeld ziet u de basisstructuur wanneer de `PurchTable`-tabel wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="21ef1-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="21ef1-175">Wanneer de `CopyToDocument`-methode wordt aangeroepen, bestaat de `this.purchTable`-buffer al.</span><span class="sxs-lookup"><span data-stu-id="21ef1-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="21ef1-176">Het doel van deze methode is om alle vereiste gegevens van `this.purchTable` naar het `document`-object te kopiëren met de setter-methode die in de `DocumentObject`-klasse is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="21ef1-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="21ef1-177">Evenzo bestaat er al een `this.purchLine`-buffer in de `CopyToLine`-methode.</span><span class="sxs-lookup"><span data-stu-id="21ef1-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="21ef1-178">Het doel van deze methode is om alle vereiste gegevens van `this.purchLine` naar het `_line`-object te kopiëren met de setter-methode die in de `LineObject`-klasse is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="21ef1-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="21ef1-179">De meest directe aanpak is om de `CopyToDocument`- en `CopyToLine`-methoden uit te breiden.</span><span class="sxs-lookup"><span data-stu-id="21ef1-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="21ef1-180">We raden u echter aan om eerst de `copyToDocumentFromHeaderTable`- en `copyToLineFromLineTable`-methoden uit te proberen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="21ef1-181">Als deze niet werken zoals u wilt, implementeert u uw eigen methode en roept u deze aan in `CopyToDocument` en `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="21ef1-182">Er zijn drie veelvoorkomende situaties waarin u deze aanpak kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="21ef1-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="21ef1-183">Het vereiste veld bevindt zich in `PurchTable` of `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="21ef1-184">In dit geval kunt u `copyToDocumentFromHeaderTable` en `copyToLineFromLineTable` uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="21ef1-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="21ef1-185">Hier is de voorbeeldcode.</span><span class="sxs-lookup"><span data-stu-id="21ef1-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="21ef1-186">De vereiste gegevens bevinden zich niet in de standaardtabel van de transactie.</span><span class="sxs-lookup"><span data-stu-id="21ef1-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="21ef1-187">Er zijn echter enkele join-relaties met de standaardtabel en het veld is vereist voor de meeste regels.</span><span class="sxs-lookup"><span data-stu-id="21ef1-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="21ef1-188">In dit geval vervangt u `getDocumentQueryObject` of `getLineObject` om een query op basis van de join-relatie uit te voeren op de tabel.</span><span class="sxs-lookup"><span data-stu-id="21ef1-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="21ef1-189">In het volgende voorbeeld is het veld **Nu leveren** geïntegreerd met de verkooporder op het regelniveau.</span><span class="sxs-lookup"><span data-stu-id="21ef1-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="21ef1-190">In dit voorbeeld wordt een `mcrSalesLineDropShipment`-buffer gedeclareerd en wordt de query gedefinieerd in `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="21ef1-191">De query gebruikt de relatie `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="21ef1-192">Terwijl u in deze situatie uitbreidt, kunt u `getLineQueryObject` vervangen door uw eigen geconstrueerde queryobject.</span><span class="sxs-lookup"><span data-stu-id="21ef1-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="21ef1-193">Houd echter rekening met het volgende:</span><span class="sxs-lookup"><span data-stu-id="21ef1-193">However, note the following points:</span></span>

    * <span data-ttu-id="21ef1-194">Omdat de retourwaarde van de `getLineQueryObject`-methode `SysDaQueryObject` is, moet u dit object construeren met de SysDa-benadering.</span><span class="sxs-lookup"><span data-stu-id="21ef1-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="21ef1-195">Kan bestaande tabel niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-195">Can't remove existed table.</span></span>

- <span data-ttu-id="21ef1-196">De vereiste gegevens zijn op basis van een gecompliceerde join-relatie aan de transactietabel gekoppeld of de relatie is niet één-op-één (1:1), maar één-op-veel (1:N).</span><span class="sxs-lookup"><span data-stu-id="21ef1-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="21ef1-197">In deze situatie wordt het een beetje ingewikkeld.</span><span class="sxs-lookup"><span data-stu-id="21ef1-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="21ef1-198">Deze situatie is van toepassing op het voorbeeld van financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="21ef1-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="21ef1-199">In dit geval kunt u uw eigen methode implementeren om de gegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="21ef1-200">Hier is de voorbeeldcode in het `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-bestand.</span><span class="sxs-lookup"><span data-stu-id="21ef1-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="21ef1-201">Stap 3.</span><span class="sxs-lookup"><span data-stu-id="21ef1-201">Step 3.</span></span> <span data-ttu-id="21ef1-202">Gegevens aan de aanvraag toevoegen</span><span class="sxs-lookup"><span data-stu-id="21ef1-202">Add data to the request</span></span>

<span data-ttu-id="21ef1-203">Breid de `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject`- of `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-methode uit om gegevens aan de aanvraag toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="21ef1-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="21ef1-204">Hier is de voorbeeldcode in het `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-bestand.</span><span class="sxs-lookup"><span data-stu-id="21ef1-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="21ef1-205">In deze code is `_destination` het wrapper-object dat wordt gebruikt om de boekingsaanvraag te genereren en is `_source` het `TaxIntegrationLineObject`-object.</span><span class="sxs-lookup"><span data-stu-id="21ef1-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="21ef1-206">Definieer de sleutel die in het aanvraagformulier wordt gebruikt als `private const str`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="21ef1-207">Stel het veld in de `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-methode in met de `SetField`-methode.</span><span class="sxs-lookup"><span data-stu-id="21ef1-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="21ef1-208">Het gegevenstype van de tweede parameter moet `string` zijn.</span><span class="sxs-lookup"><span data-stu-id="21ef1-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="21ef1-209">Als het gegevenstype niet `string` is, converteert u het naar `string`.</span><span class="sxs-lookup"><span data-stu-id="21ef1-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="21ef1-210">Bijlage</span><span class="sxs-lookup"><span data-stu-id="21ef1-210">Appendix</span></span>

<span data-ttu-id="21ef1-211">In deze bijlage ziet u de volledige voorbeeldcode voor de integratie van financiële dimensies (**Kostenplaats** en **Project**) op regelniveau.</span><span class="sxs-lookup"><span data-stu-id="21ef1-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="21ef1-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="21ef1-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="21ef1-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="21ef1-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="21ef1-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="21ef1-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
