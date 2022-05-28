---
title: Bijhouden van updates voor wegzetten
description: In dit onderwerp wordt beschreven hoe u de taak Bijhouden van updates voor wegzetten kunt instellen en uitvoeren om periodieke taken weg te zetten.
author: Weijiesa
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f02ba71b4eb32551cebc6cf160f0285eac8ae7ad
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673965"
---
# <a name="update-tracking-for-put-away"></a>Bijhouden van updates voor wegzetten

[!include [banner](../includes/banner.md)]

De periodieke taak *Bijhouden van updates voor wegzetten* is ontworpen om 's nachts als een terugkerende batch te worden uitgevoerd. Het geeft aan welke reizen alle voorraadtransacties hebben ontvangen en welke reizen geen waarde hebben voor de werkelijke einddatum. Vervolgens wordt de werkelijke einddatum op de huidige datum ingesteld.

*Containeractiviteiten* worden voor elke *etappe* van een reis voor elke *verzendcontainer* gemaakt. Deze waarden worden gedefinieerd door de reissjabloon die wordt geselecteerd wanneer er een reis wordt gemaakt. Voor elke record met activiteiten voor een container kunnen waarden worden ingesteld voor de velden **Begindatum**, **Geschatte einddatum** en **Werkelijke einddatum**. Deze velden kunnen worden bijgewerkt wanneer er een bevestiging wordt ontvangen dat een etappe is begonnen of is voltooid.

Meestal worden gegevens die betrekking hebben op bevestigde datums verstrekt door een derde partij, zoals een expediteur, omdat deze acties niet in Microsoft Dynamics 365 Supply Chain Management worden beheerd. Informatie van een derde partij is echter niet vereist om de ontvangst van goederen van een etappe van een reis in het magazijn bij te houden (zoals is gemarkeerd door het wegzetten van goederen). Het bijhouden kan dus worden bepaald op basis van informatie in Dynamics 365 Supply Chain Management.

Als u de periodieke taak *Bijhouden van updates voor wegzetten* wilt instellen, neemt u de volgende stappen:

1. Ga naar **Francoprijzen \> Periodieke taken \> Bijhouden van updates voor wegzetten**.
1. Stel in het dialoogvenster **Bijhouden van updates voor wegzetten** in het gedeelte **Parameters** de volgende velden in:

    - **Etappe**: selecteer de unieke id-naam/-nummer voor het gedeelte van een reis waarvoor u updates wilt bijhouden. De geselecteerde waarde moet staan voor de ontvangst van de reis bij het magazijn.
    - **Activiteit**: selecteer de activiteit die tijdens de geselecteerde etappe is uitgevoerd. Deze waarden worden per regel van het trajectsjabloon in het traceringscontrolecentrum toegewezen.

1. Als u de set met records wilt beperken die in de update moeten worden opgenomen, selecteert u op het sneltabblad **Op te nemen records** de knop **Filteren**. Er wordt een standaarddialoogvenster voor query's weergegeven, waarin u selectiecriteria, sorteercriteria en joins kunt definiëren. De velden werken op dezelfde manier als bij andere typen query's in Supply Chain Management. De velden hier zijn alleen-lezen en bevatten waarden die betrekking hebben op de query.
1. Stel op het sneltabblad **Uitvoeren op achtergrond** desgewenst batch- en planningsopties in, op dezelfde manier als u doet voor andere typen taken in Supply Chain Management.
1. Selecteer **OK** om de instellingen toe te passen en om de update uit te voeren of te plannen.
