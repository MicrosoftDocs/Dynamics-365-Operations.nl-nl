---
title: Uw rekeningschema plannen
description: Dit onderwerp bevat informatie waarmee u het rekeningschema voor uw organisatie kunt plannen.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26f7ca1fa539fb0cf69a7759e92c5e735bd41211
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846770"
---
# <a name="plan-your-chart-of-accounts"></a>Uw rekeningschema plannen

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie waarmee u het rekeningschema voor uw organisatie kunt plannen.

Als u financiële gegevens in een organisatie wilt bijhouden en onderhouden, kunt u een rekeningschema instellen. Een rekeningschema is een verzameling van rekeningen waarmee een financieel raamwerk wordt gedefinieerd. Als u de transacties in deze rekeningen wilt bijhouden, kunt u segmenten toevoegen. Deze segmenten worden financiële dimensies genoemd. Een onkostenrekening kan bijvoorbeeld financiële dimensies bevatten met de naam Afdeling, Kostenplaats en Doel. Met door de gebruiker gedefinieerde regels wordt bepaald hoe financiële dimensies worden gekoppeld aan de hoofdrekeningen en andere financiële dimensies, en ook hoe transacties worden ingevoerd. Deze door de gebruiker gedefinieerde regels worden rekeningstructuren en geavanceerde regels genoemd.

Het rekeningschema is een gestructureerde lijst van de grootboekrekeningen van een rechtspersoon. De lijst wordt gebruikt om financiële rapporten voor te bereiden voor autoriteiten en eigenaren. De rekeningen worden eerst gegroepeerd in typen rekeningen en worden verder in grotere categorieën samengevoegd. Op het meest algemene niveau zijn de rekeningen gegroepeerd als opbrengsten en kosten (exploitatierekeningen) en activa en passiva (balansrekeningen).

Een rekeningschema kan door elke rechtspersoon in een organisatie worden gedeeld en gebruikt. Het rekeningschema dat door een rechtspersoon wordt gebruikt, wordt gedefinieerd op de pagina **Grootboek**.

Hierna vindt u een aantal factoren waarmee u rekening dient te houden wanneer u de structuur van het rekeningschema voor uw organisatie plant:

- De rapportagevereisten van het land of de regio waarin uw organisatie zich bevindt
- De rapportage-eisen van uw rechtspersoon
- De mate van specificatie die nodig is, zowel voor externe instanties als voor uw organisatie

U maakt het rekeningschema op de pagina **Rekeningschema**. U kunt hoofdrekeningen maken op de pagina **Rekeningschema** of de pagina **Hoofdrekeningen**. Voor uw hoofdrekeningen mogen geen speciale tekens worden gebruikt die als scheidingstekens voor het rekeningschema worden gebruikt. Anders wordt het systeem instabiel of moet u altijd wellicht zoekopdrachten of het dialoogvenster gebruiken wanneer u combinaties van rekeningen en dimensies opgeeft. Zie [Een hoofdrekening maken](tasks/create-main-account.md) voor meer informatie.

> [!NOTE]
> In Microsoft Dynamics for Finance and Operations versie 8.0 (april 2018) kunt u het scheidingsteken uit het rekeningschema van de pagina **Grootboekparameters** wijzigen.

Het is daarom raadzaam de hoofdrekeningen te koppelen aan hoofdrekeningcategorieën, zodat u kunt profiteren van de financiële standaardrapporten zonder dat u wijzigingen hoeft aan te brengen. Zo kunt u rapporten sneller en eenvoudig ontwerpen en onderhouden.

U kunt rekeningstructuren maken op de pagina **Rekeningstructuren configureren**. Met rekeningstructuren worden geldige combinaties gedefinieerd. Deze combinaties vormen, samen met de hoofdrekeningen, een rekeningschema. Zie [Rekeningstructuren maken](tasks/create-account-structures.md) voor meer informatie.

**Overschrijvingen rechtspersoon**

Niet alle hoofdrekeningen zijn geldig voor alle rechtspersonen en sommige hoofdrekeningen zijn mogelijk alleen relevant voor een specifiek tijdsbestek. In dit scenario kunt u de sectie **Overschrijvingen rechtspersoon** gebruiken om de bedrijven te identificeren waarvoor de hoofdrekening moet worden opgeschort, wie de eigenaar is en gedurende welke periode de dimensie actief is. De overschrijvingen op het gedeelde niveau kunnen niet beperkender zijn dan de overschrijvingen op rechtspersoonniveau.

Zie de volgende onderwerpen voor meer informatie:

- [Financiële dimensies](financial-dimensions.md)
- [Geavanceerde regelstructuren maken en toewijzen](tasks/create-assign-advanced-rule-structures.md)
