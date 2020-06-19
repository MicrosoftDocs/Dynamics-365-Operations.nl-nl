---
title: Een exemplaar verwijderen
description: In dit artikel wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources geleid.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17f299f81d1326dfb06c11a6125acc54b8ef2a6e
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431194"
---
# <a name="remove-an-instance"></a><span data-ttu-id="8c7fa-103">Een exemplaar verwijderen</span><span class="sxs-lookup"><span data-stu-id="8c7fa-103">Remove an instance</span></span>

<span data-ttu-id="8c7fa-104">In dit artikel wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources geleid.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="8c7fa-105">Een testdrive-omgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="8c7fa-105">Remove a test drive environment</span></span>

<span data-ttu-id="8c7fa-106">Human Resources-testdrives zijn zo ingesteld dat ze na 60 dagen verlopen.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="8c7fa-107">Eigenaren van testdrive-omgevingen kunnen echter hun evaluatie eerder beëindigen met de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="8c7fa-108">Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8c7fa-109">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-109">Select **Environments**.</span></span>
3. <span data-ttu-id="8c7fa-110">Selecteer de testdrive-omgeving die een naampatroon heeft zoals: TestDrive - alias@domein</span><span class="sxs-lookup"><span data-stu-id="8c7fa-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="8c7fa-111">Selecteer **Verwijderen** en bevestig de beslissing.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="8c7fa-112">De bestaande testdrive-omgeving wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="8c7fa-113">Wanneer deze is verwijderd, kunt u zich aanmelden voor een nieuwe testdrive-omgeving.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="8c7fa-114">Een productieomgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="8c7fa-114">Remove a production environment</span></span>

<span data-ttu-id="8c7fa-115">In dit artikel wordt ervan uitgegaan dat u Human Resources hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="8c7fa-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="8c7fa-116">Aangezien één Human Resources-omgeving is opgenomen in één Power Apps-omgeving, zijn twee opties mogelijk.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="8c7fa-117">De eerste optie is het verwijderen van de gehele Power Apps-omgeving; bij de tweede optie verwijdert u alleen Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="8c7fa-118">De eerste optie is het beste wanneer u een Power Apps-omgeving speciaal voor Human Resources hebt gemaakt en u net met de implementatie bent begonnen, of wanneer er geen integratie is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="8c7fa-119">De tweede optie is geschikt wanneer u een Power Apps-omgeving hebt die is voorzien van veel gegevens, die worden gebruikt in Power Apps en Power Automate.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="8c7fa-120">Controleer voordat u de Power Apps-omgeving verwijdert, of deze niet wordt gebruikt voor de integratie van gegevens buiten het bereik van Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="8c7fa-121">Houd er ook rekening mee dat de standaard Power Apps-omgevingen niet kunnen worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="8c7fa-122">De gehele Power Apps-omgeving, inclusief Human Resources en de bijbehorende apps en stromen, verwijderen:</span><span class="sxs-lookup"><span data-stu-id="8c7fa-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="8c7fa-123">Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8c7fa-124">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-124">Select **Environments**.</span></span>
3. <span data-ttu-id="8c7fa-125">Selecteer de omgeving die u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="8c7fa-126">Selecteer **Verwijderen** en bevestig de beslissing.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="8c7fa-127">Wacht tot de verwijdering voltooid is.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="8c7fa-128">Meld u aan bij [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) met het account waarmee u zich hebt geabonneerd op Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="8c7fa-129">Selecteer het Human Resources-project dat de omgeving bevat.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="8c7fa-130">Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="8c7fa-131">Selecteer het exemplaar dat u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="8c7fa-132">Selecteer **Exemplaar verwijderen** en bevestig uw keuze.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="8c7fa-133">Als u een Human Resources-omgeving wilt verwijderen uit een bestaande Power Apps-omgeving, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="8c7fa-134">Contact opnemen met ondersteuning en het Human Resources DevOps-team is tijdelijk totdat deze functie rechtstreeks in de LCS is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="8c7fa-135">Neem contact op met ondersteuning om een aanvraag voor verwijderen in te dienen.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="8c7fa-136">Het ondersteuningsteam dient een aanvraag voor verwijderen in bij het Human Resources DevOps-team.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="8c7fa-137">Ga verder nadat u de bevestiging hebt ontvangen dat de omgeving is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="8c7fa-138">Meld u aan bij LCS met de account waarmee u zich hebt geabonneerd op Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="8c7fa-139">Selecteer het Human Resources-project dat de omgeving bevat.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="8c7fa-140">Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="8c7fa-141">Selecteer het exemplaar dat u wilt verwijderen. Dit zou gemarkeerd moeten zijn met de implementatiestatus **Mislukt**.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="8c7fa-142">Selecteer **Exemplaar verwijderen** en bevestig uw keuze.</span><span class="sxs-lookup"><span data-stu-id="8c7fa-142">Select **Remove instance** and confirm your decision.</span></span> 
