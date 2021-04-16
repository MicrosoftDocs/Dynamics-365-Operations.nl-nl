---
title: Instellingen voor twee keer wegschrijven van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e51b4ef1e309e5f89dc82a3776b88c505dc6593d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748536"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="1fc34-103">Instellingen voor twee keer wegschrijven van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="1fc34-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1fc34-104">In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen tussen een nieuwe Finance and Operations-omgeving en een nieuwe Dataverse-omgeving via Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1fc34-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1fc34-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="1fc34-105">Prerequisites</span></span>

<span data-ttu-id="1fc34-106">U moet een beheerder zijn om een verbinding voor twee keer wegschrijven instelt.</span><span class="sxs-lookup"><span data-stu-id="1fc34-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="1fc34-107">U moet toegang tot de tenant hebben.</span><span class="sxs-lookup"><span data-stu-id="1fc34-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="1fc34-108">U moet een beheerder zijn in Finance and Operations- en Dataverse-omgevingen.</span><span class="sxs-lookup"><span data-stu-id="1fc34-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="1fc34-109">Een verbinding voor twee keer wegschrijven instellen</span><span class="sxs-lookup"><span data-stu-id="1fc34-109">Set up a dual-write connection</span></span>

<span data-ttu-id="1fc34-110">Voer de onderstaande stappen uit om de verbinding voor twee keer wegschrijven in te stellen.</span><span class="sxs-lookup"><span data-stu-id="1fc34-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="1fc34-111">Ga in LCS naar uw project.</span><span class="sxs-lookup"><span data-stu-id="1fc34-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="1fc34-112">Selecteer **Configureren** om een nieuwe omgeving te implementeren.</span><span class="sxs-lookup"><span data-stu-id="1fc34-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="1fc34-113">Selecteer de versie.</span><span class="sxs-lookup"><span data-stu-id="1fc34-113">Select the version.</span></span> 
4. <span data-ttu-id="1fc34-114">Selecteer de topologie.</span><span class="sxs-lookup"><span data-stu-id="1fc34-114">Select the topology.</span></span> <span data-ttu-id="1fc34-115">Als er slechts één topologie beschikbaar is, wordt deze automatisch geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1fc34-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="1fc34-116">Voer de eerste stappen in de wizard **Implementatie-instellingen** uit.</span><span class="sxs-lookup"><span data-stu-id="1fc34-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="1fc34-117">Voer een van deze stappen uit op het tabblad **Dataverse**:</span><span class="sxs-lookup"><span data-stu-id="1fc34-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="1fc34-118">Als al een Dataverse-omgeving is ingericht voor uw tenant, kunt u deze selecteren.</span><span class="sxs-lookup"><span data-stu-id="1fc34-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="1fc34-119">Stel de optie **Dataverse configureren** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1fc34-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="1fc34-120">Selecteer in de kolom **Beschikbare omgevingen** de omgeving die u met uw Finance and Operations-gegevens wilt integreren.</span><span class="sxs-lookup"><span data-stu-id="1fc34-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="1fc34-121">De lijst bevat alle omgevingen waarvoor u beheerdersbevoegdheden hebt.</span><span class="sxs-lookup"><span data-stu-id="1fc34-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="1fc34-122">Schakel het selectie **Akkoord** in om aan te geven dat u akkoord gaat met de voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="1fc34-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Het tabblad Dataverse als al een Dataverse-omgeving is ingericht voor uw tenant](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="1fc34-124">Als voor uw tenant nog geen Dataverse-omgeving bestaat, wordt een nieuwe omgeving ingericht.</span><span class="sxs-lookup"><span data-stu-id="1fc34-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="1fc34-125">Stel de optie **Dataverse configureren** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1fc34-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="1fc34-126">Geef een naam op voor de Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="1fc34-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="1fc34-127">Selecteer de regio waarin u de omgeving wilt implementeren.</span><span class="sxs-lookup"><span data-stu-id="1fc34-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="1fc34-128">Selecteer de standaardtaal en -valuta voor de omgeving.</span><span class="sxs-lookup"><span data-stu-id="1fc34-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="1fc34-129">U kunt de taal en valuta later niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1fc34-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="1fc34-130">Schakel het selectie **Akkoord** in om aan te geven dat u akkoord gaat met de voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="1fc34-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Het tabblad Dataverse wanneer uw tenant nog geen Dataverse-omgeving heeft](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="1fc34-132">Voer de resterende stappen in de wizard **Implementatie-instellingen** uit.</span><span class="sxs-lookup"><span data-stu-id="1fc34-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="1fc34-133">Als de omgevingsstatus **Geïmplementeerd** is, opent u de pagina met omgevingsdetails.</span><span class="sxs-lookup"><span data-stu-id="1fc34-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="1fc34-134">In de sectie **Power Platform-integratie** worden de namen weergegeven van de gekoppelde Finance and Operations-omgeving en Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="1fc34-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Sectie Power Platform-integratie](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="1fc34-136">Een beheerder van de Finance and Operations-omgeving moet zich aanmelden bij LCS en **Koppeling naar CDS for Apps** selecteren om de koppeling te voltooien.</span><span class="sxs-lookup"><span data-stu-id="1fc34-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="1fc34-137">Op de pagina met omgevingsgegevens worden de contactgegevens van de beheerder weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1fc34-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="1fc34-138">Als de koppeling is voltooid, wordt de status bijgewerkt naar **Omgevingskoppelingen voltooid**.</span><span class="sxs-lookup"><span data-stu-id="1fc34-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="1fc34-139">Selecteer **Koppeling naar CDS for Apps** om het werkgebied **Gegevensintegratie** in de Finance and Operations-omgeving te openen en de beschikbare sjablonen te beheren.</span><span class="sxs-lookup"><span data-stu-id="1fc34-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![De knop Koppeling naar CDS for Apps in de sectie Power Platform-integratie](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="1fc34-141">U kunt omgevingen niet ontkoppelen met behulp van LCS.</span><span class="sxs-lookup"><span data-stu-id="1fc34-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="1fc34-142">Als u een omgeving wilt ontkoppelen, opent u het werkgebied **Gegevensintegratie** in de Finance and Operations-omgeving en selecteert u **Koppeling verbreken**.</span><span class="sxs-lookup"><span data-stu-id="1fc34-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]