---
title: Problemen met inkomende magazijnbewerkingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomende magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828221"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="041f8-103">Problemen met inkomende magazijnbewerkingen oplossen</span><span class="sxs-lookup"><span data-stu-id="041f8-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="041f8-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomende magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="041f8-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="041f8-105">Het volgende foutbericht wordt weergegeven: "Kwaliteitsorder %1 is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="041f8-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="041f8-106">Kan het clusterprofiel niet vinden, controleer uw configuratie."</span><span class="sxs-lookup"><span data-stu-id="041f8-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="041f8-107">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="041f8-107">Issue description</span></span>

<span data-ttu-id="041f8-108">Dit foutbericht is gerelateerd aan een ontvangstproces waarbij kwaliteitsbeheer (QMS) is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="041f8-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="041f8-109">Afhankelijk van de configuratie in uw omgeving, kunt u het probleem mogelijk oplossen met aanvullende informatie over de transactie die het foutbericht genereert.</span><span class="sxs-lookup"><span data-stu-id="041f8-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="041f8-110">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="041f8-110">Issue resolution</span></span>

<span data-ttu-id="041f8-111">Controleer eerst de instellingen voor [clusterverzameling](set-up-cluster-picking.md) en controleer of de clusterprofielen juist zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="041f8-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="041f8-112">U kunt een menuopdracht voor een mobiel apparaat voor clusterverzameling alleen gebruiken als clusterprofielen zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="041f8-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="041f8-113">Afhankelijk van uw omgeving, moet u mogelijk ook andere gerelateerde configuraties controleren.</span><span class="sxs-lookup"><span data-stu-id="041f8-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="041f8-114">Gecombineerde nummerplaat ontvangen werkt niet voor beschikkingscodes behalve Credit.</span><span class="sxs-lookup"><span data-stu-id="041f8-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="041f8-115">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="041f8-115">Issue description</span></span>

<span data-ttu-id="041f8-116">Wanneer het veld **Actie** voor een beschikkingscode is ingesteld op *Credit* of *Uitval*, kunt u de menuopdracht [Gecombineerde nummerplaat ontvangen](mixed-license-plate-receiving.md) alleen gebruiken om geretourneerde artikelen te verwerken.</span><span class="sxs-lookup"><span data-stu-id="041f8-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="041f8-117">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="041f8-117">Issue resolution</span></span>

<span data-ttu-id="041f8-118">Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is.</span><span class="sxs-lookup"><span data-stu-id="041f8-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="041f8-119">Op dit moment worden alleen [beschikkingscodes](../service-management/set-up-disposition-codes.md) waarvoor het veld **Actie** is ingesteld op *Credit* of *Uitval* ondersteund voor gecombineerde nummerplaat ontvangen.</span><span class="sxs-lookup"><span data-stu-id="041f8-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="041f8-120">Wanneer ik de periodieke taak Productontvangsten bijwerken uitvoer, worden onbevestigde inkooporders bevestigd.</span><span class="sxs-lookup"><span data-stu-id="041f8-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="041f8-121">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="041f8-121">Issue description</span></span>

<span data-ttu-id="041f8-122">Nadat u de periodieke taak *Productontvangsten bijwerken* hebt uitgevoerd, bevestigt het systeem automatisch onbevestigde inkooporders met de voorraadtransactiestatus *Geregistreerd*.</span><span class="sxs-lookup"><span data-stu-id="041f8-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="041f8-123">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="041f8-123">Issue resolution</span></span>

<span data-ttu-id="041f8-124">Met een nieuwe functie voor verwerking van inkomende ladingen, *Meerontvangst voor ladinghoeveelheden*, wordt dit probleem opgelost.</span><span class="sxs-lookup"><span data-stu-id="041f8-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="041f8-125">Als u deze functies wilt inschakeln, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de volgende functies in (in de volgorde waarin ze staan):</span><span class="sxs-lookup"><span data-stu-id="041f8-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="041f8-126">Voorraadtransacties van inkooporder koppelen aan lading</span><span class="sxs-lookup"><span data-stu-id="041f8-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="041f8-127">Te grote ontvangst van laadhoeveelheden</span><span class="sxs-lookup"><span data-stu-id="041f8-127">Over receipt of load quantities</span></span>

