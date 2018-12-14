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

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="05148-103">Talent wordt niet weergegeven tussen de Microsoft Dynamics 365-apps (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="05148-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="05148-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="05148-104">**Issue**</span></span>

<span data-ttu-id="05148-105">De klant ziet de app Microsoft Dynamics 365 for Talent niet tussen de Microsoft Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="05148-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="05148-106">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="05148-106">**Resolution**</span></span>

<span data-ttu-id="05148-107">De gebruiker moet worden toegevoegd aan de rol Maker omgeving in Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="05148-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="05148-108">De beheerder met een PowerApps Plan 2-licentie moet de [PowerApps-beheerportal](https://preview.admin.powerapps.com/) openen.</span><span class="sxs-lookup"><span data-stu-id="05148-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="05148-109">Selecteer **Omgevingen** en selecteer de juiste omgeving voor Talent.</span><span class="sxs-lookup"><span data-stu-id="05148-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="05148-110">Selecteer op het tabblad **Beveiliging** op het tabblad **Omgevingsrollen** de optie **Maker omgeving**.</span><span class="sxs-lookup"><span data-stu-id="05148-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Het tabblad Omgevingsrollen](media/environment-roles.png)

4. <span data-ttu-id="05148-112">Voeg op het tabblad **Gebruikers** de gebruiker of uw organisatie toe.</span><span class="sxs-lookup"><span data-stu-id="05148-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Het tabblad Gebruikers](media/environment-maker.png)

5. <span data-ttu-id="05148-114">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="05148-114">Select **Save**.</span></span>
6. <span data-ttu-id="05148-115">De gebruiker moet zich nu aanmelden bij [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="05148-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="05148-116">Selecteer **Synchroniseren** om de gebruikersapps bij te werken.</span><span class="sxs-lookup"><span data-stu-id="05148-116">Select **Sync** to update the user apps.</span></span>

    ![De knop Synchroniseren](media/get-more.png)

    <span data-ttu-id="05148-118">Als de synchronisatie is voltooid, wordt Talent weergegeven op de startpagina.</span><span class="sxs-lookup"><span data-stu-id="05148-118">After synchronization is completed, Talent will appear on the home page.</span></span>

