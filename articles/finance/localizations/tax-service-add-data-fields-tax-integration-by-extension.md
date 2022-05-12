---
title: Gegevensvelden in de belastingintegratie toevoegen met extensies
description: In dit onderwerp wordt uitgelegd hoe u X++-extensies gebruikt om gegevensvelden toe te voegen in de belastingintegratie.
author: qire
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 79b51812eac354072ebf2a0ef6fe8d39610c6385
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649096"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Gegevensvelden in de belastingintegratie toevoegen met extensies

[!include [banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u X++-extensies gebruikt om gegevensvelden toe te voegen in de belastingintegratie. Deze velden kunnen worden uitgebreid tot het belastinggegevensmodel van de belastingservice en worden gebruikt om belastingcodes te bepalen. Zie [Gegevensvelden toevoegen in belastingconfiguraties](tax-service-add-data-fields-tax-configurations.md) voor meer informatie.

## <a name="data-model"></a>Gegevensmodel

De gegevens in het gegevensmodel worden vervoerd door objecten en geïmplementeerd door klassen.

Hieronder volgt een overzicht van de belangrijke objecten:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

In de volgende afbeelding ziet u de relaties tussen deze objecten.

[![Relatie van gegevensobjectmodel.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Een object **Document** kan veel objecten van het type **Line** bevatten. Elk object bevat metagegevens voor de belastingservice.

- `TaxIntegrationDocumentObject` bevat `originAddress`-metagegevens, met informatie over het bronadres, en `includingTax`-metagegevens, waarmee wordt aangegeven of het regelbedrag btw bevat.
- `TaxIntegrationLineObject` bevat `itemId`-, `quantity`- en `categoryId`-metagegevens.

> [!NOTE]
> `TaxIntegrationLineObject` implementeert ook **Charge**-objecten.

## <a name="integration-flow"></a>Integratiestroom

De gegevens in de stroom worden gemanipuleerd door activiteiten.

### <a name="key-activities"></a>Sleutelactiviteiten

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Activiteiten worden uitgevoerd in de volgende volgorde:

1. SettingRetrieval
2. DataRetrieval
3. Calculation
4. CurrencyExchange
5. DataPersistence

Breid **DataRetrieval** bijvoorbeeld eerder uit dan **Calculation**.

#### <a name="data-retrieval-activities"></a>DataRetrieval-activiteiten

Met **DataRetrieval**-activiteiten worden gegevens opgehaald uit de database. Er zijn adapters voor verschillende transacties beschikbaar om gegevens uit verschillende transactietabellen op te halen:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

In deze **DataRetrieval**-activiteiten worden gegevens van de database naar `TaxIntegrationDocumentObject` en `TaxIntegrationLineObject` gekopieerd. Omdat al deze activiteiten dezelfde abstracte sjabloonklasse uitbreiden, hebben ze gemeenschappelijke methoden.

#### <a name="calculation-service-activities"></a>Calculation-activiteiten

De **Calculation**-activiteit is de koppeling tussen de belastingservice en de belastingintegratie. Deze activiteit is verantwoordelijk voor de volgende functies:

1. De aanvraag maken.
2. De aanvraag naar de belastingservice boeken.
3. Het antwoord van de belastingservice ontvangen.
4. Het antwoord parseren.

Een gegevensveld dat u aan de aanvraag toevoegt, wordt samen met andere metagegevens geboekt. 

## <a name="extension-implementation"></a>Extensie-implementatie

In deze sectie vindt u gedetailleerde stappen waarin wordt uitgelegd hoe u de extensie implementeert. De financiële dimensies **Kostenplaats** en **Project** worden als voorbeelden gebruikt.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>Stap 1. De gegevensvariabele toevoegen in de objectklasse

De objectklasse bevat de gegevensvariabele en getter/setter-methoden voor de gegevens. Voeg het gegevensveld toe aan `TaxIntegrationDocumentObject` of `TaxIntegrationLineObject`, afhankelijk van het niveau van het veld. In het volgende voorbeeld wordt het regelniveau gebruikt en de bestandsnaam is `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Als het gegevensveld dat u toevoegt zich op documentniveau bevindt, wijzigt u de bestandsnaam in `TaxIntegrationDocumentObject_Extension.xpp`.

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

**Kostenplaats** en **Project** worden toegevoegd als privévariabelen. Maak getter- en settermethoden voor deze gegevensvelden om de gegevens te bewerken.

### <a name="step-2-retrieve-data-from-the-database"></a>Stap 2. Gegevens uit de database ophalen

Geef de transactie op en breid de juiste adapterklassen uit om de gegevens op te halen. Voor een transactie **Inkooporder** moet u bijvoorbeeld `TaxIntegrationPurchTableDataRetrieval` en `TaxIntegrationVendInvoiceInfoTableDataRetrieval` uitbreiden. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` wordt overgenomen van `TaxIntegrationPurchTableDataRetrieval`. Wijzig dit alleen als de logica van de tabellen `purchTable` en `purchParmTable` verschilt.

Als het gegevensveld voor alle transacties moet worden toegevoegd, breidt u alle `DataRetrieval`-klassen uit.

Omdat alle **DataRetrieval**-activiteiten dezelfde sjabloonklasse uitbreiden, zijn de klassestructuren, variabelen en methoden vergelijkbaar.

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

In het volgende voorbeeld ziet u de basisstructuur wanneer de `PurchTable`-tabel wordt gebruikt.

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

Wanneer de `CopyToDocument`-methode wordt aangeroepen, bestaat de `this.purchTable`-buffer al. Het doel van deze methode is om alle vereiste gegevens van `this.purchTable` naar het `document`-object te kopiëren met de setter-methode die in de `DocumentObject`-klasse is gemaakt.

Evenzo bestaat er al een `this.purchLine`-buffer in de `CopyToLine`-methode. Het doel van deze methode is om alle vereiste gegevens van `this.purchLine` naar het `_line`-object te kopiëren met de setter-methode die in de `LineObject`-klasse is gemaakt.

De meest directe aanpak is om de `CopyToDocument`- en `CopyToLine`-methoden uit te breiden. We raden u echter aan om eerst de `copyToDocumentFromHeaderTable`- en `copyToLineFromLineTable`-methoden uit te proberen. Als deze niet werken zoals u wilt, implementeert u uw eigen methode en roept u deze aan in `CopyToDocument` en `CopyToLine`. Er zijn drie veelvoorkomende situaties waarin u deze aanpak kunt gebruiken:

- Het vereiste veld bevindt zich in `PurchTable` of `PurchLine`. In dit geval kunt u `copyToDocumentFromHeaderTable` en `copyToLineFromLineTable` uitbreiden. Hier is de voorbeeldcode.

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

- De vereiste gegevens bevinden zich niet in de standaardtabel van de transactie. Er zijn echter enkele join-relaties met de standaardtabel en het veld is vereist voor de meeste regels. In dit geval vervangt u `getDocumentQueryObject` of `getLineObject` om een query op basis van de join-relatie uit te voeren op de tabel. In het volgende voorbeeld is het veld **Nu leveren** geïntegreerd met de verkooporder op het regelniveau.

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

    In dit voorbeeld wordt een `mcrSalesLineDropShipment`-buffer gedeclareerd en wordt de query gedefinieerd in `getLineQueryObject`. De query gebruikt de relatie `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Terwijl u in deze situatie uitbreidt, kunt u `getLineQueryObject` vervangen door uw eigen geconstrueerde queryobject. Houd echter rekening met het volgende:

    * Omdat de retourwaarde van de `getLineQueryObject`-methode `SysDaQueryObject` is, moet u dit object construeren met de SysDa-benadering.
    * Kan bestaande tabel niet verwijderen.

- De vereiste gegevens zijn op basis van een gecompliceerde join-relatie aan de transactietabel gekoppeld of de relatie is niet één-op-één (1:1), maar één-op-veel (1:N). In deze situatie wordt het een beetje ingewikkeld. Deze situatie is van toepassing op het voorbeeld van financiële dimensies. 

    In dit geval kunt u uw eigen methode implementeren om de gegevens op te halen. Hier is de voorbeeldcode in het `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-bestand.

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

### <a name="step-3-add-data-to-the-request"></a>Stap 3. Gegevens aan de aanvraag toevoegen

Breid de `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject`- of `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-methode uit om gegevens aan de aanvraag toe te voegen. Hier is de voorbeeldcode in het `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-bestand.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';
    // private const str IOEnumExample = 'Enum Example';

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

        // If the field to be extended is an enum type, use enum2Symbol to convert an enum variable exampleEnum of ExampleEnumType to a string
        // _destination.SetField(IOEnumExample, enum2Symbol(enumNum(ExampleEnumType), _source.getExampleEnum()));
    }
}
```

In deze code is `_destination` het wrapper-object dat wordt gebruikt om de aanvraag te genereren en is `_source` het `TaxIntegrationLineObject`-object.

> [!NOTE]
> Definieer de veldnaam die in de aanvraag wordt gebruikt als **private const str**. De tekenreeks moet exact gelijk zijn aan de knooppuntnaam (niet het label) die is toegevoegd in het onderwerp [Gegevensvelden toevoegen in belastingconfiguraties](tax-service-add-data-fields-tax-configurations.md).
> 
> Stel het veld in de methode **copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine** in op basis van de methode **SetField**. Het gegevenstype van de tweede parameter moet **string** zijn. Als het gegevenstype niet **string** is, converteert u het naar een tekenreeks.
> Als het gegevenstype X++ **enumtype** is, raden we u aan om de methode **enum2Symbol** te gebruiken om de enumwaarde naar een tekenreeks te converteren. De opsommingswaarde die in de belastingconfiguratie is toegevoegd, moet exact gelijk zijn aan opsommingsnaam. Hieronder volgt een lijst met verschillen tussen de opsommingswaarde, het label en de naam.
> 
>   - De naam van de opsomming is een symbolische naam in code. **enum2Symbol()** kan de opsommingswaarde converteren naar de naam.
>   - De waarde van de opsomming is een geheel getal.
>   - Het label van de opsomming kan in verschillende voorkeurstalen verschillend zijn. **enum2Str()** kan de opsommingswaarde converteren naar het label.

## <a name="model-dependency"></a>Modelafhankelijkheid

Om het project te bouwen, voegt u de volgende referentiemodellen toe aan de modelafhankelijkheden:

- ApplicationPlatform
- ApplicationSuite
- Belastingengine
- Dimensies, als financiële dimensies worden gebruikt
- Andere vereiste modellen waarnaar in de code wordt verwezen

## <a name="validation"></a>Validatie

Nadat u de vorige stappen hebt voltooid, kunt u de wijzigingen valideren.

1. Ga in Finance naar **Leveranciers** en voeg **&debug=vs%2CconfirmExit&** toe aan de URL. Bijvoorbeeld https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&. De laatste **&** is essentieel.
2. Open de pagina **Inkooporder** en selecteer **Nieuw** om een inkooporder te maken.
3. Stel de waarde voor het aangepaste veld in en selecteer vervolgens **Btw**. Een probleemoplossingsbestand met het voorvoegsel **TaxServiceTroubleshootingLog** wordt automatisch gedownload. Dit bestand bevat de transactiegegevens die zijn geboekt naar de btw-berekeningsservice. 
4. Controleer of het toegevoegde aangepaste veld aanwezig is in de sectie **JSON voor invoer voor berekening van btw-service** en of de waarde juist is. Als de waarde niet correct is, controleert u de stappen in dit document nogmaals.

Voorbeeld van bestand:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>Bijlage

In deze bijlage ziet u de volledige voorbeeldcode voor de integratie van de financiële dimensies (**Kostenplaats** en **Project**) op regelniveau.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
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
