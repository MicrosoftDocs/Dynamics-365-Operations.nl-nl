---
title: Uitvoeringsvolgorde voor de eerste synchronisatie van Finance and Operations en Common Data Service
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
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873123"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="68358-103">Uitvoeringsvolgorde voor de eerste synchronisatie van Finance and Operations en Common Data Service</span><span class="sxs-lookup"><span data-stu-id="68358-103">Execution order for initial synchronization of Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="68358-104">Voordat u gegevensintegratie gebruikt, moet u de eerste gegevens maken die vereist zijn voor klanten, leveranciers en contactpersonen.</span><span class="sxs-lookup"><span data-stu-id="68358-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="68358-105">U wilt bijvoorbeeld een nieuw **Leveranciersgroepartikel** maken en de **Betalingscondities** instellen op **Net30.**</span><span class="sxs-lookup"><span data-stu-id="68358-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="68358-106">Voordat u het artikel in de **Leveranciersgroep** gaat maken, moet u er in dat geval voor zorgen dat **Net30** bestaat in zowel Microsoft Dynamics 365 for Finance and Operations en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="68358-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both Microsoft Dynamics 365 for Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="68358-107">(In de toekomst zal Microsoft in het platform Twee keer wegschrijven een functionaliteit met de naam Initiële synchronisatie uitbrengen. Deze functie voert een eenmalige gegevenssynchronisatie uit tussen Finance and Operations en Common Data Service als onderdeel van Twee keer wegschrijven.)</span><span class="sxs-lookup"><span data-stu-id="68358-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="68358-108">Microsoft geeft een toewijzing voor Twee keer wegschrijven uit voor alle referentiegegevens, inclusief **Betalingscondities** (betalingscondities).</span><span class="sxs-lookup"><span data-stu-id="68358-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="68358-109">Als u de initiële gegevens al in één systeem hebt, kan een kleine updatebewerking van een record Twee keer wegschrijven voor die record activeren.</span><span class="sxs-lookup"><span data-stu-id="68358-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="68358-110">U moet de volgende prioriteitsvolgorde volgen en ervoor zorgen dat de eerste gegevens beschikbaar zijn in zowel Finance and Operations als Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="68358-110">You must follow the following order of precedence and make sure that the initial data is available in both Finance and Operations and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="68358-111">Leverancier</span><span class="sxs-lookup"><span data-stu-id="68358-111">Vendor</span></span>

<span data-ttu-id="68358-112">Dit is de volgorde van uitvoering voor de entiteit **Leverancier**:</span><span class="sxs-lookup"><span data-stu-id="68358-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="68358-113">Leveranciersgroep</span><span class="sxs-lookup"><span data-stu-id="68358-113">Vendor group</span></span>

    1. <span data-ttu-id="68358-114">Betalingstermijn</span><span class="sxs-lookup"><span data-stu-id="68358-114">Terms of payment</span></span>

        1. <span data-ttu-id="68358-115">Betalingsdag en -regels</span><span class="sxs-lookup"><span data-stu-id="68358-115">Payment day and lines</span></span>
        2. <span data-ttu-id="68358-116">Betalingsplanning</span><span class="sxs-lookup"><span data-stu-id="68358-116">Payment schedule</span></span>

2. <span data-ttu-id="68358-117">Leveranciersbetalingsmethode</span><span class="sxs-lookup"><span data-stu-id="68358-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="68358-118">Klant (organisatie)</span><span class="sxs-lookup"><span data-stu-id="68358-118">Customer (Organization)</span></span>

<span data-ttu-id="68358-119">Dit is de volgorde van uitvoering voor de entiteit **Klant**:</span><span class="sxs-lookup"><span data-stu-id="68358-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="68358-120">Klantgroep</span><span class="sxs-lookup"><span data-stu-id="68358-120">Customer group</span></span>

    1. <span data-ttu-id="68358-121">Betalingstermijn</span><span class="sxs-lookup"><span data-stu-id="68358-121">Terms of payment</span></span>

        1. <span data-ttu-id="68358-122">Betalingsdag en -regels</span><span class="sxs-lookup"><span data-stu-id="68358-122">Payment day and lines</span></span>
        2. <span data-ttu-id="68358-123">Betaling</span><span class="sxs-lookup"><span data-stu-id="68358-123">Payment</span></span> 

2. <span data-ttu-id="68358-124">Betalingsmethode van klant</span><span class="sxs-lookup"><span data-stu-id="68358-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="68358-125">Contactpersoon (persoon)</span><span class="sxs-lookup"><span data-stu-id="68358-125">Contact (Person)</span></span>

<span data-ttu-id="68358-126">Dit is de volgorde van uitvoering voor de entiteit **Contactpersoon**:</span><span class="sxs-lookup"><span data-stu-id="68358-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="68358-127">Klant</span><span class="sxs-lookup"><span data-stu-id="68358-127">Customer</span></span>
2. <span data-ttu-id="68358-128">Leverancier</span><span class="sxs-lookup"><span data-stu-id="68358-128">Vendor</span></span>
