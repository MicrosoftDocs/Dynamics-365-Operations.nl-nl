---
title: Afmelden voor verzamelen van gebeurtenissen voor webactiviteit
description: In dit onderwerp wordt uitgelegd hoe u bezoekers van uw website in staat kunt stellen om zich af te melden voor het verzamelen van gebeurtenissen voor webactiviteiten in Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c396060017db6d7ce830b350f242d3097876e50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012308"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="6f86f-103">Afmelden voor verzamelen van gebeurtenissen voor webactiviteit</span><span class="sxs-lookup"><span data-stu-id="6f86f-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="6f86f-104">In dit onderwerp wordt uitgelegd hoe u klanten in staat kunt stellen zich af te melden voor het verzamelen van gebeurtenissen voor webactiviteiten in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6f86f-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6f86f-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="6f86f-105">Overview</span></span>

<span data-ttu-id="6f86f-106">Met Dynamics 365 Commerce kunnen sitebeheerders de webactiviteiten analyseren van gebruikers van hun e-commercesites.</span><span class="sxs-lookup"><span data-stu-id="6f86f-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="6f86f-107">Op die manier kunnen ze beter begrijpen hoe hun sites worden gebruikt en kunnen ze de sites optimaliseren voor een verbeterde gebruikerservaring en voor het behalen van zakelijke doelstellingen.</span><span class="sxs-lookup"><span data-stu-id="6f86f-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="6f86f-108">Manieren voor beheerders om een afmeldingsmethode te implementeren</span><span class="sxs-lookup"><span data-stu-id="6f86f-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="6f86f-109">Beheerders hebben drie manieren om een afmeldingsmethode te implementeren.</span><span class="sxs-lookup"><span data-stu-id="6f86f-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="6f86f-110">Afmelden namens gebruikers</span><span class="sxs-lookup"><span data-stu-id="6f86f-110">Opt out on behalf of users</span></span>

<span data-ttu-id="6f86f-111">In Accountbeheer in Commerce Headquarters (HQ) kunnen beheerders de afmelding uitvoeren namens gebruikers.</span><span class="sxs-lookup"><span data-stu-id="6f86f-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="6f86f-112">Zoek in de HQ-client op de pagina **Alle klanten** een klant en selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="6f86f-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="6f86f-113">Stel op de pagina met klantdetails op het sneltabblad **Retail** in de sectie **Privacy** de optie **Webactiviteit niet bijhouden** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6f86f-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Privacy-instellingen](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="6f86f-115">Selecteer **Opslaan** en sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f86f-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="6f86f-116">Modulegebaseerde afmelding</span><span class="sxs-lookup"><span data-stu-id="6f86f-116">Module-based opt-out experience</span></span>

<span data-ttu-id="6f86f-117">Beheerders kunnen geverifieerde gebruikers zichzelf laten afmelden voor het verzamelen van gebeurtenissen voor webactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="6f86f-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="6f86f-118">Voeg de afmeldingsmodule voor gebruikers toe aan klantrekeningprofielpagina's om deze methode van afmelding te kunnen bieden.</span><span class="sxs-lookup"><span data-stu-id="6f86f-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="6f86f-119">Aangepaste extensies</span><span class="sxs-lookup"><span data-stu-id="6f86f-119">Custom extensions</span></span>

<span data-ttu-id="6f86f-120">Beheerders kunnen hun eigen extensies maken om de afmelding voor gebruikers te beheren.</span><span class="sxs-lookup"><span data-stu-id="6f86f-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="6f86f-121">Zie [Retail Server-API's aanroepen](e-commerce-extensibility/call-retail-server-apis.md) en [Uitbreidbaarheid van online afzetkanaal](e-commerce-extensibility/overview.md). voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6f86f-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
