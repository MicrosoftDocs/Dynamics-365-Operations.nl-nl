---
title: Serviceobjecten
description: De serviceobjecten zijn de activum en de producten van een klant waarvoor u een service kunt uitvoeren.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5641077de84b6702d2c5621edef74783f2f104fd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562318"
---
# <a name="service-objects"></a>Serviceobjecten 

[!include [banner](../includes/banner.md)]

De serviceobjecten zijn de activum en de producten van een klant waarvoor u een service kunt uitvoeren. Afhankelijk van het type service dat u levert, kunnen objecten tastbaar of ontastbaar zijn:

-  Tastbare objecten zijn bijvoorbeeld machines of gebouwen waarop u een fysieke servicetaak kunt uitvoeren.

    Een tastbaar serviceobject kan ook een voorraadartikel zijn dat u maakt in het formulier Vrijgegeven productdetails. Afhankelijk van de voorraaddimensiegroep die u aan het artikel koppelt, kunt u het serviceobject maken tot het detailniveau van het serienummer van het artikel bevat. Dit is handig wanneer u het artikel dat wordt aangeduid door het serviceobject precies moet bijhouden.

    Een tastbaar serviceobject kan een artikel zijn dat niet rechtstreeks is gerelateerd aan de directe productie of de keten van toeleveranciers. Bijvoorbeeld, een toolkit reparaties in die voor een serviceorder is gebruikt kan een serviceobject dat niet in voorraad is. In dit geval, registreert u het niet als voorraadartikel.

-  Ontastbare objecten zijn niet-fysieke entiteiten, zoals een set rekeningen of een juridisch document, waarop servicetaken kunnen worden uitgevoerd.

## <a name="example-of-an-intangible-service-object"></a>Voorbeeld van een serviceobject ontastbaar

Bedrijf A onderhouden de financiële records voor kleine verschillende bedrijven. Een van de klanten van bedrijf A is de plaatselijke voetbalvereniging, waarvoor bedrijf A de wekelijkse boekhouding en de jaarlijkse controle van de rekeningen van de vereniging uitvoert. De rekeningen van de vereniging zijn ingesteld in het formulier Serviceobjecten en worden in de serviceovereenkomst aangegeven als het object. Er zijn twee serviceovereenkomstregels voor het object. Regel 1 is wekelijkse boekhouding met een wekelijks interval die aan de regel is toegewezen, en regel 2 is de jaarlijkse controle met een jaarlijks interval die eraan is toegewezen.

## <a name="related-topics"></a>Verwante onderwerpen

[Serviceobjecten maken](create-service-objects.md)

