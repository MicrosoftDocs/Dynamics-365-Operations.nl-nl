---
title: ER-configuraties ontwerpen om gegevens te importeren uit externe CSV-bestanden
description: Gebruik deze procedure voor het ontwerpen van configuraties elektronische rapportage om gegevens te importeren in een Finance and Operations-app vanuit een extern bestand in CSV-indeling.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fbae4570448a6bb1309ffe0092ff9b07825d717
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092761"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>ER-configuraties ontwerpen om gegevens te importeren uit externe CSV-bestanden

[!include [banner](../../includes/banner.md)]

Gebruik deze procedure voor het ontwerpen van ER-configuraties (elektronische rapportage) om gegevens te importeren in de toepassing vanuit een extern bestand in CSV-indeling. In deze procedure maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf Litware, Inc. Voordat u deze stappen uitvoert, moet u eerst de stappen uitvoeren in de procedure "ER Een configuratieprovider maken en deze als actief markeren".

Deze procedure is gemaakt voor gebruikers met de toegewezen rol van Systeembeheerder of Elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met de USMF-gegevensset.

U moet ook de volgende bestanden downloaden en lokaal opslaan: [Dynamics 365 Finance-voorbeelden van elektronische raqpportage](https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * U kunt een proces voor het importeren van externe bestanden in XML-, TXT- of CSV-indeling configureren voor tabellen in de toepassing. Eerst moet u een abstract gegevensmodel maken om vanuit een zakelijk oogpunt de geïmporteerde gegevens aan te duiden: hiervoor wordt een configuratie voor een ER-gegevensmodel gemaakt. Definieer vervolgens een structuur voor het geïmporteerde bestand die is gekoppeld aan het ontworpen gegevensmodel als een manier voor het doorgeven van gegevens aan het abstracte gegevensmodel: hiervoor wordt een ER-indelingsconfiguratie gemaakt. Vervolgens moet u de ER-gegevensmodelconfiguratie uitbreiden met een nieuwe modeltoewijzing die beschrijft hoe de gegevens uit het geïmporteerde bestand en de permanente gegevens uit het abstracte gegevensmodel worden gebruikt voor het bijwerken van toepassingstabellen of gegevensentiteiten.
    * De volgende stappen laten zien hoe extern bijgehouden leverancierstransacties worden geïmporteerd uit het externe CSV-bestand voor later gebruik in de leveranciersvereffening voor 1099-formulieren.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en is gemarkeerd als actief. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" uitvoeren.
2. Klik op Rapportconfiguraties.
3. Pas het filter '1099 Payments model' toe. Als u eerder de procedure "ER Vereiste configuraties maken om gegevens te importeren uit een extern bestand voor elektronische aangifte" en de configuratie '1099 Payments model' beschikbaar is in de configuratiestructuur, slaat u alle stappen in de volgende subtaak over.

## <a name="add-a-new-er-model-configuration"></a>Een nieuwe ER-modelconfiguratie toevoegen

1. U hoeft niet een nieuw model te maken ter ondersteuning van de gegevensimport, maar u laadt het bestand 1099model.xml dat u eerder hebt gedownload. Dit bestand bevat het aangepaste gegevensmodel voor leverancierstransacties. Dit gegevensmodel is al toegewezen aan de benodigde gegevensonderdelen.
2. Klik op Uitwisselen.
3. Klik op Laden uit XML-bestand.
4. Klik op Bladeren en navigeer naar het bestand 1099model.xml, dat u eerder hebt gedownload.
5. Klik op OK.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Een nieuwe ER-indelingsconfiguratie toevoegen die het importeren van gegevens ondersteunt

1. Selecteer in de structuur '1099 Payments model'.
2. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
3. Voer in het veld Nieuw de volgende tekst in: 'Indeling gebaseerd op gegevensmodel 1099 Payments model'.
4. Selecteer in het veld Ondersteunt gegevensimport de waarde Ja.
5. Druk op ESC om deze pagina te sluiten.
    * U hoeft niet een nieuwe ER-indeling te maken ter ondersteuning van de gegevensimport, maar u laadt het bestand 1099formatcsv.xml, dat u eerder hebt gedownload. Dit bestand bevat de vereiste ER-indeling waarmee de structuur van het inkomende CSV-bestand en de toewijzing van deze structuur aan het gegevensmodel van de leverancierstransacties wordt gedefinieerd.
6. Klik op Uitwisselen.
7. Klik op Laden uit XML-bestand.
    * Klik op Bladeren en navigeer naar het bestand 1099formatcsv.xml, dat u eerder hebt gedownload.
8. Klik op OK.
9. Vouw in de structuur '1099 Payments model' uit.
10. Selecteer in de structuur '1099 Payments model\For importing vendors' transactions (CSV)'.

## <a name="review-format-settings"></a>Indelingsinstellingen controleren

1. Klik op Ontwerper.
2. Klik op Uitvouwen/samenvouwen.
3. Schakel de optie 'Details weergeven' in.
    * De ontworpen opmaak vertegenwoordigt de verwachte structuur van het externe bestand in CSV-indeling.
4. Selecteer in de structuur 'Inkomend: File\Root: Sequence'.
    * Voor het basiselement van het type SEQUENCE is de optie 'Nieuwe regel - Windows (CR LF)' geselecteerd in het veld 'Speciale tekens'. Op basis van deze instelling moet elke regel in het parseerbestand worden beschouwd als een afzonderlijke record.
5. Selecteer in de structuur `Incoming: File\Root: Sequence\Line: Sequence 1..*`.
    * Voor het element Root\Line van het type SEQUENCE is de optie 'Een veel' geselecteerd in het veld 'Multipliciteit'. Op basis van deze instelling wordt ten minste één regel weergegeven in het parseerbestand.
6. Selecteer in de structuur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case`.
    * Houd er rekening mee dat het element Root\Line\Types van het type CASE is toegevoegd als het geneste element van de reeks Root\Line. Omdat dit CASE-element 3 geneste reekselementen bevat, wordt op basis van deze instelling aangenomen dat we moeten voldoen aan 3 verschillende regeltypen in het parseerbestand.
7. Selecteer in de structuur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1`.
    * Het element Root\Line\Types\Header van het type SEQUENCE bevat het geneste STRING-element waarvan de waarde is gedefinieerd als de waarde van de vaste tekenreeks. Deze reeks parseert de kopregel van het parseerbestand.
8. Selecteer in de structuur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)`.
    * Het element Root\Line\Types\Record van het type SEQUENCE is geconfigureerd voor het parseren van de transactieregels. Houd er rekening mee dat de optie 'Aangepast scheidingsteken' is geconfigureerd als een komma. Dit betekent dat de komma wordt gebruikt als scheidingsteken voor velden van dit type regel in het parseerbestand.
    * Houd er rekening mee dat meerdere geneste elementen van verschillende gegevenstypen zijn toegevoegd voor het element Root\Line\Types\Record voor het parseren van de transactieregels als afzonderlijke velden. De optie 'Toepassing aanhalingstekens' is geconfigureerd als 'Geen'. Dit betekent dat er voor het parseerbestand vanuit wordt gegaan dat alle velden van dit type geen ingesloten tekens hebben.
9. Selecteer in de structuur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime`.
    * Het element Root\Line\Types\Record\TransactionDate van het type DATETIME is bijvoorbeeld geconfigureerd om de waarde voor datum en tijd van de transactie op te halen uit het parseerbestand in de indeling 'M/d/jjjj'.
