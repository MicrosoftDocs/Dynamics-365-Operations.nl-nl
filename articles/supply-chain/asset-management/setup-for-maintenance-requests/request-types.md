---
title: Typen onderhoudsverzoeken
description: In dit onderwerp wordt uitgelegd hoe u typen onderhoudsverzoeken instelt in Activabeheer.
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
ms.openlocfilehash: 4ff80b2f3e23f46467b8a2fe7a2abd805e5e3a20
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808491"
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

![Pagina Typen onderhoudsverzoeken](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]