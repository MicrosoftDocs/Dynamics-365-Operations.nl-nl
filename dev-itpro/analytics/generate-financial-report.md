---
title: Een financieel rapport maken
description: Dit onderwerp biedt informatie over het genereren van een financieel rapport.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="generate-a-financial-report"></a>Een financieel rapport maken

[!include[banner](../includes/banner.md)]


Dit onderwerp biedt informatie over het genereren van een financieel rapport. 

Om een rapport te genereren, open de rapportdefinitie en klik vervolgens op de knop Genereren in de werkbalk. Het venster De Status van de rapportwachtrij wordt geopend en geeft de locatie van uw rapport in de wachtrij aan. Standaard, wordt het gegenereerde rapport in de Webkijker geopend.
| ![Opmerking](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Opmerking")**Opmerking**        |
|------------------------------------------------------------------------------------------------|
| U kunt rapporten alleen genereren naar mappen en locaties waarvoor u gemachtigd bent voor toegang. |

De volgende tabel beschrijft de opties die beschikbaar zijn voor het genereren van rapporten.

| Optie                                                                                | Meer informatie |
|---------------------------------------------------------------------------------------|----------------------|
| Een planning instellen om een rapport of groep rapporten automatisch te genereren              |                      |
| De controle voor ontbrekende rekeningen of gegevens in een rapport, en valideert de nauwkeurigheid van een rapport |                      |

Wanneer u een rapport genereert, worden de opties gebruikt die u op de tabbladen Rapportdefinitie hebt opgegeven. Het tabblad Uitvoer en Distributie laat u een rapportbibliotheeklocatie opgeven, waarmee u op eenvoudige wijze het rapport kunt delen.

## <a name="schedule-report-generation"></a>Planning rapport genereren
Veel bedrijven hebben een kernset van rapporten die met geplande intervallen worden uitgevoerd om met hun bedrijfsprocessen af te stemmen. U kunt een rapport plannen om regelmatig worden gegenereerd, bijvoorbeeld dagelijks, wekelijks, maandelijks, of jaarlijks. Dit kan één rapport of een groep rapporten zijn met meerdere bedrijven. U moet uw gebruikergegevens voor elk van de bedrijven die zijn gespecificeerd invoeren, zoals deze in een rapporteringsstructuurdefinitie. Als de gebruikersgegevens niet geldig zijn wordt in het rapport alleen de informatie waar u voor gemachtigd bent weergegeven, zoals het bedrijf waar u op dat moment bent aangemeld. De uitvoer informatie wordt eerst gelezen uit de rapportgroep, en vervolgens uit de afzonderlijke rapporten.

Als rapportplanning worden gemaakt en opgeslagen, worden deze weergegeven in het navigatievenster onder Rapportplanning. U kunt mappen maken om de rapporten te organiseren. Als één rapport in een planning niet wordt uitgevoerd, zullen alle andere rapporten blijven draaien.
| ![Belangrijk](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Belangrijk")**Belangrijk**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Om rapportplanning te maken, te wijzigen en te verwijderen, moet u de rol van ontwerper of beheerder hebben. Wanneer een rapport wordt uitgevoerd, worden de gebruikersgegevens van de gebruiker die het plan maakte gebruikt om het rapport te genereren. |

### <a name="create-a-report-schedule"></a>Een rapportplanning maken.

1.  In Report Designer, op het Bestand menu, klik Nieuw, en selecteer Rapportplan. Het dialoogvenster Nieuwe Rapportplanning wordt geopend.
2.  Onder Instellingen, selecteer een afzonderlijk rapport of een rapportgroep voor de planning. Alleen de rapporten of de rapportgroepen voor het bedrijf of bouwsteenselectie waar u momenteel bent aangemeld zijn beschikbaar.
3.  Selecteer het Actief selectievakje in om de rapportplanning in te schakelen. Alleen de maker van het rapport of beheerder kan een rapportplanning activeren of deactiveren.
4.  Klik op de Machtigingen knop om bedrijfreferenties in te voeren. Standaard, wordt uw aanmeldingsinformatie gebruikt voor het bedrijf waarbij u bent aangemeld. Als andere bedrijven zijn inbegrepen, zoals in rapporteringsstructuurdefinities, selecteer Afzonderlijke gebruikersgegevens gebruiken en voer vervolgens de gebruikersgegevens in voor elk ander bedrijf in dat in de rapportplanning is opgenomen. U kunt Windows-Verificatie selecteren of een gebruikersnaam en wachtwoord voor elk bedrijf typen. Selecteer het selectievakje om Sla referenties om de gebruikergegevens voor deze bedrijven op te slaan, en klik vervolgens OK om het dialoogvenster te sluiten.
5.  Onder Frequentie, in het veld Beginherhaling, selecteer de datum wanneer de planning moet beginnen. Standaard wordt de huidige systeemdatum van de clientcomputer geselecteerd.
6.  In het veld Draai rapport op, de tijd waarop het rapport moet worden uitgevoerd. Als u een tijd invoert die voor de huidige systeemtijd is, wordt het rapport op de volgende geplande datum.
7.  In het Herhalingspatroon gebied, opgeven hoe dikwijls het rapport wordt uitgevoerd. Standaard is Dagelijks geselecteerd met een waarde voor Interval (dagen) van 1. Overige opties zijn Wekelijks, Maandelijks of Jaarlijks.
8.  In het Bereik van herhaling gebied, selecteer wanneer het rapport niet meer moet worden gegenereerd.
    -   Geen einddatum - De rapportplanning draait voor onbepaalde tijd.
    -   Stel het aantal voorkomens in - De rapportplanning draait voor het opgegeven aantal keer, en wordt vervolgens uitgeschakeld.
    -   Beëindigen voor - De rapportplanning eindigt op de opgegeven datum.

9.  Klik op Oplsaan in de werkbalk. Geef in het dialoogvenster Opslaan als een unieke naam en beschrijving op voor de rapportplanning.

Om rapportplanning te kopieeren moet u de rol van ontwerper of beheerder hebben. Zelfs als een beheerder het rapportplan wijzigt, behoudt het rapport de referenties van de gebruiker die het rapport heeft gemaakt.
### <a name="copy-a-report-schedule"></a>Een rapportplanning kopiëren.

1.  In Report Designer, klik op Rapportplannen in het navigatievenster, en open een rapportplan om te kopiëren.
2.  In het Bestand menu, klik op Opslaan als, en voer vervolgens een nieuwe naam en omschrijving voor het plan in het Opslaan als dialoogvenster in. Klik op OK, en de nieuwe planning worden weergegeven in het navigatievenster.
3.  In het nieuwe schema, wijzigt u de velden en informatie als nodig, en klik vervolgens Opslaan op de werkbalk, of klik Opslaan op het Bestand menu.

Om een rapportplan te verwijderen, moet u de eigenaar van het rapportplan zijn of rol van beheerder hebben.
### <a name="delete-a-report-schedule"></a>Verwijder een rapportplanning.

1.  Klik in Report Designer in het navigatievenster op Rapportgroepen.
2.  Selecteer vervolgens het te verwijderen rapportplan, klik op Verwijderen of druk op de toets Verwijderen.
3.  In het dialoogvenster voor de verwijderingsverificatie, klik Ja rapportplan definitief om te verwijderen. Als u geen machtigingen hebt om de planning te verwijderen, wordt een bericht weergegeven en het rapport wordt niet verwijderd.

### <a name="credentials-and-report-schedules"></a>Referenties en rapportplannen

Als u geen referenties invoert die voor alle bedrijven opgenomen in de rapporten worden vereist, ontvangt u het volgende bericht wanneer u op het rapportplan: "U moet uw referenties bedrijven voor de invoeren die in dit rapportplan bevat. Selecteer de Machtigingen knop om uw referenties in te voeren.

Bijvoorbeeld, Phyllis meldt zich aan bij Bedrijf A met aan haar gebruikersnaam en wachtwoord. Ze maakt een planning voor een rapport dat een rapporteringsstructuurdefinitie gebruikt om gegevens uit meerdere bedrijven te verzamelen. Wanneer dit rapport het plan wordt opgeslagen, wordt Phyllis gevraagd de referenties voor de andere bedrijven in te voeren die in de rapporteringsstructuurdefinitie worden opgegeven. Wanneer uw referenties verlopen, dan worden de betrokken rapporten in de rapportplanning niet gegenereerd tot de referenties zijn bijgewerkt. Een bericht wordt weergegeven in de rapportwachtrij om aan te geven dat de machtigingen moeten worden bijgewerkt. Het rapport het plan mislukt als een van de volgende scenario's (omdat deze referenties vereisen) plaatsvind:
-   Een nieuw bedrijf is toegevoegd aan een rapportstructuur voor een individueel rapport.
-   Een rapport in een rapportgroep is gewijzigd.
-   Een nieuw rapport voor een nieuw bedrijf is toegevoegd aan een rapportgroep.

Om door te gaan, klik op de knop Machtigingen in het dialoogvenster Rapportplanning, en voer vervolgens de juiste referenties in.

## <a name="missing-account-analysis-feature"></a>Ontbrekende rekeninganalyse functie
U kunt voor financiële rekeningen en dimensies zoeken die kunnen missen van alle rijdefinities, rapporteringsstructuurdefinities, en rapportdefinities in een bouwsteengroep. Dit is handig wanneer u verschillende rekening of bouwstenen maakt of bijwerkt gedurende een korte periode, en u wilt controleren of alle nieuwe informatie in uw rapporten is opgenomen.

Er worden ontbrekende rekeningen bepaald door de laagste en hoogste waarden te gebruiken van de rijdefinitie of rapporteringsstructuurdefinitie, waarna een lijst wordt weergegeven met rekeningen die zich niet in de rijdefinitie of rapporteringsstructuurdefinitie bevinden, maar wel in de financiële gegevens. Als een ontbrekende rekening groter is dan of kleiner is dan de waarden in de rijdefinitie, is die rekening niet opgenomen in de lijst van ontbrekende rekeningen.
| ![Tip](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Tip")**Tip**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Voor validatiedoeleinden, moet dit proces worden uitgevoerd voordat u maandelijkse rapporten genereert en wanneer u nieuwe bouwstenen maakt. |

Rapporten die waardebereiken hebben minder kans om ontbrekende rekeningen te hebben. Wanneer mogelijk, gebruik bereiken in de bouwsteen om nieuwe rekeningen te omvatten wanneer deze worden gemaakt. Als er een rapportdefinitie is ingesteld op @ANY bedrijf, dan kunt u zich bij een specifiek bedrijf aanmelden en een ontbrekende rekeninganalyse voor dat bedrijf uitvoeren.
| ![Opmerking](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Opmerking")**Opmerking**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Als een nieuw bedrijf is toegevoegd, moet u het nieuwe bedrijf aan de rapportagestructuren in eventuele bestaande rapporten toevoegen of het bedrijf zal niet opgenomen worden in de ontbrekende rekeninganalyse. |

### <a name="run-missing-account-analysis"></a>Draai ontbrekende rekeninganalyse

1.  In Report Designer, klik Extra, en klik dan op Ontbrekende Rekeninganalyse.
2.  In het veld Bedrijf-filter, een bedrijf selecteren om resultaten te filteren, of selecteer Alle (geen filter) om all resultaten van alle beschikbare bedrijven weer te geven.
3.  In het veld Dimensiefilter, selecteer een dimensie om resultaten te filteren, of selecteer Alle (geen filter) om alle dimensieinformatie voor alle beschikbare dimensies weer te geven.
4.  In het veld Groeperen op, selecteer een optie om de resultaten te sorteren. U kunt de resultaten sorteren op basis van de bouwsteen die wordt beïnvloed, of u kunt de resultaten op dimensie en waardesets sorteren.
5.  Beoordeel de weergegeven resultaten. Wanneer u een item selecteert in het bovenste deelvenster, dan wordt extra informatie over uitzondering weergegeven in het onderste deelvenster. Dit omvat gerelateerde dimensies, waarden, en rapporten.
6.  Om het desbetreffende item te openen, klikt op het gekoppelde pictogram dat in het lijstdeelvenster wordt weergegeven, of met de rechtermuisknop op het item en selecteer Openen Om meerdere artikelen te selecteren, houdt de CTRL ingedrukt terwijl u de artikelen in het onderste deelvenster selecteert.
7.  Als eventuele waarden, bouwstenen, of rapporten worden geretourneerd die niet in de analyse worden opgenomen, klik dan met de rechtermuiskno op het item en selecteer Uitsluiten, of selecteer het Uitsluiten selectievakje naast het item om het artikel uit de lijst te verwijderen. De uitgesloten artikelen niet opgenomen wanneer de lijst wordt vernieuwd. Om meerdere artikelen te selecteren, houdt u de CTRL ingedrukt terwijl u de items in het onderste deelvenster selecteert. Om alle items, inclusief alle resultaten die u eerder selecteerde om van de analyse uit te sluiten, te bekijken selecteert u het Weergeven uitgesloten bouwstenen en waarden selectievakje in, en klik op Vernieuwen.
8.  Klik op Vernieuwen om uitzonderingen te vernieuwen die u hebt geadresseerd. Klik op Ja om volledige vernieuwing van alle resultaten uit te voeren, of klik op Nee om een gedeeltelijke vernieuwing uit te voeren van de geadresseerde items.
    | ![Opmerking](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Opmerking")**Opmerking**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Het formulier automatisch wordt vernieuwd wanneer het opent, tenzij het formulier in de laatste 15 minuten is geopend. |

9.  Wanneer er problemen worden opgelost, klik op OK om het dialoogvenster te sluiten.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Sneltoetsen voor ontbrekende rekeninganalyse
Wanneer u een ontbrekende rekeninganalyse uitvoert, zijn de volgende sneltoetsen beschikbaar.

| Actie                           | Gebruik deze toetsenbordsneltoets |
|--------------------------------------|----------------------------|
| Filteren op bedrijf                    | Alt+C                      |
| Filter op dimensie                  | Alt+D                      |
| Selecteer het veld Groepeer op.            | Alt+G                      |
| Weergeven uitgesloten blokken en waarden      | Alt+S                      |
| Vernieuw resultaten                      | Alt+R                      |
| Sluit de geselecteerde bouwsteen uit  | Alt+X                      |
| Sluit de geselecteerde rijdefinitie uit.  | Ctrl+B                     |
| Sluit de geselecteerde dimensiewaarde uit | Ctrl+D                     |
| Open de geselecteerde rapportdefinitie  | Ctrl+R                     |
| Open de geselecteerde rijdefinitie.     | Ctrl+O                     |

 
<a name="see-also"></a>Zie ook
--------

[Financiële rapportage](financial-reporting-intro.md)

[Interface van Report Designer](report-designer-interface.md)



