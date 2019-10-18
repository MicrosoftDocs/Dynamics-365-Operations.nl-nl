---
title: Elektronische rapportageconfiguraties downloaden van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u configuraties voor Elektronische rapportage (ER) kunt downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 561187343073a84b152151abe8770e89196eaa56
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174116"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="96a29-103">Elektronische rapportageconfiguraties downloaden van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="96a29-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96a29-104">In dit onderwerp wordt uitgelegd hoe u configuraties voor Elektronische rapportage (ER) kunt downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="96a29-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="96a29-105">Deze zelfstudie begeleidt u door het proces voor het downloaden van de nieuwste versie van de configuraties voor Elektronische rapportage (ER) uit Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="96a29-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="96a29-106">Meld u aan bij de toepassing met een van de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="96a29-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="96a29-107">Ontwikkelaar elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="96a29-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="96a29-108">Functioneel consultant elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="96a29-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="96a29-109">Systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="96a29-109">System administrator</span></span>

2. <span data-ttu-id="96a29-110">Ga naar **Organisatiebeheer** &gt; **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="96a29-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="96a29-111">Selecteer in de sectie **Configuratieproviders** de tegel **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="96a29-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="96a29-112">Klik op de **Microsoft**-tegel op **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="96a29-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="96a29-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="96a29-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="96a29-114">Selecteer in het raster op de pagina **Opslagplaatsen van configuraties** pagina de bestaande opslagplaats van het type **LCS**.</span><span class="sxs-lookup"><span data-stu-id="96a29-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="96a29-115">Als deze opslagplaats niet wordt weergegeven in het raster, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="96a29-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="96a29-116">Klik op **Toevoegen** en voeg een nieuwe opslagplaats toe.</span><span class="sxs-lookup"><span data-stu-id="96a29-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="96a29-117">Selecteer **LCS** als opslagplaatstype.</span><span class="sxs-lookup"><span data-stu-id="96a29-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="96a29-118">Klik op **Opslagplaats maken**.</span><span class="sxs-lookup"><span data-stu-id="96a29-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="96a29-119">Volg de instructies van de autorisatie als hierom wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="96a29-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="96a29-120">Voer een naam en een beschrijving in voor de opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="96a29-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="96a29-121">Klik op **OK** om de nieuwe opslagplaats te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="96a29-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="96a29-122">Selecteer in het raster de nieuwe opslagplaats van het type **LCS**.</span><span class="sxs-lookup"><span data-stu-id="96a29-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="96a29-123">Klik op **Openen** om de lijst met ER-configuraties voor de geselecteerde opslagplaats weer te geven.</span><span class="sxs-lookup"><span data-stu-id="96a29-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="96a29-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="96a29-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="96a29-125">Selecteer in de boomstructuur van het linkervenster de gewenste ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="96a29-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="96a29-126">Selecteer op het sneltabblad **Versies** de vereiste versie van de geselecteerde ER-configuratie.</span><span class="sxs-lookup"><span data-stu-id="96a29-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="96a29-127">Klik op **Importeren** om de geselecteerde versie vanuit LCS te downloaden naar het huidige exemplaar.</span><span class="sxs-lookup"><span data-stu-id="96a29-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="96a29-128">De knop **Importeren** is niet beschikbaar voor ER-configuratieversies die al aanwezig zijn in het huidige exemplaar.</span><span class="sxs-lookup"><span data-stu-id="96a29-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="96a29-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="96a29-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="96a29-130">Afhankelijk van de ER-instellingen worden configuraties gevalideerd nadat ze zijn geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="96a29-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="96a29-131">U krijgt mogelijk meldingen over inconsistentieproblemen die worden vastgesteld.</span><span class="sxs-lookup"><span data-stu-id="96a29-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="96a29-132">U moet deze problemen oplossen voordat u de geïmporteerde configuratieversie kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="96a29-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="96a29-133">Zie voor meer informatie de lijst van gerelateerde artikelen voor dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="96a29-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96a29-134">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="96a29-134">Additional resources</span></span>

[<span data-ttu-id="96a29-135">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="96a29-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)
