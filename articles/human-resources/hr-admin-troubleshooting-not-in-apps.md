---
title: Human Resources wordt niet weergegeven in de Microsoft Dynamics 365-apps
description: In dit onderwerp wordt uitgelegd wat u moet doen als Microsoft Dynamics 365 Human Resources niet wordt vermeld bij de Microsoft Dynamics365-apps.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a973b10a15846f7a27bff955deb2a961f45d9701
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687724"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>De Human Resources-app wordt niet weergegeven bij de Microsoft Dynamics 365-apps


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Probleem**

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
