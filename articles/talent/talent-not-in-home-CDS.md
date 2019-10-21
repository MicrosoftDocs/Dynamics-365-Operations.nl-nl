---
title: Talent wordt niet weergegeven tussen de Microsoft Dynamics 365-apps (Common Data Service 1.0)
description: In dit onderwerp wordt uitgelegd wat u moet doen als de klant de app Microsoft Dynamics 365 Talent niet ziet tussen de Microsoft Dynamics 365-apps.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 956af80a8ab2f454d9f523d3c74dda754ef0f793
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009371"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent wordt niet weergegeven tussen de Microsoft Dynamics 365-apps (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Uitgifte**

De klant ziet de Microsoft Dynamics 365 Talent-app niet tussen de Microsoft Dynamics 365-apps.

**Resolutie**

De gebruiker moet worden toegevoegd aan de rol Maker omgeving voor de omgeving in Microsoft PowerApps.

1. De beheerder met een PowerApps Plan 2-licentie moet het [PowerApps-Beheerportal](https://preview.admin.powerapps.com/) openen.
2. Selecteer **Omgevingen** en selecteer de juiste omgeving voor Talent.
3. Selecteer op het tabblad **Beveiliging** op het tabblad **Omgevingsrollen** de optie **Maker omgeving**.

    ![Het tabblad Omgevingsrollen](media/environment-roles.png)

4. Voeg op het tabblad **Gebruikers** de gebruiker of uw organisatie toe.

    ![Het tabblad Gebruikers](media/environment-maker.png)

5. Selecteer **Opslaan**.
6. De gebruiker moet zich nu aanmelden bij [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Selecteer **Synchroniseren** om de gebruikersapps bij te werken.

    ![De knop Synchroniseren](media/get-more.png)

    Als de synchronisatie is voltooid, wordt Talent weergegeven op de startpagina.