<span data-ttu-id="041f8-128">Zie [Geregistreerde ladinghoeveelheden boeken op inkooporders](inbound-load-handling.md#post-registered-quantities) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="041f8-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="041f8-129">Wanneer ik inkomende orders registreer, krijg ik het volgende foutbericht: 'De hoeveelheid is niet geldig'.</span><span class="sxs-lookup"><span data-stu-id="041f8-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="041f8-130">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="041f8-130">Issue description</span></span>

<span data-ttu-id="041f8-131">Als het veld **Groeperingsbeleid nummerplaten** is ingesteld op *Door gebruiker gedefinieerd* voor een menu-item voor mobiele apparaten dat wordt gebruikt om inkomende orders te registreren, ontvangt u een foutbericht ('De hoeveelheid is niet geldig') en kunt u de registratie niet voltooien.</span><span class="sxs-lookup"><span data-stu-id="041f8-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="041f8-132">Oorzaak van probleem</span><span class="sxs-lookup"><span data-stu-id="041f8-132">Issue cause</span></span>

<span data-ttu-id="041f8-133">Wanneer *Door gebruiker gedefinieerd* wordt gebruikt als groeperingsbeleid voor kentekenplaten, splitst het systeem de inkomende voorraad op in afzonderlijke nummerplaten, zoals aangegeven door de eenheidsvolgordegroep.</span><span class="sxs-lookup"><span data-stu-id="041f8-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="041f8-134">Als batch- of serienummers worden gebruikt om het artikel bij te houden dat wordt ontvangen, moeten de hoeveelheden van elke batch of serie worden opgegeven per nummerplaat die is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="041f8-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="041f8-135">Als de hoeveelheid die is opgegeven voor een nummerplaat groter is dan de hoeveelheid die nog moet worden ontvangen voor de huidige dimensies, wordt het foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="041f8-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="041f8-136">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="041f8-136">Issue resolution</span></span>

<span data-ttu-id="041f8-137">Wanneer u een artikel registreert met behulp van een menu-item voor mobiele apparaten waarbij het veld **Groeperingsbeleid nummerplaten** is ingesteld op *Door gebruiker gedefinieerd*, moet u mogelijk nummerplaatnummers, batchnummers of serienummers bevestigen of invoeren.</span><span class="sxs-lookup"><span data-stu-id="041f8-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="041f8-138">Op de bevestigingspagina van de nummerplaat toont het systeem de hoeveelheid die is toegewezen voor de huidige nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="041f8-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="041f8-139">Op de bevestigingspagina's voor batch- of serienummers toont het systeem de hoeveelheid die nog moet worden ontvangen voor de huidige nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="041f8-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="041f8-140">Het bevat ook een veld waarin u de hoeveelheid kunt invoeren die u wilt registreren voor die combinatie van nummerplaat en batch- of serienummer.</span><span class="sxs-lookup"><span data-stu-id="041f8-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="041f8-141">Zorg er in dat geval voor dat de hoeveelheid die wordt geregistreerd voor de nummerplaat niet groter is dan de hoeveelheid die nog moet worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="041f8-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="041f8-142">Als er te veel nummerplaten worden gegenereerd bij inkomende orderregistratie, kan de waarde van het veld **Groeperingsbeleid nummerplaten** worden gewijzigd in *Nummerplaatgroepering*, kan een nieuwe eenheidsvolgordegroep aan het artikel worden toegewezen of kan de optie **Nummerplaatgroepering** worden gedeactiveerd voor de eenheidsvolgordegroep.</span><span class="sxs-lookup"><span data-stu-id="041f8-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
