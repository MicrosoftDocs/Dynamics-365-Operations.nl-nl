---
title: Cashflowprognose
description: "Dit onderwerp bevat een overzicht van het cashflowprognoseproces. Ook wordt uitgelegd hoe cashflowprognoses worden geïntegreerd met andere modules in het systeem."
author: saraschi
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sarasch
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 75b47611f1c73a3fb771e63dc1dd12cadf8c4b32
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="cash-flow-forecasting"></a>Cashflowprognose

[!include[banner](../includes/banner.md)]

Met de functies voor cashflowprognoses kunt u de geplande cashflow en valutabehoeften analyseren, zodat u de toekomstige behoefte aan contant geld in het bedrijf kunt schatten. Voer de volgende taken uit om een prognose van de cashflow te verkrijgen:

- Bepaal alle liquiditeitsrekeningen en neem ze op in een lijst. Liquiditeitsrekeningen zijn de contant- of contantequivalente rekeningen van het bedrijf.
- Configureer het gedrag voor prognoses van transacties die van invloed zijn op de liquiditeitsrekeningen van het bedrijf.

Nadat u deze taken hebt uitgevoerd, kunt u prognoses van de cashflow en geplande valutabehoeften berekenen en analyseren.

## <a name="cash-flow-forecasting-integration"></a>Integratie van cashflowprognose

Cashflowprognose kan worden geïntegreerd met Grootboek, Klanten, Leveranciers, Budgettering en Voorraadbeheer. Het prognoseproces gebruikt transactiegegevens die in het systeem worden ingevoerd en het berekeningsproces geeft een prognose van het verwachte effect van elke transactie op contant geld. De volgende soorten transacties worden in aanmerking genomen wanneer de cashflow wordt berekend:

- **Verkooporders** - verkooporders die nog niet zijn gefactureerd en die leiden tot fysieke of financiële verkopen
- **Inkooporders** - inkooporders die nog niet zijn gefactureerd en die leiden tot fysieke of financiële inkopen
- **Klanten** - openstaande klanttransacties (facturen die nog niet zijn betaald)
- **Leveranciers** - openstaande leverancierstransacties (facturen die nog niet zijn betaald)
- **Grootboektransacties** – transacties waarvoor is opgegeven dat een toekomstige boeking zal plaatsvinden.
- **Budgetregistervermeldingen** - budgetjournaalposten die zijn geselecteerd voor cashflowprognoses.
- **Vraagprognoses** : voorraadprognosemodelregels die worden geselecteerd voor cashflowprognoses.
- **Aanbodprognoses** : voorraadprognosemodelregels die worden geselecteerd voor cashflowprognoses.

Hoewel er geen directe integratie met projectbeheer en boekhouding is, zijn er verschillende manieren om projecttransacties in de cashflowprognose op te nemen. Geboekte projectfacturen worden opgenomen in de prognose als onderdeel van openstaande klanttransacties. Door projecten geïnitieerde verkooporders en inkooporders worden in de prognose als openstaande orders opgenomen nadat ze in het systeem zijn ingevoerd. U kunt ook projectprognoses overbrengen naar een grootboekbudgetmodel. Dit grootboekbudgetmodel wordt vervolgens opgenomen in de cashflowprognose als onderdeel van de budgetregistervermeldingen.

## <a name="configuration"></a>Configuratie

U kunt het cashflowprognoseproces configureren met de pagina **Instelling van cashflowprognose**. Op deze pagina geeft u de liquiditeitsrekeningen op voor tracering, en het standaardprognosegedrag voor elk gebied.

### <a name="general-ledger"></a>Grootboek

U moet eerst de liquiditeitsrekeningen definiëren die moeten worden bijgehouden door middel van cashflowprognose. Deze liquiditeitsrekeningen zijn meestal hoofdrekeningen die zijn gekoppeld aan de bankrekeningen die contant geld ontvangen en uitkeren. Op de pagina **Instelling cashflowprognose** op het tabblad **Grootboek** selecteert u de hoofdrekeningen voor de prognose. Als een bankrekening is gekoppeld aan de hoofdrekening op de pagina **Bankrekening**, wordt deze weergegeven in het veld **Bankrekening**.

