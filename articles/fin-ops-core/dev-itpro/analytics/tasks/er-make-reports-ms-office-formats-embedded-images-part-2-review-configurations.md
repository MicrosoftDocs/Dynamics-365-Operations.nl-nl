---
title: Configuraties beoordelen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten
description: Dit onderwerp laat zien hoe u rapportageconfiguraties ontwerpt voor het genereren van elektronische documenten met ingesloten afbeeldingen. (Deel 1 - Parameters instellen).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eee6300350dd96c34f2eab44704d1895e6171ff
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093640"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Configuraties beoordelen voor het genereren van rapporten in Office-indeling die ingesloten afbeeldingen bevatten

[!include [banner](../../includes/banner.md)]

Als u deze stappen wilt voltooien, moet u eerst de stappen uitvoeren in de taakbegeleiding "ER Rapporten in MS Office-indelingen maken met ingesloten afbeeldingen (deel 1: Parameters instellen)".

Deze procedure laat zien hoe u elektronische rapportage (ER)-configuraties ontwerpt voor het genereren van elektronische documenten met ingesloten afbeeldingen in Microsoft Excel en Microsoft Word. In dit voorbeeld controleert u ER-configuraties voor voorbeeldbedrijf Litware, Inc. 

Deze procedure is bedoeld voor gebruikers met de rol Systeembeheerder of Elektronische aangifteontwikkelaar. De stappen kunnen worden voltooid met de USMF-gegevensset.


## <a name="review-the-imported-data-model"></a>Het geïmporteerde gegevensmodel controleren
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Selecteer in de structuur 'Model voor cheques'.
3. Klik op Ontwerper.
    * Dit model is ontworpen om betaalcheques voor te stellen vanuit het bedrijfsoogpunt en de toewijzing van dit model aan de gegevensbronnen van de toepassing. Controleer dit model door de ER Operations-ontwerper. Let op de kenmerken van de modelelementen die worden weergegeven: structuur, naam, omschrijving, gegevenstype, enzovoort.   
4. Vouw in de structuur 'basis' uit.
5. Selecteer in de structuur 'basis\cheques'.
6. Vouw de structuur 'basis\cheques' uit.
7. Vouw de structuur 'basis\cheques\kenmerken' uit.
8. Vouw de structuur 'basis\betaler' uit.
9. Selecteer in de structuur 'basis\istestrun'.
10. Selecteer in de structuur 'basis\indeling'.
    * Het indelingselement van dit model vertegenwoordigt de details van de afdrukindeling van het chequeformulier voor de geselecteerde bankrekening. Het bevat ook twee knooppunten van het gegevenstype Container om afbeeldingen op te slaan.   
11. Vouw in de structuur 'basis\indeling' uit.
12. Selecteer in de structuur 'basis\indeling\bedrijfslogo'.
13. Vouw in de structuur 'basis\indeling\bedrijfslogo' uit.
14. Selecteer in de structuur 'basis\indeling\bedrijfslogo\afbeelding'.
15. Selecteer in de structuur 'basis\indeling\bedrijfslogo\isprinted'.
16. Selecteer in de structuur 'basis\indeling\handtekening'.
17. Vouw in de structuur 'basis\indeling\handtekening' uit.
18. Selecteer in de structuur 'basis\indeling\handtekening\afbeelding'.
19. Selecteer in de structuur 'basis\indeling\handtekening\isprinted'.
    * Twee afbeeldingsgegevensmodelelementen zijn gebonden aan de velden van de tabellen die afbeeldingen bevatten van het bedrijfslogo en de handtekening van de bevoegde persoon in binaire indeling.  
20. Vouw in de structuur 'basis\indeling\watermerk' uit.
21. Klik op Model toewijzen aan gegevensbron.
22. Klik op Ontwerper.
23. Vouw in de structuur 'chequesgeselecteerd' uit.
24. Vouw in de structuur 'indeling' uit.
25. Vouw in de structuur 'indeling\bedrijfslogo' uit.
26. Vouw in de structuur 'indeling\handtekening' uit.
27. Vouw in de structuur 'indeling\watermerk' uit.
28. Schakel de optie 'Details weergeven' in.
    * Het chequegegevensmodelelement is gebonden aan de tabel TmpChequePrintout die tijdens runtime records bevat voor cheques die de gebruiker heeft geselecteerd om af te drukken.   
29. Sluit de pagina.
30. Sluit de pagina.
31. Sluit de pagina.

## <a name="review-the-imported-format"></a>De geïmporteerde indeling controleren
1. Vouw in de structuur 'Model voor cheques' uit.
2. Selecteer in de structuur ' Model voor cheques\Afdrukindeling van cheques'.
3. Klik op Ontwerper.
4. Klik op Bijlagen.
5. Klik op Openen.
    * De gekoppelde sjabloon van het rapport in Excel openen.  
    * Controleer de gekoppelde Excel-sjabloon van het rapport die wordt gebruikt voor het afdrukken van cheques. De sjabloon bevat twee cheques per pagina en is ontworpen voor het afdrukken van cheques naar het voorgedrukte formulier. Er zijn twee lege afbeeldingen ingesloten. Deze lege afbeeldingen zijn voor het bedrijfslogo en de handtekening van de persoon die een betaling autoriseert. Controleer of de afbeeldingen de naam CompLogo en SignatureImage, respectievelijk in Excel hebben.   
6. Sluit de pagina.
7. Vouw in de structuur 'Rapport' uit.
8. Vouw in de structuur 'Rapport\Chequeregels' uit.
9. Selecteer in de structuur 'Rapport\Chequeregels\Bedrijfslogo'.
10. Schakel de optie 'Details weergeven' in.
    * Het celelement van de indeling 'CompLogo' vertegenwoordigt het Excel-item dat wordt gebruikt om de bedrijfslogoafbeelding te vullen in het rapport. Dit indelingselement is gebonden aan het afbeeldingsgegevensmodelelement dat tijdens de uitvoering een bedrijfslogoafbeelding bevat in binaire indeling.   
11. Klik op het tabblad Toewijzing.
12. Klik op Bewerken ingeschakeld.
    * U kunt het celelement van de indeling 'CompLogo' zo maken dat het niet meer ingeschakeld is. In dit geval verbergt het bijbehorende Excel-afbeeldingselement een bedrijfslogo in het gegenereerde rapport. Als de ingeschakelde expressie TRUE retourneert en de gedefinieerde binding geen afbeelding oplevert, toont het Excel-afbeeldingselement een afbeelding die is opgeslagen in de Excel-sjabloon.   
13. Sluit de pagina.
14. Vouw in de structuur 'labels: Container' uit.
    * Sommige labels die worden weergegeven in het voorgedrukte chequeformulier, worden in het rapport opgenomen wanneer het wordt gemaakt voor testdoeleinden. Deze labels worden echter niet afgedrukt tijdens het echte afdrukken, omdat het voorgedrukte formulier deze al bevat.  
15. Sluit de pagina.

