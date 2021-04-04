---
title: ER-configuraties ontwerpen voor het parseren van inkomende documenten
description: Deze procedure toont aan hoe u ER-configuraties (Elektronische rapportage) ontwerpt om een inkomend elektronisch document te parseren.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7235d75aee3b8fdf39492cfbc1760bf6eae4b82e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562851"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>ER-configuraties ontwerpen voor het parseren van inkomende documenten

[!include [banner](../../includes/banner.md)]

Deze procedure toont aan hoe u ER-configuraties (Elektronische rapportage) ontwerpt om een inkomend elektronisch document te parseren. In deze procedure importeert u de vereiste ER-indelingsconfiguraties die zijn gemaakt voor het voorbeeldbedrijf Litware, Inc., en gebruikt u deze vervolgens voor het parseren van inkomende elektronische documenten. Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure "ER Een configuratieprovider maken en deze als actief markeren" voltooien.

Deze procedure is gemaakt voor gebruikers met de toegewezen rol van Systeembeheerder of Elektronische aangifteontwikkelaar.

Deze stappen kunnen worden voltooid met elke dataset. Voordat u begint, downloadt u de bestanden die worden vermeld in het onderwerp "Inkomende documenten parseren om toepassingsgegevens bij te werken" ([Inkomende documenten parseren](../parse-incoming-electronic-documents.md)) en slaat u deze op. De bestanden zijn: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief. Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure "Een configuratieprovider maken en deze als actief markeren".
2. Selecteer Rapportageconfiguraties.
    * Het volgende scenario wordt gebruikt voor het weergeven van de parseermogelijkheden van inkomende elektronische documenten in de XML-indeling: ERP-toepassing vraagt gegevens op van de webservice (bijvoorbeeld fiscale [efsta](http://efsta.org/)-service) en parseert de inkomende responsen om de toepassingsgegevens dienovereenkomstig bij te werken. Er wordt één ER-indeling gebruikt om zo efficiënt mogelijk te parseren, ondanks de verschillende structuur van de verwachte inkomende documenten in XML-indeling.

## <a name="import-and-review-er-configurations"></a>ER-configuraties importeren en controleren

Importeer de ER-modelconfiguratie waarin het voorbeeldgegevensmodel is ontworpen voor het opslaan van de details van het inkomende bestand.

1. Selecteer Uitwisselen.
2. Selecteer Laden uit XML-bestand.
    * Selecteer Bladeren en selecteer het EFSTA model.xml-bestand.
3. Selecteer OK.
4. Selecteer 'EFSTA-model' in de structuur.
5. Selecteer Ontwerper.
    * Controleer de structuur van het geïmporteerde gegevensmodel. De enumType-opsomming is gedefinieerd om de volgende typen serviceresponsen te herkennen: bevestiging krijgen over indiening van transactie, informatie ophalen over de laatst ingediende transactie en herkennen van niet-ondersteunde responstypen.
6. Vouw in de structuur 'Respons' uit.
    * Het basisitem 'Respons' is gedefinieerd om op te geven welke gegevens moeten worden gebruikt uit een respons van de ondersteunde service om de toepassingsgegevens dienovereenkomstig bij te werken.
7. Sluit de pagina.
    * U kunt de ER-indelingsconfiguratie importeren die aangeeft hoe inkomende documenten worden geparseerd voor het opslaan van gegevens in het ER-gegevensmodel.
8. Selecteer Uitwisselen.
9. Selecteer Laden uit XML-bestand.
    * Selecteer Bladeren en selecteer het EFSTA format.xml-bestand.
10. Selecteer OK.
11. Vouw 'EFSTA-model' uit in de structuur.
12. Selecteer 'EFSTA-model\EFSTA-indeling' in de structuur.
13. Selecteer Ontwerper.
14. Selecteer Uitvouwen/samenvouwen.
    * Het CASE-indelingselement wordt gebruikt als de basis en bevat drie geneste FILE-elementen, wat betekent dat deze indeling is ontworpen voor het parseren van inkomende bestanden van verschillende indelingen.
15. Selecteer in de structuur 'Responsen\Transactie voltooid\TraC'.
    * De respons over de ingediende transactie begint vanaf het basiselement 'TraC'.
16. Selecteer in de structuur 'Responsen\Laatste transactieaanvraag\Tra'.
    * De respons over de als laatste ingediende transactie begint vanaf het basiselement 'Era'.
17. Selecteer in de structuur 'Responsen\Onverwachte respons\Tekst '.
    * Het derde FILE-element met het geneste TEXT-element is toegevoegd om andere typen responsen te herkennen die afwijken van de bovengenoemde.
18. Selecteer Indeling aan model toewijzen.
    * Deze modeltoewijzing bevat de definitie voor gegevensstroom om gegevens van het geparseerde inkomende document op te slaan met behulp van de items van het gegevensmodel.
19. Selecteer Ontwerper.
20. Vouw in de structuur 'indeling' uit.
21. Vouw in de structuur 'Indeling\Responsen: Case(Responses)' uit.
    * Controleer de structuur van de ‘indeling’-gegevensbron. Alle drie responstypen worden afzonderlijk aangeboden.
22. Selecteer in de structuur 'Indeling\Responsen: Case(Responses)\aType'.
    * Het gegevensbronitem 'aType' is toegevoegd om het responstype aan te geven en is afhankelijk van het gegevensmodelitem 'Type'.
23. Selecteer het tabblad Validaties.
24. Selecteer in de structuur 'Type = format.Responses.aType'.
    * De ER-validatie is geconfigureerd om de gebruiker te informeren over de situatie wanneer de responsstructuur niet overeenkomt met de bevestiging over de indiening van de transactie of de informatie over de laatst ingediende transactie (aanvraag met niet-ondersteunde respons).
25. Sluit de pagina.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Modeltoewijzing van ER-indeling uitvoeren die is geconfigureerd voor inkomende bestanden

U kunt de gemaakte modeltoewijzing uitvoeren voor testdoeleinden om te zien hoe de geconfigureerde ER-indeling binnenkomende serviceresponsen parseert. Deze stap gebruikt verschillende XML-bestanden voor het simuleren van verschillende typen responsen van de webservice.

1. Open het bestand Response1.xml in een XML-lezer, zoals een webbrowser. Dit bestand bevat details over de voltooide transactie ('TraC' is het basiselement).
2. Selecteer Uitvoeren.
    * Selecteer Bladeren en selecteer het bestand Response1.xml.
3. Selecteer OK.
    * Controleer de gegenereerde uitvoer. Het responstype is correct herkend en geparseerd (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` betekent dat de transactie is voltooid).
    * Open het bestand Response2.xml in een XML-lezer. Dit bestand bevat informatie over de laatst ingediende transactie (`Tra` is het basiselement).
4. Selecteer Uitvoeren.
    * Selecteer Bladeren en selecteer het bestand Response2.xml.
5. Selecteer OK.
    * Controleer de gegenereerde uitvoer. Het responstype is correct herkend en geparseerd (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` betekent dat de herstart van het systeem is voltooid).
    * Open het bestand Response3.xml in een XML-lezer. Dit bestand begint vanaf basisitem TraZ en deze structuur is niet geconfigureerd met een ER-indeling.
6. Selecteer Uitvoeren.
    * Selecteer Bladeren en selecteer het bestand Response3.xml.
7. Selecteer OK.
    * Controleer de gegenereerde uitvoer. Het responstype is correct herkend als niet-ondersteund (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Het bijbehorende bericht is in het infologboek geplaatst (volgens de instelling voor ER-validatie) en het gegevensmodel is grotendeels niet ingevuld.
    * Open het bestand Response4.xml in een XML-lezer. De structuur van dit bestand is bijna hetzelfde als het correct geparseerde bestand Response1.xml, met uitzondering van de geneste elementen van het basiselement 'TraC'.
8. Selecteer Uitvoeren.
    * Selecteer Bladeren en selecteer het bestand Response4.xml.
9. Selecteer OK.
    * Controleer de gegenereerde uitvoer. Het responstype is correct herkend als niet-ondersteund (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Het bijbehorende bericht is in het infologboek geplaatst en het gegevensmodel is grotendeels niet ingevuld. Dit komt doordat de huidige instelling van deze ER-indeling uitgaat van een bepaalde reeks geneste elementen van het basisitem van het inkomende bestand.
10. Sluit de pagina.
11. Selecteer in de structuur 'Responsen\Transactie voltooid\TraC'.
12. Selecteer 'Alle' in het veld Parseervolgorde van geneste elementen.
    * Selecteer Alle in het veld 'Parseervolgorde van geneste elementen' om elke reeks met geneste elementen voor dit XML-basisitem toe te staan.
13. Selecteer Opslaan.
14. Selecteer Indeling aan model toewijzen.
15. Selecteer Uitvoeren.
    * Selecteer Bladeren en selecteer het bestand Response4.xml.
16. Selecteer OK.
    * Controleer de gegenereerde uitvoer. Het responstype is nu correct herkend net als voor het bestand Response1.xml.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]