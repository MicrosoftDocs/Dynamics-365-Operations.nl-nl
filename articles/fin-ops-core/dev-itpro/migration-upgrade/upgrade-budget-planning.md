---
title: Budgetplanning bijwerken
description: In dit artikel wordt uitgelegd wat opnieuw moet worden geconfigureerd en worden tevens nieuwe functies beschreven die moeten worden overwogen nadat de upgrade is voltooid.
author: panolte
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: panolte
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7d8d59def24fd138b4cf1d36e286b786e13b096e
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124023"
---
# <a name="upgrade-budget-planning"></a>Budgetplanning bijwerken

[!include [banner](../includes/banner.md)]

Er zijn belangrijke verschillen in de budgetplanning tussen Microsoft Dynamics AX 2012 en Dynamics 365 Finance. Sommige functies zijn niet bijgewerkt en moeten derhalve opnieuw worden geconfigureerd. In dit artikel wordt uitgelegd wat opnieuw moet worden geconfigureerd en worden tevens nieuwe functies beschreven die moeten worden overwogen nadat de upgrade is voltooid.  

Budgetplanning in Finance heeft veel verbeteringen die niet beschikbaar waren Dynamics AX 2012. In dit artikel worden de wijzigingen uitgelegd die klanten moeten uitvoeren bij een upgrade. Ook wordt verwezen naar de nieuwe functies die in overweging moeten worden genomen in het upgradeproces. Vanwege de omvang van de wijzigingen kunnen eventuele bestaande budgetplannen pas worden geopend nadat de wijzigingen zijn doorgevoerd die in dit artikel worden beschreven. Rapporten moeten echter blijven werken en mogen geen extra wijzigingen vereisen.

## <a name="overview-of-changes"></a>Overzicht van wijzigingen
Er zijn veel belangrijke wijzigingen aangebracht in budgettering van apps voor financiën en bedrijfsactiviteiten. Deze wijzigingen zijn bedoeld om ervoor te zorgen dat budgetplanning gemakkelijker te configureren en bruikbaarder wordt, zodat onderhoud en instelling van jaar tot jaar afnemen. De volgende gebieden in AX 2012 bestaan niet langer in Finance:

-   Budgetplansjablonen (budgetplanningsconfiguratie)
-   Budgetplanmappen (budgetplanningsconfiguratie)
-   Scenariobeperkingen (budgetplanningsconfiguratie)
-   Sjablonen voor regels en sjablonen voor budgetplanningsfasen (budgetplanningsproces)
-   Matrixvelden voor werkbladsjablonen
-   Microsoft Excel-sjabloonwizard voor budgetplan

Sommige nieuwe concepten kunnen niet rechtstreeks worden bijgewerkt vanuit de eerdere functionaliteit. Daarom moet u bepaalde onderdelen opnieuw configureren om te kunnen voorzien in deze nieuwe concepten. In de volgende secties worden de concepten beschreven die de items in de bovenstaande lijst hebben vervangen.

### <a name="columns"></a>Kolommen

Kolommen zijn een nieuw concept dat delen van de Excel-sjabloon en ook matrixvelden vervangt. Kolommen kunnen een periode, maand, kwartaal, jaar of alle tijd vertegenwoordigen. De tijdsverwijzing is dynamisch. Zij verwijst naar een relatieve periode of jaar in verband met het budgetproces. Zo verwijst bijvoorbeeld een kolom **Vorig jaar januari** naar boekperiode 1 voor jaar -1. Een kolom is specifiek voor een budgetplanscenario, zoals werkelijke waarden of budgetaanvraag.

### <a name="layouts"></a>Indelingen

Indelingen zijn een nieuw concept ter vervanging van de Excel-sjabloon. Indelingen bevatten de kolommen die definiëren welke budgetgegevens of werkelijke waarden en perioden moeten worden weergegeven. Indelingen worden ook gedeeld tussen de client en de Excel-invoegtoepassing. Daarom is de gebruikerservaring bij het invoeren of weergeven van gegevens in de client voor financiën en bedrijfsactiviteiten beter dan de gebruikerservaring in AX 2012. Als u gegevens wilt invoeren in de client van Finance, bent u niet langer beperkt tot het weergeven en invoeren van een enkel scenario in een transactieweergave. In plaats daarvan kunt u met een vergelijkingsweergave op eenvoudige wijze bedragen bekijken en invoeren voor meerdere perioden en rekeningen tegelijk. Ook kunnen indelingen worden gedefinieerd zodat u valuta, opmerkingen en andere optionele gegevens kunt invoeren en weergeven. Via indelingen kunt u definiëren welke grootboekdimensies en beschrijvingen van dimensies moeten worden weergegeven. Indelingen kunnen ook scenariobeperkingen bevatten om te bepalen welke kolommen in een sjabloon kunnen worden bewerkt en welke kolommen beschikbaar moeten zijn in Excel. Nadat u een indeling hebt gedefinieerd, wordt hiervoor een sjabloon gegenereerd. Deze sjabloon maakt op zijn beurt de bijbehorende Excel-sjabloon. Vervolgens kunt u de Excel-sjabloon bewerken om meer formules en opmaak op te nemen en deze vervolgens opnieuw uploaden. Indelingen worden vervolgens toegewezen aan elke faseregel op de pagina **Budgetplanningsproces**. Daarom vervangen de indelingen sjablonen, die op een vergelijkbare manier werden toegewezen en gebruikt.

