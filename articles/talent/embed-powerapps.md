---
title: PowerApps-apps insluiten in Core HR
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij het menu-item PowerApps uit de module Systeembeheer is verdwenen.
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
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="05b3d-103">PowerApps-apps insluiten in Core HR</span><span class="sxs-lookup"><span data-stu-id="05b3d-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="05b3d-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="05b3d-104">**Issue**</span></span>

<span data-ttu-id="05b3d-105">Het menu-item **PowerApps** is verdwenen uit de module **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="05b3d-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="05b3d-106">**Oorzaak**</span><span class="sxs-lookup"><span data-stu-id="05b3d-106">**Cause**</span></span>

<span data-ttu-id="05b3d-107">Het ontwerp van de gebruikersinterface is gewijzigd en Microsoft PowerApps is nu opgenomen in het standaardaanpassingsmodel.</span><span class="sxs-lookup"><span data-stu-id="05b3d-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="05b3d-108">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="05b3d-108">**Resolution**</span></span>

<span data-ttu-id="05b3d-109">De manier waarop PowerApps-apps zijn ingesloten, is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="05b3d-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="05b3d-110">PowerApps-apps worden nu toegevoegd via het aanpassingsmodel.</span><span class="sxs-lookup"><span data-stu-id="05b3d-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="05b3d-111">U kunt PowerApps-apps toevoegen aan vrijwel alle pagina's in Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="05b3d-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="05b3d-112">Zie [Ingesloten PowerApps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps) voor informatie over het insluiten van een PowerApps-app in Talent.</span><span class="sxs-lookup"><span data-stu-id="05b3d-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="05b3d-113">Voor PowerApps-klanten die apps hadden ingesloten voordat de wijziging van kracht werd, had een upgrade naar het nieuwe model moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="05b3d-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="05b3d-114">De knop **PowerApps** knop bevindt zich in de rechterbovenhoek van bijna elke pagina in Talent.</span><span class="sxs-lookup"><span data-stu-id="05b3d-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="05b3d-115">Met deze knop kunt u een PowerApps-app invoegen.</span><span class="sxs-lookup"><span data-stu-id="05b3d-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="05b3d-116">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="05b3d-116">Here is an example.</span></span>

1. <span data-ttu-id="05b3d-117">Ga naar **Personeelsbeheer \> Koppelingen \> Medewerkers \> Werknemers**.</span><span class="sxs-lookup"><span data-stu-id="05b3d-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="05b3d-118">Selecteer de knop **PowerApps** en selecteer vervolgens **Een PowerApp invoegen**.</span><span class="sxs-lookup"><span data-stu-id="05b3d-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![De knop PowerApps](media/png.png)

3. <span data-ttu-id="05b3d-120">Vul de velden in het dialoogvenster **Een PowerApp invoegen** in.</span><span class="sxs-lookup"><span data-stu-id="05b3d-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Het dialoogvenster Een PowerApp invoegen](media/insert-powerapp.png)

<span data-ttu-id="05b3d-122">U kunt ook deze stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="05b3d-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="05b3d-123">Selecteer **Dit formulier aanpassen** in de groep **Aanpassen** op het tabblad **Opties** van het actievenster van de pagina.</span><span class="sxs-lookup"><span data-stu-id="05b3d-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![De groep Aanpassen op het tabblad Opties](media/options.png)

    <span data-ttu-id="05b3d-125">De aanpassingswerkbalk wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="05b3d-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="05b3d-126">Selecteer **Invoegen \> PowerApp** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="05b3d-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Een PowerApps-app invoegen via de aanpassingswerkbalk](media/powerapp-bar.png)

