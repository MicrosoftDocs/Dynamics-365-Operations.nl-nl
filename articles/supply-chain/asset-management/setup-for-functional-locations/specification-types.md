---
title: Typen onderhoudskenmerken
description: In dit onderwerp wordt uitgelegd hoe u kenmerktypen maakt in Activabeheer.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 283cff931ce665ae09152c8f3d3c976b7c8b66ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808515"
---
# <a name="maintenance-attribute-types"></a>Typen onderhoudskenmerken

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt uitgelegd hoe u kenmerktypen maakt in Activabeheer. Kenmerken worden gebruikt om de eigenschappen van verschillende elementen te beschrijven. U kunt kenmerken instellen voor de volgende elementen:

- [Functionele locatietypen](../setup-for-functional-locations/functional-location-types.md)
- [Functionele locaties maken](../functional-locations/create-functional-locations.md)
- [Typen activa](../setup-for-objects/object-types.md)
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]