---
title: Classificatieprofielen
description: In dit artikel wordt beschreven hoe u de gegevens voor beoordelingsprofielen instelt.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7408574187ddb099181bd2566c46c52307f603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850462"
---
# <a name="rating-profiles"></a>Classificatieprofielen

[!include [banner](../../includes/banner.md)]

Een beoordelingsprofiel lijkt op een logistiek contract (maar niet een wettelijk contract). Het wordt gebruikt om de transporttarieven voor ladingen te bepalen. 

Elk beoordelingsprofiel is uniek voor een vervoerder. In het profiel koppelt u de vervoerder aan een tariefmodel. Het tariefmodel definieert de tariefbasistoewijzingen en de tariefbasis. De tariefbasis bepaalt het tarief van de vervoerder.

U kunt een beoordelingsprofiel instellen met behulp van een pagina met een overzicht van alle bestaande beoordelingsprofielen. U kunt ook een beoordelingsprofiel rechtstreeks instellen vanaf de vervoerder. In beide gevallen is de informatie die u voor het beoordelingsprofiel hebt ingesteld, hetzelfde.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Een beoordelingsprofiel maken of bewerken op de pagina Beoordelingsprofielen

Op de pagina **Beoordelingsprofielen** kunt u alle beschikbare beoordelingsprofielen controleren. U kunt ook bestaande profielen bewerken en nieuwe profielen maken.

1. Ga naar **Transportbeheer \> Instellingen \> Beoordeling \> Beoordelingsprofiel**.
1. Selecteer in het actievenster **Nieuw** om een nieuw beoordelingsprofiel toe te voegen aan het raster of selecteer **Bewerken** om een bestaand profiel te bewerken.
1. Stel in de rij voor het nieuwe of bestaande beoordelingsprofiel de volgende velden in:

    - **Beoordelingsprofiel**: voer een unieke id in voor het beoordelingsprofiel.
    - **Naam**: voer een beschrijvende naam in voor het beoordelingsprofiel.
    - **Vervoerder**: selecteer een vervoerder. Het beoordelingsprofiel dat u instelt, wordt ook weergegeven op de pagina **Vervoerders** voor de geselecteerde vervoerder.
    - **Locatie** en **Magazijn**: Selecteer een locatie en magazijn.
    - **Tarief-engine**: selecteer de tarief-engine voor het beoordelingsprofiel.
    - **Tariefmodel**: selecteer het tariefmodel voor het beoordelingsprofiel. U kunt het tariefmodel gebruiken om een type tariefbasis en een tariefbasis te definiëren. Zie voor meer informatie [Tariefmodellen instellen](set-up-rate-masters.md).
    - **Transittijdengine**: selecteer de transittijdengine voor het beoordelingsprofiel.
    - **Brandstofindex**: selecteer de brandstofindex van de vervoerder voor het beoordelingsprofiel.
    - **Begindatum en -tijd** en **Einddatum en -tijd**: definieer de periode waarin het beoordelingsprofiel actief moet zijn.

1. Selecteer **Opslaan** in het actievenster.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Een beoordelingsprofiel direct op de pagina Vervoerders maken of bewerken

1. Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Vervoerders**.
1. Selecteer een vervoerder in de lijst.
1. Selecteer in het sneltabblad **Beoordelingsprofiel** de optie **Nieuw** om een beoordelingsprofiel te maken.
1. Stel de velden in voor het nieuwe beoordelingsprofiel. Deze velden komen overeen met de velden op de pagina **Beoordelingsprofielen**, zoals beschreven in het vorige gedeelte van dit artikel.

> [!NOTE]
> Profielen die op de pagina **Vervoerders** worden gemaakt, worden ook weergegeven op de pagina **Beoordelingsprofielen**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]