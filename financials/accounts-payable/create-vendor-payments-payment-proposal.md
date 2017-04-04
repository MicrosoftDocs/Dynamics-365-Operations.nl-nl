---
title: Leverancierbetalingen maken met behulp van een betalingsvoorstel
description: Dit onderwerp geeft een overzicht van de opties voor betalingsvoorstel en bevat enkele voorbeelden die tonen hoe betalingsvoorstellen werken. Betalingsvoorstellen worden vaak gebruikt om leveranciersbetalingen te maken, omdat de query kan worden gebruikt om snel leveranciersfacturen voor betaling te selecteren op basis van criteria zoals vervaldatum en contantkorting.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: b46037b9509f329e18f0da69d530f6b1f88c8888
ms.lasthandoff: 03/31/2017


---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Leverancierbetalingen maken met behulp van een betalingsvoorstel

Dit onderwerp geeft een overzicht van de opties voor betalingsvoorstel en bevat enkele voorbeelden die tonen hoe betalingsvoorstellen werken. Betalingsvoorstellen worden vaak gebruikt om leveranciersbetalingen te maken, omdat de query kan worden gebruikt om snel leveranciersfacturen voor betaling te selecteren op basis van criteria zoals vervaldatum en contantkorting. 

Organisaties gebruiken vaak betalingsvoorstellen om leveranciersbetalingen te maken, omdat de voorstelquery voor klantbetalingen kan worden gebruikt om snel leveranciersfacturen voor betaling te selecteren op basis van de vervaldatum, de contantkorting, en andere criteria. 

De voorstelquery voor klantbetalingen bevat verschillende tabbladen, die elk verschillende opties bevatten om facturen te selecteren voor betaling. De **Parameter** tabblad bevat opties die een meerderheid van de organisatie het meest gebruikt. Op de **Records om op te nemen** sneltabblad kunt u opgeven welke facturen of leveranciers wilt opnemen voor de betaling door te bereiken voor verschillende kenmerken definiëren. Als u een specifieke reeks leveranciers betaalt wilt, kunt u bijvoorbeeld een filter voor het bereik van de leverancier definiëren. Deze functionaliteit wordt vaak gebruikt om facturen voor een specifieke van betalingsmethode te selecteren. Bijvoorbeeld: als u een filter definiëren waar **betalingsmethode** = **controleren op**, alleen facturen met die methode van betaling zijn geselecteerd voor betaling, mits zij voldoen ook aan andere criteria die zijn opgegeven in de query. Het tabblad **Geavanceerde parameters** bevat extra opties, die in sommige situaties mogelijk niet relevant zijn voor uw organisatie. Dit tabblad bevat bijvoorbeeld de opties voor het betalen van facturen voor gecentraliseerde betalingen.

## <a name="parameters"></a>Parameters
-   **Facturen door** – facturen binnen het datumbereik dat is opgegeven door de **vanaf datum** en **einddatum** velden kunnen worden geselecteerd door vervaldatum, contantkortingsdatum of beide. Als u de datum voor contantkorting, wordt eerst gezocht naar facturen met een datum voor contantkorting tussen de begindatum en einddatum. Het systeem bepaalt vervolgens of de factuur in aanmerking komt voor de contantkorting door de sessiedatum te gebruiken als controlemiddel om te bepalen of de datum voor contantkorting nog niet is verstreken.
-   **Begindatum** en** Einddatum** – Facturen die een vervaldatum of datum voor contantkorting hebben binnen dit datumbereik worden geselecteerd voor betaling.
-   **Betalingsdatum** – Als een datum wordt gedefinieerd, worden alle betalingen op deze datum uitgevoerd. Het veld **Datum minimumbetaling** wordt overschreven.
-   **Datum minimumbetaling** – Voer de minimumbetalingsdatum in. Bijvoorbeeld: de **vanaf datum** en **einddatum** velden opgeven in een bereik van 1 September tot 10 September en de datum minimumbetaling is 5 September. In dit geval hebben alle facturen met een vervaldatum van 1 September 5 September een betalingsdatum van 5 September. Alle facturen met een vervaldatum van 5 September tot en met 10 September hebben echter een betalingsdatum die gelijk is aan de vervaldatum van elke factuur.
-   **Grenswaarde van bedrag** – Voer het maximaal totale bedrag voor alle betalingen in.
-   **Betalingen zonder voorbeeld van een factuur maken** : als deze optie is ingesteld op **Ja**, betalingen onmiddellijk gemaakt op de **leveranciersbetalingen** pagina. De **betalingsvoorstel** pagina overgeslagen. Daarom worden betalingen sneller gemaakt. Betalingen kunnen nog steeds worden gewijzigd vanaf de pagina **Leveranciersbetalingen**. U kunt ook teruggaan naar de pagina **Betalingsvoorstel** door op de knop **Facturen bewerken voor geselecteerde betaling** te klikken.

