---
title: Uw rekeningschema plannen
description: Dit artikel bevat informatie waarmee u het rekeningschema voor uw organisatie kunt plannen.
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4c57c4fe8cc66228062f7b64c88efe255657d016
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="plan-your-chart-of-accounts"></a>Uw rekeningschema plannen

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie waarmee u het rekeningschema voor uw organisatie kunt plannen.

Als u financiële gegevens in een organisatie wilt bijhouden en onderhouden, kunt u een rekeningschema instellen. Een rekeningschema is een verzameling van rekeningen waarmee een financieel raamwerk wordt gedefinieerd. Als u de transacties in deze rekeningen verder wilt bijhouden, kunt u segmenten toevoegen. Deze segmenten worden financiële dimensies genoemd. Een onkostenrekening kan bijvoorbeeld financiële dimensies bevatten met de naam Afdeling, Kostenplaats en Doel. Met door de gebruiker gedefinieerde regels, de zogenaamde rekeningstructuren en geavanceerde regels, wordt bepaald hoe financiële dimensies worden gekoppeld aan de hoofdrekeningen en andere financiële dimensies, en ook hoe transacties worden ingevoerd. 

Het rekeningschema is een gestructureerde lijst van de grootboekrekeningen van een rechtspersoon. De lijst wordt gebruikt om financiële rapporten voor te bereiden voor autoriteiten en eigenaren. De rekeningen worden gegroepeerd in typen rekeningen en worden verder in grotere categorieën samengevoegd. Op het meest algemene niveau zijn de rekeningen gegroepeerd als opbrengsten en kosten (exploitatierekeningen) en activa en passiva (balansrekeningen). 

Een rekeningschema kan door elke rechtspersoon in een organisatie worden gedeeld en gebruikt. Het rekeningschema dat door een rechtspersoon wordt gebruikt, wordt gedefinieerd op de pagina **Grootboek**. 

Hierna vindt u een aantal factoren waarmee u rekening dient te houden wanneer u de structuur van het rekeningschema voor uw organisatie plant:

-   De rapportagevereisten van het land/de regio waarin uw organisatie zich bevindt
-   De rapportage-eisen van uw rechtspersoon
-   De mate van specificatie die nodig is, zowel voor externe instanties als voor uw organisatie

Maak het rekeningschema op de pagina **Rekeningschema**. Hoofdrekeningen kunnen op de pagina **Rekeningschema** of de pagina **Hoofdrekeningen** worden gemaakt. Voor uw hoofdrekeningen mogen geen speciale tekens worden gebruikt die als scheidingstekens voor het rekeningschema worden gebruikt. Als u geen speciaal teken hebt dat hetzelfde is als het scheidingsteken van uw rekeningschema, kunt u instabiliteit ervaren of moet u mogelijk altijd zoekopdrachten of de flyout gebruiken wanneer u rekening- en dimensiecombinaties invoert. 

Het is daarom raadzaam de hoofdrekeningen te koppelen aan hoofdrekeningcategorieën, zodat u kunt profiteren van de financiële standaardrapporten zonder dat u wijzigingen hoeft aan te brengen. Zo kunt u rapporten sneller en eenvoudig ontwerpen en onderhouden. 

Gebruik de pagina **Rekeningstructuren configureren** om rekeningstructuren te configureren. Met rekeningstructuren worden geldige combinaties gedefinieerd. De combinaties vormen, samen met de hoofdrekeningen, een rekeningschema. 

**Overschrijvingen rechtspersoon** 

Niet alle hoofdrekeningen zijn geldig voor alle rechtspersonen en sommige hoofdrekeningen zijn mogelijk alleen relevant voor een specifiek tijdsbestek. In dit scenario kan de sectie Overschrijvingen rechtspersoon worden gebruikt om te bepalen voor welke bedrijven de hoofdrekening moet worden opgeschort, wie de eigenaar is en de periode gedurende welke de dimensie actief is. De overschrijvingen op het gedeelde niveau kunnen niet beperkender zijn dan de overschrijvingen op rechtspersoonniveau.

Zie voor meer informatie het onderwerp [Financiële dimensies](financial-dimensions.md).




