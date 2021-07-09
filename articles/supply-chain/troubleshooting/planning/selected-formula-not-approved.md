---
title: Geselecteerd formulenummer is niet goedgekeurd voor een batchorder
description: Wanneer u een geplande order wilt fiatteren, wordt er een foutbericht weergegeven waarin staat dat het geselecteerde formulenummer niet is goedgekeurd voor een batchorder.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294043"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="00d51-103">Geselecteerd formulenummer is niet goedgekeurd voor een batchorder</span><span class="sxs-lookup"><span data-stu-id="00d51-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="00d51-104">Foutcode: PRO2614</span><span class="sxs-lookup"><span data-stu-id="00d51-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="00d51-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="00d51-105">Symptoms</span></span>

<span data-ttu-id="00d51-106">Wanneer u een geplande order probeert te fiatteren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="00d51-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="00d51-107">Het geselecteerde formulenummer is niet goedgekeurd voor een batchorder.</span><span class="sxs-lookup"><span data-stu-id="00d51-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="00d51-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="00d51-108">Cause</span></span>

<span data-ttu-id="00d51-109">Het systeem valideert de goedkeuringsbewerking om ervoor te zorgen dat er een goedgekeurde formule beschikbaar is voor het actieve artikel.</span><span class="sxs-lookup"><span data-stu-id="00d51-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="00d51-110">U moet de formule waarschijnlijk goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="00d51-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="00d51-111">Oplossing</span><span class="sxs-lookup"><span data-stu-id="00d51-111">Resolution</span></span>

<span data-ttu-id="00d51-112">Voer de volgende stappen uit om een formule goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="00d51-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="00d51-113">Ga naar **Productgegevensbeheer \> Stuklijsten en formules \> Formules**.</span><span class="sxs-lookup"><span data-stu-id="00d51-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="00d51-114">Selecteer de betreffende formule.</span><span class="sxs-lookup"><span data-stu-id="00d51-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="00d51-115">Selecteer in het actievenster op het tabblad **Formule** in de groep **Onderhouden** de optie **Formule goedkeuren**.</span><span class="sxs-lookup"><span data-stu-id="00d51-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="00d51-116">Selecteer een fiatteur in het dialoogvenster **Stuklijst of formule goedkeuren** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="00d51-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
