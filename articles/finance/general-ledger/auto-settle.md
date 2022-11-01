---
title: Grootboekvereffeningen automatiseren
description: Dit artikel geeft informatie over het proces Grootboekvereffeningen automatiseren.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708327"
---
# <a name="automate-ledger-settlements"></a>Grootboekvereffeningen automatiseren

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 Finance versie 10.0.31 is de functie  **Proces van grootboekvereffeningen automatiseren** beschikbaar in het werkgebied  **Functiebeheer** . U kunt de functie **Proces van grootboekvereffeningen automatiseren** alleen inschakelen als de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** is ingeschakeld.

Grootboekvereffening is het proces waarin debet- en credittransacties in het grootboek worden afgestemd. Organisaties die grootboekvereffeningsactiviteiten uitvoeren volgens een terugkerend schema kunnen het proces nu automatiseren. Tijdens het automatische grootboekvereffeningsproces kunnen een debettransactie en een credittransactie alleen met elkaar worden vereffend als de bedragen in de valuta voor boekhouding gelijk zijn.Een debetbedrag van $ 1,00 kan bijvoorbeeld automatisch worden vereffend met een creditbedrag van $ 1,00. Een debetwaarde van $ 1,00 kan echter niet automatisch worden vereffend met twee creditbedragen die elk de waarde $ 0,50 hebben. Gedeeltelijke vereffening van grootboektransactiebedragen wordt niet ondersteund.

Bij het automatiseren van grootboekvereffeningen wordt de volgende informatie gedefinieerd:

- Wanneer grootboekvereffeningen worden uitgevoerd
- Welke criteria worden gebruikt om de debet- en creditbedragen te vereffenen die automatisch kunnen worden vereffend
- De volgorde waarin de grootboekvereffeningsgegevens worden verwerkt

## <a name="define-the-occurrence-of-ledger-settlements"></a>Het patroon voor grootboekvereffeningen definiëren

Voor grootboekvereffeningsautomatisering wordt het raamwerk voor procesautomatisering gebruikt. Verschillende bedrijfsprocessen gebruiken dit raamwerk om het terugkeerpatroon van een geselecteerd proces te definiëren. Voor grootboekvereffeningen gaat u naar  **Systeembeheer \> Instellen \> Procesautomatiseringen** of **Grootboek \> Grootboek instellen \> Procesautomatiseringen**.

Selecteer eerst de optie  **Nieuwe procesautomatisering maken** en selecteer  **Grootboekvereffeningen**. Een wizard begeleidt u vervolgens bij het instellen van de automatisering.

## <a name="general-page"></a>Pagina Algemeen

Voer op de pagina  **Algemeen**  van de wizard de naam in van het grootboekvereffeningspatroon dat u maakt. Als uw overeenkomende debet- en creditbetalingen bijvoorbeeld op maandag in het grootboek worden vereffend, voert u een beschrijvende naam in, zoals  **LedgerSettle\_Ma**. De naam die u invoert, wordt weergegeven in de kolom **Automatiseringsregel** op de pagina  **Grootboekvereffeningen** .

De overige instellingen op de pagina zijn algemeen en worden gebruikt om het periodieke patroon te definiëren voor deze versie van de grootboekvereffeningen. Als een vereffening steeds op maandag plaatsvindt, kunt u definiëren dat het wekelijks wordt uitgevoerd en kunt u maandag als de dag van de week selecteren waarop het wordt uitgevoerd. U kunt ook een vroege planningstijd invoeren, zoals 2:00 u, zodat de procesautomatisering vóór het begin van de volgende werkdag wordt voltooid. U wordt aangeraden de procesautomatisering zo te plannen dat deze buiten uw normale werkuren wordt uitgevoerd. Op deze manier kunt u ervoor zorgen dat het minder gevolgen heeft voor uw boekhoudpersoneel gedurende de werkdag.

Zie de documentatie over procesautomatisering voor meer informatie over de andere velden op de pagina  **Algemeen** .

## <a name="ledger-settlements-match-criteria-page"></a>Pagina Vereffeningscriteria voor grootboekvereffening

De volgende pagina in de wizard is de pagina  **Vereffeningscriteria voor grootboekvereffening** . Deze wordt gebruikt om de hoofdrekeningen te definiëren die zijn opgenomen in het procesautomatiseringsvoorval en de criteria die worden gebruikt om corresponderende debet- en creditbedragen te bepalen.