### <a name="budget-planning-processes"></a>Budgetplanningsprocessen

Budgetplanningsprocessen zijn meestal hetzelfde als in AX 2012. De belangrijkste wijziging is de vervanging van sjablonen door indelingen. Als eerder processen werden voltooid in AX 2012, worden de processen nu bijgewerkt naar een status In uitvoering, zodat wijzigingen kunnen worden aangebracht. U moet indelingen toewijzen voor elke faseregel om te bepalen welke scenario's en tijdsperioden worden weergegeven wanneer het plan wordt geopend in de client. De indelingen bepalen ook welke Excel-sjabloon wordt geopend buiten Dynamic 365 for Finance zodat u het budget kunt weergeven. **Standaardrekeningstructuur** is een nieuw verplicht veld voor het budgetplanningsproces. Wijs voor elk budgetplanningsproces de primaire rekeningstructuur toe die moet worden gebruikt voor budgettering.

### <a name="attachments"></a>Bijlagen

In AX 2012 werden redendocumenten opgeslagen in een bijlagemap. Er vindt geen upgrade van eerdere redendocumenten plaats. Redendocumenten worden nu opgeslagen in de database. Als deze informatie moet worden opgeslagen in de bijgewerkte versie, kunt u definitieve redendocumenten voor elk plan uploaden als bijlage met de knop **Reden** in het actievenster. In AX 2012 werden voor elk budgetplan Excel-werkbladen gemaakt op basis van de sjabloon. In Finance wordt in alle plannen een kopie van de indeling geopend. Er worden echter geen wijzigingen in het Excel-bestand opgeslagen. Eventuele formules of ondersteunende gegevens die werden gebruikt op planbasis moeten worden toegevoegd via opmerkingen, een redendocument of een ander aanvullend proces.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>Een bijgewerkte omgeving configureren vanuit AX 2012
Om te helpen bepalen hoe het bijgewerkte systeem moet worden geconfigureerd, wordt in het volgende voorbeeld een bijgewerkt budgetproces uit de demogegevens voor AX 2012 gebruikt. Er zijn standaardconfiguratiegegevens voor kolommen gemaakt om te helpen met het upgradeproces. U kunt deze standaardgegevens bijwerken of verwijderen als zij niet voldoen aan uw configuratievereisten. **Opmerking:** er zijn nieuwe vereiste velden die niet worden ingesteld in het systeem. Als u vast komt te zitten op een pagina, zoals de pagina **Budgetplanningsconfiguratie** en niet weg kunt navigeren, kunt u uw browser sluiten en vervolgens opnieuw openen op een andere pagina om gegevens in de juiste volgorde in te voeren. Er zijn vereiste velden die nog niet zijn ingesteld. Daarom kunnen zich problemen voordoen totdat alles is geconfigureerd en alle vereiste velden zijn ingesteld. In dit artikel wordt uitgelegd hoe deze velden indien vereist instelt. Dit zijn enkele van deze vereiste velden:

-   Pagina **Budgetplanningsproces**: veld **Standaardrekeningstructuur**
-   Pagina **Budgetplanningsproces**: veld **Indeling** op het sneltabblad **Faseregels en indelingen van budgetplanning**

### <a name="define-columns-and-layouts"></a>Kolommen en indelingen definiëren