## <a name="advanced-options"></a>Geavanceerde opties
-   **Saldo van leverancier controleren** – Als deze optie is ingesteld op **Ja**, controleert het systeem of een leverancier geen debetsaldo heeft voordat een factuur wordt betaald. Als een leverancier een debetsaldo heeft, wordt er een betaling gemaakt. De leverancier zijn wellicht creditnota's of betalingen die zijn geboekt maar nog niet zijn vereffend. In deze gevallen, mag de leverancier niet worden betaald. In plaats daarvan, moeten de creditnota's of betalingen worden verrekend met de openstaande facturen.
-   **Negatieve betalingen verwijderen** – Deze optie werkt verschillend, afhankelijk van of betalingen worden uitgevoerd voor individuele facturen of voor de som van facturen die aan de betalingscriteria voldoen. Dit gedrag wordt gedefinieerd in de betalingsmethode.
-   **Betaling voor elke factuur** – Als de optie **Negatieve betalingen verwijderen** is ingesteld op **Ja** en er een niet-vereffende factuur en betaling voor een leverancier bestaat, wordt alleen de factuur geselecteerd voor betaling. De bestaande betaling wordt niet verrekend met de factuur. Als de optie **Negatieve betalingen verwijderen** is ingesteld op **Nee** en een factuur en een betaling niet zijn vereffend, worden zowel de factuur als de betaling geselecteerd voor betaling. Er wordt een betaling gemaakt voor de betaling en er wordt een restitutie (negatieve betaling) gemaakt voor de betaling.
-   **Betaling voor som van facturen** – Als de optie **Negatieve betalingen verwijderen** is ingesteld op **Ja** en er een niet-vereffende factuur en betaling bestaat voor een leverancier, worden zowel de niet-vereffende factuur als de betaling geselecteerd voor betaling en worden de bedragen samengevoegd om het totale betalingsbedrag te produceren. De enige uitzondering geldt in situaties waarbij de som resulteert in een restitutie. In dit geval, wordt noch de factuur noch de betaling geselecteerd. Als de ** negatieve betalingen verwijderen ** optie is ingesteld op **Nee**, en een factuur en een betaling niet zijn vereffend, zowel de factuur en de betaling zijn geselecteerd voor betaling en de bedragen worden toegevoegd samen tot het totale verschuldigde bedrag.
-   **Alleen rapport afdrukken** – Stel deze optie in op **Ja** om de resultaten van het betalingsvoorstel in een rapport te bekijken, zonder dat betalingen worden uitgevoerd.
-   **Leveranciersfacturen van andere rechtspersonen opnemen** – Als uw organisatie een gecentraliseerd proces voor betaling heeft en in het betalingsvoorstel facturen van andere rechtspersonen moeten worden opgenomen die aan de zoekcriteria voldoen, stelt u deze optie in op **Ja**.
-   **Afzonderlijke leveranciersbetaling per rechtspersoon voorstellen** – Als deze optie is ingesteld op **Ja**, wordt een aparte betaling gemaakt voor elke rechtspersoon per leverancier. De leverancier op de betaling is de leverancier van de factuur van elke rechtspersoon. Als deze optie is ingesteld op **No** en dezelfde leverancier heeft facturen in meerdere rechtspersonen, wordt er één betaling gemaakt voor het totale bedrag van de geselecteerde facturen. De leverancier op de betaling is de leverancier in de huidige rechtspersoon. Als de leverancierrekening niet bestaat in de huidige rechtspersoon, wordt de leverancierrekening gebruikt van de eerste factuur die moet worden betaald.
-   **Betalingsvaluta** : dit veld geeft de valuta die in alle betalingen worden gemaakt. Als een valuta niet is gedefinieerd, wordt elke factuur wordt betaald in de valuta van de factuur.
-   **Betalingsweekdag** – Voer hier de dag van de week in waarop de betaling moet worden uitgevoerd. Dit veld wordt alleen gebruikt als de betalingsmethode is ingesteld om facturen bij elkaar op te tellen voor betaling op een bepaalde dag van de week.
-   **Type tegenrekening** en **tegenrekening** : instellen van deze velden voor het definiëren van een bepaald rekeningtype (zoals **grootboek** of **Bank**) en de tegenrekening (zoals een bepaalde bankrekening). De betalingsmethode voor de factuur bepaalt de standaard tegenrekeningtype en tegenrekening, maar u kunt deze velden de standaardwaarden desgewenst overschrijven.
-   **Extra filters** : Schakel op het **Records om op te nemen** sneltabblad kunt u aanvullende bereiken van de criteria definiëren. Als u een reeks leveranciers betaalt wilt, kunt u bijvoorbeeld een filter voor het bereik van de leverancier definiëren. Deze functionaliteit wordt vaak gebruikt om facturen voor een specifieke van betalingsmethode te selecteren. Bijvoorbeeld: als u een filter definiëren waar **betalingsmethode** = **controleren op**, alleen facturen met die methode van betaling zijn geselecteerd voor betaling, mits zij voldoen ook aan andere criteria die zijn opgegeven in de query.

