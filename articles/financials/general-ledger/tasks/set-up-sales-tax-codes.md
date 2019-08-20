---
title: Btw-codes instellen
description: In dit onderwerp wordt uitgelegd hoe u btw-codes instelt in Dynamics 365 for Finance and Operations.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419c6b569093d717158e80bd9bc01054d82bff9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834825"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="2f1a9-103">Btw-codes instellen</span><span class="sxs-lookup"><span data-stu-id="2f1a9-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f1a9-104">In dit onderwerp wordt uitgelegd hoe u btw-codes instelt in Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-104">This topic explains how to set up sales tax codes in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="2f1a9-105">Btw-codes worden gemaakt voor elke indirecte belasting of heffing die de rechtspersoon moet doorberekenen, innen en afdragen aan belastingdiensten.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="2f1a9-106">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2f1a9-107">Ga naar **Navigatievenster > Belasting > Indirecte belastingen > Btw > Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="2f1a9-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-108">Select **New**.</span></span>
3. <span data-ttu-id="2f1a9-109">Typ een waarde in het veld **Btw-code**.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="2f1a9-110">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="2f1a9-111">Selecteer een **Vereffeningsperiode** door de vervolgkeuzelijst te openen, om op te geven welke btw-dienst en met welke intervallen deze btw moet worden aangegeven en betaald.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="2f1a9-112">Selecteer een **Grootboekboekingsgroep** om de hoofdrekeningen op te geven om btw naar het grootboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="2f1a9-113">Vouw het sneltabblad **Berekening** uit.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="2f1a9-114">Het sneltabblad bevat meerdere velden die bepalen hoe de btw-bedragen worden berekend.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="2f1a9-115">Vul deze velden naar wens in.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="2f1a9-116">Selecteer in het **actievenster**, bovenaan de interface, de optie **Btw-code**.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="2f1a9-117">Selecteer **Waarden**.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-117">Select **Values**.</span></span>
10. <span data-ttu-id="2f1a9-118">Voer de waarde voor deze btw-code in de kolom **Waarde** in.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="2f1a9-119">Als op het sneltabblad **Berekening** Bedrag per eenheid is geselecteerd, wordt in het veld Oorsprong de waarde vermenigvuldigd met de hoeveelheid op de transactie om het btw-bedrag te berekenen.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="2f1a9-120">Als de btw-code geen eenheidgebaseerde belasting is, is de waarde een percentage dat wordt toegepast op de oorsprong voor deze btw-code om het btw-bedrag te berekenen.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="2f1a9-121">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-121">Select **Save**.</span></span>
12. <span data-ttu-id="2f1a9-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-122">Close the page.</span></span>
13. <span data-ttu-id="2f1a9-123">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="2f1a9-123">Select **Save**.</span></span>