10. Selecteer in de structuur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1`.
    * Opmerking: het element Root\Line\Types\Record\CountryCode van het type STRING is geconfigureerd met de optie 'Nul een' in het veld 'Multipliciteit'. Voor deze instelling is de waarde van het veld CountryCode in de parseerregel optioneel.
11. Selecteer in de structuur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,)`.
    * Het element Root\Line\Types\Record\Remark van het type SEQUENCE is geconfigureerd met de optie 'Alle' in het veld 'Toepassing aanhalingstekens' en dubbele aanhalingstekens in het veld 'Aanhalingsteken'. Dit betekent dat alle velden met dit type regels in het parseerbestand (beschreven door de geneste elementen: tekst van het type STRING) worden beschouwd als ingesloten in dubbele aanhalingstekens.
12. Selecteer in de structuur `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1`.
    * Het element Root\Line\Types\Unparsed van het type SEQUENCE is geconfigureerd voor het parseren van de transactieregels voor de structuur die niet overeenkomt met de structuur van het hierboven beschreven bovenliggende CASE-element.

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>De instelling van de indelingstoewijzing naar het gegevensmodel controleren

1. Klik op 'Indeling aan model toewijzen'.
    * De modeltoewijzing 'Toewijzing aan het model vanuit CSV-indeling' beschrijft de gegevensstroom van de gegevensoverdracht uit het inkomende CSV-bestand naar het gegevensmodel.
