---
title: Klanten kopiëren met behulp van gedeelde nummerreeksen
description: In dit onderwerp wordt uitgelegd hoe u gedeelde nummerreeksen kunt gebruiken om een klant te kopiëren naar een andere rechtspersoon, maar met behoud van dezelfde klant-id.
author: mikefalkner
manager: aolson
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 848c5b21afccb544e2b3d26ecc8cadac0c860796
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184135"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a><span data-ttu-id="65b09-103">Klanten kopiëren met behulp van gedeelde nummerreeksen</span><span class="sxs-lookup"><span data-stu-id="65b09-103">Copy customers by using shared number sequences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65b09-104">U kunt gedeelde nummerreeksen gebruiken om klant-id's toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="65b09-104">You can use shared number sequences to assign customer IDs.</span></span> <span data-ttu-id="65b09-105">Met gedeelde nummerreeksen kunt u ook klanten kopiëren van de ene rechtspersoon naar een andere, maar dezelfde klant-id's gebruiken voor beide rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="65b09-105">Shared number sequences also let you copy customers from one legal entity to another legal entity but use the same customer IDs in both legal entities.</span></span>

## <a name="setup"></a><span data-ttu-id="65b09-106">Instellen</span><span class="sxs-lookup"><span data-stu-id="65b09-106">Setup</span></span>

<span data-ttu-id="65b09-107">De functie wordt geactiveerd wanneer u een gedeelde nummerreeks gebruikt om klant-id's toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="65b09-107">The feature is activated when you use a shared number sequence to assign customer IDs.</span></span> <span data-ttu-id="65b09-108">In elke rechtspersoon waarnaar u een klant wilt kopiëren, moet u dezelfde nummerreeks gebruiken.</span><span class="sxs-lookup"><span data-stu-id="65b09-108">You must use the same number sequence in every legal entity that you want to copy a customer to.</span></span> <span data-ttu-id="65b09-109">U wijzigt de nummerreeks voor de klant op de pagina **Parameters van module Klanten** voor elke rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="65b09-109">You change the customer number sequence on the **Accounts receivable parameters** page for each legal entity.</span></span> <span data-ttu-id="65b09-110">Selecteer **Klanten** \> **Parameters** en selecteer vervolgens het tabblad **Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="65b09-110">Select **Accounts receivable** \> **Parameters**, and then select the **Number sequences** tab.</span></span>

<span data-ttu-id="65b09-111">U kunt ook nummerreeksen voor elke klantengroep instellen.</span><span class="sxs-lookup"><span data-stu-id="65b09-111">You can also set up customer number sequences for each customer group.</span></span> <span data-ttu-id="65b09-112">Deze nummerreeksen moeten ook worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="65b09-112">These number sequences must also be shared.</span></span> <span data-ttu-id="65b09-113">Eerst wordt de nummerreeks voor een klantengroep gebruikt.</span><span class="sxs-lookup"><span data-stu-id="65b09-113">The number sequence for a customer group is used first.</span></span> <span data-ttu-id="65b09-114">Als er geen nummerreeks is opgegeven voor een klantengroep, wordt de nummerreeks gebruikt die is opgegeven op de pagina **Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="65b09-114">If no number sequence is specified for a customer group, the number sequence that is specified on the **Accounts receivable parameters** page is used.</span></span>

<span data-ttu-id="65b09-115">U kunt ook klanten kopiëren tussen rechtspersonen als u handmatige klant-id's gebruikt.</span><span class="sxs-lookup"><span data-stu-id="65b09-115">You can also copy customers between legal entities if you use manual customer IDs.</span></span> <span data-ttu-id="65b09-116">Als u echter een klant probeert te kopiëren naar een rechtspersoon waar de klant-ID al bestaat, wordt het kopieerproces niet gestart.</span><span class="sxs-lookup"><span data-stu-id="65b09-116">However, if you try to copy a customer to a legal entity where the customer ID already exists, the copy process won't be started.</span></span>

## <a name="copy-a-customer"></a><span data-ttu-id="65b09-117">Een klant kopiëren</span><span class="sxs-lookup"><span data-stu-id="65b09-117">Copy a customer</span></span>

