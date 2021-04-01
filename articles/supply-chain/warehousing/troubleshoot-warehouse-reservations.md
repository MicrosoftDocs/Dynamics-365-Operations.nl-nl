---
title: Problemen met reserveringen in magazijnbeheer oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnreserveringen in Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: a9a5d20732a802fc58c392853af8334bbc07de73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248710"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="f7881-103">Problemen met reserveringen in magazijnbeheer oplossen</span><span class="sxs-lookup"><span data-stu-id="f7881-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7881-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnreserveringen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f7881-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="f7881-105">Ik krijg het volgende foutbericht: "Reserveringen kunnen niet worden verwijderd omdat er werk is gemaakt dat afhankelijk is van de reserveringen."</span><span class="sxs-lookup"><span data-stu-id="f7881-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f7881-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="f7881-106">Issue description</span></span>

<span data-ttu-id="f7881-107">U kunt de reservering van voorraad op een verkoopregel niet verwijderen, omdat er openstaand werk is voor de regel.</span><span class="sxs-lookup"><span data-stu-id="f7881-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f7881-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="f7881-108">Issue resolution</span></span>

<span data-ttu-id="f7881-109">Controleer of er openstaand werk van een verpakkingsgroep bestaat om het artikel van een inpakstation naar een andere locatie te brengen (bijvoorbeeld *Laaddeur*).</span><span class="sxs-lookup"><span data-stu-id="f7881-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="f7881-110">Bekijk de records in het **Historielogboek van werkaanmaak** en de pagina's **Werkgegevens** om te bepalen wat het is dat fysiek de voorraad reserveert en voer vervolgens de voltooiing of verwijdering van het werk uit om de reservering vrij te maken.</span><span class="sxs-lookup"><span data-stu-id="f7881-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="f7881-111">Het volgende foutbericht wordt weergegeven: "Voorraadhoeveelheid -%1 kan niet worden bijgewerkt vanwege onvoldoende voorraadtransacties voor artikel %2...."</span><span class="sxs-lookup"><span data-stu-id="f7881-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f7881-112">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="f7881-112">Issue description</span></span>

<span data-ttu-id="f7881-113">Dit probleem kan optreden als het systeem geen voorraadhoeveelheid kan bijwerken omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn.</span><span class="sxs-lookup"><span data-stu-id="f7881-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="f7881-114">Hier volgt de hele tekst van het volledige foutbericht:</span><span class="sxs-lookup"><span data-stu-id="f7881-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="f7881-115">Voorraad hoeveelheid -%1 kan niet worden bijgewerkt vanwege onvoldoende voorraadtransacties voor artikel %2 met dimensies Grootte =%3, Kleur=%4, Toevoegingen=%5, Site=%6, Magazijn=%7, Locatie=%8, Voorraadstatus=beschikbaar, Nummerplaat=%9, Batchnummer=%10 voor verwijzing-id %11 op partij-id %12.</span><span class="sxs-lookup"><span data-stu-id="f7881-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f7881-116">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="f7881-116">Issue resolution</span></span>

<span data-ttu-id="f7881-117">Zorg ervoor dat er geen voorraadtransacties zijn die de hoeveelheid fysiek reserveren.</span><span class="sxs-lookup"><span data-stu-id="f7881-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="f7881-118">Deze transacties kunnen bijvoorbeeld openstaande kwaliteitsorders, voorraadblokkeringsrecords of uitvoerorders zijn.</span><span class="sxs-lookup"><span data-stu-id="f7881-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="f7881-119">Het volgende foutbericht wordt weergegeven: "Fysieke voorhanden...kan niet worden gereserveerd omdat slechts 0,00 in de voorraad beschikbaar zijn."</span><span class="sxs-lookup"><span data-stu-id="f7881-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f7881-120">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="f7881-120">Issue description</span></span>

<span data-ttu-id="f7881-121">Dit probleem kan optreden als het systeem geen voorraadhoeveelheid kan bijwerken omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn.</span><span class="sxs-lookup"><span data-stu-id="f7881-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="f7881-122">Hier volgt de hele tekst van het volledige foutbericht:</span><span class="sxs-lookup"><span data-stu-id="f7881-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="f7881-123">Fysiek voorhanden Site=%1, Magazijn=%2, Voorraadstatus=beschikbaar, Batchnummer=%3, Eigenaar=%4: %5 kan niet worden gereserveerd omdat slechts 0,00 in de voorraad beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="f7881-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f7881-124">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="f7881-124">Issue resolution</span></span>

<span data-ttu-id="f7881-125">Dit probleem wordt waarschijnlijk veroorzaakt door openstaand werk.</span><span class="sxs-lookup"><span data-stu-id="f7881-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="f7881-126">Voltooi het werk of ontvang een taak zonder werk te maken.</span><span class="sxs-lookup"><span data-stu-id="f7881-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="f7881-127">Zorg ervoor dat er geen voorraadtransacties zijn die de hoeveelheid fysiek reserveren.</span><span class="sxs-lookup"><span data-stu-id="f7881-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="f7881-128">Deze transacties kunnen bijvoorbeeld openstaande kwaliteitsorders, voorraadblokkeringsrecords of uitvoerorders zijn.</span><span class="sxs-lookup"><span data-stu-id="f7881-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="f7881-129">Het volgende foutbericht wordt weergegeven: "Om aan wave te worden toegewezen, moeten ladingsregels de afmetingen boven de locatie aangeven.</span><span class="sxs-lookup"><span data-stu-id="f7881-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="f7881-130">Als u deze dimensies wilt toewijzen, moet u de ladingsregel reserveren en opnieuw maken."</span><span class="sxs-lookup"><span data-stu-id="f7881-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f7881-131">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="f7881-131">Issue description</span></span>

<span data-ttu-id="f7881-132">Wanneer u een artikel gebruikt met een 'batch erboven'-reserveringshiërarchie (waarbij de dimensie **Batchnummer** *boven* de dimensie **Locatie** is geplaatst), werkt de opdracht **Vrijgeven aan magazijn** op de pagina **Workbench ladingplanning** voor een gedeeltelijke hoeveelheid niet.</span><span class="sxs-lookup"><span data-stu-id="f7881-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="f7881-133">Dit foutbericht wordt weergegeven en er wordt geen werk gemaakt voor de gedeeltelijke hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="f7881-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="f7881-134">Wanneer u echter een artikel gebruikt met een 'batch eronder'-reserveringshiërarchie (waarbij de dimensie **Batchnummer** *onder* de dimensie **Locatie** is geplaatst), kunt u een lading vrijgeven vanuit de pagina **Workbench ladingplanning** voor een gedeeltelijke hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="f7881-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f7881-135">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="f7881-135">Issue resolution</span></span>

<span data-ttu-id="f7881-136">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="f7881-136">This behavior is by design.</span></span> <span data-ttu-id="f7881-137">Als u een dimensie boven de dimensie **Locatie** in de reserveringshiërarchie plaatst, moet u deze eerst opgeven voordat wordt vrijgegeven aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="f7881-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="f7881-138">Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking was tijdens vrijgaven van het magazijn vanuit de workbench Ladingplanning.</span><span class="sxs-lookup"><span data-stu-id="f7881-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="f7881-139">Gedeeltelijke hoeveelheden kunnen niet worden vrijgegeven als een of meer dimensies boven de **locatie** niet zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="f7881-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="f7881-140">Zie voor meer informatie [Flexibel reserveringsbeleid voor dimensies op magazijnniveau](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="f7881-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]