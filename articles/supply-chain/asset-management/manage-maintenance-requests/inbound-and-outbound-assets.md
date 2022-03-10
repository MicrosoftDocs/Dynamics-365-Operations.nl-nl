---
title: Inkomende en uitgaande activa
description: In dit onderwerp wordt uitgelegd hoe u inkomende en uitgaande activa registreert in Activabeheer.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0bd3127df1b583acc6841c3e115d3beceabcab2756098e567b2269c1dcc94004
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759618"
---
# <a name="inbound-and-outbound-assets"></a>Inkomende en uitgaande activa

[!include [banner](../../includes/banner.md)]

 

Als uw bedrijf reparaties of onderhoudstaken uitvoert aan activa die van andere locaties of klanten worden ontvangen, kan Activabeheer zowel inkomende activa die op weg zijn naar uw bedrijf als uitgaande activa die worden geretourneerd volgen.

> [!NOTE]
> Als u de inkomende en uitgaande levenscyclusstatussen wilt gebruiken om de binnenkomende en terugkerende activa te beheren, moet u de levenscyclusstatussen en levenscyclusmodellen voor onderhoudsverzoeken instellen om deze acties te ondersteunen. Zie [Onderhoudsaanvragen](../setup-for-maintenance-requests/requests.md) voor meer informatie.

De instellingen van Activabeheer bepalen of u met inkomende en uitgaande activa kunt werken.

## <a name="register-assets-as-inbound"></a>Activa registreren als inkomend

1. Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Actieve onderhoudsverzoeken**.
2. Selecteer het onderhoudsverzoek.
3. Selecteer **Status van onderhoudsverzoek bijwerken**.
4. Selecteer **Inkomend** (of een andere levenscyclusstatus die u hebt gemaakt voor inkomende activa) en selecteer **OK**.

![Activa registreren als inkomend.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Inkomende activa registreren als ontvangen

1. Selecteer **Activabeheer** \> **Algemeen** \> **Inkomend/uitgaand** \> **Inkomende activa**.
2. Selecteer het activum of het onderhoudsverzoek.
3. Selecteer **Activa ontvangen**.
4. Voer de datum en de tijd in het veld **Ontvangen** in. Selecteer vervolgens **OK**. De record wordt verwijderd uit de pagina met de lijst **Inkomende activa**.

![Inkomende activa registreren als ontvangen.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Activa registreren als uitgaand

Wanneer u de onderhouds- of reparatietaak hebt voltooid, kunt u het activum als geretourneerd registreren.

1. Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Actieve onderhoudsverzoeken**.
2. Selecteer het onderhoudsverzoek.
3. Selecteer **Status van onderhoudsverzoek bijwerken**.
4. Selecteer **Uitgaand** (of een andere levenscyclusstatus die u hebt gemaakt voor uitgaande activa) en selecteer **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Uitgaande activa registreren als afgeleverd

1. Selecteer **Activabeheer** \> **Algemeen** \> **Inkomend/uitgaand** \> **Uitgaande activa**.
2. Selecteer het activum of het onderhoudsverzoek.
3. Selecteer **Activa afleveren**.
4. Voer de datum en de tijd in het veld **Afgeleverd** in. Selecteer vervolgens **OK**. De record wordt verwijderd uit de pagina met de lijst **Uitgaande activa**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]