<span data-ttu-id="65b09-118">Als u een klant wilt kopiëren, selecteert u **Nieuw** op de lijstpagina **Alle klanten** om het dialoogvenster **Klant maken** te openen.</span><span class="sxs-lookup"><span data-stu-id="65b09-118">To copy a customer, select **New** on the **All customers** list page to open the **Create customer** dialog box.</span></span> <span data-ttu-id="65b09-119">U ziet dat de nieuwe klant-id niet onmiddellijk wordt toegewezen.</span><span class="sxs-lookup"><span data-stu-id="65b09-119">Notice that the new customer ID isn't assigned immediately.</span></span> <span data-ttu-id="65b09-120">Dit gedrag wijkt af van het gedrag in eerdere versies.</span><span class="sxs-lookup"><span data-stu-id="65b09-120">This behavior differs from the behavior in previous versions.</span></span> <span data-ttu-id="65b09-121">Omdat u de klantengroep nog niet hebt geselecteerd, kan het systeem niet de juiste nummerreeks bepalen die moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="65b09-121">Because you haven't yet selected the customer group, the system can't determine the correct number sequence to use.</span></span> <span data-ttu-id="65b09-122">Het kan bovendien niet bepalen of u een nieuwe klant wilt maken of een klant kopieert.</span><span class="sxs-lookup"><span data-stu-id="65b09-122">Additionally, it can't determine whether you're trying to create a new customer or copy a customer.</span></span> <span data-ttu-id="65b09-123">Daarom wordt de klant-id pas toegewezen als u **Opslaan** selecteert onderaan in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="65b09-123">Therefore, the customer ID isn't assigned until you select **Save** at the bottom of the dialog box.</span></span>

<span data-ttu-id="65b09-124">Als u een nieuwe klant maakt, kunt u zoals gebruikelijk verdergaan met het invullen van alle velden.</span><span class="sxs-lookup"><span data-stu-id="65b09-124">If you're creating a new customer, you can continue to fill in all the fields as you usually do.</span></span> <span data-ttu-id="65b09-125">Wanneer u klaar bent en **Opslaan** selecteert, ziet u dat de klant-ID automatisch is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="65b09-125">When you've finished, and you select **Save**, you will see that the customer ID was assigned automatically.</span></span> <span data-ttu-id="65b09-126">Bij handmatige nummerreeksen ziet u dat de handmatige klant-id is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="65b09-126">Alternatively, for manual number sequences, you will see that your manual customer ID was used.</span></span>

<span data-ttu-id="65b09-127">Als u een klant wilt kopiëren, voert u in het veld **Naam** een of meer tekens in die de klant aangeven die u zoekt.</span><span class="sxs-lookup"><span data-stu-id="65b09-127">To copy a customer, in the **Name** field, enter one or more characters that represent the customer that you're looking for.</span></span> <span data-ttu-id="65b09-128">In het dialoogvenster Zoeken ziet u een overzicht van de partijen die mogelijk de gezochte klant aangeven.</span><span class="sxs-lookup"><span data-stu-id="65b09-128">A search dialog box shows a list of parties that might represent the customer that you're looking for.</span></span> <span data-ttu-id="65b09-129">Wanneer u een van de partijen selecteert, wordt aanvullende informatie aan de rechterkant van het dialoogvenster weergegeven:</span><span class="sxs-lookup"><span data-stu-id="65b09-129">When you select one of the parties, additional information appears on the right side of the dialog box:</span></span>

- <span data-ttu-id="65b09-130">Op het tabblad **Algemeen** ziet u het telefoonnummer en het adres van de partij.</span><span class="sxs-lookup"><span data-stu-id="65b09-130">The **General** tab shows the party's phone number and address.</span></span>
- <span data-ttu-id="65b09-131">Op het tabblad **Rollen** ziet u de rollen die de geselecteerde partij kan hebben en de rechtspersoon waarin de partij een rol heeft.</span><span class="sxs-lookup"><span data-stu-id="65b09-131">The **Roles** tab shows the roles that the selected party can have and the legal entity where it has each role.</span></span>
- <span data-ttu-id="65b09-132">Het tabblad **Belastingregistratie-id** geeft de belastingregistratie-id's weer die zijn toegewezen aan de partij.</span><span class="sxs-lookup"><span data-stu-id="65b09-132">**Tax registration ID** tab shows the tax registration IDs that are assigned to the party.</span></span>

<span data-ttu-id="65b09-133">U kunt een partij alleen kopiëren als deze een klantrol heeft in een rechtspersoon die niet de huidige rechtspersoon is.</span><span class="sxs-lookup"><span data-stu-id="65b09-133">You can copy a party only if it has a customer role, and if it has that role in a legal entity that isn't the current legal entity.</span></span> <span data-ttu-id="65b09-134">Volg deze stappen als u een partij vindt die aan deze criteria voldoet.</span><span class="sxs-lookup"><span data-stu-id="65b09-134">When you find a party that meets these criteria, follow these steps.</span></span>

