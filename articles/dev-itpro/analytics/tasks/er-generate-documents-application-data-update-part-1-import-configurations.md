---
title: Configuraties importeren voor het genereren van documenten die toepassingsgegevens bevatten
description: Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Een configuratieprovider maken en deze als actief markeren' voltooien.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1637ba59525f5f8bd9fe41a00c34eca90f7a2751
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "340793"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Configuraties importeren voor het genereren van documenten die toepassingsgegevens bevatten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Een configuratieprovider maken en deze als actief markeren' voltooien.

De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren. In deze procedure importeert u de vereiste ER-indelingsconfiguraties die zijn gemaakt voor het voorbeeldbedrijf, Litware, Inc., en genereert u vervolgens elektronische documenten. Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met de DEMF-gegevensset. Voordat u begint, downloadt u de bestanden die worden genoemd in Help-onderwerp Elektronische documenten genereren en toepassingsgegevens bijwerken met het ER-hulpmiddel (generate-electronic-documents-update-application-data/) en slaat u deze op. De bestanden zijn .XML-Intrastat (model), Intrastat (toewijzing) XML- en .XML-Intrastat (indeling).

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief. Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure Een configuratieprovider maken en deze als actief markeren.  
    * De stappen in deze procedure laten zien hoe u ER-mogelijkheden gebruikt om een update van toepassingsgegevens te voltooien en hoe u een Intrastat-rapport genereert. De details van het rapportageproces worden gearchiveerd in de toepassingstabellen. Wanneer het Intrastat-rapportageproces wordt geactiveerd vanuit het Intrastat-formulier, vindt archivering momenteel plaats op basis van de logica die is geprogrammeerd in de bestaande broncode. In deze procedure configureert u een vergelijkbare maar vereenvoudigde logica van toepassingsgegevens met alleen het ER-framework. Er worden geen wijzigingen aangebracht in de broncode.   

## <a name="import-er-configurations"></a>ER-configuraties importeren
1. Klik op Rapportconfiguraties.
2. Klik op Uitwisselen.
3. Klik op Laden uit XML-bestand.
    * Importeer de ER-modelconfiguratie die het gegevensmodel bevat die is ontworpen om te worden gebruikt als de gegevensbron voor het genereren van het Intrastat-rapport. Later gaat u deze gegevensmodeldefinitie uitbreiden om deze te gebruiken voor de update van toepassingsgegevens om details te archiveren van het Intrastat-rapportageproces.   
    * Klik op Bladeren en selecteer het .XML-bestand voor Intrastat (model).  
4. Klik op OK.
5. Selecteer in de structuur 'Intrastat (model)'.
6. Klik op Ontwerper.
7. Vouw in de structuur 'Voor uitgaand document' uit.
8. Vouw in de structuur 'Voor uitgaand document\Transacties' uit.
    * Controleer de structuur van het geïmporteerde gegevensmodel. Houd er rekening mee dat het basisitem 'Voor uitgaand document' is gedefinieerd om de gegevensstroom op te geven voor het verkrijgen van gegevens uit de toepassing en deze te gebruiken als een gegevensbron om het Intrastat-rapport te genereren. 'Transacties (lijst met records)' wordt gebruikt om de lijst met Intrastat-transacties voor te stellen die moeten worden gerapporteerd. Omdat u gerapporteerde basisproductcodes zult archiveren, is de unieke id van één basisproductcode 'Basisproductrecord-id (Int64)' in deze gegevensstroom nodig.   
9. Sluit de pagina.
10. Klik op Uitwisselen.
11. Klik op Laden uit XML-bestand.
    * Importeer de ER-toewijzingsconfiguratie die de gegevensstroom opgeeft voor het verkrijgen van gegevens uit de toepassing en het gebruiken ervan om het Intrastat-rapport te genereren. Later gaat u deze modeltoewijzingsdefinitie uitbreiden om gegevens op te halen uit het Intrastat-rapport en deze te gebruiken voor de update van toepassingsgegevens om details te archiveren van het Intrastat-rapportageproces.   
    * Klik op Bladeren en selecteer het .XML-bestand voor Intrastat (toewijzing).  
12. Klik op OK.
13. Vouw in de structuur 'Intrastat (model)' uit.
14. Selecteer in de structuur 'Intrastat (model)\Intrastat (toewijzing)'.
15. Klik op Ontwerper.
    * Houd er rekening mee dat de huidige modeltoewijzing de waarde 'Naar model' bevat in het veld Richting. Dit betekent dat deze modeltoewijzing is ontworpen voor het ophalen van gegevens uit de toepassing en deze op te slaan in het gegevensmodel.  
16. Klik op Ontwerper.
17. Vouw in de structuur 'Lijst' uit.
18. Vouw in de structuur 'Transacties= Lijst' uit.
    * Controleeer de structuur van de modeltoewijzing die gebruikmaakt van het gegevensmodel dat wordt gefilterd op basis van het basisartikel 'voor uitgaand document'. Houd er rekening mee dat de toegevoegde gegevensbron 'Lijst' toegang biedt tot de vereiste toepassingsgegevens, zoals de lijst met records uit de Intrastat-tabel.  
19. Sluit de pagina.
20. Sluit de pagina.
21. Klik op Uitwisselen.
22. Klik op Laden uit XML-bestand.
    * Importeer de ER-indelingsconfiguratie waarmee de indeling van het Intrastat-rapport en het proces voor het invullen van gegevens in het rapport wordt opgegeven. Later gaat u deze indelingsdefinitie uitbreiden om gegevens uit het Intrastat-rapport in het gegevensmodel te plaatsen en het vervolgens te gebruiken om toepassingsgegevens bij te werken om de details te archiveren van het Intrastat-rapportageproces.   
    * Klik op Bladeren en selecteer het .XML-bestand voor Intrastat (indeling).  
23. Klik op OK.
24. Selecteer in de structuur 'Intrastat (model)\Intrastat (indeling)'.
25. Klik op Ontwerper.
26. Klik op Uitvouwen/samenvouwen.
27. Selecteer in de structuur 'Bestand\Declaratie'.
28. Klik op het tabblad Toewijzing.
29. Selecteer in de structuur 'Bestand'.
    * Controleer de structuur van de indeling die wordt gebruikt om het Intrastat-rapport te genereren. Houd er rekening mee dat het is ontworpen voor het genereren van een XML-bestand door gegevens in te vullen uit het gegevensmodel, dat is gebaseerd op het basisitem 'Voor uitgaand document'. Controleer of de naam voor het gegenereerde bestand is gedefinieerd in het gebruikersdialoogvenster (hiervoor wordt de 'fn'-gegevensbron gebruikt).   
30. Sluit de pagina.

