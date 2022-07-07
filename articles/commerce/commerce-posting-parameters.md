---
title: Parameters voor boekingen in Commerce
description: In dit artikel worden de parameters beschreven die specifiek zijn voor het boeken van financiële en fysieke transacties in Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 56a2d1d2bcafdcdd9d88c132986e8ef485bf6b24
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027223"
---
# <a name="commerce-posting-parameters"></a>Parameters voor boekingen in Commerce

[!include [banner](includes/banner.md)]

In dit artikel worden de parameters beschreven die specifiek zijn voor het boeken van financiële en fysieke transacties in Microsoft Dynamics 365 Commerce. Commerce-boekingsparameters bevinden zich in Commerce Headquarters in **Retail en Commerce \> Headquarters instellen \> Parameters \> Commerce-parameters \> Boeken**.

## <a name="periodic-discount-parameters"></a>Parameters periodieke kortingen

In de volgende tabel worden de periodieke kortingsparameters beschreven die specifiek zijn voor het boeken van financiële en fysieke transacties.

| Parameter | Description |
|-----------|-------------|
| Periodieke korting boeken | Deze optie bepaalt of periodieke aanbiedingen worden geboekt naar grootboekrekeningen. Periodieke kortingen zijn combinatiekortingen, kwantumkortingen en kortingsaanbiedingen. Wanneer deze parameter wordt ingeschakeld, kunnen er extra velden worden ingesteld in de sectie **Periodieke kortingen**. |
| Type grootboekrekening | <p>Selecteer het type rekening dat wordt gebruikt om periodieke kortingen te boeken:</p><ul><li>**Standaard**: de kortingsvelden op deze pagina worden niet gebruikt. In plaats daarvan worden de rekeningen gebruikt die zijn gedefinieerd op de pagina **Boeking** in Commerce Headquarters (**Voorraadbeheer \> Instellen \> Boeken \> Boekingsformulieren**).</li><li>**Periodiek**: het systeem gebruikt de Commerce-kortingsrekeningen die worden opgegeven door de kortingsgerelateerde velden op deze pagina. Als u deze optie selecteert, moet u een grootboekrekening (GL) voor ieder type aanbieding opgeven (korting, combinatiekorting, hoeveelheid en drempel). Bij het instellen van de kortingen kunt u een rekening definiëren. Wanneer de boekingsfunctie voor kortingsrekeningen wordt gebruikt op de kortingsinstellingenpagina, wordt een extra debet- en creditboeking gemaakt om de kortingsboeking van de grootboekrekening Commerce-korting naar de grootboekkortingsrekening opnieuw te classificeren. Zie [Detailhandelkortingen](retail-discounts-overview.md) voor meer informatie.</li></ul> |
| Infocodekorting boeken | Deze optie wordt niet meer gebruikt in de standaard Commerce-oplossing en wordt afgeschaft. |
| Periodieke korting boeken voor orders | Met deze optie bepaalt u of periodieke kortingen voor detailhandel naar het grootboek worden geboekt voor klantorders en callcenterorders |

## <a name="inventory-update-parameters"></a>Voorraadbijwerkparameters

In de volgende tabel worden de voorraadbijwerkparameters beschreven die specifiek zijn voor het boeken van financiële en fysieke transacties.

| Parameter | Description |
|-----------|-------------|
| Standaard batch-id gebruiken als er geen batchnummers zijn gevonden | Deze optie bepaalt of een standaard batch-id wordt gebruikt voor batchartikelen wanneer er geen batchnummers zijn gevonden en negatieve voorraad is toegestaan. |
| Standaard batch-id | Het batchnummer dat wordt gebruikt wanneer batchnummers voor artikelen niet zijn gevonden en de parameter **Standaard batch-id gebruiken als er geen batchnummers zijn gevonden** is ingeschakeld. |

## <a name="aggregation-parameters"></a>Aggregatieparameters

In de volgende tabel worden de aggregatieparameters beschreven die specifiek zijn voor het boeken van financiële en fysieke transacties.

| Parameter | Description |
|-----------|-------------|
| Kluisstorting | Schakel deze parameter in om alle transacties tijdens het boeken van overzichten te totaliseren en één regel in het journaal te maken voor boeking in plaats van een aparte regel voor elke batch. |
| Bankstorting | Schakel deze parameter in om alle transacties tijdens het boeken van overzichten te totaliseren en één regel in het journaal te maken voor boeking in plaats van een aparte regel voor elke batch. |
| Verkooptransacties | Schakel deze parameter in om de transacties te consolideren als onderdeel van het boekingsproces voor transactieoverzichten. We raden u aan deze parameter in te schakelen. Dit werd eerder **Boekstuktransacties** genoemd. |
| Retouren niet samenvoegen | Als deze optie is geselecteerd, wordt elke retourtransactie als een aparte verkooporder geboekt bij het boeken van een detailhandeloverzicht. |

## <a name="batch-processing-parameters"></a>Batchverwerkingsparameters

