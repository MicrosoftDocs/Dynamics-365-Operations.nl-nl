---
title: Verbeterde afhandeling van artikelen met batchtracering
description: In dit onderwerp worden de verbeteringen beschreven die zijn aangebracht in de batchafhandeling van artikelen met batchtracering tijdens het proces voor boeken van detailhandeloverzichten.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617384"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="4a283-103">Verbeterde afhandeling van artikelen met batchtracering</span><span class="sxs-lookup"><span data-stu-id="4a283-103">Improved handling of batch-tracked items</span></span>

<span data-ttu-id="4a283-104">In Microsoft Dynamics 365 for Retail Point of Sale (POS) kunnen op het moment van verkoop geen batchnummers worden vastgelegd voor artikelen met batchtracering.</span><span class="sxs-lookup"><span data-stu-id="4a283-104">In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="4a283-105">Voor specifieke configuraties wanneer de verkoop wordt geboekt in het hoofdkantoor via klantorders of het boeken van overzichten, verwacht het Microsoft Dynamics-systeem dat er geldige batchnummers zijn voor artikelen met batchtracering en dat deze worden gebruikt bij de facturering.</span><span class="sxs-lookup"><span data-stu-id="4a283-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="4a283-106">Als er geldige batchnummers beschikbaar zijn voor producten, worden deze gebruikt door de factureringsprocessen voor klantorder en verkooporder op basis van de overzichtboekingen.</span><span class="sxs-lookup"><span data-stu-id="4a283-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="4a283-107">Anders kan het factureringsproces voor de klantorder niet worden geboekt en ontvangt de POS-gebruiker een foutmelding.</span><span class="sxs-lookup"><span data-stu-id="4a283-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="4a283-108">De overzichtboeking gaat vervolgens naar een foutstatus.</span><span class="sxs-lookup"><span data-stu-id="4a283-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="4a283-109">Deze foutstatus vindt ook plaats wanneer negatieve voorraad is ingeschakeld voor de producten.</span><span class="sxs-lookup"><span data-stu-id="4a283-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="4a283-110">Verbeteringen in Microsoft Dynamics for Retail versie 10.0.4 en later zorgen dat wanneer negatieve voorraad is ingeschakeld voor artikelen met batchtracering, facturering van klantorder en verkooporder via overzichtboekingen niet worden geblokkeerd voor deze artikelen als de voorraad 0 (nul) is of er geen batchnummer beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="4a283-110">Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="4a283-111">Bij de nieuwe functionaliteit wordt een standaard batch-id gebruikt voor de verkoopregels wanneer er geen batchnummers beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="4a283-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="4a283-112">Als u de standaard batch-id wilt definiëren die wordt gebruikt voor klantorders, gaat u op de pagina **Detailhandelparameters** naar het tabblad **Klantorders** en stelt u op het sneltabblad **Order** het veld **Standaard batch-id** in.</span><span class="sxs-lookup"><span data-stu-id="4a283-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="4a283-113">Als u de standaard batch-id wilt definiëren die wordt gebruikt voor de facturering van verkooporders op basis van overzichtboekingen, gaat u op de pagina **Detailhandelparameters** naar het tabblad **Boeking** en stelt u op het sneltabblad **Voorraad bijwerken** het veld **Standaard batch-id** in.</span><span class="sxs-lookup"><span data-stu-id="4a283-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="4a283-114">Deze functionaliteit is alleen beschikbaar wanneer geavanceerde magazijnfuncties zijn ingeschakeld voor het specifieke winkelmagazijn en de artikelen.</span><span class="sxs-lookup"><span data-stu-id="4a283-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="4a283-115">In een latere versie wordt de functionaliteit ook ondersteund voor scenario's waarbij geavanceerd magazijnbeheer niet wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4a283-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>
