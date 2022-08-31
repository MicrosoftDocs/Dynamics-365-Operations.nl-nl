---
title: Extra locatiezones
description: Dit artikel biedt een overzicht van de nieuwe locatiezones die zijn toegevoegd aan Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336510"
---
# <a name="additional-location-zones"></a>Extra locatiezones

[!include [banner](../includes/banner.md)]

Er zijn drie nieuwe zonevelden beschikbaar in Microsoft Dynamics 365 Supply Chain Management. Magazijnbeheerders kunnen deze gebruiken om aanvullende magazijnorganisaties of -indelingen te definiëren. De nieuwe zonevelden kunnen handmatig of met de **wizard voor locatie-instelling** worden geconfigureerd. Deze kunnen worden gebruikt in query's of filters waarin de tabel Locaties wordt gebruikt.

Er is geen aanvullende configuratie nodig om de zonevelden te gebruiken.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>De functie Extra locatiezone in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Extra locatiezone* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="use-location-zones"></a>Locatiezones gebruiken

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Wizard voor locatie-instelling**.
2. Stel de volgende waarden in:

    - Selecteer **62** in het veld _Magazijn_.
    - Selecteer in het veld **Zone-id** de waarde _VERDIEPING_.
    - Selecteer in het veld **Extra zone 1** de waarde _PICKZONE_.
    - Selecteer in het veld **Extra zone 2** de waarde _WEBSHOP1_.
    - Selecteer in het veld **Locatieprofiel-ID** de waarde _VERDIEPING_.

3. Selecteer de regel **Verdieping**.
4. Voer in het veld **Vanaf nummer** de waarde _1_ in. Voer in het veld **Tot nummer** de waarde _3_ in.
5. Selecteer de regel **Aisle**.
6. Voer in het veld **Vanaf nummer** de waarde _1_ in. Voer in het veld **Tot nummer** de waarde _5_ in.
7. Selecteer **Maken**.
8. U ontvangt berichten waarin wordt vermeld dat nieuwe locaties zijn toegevoegd. Klik op de knop **Berichten weergeven** om de berichten weer te geven.
9. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**. De nieuwe locaties worden weergegeven in de lijst en alle zonevelden zijn beschikbaar (dat wil zeggen: het bestaande zoneveld en de nieuwe extra zonevelden).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]