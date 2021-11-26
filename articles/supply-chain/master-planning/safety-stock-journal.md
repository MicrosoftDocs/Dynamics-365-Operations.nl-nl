---
title: Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning voor artikelen bij te werken
description: In dit onderwerp wordt beschreven hoe u veiligheidsvoorraadjournalen gebruikt om de veiligheidsvoorraadhoeveelheid voor artikelen bij te werken door voorstellen voor minimale behoefteplanning te berekenen op basis van historische transacties.
author: ChristianRytt
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 59e4959898cd961582e1ac1d2285c0c0867ee7af
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790965"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning voor artikelen bij te werken

[!include [banner](../../includes/banner.md)]

Veiligheidsvoorraad duidt op een extra hoeveelheid van een artikel dat op voorraad wordt gehouden om het risico te verkleinen dat het artikel uitverkocht raakt. Veiligheidsvoorraad wordt gebruikt als een buffer voor het geval er verkooporders binnenkomen, maar de leverancier niet kan voldoen aan de gevraagde verzenddatum van de klant.

In dit onderwerp wordt beschreven hoe het veiligheidsvoorraadjournaal moet worden gebruikt voor het berekenen van de voorstellen voor minimumbehoefteplanning op basis van historische transacties en om vervolgens de artikelbehoefteplanning met de voorstellen bij te werken.

## <a name="overview-of-minimum-coverage-usage"></a>Overzicht van minimaal gebruik van behoefteplanning

De veiligheidsvoorraad wordt ingesteld op de pagina **Artikelbehoefteplanning** voor elk artikel. Verschillende typen aanvulling worden vertegenwoordigd door verschillende behoefteplanningscodes. (Zie [Afhandeling van veiligheidsvoorraad voor artikelen](safety-stock-replenishment.md) voor meer informatie.) Voor alle behoefteplanningscodes wordt echter de waarde gebruikt die is ingesteld in het veld **Minimum** op de pagina **Artikelbehoefteplanning** voor elk artikel. Het veld **Minimum** kan op twee manieren worden gebruikt:

- **Minimumhoeveelheid voor min/max. doeleinden**: bij deze benadering wordt de minimumhoeveelheid samen met min/max-logica gebruikt. Dit geldt wanneer het veld **Behoefteplanningscode** is ingesteld op *Min/Max* voor het relevante artikel of de relevante behoefteplanningsgroep. De hoeveelheid van **Minimum** staat voor het gemiddelde dagelijkse gebruik vermenigvuldigd met de doorlooptijd van het artikel.
- **Minimumhoeveelheid voor voorraadplandoeleinden**: bij deze benadering wordt de minimumhoeveelheid gebruikt om een voorraadplan weer te geven in combinatie met vraagprognoses. Dit geldt wanneer het veld **Behoefteplanningscode** is ingesteld op *Periode* of *Behoefte* voor het relevante artikel of de relevante behoefteplanningsgroep. De hoeveelheid van **Minimum** staat voor een voorraadplan dat het gewenste serviceniveau voor de klant weergeeft om de voorraadtekorten, gedeeltelijke zendingen en levertijden te reduceren. De minimumhoeveelheid geeft een percentage van de prognosenauwkeurigheid voor een bepaald artikel aan. Hiermee wordt geen gewenste voorraadpositie aangegeven.

De waarde voor **Minimum** kan op drie manieren worden ingesteld:

- Handmatig op de pagina **Artikelbehoefteplanning**
- Met het Gegevensbeheer-framework (*Artikelbehoefteplanning*-gegevensentiteiten)
- Met de berekening van de veiligheidsvoorraad die wordt uitgevoerd door veiligheidsvoorraadjournalen

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Minimumbehoefteplanning berekenen op basis van historisch gebruik

Veiligheidsvoorraadjournalen worden gebruikt om een voorgestelde minimumhoeveelheid te berekenen op basis van het historische gebruik van een artikel, voor min/max-doeleinden of voor voorraadplandoeleinden. Historisch gebruik vertegenwoordigt alle uitgiftetransacties gedurende een opgegeven periode. Deze uitgiftetransacties omvatten verkoopordertransacties en voorraadcorrecties. De berekeningen geven ook het effect van de voorgestelde minimumhoeveelheid op de voorraadwaarde aan en de wijziging in de voorraadwaarde vergeleken met de huidige minimumhoeveelheden.

