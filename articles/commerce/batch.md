---
title: Verbeterde afhandeling van artikelen met batchtracering
description: In dit onderwerp worden de verbeteringen beschreven die zijn aangebracht in de batchafhandeling van artikelen met batchtracering tijdens het proces voor boeken van overzichten.
author: josaw1
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2453ed711d47e062c82d3888ff471b770b5bb2ef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799704"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="6288b-103">Verbeterde afhandeling van artikelen met batchtracering</span><span class="sxs-lookup"><span data-stu-id="6288b-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="6288b-104">In Point of Sale (POS) kunnen op het moment van verkoop geen batchnummers worden vastgelegd voor artikelen met batchtracering.</span><span class="sxs-lookup"><span data-stu-id="6288b-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="6288b-105">Voor specifieke configuraties wanneer de verkoop wordt geboekt in het hoofdkantoor via klantorders of het boeken van overzichten, verwacht het Microsoft Dynamics-systeem dat er geldige batchnummers zijn voor artikelen met batchtracering en dat deze worden gebruikt bij de facturering.</span><span class="sxs-lookup"><span data-stu-id="6288b-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="6288b-106">Als er geldige batchnummers beschikbaar zijn voor producten, worden deze gebruikt door de factureringsprocessen voor klantorder en verkooporder op basis van de overzichtboekingen.</span><span class="sxs-lookup"><span data-stu-id="6288b-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="6288b-107">Anders kan het factureringsproces voor de klantorder niet worden geboekt en ontvangt de POS-gebruiker een foutmelding.</span><span class="sxs-lookup"><span data-stu-id="6288b-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="6288b-108">De overzichtboeking gaat vervolgens naar een foutstatus.</span><span class="sxs-lookup"><span data-stu-id="6288b-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="6288b-109">Deze foutstatus vindt ook plaats wanneer negatieve voorraad is ingeschakeld voor de producten.</span><span class="sxs-lookup"><span data-stu-id="6288b-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="6288b-110">Verbeteringen in Retail versie 10.0.4 en later zorgen dat wanneer negatieve voorraad is ingeschakeld voor artikelen met batchtracering, facturering van klantorder en verkooporder via overzichtboekingen niet worden geblokkeerd voor deze artikelen als de voorraad 0 (nul) is of er geen batchnummer beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="6288b-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="6288b-111">Bij de nieuwe functionaliteit wordt een standaard batch-id gebruikt voor de verkoopregels wanneer er geen batchnummers beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="6288b-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="6288b-112">Als u de standaard batch-id wilt definiëren die wordt gebruikt voor klantorders, gaat u op de pagina **Commerce-parameters** naar het tabblad **Klantorders** en stelt u op het sneltabblad **Order** het veld **Standaard batch-id** in.</span><span class="sxs-lookup"><span data-stu-id="6288b-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="6288b-113">Als u de standaard batch-id wilt definiëren die wordt gebruikt voor de facturering van verkooporders op basis van overzichtboekingen, gaat u op de pagina **Commerce-parameters** naar het tabblad **Boeking** en stelt u op het sneltabblad **Voorraad bijwerken** het veld **Standaard batch-id** in.</span><span class="sxs-lookup"><span data-stu-id="6288b-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="6288b-114">Deze functionaliteit is alleen beschikbaar wanneer geavanceerde magazijnfuncties zijn ingeschakeld voor het specifieke winkelmagazijn en de artikelen.</span><span class="sxs-lookup"><span data-stu-id="6288b-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="6288b-115">In een latere versie wordt de functionaliteit ook ondersteund voor scenario's waarbij geavanceerd magazijnbeheer niet wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6288b-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="6288b-116">Ondersteuning voor de verbeterde verwerking van artikelen met batchtracering tijdens overzichtsboekingen voor niet-geavanceerde magazijnbeheerscenario's is geïntroduceerd in Retail versie 10.0.5.</span><span class="sxs-lookup"><span data-stu-id="6288b-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]