### <a name="account-selection"></a>Rekening selecteren

De hoofdrekeningen die u eerder hebt gedefinieerd als grootboekvereffeningsrekeningen voor de rechtspersoon worden weergegeven. (U definieert hoofdrekeningen als grootboekvereffeningsrekeningen in **Grootboek \> Grootboek instellen \> Grootboekparameters \> Grootboekvereffeningen**.)

### <a name="main-account-and-posting-layer"></a>Hoofdrekening en boekingslaag

De waarden  **Hoofdrekening** en **Boekingslaag**  zijn vereiste vereffeningscriteria. De waarden **Hoofdrekening** en **Boekingslaag** van de debettransactie en credittransactie in het grootboek moeten hetzelfde zijn om met elkaar te kunnen worden vereffend tijdens het automatische grootboekvereffeningsproces.

### <a name="posting-type"></a>Boekingstype

Selecteer de optie **Boekingstype** als de debet- en credittransacties in het grootboek hetzelfde boekingstype moeten hebben om met elkaar te kunnen worden vereffend tijdens het automatische grootboekvereffeningsproces.

### <a name="financial-dimensions"></a>Financiële dimensies

Selecteer de optie **Financiële dimensies** als de debet- en credittransacties in het grootboek dezelfde financiële dimensies moeten hebben om met elkaar te kunnen worden vereffend tijdens het automatische grootboekvereffeningsproces. Als deze optie is geselecteerd, moeten de criteria voor financiële dimensies worden geselecteerd in de lijst **Beschikbare financiële dimensies**. De lijst **Beschikbare financiële dimensies** bevat geen hoofdrekeningdimensie omdat deze automatisch is vereist als onderdeel van de vereffeningscriteria.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>De resultaten van een grootboekvereffeningsautomatisering weergeven

Nadat de reeks automatiseringen voor grootboekvereffening is gemaakt, worden de herhalingen voor elke grootboekvereffening weergegeven in de weekweergave van de procesautomatisering. Bovendien wordt de status van elk exemplaar weergegeven. De volgende statussen worden gebruikt:

- **Gepland** : de automatisering is gepland, maar nog niet uitgevoerd.
- **Uitvoeren**: de automatisering wordt momenteel uitgevoerd.
- **Fout** : de automatisering is uitgevoerd, maar er is een fout opgetreden. U kunt de fouten weergeven door de knop  **Resultaten weergeven**  te selecteren.
- **Voltooid** : de automatisering is uitgevoerd. U kunt de vereffeningsresultaten weergeven op de pagina **Grootboekvereffeningen**.

Als u de overeenkomende resultaten wilt weergeven, gaat u naar **Grootboekvereffeningen \> Periodieke taken \> Grootboekverffeningen**. In het veld **Automatiseringsregel** op de pagina **Grootboekvereffeningen** wordt de naam weergegeven van de geplande taak voor automatische grootboekvereffening waarmee de transactie is vereffend. Bij mislukte vereffeningspogingen zal de waarde van de **Automatiseringsregel** niet worden bijgewerkt. Als u handmatig een transactie omkeert die eerder met succes is vereffend door het automatiseringsproces, wordt de waarde van **Automatiseringsregel** verwijderd.

Het veld **Datum vereffend** voor de vereffende records geeft de datum weer waarop het automatiseringsproces is uitgevoerd.

## <a name="editing-a-ledger-settlement-automation"></a>Een grootboekvereffeningsautomatisering bewerken

Met het raamwerk voor procesautomatisering kunt u de reeks en de herhalingen bewerken die voor de grootboekvereffening zijn gemaakt. De reeks kan worden bewerkt via de pagina  **Procesautomatisering**  of via de weekweergave van de procesautomatisering. Als de manager bijvoorbeeld grootboekvereffening op woensdag in plaats van op maandag wil uitvoeren, kan hij een herhaling selecteren in de weekweergave en vervolgens  **Weergeven/bewerken – reeks**.

