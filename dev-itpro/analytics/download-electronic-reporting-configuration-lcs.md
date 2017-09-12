---
title: Elektronische rapportageconfiguraties downloaden van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u configuraties voor Elektronische rapportage (ER) kunt downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a4411b25285128c849a715fdc7a2f5fe51580a3b
ms.contentlocale: nl-nl
ms.lasthandoff: 07/18/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="397cd-103">Elektronische rapportageconfiguraties downloaden van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="397cd-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="397cd-104">In dit onderwerp wordt uitgelegd hoe u configuraties voor Elektronische rapportage (ER) kunt downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="397cd-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="397cd-105">Deze zelfstudie begeleidt u door het proces voor het downloaden van de nieuwste versie van de configuraties voor Elektronische rapportage (ER) uit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="397cd-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1.  <span data-ttu-id="397cd-106">Meld u aan bij Finance and Operations met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="397cd-106">Sign in to Finance and Operations by using one of the following roles:</span></span>
    -   <span data-ttu-id="397cd-107">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="397cd-107">Electronic reporting developer</span></span>
    -   <span data-ttu-id="397cd-108">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="397cd-108">Electronic reporting functional consultant</span></span>
    -   <span data-ttu-id="397cd-109">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="397cd-109">System administrator</span></span>

2.  <span data-ttu-id="397cd-110">Ga naar **Organisatiebeheer** &gt; **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="397cd-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3.  <span data-ttu-id="397cd-111">Selecteer in de sectie **Configuratieproviders** de tegel **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="397cd-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4.  <span data-ttu-id="397cd-112">Klik op de **Microsoft**-tegel op **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="397cd-112">On the **Microsoft** tile, click **Repositories**.</span></span> <span data-ttu-id="397cd-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="397cd-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>
5.  <span data-ttu-id="397cd-114">Selecteer in het raster op de pagina **Opslagplaatsen van configuraties** pagina de bestaande opslagplaats van het type **LCS**.</span><span class="sxs-lookup"><span data-stu-id="397cd-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="397cd-115">Als deze opslagplaats niet wordt weergegeven in het raster, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="397cd-115">If this repository doesn't appear in the grid, follow these steps:</span></span>
    1.  <span data-ttu-id="397cd-116">Klik op **Toevoegen** en voeg een nieuwe opslagplaats toe.</span><span class="sxs-lookup"><span data-stu-id="397cd-116">Click **Add** to add a new repository.</span></span>
    2.  <span data-ttu-id="397cd-117">Selecteer **LCS** als opslagplaatstype.</span><span class="sxs-lookup"><span data-stu-id="397cd-117">Select **LCS** as the repository type.</span></span>
    3.  <span data-ttu-id="397cd-118">Klik op **Opslagplaats maken**.</span><span class="sxs-lookup"><span data-stu-id="397cd-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="397cd-119">Volg de instructies van de autorisatie als hierom wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="397cd-119">If prompted, follow the authorization instructions.</span></span>
    5.  <span data-ttu-id="397cd-120">Voer een naam en een beschrijving in voor de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="397cd-120">Enter a name and description for the repository.</span></span>
    6.  <span data-ttu-id="397cd-121">Klik op **OK** om de nieuwe opslagplaats te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="397cd-121">Click **OK** to confirm the new repository entry.</span></span>
    7.  <span data-ttu-id="397cd-122">Selecteer in het raster de nieuwe opslagplaats van het type **LCS**.</span><span class="sxs-lookup"><span data-stu-id="397cd-122">In the grid, select the new repository of the **LCS** type.</span></span>

6.  <span data-ttu-id="397cd-123">Klik op **Openen** om de lijst met ER-configuraties voor de geselecteerde opslagplaats weer te geven.</span><span class="sxs-lookup"><span data-stu-id="397cd-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span> <span data-ttu-id="397cd-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="397cd-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>
7.  <span data-ttu-id="397cd-125">Selecteer in de boomstructuur van het linkervenster de gewenste ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="397cd-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8.  <span data-ttu-id="397cd-126">Selecteer op het sneltabblad **Versies** de vereiste versie van de geselecteerde ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="397cd-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9.  <span data-ttu-id="397cd-127">Klik op **Importeren** om de geselecteerde versie vanuit LCS te downloaden naar het huidige exemplaar van Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="397cd-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span> <span data-ttu-id="397cd-128">**Opmerking:** de knop **Importeren** is niet beschikbaar voor ER-configuratieversies die al aanwezig zijn in het huidige Finance and Operations-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="397cd-128">**Note:** The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span> <span data-ttu-id="397cd-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="397cd-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

<span data-ttu-id="397cd-130">**Opmerking:** Afhankelijk van de ER-instellingen worden configuraties gevalideerd nadat ze zijn geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="397cd-130">**Note:** Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="397cd-131">U krijgt mogelijk meldingen over inconsistentieproblemen die worden vastgesteld.</span><span class="sxs-lookup"><span data-stu-id="397cd-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="397cd-132">U moet deze problemen oplossen voordat u de geïmporteerde configuratieversie kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="397cd-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="397cd-133">Zie voor meer informatie de lijst van gerelateerde artikelen voor dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="397cd-133">For more information, see the list of related articles for this topic.</span></span>

<a name="see-also"></a><span data-ttu-id="397cd-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="397cd-134">See also</span></span>
--------

[<span data-ttu-id="397cd-135">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="397cd-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)




