---
title: Een exemplaar verwijderen
description: In dit artikel wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources geleid.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72a5b99150e5ccdf9a542b569c94c64cb95923fd
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053606"
---
# <a name="remove-an-instance"></a><span data-ttu-id="dca4f-103">Een exemplaar verwijderen</span><span class="sxs-lookup"><span data-stu-id="dca4f-103">Remove an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dca4f-104">In dit artikel wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources geleid.</span><span class="sxs-lookup"><span data-stu-id="dca4f-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="dca4f-105">Een testdrive-omgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="dca4f-105">Remove a test drive environment</span></span>

<span data-ttu-id="dca4f-106">Human Resources-testdrives zijn zo ingesteld dat ze na 60 dagen verlopen.</span><span class="sxs-lookup"><span data-stu-id="dca4f-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="dca4f-107">Eigenaren van testdrive-omgevingen kunnen echter hun evaluatie eerder beëindigen met de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="dca4f-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="dca4f-108">Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.</span><span class="sxs-lookup"><span data-stu-id="dca4f-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="dca4f-109">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="dca4f-109">Select **Environments**.</span></span>
3. <span data-ttu-id="dca4f-110">Selecteer de testdrive-omgeving die een naampatroon heeft zoals: TestDrive - alias@domein</span><span class="sxs-lookup"><span data-stu-id="dca4f-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="dca4f-111">Selecteer **Verwijderen** en bevestig de beslissing.</span><span class="sxs-lookup"><span data-stu-id="dca4f-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="dca4f-112">De bestaande testdrive-omgeving wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="dca4f-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="dca4f-113">Wanneer deze is verwijderd, kunt u zich aanmelden voor een nieuwe testdrive-omgeving.</span><span class="sxs-lookup"><span data-stu-id="dca4f-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="dca4f-114">Een productieomgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="dca4f-114">Remove a production environment</span></span>

<span data-ttu-id="dca4f-115">In dit artikel wordt ervan uitgegaan dat u Human Resources hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="dca4f-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="dca4f-116">Aangezien één Human Resources-omgeving is opgenomen in één Power Apps-omgeving, zijn twee opties mogelijk.</span><span class="sxs-lookup"><span data-stu-id="dca4f-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="dca4f-117">De eerste optie is het verwijderen van de gehele Power Apps-omgeving; bij de tweede optie verwijdert u alleen Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dca4f-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="dca4f-118">De eerste optie is het beste wanneer u een Power Apps-omgeving speciaal voor Human Resources hebt gemaakt en u net met de implementatie bent begonnen, of wanneer er geen integratie is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="dca4f-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="dca4f-119">De tweede optie is geschikt wanneer u een Power Apps-omgeving hebt die is voorzien van veel gegevens, die worden gebruikt in Power Apps en Power Automate.</span><span class="sxs-lookup"><span data-stu-id="dca4f-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="dca4f-120">Controleer voordat u de Power Apps-omgeving verwijdert, of deze niet wordt gebruikt voor de integratie van gegevens buiten het bereik van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dca4f-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="dca4f-121">Houd er ook rekening mee dat de standaard Power Apps-omgevingen niet kunnen worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="dca4f-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="dca4f-122">De gehele Power Apps-omgeving, inclusief Human Resources en de bijbehorende apps en stromen, verwijderen:</span><span class="sxs-lookup"><span data-stu-id="dca4f-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="dca4f-123">Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.</span><span class="sxs-lookup"><span data-stu-id="dca4f-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="dca4f-124">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="dca4f-124">Select **Environments**.</span></span>
3. <span data-ttu-id="dca4f-125">Selecteer de omgeving die u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="dca4f-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="dca4f-126">Selecteer **Verwijderen** en bevestig de beslissing.</span><span class="sxs-lookup"><span data-stu-id="dca4f-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="dca4f-127">Wacht tot de verwijdering voltooid is.</span><span class="sxs-lookup"><span data-stu-id="dca4f-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="dca4f-128">Meld u aan bij [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) met het account waarmee u zich hebt geabonneerd op Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dca4f-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="dca4f-129">Selecteer het Human Resources-project dat de omgeving bevat.</span><span class="sxs-lookup"><span data-stu-id="dca4f-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="dca4f-130">Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="dca4f-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="dca4f-131">Selecteer het exemplaar dat u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="dca4f-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="dca4f-132">Selecteer **Exemplaar verwijderen** en bevestig uw keuze.</span><span class="sxs-lookup"><span data-stu-id="dca4f-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="dca4f-133">Als u een Human Resources-omgeving wilt verwijderen uit een bestaande Power Apps-omgeving, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="dca4f-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="dca4f-134">Contact opnemen met ondersteuning en het Human Resources DevOps-team is tijdelijk totdat deze functie rechtstreeks in de LCS is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="dca4f-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="dca4f-135">Neem contact op met ondersteuning om een aanvraag voor verwijderen in te dienen.</span><span class="sxs-lookup"><span data-stu-id="dca4f-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="dca4f-136">Het ondersteuningsteam dient een aanvraag voor verwijderen in bij het Human Resources DevOps-team.</span><span class="sxs-lookup"><span data-stu-id="dca4f-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="dca4f-137">Ga verder nadat u de bevestiging hebt ontvangen dat de omgeving is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="dca4f-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="dca4f-138">Meld u aan bij LCS met de account waarmee u zich hebt geabonneerd op Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dca4f-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="dca4f-139">Selecteer het Human Resources-project dat de omgeving bevat.</span><span class="sxs-lookup"><span data-stu-id="dca4f-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="dca4f-140">Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="dca4f-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="dca4f-141">Selecteer het exemplaar dat u wilt verwijderen. Dit zou gemarkeerd moeten zijn met de implementatiestatus **Verwijderd**.</span><span class="sxs-lookup"><span data-stu-id="dca4f-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="dca4f-142">Selecteer **Exemplaar verwijderen** en bevestig uw keuze.</span><span class="sxs-lookup"><span data-stu-id="dca4f-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="dca4f-143">Een zacht verwijderde omgeving herstellen</span><span class="sxs-lookup"><span data-stu-id="dca4f-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="dca4f-144">Als u de Power Apps-omgeving verwijdert waarop uw HRM-omgeving is aangesloten, wordt de status van de human resources-omgeving in Lifecycle Services **zacht verwijderd**.</span><span class="sxs-lookup"><span data-stu-id="dca4f-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="dca4f-145">In dit geval kunnen gebruikers geen verbinding maken met human resources.</span><span class="sxs-lookup"><span data-stu-id="dca4f-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="dca4f-146">De omgeving herstellen:</span><span class="sxs-lookup"><span data-stu-id="dca4f-146">To restore the environment:</span></span>

1. <span data-ttu-id="dca4f-147">Volg de instructies in [De Power Apps-omgeving herstellen](/power-platform/admin/recover-environment.md).</span><span class="sxs-lookup"><span data-stu-id="dca4f-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="dca4f-148">Neem contact op met de ondersteuning om de HRM-omgeving te herstellen.</span><span class="sxs-lookup"><span data-stu-id="dca4f-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="dca4f-149">Zie voor meer informatie [Ondersteuning krijgen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="dca4f-149">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="dca4f-150">Power Apps-omgevingen worden slechts zeven dagen na verwijdering bewaard.</span><span class="sxs-lookup"><span data-stu-id="dca4f-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="dca4f-151">U moet de omgeving binnen zeven dagen herstellen.</span><span class="sxs-lookup"><span data-stu-id="dca4f-151">You must recover the environment within the seven day period.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]