1. <span data-ttu-id="65b09-135">De optie **Klant kopiëren** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="65b09-135">A **Copy customer** option appears.</span></span> <span data-ttu-id="65b09-136">Standaard is deze optie ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="65b09-136">By default, this option is set to **No**.</span></span> <span data-ttu-id="65b09-137">Als u de klant naar de huidige rechtspersoon wilt kopiëren, zet u de optie op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="65b09-137">To copy the customer to the current legal entity, set the option to **Yes**.</span></span> 
2. <span data-ttu-id="65b09-138">Het veld **Rechtspersoon** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="65b09-138">A **Legal entity** field appears.</span></span> <span data-ttu-id="65b09-139">Selecteer de rechtspersoon waarvan u de klant wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="65b09-139">Select the legal entity to copy the customer from.</span></span> <span data-ttu-id="65b09-140">Als de klant alleen in één rechtspersoon bestaat, wordt het veld standaard ingesteld op die rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="65b09-140">If the customer exists in only one legal entity, the field is set to that legal entity by default.</span></span>
3. <span data-ttu-id="65b09-141">Selecteer **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="65b09-141">Select **Select**.</span></span> <span data-ttu-id="65b09-142">De klant wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="65b09-142">The new customer is created.</span></span>

## <a name="validation"></a><span data-ttu-id="65b09-143">Validatie</span><span class="sxs-lookup"><span data-stu-id="65b09-143">Validation</span></span>

<span data-ttu-id="65b09-144">Wanneer u een klant kopieert, probeert het systeem de gegevens van de nieuwe klant op te slaan.</span><span class="sxs-lookup"><span data-stu-id="65b09-144">When you copy a customer, the system tries to save the new customer information.</span></span> <span data-ttu-id="65b09-145">Er worden validaties uitgevoerd om te controleren of de gekopieerde gegevens correct zijn.</span><span class="sxs-lookup"><span data-stu-id="65b09-145">Validations are run to verify that the data that was copied is good.</span></span> <span data-ttu-id="65b09-146">U ontvangt een foutbericht voor elke mislukte validatie.</span><span class="sxs-lookup"><span data-stu-id="65b09-146">You receive an error message for every validation that fails.</span></span> <span data-ttu-id="65b09-147">In het foutbericht wordt uitgelegd welke gegevens moeten worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="65b09-147">The error messages explain what information must be updated.</span></span> <span data-ttu-id="65b09-148">De kopie van de klant kan pas worden opgeslagen als u alle validatiefouten hebt opgelost.</span><span class="sxs-lookup"><span data-stu-id="65b09-148">The copy of the customer can't be saved until you fix all the validation errors.</span></span>

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a><span data-ttu-id="65b09-149">Een klant kopiëren met de functie Btw-nummer zoeken</span><span class="sxs-lookup"><span data-stu-id="65b09-149">Copy a customer by using tax exempt number search feature</span></span>

<span data-ttu-id="65b09-150">U kunt klanten ook kopiëren met de functie Btw-nummer zoeken die u vindt in de groep **Registratie** op het tabblad **Klant** in het actievenster van de pagina **Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="65b09-150">You can also copy customers by using the Tax exempt number search feature that is in the **Registration** group on the **Customer** tab on the Action Pane of the **All customers** page.</span></span> <span data-ttu-id="65b09-151">In het dialoogvenster **Btw-nummer zoeken** dat wordt weergegeven, ziet u btw-nummers, de klant-id, de naam van de klant en de rechtspersoon waarin de btw-id wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="65b09-151">The **Tax exempt number search** dialog box that appears shows tax exempt numbers, the customer ID, the customer name, and the legal entity where the tax exempt ID is used.</span></span> <span data-ttu-id="65b09-152">U kunt een klant alleen kopiëren als deze bij een rechtspersoon hoort die niet de huidige rechtspersoon is.</span><span class="sxs-lookup"><span data-stu-id="65b09-152">You can copy a customer only if it's in a legal entity that isn't the current legal entity.</span></span> <span data-ttu-id="65b09-153">Nadat u een klant hebt geselecteerd die aan dit criterium voldoet, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="65b09-153">After you select a customer that meets this criterion, follow these steps.</span></span>

1. <span data-ttu-id="65b09-154">De optie **Klant kopiëren** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="65b09-154">A **Copy customer** option appears.</span></span> <span data-ttu-id="65b09-155">Standaard is deze optie ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="65b09-155">By default, this option is set to **No**.</span></span> <span data-ttu-id="65b09-156">Als u de klant naar de huidige rechtspersoon wilt kopiëren, zet u de optie op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="65b09-156">To copy the customer to the current legal entity, set the option to **Yes**.</span></span> 
2. <span data-ttu-id="65b09-157">Selecteer **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="65b09-157">Select **Select**.</span></span> <span data-ttu-id="65b09-158">De klant wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="65b09-158">The new customer is created.</span></span>