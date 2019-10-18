---
title: Typen onderhoudskenmerken
description: In dit onderwerp wordt uitgelegd hoe u kenmerktypen maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 067d1085d9afa04cb76b78393a8a8b9834ce4d8c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250939"
---
# <a name="maintenance-attribute-types"></a>Typen onderhoudskenmerken

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u kenmerktypen maakt in Activabeheer. Kenmerken worden gebruikt om de eigenschappen van verschillende elementen te beschrijven. U kunt kenmerken instellen voor de volgende elementen:

- [Typen functionele locaties](../setup-for-functional-locations/functional-location-types.md)
- [Functionele locaties](../functional-locations/create-functional-locations.md)
- [Activatypen](../setup-for-objects/object-types.md)
- Activa

De kenmerken die u kunt instellen, variëren, afhankelijk van het element. Zo kunt u bijvoorbeeld voor een functionele locatie kenmerken instellen voor de configuratie en de fysieke grootte van de locatie. Voor een activatype of een activum kunt u kenmerken instellen voor motorinhoud, stroomverbruik en maximale belastingscapaciteit onder verschillende omstandigheden.

## <a name="create-attribute-types"></a>Kenmerktypen maken

U kunt uw eigen kenmerktypen maken Bovendien kunt u productdimensies overbrengen naar de pagina **Kenmerktypen**.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Kenmerktypen**.
2. Wanneer u voor het eerst kenmerktypen instelt, selecteert u **Productdimensies maken** om automatisch standaard productdimensies over te zetten.
3. Selecteer **Nieuw** om een nieuw kenmerktype te maken.
4. Voer in het veld **Kenmerktype** een naam in voor het kenmerktype.
5. Voer in het veld **Beschrijving** een beschrijving in.
6. Selecteer indien nodig in het veld **Eenheid** de relevante kenmerkeenheid.
7. Selecteer in het veld **Gegevenstype** een gegevenstype voor de eenheid.
8. Als u **Tekenreeks** hebt geselecteerd als gegevenstype, voert u de volgende stappen uit om waarden voor het kenmerktype te maken:

    1. Selecteer het kenmerktype en selecteer vervolgens **Waarden**.
    2. Selecteer **Nieuw** in het veld **Kenmerkwaarden**.
    3. Selecteer een kenmerktype (dimensie) in het veld **Kenmerktype**.
    4. Voer een gerelateerde waarde in het veld **Waarde** in.
    5. Voer in het veld **Beschrijving** een beschrijving in.
    6. Sla de record op.
    7. Ga terug naar de pagina **Kenmerktypen**.

9. Sla de record op.

    Het veld **Typen functionele locatie** bevat het aantal functionele locaties dat het kenmerktype gebruikt. Het veld **Activatypen** bevat het aantal activatypen dat hiervan gebruikmaakt.
