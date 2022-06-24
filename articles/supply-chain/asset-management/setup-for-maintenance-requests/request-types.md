---
title: Typen onderhoudsverzoek
description: In dit artikel wordt uitgelegd hoe u typen onderhoudsverzoeken instelt in Activabeheer.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a2d707cc9c0aa4863968651a8434883cc1322eb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888696"
---
# <a name="maintenance-request-types"></a>Typen onderhoudsverzoeken

[!include [banner](../../includes/banner.md)]

 

Typen onderhoudsverzoeken worden gebruikt voor het categoriseren van onderhoudsverzoeken. Zo kunnen er typen onderhoudsverzoeken zijn die betrekking hebben op preventief onderhoud en correctief onderhoud. Of u hebt een speciaal type onderhoudsverzoek dat wordt gebruikt voor het beheren van reparatie van activa (depotreparatie).

Een type onderhoudsverzoek definieert de aansluiting met een levenscyclusstatusgroep met onderhoudsverzoeken (onderhoudslevenscyclusmodel). Levenscyclusmodellen voor onderhoudsverzoeken bepalen welke levenscyclusstatussen voor een onderhoudsverzoek kunnen worden ingesteld. (Voorbeelden van levenscyclusstatussen voor onderhoudsverzoeken **Gemaakt**, **Actief** en **Beëindigd**.)

1. Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudsverzoeken** \> **Typen onderhoudsverzoeken**.
2. Selecteer **Nieuw** als u een type onderhoudsverzoek wilt maken.
3. Voer in het veld **Type onderhoudsverzoek** een id in voor het type onderhoudsverzoek.
4. Voer in het veld **Naam** een naam in.
5. Ga naar het sneltabblad **Algemeen** en selecteer in het veld **Levenscyclusmodel voor onderhoudsverzoek** een levenscyclusmodel voor het onderhoudsverzoek.
6. Selecteer een type werkorder in het veld **Werkordertype**. Wanneer een onderhoudsverzoek wordt geconverteerd naar een werkorder, haalt de werkorder automatisch het werkordertype op dat is gerelateerd aan het type onderhoudsverzoek.

In de volgende afbeelding ziet u een voorbeeld van de pagina **Typen onderhoudsverzoeken**.

![Pagina Typen onderhoudsverzoeken.](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]