U kunt een afhankelijke cashflowprognose instellen voor een hoofdrekening die transacties bevat die rechtstreeks zijn gerelateerd aan transacties in een andere hoofdrekening. Met elke regel die u toevoegt in de sectie **Afhankelijke rekeningen**, wordt een cashflowprognosebedrag gemaakt in een afhankelijke hoofdrekening gemaakt. Dit bedrag is een percentage van de cashflowbedragen voor de primaire hoofdrekening die u hebt geselecteerd.

Stel eerst het veld **Hoofdrekening** in op de primaire hoofdrekening waarin transacties naar verwachting in eerste instantie zullen plaatsvinden. Stel het veld **Afhankelijke hoofdrekening** in op de rekening die wordt beïnvloed door de eerste transactie ten opzichte van de primaire hoofdrekening. Stel de juiste waarden voor de overige velden op de regel in. U kunt de waarde in het veld **Percentage** wijzigen om het effect van de primaire hoofdrekening op de afhankelijke hoofdrekening weer te geven. Selecteer voor een verkoop- of inkoopprognose een waarde voor **Betalingstermijnen** die wordt gebruikt voor de meeste klanten of leveranciers. Stel het veld **Boekingstype** in op het verwachte boekingstype dat is gerelateerd aan de cashflowprognose.

### <a name="accounts-payable"></a>Leveranciers    

U kunt de prognose voor inkopen berekenen met behulp van de instellingsopties op het tabblad **Leveranciers** van de pagina **Instelling cashflowprognose**. Voordat u de cashflowprognoses voor leveranciers kunt configureren, moet u betalingstermijnen, leveranciersgroepen en boekingsprofielen van leveranciers configureren.

In de sectie **Standaardwaarden inkoopprognose** kunt u het standaardinkoopgedrag voor cashflowprognose selecteren. Drie velden bepalen het tijdstip van het effect op contant geld: **Tijd tussen leveringsdatum en factuurdatum**, **Betalingstermijnen** en **Tijd tussen vervaldatum van factuur en betaaldatum**. In de prognose wordt de standaardinstelling alleen voor het veld **Betalingstermijnen** gebruikt als er geen waarde voor de transactie is opgegeven. Gebruik een betalingstermijn om het meest gangbare aantal dagen voor elk deel van het proces te beschrijven.

Met het veld **Liquiditeitsrekeningen voor betalingen** wordt de liquiditeitsrekening opgegeven die het meest voor betalingen wordt gebruikt. Gebruik het veld **Percentage van bedrag om toe te wijzen aan cashflowprognose** om op te geven of een percentage van bedragen moet worden gebruikt tijdens prognoses. Laat dit veld leeg als de volledige transactiebedragen moeten worden gebruikt tijdens prognoses.

U kunt de standaardinstelling voor het veld **Tijd tussen vervaldatum van factuur en betalingsdatum** voor specifieke leveranciersgroepen overschrijven. In de prognose wordt de standaardwaarde van de sectie **Standaardwaarden van inkoopprognose** gebruikt tenzij een andere waarde is opgegeven voor de leveranciersgroep die is gerelateerd aan de leverancier in de transactie. Als u de standaardwaarde wilt overschrijven, selecteert u een leveranciersgroep en stelt u vervolgens de nieuwe waarde voor het veld **Tijd inkoop** in.

U kunt de standaardinstelling voor het veld **Liquiditeitsrekening** overschrijven voor specifieke boekingsprofielen van leveranciers. In de prognose wordt de standaardwaarde van de sectie **Standaardwaarden van inkoopprognose** gebruikt tenzij een andere liquiditeitsrekening is opgegeven voor het boekingsprofiel dat is gerelateerd aan de leverancier in de transactie. Als u de standaardwaarde wilt overschrijven, selecteert u een boekingsprofiel en geeft u vervolgens de liquiditeitsrekening op die naar verwachting zal worden beïnvloed.

### <a name="accounts-receivable"></a>Klanten  

U kunt de prognose voor verkopen berekenen met behulp van de instellingsopties op het tabblad **Klanten** van de pagina **Instelling cashflowprognose**. Voordat u de cashflowprognoses voor klanten kunt configureren, moet u betalingstermijnen, klantgroepen en boekingsprofielen van klanten configureren.