Elke veiligheidsvoorraadjournaalregel vertegenwoordigt een artikel en de bijbehorende behoefteplanningsdimensies. Deze journaalregels worden gemaakt en weergegeven op de pagina **Journaalregels veiligheidsvoorraad** (**Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Berekening veiligheidsvoorraad)**. Het bedrijfsproces waarbij de veiligheidsvoorraadjournalen worden gebruikt om de voorgestelde minimumhoeveelheden te berekenen, wordt verderop in dit onderwerp beschreven.

De planner gebruikt een veiligheidsvoorraadjournaal om voorgestelde minimumhoeveelheden voor geselecteerde artikelen te berekenen op basis van het historische gebruik tijdens geselecteerde perioden. De voorgestelde minimumhoeveelheden kunnen indien nodig handmatig worden overschreven en u kunt de mogelijke invloed van de voorgestelde minimumhoeveelheden op de voorraadwaarde controleren. Als het journaal wordt geboekt, worden de bijbehorende minimumhoeveelheden in de artikelbehoefteplanning automatisch bijgewerkt.

### <a name="create-a-new-safety-stock-journal-name"></a>Een nieuw veiligheidsvoorraadjournaal maken

U moet ten minste één journaalnaam voor veiligheidsvoorraad maken voordat u dit type journaal kunt genereren. U kunt doorgaans verschillende journaalnamen gebruiken om uw veiligheidsvoorraadberekeningen te scheiden.

1. Ga naar **Hoofdplanning \> Instellen \> Journaalnamen veiligheidsvoorraad**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel de volgende velden op de nieuwe regel in:

    - **Naam**: voer een korte naam voor het journaal in.
    - **Beschrijving**: voer een beschrijving van het journaal in.
    - **Privé voor gebruikersgroep**: selecteer een gebruikersgroep om de doelgroep voor de huidige journaalnaam te beperken.
    - **Regels verwijderen na de boeking**: schakel dit selectievakje in om journaalregels standaard op te schonen bij het boeken. Schakel het selectievakje uit als u alle geboekte regels wilt behouden.

    Het veld **Journaaltype** is alleen-lezen en is vooraf ingesteld op *Veiligheidsvoorraad*.

1. Sluit de pagina.

### <a name="create-a-safety-stock-journal-and-lines"></a>Een veiligheidsvoorraadjournaal en regels maken

Met deze stap wordt een journaal gemaakt en worden er automatisch regels aan toegevoegd. Met elke regel worden een artikel, de bijbehorende behoefteplanningsdimensies en verschillende berekende hoeveelheden uit de gebruikshistorie aangegeven. De berekende hoeveelheden bevatten gemiddelde uitgiften per doorlooptijd van het artikel, gemiddelde uitgiften per maand en de standaardafwijking per maand.

#### <a name="automatically-generate-journal-lines"></a>Journaalregels automatisch genereren

Journaalregels kunnen alleen automatisch worden gegenereerd als er geen regels bestaan voor het journaal dat momenteel wordt weergegeven.

Voer de volgende stappen uit om automatisch journaalregels te genereren.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Berekening veiligheidsvoorraad**.
1. Selecteer **Nieuw** in het actievenster. Er wordt een nieuw veiligheidsvoorraadjournaal gemaakt.
1. Stel op het sneltabblad **Details journaalkoptekst** de volgende velden in:

    - **Naam**: selecteer de naam van het veiligheidsvoorraadjournaal waaraan u de regel wilt toevoegen.
    - **Beschrijving**: de standaardwaarde is de beschrijving van de geselecteerde journaalnaam. U kunt deze waarde echter zo nodig bewerken.
    - **Regels verwijderen na de boeking**: schakel dit selectievakje in om journaalregels op te schonen bij het boeken. Schakel het selectievakje uit als u alle geboekte regels wilt behouden. De instelling wordt overgenomen van de geselecteerde journaalnaam.

    Het veld **Journaal** is alleen-lezen en bevat het ID-nummer van het journaal dat u maakt en waaraan u regels toevoegt.

