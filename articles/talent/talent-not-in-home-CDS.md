---
title: Talent wordt niet weergegeven tussen de Microsoft Dynamics 365-apps (CDS1.0)
description: In dit onderwerp wordt uitgelegd wat u moet doen als de klant de app Microsoft Dynamics 365 for Talent niet ziet tussen de Microsoft Dynamics 365-apps.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent wordt niet weergegeven tussen de Microsoft Dynamics 365-apps (CDS1.0)

[!include [banner](includes/banner.md)]

**Probleem**

De klant ziet de app Microsoft Dynamics 365 for Talent niet tussen de Microsoft Dynamics 365-apps.

**Resolutie**

De gebruiker moet worden toegevoegd aan de rol Maker omgeving in Microsoft PowerApps.

1. De beheerder met een PowerApps Plan 2-licentie moet de [PowerApps-beheerportal](https://preview.admin.powerapps.com/) openen.
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
