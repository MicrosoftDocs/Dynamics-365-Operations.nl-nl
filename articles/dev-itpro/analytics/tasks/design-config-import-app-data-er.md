---
title: ER-configuraties ontwerpen voor het parseren van inkomende documenten
description: Deze procedure toont aan hoe u ER-configuraties (Elektronische rapportage) ontwerpt om een inkomend elektronisch document te parseren.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e5f826afa141c0851a963b33e40c58513e60a07
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551478"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>ER-configuraties ontwerpen voor het parseren van inkomende documenten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont aan hoe u ER-configuraties (Elektronische rapportage) ontwerpt om een inkomend elektronisch document te parseren. In deze procedure importeert u de vereiste ER-indelingsconfiguraties die zijn gemaakt voor het voorbeeldbedrijf Litware, Inc., en gebruikt u deze vervolgens voor het parseren van inkomende elektronische documenten. Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Een configuratieprovider maken en deze als actief markeren' voltooien.

Deze procedure is gemaakt voor gebruikers met de toegewezen rol van Systeembeheerder of Elektronische aangifteontwikkelaar. 

Deze stappen kunnen worden voltooid met elke dataset. Voordat u begint, downloadt u de bestanden die worden vermeld in het onderwerp 'Inkomende documenten parseren om toepassingsgegevens bij te werken' (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents)) en slaat u deze op. De bestanden zijn: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief. Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure 'Een configuratieprovider maken en deze als actief markeren'.  
2. Klik op Rapportconfiguraties.
    * Het volgende scenario wordt gebruikt voor het weergeven van de parseermogelijkheden van inkomende elektronische documenten in de XML-indeling: ERP-toepassing (Dynamics 365 for Finance and Operations)vraagt gegevens op van de webservice (bijvoorbeeld http://efsta.org/fiscale EFSTA-service) en parseert de inkomende antwoorden om de toepassingsgegevens dienovereenkomstig bij te werken. Er wordt één ER-indeling gebruikt om zo efficiënt mogelijk te parseren, ondanks de verschillende structuur van de verwachte inkomende documenten in XML-indeling.   

## <a name="import-and-review-er-configurations"></a>ER-configuraties importeren en controleren
Importeer de ER-modelconfiguratie waarin het voorbeeldgegevensmodel is ontworpen voor het opslaan van de details van het inkomende bestand.  
1. Klik op Uitwisselen.
2. Klik op Laden uit XML-bestand.
    * Klik op Bladeren en selecteer het EFSTA model.xml-bestand.  
3. Klik op OK.
4. Selecteer 'EFSTA-model' in de structuur.
5. Klik op Ontwerper.
    * Controleer de structuur van het geïmporteerde gegevensmodel. Houd er rekening mee dat de enumType-opsomming is gedefinieerd om de volgende soorten service-antwoorden te herkennen: bevestiging krijgen over indiening van transactie, informatie ophalen over de laatst ingediende transactie en herkennen van niet-ondersteunde antwoordtypen.   
6. Vouw in de structuur 'Antwoord' uit.
    * Houd er rekening mee dat het basisitem 'Antwoord' is gedefinieerd om op te geven welke gegevens moeten worden gebruikt uit een antwoord van de ondersteunde service om de toepassingsgegevens dienovereenkomstig bij te werken.   
7. Sluit de pagina.
    * U kunt de ER-indelingsconfiguratie importeren die aangeeft hoe inkomende documenten worden geparseerd voor het opslaan van gegevens in het ER-gegevensmodel.   
8. Klik op Uitwisselen.
9. Klik op Laden uit XML-bestand.
    * Klik op Bladeren en selecteer het EFSTA format.xml-bestand.  
10. Klik op OK.
11. Vouw 'EFSTA-model' uit in de structuur.
12. Selecteer 'EFSTA-model\EFSTA-indeling' in de structuur.
13. Klik op Ontwerper.
14. Klik op Uitvouwen/samenvouwen.
    * Houd er rekening mee dat het CASE-indelingselement wordt gebruikt als de basis en drie geneste FILE-elementen bevat, wat betekent dat deze indeling is ontworpen voor het parseren van inkomende bestanden van verschillende indelingen.  
15. Selecteer in de structuur 'Antwoorden\Transactie voltooid\TraC'.
    * Houd er rekening mee dat het antwoord over de ingediende transactie begint vanaf het basiselement 'TraC'.   
16. Selecteer in de structuur 'Antwoorden\Laatste transactieaanvraag\Tra'.
    * Houd er rekening mee dat het antwoord over de laatst ingediende transactie begint vanaf het basiselement 'Tra'.   
17. Selecteer in de structuur 'Antwoorden\Onverwacht antwoord\Tekst '.
    * Het derde FILE-element met het geneste TEXT-element is toegevoegd om andere soorten antwoorden te herkennen die afwijken van de bovengenoemde.   
18. Klik op 'Indeling aan model toewijzen'.
    * Deze modeltoewijzing bevat de definitie voor gegevensstroom om gegevens van het geparseerde inkomende document op te slaan met behulp van de items van het gegevensmodel.  
19. Klik op Ontwerper.
20. Vouw in de structuur 'indeling' uit.
21. Vouw in de structuur 'Indeling\Antwoorden: Case(Responses)' uit.
    * Controleer de structuur van de ‘indeling’-gegevensbron. Houd er rekening mee dat alle drie antwoordtypen afzonderlijk worden aangeboden.   
22. Selecteer in de structuur 'Indeling\Antwoorden: Case(Responses)\aType'.
    * Het gegevensbronitem ‘aType’ is toegevoegd om het antwoordtype aan te geven en is afhankelijk van het gegevensmodelitem ‘Type’.  
23. Klik op het tabblad Validaties.
24. Selecteer in de structuur 'Type = format.Responses.aType'.
    * Houd er rekening mee dat de ER-validatie is geconfigureerd om de gebruiker te informeren over de situatie wanneer de antwoordstructuur niet overeenkomt met de bevestiging over de indiening van de transactie of de informatie over de laatst ingediende transactie (aanvraag met niet-ondersteund antwoord).   
25. Sluit de pagina.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Modeltoewijzing van ER-indeling uitvoeren die is geconfigureerd voor inkomende bestanden
U kunt de gemaakte modeltoewijzing uitvoeren voor testdoeleinden om te zien hoe de geconfigureerde ER-indeling binnenkomende service-antwoorden parseert. Deze stap gebruikt verschillende XML-bestanden voor het simuleren van verschillende soorten antwoorden van de webservice.   
1. Open het bestand Response1.xml in een XML-lezer, zoals een webbrowser. Houd er rekening mee dat dit bestand details over de voltooide transactie bevat ('TraC' is het basiselement).   
2. Klik op Uitvoeren.
    * Klik op Bladeren en selecteer het Response1.xml-bestand.  
3. Klik op OK.
    * Controleer de gegenereerde uitvoer. Merk op dat het antwoordtype correct is herkend en geparseerd (ERModelEnumDataSourceHandler#EFSTA model#enumType#C betekent aanvraag met voltooide transactie).   
    * Open het bestand Response2.xml in een XML-lezer. Dit bestand bevat informatie over de laatst ingediende transactie ('Tra' is het basiselement).   
4. Klik op Uitvoeren.
    * Klik op Bladeren en selecteer het Response2.xml-bestand.  
5. Klik op OK.
    * Controleer de gegenereerde uitvoer. Merk op dat het antwoordtype correct is herkend en geparseerd (ERModelEnumDataSourceHandler#EFSTA model#enumType#R betekent aanvraag met herstarten van systeem).   
    * Open het bestand Response3.xml in een XML-lezer. Dit bestand begint vanaf basisitem TraZ en deze structuur is niet geconfigureerd met een ER-indeling.   
6. Klik op Uitvoeren.
    * Klik op Bladeren en selecteer het Response3.xml-bestand.  
7. Klik op OK.
    * Controleer de gegenereerde uitvoer. Merk op dat het antwoordtype correct is herkend als niet ondersteund (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Het bijbehorende bericht is in het infologboek geplaatst (volgens de instelling voor ER-validatie) en het gegevensmodel is grotendeels niet ingevuld.   
    * Open het bestand Response4.xml in een XML-lezer. De structuur van dit bestand is bijna hetzelfde als het correct geparseerde bestand Response1.xml, met uitzondering van de geneste elementen van het basiselement 'TraC'.   
8. Klik op Uitvoeren.
    * Klik op Bladeren en selecteer het Response4.xml-bestand.  
9. Klik op OK.
    * Controleer de gegenereerde uitvoer. Merk op dat het antwoordtype correct is herkend als niet ondersteund (ERModelEnumDataSourceHandler#EFSTA model#enumType#U)). Het bijbehorende bericht is in het infologboek geplaatst en het gegevensmodel is grotendeels niet ingevuld. Dit is omdat de huidige instelling van deze ER-indeling uitgaat van een bepaalde reeks geneste elementen van het basisitem van het inkomende bestand.   
10. Sluit de pagina.
11. Selecteer in de structuur 'Antwoorden\Transactie voltooid\TraC'.
12. Selecteer 'Alle' in het veld Parseervolgorde van geneste elementen.
    * Selecteer Alle in het veld 'Parseervolgorde van geneste elementen' om elke reeks met geneste elementen voor dit XML-basisitem toe te staan.  
13. Klik op Opslaan.
14. Klik op 'Indeling aan model toewijzen'.
15. Klik op Uitvoeren.
    * Klik op Bladeren en selecteer het Response4.xml-bestand.  
16. Klik op OK.
    * Controleer de gegenereerde uitvoer. Merk op dat het antwoordtype nu correct is herkend net als voor Response1.xml-bestand.  

