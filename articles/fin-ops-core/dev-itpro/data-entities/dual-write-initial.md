---
title: Uitvoeringsvolgorde voor de eerste synchronisatie van Finance and Operations-apps en Common Data Service
description: In dit onderwerp wordt de synchronisatievolgorde aangegeven die u moet volgen om de eerste gegevens te maken.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769632"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="eebfb-103">Uitvoeringsvolgorde voor de eerste synchronisatie van Finance and Operations-apps en Common Data Service</span><span class="sxs-lookup"><span data-stu-id="eebfb-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eebfb-104">Voordat u gegevensintegratie gebruikt, moet u de eerste gegevens maken die vereist zijn voor klanten, leveranciers en contactpersonen.</span><span class="sxs-lookup"><span data-stu-id="eebfb-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="eebfb-105">U wilt bijvoorbeeld een nieuw **Leveranciersgroepartikel** maken en de **Betalingscondities** instellen op **Net30.**</span><span class="sxs-lookup"><span data-stu-id="eebfb-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="eebfb-106">Voordat u het artikel in de **Leveranciersgroep** gaat maken, moet u er in dat geval voor zorgen dat **Net30** bestaat in zowel de toepassing en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eebfb-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="eebfb-107">(In de toekomst zal Microsoft in het platform Twee keer wegschrijven een functionaliteit met de naam Initiële synchronisatie uitbrengen. Deze functie voert een eenmalige gegevenssynchronisatie uit tussen de toepassing en Common Data Service als onderdeel van Twee keer wegschrijven.)</span><span class="sxs-lookup"><span data-stu-id="eebfb-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="eebfb-108">Microsoft geeft een toewijzing voor Twee keer wegschrijven uit voor alle referentiegegevens, inclusief **Betalingscondities** (betalingscondities).</span><span class="sxs-lookup"><span data-stu-id="eebfb-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="eebfb-109">Als u de initiële gegevens al in één systeem hebt, kan een kleine updatebewerking van een record Twee keer wegschrijven voor die record activeren.</span><span class="sxs-lookup"><span data-stu-id="eebfb-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="eebfb-110">U moet de volgende prioriteitsvolgorde volgen en ervoor zorgen dat de eerste gegevens beschikbaar zijn in zowel de toepassing als Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eebfb-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="eebfb-111">Leverancier</span><span class="sxs-lookup"><span data-stu-id="eebfb-111">Vendor</span></span>

<span data-ttu-id="eebfb-112">Dit is de volgorde van uitvoering voor de entiteit **Leverancier**:</span><span class="sxs-lookup"><span data-stu-id="eebfb-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="eebfb-113">Leveranciersgroep</span><span class="sxs-lookup"><span data-stu-id="eebfb-113">Vendor group</span></span>

    1. <span data-ttu-id="eebfb-114">Betalingstermijn</span><span class="sxs-lookup"><span data-stu-id="eebfb-114">Terms of payment</span></span>

        1. <span data-ttu-id="eebfb-115">Betalingsdag en -regels</span><span class="sxs-lookup"><span data-stu-id="eebfb-115">Payment day and lines</span></span>
        2. <span data-ttu-id="eebfb-116">Betalingsplanning</span><span class="sxs-lookup"><span data-stu-id="eebfb-116">Payment schedule</span></span>

2. <span data-ttu-id="eebfb-117">Leveranciersbetalingsmethode</span><span class="sxs-lookup"><span data-stu-id="eebfb-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="eebfb-118">Klant (organisatie)</span><span class="sxs-lookup"><span data-stu-id="eebfb-118">Customer (Organization)</span></span>

<span data-ttu-id="eebfb-119">Dit is de volgorde van uitvoering voor de entiteit **Klant**:</span><span class="sxs-lookup"><span data-stu-id="eebfb-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="eebfb-120">Klantgroep</span><span class="sxs-lookup"><span data-stu-id="eebfb-120">Customer group</span></span>

    1. <span data-ttu-id="eebfb-121">Betalingstermijn</span><span class="sxs-lookup"><span data-stu-id="eebfb-121">Terms of payment</span></span>

        1. <span data-ttu-id="eebfb-122">Betalingsdag en -regels</span><span class="sxs-lookup"><span data-stu-id="eebfb-122">Payment day and lines</span></span>
        2. <span data-ttu-id="eebfb-123">Betaling</span><span class="sxs-lookup"><span data-stu-id="eebfb-123">Payment</span></span> 

2. <span data-ttu-id="eebfb-124">Betalingsmethode van klant</span><span class="sxs-lookup"><span data-stu-id="eebfb-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="eebfb-125">Contactpersoon (persoon)</span><span class="sxs-lookup"><span data-stu-id="eebfb-125">Contact (Person)</span></span>

<span data-ttu-id="eebfb-126">Dit is de volgorde van uitvoering voor de entiteit **Contactpersoon**:</span><span class="sxs-lookup"><span data-stu-id="eebfb-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="eebfb-127">Klant</span><span class="sxs-lookup"><span data-stu-id="eebfb-127">Customer</span></span>
2. <span data-ttu-id="eebfb-128">Leverancier</span><span class="sxs-lookup"><span data-stu-id="eebfb-128">Vendor</span></span>
