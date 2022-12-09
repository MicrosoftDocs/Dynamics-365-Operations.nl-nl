---
title: Financiële rapporten genereren
description: Dit artikel biedt informatie over het genereren van een financieel rapport.
author: jinniew
ms.date: 02/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2f55fe1a23735d8631a5918fa49e08f74eee4d37
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802764"
---
# <a name="generate-financial-reports"></a>Financiële rapporten genereren

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over het genereren van een financieel rapport.

Om een rapport te genereren, opent u de rapportdefinitie en selecteert u **Genereren** op de werkbalk. De pagina **Status rapportwachtrij** wordt geopend en geeft de locatie van uw rapport in de wachtrij aan.

Naarmate het genereren van het rapport vordert, kunnen de volgende statusindicatoren voor rapportwachtrijen worden weergegeven op de pagina **Status rapportwachtrij**.

| Status          | Provincie | Description|
|-----------------|--------|--------------------|
| In wachtrij plaatsen        | Tussentijds |De rapportdefinitie wordt gevalideerd voordat het rapport in de wachtrij voor genereren wordt geplaatst.                    |
| In wachtrij gezet          | Tussentijds | Het rapport wordt toegevoegd aan de wachtrij voor het genereren van het rapport en wacht op verwerking.                      |
| In verwerking      | Tussentijds | Deze status volgt doorgaans op de status **In wachtrij gezet** en gaat meestal over in de status **Definitief** wanneer de verwerking is voltooid.       |
| Naverwerking | Tussentijds | Deze status volgt op de status **In verwerking** en geeft aan dat alle rapportgegevens zijn verzameld, maar dat er afgeleide acties, zoals berekenen en totaliseren, worden uitgevoerd.            |
| Annuleren      | Tussentijds | De rapportage wordt op verzoek van de gebruiker geannuleerd. Deze status is het resultaat van een door de gebruiker aangevraagde annulering voor een rapport met de status **In wachtrij gezet** of In **verwerking**. Het systeem probeert het rapport in de status **Geannuleerd** te zetten, tenzij het systeem al te ver is en het rapport in een andere status moet worden voltooid. |
| Geannuleerd        | Definitief | De verwerking van het rapport is beëindigd, maar niet voltooid vanwege een door de gebruiker aangevraagde stop.            |
| Voltooid       | Definitief | Het rapport is gereed voor gebruik.                      |
| Niet geslaagd          | Definitief | De verwerking van het rapport is beëindigd, maar het rapport is mislukt en moet niet worden gebruikt. |

Standaard, wordt het gegenereerde rapport in de Webkijker geopend. De volgende opties zijn beschikbaar voor het genereren van rapporten:

- Een planning instellen om een rapport of groep rapporten automatisch te genereren
- De controle voor ontbrekende rekeningen of gegevens in een rapport, en valideert de nauwkeurigheid van een rapport

Wanneer u een rapport genereert, worden de opties gebruikt die u op de tabbladen Rapportdefinitie hebt opgegeven.

## <a name="generate-a-financial-report"></a>Een financieel rapport maken

Voor het genereren van een financieel rapport gaat u naar **Grootboek** \> **Query's en rapporten** \> **Financiële rapporten**.

- Selecteer het rapport dat u wilt genereren en selecteer vervolgens **Genereren**.
- Vul het veld **Rapportdatum** in en selecteer **OK**.

Als het rapport is gegenereerd, kan het rapport worden weergeven in de sectie **Rapporten**.

U kunt het rapport **weergeven** of **verwijderen**.

Als u een rapport wilt genereren met **Rapportontwerper**, opent u de rapportdefinitie en selecteer u vervolgens de knop **Genereren** op de werkbalk. Het venster **Status rapportwachtrij** wordt geopend en geeft de locatie van uw rapport in de wachtrij aan. Standaard, wordt het gegenereerde rapport in de Webkijker geopend.

## <a name="report-groups"></a>Rapportgroepen

Rapportgroepen zijn een efficiënte manier om verschillende rapporten tegelijk te genereren. Stel dat u weet dat uw gebruikers aan het einde van de maand acht rapporten per maand genereren. Maak een rapportgroep en selecteer in plaats van **Genereren** voor elk van de acht rapporten in de groep de optie **Genereren** voor de hele rapportgroep, zodat de acht rapporten in één stap worden gegenereerd. Wanneer de rapporten in de geselecteerde rapportgroep zijn gegenereerd, kunt u naar **Financiële rapporten** (**Grootboek > Opvragen en rapporten > Financiële rapporten**) gaan om de afzonderlijke rapporten weer te geven. Voer de volgende stappen uit om een rapportgroep in te stellen:

