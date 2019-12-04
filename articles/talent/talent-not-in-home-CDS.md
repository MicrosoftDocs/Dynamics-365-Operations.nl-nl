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
ms.openlocfilehash: 7f0cc1c7ec1234b7eedaade0ffadb66965ed2121
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772983"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent wordt niet weergegeven tussen de Microsoft Dynamics 365-apps (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Uitgifte**

De klant ziet de Microsoft Dynamics 365 Talent-app niet tussen de Microsoft Dynamics 365-apps.

**Resolutie**

De gebruiker moet worden toegevoegd aan de rol Maker omgeving voor de omgeving in Microsoft Power Apps.

1. De beheerder met een Power Apps Plan 2-licentie moet het [Power Apps-Beheerportal](https://preview.admin.powerapps.com/) openen.
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
