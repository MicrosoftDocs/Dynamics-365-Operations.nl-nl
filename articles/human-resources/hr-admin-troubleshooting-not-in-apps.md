---
title: Human Resources wordt niet weergegeven in de Microsoft Dynamics 365-apps
description: In dit artikel wordt uitgelegd wat u moet doen als de klant de app Microsoft Dynamics 365 Human Resources niet ziet tussen de Microsoft Dynamics 365-apps.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 292db7e430bf0f2171f2b0a482ad70250774caec
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346341"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources wordt niet weergegeven in de Microsoft Dynamics 365-apps

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Uitgifte**

De klant ziet Dynamics 365 Human Resources niet tussen de Microsoft Dynamics 365-apps.

**Oplossing**

De gebruiker moet worden toegevoegd aan de rol Maker omgeving voor de omgeving in Microsoft Power Apps.

1. De beheerder met een Power Apps Plan 2-licentie moet het [Power Apps-Beheerportal](https://preview.admin.powerapps.com/) openen.

2. Selecteer **Omgevingen** en selecteer de juiste omgeving voor Human Resources.

3. Selecteer op het tabblad **Beveiliging** op het tabblad **Omgevingsrollen** de optie **Maker omgeving**.

    ![Het tabblad Omgevingsrollen.](media/environment-roles.png)

4. Voeg op het tabblad **Gebruikers** de gebruiker of uw organisatie toe.

    ![Het tabblad Gebruikers.](media/environment-maker.png)

5. Selecteer **Opslaan**.

6. De gebruiker moet zich nu aanmelden bij [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Selecteer **Synchroniseren** om de gebruikersapps bij te werken.

    ![De knop Synchroniseren.](media/get-more.png)

    Als de synchronisatie is voltooid, wordt Human Resources weergegeven op de startpagina.


[!INCLUDE[footer-include](../includes/footer-banner.md)]