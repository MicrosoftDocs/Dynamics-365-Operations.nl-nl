---
title: Power Apps-apps insluiten in Dynamics 365 - Core HR
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij het menu-item Microsoft Power Apps uit de module Systeembeheer is verdwenen.
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
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898707"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="54cb5-103">Power Apps-apps insluiten in Dynamics 365 - Core HR</span><span class="sxs-lookup"><span data-stu-id="54cb5-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

<span data-ttu-id="54cb5-104">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="54cb5-104">**Issue**</span></span>

<span data-ttu-id="54cb5-105">Het menu-item **Power Apps** is verdwenen uit de module **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="54cb5-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="54cb5-106">**Oorzaak**</span><span class="sxs-lookup"><span data-stu-id="54cb5-106">**Cause**</span></span>

<span data-ttu-id="54cb5-107">Het ontwerp van de gebruikersinterface is gewijzigd en Microsoft Power Apps is nu opgenomen in het standaardaanpassingsmodel.</span><span class="sxs-lookup"><span data-stu-id="54cb5-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="54cb5-108">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="54cb5-108">**Resolution**</span></span>

<span data-ttu-id="54cb5-109">De manier waarop Power Apps zijn ingesloten, is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="54cb5-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="54cb5-110">Power Apps worden nu toegevoegd via het aanpassingsmodel.</span><span class="sxs-lookup"><span data-stu-id="54cb5-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="54cb5-111">U kunt Power Apps toevoegen aan vrijwel alle pagina's in Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="54cb5-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="54cb5-112">Zie [Microsoft Power Apps insluiten](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps) voor informatie over het insluiten van Power Apps in Talent.</span><span class="sxs-lookup"><span data-stu-id="54cb5-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="54cb5-113">Voor Power Apps-klanten die apps hadden ingesloten voordat de wijziging van kracht werd, had een upgrade naar het nieuwe model moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="54cb5-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="54cb5-114">De knop **Power Apps** bevindt zich in de rechterbovenhoek van bijna elke pagina in Talent.</span><span class="sxs-lookup"><span data-stu-id="54cb5-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="54cb5-115">Met deze knop kunt u een Power Apps invoegen.</span><span class="sxs-lookup"><span data-stu-id="54cb5-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="54cb5-116">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="54cb5-116">Here is an example.</span></span>

1. <span data-ttu-id="54cb5-117">Ga naar **Personeelsbeheer \> Koppelingen \> Medewerkers \> Werknemers**.</span><span class="sxs-lookup"><span data-stu-id="54cb5-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="54cb5-118">Selecteer de knop **Power Apps** en selecteer vervolgens **Een PowerApp invoegen**.</span><span class="sxs-lookup"><span data-stu-id="54cb5-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps-knop](media/png.png)

3. <span data-ttu-id="54cb5-120">Vul de velden in het dialoogvenster **Een PowerApp invoegen** in.</span><span class="sxs-lookup"><span data-stu-id="54cb5-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Het dialoogvenster Een PowerApp invoegen](media/insert-powerapp.png)

<span data-ttu-id="54cb5-122">U kunt ook deze stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="54cb5-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="54cb5-123">Selecteer **Dit formulier aanpassen** in de groep **Aanpassen** op het tabblad **Opties** van het actievenster van de pagina.</span><span class="sxs-lookup"><span data-stu-id="54cb5-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![De groep Aanpassen op het tabblad Opties](media/options.png)

    <span data-ttu-id="54cb5-125">De aanpassingswerkbalk wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="54cb5-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="54cb5-126">Selecteer **Invoegen \> PowerApp** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="54cb5-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Een Power Apps-app invoegen via de aanpassingswerkbalk](media/powerapp-bar.png)
