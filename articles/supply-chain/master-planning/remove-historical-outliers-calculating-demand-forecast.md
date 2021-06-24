---
title: Verwijder uitschieters uit historische transactiegegevens bij het berekenen van een vraagprognose
description: In dit artikel wordt beschreven hoe u uitschieters kunt verwijderen uit de historische gegevens die worden gebruikt om een vraagprognose te berekenen. Door uitschieters uit te sluiten, kunt u de prognosenauwkeurigheid verbeteren.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df20a45707d3f6ff2ba963e3310194c1af830234
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187381"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="b3757-104">Verwijder uitschieters uit historische transactiegegevens bij het berekenen van een vraagprognose</span><span class="sxs-lookup"><span data-stu-id="b3757-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3757-105">In dit artikel wordt beschreven hoe u uitschieters kunt verwijderen uit de historische gegevens die worden gebruikt om een vraagprognose te berekenen.</span><span class="sxs-lookup"><span data-stu-id="b3757-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="b3757-106">Door uitschieters uit te sluiten, kunt u de prognosenauwkeurigheid verbeteren.</span><span class="sxs-lookup"><span data-stu-id="b3757-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="b3757-107">U kunt uitschieters uitsluiten om de prognosenauwkeurigheid te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="b3757-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="b3757-108">Deze taak is optioneel.</span><span class="sxs-lookup"><span data-stu-id="b3757-108">This is an optional task.</span></span> <span data-ttu-id="b3757-109">Hier is een overzicht van het proces:</span><span class="sxs-lookup"><span data-stu-id="b3757-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="b3757-110">Klik op **Hoofdplanning** &gt; **Instellen** &gt; **Vraagprognose** &gt; **Verwijdering van uitschieters** om de pagina **Verwijdering van uitschieters** te openen, waar u een query kunt gebruiken om de uit te sluiten transacties te selecteren.</span><span class="sxs-lookup"><span data-stu-id="b3757-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="b3757-111">Selecteer het bedrijf waarop de query van toepassing is en geef een naam en een omschrijving op.</span><span class="sxs-lookup"><span data-stu-id="b3757-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="b3757-112">Het veld **Querydatum** wordt automatisch ingesteld op de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="b3757-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="b3757-113">Schakel het selectievakje **Actief** in om de transacties die door de query worden gevonden uit de historische gegevens te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b3757-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="b3757-114">Deze instelling is van kracht wanneer u een basislijnprognose maakt.</span><span class="sxs-lookup"><span data-stu-id="b3757-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="b3757-115">Op de pagina **Query voor verwijdering van uitschieters** kunt u de criteria toevoegen, verwijderen en selecteren waarmee de transacties worden gedefinieerd die moeten worden uitgesloten wanneer de basislijnprognose wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="b3757-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="b3757-116">Selecteer bijvoorbeeld een bepaald artikel of een ordertransactie die u wilt uitsluiten.</span><span class="sxs-lookup"><span data-stu-id="b3757-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="b3757-117">Klik op **Transacties weergeven**.</span><span class="sxs-lookup"><span data-stu-id="b3757-117">Click **Display transactions**.</span></span> <span data-ttu-id="b3757-118">Op de pagina **Transacties met uitschieters** worden de transacties weergegeven die voldoen aan de criteria die u in de query hebt gedefinieerd en die van de historische gegevens worden uitgesloten wanneer de vraagprognose wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="b3757-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="b3757-119">**Opmerking:** u kunt ook een query maken die op een bestaande query is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="b3757-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="b3757-120">Selecteer de query die u wilt kopiëren en klik op **Dupliceren**.</span><span class="sxs-lookup"><span data-stu-id="b3757-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="b3757-121">Het veld **Querydatum** bevat de versie.</span><span class="sxs-lookup"><span data-stu-id="b3757-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="b3757-122">U kunt de query zo gebruiken of klikken op **Query bewerken** om de criteria te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b3757-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="b3757-123">U kunt de naam en omschrijving van de nieuwe query desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b3757-123">You can optionally modify the name and description of the new query.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3757-124">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b3757-124">Additional resources</span></span>

[<span data-ttu-id="b3757-125">Overzicht van Vraagprognose</span><span class="sxs-lookup"><span data-stu-id="b3757-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="b3757-126">Prognosenauwkeurigheid controleren</span><span class="sxs-lookup"><span data-stu-id="b3757-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]