In de sectie **Standaardwaarden verkoopprognose** kunt u het standaardverkoopgedrag voor cashflowprognose selecteren. Drie velden bepalen het tijdstip van het effect op contant geld: **Tijd tussen verzenddatum en factuurdatum**, **Betalingstermijnen** en **Tijd tussen vervaldatum van factuur en betaaldatum**. In de prognose wordt de standaardinstelling alleen voor het veld **Betalingstermijnen** gebruikt als er geen waarde voor de transactie is opgegeven. Gebruik een betalingstermijn om het meest gangbare aantal dagen voor elk deel van het proces te beschrijven. 

Met het veld **Liquiditeitsrekeningen voor betalingen** wordt de liquiditeitsrekening opgegeven die het meest voor betalingen wordt gebruikt. Gebruik het veld **Percentage van bedrag om toe te wijzen aan cashflowprognose** om op te geven of een percentage van bedragen moet worden gebruikt tijdens prognoses. Laat dit veld leeg als de volledige transactiebedragen moeten worden gebruikt tijdens prognoses.

U kunt de standaardinstelling voor het veld **Tijd tussen vervaldatum van factuur en betalingsdatum** voor specifieke klantgroepen overschrijven. In de prognose wordt de standaardwaarde van de sectie **Standaardwaarden van verkoopprognose** gebruikt tenzij een andere waarde is opgegeven voor de klantgroep die is gerelateerd aan de klant in de transactie. Als u de standaardwaarde wilt overschrijven, selecteert u een klantgroep en stelt u vervolgens de nieuwe waarde voor het veld **Tijd verkoop** in.

U kunt de standaardinstelling voor het veld **Liquiditeitsrekening** overschrijven voor specifieke boekingsprofielen van klanten. In de prognose wordt de standaardwaarde van de sectie **Standaardwaarden van verkoopprognose** gebruikt tenzij een andere liquiditeitsrekening is opgegeven voor het boekingsprofiel dat is gerelateerd aan de klant in de transactie. Als u de standaardwaarde wilt overschrijven, selecteert u een boekingsprofiel en stelt u vervolgens de liquiditeitsrekening in die naar verwachting zal worden beïnvloed.

### <a name="budgeting"></a>Budgettering

Budgetten die zijn gemaakt op basis van budgetmodellen, kunnen in cashflowprognoses worden opgenomen. Op het tabblad **Budgettering** van de pagina **Instelling cashflowprognose** selecteert u de budgetmodellen die u in de prognose wilt opnemen. Standaard worden nieuwe budgetregistervermeldingen opgenomen in prognoses nadat het budgetmodel is ingeschakeld voor cashflowprognoses. Opname in cashflowprognose kan voor afzonderlijke budgetregistervermeldingen worden overschreven.

### <a name="inventory-management"></a>Voorraadbeheer

Prognoses voor vraag en aanbod van voorraad kunnen worden opgenomen in cashflowprognoses. Op het tabblad **Voorraadbeheer** van de pagina **Instelling cashflowprognose** selecteert u het prognosemodel dat u in de cashflowprognose wilt opnemen. Opname in cashflowprognose kan voor afzonderlijke prognoseregels voor vraag en aanbod worden overschreven.

### <a name="calculation"></a>Berekening

Voordat u analyses van cashflowprognoses kunt bekijken, moet u het cashflowberekeningsproces uitvoeren. Met het berekeningsproces worden de toekomstige effecten van ingevoerde transacties op contant geld worden voorspeld.

Bereken de cashflowprognose met behulp van de pagina **Cashflowprognoses berekenen**. U kunt de volledige cashflowprognose of een incrementele cashflowprognose berekenen. 

- Als u alle cashflowprognosetransacties wilt wissen en herberekenen, stelt u het veld **Berekeningsmethode van cashflowprognose** in op **Totaal**. Het wordt aanbevolen deze methode te gebruiken als u de cashflowprognoses lange tijd niet hebt bijgewerkt. 
- Als u de bestaande cashflowinformatie alleen voor nieuwe transacties wilt bijwerken, stelt u het veld **Berekeningsmethode van cashflowprognose** in op **Nieuw**. Op de pagina wordt de datum weergegeven waarop uw cashflowberekening voor het laatst is uitgevoerd.