1. Selecteer op het sneltabblad **Journaalregels** de optie **Regels maken** op de werkbalk.
1. Stel de volgende velden in het dialoogvenster **Journaalregels maken voor voorgestelde minimumvoorraadniveaus** in:

    - **Begindatum**: selecteer de begindatum van de periode waarin uitgiften in de berekening moeten worden opgenomen.
    - **Einddatum**: selecteer de einddatum van de periode waarin uitgiften in deze berekening moeten worden opgenomen. Er moeten ten minste twee maanden tussen de begin- en einddatum zitten.
    - **Standaardafwijking berekenen**: stel deze optie in op *Ja* om de standaardafwijking te berekenen. U moet deze optie op *Ja* instellen als u de optie **Serviceniveau gebruiken** wilt gebruiken wanneer u het voorstel berekent (zoals verderop in dit onderwerp wordt beschreven).

1. Op het sneltabblad **Op te nemen records** kunt u filters en beperkingen instellen om aan te geven welke gegevens u in het rapport wilt opnemen. (U kunt bijvoorbeeld filteren op waarde van **Behoefteplanningsgroep**.) Selecteer **Filter** om een standaarddialoogvenster van de query-editor te openen, waarin u selectiecriteria, sorteercriteria en joins kunt definiëren. De velden werken op dezelfde manier als bij andere typen query's in Microsoft Dynamics 365 Supply Chain Management.
1. Geef op het sneltabblad **Op de achtergrond uitvoeren** aan of de taak in de batchmodus moet worden uitgevoerd en/of stel een terugkerend schema in. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK**. Regels worden gemaakt voor de dimensies die voorraadtransacties hebben.

#### <a name="manually-add-or-remove-journal-lines"></a>Journaalregels handmatig toevoegen of verwijderen

U kunt journaalregels op elk moment handmatig toevoegen en/of verwijderen (na of in plaats van automatisch regels te genereren). Gebruik de volgende knoppen op de werkbalk van het sneltabblad **Journaalregels**:

- **Nieuw**: voeg een nieuwe regel toe. Voer vervolgens een waarde in elke kolom in om het product te definiëren waarvoor u een nieuwe minimum wilt berekenen en toepassen. Aangezien voorgestelde minimumberekeningen niet beschikbaar zijn voor handmatig toegevoegde regels, worden er geen nieuwe waarden voor **Berekende minimumhoeveelheid** voor de regels weergegeven. Daarom moet u de waarden voor de **Nieuwe minimumhoeveelheid** handmatig invoeren. U kunt echter nog steeds de mogelijke impact bekijken van de waarde van **Nieuwe minimumhoeveelheid** op de voorraadwaarde en de mogelijke wijziging in de voorraad vergeleken met het opgegeven minimum.
- **Verwijderen**: verwijder de geselecteerde regel.
- **Journaalregels verwijderen**: verwijder alle regels in het journaal.

### <a name="calculate-a-proposal"></a>Een voorstel berekenen

Met deze stap berekent u een voorgesteld minimum voor elke journaalregel en de mogelijke invloed van de regel op de voorraadwaarde. (Het voorgestelde minimum wordt weergegeven als de waarde **Berekende minimumhoeveelheid**.) U kunt de berekening indien nodig meerdere keren uitvoeren. Met de berekening wordt de waarde **Berekende minimumhoeveelheid** bijgewerkt die voor alle journaalregels wordt weergegeven.

