---
title: Een online functionaliteitsprofiel maken
description: In dit artikel wordt beschreven hoe u een online functionaliteitsprofiel maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5ce81900cd0648132748167d03906afc64e97f25
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276796"
---
# <a name="create-an-online-functionality-profile"></a>Een online functionaliteitsprofiel maken

[!include [banner](includes/banner.md)]

Dit artikel bevat een overzicht van het instellen van een online functionaliteitsprofiel voor Microsoft Dynamics 365 Commerce.

Het online functionaliteitsprofiel biedt verschillende instellingen voor online kanalen. In elk online kanaal moet een online functionaliteitsprofiel worden opgegeven.

## <a name="create-an-online-functionality-profile"></a>Een online functionaliteitsprofiel maken

In de volgende procedure wordt beschreven hoe u een online functionaliteitsprofiel maakt vanuit de Commerce Headquarters-app.

1. Ga in het navigatievenster naar **Modules \> Kanaalinstelling \> Onlinewinkel instellen \> Functionaliteitsprofielen**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Profiel** een id voor het profiel in.
1. Voer in het veld **Beschrijving** een waarde in ('Profiel van Adventure Works' in de voorbeeldafbeelding hieronder).
1. Wijzig indien nodig in de sectie **Functies** de instellingen **WINKELWAGEN**, **DETAILHANDELKLANTEN** of **UITCHECKEN**.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van een online functionaliteitsprofiel.
  
![Voorbeeld van online functionaliteitprofiel.](media/online-functionality-profile.png)

## <a name="functions"></a>Functies

- **Producten samenvoegen**: als deze functie is ingeschakeld, kan de winkelwagen de hoeveelheid bijwerken wanneer hetzelfde artikel meerdere keren wordt toegevoegd.
- **Uitchecken zonder betalingen toestaan**: als deze functie is ingeschakeld, wordt het scenario verwerkt waarbij artikelen die aan de winkelwagen zijn toegevoegd een prijs van $ 0,00 hebben.
- **Klant maken in asynchrone modus**: dit is een verouderde instelling die van toepassing is op e-Commerce-kanalen van derden en is niet van toepassing op de Dynamics 365 e-Commerce-site.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van kanalen](channels-overview.md)

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Een online afzetkanaal instellen](channel-setup-online.md)

[Een detailhandelafzetkanaal instellen](channel-setup-retail.md)

[Een callcenterkanaal instellen](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
