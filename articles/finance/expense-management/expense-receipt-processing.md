---
title: Verwerking van onkostenkwitanties
description: Dit onderwerp biedt informatie over de verwerking van optische tekenherkenning (OCR) voor kwitanties. Deze functie is bedoeld om de gebruikerservaring te verbeteren bij het maken van onkostennota's in Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378226"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="64d0b-104">Verwerking van onkostenkwitanties</span><span class="sxs-lookup"><span data-stu-id="64d0b-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64d0b-105">Onkosteninvoer is verbeterd via de introductie van de OCR-verwerking (Optical Character Recognition) voor kwitanties.</span><span class="sxs-lookup"><span data-stu-id="64d0b-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="64d0b-106">Deze functie is bedoeld om de gebruikerservaring te verbeteren bij het maken van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="64d0b-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="64d0b-107">Belangrijke functies</span><span class="sxs-lookup"><span data-stu-id="64d0b-107">Key features</span></span>

- <span data-ttu-id="64d0b-108">De handelaarsnaam, de datum en het totaalbedrag worden opgehaald uit ontvangsten.</span><span class="sxs-lookup"><span data-stu-id="64d0b-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="64d0b-109">De functie probeert niet-gekoppelde kwitanties te koppelen aan niet-gekoppelde onkostentransacties.</span><span class="sxs-lookup"><span data-stu-id="64d0b-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="64d0b-110">Gebruikers kunnen handmatig ingevoerde onkostentransacties maken vanuit kwitanties.</span><span class="sxs-lookup"><span data-stu-id="64d0b-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="64d0b-111">Voorbeelden van gebruik</span><span class="sxs-lookup"><span data-stu-id="64d0b-111">Usage examples</span></span>

<span data-ttu-id="64d0b-112">Ga als volgt te werk om automatisch kwitanties te koppelen waarin creditcardtransacties zijn opgenomen wanneer een onkostennota wordt gemaakt:</span><span class="sxs-lookup"><span data-stu-id="64d0b-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="64d0b-113">Open het werkgebied **Onkostenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="64d0b-114">Controleer op het tabblad **Ontvangstbewijzen** of er niet-gekoppelde ontvangstbewijzen zijn.</span><span class="sxs-lookup"><span data-stu-id="64d0b-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="64d0b-115">U kunt ook ontvangstbewijzen uploaden op het tabblad **Ontvangstbewijzen**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="64d0b-116">Controleer op het tabblad **Onkosten** of er niet-gekoppelde onkosten zijn.</span><span class="sxs-lookup"><span data-stu-id="64d0b-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="64d0b-117">De onkostenbeheerder importeert deze onkosten meestal van de creditcardprovider.</span><span class="sxs-lookup"><span data-stu-id="64d0b-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="64d0b-118">Selecteer **Nieuwe onkostennota**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-118">Select **New expense report**.</span></span> <span data-ttu-id="64d0b-119">Zoals u ziet, kunt u onkosten en ontvangsten nu ook opnemen wanneer u een onkostennota maakt.</span><span class="sxs-lookup"><span data-stu-id="64d0b-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="64d0b-120">Als u zowel onkosten als ontvangsten toevoegt, wordt automatisch afstemmen van ontvangstbewijzen op onkosten geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="64d0b-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="64d0b-121">Ga als volgt te werk om onkosten te maken of af te stemmen op een ontvangstbewijs:</span><span class="sxs-lookup"><span data-stu-id="64d0b-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="64d0b-122">Voeg op het tabblad **Ontvangstbewijzen** van een onkostennota een ontvangstbewijs toe door **Ontvangstbewijzen toevoegen** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="64d0b-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="64d0b-123">Onder de geüploade kopie van het ontvangstbewijs ziet u de opties **Maken** en **Afstemmen**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="64d0b-124">Selecteer **Maken** om een handmatig ingevoerde onkostentransactie te maken en vul de waarden in die worden opgehaald uit het ontvangstbewijs.</span><span class="sxs-lookup"><span data-stu-id="64d0b-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="64d0b-125">Als u **Afstemmen** selecteert, probeert het systeem de bestaande onkosten te koppelen aan het ontvangstbewijs.</span><span class="sxs-lookup"><span data-stu-id="64d0b-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="64d0b-126">Installatie</span><span class="sxs-lookup"><span data-stu-id="64d0b-126">Installation</span></span>

