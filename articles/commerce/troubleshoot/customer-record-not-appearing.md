---
title: Klantrecords worden niet weergegeven in Commerce Headquarters
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen wanneer klantrecords niet direct in Commerce Headquarters worden weergegeven.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018477"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="b4f2d-103">Klantrecords worden niet weergegeven in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="b4f2d-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4f2d-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die u kunnen helpen wanneer klantrecords niet direct in Commerce Headquarters worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="b4f2d-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b4f2d-105">Description</span></span>

<span data-ttu-id="b4f2d-106">Wanneer u een nieuwe klantrecord maakt met de aanmeldingsstroom in de e-commerce-winkel, wordt de bijbehorende klantrecord niet direct weergegeven in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="b4f2d-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="b4f2d-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="b4f2d-108">Maken van klant in asynchrone modus uitschakelen</span><span class="sxs-lookup"><span data-stu-id="b4f2d-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4f2d-109">Als u het asynchroon maken van klanten uitschakelt, kan dit gevolgen hebben voor de systeemprestaties, omdat er door het maken van elke record een realtime aanvraag voor Commerce Headquarters wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="b4f2d-110">Bovendien resulteren eventuele nieuwe stromen voor het maken van klanten in fouten als Commerce Headquarters inactief is (bijvoorbeeld tijdens het onderhoud).</span><span class="sxs-lookup"><span data-stu-id="b4f2d-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="b4f2d-111">Voer deze stappen uit om het maken van klanten in de asynchrone modus in Commerce Headquarters uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b4f2d-112">Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Onlinewinkel instellen \> Functionaliteitsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="b4f2d-113">Maak een functionaliteitsprofiel voor uw online afzetkanaal als u nog geen functionaliteitsprofiel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="b4f2d-114">Zorg ervoor dat de optie **Klant maken in asynchrone modus** is ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="b4f2d-115">Ga naar **Retail en Commerce \> Afzetkanalen \> Online winkels**.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="b4f2d-116">Selecteer de online winkel om het maken van klanten in de asynchrone modus uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="b4f2d-117">Ga naar het tabblad **Algemeen** en zorg ervoor dat het veld **Functionaliteitsprofiel** is ingesteld op het functionaliteitsprofiel dat u voor uw online kanaal gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b4f2d-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4f2d-118">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b4f2d-118">Additional resources</span></span>

[<span data-ttu-id="b4f2d-119">Een B2C-tenant instellen in Commerce</span><span class="sxs-lookup"><span data-stu-id="b4f2d-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
