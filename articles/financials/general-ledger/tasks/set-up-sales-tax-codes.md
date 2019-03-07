---
title: Btw-codes instellen
description: Btw-codes worden gemaakt voor elke indirecte belasting of heffing die de rechtspersoon moet doorberekenen, innen en afdragen aan belastingdiensten.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "349165"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="50e86-103">Btw-codes instellen</span><span class="sxs-lookup"><span data-stu-id="50e86-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50e86-104">Btw-codes worden gemaakt voor elke indirecte belasting of heffing die de rechtspersoon moet doorberekenen, innen en afdragen aan belastingdiensten.</span><span class="sxs-lookup"><span data-stu-id="50e86-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="50e86-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="50e86-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="50e86-106">Ga naar Btw > Indirecte belastingen > Btw > Btw-codes.</span><span class="sxs-lookup"><span data-stu-id="50e86-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="50e86-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="50e86-107">Click New.</span></span>
3. <span data-ttu-id="50e86-108">Typ een waarde in het veld Btw-code.</span><span class="sxs-lookup"><span data-stu-id="50e86-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="50e86-109">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="50e86-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="50e86-110">Selecteer een vereffeningsperiode om op te geven welke btw-dienst en in welke intervallen deze btw moet worden aangegeven en betaald.</span><span class="sxs-lookup"><span data-stu-id="50e86-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="50e86-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="50e86-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="50e86-112">Selecteer een grootboekboekingsgroep om de hoofdrekeningen op te geven om btw naar het grootboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="50e86-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="50e86-113">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="50e86-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="50e86-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="50e86-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="50e86-115">Vouw het sneltabblad Berekening uit.</span><span class="sxs-lookup"><span data-stu-id="50e86-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="50e86-116">Het sneltabblad Berekening heeft meerdere velden die bepalen hoe de btw-bedragen worden berekend.</span><span class="sxs-lookup"><span data-stu-id="50e86-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="50e86-117">Klik in het actievenster op Btw-code.</span><span class="sxs-lookup"><span data-stu-id="50e86-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="50e86-118">Klik op Waarden.</span><span class="sxs-lookup"><span data-stu-id="50e86-118">Click Values.</span></span>
13. <span data-ttu-id="50e86-119">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="50e86-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="50e86-120">Voer de waarde voor deze btw-code in.</span><span class="sxs-lookup"><span data-stu-id="50e86-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="50e86-121">Op het sneltabblad Berekening wordt in het veld Oorsprong, als Bedrag per eenheid is geselecteerd, de waarde vermenigvuldigd met de hoeveelheid op de transactie om het btw-bedrag te berekenen.</span><span class="sxs-lookup"><span data-stu-id="50e86-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="50e86-122">Als de btw-code geen eenheidgebaseerde belasting is, is de waarde een percentage dat wordt toegepast op de oorsprong voor deze btw-code om het btw-bedrag te berekenen.</span><span class="sxs-lookup"><span data-stu-id="50e86-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="50e86-123">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="50e86-123">Click Save.</span></span>
16. <span data-ttu-id="50e86-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="50e86-124">Close the page.</span></span>
17. <span data-ttu-id="50e86-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="50e86-125">Click Save.</span></span>

