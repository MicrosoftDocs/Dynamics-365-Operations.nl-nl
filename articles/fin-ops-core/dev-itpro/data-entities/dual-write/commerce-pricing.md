---
title: De Dynamics 365 Commerce-prijsengine gebruiken met Dynamics 365 Sales
description: In dit onderwerp wordt beschreven hoe u de prijsengine in Microsoft Dynamics 365 Commerce gebruikt om verkoopoffertes te maken in Dynamics 365 Sales.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594913"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="4e818-103">De Dynamics 365 Commerce-prijsengine gebruiken met Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="4e818-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e818-104">In dit onderwerp wordt beschreven hoe u de prijsengine in Microsoft Dynamics 365 Commerce gebruikt om verkoopoffertes te maken in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="4e818-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="4e818-105">De Dynamics 365 Commerce-prijsengine ondersteunt de meeste B2C-prijsscenario's (Business-to-consumer), zoals prijzen op winkelniveau, prijzen op basis van relatie en loyaliteit, combinatiekortingen, kwantumkortingen en drempelkortingen.</span><span class="sxs-lookup"><span data-stu-id="4e818-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="4e818-106">De prijsengine gebruikt complexe regels om de beste prijs voor een bepaalde offerte of order te bepalen.</span><span class="sxs-lookup"><span data-stu-id="4e818-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="4e818-107">Wanneer u [twee keer wegschrijven](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) gebruikt, hebt u drie opties voor uw prijsbehoeften.</span><span class="sxs-lookup"><span data-stu-id="4e818-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="4e818-108">U kunt de statische prijzen gebruiken die afkomstig zijn van de prijslijst in Dynamics 365 Sales, de prijsengine in Dynamics 365 Supply Chain Management of de prijsengine in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e818-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="4e818-109">Onder deze opties is de Commerce-prijsengine het meest geschikt voor B2C-scenario's.</span><span class="sxs-lookup"><span data-stu-id="4e818-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="4e818-110">De Commerce-prijsengine gebruiken in Sales</span><span class="sxs-lookup"><span data-stu-id="4e818-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="4e818-111">Op dit moment kan de Commerce-prijsengine alleen worden gebruikt voor het maken van offertes in Sales.</span><span class="sxs-lookup"><span data-stu-id="4e818-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="4e818-112">Integratie van verkooporders met de Commerce-prijsengine is nog niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="4e818-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="4e818-113">Wanneer gebruikers een offerte in Sales starten, kopieert het raamwerk voor twee keer wegschrijven de offertegegevens naar Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e818-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="4e818-114">Eventuele wijzigingen in bestaande offerteregels of nieuw toegevoegde offerteregels in Sales worden naar Commerce gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="4e818-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="4e818-115">Wanneer gebruikers de Commerce-prijsengine willen gebruiken voor de prijscalculatie, kunnen zij **Prijsopgave** selecteren om de prijzen van de offerte bij te werken op basis van de Commerce-prijsengine.</span><span class="sxs-lookup"><span data-stu-id="4e818-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="4e818-116">Prijzen worden vervolgens automatisch bijgewerkt in Sales en Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e818-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4e818-117">Vereisten</span><span class="sxs-lookup"><span data-stu-id="4e818-117">Prerequisites</span></span>

- <span data-ttu-id="4e818-118">Voordat u de Commerce-prijsengine in Sales kunt gebruiken, moet u de stappen in [Prospect naar contant geld in twee keer wegschrijven](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/) volgen.</span><span class="sxs-lookup"><span data-stu-id="4e818-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="4e818-119">U moet evaluatie van handelsovereenkomst uitschakelen door de volgende stappen uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="4e818-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="4e818-120">Ga in uw Commerce-omgeving naar **Klanten \> Instellen \> Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="4e818-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="4e818-121">Schakel op het tabblad **Prijzen** op het sneltabblad **Evaluatie van handelsovereenkomst** het selectievakje **Handmatige invoer** uit.</span><span class="sxs-lookup"><span data-stu-id="4e818-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e818-122">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="4e818-122">Additional resources</span></span>

[<span data-ttu-id="4e818-123">Prospect naar contant geld in twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="4e818-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)
