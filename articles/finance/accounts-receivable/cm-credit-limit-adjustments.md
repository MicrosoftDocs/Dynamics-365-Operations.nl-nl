---
title: Correcties kredietlimiet
description: In dit onderwerp wordt uitgelegd hoe u correcties voor kredietlimieten instelt en toevoegt.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d55a7c5e24213f70a1b71f89691f0e5be8c36f10
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976566"
---
# <a name="credit-limit-adjustments"></a>Correcties kredietlimiet 

[!include [banner](../includes/banner.md)]

Met kredietlimietcorrecties kunnen creditmanagers de kredietlimieten en vervaldatums van één klant, een groep klanten of alle klanten bijwerken via een boekingsproces. U kunt correctieposten voor kredietlimieten toevoegen om klanten en klantkredietgroepen bij te werken of u kunt ze gebruiken om automatische kredietlimieten te berekenen. De gegevens kunnen vervolgens worden beoordeeld, ter goedkeuring worden verzonden via een workflow en geboekt naar klantrekeningen.

## <a name="set-up-credit-limit-adjustments"></a>Kredietlimietcorrecties instellen

U kunt posten in het journaal voor kredietlimietcorrecties maken op de pagina **Kredietlimietcorrectie** (**Kredietbeheer \> Kredietlimietcorrecties \> Kredietlimietcorrecties**).

1. Selecteer **Nieuw**. Er wordt een nieuwe groep boekingen gemaakt met een nummer voor de kredietlimietcorrectie.
2. Selecteer het type kredietlimietcorrectie:

    - Selecteer **Kredietlimiet** als u de kredietlimiet van de klant wilt wijzigen.
    - Selecteer **Tijdelijke kredietlimiet** om een tijdelijke kredietlimiet te maken in plaats van de huidige kredietlimiet van de klant te wijzigen. Tijdelijke kredietlimieten overschrijven de kredietlimiet van een klant gedurende een vastgestelde periode. Na afloop van deze periode wordt de kredietlimiet van de klant weer gebruikt.
3. Voer een omschrijving in. 

Als het selectievakje **Geboekt** is ingeschakeld, zijn de kredietlimieten toegepast. Het veld **Goedkeuringsstatus** geeft de workflowstatus van het journaal aan. Een workflow is optioneel.

### <a name="add-credit-limit-adjustments"></a>Kredietlimietcorrecties toevoegen

Als u handmatig kredietlimietcorrecties wilt toevoegen, selecteert u **Regels** en voert u de volgende stappen uit.

1. Gebruik het menu **Klantcorrecties** om een kredietlimietcorrectie voor een klant toe te voegen. Selecteer **Kredietgroepcorrecties voor klant** om een kredietlimiet voor een kredietgroep van een klant toe te voegen.
2. Voer een klantrekening in voor de factuurklantrekening die moet worden bijgewerkt met de nieuwe kredietlimiet. Als u in stap 1 **Kredietgroepcorrecties voor de klant** hebt geselecteerd, voert u de kredietgroep voor de klant in. U kunt niet zowel een klantrekening als een klantkredietgroep-id invoeren op dezelfde journaalregel.

    De huidige kredietlimiet wordt weergegeven en de naam wordt automatisch weergegeven.

3. Voer de nieuwe kredietlimiet in die de huidige kredietlimiet moet vervangen wanneer de kredietlimietpost wordt geboekt.
4. Voer een datum in om de nieuwe vervaldatum voor de kredietlimiet van de klant te definiëren. U moet een vervaldatum voor de kredietlimiet invoeren wanneer u een kredietlimietcorrectie maakt.

Het veld **Goedkeuringsstatus** geeft de workflowstatus van het journaalregel aan.

Als u wilt dat de kredietlimietcorrecties automatisch worden gegenereerd, kunt u het menu **Genereren** in het actiedeelvenster gebruiken.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Tijdelijke kredietlimietcorrecties toevoegen

Als u handmatig tijdelijke kredietlimietcorrecties wilt toevoegen, voert u de volgende stappen voor de journaalregels uit.

1. Gebruik het menu **Klantcorrecties** om een kredietlimietcorrectie voor een klant toe te voegen. Selecteer **Kredietgroepcorrecties voor klant** om een kredietlimiet voor een kredietgroep van een klant toe te voegen.
2. Voer een klantrekening in voor de factuurklantrekening die moet worden bijgewerkt met de nieuwe kredietlimiet. Als u in stap 1 **Kredietgroepcorrecties voor de klant** hebt geselecteerd, voert u de kredietgroep voor de klant in. U kunt niet zowel een klantrekening als een klantkredietgroep-id invoeren op dezelfde journaalregel.

    Als er al een actieve of toekomstige tijdelijke kredietlimiet bestaat, worden voor elke tijdelijke kredietlimiet de huidige tijdelijke kredietlimiet en datumbereiken weergegeven. De naam wordt automatisch weergegeven.

3. Voer de nieuwe kredietlimiet in die de huidige kredietlimiet moet vervangen.
4. Definieer in de velden **Nieuwe begindatum** en **Nieuwe einddatum** de periode waarin de geavanceerde kredietlimiet geldig is. U moet vervaldatums voor de kredietlimiet invoeren wanneer u een kredietlimietcorrectiejournaal maakt.

Het veld **Goedkeuringsstatus** geeft de workflowstatus van het journaalregel aan.

## <a name="generate-credit-limit-adjustments"></a>Kredietlimietcorrecties genereren

