---
title: Verbeterde afhandeling van artikelen met batchtracering
description: In dit onderwerp wordt de verbeterde afhandeling van artikelen met batchtracering tijdens het proces voor boeken van overzichten in Microsoft Dynamics 365 Commerce beschreven.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 513b6ca84fa71e851a5a3e4275e0b6572789e1eb
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485778"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Verbeterde afhandeling van artikelen met batchtracering

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de verbeterde afhandeling van artikelen met batchtracering tijdens het proces voor boeken van overzichten in Microsoft Dynamics 365 Commerce beschreven.

In Dynamics 365 Commerce POS (Point of Sale) kunnen op het moment van verkoop geen batchnummers worden vastgelegd voor artikelen met batchtracering. Voor specifieke configuraties wanneer de verkoop wordt geboekt in Commerce Headquarters via klantorders of het boeken van overzichten, verwacht Commerce dat er geldige batchnummers bestaan voor artikelen met batchtracering en dat deze worden gebruikt bij de facturering.

Als er geldige batchnummers beschikbaar zijn voor producten, worden deze op basis van de overzichtsboekingen gebruikt door de factureringsprocessen voor klant- en verkooporders. Als er geen geldige batchnummers beschikbaar zijn voor producten, kan het factureringsproces voor de klantorder niet worden geboekt en ontvangt de POS-gebruiker een foutbericht. De overzichtsboeking krijgt vervolgens een foutstatus, zelfs als negatieve voorraad is ingeschakeld voor de producten.

Verbeteringen in Commerce zorgen ervoor dat als negatieve voorraad is ingeschakeld voor artikelen met batchtracering, de facturering van klantorders en verkooporders via overzichtsboekingen niet wordt geblokkeerd voor deze artikelen als de voorraad 0 (nul) is of er geen batchnummer beschikbaar is. In de verbeterde functionaliteit wordt een standaard batch-id gebruikt voor de verkoopregels wanneer er geen batchnummers beschikbaar zijn.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>De standaard batch-id definiëren die voor klantorders wordt gebruikt

Ga als volgt te werk om de standaard batch-id te definiëren die voor klantorders wordt gebruikt.

1. Ga in Commerce Headquarters naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters**.
1. Voer op het tabblad **Klantorders** op het sneltabblad **Order** een waarde in het veld **Standaard batch-id** in.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>De standaard batch-id definiëren die wordt gebruikt voor het factureren van verkooporders via het boeken van overzichten

Ga als volgt te werk om de standaard batch-id te definiëren die wordt gebruikt voor het factureren van verkooporders via overzichtsboekingen.

1. Ga in Commerce Headquarters naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters**.
1. Voer op het tabblad **Boeking** op het sneltabblad **Voorraad bijwerken** een waarde in het veld **Standaard batch-id** in.

> [!NOTE]
> - De functionaliteit Standaard batch-id is alleen beschikbaar wanneer geavanceerde magazijnfuncties zijn ingeschakeld voor het specifieke winkelmagazijn en de artikelen. In een latere versie wordt de functionaliteit voor standaard batch-id's ook ondersteund voor scenario's waarbij geavanceerd magazijnbeheer niet is ingeschakeld.
> - Ondersteuning voor de verbeterde afhandeling van artikelen met batchtracering tijdens overzichtsboekingen voor niet-geavanceerde magazijnbeheerscenario's is geïntroduceerd in versie 10.0.5 van Commerce.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
