---
title: Vertraagde belastingberekening inschakelen in journaal
description: In dit onderwerp wordt uitgelegd hoe u de functie **Vertraagde belastingberekening inschakelen in journaal** gebruikt om de belastingberekening te verbeteren bij een groot volume van journaalregels.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177123"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="c03ca-103">Vertraagde belastingberekening inschakelen in journaal</span><span class="sxs-lookup"><span data-stu-id="c03ca-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c03ca-104">In dit onderwerp wordt uitgelegd hoe u de functie **Vertraagde belastingberekening inschakelen in journaal** gebruikt om de belastingberekening te verbeteren bij een groot volume van journaalregels.</span><span class="sxs-lookup"><span data-stu-id="c03ca-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="c03ca-105">Het huidige gedrag van btw-berekening in journaal wordt tijdens real-time geactiveerd wanneer de gebruiker btw-gerelateerde velden bijwerkt, bijvoorbeeld btw-groep/btw-groep van artikel.</span><span class="sxs-lookup"><span data-stu-id="c03ca-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="c03ca-106">Bij een update op journaalregelniveau wordt het btw-bedrag op alle journaalregels opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="c03ca-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="c03ca-107">Het helpt de gebruiker om het real-time berekende belastingbedrag te zien, maar dit kan ook tot prestatieproblemen leiden bij een groot aantal journaalregels.</span><span class="sxs-lookup"><span data-stu-id="c03ca-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="c03ca-108">Deze functie biedt een optie om de belastingberekening te vertragen om de prestatieproblemen op te lossen.</span><span class="sxs-lookup"><span data-stu-id="c03ca-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="c03ca-109">Als deze functie is ingeschakeld, wordt het btw-bedrag alleen berekend wanneer de gebruiker op de opdracht "Btw" klikt of het journaal boekt.</span><span class="sxs-lookup"><span data-stu-id="c03ca-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="c03ca-110">Gebruiker kan de parameter op drie niveaus in- of uitschakelen:</span><span class="sxs-lookup"><span data-stu-id="c03ca-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="c03ca-111">Per rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="c03ca-111">By legal entity</span></span>
- <span data-ttu-id="c03ca-112">Per journaalnaam</span><span class="sxs-lookup"><span data-stu-id="c03ca-112">By journal name</span></span>
- <span data-ttu-id="c03ca-113">Per journaalkoptekst</span><span class="sxs-lookup"><span data-stu-id="c03ca-113">By journal header</span></span>

<span data-ttu-id="c03ca-114">Het systeem zal de parameterwaarde in de journaalkoptekst opnemen als definitief.</span><span class="sxs-lookup"><span data-stu-id="c03ca-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="c03ca-115">De parameterwaarde op de journaalkoptekst wordt standaard opgehaald uit de journaalnaam.</span><span class="sxs-lookup"><span data-stu-id="c03ca-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="c03ca-116">De parameterwaarde in de journaalnaam wordt standaard opgehaald uit de grootboekparameter wanneer de journaalnaam wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c03ca-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="c03ca-117">De velden "Werkelijk btw-bedrag" en "Berekend btw-bedrag" in het journaal worden verborgen als deze parameter wordt ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c03ca-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="c03ca-118">Dit is om de gebruiker niet in verwarring te brengen, omdat de waarde van deze twee velden altijd 0 aangeeft voordat de belastingberekening door de gebruiker wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="c03ca-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="c03ca-119">Berekening van vertraagde btw per rechtspersoon inschakelen</span><span class="sxs-lookup"><span data-stu-id="c03ca-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="c03ca-120">Ga naar **Grootboek > Grootboek instellen > Grootboekparameters**</span><span class="sxs-lookup"><span data-stu-id="c03ca-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="c03ca-121">Klik op het tabblad **Btw**</span><span class="sxs-lookup"><span data-stu-id="c03ca-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="c03ca-122">Zoek op het sneltabblad **Algemeen** de parameter **Vertraagde belastingberekening** en schakel deze in/uit</span><span class="sxs-lookup"><span data-stu-id="c03ca-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="c03ca-123">Vertraagde belastingberekening inschakelen per journaalnaam</span><span class="sxs-lookup"><span data-stu-id="c03ca-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="c03ca-124">Ga naar **Grootboek > Journaalinstellingen > Journaalnamen**</span><span class="sxs-lookup"><span data-stu-id="c03ca-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="c03ca-125">Zoek op het sneltabblad **Algemeen** de parameter **Vertraagde belastingberekening** en schakel deze in/uit</span><span class="sxs-lookup"><span data-stu-id="c03ca-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="c03ca-126">Vertraagde belastingberekening inschakelen per journaal</span><span class="sxs-lookup"><span data-stu-id="c03ca-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="c03ca-127">Ga naar **Grootboek > Journaalboekingen > Algemene journalen**</span><span class="sxs-lookup"><span data-stu-id="c03ca-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="c03ca-128">Klik op **Nieuw**</span><span class="sxs-lookup"><span data-stu-id="c03ca-128">Click **New**</span></span>
3. <span data-ttu-id="c03ca-129">Selecteer een journaalnaam</span><span class="sxs-lookup"><span data-stu-id="c03ca-129">Select a journal name</span></span>
4. <span data-ttu-id="c03ca-130">Klik op **Instellen**</span><span class="sxs-lookup"><span data-stu-id="c03ca-130">Click **Setup**</span></span>
5. <span data-ttu-id="c03ca-131">Zoek de parameter **Vertraagde belastingberekening** en schakel deze in/uit</span><span class="sxs-lookup"><span data-stu-id="c03ca-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
