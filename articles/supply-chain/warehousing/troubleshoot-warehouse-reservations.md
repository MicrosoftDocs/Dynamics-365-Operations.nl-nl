---
title: Problemen met reserveringen in magazijnbeheer oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnreserveringen in Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828101"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="3da3a-103">Problemen met reserveringen in magazijnbeheer oplossen</span><span class="sxs-lookup"><span data-stu-id="3da3a-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3da3a-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met magazijnreserveringen in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3da3a-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="3da3a-105">Zie [Problemen met magazijnbatch- en seriereserveringshiërarchieën oplossen](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) voor onderwerpen die betrekking hebben op batch- en serienummerregistraties.</span><span class="sxs-lookup"><span data-stu-id="3da3a-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="3da3a-106">Ik krijg het volgende foutbericht: "Reserveringen kunnen niet worden verwijderd omdat er werk is gemaakt dat afhankelijk is van de reserveringen."</span><span class="sxs-lookup"><span data-stu-id="3da3a-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3da3a-107">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="3da3a-107">Issue description</span></span>

<span data-ttu-id="3da3a-108">U kunt de reservering van voorraad op een verkoopregel niet verwijderen, omdat er openstaand werk is voor de regel.</span><span class="sxs-lookup"><span data-stu-id="3da3a-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3da3a-109">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="3da3a-109">Issue resolution</span></span>

<span data-ttu-id="3da3a-110">Controleer of er openstaand werk van een verpakkingsgroep bestaat om het artikel van een inpakstation naar een andere locatie te brengen (bijvoorbeeld *Laaddeur*).</span><span class="sxs-lookup"><span data-stu-id="3da3a-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="3da3a-111">Bekijk de records in het **Historielogboek van werkaanmaak** en de pagina's **Werkgegevens** om te bepalen wat het is dat fysiek de voorraad reserveert en voer vervolgens de voltooiing of verwijdering van het werk uit om de reservering vrij te maken.</span><span class="sxs-lookup"><span data-stu-id="3da3a-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="3da3a-112">Het volgende foutbericht wordt weergegeven: "Voorraadhoeveelheid -%1 kan niet worden bijgewerkt vanwege onvoldoende voorraadtransacties voor artikel %2...."</span><span class="sxs-lookup"><span data-stu-id="3da3a-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3da3a-113">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="3da3a-113">Issue description</span></span>

<span data-ttu-id="3da3a-114">Dit probleem kan optreden als het systeem geen voorraadhoeveelheid kan bijwerken omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn.</span><span class="sxs-lookup"><span data-stu-id="3da3a-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="3da3a-115">Hier volgt de hele tekst van het volledige foutbericht:</span><span class="sxs-lookup"><span data-stu-id="3da3a-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="3da3a-116">Voorraad hoeveelheid -%1 kan niet worden bijgewerkt vanwege onvoldoende voorraadtransacties voor artikel %2 met dimensies Grootte =%3, Kleur=%4, Toevoegingen=%5, Site=%6, Magazijn=%7, Locatie=%8, Voorraadstatus=beschikbaar, Nummerplaat=%9, Batchnummer=%10 voor verwijzing-id %11 op partij-id %12.</span><span class="sxs-lookup"><span data-stu-id="3da3a-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3da3a-117">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="3da3a-117">Issue resolution</span></span>

<span data-ttu-id="3da3a-118">Zorg ervoor dat er geen voorraadtransacties zijn die de hoeveelheid fysiek reserveren.</span><span class="sxs-lookup"><span data-stu-id="3da3a-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="3da3a-119">Deze transacties kunnen bijvoorbeeld openstaande kwaliteitsorders, voorraadblokkeringsrecords of uitvoerorders zijn.</span><span class="sxs-lookup"><span data-stu-id="3da3a-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="3da3a-120">Het volgende foutbericht wordt weergegeven: "Fysieke voorhanden...kan niet worden gereserveerd omdat slechts 0,00 in de voorraad beschikbaar zijn."</span><span class="sxs-lookup"><span data-stu-id="3da3a-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3da3a-121">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="3da3a-121">Issue description</span></span>

<span data-ttu-id="3da3a-122">Dit probleem kan optreden als het systeem geen voorraadhoeveelheid kan bijwerken omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn.</span><span class="sxs-lookup"><span data-stu-id="3da3a-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="3da3a-123">Hier volgt de hele tekst van het volledige foutbericht:</span><span class="sxs-lookup"><span data-stu-id="3da3a-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="3da3a-124">Fysiek voorhanden Site=%1, Magazijn=%2, Voorraadstatus=beschikbaar, Batchnummer=%3, Eigenaar=%4: %5 kan niet worden gereserveerd omdat slechts 0,00 in de voorraad beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="3da3a-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3da3a-125">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="3da3a-125">Issue resolution</span></span>

<span data-ttu-id="3da3a-126">Dit probleem wordt waarschijnlijk veroorzaakt door openstaand werk.</span><span class="sxs-lookup"><span data-stu-id="3da3a-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="3da3a-127">Voltooi het werk of ontvang een taak zonder werk te maken.</span><span class="sxs-lookup"><span data-stu-id="3da3a-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="3da3a-128">Zorg ervoor dat er geen voorraadtransacties zijn die de hoeveelheid fysiek reserveren.</span><span class="sxs-lookup"><span data-stu-id="3da3a-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="3da3a-129">Deze transacties kunnen bijvoorbeeld openstaande kwaliteitsorders, voorraadblokkeringsrecords of uitvoerorders zijn.</span><span class="sxs-lookup"><span data-stu-id="3da3a-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
