---
title: Talent-omgevingen verwijderen
description: In dit onderwerp wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Dynamics 365 Talent geleid.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e752d658388fc6cb6f4b84ac83cb12a71522199b
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898105"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="8623f-103">Talent-omgevingen verwijderen</span><span class="sxs-lookup"><span data-stu-id="8623f-103">Remove Talent environments</span></span>

<span data-ttu-id="8623f-104">In dit onderwerp wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Dynamics 365 Talent geleid.</span><span class="sxs-lookup"><span data-stu-id="8623f-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="8623f-105">Een testdrive-omgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="8623f-105">Removing a test drive environment</span></span>

<span data-ttu-id="8623f-106">Talent-testdrives zijn zo ingesteld dat ze na 60 dagen verlopen.</span><span class="sxs-lookup"><span data-stu-id="8623f-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="8623f-107">Eigenaren van testdrive-omgevingen kunnen echter hun evaluatie eerder beëindigen met de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="8623f-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="8623f-108">Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.</span><span class="sxs-lookup"><span data-stu-id="8623f-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8623f-109">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="8623f-109">Select **Environments**.</span></span>
3. <span data-ttu-id="8623f-110">Selecteer de testdrive-omgeving die een naampatroon heeft zoals: TestDrive - alias@domein</span><span class="sxs-lookup"><span data-stu-id="8623f-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="8623f-111">Selecteer **Verwijderen** en bevestig de beslissing.</span><span class="sxs-lookup"><span data-stu-id="8623f-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="8623f-112">De bestaande testdrive-omgeving wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="8623f-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="8623f-113">Wanneer deze is verwijderd, kunt u zich aanmelden voor een nieuwe testdrive-omgeving.</span><span class="sxs-lookup"><span data-stu-id="8623f-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="8623f-114">Een productieomgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="8623f-114">Removing a production environment</span></span>

<span data-ttu-id="8623f-115">In dit onderwerp wordt ervan uitgegaan dat u Talent hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="8623f-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="8623f-116">Aangezien één Talent-omgeving is opgenomen in één Power Apps-omgeving, zijn twee opties mogelijk.</span><span class="sxs-lookup"><span data-stu-id="8623f-116">Since a single Talent environment is “contained” within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="8623f-117">De eerste optie is het verwijderen van de gehele Power Apps-omgeving; bij de tweede optie verwijdert u alleen Talent.</span><span class="sxs-lookup"><span data-stu-id="8623f-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="8623f-118">De eerste optie is het beste wanneer u een Power Apps-omgeving speciaal voor Talent hebt gemaakt en u net met de implementatie bent begonnen, of wanneer er geen integratie is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8623f-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="8623f-119">De tweede optie is geschikt wanneer u een Power Apps-omgeving hebt die is voorzien van veel gegevens, die worden gebruikt in Power Apps en Power Automate.</span><span class="sxs-lookup"><span data-stu-id="8623f-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="8623f-120">Controleer voordat u de Power Apps-omgeving verwijdert, of deze niet wordt gebruikt voor de integratie van gegevens buiten het bereik van Talent.</span><span class="sxs-lookup"><span data-stu-id="8623f-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="8623f-121">Houd er ook rekening mee dat de standaard Power Apps-omgevingen niet kunnen worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="8623f-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="8623f-122">De gehele Power Apps-omgeving, inclusief Talent en de bijbehorende apps en stromen, verwijderen:</span><span class="sxs-lookup"><span data-stu-id="8623f-122">To remove the entire Power Apps environment, including Talent and the associated apps and flows:</span></span>

1. <span data-ttu-id="8623f-123">Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.</span><span class="sxs-lookup"><span data-stu-id="8623f-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8623f-124">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="8623f-124">Select **Environments**.</span></span>
3. <span data-ttu-id="8623f-125">Selecteer de omgeving die u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="8623f-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="8623f-126">Selecteer **Verwijderen** en bevestig de beslissing.</span><span class="sxs-lookup"><span data-stu-id="8623f-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="8623f-127">Wacht tot de verwijdering voltooid is.</span><span class="sxs-lookup"><span data-stu-id="8623f-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="8623f-128">Meld u aan bij [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) met het account waarmee u zich hebt geabonneerd op Talent.</span><span class="sxs-lookup"><span data-stu-id="8623f-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="8623f-129">Selecteer het Talent-project dat de omgeving bevat.</span><span class="sxs-lookup"><span data-stu-id="8623f-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="8623f-130">Selecteer in uw LCS-project de tegel **Beheer Talent-app**.</span><span class="sxs-lookup"><span data-stu-id="8623f-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="8623f-131">Selecteer het exemplaar dat u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="8623f-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="8623f-132">Selecteer **Exemplaar verwijderen** en bevestig uw keuze.</span><span class="sxs-lookup"><span data-stu-id="8623f-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="8623f-133">Als u een Talent-omgeving wilt verwijderen uit een bestaande Power Apps-omgeving, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="8623f-133">To remove a Talent environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="8623f-134">Contact opnemen met ondersteuning en het Talent DevOps-team is tijdelijk totdat deze functie rechtstreeks in de LCS is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8623f-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="8623f-135">Neem contact op met ondersteuning om een aanvraag voor verwijderen in te dienen.</span><span class="sxs-lookup"><span data-stu-id="8623f-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="8623f-136">Het ondersteuningsteam dient een aanvraag voor verwijderen in bij het Talent DevOps-team.</span><span class="sxs-lookup"><span data-stu-id="8623f-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="8623f-137">Ga verder nadat u de bevestiging hebt ontvangen dat de omgeving is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="8623f-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="8623f-138">Meld u aan bij LCS met het account waarmee u zich hebt geabonneerd op Talent.</span><span class="sxs-lookup"><span data-stu-id="8623f-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="8623f-139">Selecteer het Talent-project dat de omgeving bevat.</span><span class="sxs-lookup"><span data-stu-id="8623f-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="8623f-140">Selecteer in uw LCS-project de tegel **Beheer Talent-app**.</span><span class="sxs-lookup"><span data-stu-id="8623f-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="8623f-141">Selecteer het exemplaar dat u wilt verwijderen. Dit zou gemarkeerd moeten zijn met de implementatiestatus **Mislukt**.</span><span class="sxs-lookup"><span data-stu-id="8623f-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="8623f-142">Selecteer **Exemplaar verwijderen** en bevestig uw keuze.</span><span class="sxs-lookup"><span data-stu-id="8623f-142">Select **Remove instance** and confirm your decision.</span></span> 

