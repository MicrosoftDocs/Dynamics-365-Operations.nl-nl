---
title: Problemen met inkomende magazijnbewerkingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomende magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970238"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="d61a0-103">Problemen met inkomende magazijnbewerkingen oplossen</span><span class="sxs-lookup"><span data-stu-id="d61a0-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d61a0-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomende magazijnbewerkingen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d61a0-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="d61a0-105">Het volgende foutbericht wordt weergegeven: "Kwaliteitsorder %1 is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d61a0-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="d61a0-106">Kan het clusterprofiel niet vinden, controleer uw configuratie."</span><span class="sxs-lookup"><span data-stu-id="d61a0-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d61a0-107">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d61a0-107">Issue description</span></span>

<span data-ttu-id="d61a0-108">Dit foutbericht is gerelateerd aan een ontvangstproces waarbij kwaliteitsbeheer (QMS) is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d61a0-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="d61a0-109">Afhankelijk van de configuratie in uw omgeving, kunt u het probleem mogelijk oplossen met aanvullende informatie over de transactie die het foutbericht genereert.</span><span class="sxs-lookup"><span data-stu-id="d61a0-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d61a0-110">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d61a0-110">Issue resolution</span></span>

<span data-ttu-id="d61a0-111">Controleer eerst de instellingen voor [clusterverzameling](set-up-cluster-picking.md) en controleer of de clusterprofielen juist zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d61a0-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="d61a0-112">U kunt een menuopdracht voor een mobiel apparaat voor clusterverzameling alleen gebruiken als clusterprofielen zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d61a0-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="d61a0-113">Afhankelijk van uw omgeving, moet u mogelijk ook andere gerelateerde configuraties controleren.</span><span class="sxs-lookup"><span data-stu-id="d61a0-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="d61a0-114">Gecombineerde nummerplaat ontvangen werkt niet voor beschikkingscodes behalve Credit.</span><span class="sxs-lookup"><span data-stu-id="d61a0-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d61a0-115">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d61a0-115">Issue description</span></span>

<span data-ttu-id="d61a0-116">Wanneer het veld **Actie** voor een beschikkingscode is ingesteld op *Credit* of *Uitval*, kunt u de menuopdracht [Gecombineerde nummerplaat ontvangen](mixed-license-plate-receiving.md) alleen gebruiken om geretourneerde artikelen te verwerken.</span><span class="sxs-lookup"><span data-stu-id="d61a0-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d61a0-117">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d61a0-117">Issue resolution</span></span>

<span data-ttu-id="d61a0-118">Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is.</span><span class="sxs-lookup"><span data-stu-id="d61a0-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="d61a0-119">Op dit moment worden alleen [beschikkingscodes](../service-management/set-up-disposition-codes.md) waarvoor het veld **Actie** is ingesteld op *Credit* of *Uitval* ondersteund voor gecombineerde nummerplaat ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d61a0-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="d61a0-120">Wanneer ik de periodieke taak Productontvangsten bijwerken uitvoer, worden onbevestigde inkooporders bevestigd.</span><span class="sxs-lookup"><span data-stu-id="d61a0-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d61a0-121">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d61a0-121">Issue description</span></span>

<span data-ttu-id="d61a0-122">Nadat u de periodieke taak *Productontvangsten bijwerken* hebt uitgevoerd, bevestigt het systeem automatisch onbevestigde inkooporders met de voorraadtransactiestatus *Geregistreerd*.</span><span class="sxs-lookup"><span data-stu-id="d61a0-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d61a0-123">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d61a0-123">Issue resolution</span></span>

<span data-ttu-id="d61a0-124">Met een nieuwe functie voor verwerking van inkomende ladingen, *Meerontvangst voor ladinghoeveelheden*, wordt dit probleem opgelost.</span><span class="sxs-lookup"><span data-stu-id="d61a0-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="d61a0-125">Als u deze functies wilt inschakeln, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de volgende functies in (in de volgorde waarin ze staan):</span><span class="sxs-lookup"><span data-stu-id="d61a0-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="d61a0-126">Voorraadtransacties van inkooporder koppelen aan lading</span><span class="sxs-lookup"><span data-stu-id="d61a0-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="d61a0-127">Te grote ontvangst van laadhoeveelheden</span><span class="sxs-lookup"><span data-stu-id="d61a0-127">Over receipt of load quantities</span></span>

<span data-ttu-id="d61a0-128">Zie [Geregistreerde ladinghoeveelheden boeken op inkooporders](inbound-load-handling.md#post-registered-quantities) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d61a0-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>
