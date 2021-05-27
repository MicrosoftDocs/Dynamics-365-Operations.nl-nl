---
title: Tijdens de hoofdplanning worden geplande orders voor phantom-producten gegenereerd
description: Geplande orders worden gegenereerd voor phantom-producten nadat de hoofdplanning is uitgevoerd.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026412"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="0bd1c-103">Tijdens de hoofdplanning worden geplande orders voor phantom-producten gegenereerd</span><span class="sxs-lookup"><span data-stu-id="0bd1c-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="0bd1c-104">KB-nummer: 4614729</span><span class="sxs-lookup"><span data-stu-id="0bd1c-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="0bd1c-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="0bd1c-105">Symptoms</span></span>

<span data-ttu-id="0bd1c-106">Geplande orders worden gegenereerd voor phantom-producten nadat de hoofdplanning is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0bd1c-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="0bd1c-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="0bd1c-107">Resolution</span></span>

<span data-ttu-id="0bd1c-108">De instelling van de optie **Phantom** voor vrijgegeven producten bepaalt het standaardregeltype op de stuklijst.</span><span class="sxs-lookup"><span data-stu-id="0bd1c-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="0bd1c-109">Wanneer de optie **Phantom** is ingesteld op *Ja*, worden er nog steeds geplande orders gemaakt voor het artikel, maar de optie **Rechtstreeks afgeleide behoefte** voor elke geplande order wordt ingesteld op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="0bd1c-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="0bd1c-110">De geplande productieorder kan daarom niet alleen worden gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="0bd1c-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="0bd1c-111">In plaats daarvan wordt deze altijd automatisch opgenomen wanneer de bovenliggende productieorder wordt gefiatteerd.</span><span class="sxs-lookup"><span data-stu-id="0bd1c-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="0bd1c-112">Daarnaast worden de stuklijstregels van de geplande phantom-order opgenomen in de stuklijst van de bovenliggende productieorder.</span><span class="sxs-lookup"><span data-stu-id="0bd1c-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