1. Klik op de pagina **Configuratie budgetplanning** op het tabblad **Kolommen**. Als onderdeel van de upgrade worden automatisch nieuwe kolommen gemaakt op basis van uw budgetplanregels. Kolommen maken nu gebruik van dynamische datums, waarbij de tijd en het jaar worden afgezet tegen het fiscaal jaar dat is gedefinieerd in het budgetplanningsproces. **Opmerking:** om prestatieredenen tijdens de upgrade wordt ervan uitgegaan dat alle budgetcycli kalenderjaren en geen fiscale jaren vertegenwoordigen. Als u fiscale jaren gebruikt, moet u bewerkingen doorvoeren om de kolommen op correcte wijze toe te wijzen aan hun fiscale jaar. Zo bestonden bijvoorbeeld de volgende elementen in AX 2012:
   -   Budgetplanscenario's: werkelijke waarden, basislijn, budgetaanvraag, goedgekeurd budget
   -   Budgetplanregels voor alle scenario's in 2017 en werkelijke waarden voor zowel 2017 als 2016

   De volgende kolommen worden gemaakt in apps voor financiën en bedrijfsactiviteiten:

   | Kolomnaam    | Budgetplanscenario | Kolomperiode | Jaargrens |
   |----------------|----------------------|--------------------|-------------|
   | Jan Scenario 1 | Werkelijke kosten              | 1                  | 0           |
   | Jan Scenario 2 | Basislijn             | 1                  | 0           |
   | Jan Scenario 3 | Budgetaanvraag       | 1                  | 0           |
   | Jan Scenario 4 | Budget goedgekeurd      | 1                  | 0           |
   | Jan Scenario 5 | Werkelijke kosten              | 1                  | -1          |
   | Feb Scenario 1 | Werkelijke kosten              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   In dit voorbeeld wordt een kolom met de naam **Jan Scenario 1** gemaakt voor de meest recente transactiegegevens voor budgetplanning die zijn gevonden waar transacties bestaan in januari. Een soortgelijke kolom wordt gemaakt voor elk scenario dat gegevens bevat. Zodra kolommen bestaan voor alle perioden in dat jaar, worden kolommen gemaakt voor voorgaande jaren.
2. Wijzig de kolomnamen en -beschrijvingen en eventuele andere gegevens handmatig in de client of via bulkupdates met de Excel-invoegtoepassing die wijst naar de gegevensentiteit voor budgetplankolommen. Alle filters die eerder zijn ingesteld voor matrixvelden worden nu ingesteld binnen de kolommen.
3. Maak een nieuwe indeling voor een budgetplan. Een indeling verwijst naar meerdere kolommen voor het definiëren van de weergave die wordt weergegeven in Excel en de client. De indeling vereist eerst dat u een grootboekdimensieset opgeeft om te bepalen welke financiële dimensies kunnen worden ingevoerd. Nadat u de dimensieset hebt opgegeven, klikt u op **Beschrijvingen** om beschrijvingen te selecteren van de dimensies die moeten worden opgenomen in de indeling.
4. Klik op het sneltabblad **Indelingselementen** op **Toevoegen** om metagegevens toe te voegen voor elke rij, zoals een valuta, een opmerking of een budgetklasse waarmee omzet- met onkostenrijen worden vergeleken. Voeg vervolgens kolommen toe voor de tijdsperiode en scenario's die van toepassing zijn op deze budgetcyclus en fase. U kunt deze wijzigingen handmatig doorvoeren in de client of via de Excel-invoegtoepassing die naar de gegevensentiteit voor indelingselementen van het budgetplan verwijst.
5. Selecteer voor elk indelingselement of de kolom bewerkbaar moet zijn en of de kolom ook moet worden weergegeven in de Excel-werkmap voor deze indeling. **Opmerking:** voor onze historische plannen wilt u mogelijk een indeling in overweging nemen waarin 12 maandelijkse kolommen worden weergegeven voor elk budgetplanscenario voor dat proces.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Budgetplanningsprocessen bijwerken voor het gebruik van de juiste indeling voor elke budgetfase

1.  Selecteer op de pagina **Budgetplanningsproces** het proces dat u wilt configureren.
2.  Klik in het actievenster op **Bewerken**.
3.  Geef de standaardrekeningstructuur op voor dit budgetproces. **Standaardrekeningstructuur** is een nieuw vereist veld dat moet worden ingesteld.
4.  Selecteer op het sneltabblad **Faseregels en indelingen van budgetplanning** in het veld **Indeling** een indeling die eerder is geconfigureerd en die geschikt is voor deze fase.
5.  Ga door met het selecteren van de dezelfde of andere indelingen voor de verschillende budgetplanningsfasen en sla vervolgens uw wijzigingen op.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Extra functies om rekening mee te houden in uw budgetteringsproces
### <a name="budget-planning-workspace"></a>Werkgebied voor budgetplanning

