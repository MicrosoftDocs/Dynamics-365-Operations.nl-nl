---
title: Prestatieverbeteringen bij opschonen van verkoophistorie
description: In dit onderwerp wordt de functie voor prestatieverbeteringen bij het opschonen van de verkoophistorie beschreven en wordt beschreven hoe u deze functie kunt inschakelen.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3c8ad7b0bd46c49fc989be091f44630a6a3eebc1
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985906"
---
# <a name="sales-history-cleanup-performance-improvements"></a>Prestatieverbeteringen bij opschonen van verkoophistorie

[!include [banner](../includes/banner.md)]

De periodieke batchtaak **Opschoning van verkoophistorie** kan veel tijd kosten als deze niet vaak in omgevingen wordt uitgevoerd met veel verkoopupdates. In deze situaties kan de functie *Prestatieverbeteringen bij opschonen van verkoophistorie* de uitvoeringsduur verminderen en de betrouwbaarheid verbeteren.

Met deze functie kunt u de bestaande opschoonfunctie op de volgende manieren verbeteren:

- De opschoning wordt opgesplitst in batches (u kunt de batchgrootte wijzigen via aanpassingen).
- De opschoning wordt maximaal 2 uur uitgevoerd (u kunt de duur wijzigen via aanpassingen).
- Waar mogelijk wordt gebruik gemaakt van databasemogelijkheden om vergrendelconflicten tot een minimum te beperken en samenvoeging van transactietabellen tijdens opschonen te voorkomen.

Nadat u de functie hebt ingeschakeld, wordt de batchtaak **Opschoning van verkoophistorie** (**Verkoop en marketing \> Periodieke taken \> Opschonen \> Opschoning van verkoophistorie**) uitgevoerd zoals eerder, maar met betere prestaties en maximaal twee uur. Dit betekent dat de taak mogelijk meerdere keren moet worden uitgevoerd om alle gegevens op te schonen voor een bepaalde periode.

## <a name="turn-on-the-sales-history-cleanup-performance-improvements-feature"></a>De functie Prestatieverbeteringen bij opschonen van verkoophistorie inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in de werkruimte **Functiebeheer** de functie als volgt in:

- **Module:** *Verkoop en marketing*
- **Functienaam:** *Prestatieverbeteringen bij opschonen van verkoophistorie*
