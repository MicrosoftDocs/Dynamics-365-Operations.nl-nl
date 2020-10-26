---
title: Gebeurtenissen in app voor magazijnbeheer
description: In dit onderwerp wordt de verwerking van gebeurtenissen in de app voor magazijnbeheer beschreven die wordt gebruikt om gebeurtenisberichten van de app voor magazijnbeheer te verwerken als onderdeel van een batchtaak.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988370"
---
# <a name="warehouse-app-event-processing"></a>Verwerking van gebeurtenissen in de app voor magazijnbeheer

[!include [banner](../includes/banner.md)]

Batchtaken die worden uitgevoerd in Supply Chain Management kunnen gegevens uit een wachtrij verwerken voor de verwerking van gebeurtenissen die zijn uitgegeven door de app voor magazijnbeheer om zo nodig te reageren op de gesignaleerde gebeurtenissen. Deze functie voegt relevante gebeurtenissen toe aan de wachtrij als reactie op bepaalde typen acties die door medewerkers met de app worden uitgevoerd. Een voorbeeld is dat bij gebruik van de functie **Transferorders maken en verwerken vanuit de app voor magazijnbeheer** de koptekst en regels van de transferorder worden gemaakt en bijgewerkt in de back-end wanneer de batchtaak **Gebeurtenissen van de app voor magazijnbeheer verwerken** wordt uitgevoerd door het systeem.

## <a name="enable-the-process-warehouse-app-events-feature"></a>De functie Gebeurtenissen van de app voor magazijnbeheer verwerken inschakelen

Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem. Beheerders kunnen gebruikmaken van de pagina voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen. De functie Gebeurtenissen van de app voor magazijnbeheer verwerken staat vermeld als:

- **Module** - Magazijnbeheer
- **Functienaam**: gebeurtenissen van de app voor magazijnbeheer verwerken

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Een batchtaak instellen om gebeurtenissen van de app voor magazijnbeheer te verwerken

### <a name="process-warehouse-app-events"></a>Gebeurtenissen in app voor magazijnbeheer verwerken

Stel een geplande batc taak in om de gebeurtenissen van de app voor magazijnbeheer te verwerken voor het maken van transferorders en regelupdates.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Gebeurtenissen in app voor magazijnbeheer verwerken**.
1. Het dialoogvenster Gebeurtenissen in app voor magazijnbeheer verwerken wordt geopend. Vouw het sneltabblad **Op de achtergrond uitvoeren** uit en stel **Batchverwerking** in op **Ja**.
1. Selecteer op het tabblad **Op de achtergrond uitvoeren** de optie **Terugkeer**.
1. Het dialoogvenster **Terugkeerpatroon definiëren** wordt geopend. Stel het uitvoeringsschema in voor uw bedrijf.
1. Selecteer **OK** om terug te gaan naar het dialoogvenster **Gebeurtenissen in app voor magazijnbeheer verwerken**.
1. Selecteer **OK** in het dialoogvenster **Gebeurtenissen in app voor magazijnbeheer verwerken** om de batchtaak aan de batchwachtrij toe te voegen.

## <a name="query-warehouse-app-events"></a>Query's uitvoeren op gebeurtenissen in app voor magazijnbeheer

U kunt de gebeurtenissenwachtrij en gebeurtenisberichten die zijn gegenereerd door de magazijnapp weergeven door naar **Magazijnbeheer \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Gebeurtenissen in app voor magazijnbeheer** te gaan.

## <a name="the-standard-event-queue-process"></a>Het standaardproces voor de gebeurtenissenwachtrij

De wachtrij met gebeurtenissen in de app voor magazijnbeheer wordt doorgaans gebruikt met de volgende beschreven stroom:

1. Er wordt een gebeurtenis aan de wachtrij toegevoegd met een gebeurtenisbericht. Het nieuwe bericht heeft in eerste instantie de gebeurtenisstatus **Wachten**, wat betekent dat de batchtaak **Gebeurtenissen in app voor magazijnbeheer verwerken** dit bericht niet ophaalt en verwerkt.
1. Zodra de status van het bericht is gewijzigd in **In wachtrij**, wordt de gebeurtenis opgehaald en verwerkt door de batchtaak **Gebeurtenissen in app voor magazijnbeheer verwerken**.
1. Met de batchtaak worden de statuswaarden bijgewerkt naar **Voltooid** of **Mislukt**, afhankelijk van het feit of het aangevraagde proces mogelijk was.
1. Wanneer alle gerelateerde gebeurtenisberichten zijn **Voltooid**, wordt de gebeurtenis uit de wachtrij verwijderd.

 Zie [Transferorder maken vanuit proces van app voor magazijnbeheer](create-transfer-order-from-warehouse-app.md) voor een gedetailleerd voorbeeld.

## <a name="handle-event-errors"></a>Gebeurtenisfouten afhandelen

Als onderdeel van de verwerking van magazijngebeurtenissen ontvangt de aangevraagde berichtactiviteit mogelijk geen processen van de batchtaak. In dit geval wordt het gebeurtenisbericht gewijzigd in **Mislukt**. U kunt de informatie in **Batchlogboek** gebruiken om de oorzaak van problemen op te lossen en de benodigde actie te ondernemen.

Zie [Transferorder maken vanuit app voor magazijnbeheer](create-transfer-order-from-warehouse-app.md) voor een gedetailleerd voorbeeld.

U kunt een bericht over een mislukte gebeurtenis in de app voor magazijnbeheer als volgt opnieuw instellen:

1. Ga naar **Magazijnbeheer \> Query's en rapporten \> Logboeken voor mobiel apparaat \> Gebeurtenissen in app voor magazijnbeheer**.
1. Zoek en selecteer op het sneltabblad **Gebeurtenisberichten van de app voor magazijnbeheer** een relevante gebeurtenis waarvoor **Mislukt** wordt weergegeven in de kolom **Gebeurtenisstatus**.
1. Selecteer **Opnieuw instellen** op de werkbalk **Gebeurtenisberichten van de app voor magazijnbeheer**.
1. Ga door met werken totdat alle relevante berichten opnieuw zijn ingesteld.

U kunt een gebeurtenisbericht **Mislukt** ook verwijderen met de optie **Verwijderen** op de werkbalk **Gebeurtenisberichten van de app voor magazijnbeheer**.
