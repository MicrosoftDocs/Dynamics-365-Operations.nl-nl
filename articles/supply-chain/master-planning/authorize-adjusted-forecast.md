---
title: Een gecorrigeerde prognose autoriseren
description: Niet alle prognosegegevens moeten onmiddellijk worden geautoriseerd. In dit artikel wordt uitgelegd hoe u de periode kunt opgeven waarvoor een prognose is geautoriseerd. Het legt ook uit hoe u de prognose voor specifieke bedrijven en prognosemodellen kunt autoriseren.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ab8558f25f5ffd3b7eb3e1bc5680b1a1f8d5139
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961426"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="1a190-105">Een gecorrigeerde prognose autoriseren</span><span class="sxs-lookup"><span data-stu-id="1a190-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a190-106">Niet alle prognosegegevens moeten onmiddellijk worden geautoriseerd.</span><span class="sxs-lookup"><span data-stu-id="1a190-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="1a190-107">In dit artikel wordt uitgelegd hoe u de periode kunt opgeven waarvoor een prognose is geautoriseerd.</span><span class="sxs-lookup"><span data-stu-id="1a190-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="1a190-108">Het legt ook uit hoe u de prognose voor specifieke bedrijven en prognosemodellen kunt autoriseren.</span><span class="sxs-lookup"><span data-stu-id="1a190-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="1a190-109">Niet alle prognosegegevens moeten onmiddellijk worden geautoriseerd.</span><span class="sxs-lookup"><span data-stu-id="1a190-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="1a190-110">U kunt de begin- en einddatums van de periode opgeven waarvoor de prognose wordt geautoriseerd.</span><span class="sxs-lookup"><span data-stu-id="1a190-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="1a190-111">Met deze functie kunt u specifieke buckets blokkeren.</span><span class="sxs-lookup"><span data-stu-id="1a190-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="1a190-112">De begin- en einddatums die u opgeeft, moeten overeenkomen met de begin- en einddatums van de verzameling waarin de prognose is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1a190-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="1a190-113">Deze beperking wordt afgedwongen en de datums worden automatisch aangepast als een correctie nodig is.</span><span class="sxs-lookup"><span data-stu-id="1a190-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="1a190-114">Op het **Details** tabblad van de **Autorisatie** pagina, kunt u details bekijken over de prognose die zonet is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1a190-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="1a190-115">U kunt de bedrijven en prognosemodellen selecteren om de prognose te autoriseren voor gebruik.</span><span class="sxs-lookup"><span data-stu-id="1a190-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="1a190-116">Standaard bevat het raster alle bedrijven waarvoor vraagprognose is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1a190-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="1a190-117">Voor elk bedrijf, wordt het prognosemodel dat correspondeert met het huidige prognoseplan dat wordt ingesteld in de parameters van de hoofdplanning, vooraf ingevuld.</span><span class="sxs-lookup"><span data-stu-id="1a190-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="1a190-118">U kunt dit prognosemodel echter in elk prognosemodel wijzigen dat tot dat bedrijf behoort.</span><span class="sxs-lookup"><span data-stu-id="1a190-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="1a190-119">Als geen prognosegegevens zijn gegenereerd voor een geselecteerd bedrijf, ontvangt u een waarschuwing tijdens importeren.</span><span class="sxs-lookup"><span data-stu-id="1a190-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="1a190-120">Het is zeer belangrijk dat u begrijpt hoe het selectievakje **De handmatige correcties opslaan die in de basislijnvraagprognose zijn gemaakt** werkt.</span><span class="sxs-lookup"><span data-stu-id="1a190-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="1a190-121">Als u handmatige aanpassingen hebt aangebracht in de statistische basislijnprognose, worden de aangepaste waarden geautoriseerd voor gebruik, zelfs als dit selectievakje is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1a190-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="1a190-122">De wijzigingen worden echter verwijderd na de autorisatie.</span><span class="sxs-lookup"><span data-stu-id="1a190-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="1a190-123">Daarom is die prognose, de volgende keer dat een prognose wordt gegenereerd, alleen een statistische prognose zonder handmatig overschreven waarden, zelfs als **Handmatige correcties overbrengen naar de vraagprognose** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1a190-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="1a190-124">Daarom kunt u het selectievakje **De handmatige correcties opslaan die in de basislijnvraagprognose zijn gemaakt** als mechanisme beschouwen voor het behouden of verwijderen van alle handmatige wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="1a190-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1a190-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1a190-125">Additional resources</span></span>
--------

[<span data-ttu-id="1a190-126">Handmatige correcties aanbrengen in de basislijnprognose</span><span class="sxs-lookup"><span data-stu-id="1a190-126">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="1a190-127">Prognosenauwkeurigheid controleren</span><span class="sxs-lookup"><span data-stu-id="1a190-127">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



