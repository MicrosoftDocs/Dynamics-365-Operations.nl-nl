---
title: Human Resources wordt niet weergegeven in de Microsoft Dynamics 365-apps
description: In dit artikel wordt uitgelegd wat u moet doen als de klant de app Microsoft Dynamics 365 Human Resources niet ziet tussen de Microsoft Dynamics 365-apps.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008692"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="f4ddb-103">Human Resources wordt niet weergegeven in de Microsoft Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="f4ddb-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="f4ddb-104">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="f4ddb-104">**Issue**</span></span>

<span data-ttu-id="f4ddb-105">De klant ziet Dynamics 365 Human Resources niet tussen de Microsoft Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="f4ddb-106">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="f4ddb-106">**Resolution**</span></span>

<span data-ttu-id="f4ddb-107">De gebruiker moet worden toegevoegd aan de rol Maker omgeving voor de omgeving in Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="f4ddb-108">De beheerder met een Power Apps Plan 2-licentie moet het [Power Apps-Beheerportal](https://preview.admin.powerapps.com/) openen.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="f4ddb-109">Selecteer **Omgevingen** en selecteer de juiste omgeving voor Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="f4ddb-110">Selecteer op het tabblad **Beveiliging** op het tabblad **Omgevingsrollen** de optie **Maker omgeving**.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Het tabblad Omgevingsrollen](media/environment-roles.png)

4. <span data-ttu-id="f4ddb-112">Voeg op het tabblad **Gebruikers** de gebruiker of uw organisatie toe.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Het tabblad Gebruikers](media/environment-maker.png)

5. <span data-ttu-id="f4ddb-114">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-114">Select **Save**.</span></span>

6. <span data-ttu-id="f4ddb-115">De gebruiker moet zich nu aanmelden bij [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="f4ddb-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="f4ddb-116">Selecteer **Synchroniseren** om de gebruikersapps bij te werken.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-116">Select **Sync** to update the user apps.</span></span>

    ![De knop Synchroniseren](media/get-more.png)

    <span data-ttu-id="f4ddb-118">Als de synchronisatie is voltooid, wordt Human Resources weergegeven op de startpagina.</span><span class="sxs-lookup"><span data-stu-id="f4ddb-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
