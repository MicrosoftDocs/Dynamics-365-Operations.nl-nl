---
title: Welkomste-mail wordt niet verzonden bij maken van nieuwe klanten
description: Dit onderwerp bevat richtlijnen voor het oplossen van problemen als een welkomstmelding per e-mail niet wordt verzonden wanneer een nieuwe klant wordt gemaakt in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349946"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Welkomste-mail wordt niet verzonden bij maken van nieuwe klanten

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor het oplossen van problemen als een welkomstmelding per e-mail niet wordt verzonden wanneer een nieuwe klant wordt gemaakt in Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Description

Wanneer er in Commerce Headquarters een nieuwe klant wordt gemaakt, wordt er een welkomst-e-mail naar de klant verzonden, zelfs als er een e-mailmelding is geconfigureerd voor het meldingstype **Klant is gemaakt**.

## <a name="resolution"></a>Oplossing

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>De juiste e-mail-id instellen voor het e-mailmeldingstype Klant is gemaakt

Volg deze stappen om de juiste waarde voor **E-mail-id** in te stellen voor het type e-mailmelding **Klant is gemaakt** in Headquarters.

1. Ga naar **Detailhandel en commerce \> Instellingen van hoofdkantoor \> E-mailmeldingsprofiel voor Commerce**.
1. Selecteer het e-mailmeldingsprofiel in het navigatievenster aan de linkerkant.
1. Stel onder **Instellingen voor meldingen van detailhandelgebeurtenisen** voor het type e-mailmelding **Klant is gemaakt** het veld **E-mail-id** in op **NewCust**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een profiel voor e-mailmeldingen instellen](../email-notification-profiles.md)
