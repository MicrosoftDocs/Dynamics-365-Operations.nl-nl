---
title: Elektronische documenten genereren en toepassingsgegevens bijwerken via ER
description: U kunt indelingen voor elektronische rapportage (ER) ontwerpen, die in de toepassing Finance and Operations kunnen worden gebruikt voor het genereren van uitgaande elektronische documenten. U kunt ook ER-indelingen ontwerpen die binnenkomende elektronische documenten parseren en de inhoud in die documenten gebruiken om toepassingsgegevens bij te werken.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a989b0000766478c71b243d7793b2fc8c4ece28
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "349211"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Elektronische documenten genereren en toepassingsgegevens bijwerken via ER

[!include [banner](../includes/banner.md)]

U kunt indelingen voor elektronische rapportage (ER) ontwerpen, die in de toepassing Finance and Operations kunnen worden gebruikt voor het genereren van uitgaande elektronische documenten. U kunt ook ER-indelingen ontwerpen die binnenkomende elektronische documenten parseren en de inhoud in die documenten gebruiken om toepassingsgegevens bij te werken.

Met deze functionaliteit kan één ER-indeling worden gebruikt om uitgaande elektronische documenten te genereren en vervolgens de toepassingsgegevens bij te werken. U kunt deze functie gebruiken in de volgende scenario's:

- Om te voorkomen dat toepassingsgegevens in opeenvolgende processen herhaaldelijk worden gebruikt, kunt u de gegevens van een toepassing markeren nadat deze zijn gebruik voor het genereren van elektronische documenten. U kunt bijvoorbeeld betalingstransacties markeren als verwerkt, direct nadat ze zijn opgenomen in een gegenereerd betalingsbericht.
- Voor het opslaan van de verwerkingsgegevens van elektronische documenten die zijn gegenereerd door middel van ER-logica. Bijvoorbeeld, een unieke betalingsbericht-id die wordt gegenereerd op basis van de ER-expressie. De expressie is gebaseerd op gegevens die zijn ingevoerd in het ER-dialoogvenster bij het uitvoeren van de ER-indeling voor het genereren van documenten.

Voor meer informatie over deze functie speelt u de set taakbegeleidingen ER: Documenten genereren met bijwerken van toepassingsgegevens (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) af waarin u de details van Intrastat-rapportage en -archivering krijgt uitgelegd. De volgende bestanden zijn vereist voor het uitvoeren van bepaalde stappen in deze taakbegeleidingen. Download deze bestanden naar uw lokale computer en sla ze daar op.

- [ER-gegevensmodel configureren: Intrastat (model)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER-modeltoewijzing configureren: Intrastat (toewijzing)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER-indeling configureren: Intrastat (indeling)](https://go.microsoft.com/fwlink/?linkid=849038)