<span data-ttu-id="64d0b-127">Deze functie werkt in combinatie met de functie **Nieuwe invulling voor het begrip onkostennota's** om de onkostenervaring te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="64d0b-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="64d0b-128">Deze functie is alleen beschikbaar voor Tier 2-omgevingen (Sandbox en Productie).</span><span class="sxs-lookup"><span data-stu-id="64d0b-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="64d0b-129">Als u deze geavanceerde onkostenmogelijkheden wilt gebruiken, installeert u de invoegtoepassing Service voor onkostenbeheer voor Microsoft Dynamics 365 Finance en schakelt u de functies in uw instantie in.</span><span class="sxs-lookup"><span data-stu-id="64d0b-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="64d0b-130">U kunt de invoegtoepassing vanuit uw project openen in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="64d0b-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="64d0b-131">Meld u aan bij LCS en open de gewenste omgeving.</span><span class="sxs-lookup"><span data-stu-id="64d0b-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="64d0b-132">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="64d0b-133">Selecteer **Onderhouden** of ga omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="64d0b-134">Selecteer **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="64d0b-135">Selecteer **Service voor onkostenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="64d0b-136">Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.</span><span class="sxs-lookup"><span data-stu-id="64d0b-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="64d0b-137">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="64d0b-137">Select **Install**.</span></span>

<span data-ttu-id="64d0b-138">Schakel in het werkgebied **Functiebeheer** de volgende functies in:</span><span class="sxs-lookup"><span data-stu-id="64d0b-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="64d0b-139">Nieuwe invulling voor het begrip onkostennota's</span><span class="sxs-lookup"><span data-stu-id="64d0b-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="64d0b-140">Automatisch afstemmen en onkosten maken op basis van ontvangst</span><span class="sxs-lookup"><span data-stu-id="64d0b-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="64d0b-141">Wanneer u deze functies inschakelt, worden de volgende acties uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="64d0b-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="64d0b-142">Het bestaande werkgebied **Onkostenbeheer** wordt vervangen door het nieuwe werkgebied.</span><span class="sxs-lookup"><span data-stu-id="64d0b-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="64d0b-143">Er is een nieuwe menuopdracht voor zichtbaarheid van onkostenvelden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="64d0b-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="64d0b-144">U kunt de vorige pagina **Onkostennota's** nog steeds openen door naar **Onkostenbeheer > Mijn onkosten > Onkostennota's** te gaan.</span><span class="sxs-lookup"><span data-stu-id="64d0b-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="64d0b-145">Met workflows en eventuele goedkeuringen gaat u nog steeds naar de bestaande pagina voor onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="64d0b-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="64d0b-146">Ontvangstbewijzen worden verwerkt via Microsoft Azure Cognitive Services en metagegevens worden opgehaald en toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="64d0b-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="64d0b-147">Er wordt een optie toegevoegd waarmee u een onkostennota kunt maken die overeenkomende niet-gekoppelde ontvangstbewijzen bevat.</span><span class="sxs-lookup"><span data-stu-id="64d0b-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="64d0b-148">Met een optie die wordt toegevoegd aan onkostennota's kunt u een onkostenregel maken op basis van een ontvangst of wordt geprobeerd een bestaand ontvangstbewijs te koppelen aan een bestaande onkostenregel.</span><span class="sxs-lookup"><span data-stu-id="64d0b-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="64d0b-149">Zie [Nieuwe invulling voor het begrip onkostennota's](ExpenseWorkspaceNew.md) voor meer informatie over de nieuwe functie voor onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="64d0b-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="64d0b-150">Veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="64d0b-150">Frequently asked questions</span></span>

<span data-ttu-id="64d0b-151">**Worden mijn gegevens door Microsoft gebruikt voor modellen?**</span><span class="sxs-lookup"><span data-stu-id="64d0b-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="64d0b-152">Nee, Microsoft heeft een algemeen machinetrainingsmodel voor de verwerkingsservice voor ontvangstbewijzen.</span><span class="sxs-lookup"><span data-stu-id="64d0b-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="64d0b-153">Dit model is niet gebaseerd op de ontvangstbewijzen die u uploadt.</span><span class="sxs-lookup"><span data-stu-id="64d0b-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="64d0b-154">**Waar is deze functie beschikbaar en wordt deze verwerkt?**</span><span class="sxs-lookup"><span data-stu-id="64d0b-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="64d0b-155">Momenteel worden de Verenigde Staten ondersteund.</span><span class="sxs-lookup"><span data-stu-id="64d0b-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="64d0b-156">**Waar gaan mijn ontvangstbewijzen naartoe?**</span><span class="sxs-lookup"><span data-stu-id="64d0b-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="64d0b-157">Finance neemt contact op met Cognitive Services om de veldgegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="64d0b-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="64d0b-158">Cognitive Services behoudt een kopie van uw ontvangstbewijs gedurende maximaal 24 uur terwijl de verwerking plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="64d0b-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="64d0b-159">Nadat de verwerking is voltooid, wordt het ontvangstbewijs door Cognitive Services verwijderd.</span><span class="sxs-lookup"><span data-stu-id="64d0b-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="64d0b-160">Ontvangstbewijzen worden nog steeds in Finance opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="64d0b-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="64d0b-161">Zie [Ontvangstbewijzen begrijpen inschakelen met de nieuwe mogelijkheid Formulierherkenning](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="64d0b-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
