---
title: Vertragingen
description: Dit onderwerp geeft informatie over vertragingsdatums in de hoofdplanning. Een vertragingsdatum is een realistische vervaldatum waarop een transactie wordt ontvangen als de eerste afhandelingsdatum die de hoofdplanning plant, later is dan de aangevraagde datum.
author: ChristianRytt
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e89830feea12b4f5703e0eda622729887dd9bf46
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573748"
---
# <a name="delays"></a>Vertragingen

[!include [banner](../includes/banner.md)]

Dit onderwerp geeft informatie over vertragingsdatums in de hoofdplanning. Een vertragingsdatum is een realistische vervaldatum waarop een transactie wordt ontvangen als de eerste afhandelingsdatum die de hoofdplanning plant, later is dan de aangevraagde datum.

Hoofdplanning kan de vroegste afrondingsdatum voor een transactie berekenen, op basis van levertijden, materiaalbeschikbaarheid, capaciteitsbeschikbaarheid en verschillende planningsparameters. 

Als hoofdplanning een orderdatum berekent die de huidige datum voorafgaat, kan de order niet op tijd worden afgerond. Daarom wordt de order vertraagd. In dit geval plant de hoofdplanning de order vooruit vanaf de huidige datum, inclusief levertijden. Deze levertijden beginnen met alle componentartikelen op lager niveau. De order krijgt vervolgens een vertraagde datum. Een vertraagde datum is een realistische vervaldatum op basis van de huidige gegevens. De hoofdplanning berekent ook het aantal vertragingdagen. 

In bepaalde situaties kiest u er misschien voor om vertragingen te berekenen, zoals wanneer gebruikers weten dat ze levertijden kunnen versnellen door alternatieve leveringsmethoden te selecteren. 

U kunt instellen hoe de vertragingen worden berekend voor een behoefteplanningsgroep. U kunt vervolgens de behoefteplanningsgroep later aan een artikel koppelen. 

Op de pagina **Parameters hoofdplanning** kunt u de begintijd instellen voor de berekening van vertragingen. Als een order na deze tijd wordt uitgevoerd, wordt aan de vertraagde datum van de order een vertraging van één dag toegevoegd. 

> [!NOTE]
> In eerdere versies stonden berekende vertragingen bekend als *vertragingsberichten*, werd de vertraagde datum *vertragingsdatum* genoemd en werd naar een vertraagde transactie verwezen als een *transactie die in de toekomst is ingesteld*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Beperkte vertragingen in productie-instellingen met meerdere stuklijstniveaus
Wanneer u met vertragingen werkt in een productie-instelling met meerdere stuklijstniveaus, is het belangrijk dat alleen de artikelen direct boven het artikel (in de stuklijststructuur) dat de vertraging veroorzaakt, worden bijgewerkt met een vertraging als onderdeel van de uitvoering van de hoofdplanning. Andere artikelen in de stuklijststructuur krijgen pas de vertraging bij de eerste uitvoering van de hoofdplanning, wanneer de geplande order voor het hoogste niveau wordt goedgekeurd of gefiatteerd. 

Om deze bekende beperking te omzeilen, kunnen de productieorders boven aan de stuklijststructuur met vertragingen worden goedgekeurd (of gefiatteerd) voordat de volgende uitvoering van de hoofdplanning wordt uitgevoerd. Op deze manier wordt de vertraging van de vertraagde goedgekeurde geplande productieorder behouden en worden alle onderliggende onderdelen dienovereenkomstig bijgewerkt.
Actieberichten kunnen ook worden gebruikt om geplande orders te identificeren die naar een latere datum kunnen worden verplaatst, vanwege andere vertragingen in de stuklijststructuur.

## <a name="desired-date"></a>Gewenste datum

Op de pagina **Geplande order** onder het tabblad **Vertragingen** staat de **Gewenste datum** voor de geplande order. De gewenste datum van een geplande order is de basisdatum voor vertragingen. Dit is een berekende datum die gelijk is aan de **Gevraagde datum** die is berekend op basis van de **Nettobehoefte**. Als de geplande order een stuklijstregel, productieregel of kanbanregel is, wordt de gewenste datum gebaseerd op de **Behoeftedatum** en wordt de gewenste datum niet weergegeven op de pagina **Geplande order**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Behoefteplanningsinstellingen](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]