---
title: Welkomst-e-mail wordt niet verzonden bij maken van nieuwe klanten
description: Dit artikel bevat richtlijnen voor het oplossen van problemen als een welkomstmelding per e-mail niet wordt verzonden wanneer een nieuwe klant wordt gemaakt in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853678"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Welkomst-e-mail wordt niet verzonden bij maken van nieuwe klanten

[!include [banner](../../includes/banner.md)]

Dit artikel bevat richtlijnen voor het oplossen van problemen als een welkomstmelding per e-mail niet wordt verzonden wanneer een nieuwe klant wordt gemaakt in Microsoft Dynamics 365 Commerce.

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
