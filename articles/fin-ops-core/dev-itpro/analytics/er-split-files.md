---
title: Gegenereerde XML-bestanden splitsen op basis van bestandsgrootte en hoeveelheid inhoud
description: Dit onderwerp bevat informatie over het splitsen van gegenereerde bestanden op basis van de bestandsgrootte en de hoeveelheid inhoudsitems.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3735bcb06eff966fc364a891b38d44e34e845e35f59314822d13eba40d51d5f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769967"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Gegenereerde XML-bestanden splitsen op basis van bestandsgrootte en hoeveelheid inhoud

[!include[banner](../includes/banner.md)]

U kunt ER-indelingen (elektronische rapportage) ontwerpen om uitgaande documenten te genereren in XML-indeling. Deze documenten kunnen soms alleen worden geaccepteerd als ze voldoen aan bepaalde criteria, zoals een maximale bestandsgrootte of een maximumaantal van bepaalde XML-knooppunten. U kunt ER-indelingen ontwerpen voor het genereren van elektronische documenten die voldoen aan de eisen die de ontvangers van deze documenten opgeven.

- Voor het indelingselement FILE kunt u een limiet op de bestandsgrootte definiëren als een ER-expressie. Als de ingestelde limiet wordt overschreden wanneer een ER-rapport wordt gegenereerd, maakt ER het maken van het huidige bestand af en wordt doorgegaan naar het volgende bestand.
- Voor een XML-indelingselement kunt u een limiet definiëren voor het aantal elementen als een ER-expressie. Als het aantal XML-knooppunten in het bestand dat wordt gegenereerd, de gedefinieerde limiet overschrijdt wanneer een ER-rapport wordt uitgevoerd, maakt ER het maken van het huidige bestand af en wordt doorgegaan naar het volgende bestand.
- Voor een XML SEQUENCE-indelingselement kunt u een limiet definiëren voor het aantal onderliggende elementen als een ER-expressie. Als het aantal ingesloten XML-knooppunten van het indelingselement in het bestand dat wordt gegenereerd, de gedefinieerde limiet overschrijdt wanneer een ER-rapport wordt uitgevoerd, maakt ER het maken van het huidige bestand af en wordt doorgegaan naar het volgende bestand.
- U kunt elk XML ELEMENT-indelingselement markeren als niet-breekbaar. Op deze manier kunt u de geneste items van XML-knooppunten die onder het indelingselement worden gegenereerd, in één bestand houden.

Naast de indelingselementen XML ELEMENT en XML SEQUENCE gebruiken om XML-knooppunten toe te voegen aan het gegenereerde bestand, kunt u het indelingselement RAW XML gebruiken. Knooppunten die u toevoegt met behulp van het indelingselement RAW XML worden echter niet beschouwd wanneer het aantal knooppunten wordt berekend om de limieten op het aantal elementen te evalueren.

Als u bestandsbestemmingen hebt geconfigureerd voor een FILE-indelingselement dat is geconfigureerd om de gegenereerde uitvoer te splitsen wanneer specifieke limieten worden overschreden, wordt elk stuk gegenereerde uitvoer naar de geconfigureerde bestandsbestemming verzonden als een afzonderlijk bestand. Als u de bestanden die worden gemaakt door de uitvoer te splitsen, uniek wilt benoemen, moet u een ER-expressie configureren voor het FILE-indelingselement. Als u een ER-gegevensbron van het type NUMBER SEQUENCE opneemt, wordt de nummerreeks verhoogd voor elk stuk van de gesplitste uitvoer.

Voor meer informatie over deze functie speelt u de taakbegeleiding **ER gesplitste XML-bestanden op basis van bestandsgrootte en hoeveelheid inhoudsitems** af, die deel uitmaakt van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** en kan worden gedownload uit het [Microsoft Downloadcentrum](https://go.microsoft.com/fwlink/?linkid=874684). Deze taakbegeleiding helpt u bij het proces van het configureren van een ER-indeling als u gegenereerde bestanden wilt splitsen op basis van beperkingen op de bestandsgrootte en de hoeveelheid inhoudsitems. Als u de taakbegeleiding wilt voltooien, moet u de volgende bestanden downloaden:

- [ER-modelconfiguratie - XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER-indelingsconfiguratie - XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>Aanvullende resources
[Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)

[Formuleontwerper in elektronische rapportage (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