Dit werkgebied is ontworpen voor zowel de budgeteigenaar als voor afzonderlijke medewerkers die bijdragen aan het budget. Het bevat koppelingen naar budgetdocumenten die uw aandacht vereisen. Het bevat tevens rapporten en key performance indicators (KPI's) voor het budgetproces. De budgetbeheerder kan het huidige budgetplanningsproces voor alle gebruikers definiëren op de pagina **Budgetteringsparameters**. Op het tabblad **Werkgebiedinstellingen** bevat het sneltabblad **Budgetplanning** een veld waarin u het budgetplanningsproces kunt selecteren.

### <a name="alternate-layouts"></a>Alternatieve indelingen

Alternatieve indelingen zijn een nieuwe functie waarmee u plannen in verschillende indelingen kunt weergeven. Een of meer indelingen kunnen als opties worden geleverd. U kunt vervolgens een budgetplan bekijken in een maandelijkse indeling of een kwartaalindeling. U definieert alternatieve indelingen op het sneltabblad **Faseregels en indelingen van budgetplanning** op de pagina **Budgetplanningsproces**.

### <a name="budget-milestones"></a>Budgetmijlpalen

Als onderdeel van het budgetproces is het essentieel dat u belangrijke datums en deadlines begrijpt. U kunt nu datums configureren zodat deze omschrijvingen hebben. Budgetteringsgebruikers zien deze beschrijvingen als zij budgetten openen om items die aan hen zijn toegewezen te bewerken of weer te geven.

### <a name="copy-from-budget-plan-allocation"></a>Kopiëren vanuit budgetplantoewijzing

Via een nieuwe toewijzingsmethode kunt u distribueren vanuit een bovenliggend plan naar een onderliggend plan zonder via een tussenliggend niveau in de hiërarchie te hoeven gaan. Deze methode is vooral handig voor klanten die eerder een financiële dimensie voor budgetdistributie en -goedkeuringen hebben gemaakt.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Budgetplannen genereren vanuit nieuwe budgetbronnen

De volgende opties zijn toegevoegd als periodieke processen. Met deze opties kunt u een budgetplan genereren door bestaande gegevens uit een andere module als uitgangspunt te nemen:

-   Budgetplan genereren op basis van vraagprognose
-   Budgetplan genereren op basis van aanbodprognose
-   Budgetplan genereren op basis van project
-   Budgetplan genereren op basis van budgetregister

### <a name="more-complete-tracking-of-amounts"></a>Gedetailleerdere tracering van bedragen

In AX 2012 had budgetplanning een enkel planbedrag dat werd opgeslagen voor elke waarde. In Finance is het gegevensmodel uitgebreid. Er zijn nu bedragen in valuta voor boekhouding, transactievaluta en aangiftevaluta voor elke waarde. Tijdens de upgrade worden deze nieuwe kolommen automatisch ingevuld voor bestaande gegevens.

### <a name="do-not-convert-currency-in-aggregation"></a>Valuta niet converteren in aggregatie

Normaal gesproken worden, wanneer een onderliggend plan wordt samengevoegd op een bovenliggend niveau, de bedragen automatisch omgezet van de transactievaluta naar de valuta voor boekhouding voor de organisatie. Als u de optie **Valuta niet converteren in aggregatie** instelt op **Nee**, blijven de samengevoegde bedragen in de oorspronkelijke valuta. Daarom staat deze nauwkeurigere correcties toe die worden beïnvloed door wisselkoersfluctuaties.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Terugkijken vanuit een budgetplan naar andere modules die hebben bijgedragen aan het budget

Budgetplannen kunnen worden gegenereerd op basis van vraag- of aanbodprognoses, project en andere gebieden. De query Budgetplannen per dimensieset bevat meerdere opties waarmee u query's kunt uitvoeren om de gegevens te identificeren die bron voor het budgetplan vormden.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Overschrijven of toevoegen om te plannen voor toewijzingsplanningen

Als er meerdere bronnen zijn voor bedragen die moeten worden gedistribueerd, kunt u opgeven dat de bedragen additief moeten zijn. In dat geval overschrijven de bedragen geen bestaande bedragen. In plaats daarvan worden ze toegevoegd aan de bestaande bedragen.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Standaard financiële dimensieset voor budgetplanningsconfiguratie

De pagina **Budgetplanningsconfiguratie** bevat nu een veld waarin u de standaard financiële dimensieset kunt opgeven. Hoewel dit veld een optioneel veld is, is het mogelijk vereist voor bepaalde query's. Het kan ook zijn vereist als u rapporten gegroepeerd op dimensieset wilt groeperen of filteren.

### <a name="data-entities"></a>Gegevensentiteiten

Verscheidene gegevensentiteiten zijn toegevoegd om snelle implementatie van de budgetplanning mogelijk te maken. De entiteiten stellen u tevens in staat vele wijzigingen door te voeren via Excel. U hoeft daarom niet items één voor één te maken via de client. Hier volgt een lijst van de nieuwe gegevensentiteiten:

-   Naam entiteit
-   Budgetparameters
-   Budgetplanparameter
-   Budgetplanscenario's
-   Fasen van budgetplan
-   Workflowfase van budgetplan
-   Toewijzingschema's van budgetplan
-   Toewijzingen van budgetplanfase
-   Prioriteiten budgetplan
-   Budgetplankolommen
-   Indelingselementen van budgetplan






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