1. Selecteer **Rapportgroepen** in **Report Designer**. 
2. Selecteer de bestaande rapportdefinities die u in de rapportgroep wilt opnemen. 
3. Selecteer overschrijvende bedrijfs-, detail- en datuminstellingen voor elk van de rapporten die in de groep worden opgenomen.
   Het is raadzaam om voor elk rapport **Bedrijf**, **Periode**, **Jaar** en **Detailniveau** in te stellen. 
4. Sla de rapportgroep op.

## <a name="schedule-report-generation"></a>Het genereren van rapporten plannen
Veel bedrijven hebben een aantal standaardrapporten die op geplande tijdstippen worden uitgevoerd in overeenstemming met hun bedrijfsprocessen. U kunt een rapport plannen om regelmatig worden gegenereerd, bijvoorbeeld dagelijks, wekelijks, maandelijks, of jaarlijks. U kunt één rapport plannen, of een groep rapporten die betrekking hebben op meerdere bedrijven. U moet uw referenties invoeren voor elk bedrijf dat is opgegeven, zoals die in een rapporteringsstructuurdefinitie. Als de gebruikersgegevens niet geldig zijn, wordt in het rapport alleen de informatie waar u voor gemachtigd bent weergegeven, zoals het bedrijf waar u op dat moment bent aangemeld. De uitvoer informatie wordt eerst gelezen uit de rapportgroep, en vervolgens uit de afzonderlijke rapporten.

Als rapportschema's worden gemaakt en opgeslagen, worden deze weergegeven in het navigatievenster onder **Rapportschema's**. U kunt mappen maken om de rapporten overzichtelijk in te delen. Als een rapport in een groep geplande rapporten niet kan worden uitgevoerd, wordt doorgegaan met de overige rapporten.

> [!IMPORTANT]
> U kunt alleen geplande rapporten maken, wijzigen en verwijderen als u beschikt over de rol van ontwerper of beheerder. Wanneer een rapport wordt uitgevoerd, worden de gebruikersgegevens van de gebruiker die het plan maakte gebruikt om het rapport te genereren.

### <a name="create-a-report-schedule"></a>Een rapportplanning maken.

1. Selecteer in **Report Designer** in het menu **Bestand** de optie **Nieuw** en selecteer vervolgens **Rapportschema**. Het dialoogvenster **Nieuw rapportschema** wordt geopend.
2. Selecteer onder **Instellingen** een afzonderlijk rapport of een rapportgroep voor de planning. Alleen rapporten of rapportgroepen voor de selectie bedrijven of bouwstenen waarvoor u momenteel bent aangemeld, zijn beschikbaar.
3. Schakel het selectievakje **Actief** in om de rapportplanning in te schakelen. Alleen de maker (ontwerper) van het rapport of een beheerder kan een rapportplanning in- of uitschakelen.
4. Selecteer de knop **Machtigingen** om bedrijfreferenties in te voeren. Standaard worden uw aanmeldingsgegevens gebruikt voor het bedrijf waarbij u bent aangemeld. Als andere bedrijven zijn inbegrepen, zoals in rapporteringsstructuurdefinities, selecteert u **Afzonderlijke gebruikersgegevens gebruiken** en voert u vervolgens de gebruikersgegevens in voor elk ander bedrijf dat in de rapportplanning is opgenomen. U kunt **Windows-verificatie** selecteren of een gebruikersnaam en wachtwoord voor elk bedrijf typen. Schakel het selectievakje **Referenties opslaan** in om de gebruikergegevens voor deze bedrijven op te slaan en selecteer vervolgens **OK** om het dialoogvenster te sluiten.
5. Selecteer onder **Frequentie**, in het veld **Beginherhaling** de datum wanneer de planning moet ingaan. Standaard wordt de huidige systeemdatum van de clientcomputer geselecteerd.
6. Selecteer in het veld **Rapport uitvoeren op** de tijd waarop het rapport moet worden uitgevoerd. Als u een tijdstip vóór de huidige systeemtijd invoert, wordt het rapport uitgevoerd op de volgende geplande datum.
7. Geef in het gebied **Herhalingspatroon** op hoe dikwijls het rapport wordt uitgevoerd. Standaard is **Dagelijks** geselecteerd met een waarde van **1** voor **Interval (dagen)**. Overige opties zijn **Wekelijks**, **Maandelijks** en **Jaarlijks**.
8. Selecteer in het gebied **Bereik van terugkeerpatroon** wanneer het rapport niet meer moet worden gegenereerd.

    - **Geen einddatum**: de rapportplanning wordt voor onbepaalde tijd uitgevoerd.
    - **Aantal voorvallen**: de rapportplanning wordt het opgegeven aantal keren uitgevoerd en wordt vervolgens uitgeschakeld.
    - **Beëindigen voor**: de rapportplanning eindigt op de opgegeven datum.

