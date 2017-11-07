---
title: Een financieel rapport maken
description: Dit onderwerp biedt informatie over het genereren van een financieel rapport.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 01bb8999e5d9c0e16f133a621ebfe1d102565f2f
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

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
Veel bedrijven hebben een kernset van rapporten die met geplande intervallen worden uitgevoerd om met hun bedrijfsprocessen af te stemmen. U kunt een rapport plannen om regelmatig worden gegenereerd, bijvoorbeeld dagelijks, wekelijks, maandelijks, of jaarlijks. U kunt één rapport plannen, of een groep rapporten die betrekking hebben op meerdere bedrijven. U moet uw referenties invoeren voor elk bedrijf dat is opgegeven, zoals die in een rapporteringsstructuurdefinitie. Als de gebruikersgegevens niet geldig zijn wordt in het rapport alleen de informatie waar u voor gemachtigd bent weergegeven, zoals het bedrijf waar u op dat moment bent aangemeld. De uitvoer informatie wordt eerst gelezen uit de rapportgroep, en vervolgens uit de afzonderlijke rapporten.

Als rapportplanning worden gemaakt en opgeslagen, worden deze weergegeven in het navigatievenster onder Rapportplanning. U kunt mappen maken om de rapporten overzichtelijk in te delen. Als één rapport in een planning niet wordt uitgevoerd, zullen alle andere rapporten blijven draaien.
| ![Belangrijk](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Belangrijk")**Belangrijk**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Om rapportplanning te maken, te wijzigen en te verwijderen, moet u de rol van ontwerper of beheerder hebben. Wanneer een rapport wordt uitgevoerd, worden de gebruikersgegevens van de gebruiker die het plan maakte gebruikt om het rapport te genereren. |

### <a name="create-a-report-schedule"></a>Een rapportplanning maken.

1.  In Report Designer, op het Bestand menu, klik Nieuw, en selecteer Rapportplan. Het dialoogvenster Nieuwe Rapportplanning wordt geopend.
2.  Onder Instellingen, selecteer een afzonderlijk rapport of een rapportgroep voor de planning. Alleen rapporten of rapportgroepen voor de selectie bedrijven of bouwstenen waarvoor u momenteel bent aangemeld, zijn beschikbaar.
3.  Schakel het selectievakje Actief in om de rapportplanning in te schakelen. Alleen de maker (ontwerper) van het rapport of een beheerder kan een rapportplanning in- of uitschakelen.
4.  Klik op de knop Machtigingen om bedrijfsreferenties in te voeren. Standaard worden uw aanmeldingsgegevens gebruikt voor het bedrijf waarbij u bent aangemeld. Als er ook andere bedrijven zijn, zoals in rapporteringsstructuurdefinities, selecteert u Afzonderlijke referenties gebruiken en voert u vervolgens de referenties in voor alle overige bedrijven in de rapportplanning. U kunt Windows-verificatie selecteren of een gebruikersnaam en wachtwoord voor elk bedrijf typen. Selecteer het selectievakje om Sla referenties om de gebruikergegevens voor deze bedrijven op te slaan, en klik vervolgens OK om het dialoogvenster te sluiten.
5.  Onder Frequentie, in het veld Beginherhaling, selecteer de datum wanneer de planning moet beginnen. Standaard wordt de huidige systeemdatum van de clientcomputer geselecteerd.
6.  Selecteer in het veld Rapport uitvoeren op het tijdstip waarop het rapport moet worden uitgevoerd. Als u een tijdstip vóór de huidige systeemtijd invoert, wordt het rapport uitgevoerd op de volgende geplande datum.
7.  Geef in het gebied Terugkeerpatroon op hoe vaak het rapport moet worden uitgevoerd. Standaard is Dagelijks geselecteerd met een waarde voor Interval (dagen) van 1. Overige opties zijn Wekelijks, Maandelijks of Jaarlijks.
8.  Selecteer in het gebied Bereik van terugkeerpatroon wanneer het rapport niet meer moet worden gegenereerd.
    -   Geen einddatum – De rapportplanning wordt oneindig uitgevoerd.
    -   Aantal voorvallen – De rapportplanning wordt het opgegeven aantal keer uitgevoerd en daarna uitgeschakeld.
    -   Beëindigen voor – De rapportplanning wordt beëindigd op de opgegeven datum.

9.  Klik op Opslaan op de werkbalk. Geef in het dialoogvenster Opslaan als een unieke naam en beschrijving op voor de rapportplanning.

Om rapportplanning te kopieeren moet u de rol van ontwerper of beheerder hebben. Zelfs als een beheerder het rapportplan wijzigt, behoudt het rapport de referenties van de gebruiker die het rapport heeft gemaakt.
### <a name="copy-a-report-schedule"></a>Een rapportplanning kopiëren.

1.  In Report Designer, klik op Rapportplannen in het navigatievenster, en open een rapportplan om te kopiëren.
2.  Klik in het menu Bestand op Opslaan als en typ een nieuwe naam en beschrijving voor de planning in het dialoogvenster Opslaan als. Klik op OK. De nieuwe planning wordt weergegeven in het navigatievenster.
3.  In het nieuwe schema, wijzigt u de velden en informatie als nodig, en klik vervolgens Opslaan op de werkbalk, of klik Opslaan op het Bestand menu.

Om een rapportplan te verwijderen, moet u de eigenaar van het rapportplan zijn of rol van beheerder hebben.
### <a name="delete-a-report-schedule"></a>Verwijder een rapportplanning.

1.  Klik in Report Designer in het navigatievenster op Rapportgroepen.
2.  Selecteer de rapportplanning die u wilt verwijderen en klik vervolgens op Verwijderen of druk op de toets Delete.
3.  Klik in het bevestigingsvenster voor het verwijderen op Ja om de rapportplanning permanent te verwijderen. Als u geen machtigingen hebt om de planning te verwijderen, wordt een bericht weergegeven en het rapport wordt niet verwijderd.

### <a name="credentials-and-report-schedules"></a>Referenties en rapportschema's

Als u geen referenties invoert die voor alle bedrijven opgenomen in de rapporten worden vereist, ontvangt u het volgende bericht wanneer u op het rapportplan: "U moet uw referenties bedrijven voor de invoeren die in dit rapportplan bevat. Klik op de knop Machtigingen om uw referenties in te voeren."

Bijvoorbeeld, Phyllis meldt zich aan bij Bedrijf A met aan haar gebruikersnaam en wachtwoord. Ze maakt een planning voor een rapport dat een rapporteringsstructuurdefinitie gebruikt om gegevens uit meerdere bedrijven te verzamelen. Wanneer Phyllis het rapport opslaat, wordt haar gevraagd de referenties voor alle overige bedrijven in de rapporteringsstructuurdefinitie op te geven. Wanneer uw referenties verlopen, dan worden de betrokken rapporten in de rapportplanning niet gegenereerd tot de referenties zijn bijgewerkt. Een bericht wordt weergegeven in de rapportwachtrij om aan te geven dat de machtigingen moeten worden bijgewerkt. Het rapport het plan mislukt als een van de volgende scenario's (omdat deze referenties vereisen) plaatsvind:
-   Een nieuw bedrijf is toegevoegd aan een rapportstructuur voor een individueel rapport.
-   Een rapport in een rapportgroep is gewijzigd.
-   Er is een nieuw rapport voor een aanvullend bedrijf toegevoegd aan een rapportgroep.

Om door te gaan, klik op de knop Machtigingen in het dialoogvenster Rapportplanning, en voer vervolgens de juiste referenties in.

## <a name="missing-account-analysis-feature"></a>Analysefunctie ontbrekende rekeningen
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
2.  Selecteer in het veld Bedrijfsfilter een bedrijf waarop u de resultaten wilt filteren of selecteer Alles (geen filter) om resultaten van alle beschikbare bedrijven weer te geven.
3.  Selecteer in het veld Dimensiefilter een dimensie waarop u de resultaten wilt filteren of selecteer Alles (geen filter) om resultaten van alle beschikbare dimensies weer te geven.
4.  Selecteer in het veld Groeperen op een optie voor het sorteren van de resultaten. U kunt resultaten sorteren op de bouwsteen waarop deze van invloed zijn of op de dimensie en waardesets.
5.  Controleer de weergegeven resultaten. Wanneer u in het bovenste deelvenster een item selecteert, wordt in het onderste deelvenster aanvullende informatie over de uitzondering weergegeven. Dit omvat gerelateerde dimensies, waarden en rapporten.
6.  Om het desbetreffende item te openen, klikt op het gekoppelde pictogram dat in het lijstdeelvenster wordt weergegeven, of met de rechtermuisknop op het item en selecteer Openen Om meerdere artikelen te selecteren, houdt de CTRL ingedrukt terwijl u de artikelen in het onderste deelvenster selecteert.
7.  Als eventuele waarden, bouwstenen, of rapporten worden geretourneerd die niet in de analyse worden opgenomen, klik dan met de rechtermuiskno op het item en selecteer Uitsluiten, of selecteer het Uitsluiten selectievakje naast het item om het artikel uit de lijst te verwijderen. De uitgesloten artikelen niet opgenomen wanneer de lijst wordt vernieuwd. Om meerdere artikelen te selecteren, houdt u de CTRL ingedrukt terwijl u de items in het onderste deelvenster selecteert. Om alle items, inclusief alle resultaten die u eerder selecteerde om van de analyse uit te sluiten, te bekijken selecteert u het Weergeven uitgesloten bouwstenen en waarden selectievakje in, en klik op Vernieuwen.
8.  Klik op Vernieuwen om uitzonderingen te vernieuwen die u hebt opgelost. Klik op Ja om volledige vernieuwing van alle resultaten uit te voeren, of klik op Nee om een gedeeltelijke vernieuwing uit te voeren van de geadresseerde items.
    | ![Opmerking](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Opmerking")**Opmerking**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Het formulier automatisch wordt vernieuwd wanneer het opent, tenzij het formulier in de laatste 15 minuten is geopend. |

9.  Wanneer er problemen worden opgelost, klik op OK om het dialoogvenster te sluiten.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Sneltoetsen voor ontbrekende rekeninganalyse
Wanneer u een ontbrekende rekeninganalyse uitvoert, zijn de volgende sneltoetsen beschikbaar.

| Actie                           | Gebruik deze toetsenbordsneltoets |
|--------------------------------------|----------------------------|
| Filteren op bedrijf                    | Alt+C                      |
| Filteren op dimensie                  | Alt+D                      |
| Het veld Groeperen op            | Alt+G                      |
| Uitgesloten blokken en waarden weergeven      | Alt+S                      |
| Resultaten vernieuwen                      | Alt+R                      |
| De geselecteerde bouwstenen uitsluiten  | Alt+X                      |
| De geselecteerde rijdefinitie uitsluiten  | Ctrl+B                     |
| De geselecteerde dimensiewaarde uitsluiten | Ctrl+D                     |
| Open de geselecteerde rapportdefinitie  | Ctrl+R                     |
| Open de geselecteerde rijdefinitie.     | Ctrl+O                     |

 
<a name="see-also"></a>Zie ook
--------

[Financiële rapportage](financial-reporting-intro.md)

[Interface van Report Designer](report-designer-interface.md)