De berekeningen die worden weergegeven, hebben geen invloed op de werkelijke waarden voor minimumhoeveelheid voor elk product totdat u **Boeken** in het actievenster selecteert. Op dat moment worden de waarden voor **Nieuwe minimumhoeveelheid** toegepast op elk product.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Berekening veiligheidsvoorraad**.
1. Open het journaal waarvoor u een voorstel wilt berekenen. U kunt ook een nieuw journaal maken zoals eerder in dit onderwerp is beschreven.
1. Selecteer op het sneltabblad **Journaalregels** **Voorstel berekenen** op de werkbalk. (U hoeft geen regels te selecteren.)
1. Stel de volgende velden in het dialoogvenster **Voorstel berekenen voor minimumvoorraadniveau** in:

    - **Gemiddelde uitgifte tijdens doorlooptijd gebruiken**: selecteer deze optie om waarden voor **Berekende minimumhoeveelheid** te genereren op basis van de gemiddelde uitgifte gedurende de opgegeven periode. Voer vervolgens in het veld **Vermenigvuldigingsfactor** een waarde in om het resultaat zo nodig aan te passen. Voer bijvoorbeeld *1,0* in om het exacte berekende gemiddelde te gebruiken of *1,1* om een extra buffer van 10 procent toe te voegen.
    - **Serviceniveau gebruiken**: selecteer deze optie om een voorgesteld minimum te berekenen op basis van het gewenste serviceniveau. Selecteer vervolgens uw voorkeursserviceniveau in het veld **Serviceniveau**.
    - **Marge doorlooptijd**: voer een waarde in waarmee de normale doorlooptijd moet worden verlengd (bijvoorbeeld voor administratie).
    - **De berekende minimumhoeveelheid gebruiken als nieuwe minimumhoeveelheid**: stel deze optie in op *Ja* om automatisch waarden te kopiëren van de kolom **Berekende minimumhoeveelheid** naar de kolom **Nieuwe minimumhoeveelheid** voor alle regels nadat de berekening is voltooid. Als u deze optie op *Nee* instelt, wordt de waarde voor **Huidige minimumhoeveelheid** gekopieerd naar de kolom **Nieuwe minimumhoeveelheid** voor alle regels. U moet vervolgens de waarden voor **Nieuwe minimumhoeveelheid** indien nodig handmatig bewerken.

1. Geef op het sneltabblad **Op de achtergrond uitvoeren** aan of de taak in de batchmodus moet worden uitgevoerd en/of stel een terugkerend schema in. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK**. De resultaten van de berekening worden weergegeven in de kolom **Berekende minimumhoeveelheid** op het sneltabblad **Journaalregels**. Op dit moment zijn de waarden alleen voorgestelde waarden die nog niet op uw producten zijn toegepast.

### <a name="update-minimum-quantity"></a>Minimumhoeveelheid bijwerken

U kunt elke regel in een veiligheidsvoorraadjournaal selecteren en de waarde van het bijbehorende veld **Nieuwe minimumhoeveelheid** handmatig overschrijven.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Berekening veiligheidsvoorraad**.
1. Open het journaal dat u wilt bewerken. U kunt ook een nieuw journaal maken zoals eerder in dit onderwerp is beschreven.
1. Zoek op het sneltabblad **Journaalregels** naar de regel die u wilt aanpassen en bewerk vervolgens de waarde in de kolom **Nieuwe minimumhoeveelheid**. U kunt bijvoorbeeld de waarde voor **Nieuwe minimumhoeveelheid** zo instellen dat deze overeenkomt met de waarde van **Berekende minimumhoeveelheid**. Als de waarde van **Berekende minimumhoeveelheid** *0* (nul) is, kunt u de gewenste toekomstige waarde invoeren.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>De nieuwe minimumhoeveelheid boeken en het resultaat valideren

Voer de volgende stappen uit om de nieuwe minimumhoeveelheid te boeken en het resultaat te valideren.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Berekening veiligheidsvoorraad**.
1. Open het journaal waarvoor u nieuwe minimumhoeveelheden wilt boeken. U kunt ook een nieuw journaal maken zoals eerder in dit onderwerp is beschreven.
1. Selecteer **Boeken** in het actievenster.
1. Stel in het dialoogvenster **Journaal boeken** het veld **Alle boekingsfouten overboeken naar een nieuw journaal** indien nodig in. Selecteer vervolgens **OK** om het journaal te boeken.
1. Als u de waarde van **Nieuwe minimumhoeveelheid** voor een regel op het sneltabblad **Journaalregels** hebt gewijzigd, kunt u de wijziging bevestigen door de volgende stappen uit te voeren:

    1. Selecteer voor de regel die u hebt bewerkt de koppeling in de kolom **Artikelnummer**.
    1. Selecteer in het dialoogvenster **Productgegevens** de koppeling in het veld **Artikelnummer** om de gerelateerde vrijgegeven productrecord te openen.
    1. Selecteer in het actievenster op het tabblad **Plannen** in de groep **Behoefteplanning** de optie **Artikelbehoefteplanning**.
    1. De waarde van **Minimum** voor de locatie en het magazijn die u hebt gecorrigeerd met het geboekte veiligheidsvoorraadjournaal is nu bijgewerkt zodat dit overeenkomt met de bewerking.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Afhandeling van veiligheidsvoorraad voor artikelen](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