In de volgende tabel worden de batchverwerkingsparameters beschreven die specifiek zijn voor het boeken van financiële en fysieke transacties.

| Parameter | Description |
|-----------|-------------|
| Maximumaantal parallelle overzichten | Dit veld definieert het aantal batchtaken dat wordt gebruikt om meerdere overzichten te boeken. |
| Maximale thread voor orderverwerking per overzicht | Dit veld geeft het maximale aantal threads aan dat wordt gebruikt door de batchtaak voor het boeken van overzichten om verkooporders voor een enkel overzicht te maken en te factureren. Het totale aantal threads dat door het boekingsproces voor overzichten wordt gebruikt, wordt berekend door de waarde in deze parameter te vermenigvuldigen met de waarde van de parameter **Maximumaantal parallelle overzichtboekingen**. Als u de waarde van deze parameter te hoog instelt, kunnen de prestaties van het boekingsproces voor overzichten negatief worden beïnvloed. |
| Maximumaantal transactieregels dat is opgenomen in een aggregatie | In dit veld wordt het aantal transactieregels gedefinieerd dat wordt opgenomen in één geaggregeerde transactie voordat een nieuwe transactie wordt gemaakt. Geaggregeerde transacties worden gemaakt op basis van verschillende aggregatiecriteria zoals klant, werkdag of financiële dimensies. Het is belangrijk te weten dat de regels van een enkele transactie niet over verschillende geaggregeerde transacties worden verdeeld. Dit betekent dat het aantal regels in een geaggregeerde transactie iets hoger of lager kan liggen, op basis van factoren zoals het aantal verschillende producten. |
| Maximumaantal threads voor het valideren van winkeltransacties | In dit veld wordt het maximumaantal threads bepaald dat kan worden gebruikt voor de validatie van transacties. Het valideren van transacties is een vereiste stap die moet plaatsvinden voordat de transacties in de overzichten kunnen worden opgenomen. U moet ook een geschenkbonproduct definiëren op het sneltabblad **Geschenkbon** van het tabblad **Boeking** van de pagina **Commerce-parameters**, zelfs wanneer de organisatie geen geschenkbonnen gebruikt. |

In de volgende tabel staan de aanbevolen waarden voor de parameters in de voorgaande tabel. Deze waarden moeten worden getest op en aangepast aan de implementatieconfiguratie en beschikbare infrastructuur. Overschrijding van de aanbevolen waarden kan een nadelige invloed hebben op andere batchverwerkingen en moet worden gevalideerd.

| Parameter | Aanbevolen waarde | Gegevens |
|-----------|-------------------|---------|
| Maximumaantal parallelle overzichtboekingen | <p>Stel deze parameter in op het aantal batchtaken dat beschikbaar is voor de batchgroep die de taak **Overzicht** uitvoert.</p><p>**Algemene regel:** het aantal virtuele AOS-servers (Application Object Server) vermenigvuldigen met het aantal batchtaken dat beschikbaar is per virtuele AOS-server.</p> | Deze parameter is niet van toepassing als de functie **Detailhandeloverzichten - groepsgewijze invoer** is ingeschakeld. |
| Maximale thread voor orderverwerking per overzicht | Begin met het testen van waarden bij **4**. Normaal gesproken mag de waarde niet hoger zijn dan **8**. | Deze parameter geeft het aantal threads aan dat wordt gebruikt om verkooporders te maken en te boeken. De parameter vertegenwoordigt het aantal threads dat voor boeking per overzicht beschikbaar is. |
| Maximumaantal transactieregels dat is opgenomen in een aggregatie | Begin met het testen van waarden bij **1000**. Afhankelijk van de configuratie van Commerce Headquarters kunnen kleinere orders gunstiger zijn voor de prestaties. | Deze parameter bepaalt het aantal regels dat in elke verkooporder wordt opgenomen tijdens het boeken van het overzicht. Als dit nummer is bereikt, worden regels opgedeeld in een nieuwe order. Het aantal verkoopregels is niet exact gelijk aan het opgegeven aantal, omdat de opsplitsing op verkooporderniveau plaatsvindt. Het aantal ligt echter dicht bij het aantal dat is ingesteld. Deze parameter wordt gebruikt om verkooporders te genereren voor detailhandeltransacties die geen benoemde klant hebben. |
| Maximumaantal threads voor het valideren van winkeltransacties | We raden u aan om deze parameter op **4** in te stellen en deze alleen te verhogen als u geen acceptabele prestaties behaalt. Het aantal threads dat in dit proces wordt gebruikt, kan niet hoger zijn dan het aantal processors dat beschikbaar is op de batchserver. Als het aantal threads te hoog is, heeft dit mogelijk invloed op andere batchverwerkingen. | Met deze parameter wordt het aantal transacties bepaald dat tegelijkertijd kan worden gevalideerd voor een bepaalde winkel. |

> [!NOTE]
> Alle instellingen en parameters die zijn gerelateerd aan overzichtsboekingen en die zijn gedefinieerd in winkels op de pagina **Commerce-parameters** zijn van toepassing op de verbeterde functie voor het boeken van overzichten.

