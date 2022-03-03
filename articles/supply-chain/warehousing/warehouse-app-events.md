---
title: Gebeurtenissen in app voor magazijnbeheer
description: In dit onderwerp wordt de verwerking van gebeurtenissen in de app voor magazijnbeheer beschreven die wordt gebruikt om gebeurtenisberichten van de app voor magazijnbeheer te verwerken als onderdeel van een batchtaak.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8c92bf179006d668f8673e9abc3419a10e644184
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103258"
---
# <a name="warehouse-app-event-processing"></a>Verwerking van gebeurtenissen in de app voor magazijnbeheer

[!include [banner](../includes/banner.md)]

Batchtaken die worden uitgevoerd in Supply Chain Management kunnen gegevens uit een wachtrij verwerken voor de verwerking van gebeurtenissen die zijn uitgegeven door de mobiele app Magazijnbeheer om zo nodig te reageren op de gesignaleerde gebeurtenissen. Deze functie voegt relevante gebeurtenissen toe aan de wachtrij als reactie op bepaalde typen acties die door medewerkers met de app worden uitgevoerd. Een voorbeeld is dat bij gebruik van de functie *overboekingsorders maken en verwerken vanuit de app voor magazijnbeheer* de koptekst en regels van de overboekingsorder worden gemaakt en bijgewerkt in de back-end wanneer de batchtaak **Gebeurtenissen van de app voor magazijnbeheer verwerken** wordt uitgevoerd door het systeem.

## <a name="turn-the-process-warehouse-app-events-feature-on-or-off"></a>De functie Gebeurtenissen in magazijnapp verwerken in- of uitschakelen

Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Gebeurtenissen in magazijnapp verwerken* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Een batchtaak instellen om gebeurtenissen van de app voor magazijnbeheer te verwerken

### <a name="process-warehouse-app-events"></a>Gebeurtenissen in magazijnapp verwerken

Stel een geplande batc taak in om de gebeurtenissen van de app voor magazijnbeheer te verwerken voor het maken van overboekingsorders en regelupdates.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Gebeurtenissen in app voor magazijnbeheer verwerken**.
1. Het dialoogvenster Gebeurtenissen in app voor magazijnbeheer verwerken wordt geopend. Vouw het sneltabblad **Op de achtergrond uitvoeren** uit en stel **Batchverwerking** in op **Ja**.
1. Selecteer op het tabblad **Op de achtergrond uitvoeren** de optie **Terugkeer**.
1. Het dialoogvenster **Terugkeerpatroon definiëren** wordt geopend. Stel het uitvoeringsschema in voor uw bedrijf.
1. Selecteer **OK** om terug te gaan naar het dialoogvenster **Gebeurtenissen in app voor magazijnbeheer verwerken**.
1. Selecteer **OK** in het dialoogvenster **Gebeurtenissen in app voor magazijnbeheer verwerken** om de batchtaak aan de batchwachtrij toe te voegen.

## <a name="query-warehouse-app-events"></a>Query's uitvoeren op gebeurtenissen in app voor magazijnbeheer

U kunt de gebeurtenissenwachtrij en gebeurtenisberichten die zijn gegenereerd door de mobiele app Magazijnbeheer weergeven door naar **Magazijnbeheer \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Gebeurtenissen in app voor magazijnbeheer** te gaan.

## <a name="the-standard-event-queue-process"></a>Het standaardproces voor de gebeurtenissenwachtrij

De wachtrij met gebeurtenissen in de app voor magazijnbeheer wordt doorgaans gebruikt met de volgende beschreven stroom:

1. Er wordt een gebeurtenis aan de wachtrij toegevoegd met een gebeurtenisbericht. Het nieuwe bericht heeft in eerste instantie de gebeurtenisstatus **Wachten**, wat betekent dat de batchtaak **Gebeurtenissen in app voor magazijnbeheer verwerken** dit bericht niet ophaalt en verwerkt.
1. Zodra de status van het bericht is gewijzigd in **In wachtrij**, wordt de gebeurtenis opgehaald en verwerkt door de batchtaak **Gebeurtenissen in app voor magazijnbeheer verwerken**.
1. Met de batchtaak worden de statuswaarden bijgewerkt naar **Voltooid** of **Mislukt**, afhankelijk van het feit of het aangevraagde proces mogelijk was.
1. Wanneer alle gerelateerde gebeurtenisberichten zijn **Voltooid**, wordt de gebeurtenis uit de wachtrij verwijderd.

 Zie [overboekingsorder maken vanuit proces van app voor magazijnbeheer](create-transfer-order-from-warehouse-app.md) voor een gedetailleerd voorbeeld.

## <a name="handle-event-errors"></a>Gebeurtenisfouten afhandelen

Als onderdeel van de verwerking van magazijngebeurtenissen ontvangt de aangevraagde berichtactiviteit mogelijk geen processen van de batchtaak. In dit geval wordt het gebeurtenisbericht gewijzigd in **Mislukt**. U kunt de informatie in **Batchlogboek** gebruiken om de oorzaak van problemen op te lossen en de benodigde actie te ondernemen.

Zie [overboekingsorder maken vanuit app voor magazijnbeheer](create-transfer-order-from-warehouse-app.md) voor een gedetailleerd voorbeeld.

U kunt een bericht over een mislukte gebeurtenis in de app voor magazijnbeheer als volgt opnieuw instellen:

1. Ga naar **Magazijnbeheer \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Gebeurtenissen in app voor magazijnbeheer**.
1. Zoek en selecteer op het sneltabblad **Gebeurtenisberichten van de app voor magazijnbeheer** een relevante gebeurtenis waarvoor **Mislukt** wordt weergegeven in de kolom **Gebeurtenisstatus**.
1. Selecteer **Opnieuw instellen** op de werkbalk **Gebeurtenisberichten van de app voor magazijnbeheer**.
1. Ga door met werken totdat alle relevante berichten opnieuw zijn ingesteld.

U kunt een gebeurtenisbericht **Mislukt** ook verwijderen met de optie **Verwijderen** op de werkbalk **Gebeurtenisberichten van de app voor magazijnbeheer**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]