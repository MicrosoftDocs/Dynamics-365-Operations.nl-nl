---
title: Typen onderhoudsverzoeken
description: In dit onderwerp wordt uitgelegd hoe u typen onderhoudsverzoeken instelt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790481"
---
# <a name="maintenance-request-types"></a>Typen onderhoudsverzoeken

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Typen onderhoudsverzoeken worden gebruikt voor het categoriseren van onderhoudsverzoeken. Zo kunnen er typen onderhoudsverzoeken zijn die betrekking hebben op preventief onderhoud en correctief onderhoud. Of u hebt een speciaal type onderhoudsverzoek dat wordt gebruikt voor het beheren van reparatie van activa (depotreparatie).

Een type onderhoudsverzoek definieert de aansluiting met een levenscyclusstatusgroep met onderhoudsverzoeken (onderhoudslevenscyclusmodel). Levenscyclusmodellen voor onderhoudsverzoeken bepalen welke levenscyclusstatussen voor een onderhoudsverzoek kunnen worden ingesteld. (Voorbeelden van levenscyclusstatussen voor onderhoudsverzoeken **Gemaakt**, **Actief** en **Beëindigd**.)

1. Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudsverzoeken** \> **Typen onderhoudsverzoeken**.
2. Selecteer **Nieuw** als u een type onderhoudsverzoek wilt maken.
3. Voer in het veld **Type onderhoudsverzoek** een id in voor het type onderhoudsverzoek.
4. Voer in het veld **Naam** een naam in.
5. Ga naar het sneltabblad **Algemeen** en selecteer in het veld **Levenscyclusmodel voor onderhoudsverzoek** een levenscyclusmodel voor het onderhoudsverzoek.
6. Selecteer een type werkorder in het veld **Werkordertype**. Wanneer een onderhoudsverzoek wordt geconverteerd naar een werkorder, haalt de werkorder automatisch het werkordertype op dat is gerelateerd aan het type onderhoudsverzoek.

In de volgende afbeelding ziet u een voorbeeld van de pagina **Typen onderhoudsverzoeken**.

![Figuur 1](media/07-setup-for-requests.png)