2. Klik op Ontwerper.
3. Vouw in de structuur 'indeling' uit.
    * Merk op dat de ontworpen indeling hier wordt weergegeven als een onderdeel van de gegevensbron.
4. Vouw in de structuur 'indeling\Inkomend: File(Incoming)' uit.
5. Vouw in de structuur 'indeling\Inkomend: File(Incoming)\Root: Sequence(Root)' uit.
6. Vouw in de structuur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)` uit.
7. Vouw in de structuur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)` uit.
8. Vouw in de structuur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)` uit.
9. Vouw in de structuur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data` uit.
10. Vouw in de structuur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode)` uit.
11. Selecteer in de structuur `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate)`.
    * Houd er rekening mee dat de vereiste en optionele indelingselementen, zoals TransactionDate en CountryCode, er anders uitzien in het vooraf gedefinieerde gegevensbrononderdeel voor de 'indeling'.
12. Vouw in de structuur 'Transacties = '$both'' uit.
    * Houd er rekening mee dat de elementen van de indeling waarmee de structuur van het geïmporteerde bestand wordt gedefinieerd, zijn gebonden aan de elementen van het gegevensmodel. Op basis van deze bindingen wordt de inhoud van het geïmporteerde CSV-bestand tijdens de uitvoering opgeslagen in het bestaande gegevensmodel. Let op de binding van het element CountryRegion. Voor elk transactie-element in het inkomende bestand waarvoor geen landcodewaarde is opgegeven, wordt standaard de landcode 'V.S.' ingevuld in het gegevensmodel.
13. Schakel de optie 'Details weergeven' in.
14. Klik op het tabblad Validaties.
15. Klik op Zoeken.
16. Typ in het veld Zoeken 'vend'.
17. Klik op Volgende zoeken.
    * Deze indelingstoewijzing kan door de gebruiker gedefinieerde logica bevatten voor het valideren van de nauwkeurigheid van de geïmporteerde gegevens vanuit een zakelijk oogpunt. Bijvoorbeeld wordt op basis van de instelling voor elke regel in het importbestand waarvan de structuur niet overeenkomt met de structuur van de kopregel of de transactieregel, een waarschuwingsbericht gegenereerd in het infologboek om de gebruiker te informeren over deze aanvraag waarbij het volgnummer van de transactie in het bestand wordt aangegeven.
18. Sluit de pagina.

## <a name="run-the-format-mapping"></a>De toewijzing van de bestandsindeling uitvoeren

Voer voor testdoeleinden de toewijzing van de indeling uit met behulp van het 1099entriescsv.csv-bestand dat u eerder hebt gedownload. De gegenereerde uitvoer geeft de gegevens aan die worden geïmporteerd vanuit het geselecteerde CSV-bestand en ingevuld in het aangepaste gegevensmodel bij de daadwerkelijke import.

1. Klik op Uitvoeren.
    * Klik op Bladeren en navigeer naar het bestand 1099entriescsv.csv, dat u eerder hebt gedownload.
2. Klik op OK.
    * Noteer de waarschuwingsberichten over de regels die niet worden geaccepteerd. Regel 4 bevat de waarde van de inkomsten die wordt weergegeven in de niet-toegestane indeling terwijl in regel 7 de tekst van de opmerking niet tussen dubbele aanhalingstekens is geplaatst.
    * Bekijk de uitvoer in XML-indeling, die de gegevens vertegenwoordigt die zijn geïmporteerd vanuit het geselecteerde bestand en overgezet naar het gegevensmodel. Alle 7 regels van het geïmporteerde CSV-bestand zijn verwerkt. Regel 1 van de titels van de opgenomen velden is overgeslagen, 4 transacties zijn correct geparseerd en 2 transacties zijn aangeduid als ongeldig.
3. Sluit de pagina.
4. Sluit de pagina.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]