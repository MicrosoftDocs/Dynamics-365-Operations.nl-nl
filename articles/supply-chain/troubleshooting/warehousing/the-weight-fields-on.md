---
title: De gewichtsvelden op ladingregels komen niet overeen met de gewichtsvelden op de lading
description: De gewichtsvelden op ladingregels komen niet overeen met de gewichtsvelden op de lading
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924346"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="a81b8-103">De gewichtsvelden op ladingregels komen niet overeen met de gewichtsvelden op de lading</span><span class="sxs-lookup"><span data-stu-id="a81b8-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="a81b8-104">Foutcodes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="a81b8-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="a81b8-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="a81b8-105">Symptoms</span></span>

<span data-ttu-id="a81b8-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="a81b8-106">The system shows the following error message:</span></span>

> <span data-ttu-id="a81b8-107">De gewichtsvelden op ladingregels komen niet overeen met de gewichtsvelden op de lading %1.</span><span class="sxs-lookup"><span data-stu-id="a81b8-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="a81b8-108">Voer de Consistentiecontrole capaciteit magazijn uit om de gewichtsvelden opnieuw te berekenen.</span><span class="sxs-lookup"><span data-stu-id="a81b8-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="a81b8-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="a81b8-109">Cause</span></span>

<span data-ttu-id="a81b8-110">De velden **Nettogewicht** en **Tarragewicht** worden op de ladingregel ingesteld op *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="a81b8-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="a81b8-111">De gewichtsvelden zijn echter niet ingesteld op *0* voor de gewichtsmaten op het product.</span><span class="sxs-lookup"><span data-stu-id="a81b8-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="a81b8-112">Wanneer er geen gewichtsvelden op de ladingregel zijn ingesteld, kunnen correcties van de hoeveelheid op de ladingregel leiden tot een onjuiste gewichtsberekening van de lading.</span><span class="sxs-lookup"><span data-stu-id="a81b8-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="a81b8-113">Dit probleem kan optreden als het gewicht van het product is gewijzigd nadat de ladingregel werd gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a81b8-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="a81b8-114">Oplossing</span><span class="sxs-lookup"><span data-stu-id="a81b8-114">Resolution</span></span>

<span data-ttu-id="a81b8-115">Wanneer u een ladingregel maakt, worden de gewichtsvelden van het product standaard ingevuld.</span><span class="sxs-lookup"><span data-stu-id="a81b8-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="a81b8-116">Als het gewicht nul is, kunt u deze opnieuw berekenen met behulp van de functionaliteit *Consistentiecontrole capaciteit magazijn*.</span><span class="sxs-lookup"><span data-stu-id="a81b8-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="a81b8-117">Ga naar **Systeembeheer \> Periodieke taken \> Database \> Consistentiecontrole**.</span><span class="sxs-lookup"><span data-stu-id="a81b8-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="a81b8-118">In het dialoogvenser **Consistentiecontrole**, stelt u het veld **Module** in op *Magazijnbeheer*.</span><span class="sxs-lookup"><span data-stu-id="a81b8-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="a81b8-119">Stel het veld **Controleren/corrigeren** in op *Fout oplossen*.</span><span class="sxs-lookup"><span data-stu-id="a81b8-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="a81b8-120">Schakel in de lijst met selectievakjes het selectievakje **Consistentiecontrole capaciteit magazijn** in en zorg ervoor dat alleen de rij voor dit selectievakje is gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="a81b8-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="a81b8-121">Selecteer de knop met het weglatingsteken (**...**) boven aan de lijst met selectievakjes en selecteer vervolgens **Dialoog** in het menu.</span><span class="sxs-lookup"><span data-stu-id="a81b8-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="a81b8-122">In het dialoogvenster **Consistentiecontrole capaciteit magazijn** stelt u de volgende velden in om de criteria van de consistentiecontrole op te geven:</span><span class="sxs-lookup"><span data-stu-id="a81b8-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="a81b8-123">**Lading-id:** Geef een lading-id op.</span><span class="sxs-lookup"><span data-stu-id="a81b8-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="a81b8-124">Laat dit leeg als u alle lading-id's wilt controleren.</span><span class="sxs-lookup"><span data-stu-id="a81b8-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="a81b8-125">**Artikelnummer:** Geef een artikelnummer op.</span><span class="sxs-lookup"><span data-stu-id="a81b8-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="a81b8-126">Laat dit leeg als u alle artikelen wilt controleren.</span><span class="sxs-lookup"><span data-stu-id="a81b8-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="a81b8-127">**Altijd opnieuw berekenen van gewicht voor ladingen:** Zet deze optie op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="a81b8-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="a81b8-128">**Overschrijven van gewicht op ladingregels toestaan:** Zet deze optie op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="a81b8-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="a81b8-129">Selecteer **OK** om het dialoogvenster **Consistentiecontrole capaciteit magazijn** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="a81b8-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="a81b8-130">Selecteer de knop met het weglatingsteken en selecteer vervolgens **Uitvoeren** in het menu.</span><span class="sxs-lookup"><span data-stu-id="a81b8-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="a81b8-131">Het gewicht wordt opnieuw berekend op basis van de criteria die u hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="a81b8-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="a81b8-132">Selecteer de koppeling **Berichtdetails** als u het resultaat van de consistentiecontrole wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="a81b8-132">Select the **Message details** link to view the result of the consistency check.</span></span>