## <a name="scenarios"></a>Scenario's
| Leverancier | Factuur | Factuurdatum | Factuurbedrag | Vervaldatum | Datum van contantkorting | Contantkortingsbedrag |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15 juni      | 500,00         | 15 juli  | 29 juni            | 10,00                |
| 3050   | 1002    | 20 juni      | 600,00         | 20 juli  | 4 juli             | 12,00                |
| 3075   | 1003    | 15 juni      | 250,00         | 29 juni  |                    | 0,00                 |
| 3100   | 1004    | 17 juni      | 100,00         | 17 juli  | 1 juli             | 1,00                 |

Op 1 juli betaalt April leveranciers. Ze gebruikt een betalingsvoorstel om deze taak efficiënter te voltooien.

### <a name="option-1-by-cash-discount"></a>Optie 1: Met contantkorting

April selecteert **Contantkorting** als het voorsteltype. Ze voert een datum bereik van juni 26 tot 10 juli. De volgende facturen zijn opgenomen in het voorstel:

-   1002, omdat de kortingsdatum van 4 juli in het bereik van de betalingsdatums valt.
-   1004, omdat de kortingsdatum van 1 juli in het bereik van de betalingsdatums valt.

De volgende facturen worden niet opgenomen in het voorstel:

-   1001, omdat de kortingsdatum van 29 juni al is vervallen, zodat deze factuur niet meer in aanmerking komt voor de contantkorting.
-   1003, omdat deze factuur geen kortingsdatum heeft.

### <a name="option-2-by-due-date"></a>Optie 2: Volgens vervaldatum