9. Selecteer **Opslaan**. Geef in het dialoogvenster **Opslaan als** een unieke naam en beschrijving op voor het rapportschema.

Om rapportplanning te kopieeren moet u de rol van ontwerper of beheerder hebben. Zelfs als een beheerder het rapportplan wijzigt, behoudt het rapport de referenties van de gebruiker die het rapport heeft gemaakt.

### <a name="copy-a-report-schedule"></a>Een rapportplanning kopiëren.

1. Selecteer in Report Designer de optie **Rapportschema's** in het navigatievenster en open een rapportschema om te kopiëren.
2. Selecteer in het menu **Bestand** de optie **Opslaan als** en voer vervolgens een nieuwe naam en beschrijving voor het schema in het dialoogvenster **Opslaan als** in. Selecteer **OK**. De nieuwe planning wordt nu weergegeven in het navigatievenster.
3. Wijzig on het nieuwe schema naar behoefte de velden en informatie en selecteer vervolgens **Opslaan** op de werkbalk of **Opslaan** in het menu **Bestand**.

Om een rapportplan te verwijderen, moet u de eigenaar van het rapportplan zijn of rol van beheerder hebben.

### <a name="delete-a-report-schedule"></a>Verwijder een rapportplanning.

1. Selecteer in Report Designer de optie **Rapportschema's** in het navigatievenster.
2. Selecteer vervolgens het te verwijderen rapportplan en selecteer **Verwijderen** of druk op de toets **Delete**.
3. Selecteer **Ja** in het dialoogvenster voor de verwijderingsverificatie om het rapportplan definitief te verwijderen. Als u geen machtigingen hebt om de planning te verwijderen, wordt een bericht weergegeven en het rapport wordt niet verwijderd.

### <a name="credentials-and-report-schedules"></a>Referenties en rapportschema's

Als u geen referenties invoert die voor alle bedrijven opgenomen in de rapporten worden vereist, ontvangt u het volgende bericht wanneer u op het rapportplan: "U moet uw referenties voor de bedrijven invoeren die dit rapportplan bevat. Selecteer de knop **Machtigingen** om uw referenties in te voeren."

Bijvoorbeeld: een gebruiker meldt zich aan bij bedrijf A met een gebruikersnaam en wachtwoord. De gebruiker maakt een planning voor een rapport dat een rapporteringsstructuurdefinitie gebruikt om gegevens uit meerdere bedrijven te verzamelen. Wanneer Phyllis het rapport opslaat, wordt de gebruiker gevraagd de referenties voor alle overige bedrijven in de rapporteringsstructuurdefinitie op te geven. Wanneer uw referenties verlopen, worden de betrokken rapporten in de rapportplanning pas gegenereerd als de referenties zijn bijgewerkt. Een bericht wordt weergegeven in de rapportwachtrij om aan te geven dat de machtigingen moeten worden bijgewerkt. Het rapport het plan mislukt als een van de volgende scenario's (omdat deze referenties vereisen) plaatsvind:

- Een nieuw bedrijf is toegevoegd aan een rapportstructuur voor een individueel rapport.
- Een rapport in een rapportgroep is gewijzigd.
- Er is een nieuw rapport voor een aanvullend bedrijf toegevoegd aan een rapportgroep.

U kunt doorgaan door de knop **Machtigingen** in het dialoogvenster **Rapportplanning** te selecteren en vervolgens de juiste referenties in te voeren.

## <a name="missing-account-analysis-feature"></a>Analysefunctie ontbrekende rekeningen
U kunt voor financiële rekeningen en dimensies zoeken die kunnen missen van alle rijdefinities, rapporteringsstructuurdefinities, en rapportdefinities in een bouwsteengroep. Dit is handig wanneer u verschillende rekeningen of bouwstenen maakt of bijwerkt gedurende een korte periode, en u wilt controleren of alle nieuwe informatie in uw rapporten is opgenomen.

Er worden ontbrekende rekeningen bepaald door de laagste en hoogste waarden te gebruiken van de rijdefinitie of rapporteringsstructuurdefinitie, waarna een lijst wordt weergegeven met rekeningen die zich niet in de rijdefinitie of rapporteringsstructuurdefinitie bevinden, maar wel in de financiële gegevens. Als een ontbrekende rekening hoger of lager is dan de waarden in de rijdefinitie, wordt deze rekening niet in de lijst met ontbrekende rekeningen opgenomen.

> [!TIP]
> Dit proces moet voor validatiedoeleinden worden uitgevoerd voordat u maandelijkse rapporten genereert en wanneer u nieuwe bouwstenen maakt.