U kunt ook de kredietlimieten automatisch laten aanpassen. Selecteer **Genereren** in het actiedeelvenster en selecteer een van de volgende opties:

- Van bestaande klant
- Van bestaande klantkredietgroep
- Automatische kredietlimieten

### <a name="from-existing-customer"></a>Van bestaande klant

U kunt journaalregels maken van bestaande klanten. Wanneer u **Genereren \> Van bestaande klant** selecteert, wordt een dialoogvenster weergegeven waarin u criteria kunt opgeven voor het selecteren van klanten en het berekenen van de nieuwe limieten.

1. Voer een correctiewaarde in om een bedrag bij de kredietlimiet op te tellen of ervan af te trekken. Voer een negatieve waarde in om de huidige kredietlimiet te verlagen of een positieve waarde om deze te verhogen.
2. Selecteer in het veld **Waardetype** hoe de waarde die u in stap 1 hebt ingevoerd, moet worden gebruikt om de nieuwe kredietlimiet te berekenen:

    - Selecteer **Vaste waarde** als u de kredietlimiet met een bedrag wilt wijzigen.
    - Selecteer **Percentage** als u de kredietlimiet met een percentage wilt wijzigen.

3. Voer een waarde in die wordt gebruikt om de berekende kredietlimiet af te ronden. Voer bijvoorbeeld **10,00** in om de kredietlimiet af te ronden op de dichtstbijzijnde 10,00 valuta-eenheden.
4. Stel het veld **Afrondingsformulier** in om op te geven of het restbedrag naar boven of naar beneden moet worden afgerond.
5. Selecteer de methode die wordt gebruikt om datums aan te passen.

    - Als u **Absoluut** selecteert, kunt u datums invoeren waarmee het datumbereik voor de kredietlimieten wordt gedefinieerd.
    - Als u **Relatief** selecteert, kunt u de verschuivingsdatums voor het bereik invoeren. Het huidige datumbereik voor de kredietlimiet wordt gecorrigeerd met het verschuivingsgetal.

6. Gebruik het sneltabblad **Op te nemen records** om te filteren welke lijst met klanten moet worden opgenomen. Als u geen filters opneemt, worden kredietlimietposten voor alle klanten gegenereerd.
7. Selecteer **OK** om de correctieposten voor de kredietlimiet te maken.

### <a name="from-existing-customer-credit-group"></a>Van bestaande klantkredietgroep

U kunt journaalregels maken van bestaande klantkredietgroepen. Wanneer u **Genereren \> Van bestaande klantkredietgroep** selecteert, wordt een dialoogvenster weergegeven waarin u criteria kunt opgeven om klantkredietgroepen te selecteren en de nieuwe limieten te berekenen. De criteria zijn dezelfde criteria die worden gebruikt om journaalregels te maken van bestaande klanten. Zie de stappen in de vorige sectie.

### <a name="automatic-credit-limits"></a>Automatische kredietlimieten

U kunt automatische kredietlimieten maken om kredietlimieten van klanten te definiëren en bij te werken. De automatische kredietlimieten worden voor een risicogroep gemaakt en zijn gebaseerd op specifieke waarden die worden gebruikt in de scoregroepen. U kunt deze automatische kredietlimieten gebruiken om kredietlimietposten te genereren. Als een klant aan een specifieke risicogroep is toegewezen en de kredietgegevens van de klant voldoen aan de criteria voor een automatische kredietlimiet, wordt een correctie van de kredietlimiet gemaakt.

#### <a name="create-automatic-credit-limits"></a>Automatische kredietlimieten maken

U maakt automatische kredietlimieten met behulp van kredietlimietcorrecties. Wanneer u **Genereren \> Automatische kredietlimieten** inschakelt, wordt een dialoogvenster weergegeven waarin u een vervaldatum kunt instellen voor de nieuwe kredietlimieten die worden gemaakt op basis van de risicogroepen waaraan klanten zijn toegewezen. Wanneer u klaar bent, selecteert u **OK** om de regels voor kredietlimietcorrecties te maken.

### <a name="post-adjustments"></a>Correcties boeken

Nadat u correctieregels voor de kredietlimieten hebt gemaakt, kunt u de knop **Boeken** in het actievenster gebruiken om de posten te boeken en de kredietlimieten van de klant bij te werken. Als u echter een workflow hebt ingesteld, moet u **Workflow \>Indienen** in het actievenster selecteren om het journaal ter goedkeuring in te dienen.

### <a name="credit-limit-adjustments-workflows"></a>Workflows voor kredietlimietcorrecties

De workflows voor **Kredietlimietcorrecties** kunnen worden gebruikt voor het verzenden van kredietlimietcorrecties via een goedkeuringsproces voor workflows. U kunt twee workflows maken op de pagina **Kredietbeheerworfklow** (**Kredietbeheer \> Instellen \> Kredietbeheerworfklow**):

- **Kredietlimietcorrecties**: u kunt deze workflow gebruiken om boekingen op koptekstniveau goed te keuren.
- **Kredietlimietcorrectieregel**: u kunt deze workflow gebruiken om de correctieposten goed te keuren, zodat deze door verschillende personen kunnen worden goedgekeurd op basis van de criteria in de workflow.

> [!NOTE]
> Wanneer u de workflow **Kredietlimietcorrecties** maakt, kunt u deze zo instellen dat de correcties automatisch worden geboekt nadat de regels zijn goedgekeurd. U hoeft alleen de taak **Journaal automatisch boeken** in de workflow op te nemen.