April selecteert **Volgens vervaldatum** als het voorsteltype. Ze voert een datum bereik van juni 26 tot 10 juli. De volgende facturen zijn opgenomen in het voorstel:

-   1003, omdat de vervaldatum van 29 juni in het bereik van de betalingsdatums valt.

De volgende facturen worden niet opgenomen in het voorstel:

-   1001, omdat de vervaldatum van 15 juli buiten het bereik van de betalingsdatums valt.
-   1002, omdat de vervaldatum van 20 juli buiten het bereik van de betalingsdatums valt.
-   1004, omdat de vervaldatum van 17 juli buiten het bereik van de betalingsdatums valt.

### <a name="option-3-by-due-date-and-cash-discount"></a>Optie 3: Volgens vervaldatum en contantkorting

April selecteert **Vervaldatum en contantkorting** als het voorsteltype. Ze voert een datum bereik van juni 26 tot 10 juli. De volgende facturen zijn opgenomen in het voorstel:

-   1003, omdat de vervaldatum van 29 juni in het bereik van de betalingsdatums valt.
-   1002, omdat de kortingsdatum van 4 juli in het bereik van de betalingsdatums valt.
-   1004, omdat de kortingsdatum van 1 juli in het bereik van de betalingsdatums valt.

De volgende facturen worden niet opgenomen in het voorstel:

-   1001, omdat de kortingsdatum van 29 juni al is vervallen, zodat deze factuur niet meer in aanmerking komt voor de contantkorting, en de vervaldatum van 15 juli eveneens buiten het datumbereik ligt.

## <a name="country-specific-considerations"></a>Landafhankelijke overwegingen
### <a name="norway"></a>Noorwegen

#### <a name="dimension-control"></a>Dimensiebesturingselement

Met een dimensiebesturingselement kunt u het groeperen van gegenereerde regels op betalingsvoorstel regelen en standaarddimensies instellen op basis van financiële dimensies voor de toegepaste facturen. In de context van Noorwegen is er voor elke betalingsmethode een financieel dimensietabblad waarin u de dimensiecontrole kunt activeren en het groeperen voor elke dimensie activeren kunt inschakelen. Mogelijke opties zijn:

-   Het veld **Dimensiebesturingselement** is uitgeschakeld. Het betalingsvoorstel werkt als voor elk ander land.
-   Het veld **Dimensiebesturingselement** wordt geactiveerd zonder de dimensies verder te definiëren. Het betalingsvoorstel wordt gemaakt zonder rekening te houden met dimensies. De gemaakte transactie neemt geen dimensies over van de toegepaste invoer.
-   Het veld **Dimensiebesturingselement** wordt geactiveerd en de overige dimensies worden ingeschakeld. Nu definieert u hoe de dimensies naar het journaal worden gekopieerd. Bijvoorbeeld: • Selecteer de **Business Unit** selectievakje in om een betalingsvoorstel per bedrijfseenheid voor de betalingsmethode van betaling, • selecteer de **CostCenter** selectievakje in om een betalingsvoorstel per kostenplaats voor de betalingsmethode van betaling maken

**Opmerking:** Als u meer dan een dimensie selecteert in de derde optie, wordt er een betalingsvoorstel gemaakt voor de dimensiecombinatie.

#### <a name="bank-account-selection"></a>Bankrekening selecteren

U kunt een standaard betaalrekening definiëren per betalingsmethode ongeacht de context van het land. Dit wordt ingesteld in betalingsregels die door een voorstel worden gegenereerd. Met de bankrekeningsfunctie kunt u meerdere betaalrekeningen definiëren die op dimensie en valuta worden beheerd of een combinatie van deze om andere betaalrekeningen te gebruiken, afhankelijk van elke combinatie. U kunt deze combinaties instelt in **betalingsmethoden** pagina met behulp van de **bankrekeningen** knop beschikbaar is voor elke betalingsmethode met **rekening boekingstype** = **Bank**.


