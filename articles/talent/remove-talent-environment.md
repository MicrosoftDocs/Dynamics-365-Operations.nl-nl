---
title: Talent-omgevingen verwijderen
description: In dit onderwerp wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 for Talent geleid.
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: e0422a5b7ac227ad03ccafb4e34e614dc770a363
ms.contentlocale: nl-nl
ms.lasthandoff: 09/17/2018

---
# <a name="remove-talent-environments"></a><span data-ttu-id="04dd1-103">Talent-omgevingen verwijderen</span><span class="sxs-lookup"><span data-stu-id="04dd1-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04dd1-104">In dit onderwerp wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 for Talent geleid.</span><span class="sxs-lookup"><span data-stu-id="04dd1-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="04dd1-105">Een testdrive-omgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="04dd1-105">Removing a test drive environment</span></span>

<span data-ttu-id="04dd1-106">Talent-testdrives zijn zo ingesteld dat ze na 60 dagen verlopen.</span><span class="sxs-lookup"><span data-stu-id="04dd1-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="04dd1-107">Eigenaren van testdrive-omgevingen kunnen echter hun evaluatie eerder beëindigen met de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="04dd1-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="04dd1-108">Navigeer naar het [PowerApps-beheercentrum](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="04dd1-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="04dd1-109">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="04dd1-109">Select **Environments**.</span></span>
3. <span data-ttu-id="04dd1-110">Selecteer de testdrive-omgeving die een naampatroon heeft zoals: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="04dd1-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="04dd1-111">Selecteer **Verwijderen** en bevestig de beslissing.</span><span class="sxs-lookup"><span data-stu-id="04dd1-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="04dd1-112">De bestaande testdrive-omgeving wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="04dd1-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="04dd1-113">Wanneer deze is verwijderd, kunt u zich aanmelden voor een nieuwe testdrive-omgeving.</span><span class="sxs-lookup"><span data-stu-id="04dd1-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="04dd1-114">Een productieomgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="04dd1-114">Removing a production environment</span></span>

<span data-ttu-id="04dd1-115">In dit onderwerp wordt ervan uitgegaan dat u Talent hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="04dd1-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="04dd1-116">Aangezien één Talent-omgeving is opgenomen in één PowerApps-omgeving, zijn twee opties mogelijk.</span><span class="sxs-lookup"><span data-stu-id="04dd1-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="04dd1-117">De eerste optie is het verwijderen van de gehele PowerApps-omgeving; bij de tweede optie verwijdert u alleen Talent.</span><span class="sxs-lookup"><span data-stu-id="04dd1-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="04dd1-118">De eerste optie is het beste wanneer u een PowerApps-omgeving speciaal voor Talent hebt gemaakt en dat u net met implementatie bent begonnen of wanneer er geen integratie is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="04dd1-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="04dd1-119">De tweede optie is geschikt wanneer er een PowerApps-omgeving hebt voorzien van veel gegevens die worden gebruikt in PowerApps en Flows.</span><span class="sxs-lookup"><span data-stu-id="04dd1-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="04dd1-120">Controleer voordat u de PowerApps-omgeving verwijdert, of deze niet wordt gebruikt voor de integratie van gegevens buiten het bereik van Talent.</span><span class="sxs-lookup"><span data-stu-id="04dd1-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="04dd1-121">Houd er ook rekening mee dat de standaard PowerApps-omgevingen niet kunnen worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="04dd1-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="04dd1-122">De gehele PowerApps-omgeving, inclusief Talent en de bijbehorende Apps en Flows verwijderen:</span><span class="sxs-lookup"><span data-stu-id="04dd1-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="04dd1-123">Navigeer naar het [PowerApps-beheercentrum](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="04dd1-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="04dd1-124">Selecteer **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="04dd1-124">Select **Environments**.</span></span>
3. <span data-ttu-id="04dd1-125">Selecteer de omgeving die u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="04dd1-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="04dd1-126">Selecteer **Verwijderen** en bevestig de beslissing.</span><span class="sxs-lookup"><span data-stu-id="04dd1-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="04dd1-127">Wacht tot de verwijdering voltooid is.</span><span class="sxs-lookup"><span data-stu-id="04dd1-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="04dd1-128">Meld u aan bij [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) met het account waarmee u zich hebt geabonneerd op Talent.</span><span class="sxs-lookup"><span data-stu-id="04dd1-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="04dd1-129">Selecteer het Talent-project dat de omgeving bevat.</span><span class="sxs-lookup"><span data-stu-id="04dd1-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="04dd1-130">Selecteer in uw LCS-project de tegel **Beheer Talent-app**.</span><span class="sxs-lookup"><span data-stu-id="04dd1-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="04dd1-131">Selecteer het exemplaar dat u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="04dd1-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="04dd1-132">Selecteer **Exemplaar verwijderen** en bevestig uw keuze.</span><span class="sxs-lookup"><span data-stu-id="04dd1-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="04dd1-133">Als u een Talent-omgeving wilt verwijderen uit een bestaande PowerApps-omgeving, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="04dd1-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="04dd1-134">Contact opnemen met ondersteuning en het Talent DevOps-team is tijdelijk totdat deze functie rechtstreeks in de LCS is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="04dd1-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="04dd1-135">Neem contact op met ondersteuning om een aanvraag voor verwijderen in te dienen.</span><span class="sxs-lookup"><span data-stu-id="04dd1-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="04dd1-136">Het ondersteuningsteam dient een aanvraag voor verwijderen in bij het Talent DevOps-team.</span><span class="sxs-lookup"><span data-stu-id="04dd1-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="04dd1-137">Ga verder nadat u de bevestiging hebt ontvangen dat de omgeving is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="04dd1-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="04dd1-138">Meld u aan bij LCS met het account waarmee u zich hebt geabonneerd op Talent.</span><span class="sxs-lookup"><span data-stu-id="04dd1-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="04dd1-139">Selecteer het Talent-project dat de omgeving bevat.</span><span class="sxs-lookup"><span data-stu-id="04dd1-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="04dd1-140">Selecteer in uw LCS-project de tegel **Beheer Talent-app**.</span><span class="sxs-lookup"><span data-stu-id="04dd1-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="04dd1-141">Selecteer het exemplaar dat u wilt verwijderen. Dit zou gemarkeerd moeten zijn met de implementatiestatus **Mislukt**.</span><span class="sxs-lookup"><span data-stu-id="04dd1-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="04dd1-142">Selecteer **Exemplaar verwijderen** en bevestig uw keuze.</span><span class="sxs-lookup"><span data-stu-id="04dd1-142">Select **Remove instance** and confirm your decision.</span></span> 


