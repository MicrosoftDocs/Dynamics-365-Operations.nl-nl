---
title: Uw rekeningschema plannen
description: Dit artikel bevat informatie waarmee u het rekeningschema voor uw organisatie kunt plannen.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 424ea5ce12d51d384c86878b7d2199bcd52c40f8
ms.contentlocale: nl-nl
ms.lasthandoff: 08/01/2017

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

Maak het rekeningschema op de pagina **Rekeningschema**. Hoofdrekeningen kunnen op de pagina **Rekeningschema** of de pagina **Hoofdrekeningen** worden gemaakt. Voor uw hoofdrekeningen mogen geen speciale tekens worden gebruikt die als scheidingstekens voor het rekeningschema worden gebruikt. Als u geen speciaal teken hebt dat hetzelfde is als het scheidingsteken van uw rekeningschema, kunt u instabiliteit ervaren of moet u mogelijk altijd zoekopdrachten of de flyout gebruiken wanneer u rekening- en dimensiecombinaties invoert. Zie [Een hoofdrekening maken](tasks/create-account-structures.md) voor meer informatie.


Het is daarom raadzaam de hoofdrekeningen te koppelen aan hoofdrekeningcategorieën, zodat u kunt profiteren van de financiële standaardrapporten zonder dat u wijzigingen hoeft aan te brengen. Zo kunt u rapporten sneller en eenvoudig ontwerpen en onderhouden. 

Gebruik de pagina **Rekeningstructuren configureren** om rekeningstructuren te configureren. Met rekeningstructuren worden geldige combinaties gedefinieerd. De combinaties vormen, samen met de hoofdrekeningen, een rekeningschema.  Zie [Rekeningstructuren maken](tasks/create-main-account.md) voor meer informatie.

**Overschrijvingen rechtspersoon** 

Niet alle hoofdrekeningen zijn geldig voor alle rechtspersonen en sommige hoofdrekeningen zijn mogelijk alleen relevant voor een specifiek tijdsbestek. In dit scenario kan de sectie Overschrijvingen rechtspersoon worden gebruikt om te bepalen voor welke bedrijven de hoofdrekening moet worden opgeschort, wie de eigenaar is en de periode gedurende welke de dimensie actief is. De overschrijvingen op het gedeelde niveau kunnen niet beperkender zijn dan de overschrijvingen op rechtspersoonniveau.

Zie de volgende onderwerpen voor meer informatie: [Financiële dimensies](financial-dimensions.md)
[Geavanceerde regelstructuren maken en toewijzen](tasks/create-assign-advanced-rule-structures.md)