Ook kunt u batchverwerking voor uw cashflowprognoses gebruiken. Om te garanderen dat uw prognoseanalyses regelmatig worden bijgewerkt, stelt u een terugkerend batchproces in voor berekening van cashflowprognoses.

### <a name="reporting"></a>Rapportage

Nadat de cashflowprognose is berekend, moet u de gekoppelde entiteitsinformatie voor analytische rapportage vernieuwen. Selecteer op de pagina **Entiteitopslag** de maateenheid **LedgerCovLiquidityMeasurement aggregate** in en klik vervolgens op **vernieuwen**.

Er zijn twee werkgebieden die cashflowprognosegegevens bevatten. Eén werkgebied bevat gegevens voor alle bedrijven en de andere werkgebieden bevatten alleen gegevens voor het huidige bedrijf.

Toegang tot het werkgebied voor alle bedrijven wordt beheerd via de werkgebiedfunctie **Cashflow alle bedrijven weergeven**. Standaard is het werkgebied **Overzicht van contant geld - alle bedrijven** beschikbaar voor de volgende rollen:

- CEO (Chief Executive Officer)
- CFO (Chief Financial Officer)
- Financieel controller

Toegang tot het werkgebied voor het huidige bedrijf wordt beheerd via de werkgebiedfunctie **Cashflow huidig bedrijf weergeven**. Standaard is het werkgebied **Overzicht van contant geld - huidig bedrijf** beschikbaar voor de volgende rollen:

- Accountant
- Accountingmanager
- Supervisor boekhouding
- Leveranciersmanager
- Klantenmanager

Het werkgebied **Overzicht van contant geld - alle bedrijven** bevat analyses van cashflowprognoses in de systeemvaluta. De systeemvaluta en het systeemwisselkoerstype die worden gebruikt voor de analyses, worden gedefinieerd op de pagina **Systeemparameters**. Dit werkgebied bevat een overzicht van cashflowprognoses en bankrekeningsaldi voor alle bedrijven. Een diagram van de kasinkomsten en -uitgaven bevat een overzicht van toekomstige verplaatsingen van contant geld en saldi in de systeemvaluta, samen met gedetailleerde informatie over de voorspelde transacties. U kunt ook de voorspelde valutasaldi bekijken.

Het werkgebied **Overzicht van contant geld - huidig bedrijf** bevat analyses van cashflowprognoses in de gedefinieerde valuta voor boekhouding van het bedrijf. De valuta voor boekhouding die wordt gebruikt voor de analyses wordt gedefinieerd op de pagina **Grootboek**. Dit werkgebied bevat een overzicht van cashflowprognoses en bankrekeningsaldi voor het huidige bedrijf. Een diagram van de kasinkomsten en -uitgaven bevat een overzicht van toekomstige verplaatsingen van contant geld en saldi in de valuta voor boekhouding, samen met gedetailleerde informatie over de voorspelde transacties. U kunt ook de voorspelde valutasaldi bekijken.

Zie het onderwerp Power BI-inhoud Overzicht van contant geld voor meer informatie over de analyses van cashflowprognoses.

Bovendien kunt u gegevens van cashflowprognoses weergeven voor specifieke accounts, orders en artikelen op de volgende pagina's:

- **Proefbalans**: Selecteer **Cashflowprognoses** om de toekomstige cashflows voor de geselecteerde hoofdrekening weer te geven.
- **Alle verkooporders**: selecteer op het tabblad **Factuur** **Cashflowprognoses** om het voorspelde effect van de geselecteerde verkooporder op contant geld weer te geven.
- **Alle inkooporders**: selecteer op het tabblad **Factuur** **Cashflowprognoses** om het voorspelde effect van de geselecteerde inkooporder op contant geld weer te geven.
- **Aanbodprognose**: selecteer **Cashflowprognoses** om de toekomstige cashflows die zijn gekoppeld aan de geselecteerde aanbodprognose van items weer te geven.
- **Vraagprognose**: selecteer **Cashflowprognoses** om de toekomstige cashflows die zijn gekoppeld aan de geselecteerde vraagprognose van items weer te geven.


