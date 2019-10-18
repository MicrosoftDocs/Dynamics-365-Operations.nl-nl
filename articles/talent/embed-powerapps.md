---
title: PowerApps-apps insluiten in Dynamics 365 - Core HR
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij het menu-item PowerApps uit de module Systeembeheer is verdwenen.
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
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008425"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="2dee4-103">PowerApps-apps insluiten in Core HR</span><span class="sxs-lookup"><span data-stu-id="2dee4-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2dee4-104">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="2dee4-104">**Issue**</span></span>

<span data-ttu-id="2dee4-105">Het menu-item **PowerApps** is verdwenen uit de module **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="2dee4-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="2dee4-106">**Oorzaak**</span><span class="sxs-lookup"><span data-stu-id="2dee4-106">**Cause**</span></span>

<span data-ttu-id="2dee4-107">Het ontwerp van de gebruikersinterface is gewijzigd en Microsoft PowerApps is nu opgenomen in het standaardaanpassingsmodel.</span><span class="sxs-lookup"><span data-stu-id="2dee4-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="2dee4-108">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="2dee4-108">**Resolution**</span></span>

<span data-ttu-id="2dee4-109">De manier waarop PowerApps-apps zijn ingesloten, is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="2dee4-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="2dee4-110">PowerApps-apps worden nu toegevoegd via het aanpassingsmodel.</span><span class="sxs-lookup"><span data-stu-id="2dee4-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="2dee4-111">U kunt PowerApps-apps toevoegen aan vrijwel alle pagina's in Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="2dee4-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="2dee4-112">Zie [Ingesloten PowerApps-apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps) voor informatie over het insluiten van een PowerApps-app in Talent.</span><span class="sxs-lookup"><span data-stu-id="2dee4-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="2dee4-113">Voor PowerApps-klanten die apps hadden ingesloten voordat de wijziging van kracht werd, had een upgrade naar het nieuwe model moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2dee4-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="2dee4-114">De knop **PowerApps** bevindt zich in de rechterbovenhoek van bijna elke pagina in Talent.</span><span class="sxs-lookup"><span data-stu-id="2dee4-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="2dee4-115">Met deze knop kunt u een PowerApps-app invoegen.</span><span class="sxs-lookup"><span data-stu-id="2dee4-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="2dee4-116">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="2dee4-116">Here is an example.</span></span>

1. <span data-ttu-id="2dee4-117">Ga naar **Personeelsbeheer \> Koppelingen \> Medewerkers \> Werknemers**.</span><span class="sxs-lookup"><span data-stu-id="2dee4-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="2dee4-118">Selecteer de knop **PowerApps** en selecteer vervolgens **Een PowerApp invoegen**.</span><span class="sxs-lookup"><span data-stu-id="2dee4-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-knop](media/png.png)

3. <span data-ttu-id="2dee4-120">Vul de velden in het dialoogvenster **Een PowerApp invoegen** in.</span><span class="sxs-lookup"><span data-stu-id="2dee4-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Het dialoogvenster Een PowerApp invoegen](media/insert-powerapp.png)

<span data-ttu-id="2dee4-122">U kunt ook deze stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="2dee4-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="2dee4-123">Selecteer **Dit formulier aanpassen** in de groep **Aanpassen** op het tabblad **Opties** van het actievenster van de pagina.</span><span class="sxs-lookup"><span data-stu-id="2dee4-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![De groep Aanpassen op het tabblad Opties](media/options.png)

    <span data-ttu-id="2dee4-125">De aanpassingswerkbalk wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="2dee4-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="2dee4-126">Selecteer **Invoegen \> PowerApp** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="2dee4-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Een PowerApps-app invoegen via de aanpassingswerkbalk](media/powerapp-bar.png)
