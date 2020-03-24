---
title: Instellingen voor twee keer wegschrijven van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen tussen een nieuwe Finance and Operations-omgeving en een nieuwe Common Data Service-omgeving via Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 75765c0cc03c64030fac6bc656f57a143828b85b
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112417"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="6a94a-103">Instellingen voor twee keer wegschrijven van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6a94a-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6a94a-104">In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen tussen een nieuwe Finance and Operations-omgeving en een nieuwe Common Data Service-omgeving via Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6a94a-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6a94a-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="6a94a-105">Prerequisites</span></span>

<span data-ttu-id="6a94a-106">U moet een beheerder zijn om een verbinding voor twee keer wegschrijven instelt.</span><span class="sxs-lookup"><span data-stu-id="6a94a-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="6a94a-107">U moet toegang tot de tenant hebben.</span><span class="sxs-lookup"><span data-stu-id="6a94a-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="6a94a-108">U moet een beheerder zijn in Finance and Operations- en Common Data Service-omgevingen.</span><span class="sxs-lookup"><span data-stu-id="6a94a-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="6a94a-109">Een verbinding voor twee keer wegschrijven instellen</span><span class="sxs-lookup"><span data-stu-id="6a94a-109">Set up a dual-write connection</span></span>

<span data-ttu-id="6a94a-110">Voer de onderstaande stappen uit om de verbinding voor twee keer wegschrijven in te stellen.</span><span class="sxs-lookup"><span data-stu-id="6a94a-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="6a94a-111">Ga in LCS naar uw project.</span><span class="sxs-lookup"><span data-stu-id="6a94a-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="6a94a-112">Selecteer **Configureren** om een nieuwe omgeving te implementeren.</span><span class="sxs-lookup"><span data-stu-id="6a94a-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="6a94a-113">Selecteer de versie.</span><span class="sxs-lookup"><span data-stu-id="6a94a-113">Select the version.</span></span> 
4. <span data-ttu-id="6a94a-114">Selecteer de topologie.</span><span class="sxs-lookup"><span data-stu-id="6a94a-114">Select the topology.</span></span> <span data-ttu-id="6a94a-115">Als er slechts één topologie beschikbaar is, wordt deze automatisch geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="6a94a-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="6a94a-116">Voer de eerste stappen in de wizard **Implementatie-instellingen** uit.</span><span class="sxs-lookup"><span data-stu-id="6a94a-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="6a94a-117">Voer een van deze stappen uit op het tabblad **Common Data Service**:</span><span class="sxs-lookup"><span data-stu-id="6a94a-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="6a94a-118">Als al een Common Data Service-omgeving is ingericht voor uw tenant, kunt u deze selecteren.</span><span class="sxs-lookup"><span data-stu-id="6a94a-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="6a94a-119">Stel de optie **Common Data Service configureren** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6a94a-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="6a94a-120">Selecteer in het veld **Beschikbare omgevingen** de omgeving die u met uw Finance and Operations-gegevens wilt integreren.</span><span class="sxs-lookup"><span data-stu-id="6a94a-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="6a94a-121">De lijst bevat alle omgevingen waarvoor u beheerdersbevoegdheden hebt.</span><span class="sxs-lookup"><span data-stu-id="6a94a-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="6a94a-122">Schakel het selectie **Akkoord** in om aan te geven dat u akkoord gaat met de voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="6a94a-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Het tabblad Common Data Service als al een Common Data Service-omgeving is ingericht voor uw tenant](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="6a94a-124">Als voor uw tenant nog geen Common Data Service-omgeving bestaat, wordt een nieuwe omgeving ingericht.</span><span class="sxs-lookup"><span data-stu-id="6a94a-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="6a94a-125">Stel de optie **Common Data Service configureren** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6a94a-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="6a94a-126">Geef een naam op voor de Common Data Service-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6a94a-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="6a94a-127">Selecteer de regio waarin u de omgeving wilt implementeren.</span><span class="sxs-lookup"><span data-stu-id="6a94a-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="6a94a-128">Selecteer de standaardtaal en -valuta voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="6a94a-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="6a94a-129">U kunt de taal en valuta later niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6a94a-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="6a94a-130">Schakel het selectie **Akkoord** in om aan te geven dat u akkoord gaat met de voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="6a94a-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Het tabblad Common Data Service wanneer uw tenant nog geen Common Data Service-omgeving heeft](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="6a94a-132">Voer de resterende stappen in de wizard **Implementatie-instellingen** uit.</span><span class="sxs-lookup"><span data-stu-id="6a94a-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="6a94a-133">Als de omgevingsstatus **Geïmplementeerd** is, opent u de pagina met omgevingsdetails.</span><span class="sxs-lookup"><span data-stu-id="6a94a-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="6a94a-134">In de sectie **Common Data Service-omgevingsgegevens** worden de namen weergegeven van de gekoppelde Finance and Operations-omgeving en Common Data Service-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6a94a-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![De sectie Common Data Service-omgevingsgegevens](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="6a94a-136">Een beheerder van de Finance and Operations-omgeving moet zich aanmelden bij LCS en **Koppeling naar CDS for Apps** selecteren om de koppeling te voltooien.</span><span class="sxs-lookup"><span data-stu-id="6a94a-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="6a94a-137">Op de pagina met omgevingsgegevens worden de contactgegevens van de beheerder weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6a94a-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="6a94a-138">Als de koppeling is voltooid, wordt de status bijgewerkt naar **Omgevingskoppelingen voltooid**.</span><span class="sxs-lookup"><span data-stu-id="6a94a-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="6a94a-139">Selecteer **Koppeling naar CDS for Apps** om het werkgebied **Gegevensintegratie** in de Finance and Operations-omgeving te openen en de beschikbare sjablonen te beheren.</span><span class="sxs-lookup"><span data-stu-id="6a94a-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![De knop Koppeling naar CDS for Apps in de sectie Common Data Service-omgevingsgegevens](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="6a94a-141">U kunt omgevingen niet ontkoppelen met behulp van LCS.</span><span class="sxs-lookup"><span data-stu-id="6a94a-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="6a94a-142">Als u een omgeving wilt ontkoppelen, opent u het werkgebied **Gegevensintegratie** in de Finance and Operations-omgeving en selecteert u **Koppeling verbreken**.</span><span class="sxs-lookup"><span data-stu-id="6a94a-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
