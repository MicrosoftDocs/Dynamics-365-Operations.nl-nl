---
title: Welkomst-e-mail wordt niet verzonden bij het aanmaken van nieuwe klanten
description: Dit artikel bevat richtlijnen voor het oplossen van problemen als een welkomstmelding per e-mail niet wordt verzonden wanneer een nieuwe klant wordt gemaakt in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219399"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Welkomst-e-mail wordt niet verzonden bij het aanmaken van nieuwe klanten

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor het oplossen van problemen als een welkomstmelding per e-mail niet wordt verzonden wanneer een nieuwe klant wordt gemaakt in Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Description

Wanneer er in Commerce Headquarters een nieuwe klant wordt gemaakt, wordt er een welkomst-e-mail naar de klant verzonden, zelfs als er een e-mailmelding is geconfigureerd voor het meldingstype **Klant is gemaakt**.

## <a name="resolution"></a>Oplossing

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Een e-mailmeldingsprofiel koppelen onder Commerce-parameters

1. Ga in headquarters naar **Retail en Commerce \> Instelling hoofdkantoor \> Parameters \> Commerce-parameters \> Algemeen**.
2. Selecteer in de vervolgkeuzelijst voor het **e-mailmeldingsprofiel** het e-mailmeldingsprofiel dat een koppeling bevat tussen het door de klant aangemaakte meldingstype en een door de klant aangemaakte e-mailsjabloon.  

> [!NOTE] 
> Wanneer u door klanten aangemaakte meldingen inschakelt, ontvangen klanten die zijn aangemaakt via alle kanalen binnen de rechtspersoon een door de klant aangemaakt e-mail. Op dit moment kunnen door de klant aangemaakte meldingen niet worden beperkt tot één kanaal.

Zie voor meer informatie [E-mailsjablonen maken voor transactiegebeurtenissen](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Aanvullende bronnen

[Een profiel voor e-mailmeldingen instellen](../email-notification-profiles.md)
