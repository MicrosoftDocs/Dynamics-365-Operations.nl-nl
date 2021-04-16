---
title: Standaardomschrijvingen voor het grootboek
description: Standaardomschrijvingen kunnen worden gebruikt om het veld Omschrijving bij te werken in boekstukboekingen naar het grootboek.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a38af57d614ae2c93b0af74ec4a1c085519d46
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841886"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="c3493-103">Standaardomschrijvingen voor het grootboek</span><span class="sxs-lookup"><span data-stu-id="c3493-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3493-104">Standaardomschrijvingen kunnen worden gebruikt om het veld **Omschrijving** bij te werken in boekstukboekingen naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="c3493-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="c3493-105">Deze functionaliteit is verbeterd om te werken met Francoprijzen.</span><span class="sxs-lookup"><span data-stu-id="c3493-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="c3493-106">Als u standaardomschrijvingen voor boekingen in het grootboek wilt instellen, gaat u naar **Organisatiebeheer \> Instellen \> Standaardomschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="c3493-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="c3493-107">In de volgende tabel worden de nieuwe waarden weergegeven die zijn toegevoegd aan het veld **Omschrijving** op de pagina **Standaardomschrijvingen** ter ondersteuning van de francoprijzen.</span><span class="sxs-lookup"><span data-stu-id="c3493-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="c3493-108">Type omschrijving</span><span class="sxs-lookup"><span data-stu-id="c3493-108">Description type</span></span> | <span data-ttu-id="c3493-109">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c3493-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="c3493-110">Kostprijsberekening bij import - Kostentoerekening</span><span class="sxs-lookup"><span data-stu-id="c3493-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="c3493-111">Wanneer een inkooporderfactuur wordt geboekt, wordt een kostentoerekening verwerkt voor ramingskosten.</span><span class="sxs-lookup"><span data-stu-id="c3493-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="c3493-112">Er kunnen standaardomschrijvingen worden opgegeven om het trajectnummer toe te voegen aan de omschrijving.</span><span class="sxs-lookup"><span data-stu-id="c3493-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="c3493-113">Gebruik *%4* voor het zendingsnummer.</span><span class="sxs-lookup"><span data-stu-id="c3493-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="c3493-114">Kostprijsberekening bij import - Order voor goederen in transit</span><span class="sxs-lookup"><span data-stu-id="c3493-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="c3493-115">Als u verwerking in transit gebruikt, wordt de inkooporderfactuur geboekt en worden de goederen geboekt naar een rekening voor goederen in transit.</span><span class="sxs-lookup"><span data-stu-id="c3493-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="c3493-116">Er kunnen standaardomschrijvingen worden opgegeven om het ordernummer in transit toe te voegen aan de omschrijving.</span><span class="sxs-lookup"><span data-stu-id="c3493-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="c3493-117">Gebruik *%4* voor het ordernummer in transit.</span><span class="sxs-lookup"><span data-stu-id="c3493-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="c3493-118">Voorraad - afsluiten - correctie</span><span class="sxs-lookup"><span data-stu-id="c3493-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="c3493-119">Wanneer de factuur voor de leveranciers wordt verwerkt voor trajectkosten, wordt een voorraadcorrectie verwerkt om trajectkosten te ramen.</span><span class="sxs-lookup"><span data-stu-id="c3493-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="c3493-120">Er kunnen standaardomschrijvingen worden opgegeven om het trajectnummer toe te voegen aan de omschrijving.</span><span class="sxs-lookup"><span data-stu-id="c3493-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="c3493-121">Gebruik *%4* voor het zendingsnummer.</span><span class="sxs-lookup"><span data-stu-id="c3493-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="c3493-122">Zie [Standaardomschrijvingen voor automatische boeking instellen](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md) voor meer informatie over het werken met de pagina **Standaardomschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="c3493-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