## <a name="invoice-parameters"></a>Factuurparameters

In de volgende tabel worden de factuurparameters beschreven die specifiek zijn voor het boeken van financiële en fysieke transacties.

| Parameter | Description |
|-----------|-------------|
| Journaalnaam | De naam van het betalingsjournaal dat wordt gebruikt wanneer klantbetalingsjournalen voor verkooporderbetalingen worden gemaakt. Deze instelling is van toepassing op alle orderbetalingen die zijn geboekt voor orders voor het POS (verkooppunt), callcenter en e-commercekanaal. |
| Rekeningnaam | De naam van de betaalrekening. |
| Dimensies prioriteren op basis van betalingsmethode | Als de vlag is ingeschakeld, bevat de betalingsjournalen dimensies met prioriteit uit de betalingsmethode in plaats van dimensies uit de winkel. |
| Gedrag belastingberekening | Deze parameter specificeert het gedrag wanneer verkooporders die tijdens het boeken van overzichten worden gemaakt, worden gefactureerd:<ul><li>**Opnieuw berekenen**: belasting opnieuw berekenen.</li><li> **Niet opnieuw berekenen**: de belastingbedragen gebruiken die in POS zijn berekend.</li></ul> |
| Journaalnaam | De journaalnaam die wordt gebruikt wanneer een klantbetalingsjournaal voor restituties wordt gemaakt. Deze instelling is van toepassing op alle orderbetalingen die zijn geboekt voor orders voor het POS, callcenter en e-commercekanaal. |

## <a name="statement-parameters"></a>Overzichtparameters

In de volgende tabel worden de overzichtparameters beschreven die specifiek zijn voor het boeken van financiële en fysieke transacties.

| Parameter | Description |
|-----------|-------------|
| Voorraad reserveren tijdens berekening | Wanneer deze parameter is ingeschakeld, wordt via de overzichtsberekening de voorraad tijdelijk gereserveerd totdat het overzicht is geboekt. Deze parameter wordt standaard uitgeschakeld om de prestaties van overzichtsberekeningen te verbeteren. Bijgewerkte voorraadgegevens kunnen worden berekend met de batchtaak **Voorraad boeken**. De batchtaak **Voorraad boeken** wordt niet meer gebruikt wanneer voor orders [groepsgewijs boeken](trickle-feed.md) is ingeschakeld voor winkeltransacties. |
| Telling uitschakelen vereist | Deze vlag schakelt de telling uit tijdens het boeken in Commerce Headquarters. |
| Financiële dimensies herberekenen bij fout | Als deze parameter is ingeschakeld, worden financiële dimensies opnieuw geëvalueerd op achtereenvolgende overzichtboekingen wanneer de overzichtboeking mislukt. |
| Financiële dimensies van de retourwinkel gebruiken | Wanneer deze parameter is ingeschakeld, kunnen gekoppelde retourverkooporders worden gemaakt die de financiële dimensies van de winkel gebruiken in plaats van de financiële dimensies van de oorspronkelijke transactie. |
| Retouren ontkoppelen | Wanneer deze parameter is ingeschakeld, kan het overzicht retouren van niet-geboekte verkopen als blinde retouren maken. Deze parameter is standaard uitgeschakeld en het wordt aangeraden dit zo te laten. |
| Boeken van afrondingsverschillen uitschakelen | Met deze parameter wordt het boeken van afrondingsverschillen tussen transactiebetalingen en brutobedragen tijdens betalingsverwerkingen uitgeschakeld. |
| Automatisch vereffenen van klantdeposito's | Wanneer deze parameter wordt ingeschakeld, worden klantdeposito's die zijn geboekt tijdens de verwerking van het detailhandeloverzicht vereffend met openstaande klanttransacties. |
| Afstemming beheer van contant geld inschakelen en gebruiken vanuit POS | Als deze parameter is ingeschakeld, wordt er afstemming van contantbeheer uitgevoerd in het POS en worden de waarden doorgegeven aan de boeking van het financiële overzicht van de detailhandel om overzichtregels te maken. |
| Detailniveau boekstuk van grootboek | Met deze parameter wordt het detailniveau van het boekstuk van het grootboek bepaald voor geselecteerde transacties die afkomstig zijn uit het POS. Transactietypen omvatten inkomsten, onkosten en kortingen. Voor kortingen wordt alleen rekening gehouden met deze parameter als het rekeningnummer voor een periodieke korting en het rekeningnummer voor een normale korting niet hetzelfde zijn. Tenzij details vereist zijn, is **Overzicht** de aanbevolen waarde voor deze boekingen. Wanneer boeking op overzichtsniveau is gedefinieerd, wordt **TransactionDiscountTrans.RecID** niet ingevuld. In de versie Commerce 10.0.27 is deze vlag hernoemd en verplaatst. Eerder was dit **Detailniveau** in de sectie **Voorraadupdate**. |