Rapporten die waardebereiken hebben minder kans om ontbrekende rekeningen te hebben. Gebruik zo mogelijk bereiken in de bouwsteen om nieuwe rekeningen te omvatten wanneer deze worden gemaakt. Als een rapportdefinitie is ingesteld op de bedrijfswaarde @ANY, kunt u zich vervolgens aanmelden bij een specifiek bedrijf en een analyse uitvoeren naar ontbrekende rekeningen voor dat bedrijf.

> [!NOTE]
> Als een nieuw bedrijf is toegevoegd, moet u het nieuwe bedrijf aan de rapportagestructuren in eventuele bestaande rapporten toevoegen of het bedrijf zal niet opgenomen worden in de ontbrekende rekeninganalyse.

### <a name="run-missing-account-analysis"></a>Draai ontbrekende rekeninganalyse

1. Selecteer in Report Designer de optie **Extra** en selecteer vervolgens **Ontbrekende rekeninganalyse**.
2. Selecteer in het veld **Bedrijfsfilter** een bedrijf om resultaten te filteren of selecteer **Alle (geen filter)** om alle resultaten van alle beschikbare bedrijven weer te geven.
3. Selecteer in het veld **Dimensiefilter** een dimensie om resultaten te filteren of selecteer **Alle (geen filter)** om alle dimensiegegevens voor alle beschikbare dimensies weer te geven.
4. Selecteer in het veld **Groeperen op** een optie om de resultaten te sorteren. U kunt resultaten sorteren op de bouwsteen waarop deze van invloed zijn of op de dimensie en waardesets.
5. Controleer de weergegeven resultaten. Wanneer u in het bovenste deelvenster een item selecteert, wordt in het onderste deelvenster aanvullende informatie over de uitzondering weergegeven. Dit omvat gerelateerde dimensies, waarden en rapporten.
6. Om het desbetreffende item te openen, selecteert u het gekoppelde pictogram dat in het lijstdeelvenster wordt weergegeven of klikt umet de rechtermuisknop op het item en selecteert u **Openen**. Als u meerdere items wilt selecteren, houdt u de toets **Ctrl** ingedrukt terwijl u de items in het onderste deelvenster selecteert.
7. Als eventuele waarden, bouwstenen, of rapporten worden geretourneerd die niet in de analyse moeten worden opgenomen, klikt u met de rechtermuisknop op het item en selecteert u **Uitsluiten** of schakelt u het selectievakje **Uitsluiten** naast het item in om het artikel uit de lijst te verwijderen. Uitgesloten artikelen worden niet opgenomen wanneer de lijst wordt vernieuwd. Als u meerdere items wilt selecteren, houdt u de toets **Ctrl** ingedrukt terwijl u de items in het onderste deelvenster selecteert. Schakel het selectievakje **Uitgesloten bouwstenen en waarden weergeven** in en selecteer vervolgens **Vernieuwen** als u alle items wilt weergeven, waaronder eventuele items die u eerder hebt uitgesloten van de analyse.
8. Selecteer **Vernieuwen** om uitzonderingen te vernieuwen die u hebt aangepakt. Selecteer **Ja** om volledige vernieuwing van alle resultaten uit te voeren of selecteer **Nee** om een gedeeltelijke vernieuwing uit te voeren van de geadresseerde items.

    > [!NOTE]
    > Het formulier wordt tijdens het openen automatisch vernieuwd, tenzij de pagina in de afgelopen 15 minuten al is geopend.

9. Wanneer er problemen worden opgelost, selecteert u **OK** om het dialoogvenster te sluiten.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Sneltoetsen voor ontbrekende rekeninganalyse
Wanneer u een ontbrekende rekeninganalyse uitvoert, zijn de volgende sneltoetsen beschikbaar.

| Gewenste bewerking                           | Druk op |
|--------------------------------------|----------------------------|
| Filteren op bedrijf                    | Alt+C                      |
| Filteren op dimensie                  | Alt+D                      |
| Het veld Groeperen op            | Alt+G                      |
| Uitgesloten blokken en waarden weergeven      | Alt+S                      |
| Resultaten vernieuwen                      | Alt+R                      |
| De geselecteerde bouwstenen uitsluiten  | Alt+X                      |
| De geselecteerde rijdefinitie uitsluiten  | Ctrl+B                     |
| De geselecteerde dimensiewaarde uitsluiten | Ctrl+D                     |
| De geselecteerde rapportdefinitie uitsluiten  | Ctrl+R                     |
| De geselecteerde rijdefinitie openen     | Ctrl+O                     |


## <a name="additional-resources"></a>Aanvullende resources

[Financiële rapportage](financial-reporting-intro.md)

[De Report Designer-interface](report-designer-interface.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
