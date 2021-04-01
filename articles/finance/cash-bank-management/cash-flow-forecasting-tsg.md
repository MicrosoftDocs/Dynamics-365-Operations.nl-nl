---
title: Problemen met het instellen van cashflowprognoses oplossen
description: Dit onderwerp bevat beantwoorden op vragen die u kunt hebben wanneer u cashflowprognoses configureert. Hierin komen veelgestelde vragen (FAQ) over de opzet voor cashflow, updates van cashflow en cashflow Power BI aan de orde.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232484"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="9c5a6-104">Problemen met het instellen van cashflowprognoses oplossen</span><span class="sxs-lookup"><span data-stu-id="9c5a6-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c5a6-105">Dit onderwerp bevat beantwoorden op vragen die u kunt hebben wanneer u cashflowprognoses configureert.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="9c5a6-106">Hierin komen veelgestelde vragen (FAQ) over de opzet voor cashflow, updates van cashflow en cashflow Power BI aan de orde.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="9c5a6-107">Waarom wordt de cashflow voor slechts één rechtspersoon weergegeven?</span><span class="sxs-lookup"><span data-stu-id="9c5a6-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="9c5a6-108">Cashflowprognoses worden geconfigureerd en berekend per rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="9c5a6-109">Power BI-rapporten en de cashflowprognosemogelijkheden in Finance Insights geven de resultaten weer.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="9c5a6-110">Cashflowprognoses moeten worden ingesteld voor elke rechtspersoon voor wie u een prognose wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="9c5a6-111">Controleer de configuratie van cashflowprognoses in al uw rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="9c5a6-112">U kunt ook de configuratie van alle rechtspersonen voor cashflowprognose controleren en controleren of deze zijn ingesteld zoals u bedoeld hebt.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="9c5a6-113">Waarom worden in Power BI niet alle cashflowgegevens weergegeven?</span><span class="sxs-lookup"><span data-stu-id="9c5a6-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="9c5a6-114">Er moeten verschillende stappen worden uitgevoerd voordat cashflowprognoses in Power BI-weergaven kunnen verschijnen.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="9c5a6-115">Loop de volgende controlelijst na en controleer of elke stap is voltooid:</span><span class="sxs-lookup"><span data-stu-id="9c5a6-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="9c5a6-116">Stel de cashflow in voor elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="9c5a6-117">In grootboekparameters stelt u de systeemvaluta en het systeemwisselkoerstype in.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="9c5a6-118">De valuta voor boekhouding van het grootboek en het wisselkoerstype instellen.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="9c5a6-119">Voer wisselkoersen in tussen de transactievaluta en de valuta voor de boekhouding.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="9c5a6-120">Voer wisselkoersen in tussen de valuta voor de boekhouding en de systeemvaluta.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="9c5a6-121">Voer wisselkoersen in tussen de valuta voor de boekhouding en elke bankvaluta.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="9c5a6-122">Waarom werkt cashflow Power BI in vorige versies, maar is nu leeg?</span><span class="sxs-lookup"><span data-stu-id="9c5a6-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="9c5a6-123">Controleer of de metingen 'Cashflowmeting V2' en 'LedgerCovLiquidityMeasurement' van Entiteitopslag zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="9c5a6-124">Zie [Power BI-integratie met Entiteitopslag](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) voor more informatie over hoe u kunt werken met Entiteitopslag. Controleer of alle vereiste stappen voor het weergeven van Power BI-inhoud zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="9c5a6-125">Zie [Power BI-inhoud Overzicht van contant geld](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="9c5a6-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="9c5a6-126">Zijn de entiteiten van de Entiteitopslag vernieuwd?</span><span class="sxs-lookup"><span data-stu-id="9c5a6-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="9c5a6-127">U moet uw entiteiten periodiek vernieuwen om er zeker van te zijn dat de gegevens actueel en nauwkeurig zijn.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="9c5a6-128">Als u een specifieke entiteit handmatig wilt vernieuwen, gaat u naar **Systeembeheer \> Setup \> Entiteitopslag**, selecteert u de entiteit en u vervolgens **Vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="9c5a6-129">De gegevens kunnen ook automatisch worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-129">The data can also be updated automatically.</span></span> <span data-ttu-id="9c5a6-130">Stel op de pagina **Entiteitopslag** de optie **Automatisch vernieuwen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9c5a6-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]