Als u een reeks bewerkt, wordt u gevraagd om op te geven of de wijziging in alle bestaande herhalingen moet worden aangebracht of alleen in de nieuwe. Herhalingen uit het verleden die al de status **Voltooid** hebben of die met een de status  **Fout**  zijn geëindigd, worden niet gewijzigd.

U kunt ook een nieuw exemplaar toevoegen of een bestaand exemplaar wijzigen. De volgende grootboekvereffeningsherhaling is bijvoorbeeld gepland voor uitvoering op woensdag 1 januari, maar deze datum is een feestdag. U kunt de herhaling wijzigen via de pagina  **Procesautomatisering**  of via de weekweergave van de procesautomatisering. Er wordt een pagina geopend waarin de planningsdetails en de vereffeningscriteria worden weergegeven. Hier kunt u de geplande tijd en datum bewerken. U kunt ook de criteria voor vereffening bewerken als er wijzigingen zijn vereist. 

U kunt ook een exemplaar of een reeks uitschakelen. Als u een herhaling wilt uitschakelen en de verwerking wilt uitstellen, selecteert u deze in de weekweergave voor procesautomatisering en vervolgens selecteert u  **Uitschakelen**. U kunt een reeks uitschakelen op de pagina **Procesautomatisering** .

## <a name="security-for-ledger-settlement-automation"></a>Beveiliging voor automatisering van grootboekvereffening

De functie **Onderhouden van instellingen voor automatiseringsreeksen voor grootboekvereffening** is toegevoegd aan de rollen Accounting Manager en Accounting Supervisor en de functie **Weergeven van instellingen van automatiseringsreeksen voor grootboekvereffening** is toegevoegd aan de rollen Accountant, Accounting Manager en Accounting Supervisor voor automatiseringen van grootboekvereffeningen. Deze functies zijn de standaard beveiligingsinstellingen, maar ze kunnen worden gewijzigd op basis van de vereisten van uw organisatie.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Grootboekparameters voor automatisering van grootboekvereffening

Het veld **Gebruikelijk saldo vereffening** geeft de volgorde aan waarin de automatische grootboekvereffening wordt verwerkt. Als u de waarde **Gebruikelijk saldo vereffening** wilt instellen of weergeven, gaat u naar **Grootboek \> Instellen \> Grootboekparameters** en selecteert u het tabblad **Grootboekvereffeningen**.

Als **Debet** is geselecteerd, wordt het geautomatiseerde grootboekvereffeningsproces gestart aan de debetzijde en wordt naar corresponderende creditbedragen gezocht. Als **Credit** is geselecteerd, wordt het geautomatiseerde grootboekvereffeningsproces gestart aan de creditzijde en wordt naar corresponderende debetbedragen gezocht. Deze optie moet het gebruikelijke saldo van de hoofdrekening aangeven.

## <a name="processing-a-ledger-settlement-automation"></a>Automatisering van een grootboekvereffening verwerken

Wanneer de automatisering wordt uitgevoerd, selecteert het systeem grootboektransacties voor de hoofdrekeningen die voor de procesautomatiseringsreeks zijn gedefinieerd. Het ordent de transacties op datum met behulp van een datumbereik van het begin van het fiscaal jaar tot de datum waarop de procesautomatisering wordt uitgevoerd. Er wordt vereffend op basis van de opgegeven vereffeningscriteria. De absolute waarden van de bedragen in de boekhoudvaluta van het debet- en het creditbedrag moeten overeenkomen om te worden vereffend.

Terwijl een hoofdrekening wordt verwerkt door een herhaling van een grootboekvereffeningsautomatisering, kunt u dit niet weergeven op de pagina **Grootboekvereffeningen**. U moet wachten tot het automatiseringsproces is voltooid. Het is raadzaam om te plannen dat de procesautomatisering buiten werkuren wordt uitgevoerd om conflicten te voorkomen.

Het automatiseringsproces bevat alle transacties die aan de criteria voldoen, behalve transacties die handmatig zijn gemarkeerd voor vereffening op de pagina **Grootboekvereffeningen**.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Omkering van transacties die zijn vereffend door het automatiseringsproces

U kunt een vereffening omkeren die door het geautomatiseerde grootboekvereffeningsproces is gemaakt. Wanneer een transactie wordt omgekeerd die al was vereffend door het automatiseringsproces, wordt de waarde van **Automatiseringsregel** verwijderd.
