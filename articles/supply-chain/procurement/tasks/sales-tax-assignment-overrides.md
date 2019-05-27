---
title: Btw-overeenkomst en -overschrijvingen
description: Deze procedure laat zien hoe u btw-groepen kunt toewijzen aan detailhandelkanalen.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1907b0d0266eaa405ac2b92b40d6a2d310cf07b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569932"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="80c3d-103">Btw-overeenkomst en -overschrijvingen</span><span class="sxs-lookup"><span data-stu-id="80c3d-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80c3d-104">Deze procedure laat zien hoe u btw-groepen kunt toewijzen aan detailhandelkanalen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="80c3d-105">Ook wordt het proces doorlopen van het maken van een nieuwe btw-overschrijving en het toewijzen hiervan aan een bestaande groep voor btw-overschrijving.</span><span class="sxs-lookup"><span data-stu-id="80c3d-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="80c3d-106">Deze procedure</span><span class="sxs-lookup"><span data-stu-id="80c3d-106">This procedure</span></span>

<span data-ttu-id="80c3d-107">gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="80c3d-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="80c3d-108">Ga naar Detailhandel en commerce > Kanalen > Detailhandelwinkels > Alle detailhandelwinkels.</span><span class="sxs-lookup"><span data-stu-id="80c3d-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="80c3d-109">Klik in de lijst op de koppeling Id van detailhandelafzetkanaal voor "Houston".</span><span class="sxs-lookup"><span data-stu-id="80c3d-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="80c3d-110">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="80c3d-110">Click Edit.</span></span>
    * <span data-ttu-id="80c3d-111">Het veld Btw-groep bevat de lijst met btw-groepen voor het huidige bedrijf.</span><span class="sxs-lookup"><span data-stu-id="80c3d-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="80c3d-112">De huidige toegewezen groep is een algemene btw-groep genaamd "Texas".</span><span class="sxs-lookup"><span data-stu-id="80c3d-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="80c3d-113">Er zijn ook btw-groepen voor 'Washington' en 'Washington, King County.'</span><span class="sxs-lookup"><span data-stu-id="80c3d-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="80c3d-114">Btw-groepen kunnen van toepassing zijnde belastingen voor meerdere gemeenten bevatten.</span><span class="sxs-lookup"><span data-stu-id="80c3d-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="80c3d-115">In het veld Btw-overschrijving kunnen groepen voor btw-overschrijving aan het kanaal worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="80c3d-116">Groepen voor btw-overschrijving kunnen worden gebruikt om btw-overschrijvingen te groeperen die werken voor meerdere winkelen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="80c3d-117">In plaats van btw-overschrijvingen handmatig één voor één toe te wijzen, kan de groep worden gemaakt en rechtstreeks aan de kanalen worden toegewezen om tijd te besparen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="80c3d-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="80c3d-118">Click Save.</span></span>
5. <span data-ttu-id="80c3d-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="80c3d-119">Close the page.</span></span>
6. <span data-ttu-id="80c3d-120">Ga naar Detailhandel en commerce > Kanaalinstellingen > Btw > Btw-overschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="80c3d-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="80c3d-121">Click New.</span></span>
8. <span data-ttu-id="80c3d-122">Geef in het veld Btw-overschrijving een naam op voor uw nieuwe overschrijving.</span><span class="sxs-lookup"><span data-stu-id="80c3d-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="80c3d-123">Neem in het veld Omschrijving een beschrijving van de overschrijving op.</span><span class="sxs-lookup"><span data-stu-id="80c3d-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="80c3d-124">Stel de status in op "Inschakelen".</span><span class="sxs-lookup"><span data-stu-id="80c3d-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="80c3d-125">Vouw de sectie Overschrijving uit of samen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="80c3d-126">Selecteer een optie in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="80c3d-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="80c3d-127">Btw-groepen voor artikel kunnen worden gebruikt om de btw te negeren voor specifieke artikelen die bij de groep behoren.</span><span class="sxs-lookup"><span data-stu-id="80c3d-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="80c3d-128">Zo worden bijvoorbeeld voedingsartikelen meestal anders belast dan harde goederen en hebben waarschijnlijk een eigen btw-groep.</span><span class="sxs-lookup"><span data-stu-id="80c3d-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="80c3d-129">Btw-groepen zijn groepen belastingen op een bepaald kanaal van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="80c3d-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="80c3d-130">Als bijvoorbeeld een kanaal zowel aan de detailhandel als business-to-business verkoopt, kunnen verschillende btw-groepen voor artikelen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="80c3d-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="80c3d-131">Alle relevante belastingen worden dan aan de btw-groep toegewezen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="80c3d-132">U kunt nu de "Vanaf"- en "T/m"-btw of "Vanaf btw-groep" en "T/m btw-groep" selecteren om uw eigen btw-overschrijving te maken.</span><span class="sxs-lookup"><span data-stu-id="80c3d-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="80c3d-133">Het veld "Vanaf" geeft de btw of btw-groep aan die moet worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="80c3d-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="80c3d-134">Overschrijving van btw-groep van artikel biedt andere opties dan overschrijving van btw-groep.</span><span class="sxs-lookup"><span data-stu-id="80c3d-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="80c3d-135">Btw-overschrijvingen kunnen worden ingesteld voor het overschrijven van btw over hele transacties of over specifieke regels in de transactie.</span><span class="sxs-lookup"><span data-stu-id="80c3d-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="80c3d-136">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="80c3d-136">Click Save.</span></span>
14. <span data-ttu-id="80c3d-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="80c3d-137">Close the page.</span></span>
15. <span data-ttu-id="80c3d-138">Ga naar Detailhandel en commerce > Kanaalinstellingen > Btw > Groepen voor btw-overschrijving.</span><span class="sxs-lookup"><span data-stu-id="80c3d-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="80c3d-139">In deze stap gaat u de nieuw gemaakte btw-overschrijving toewijzen aan de groep voor btw-overschrijving die is toegewezen aan het Houston-kanaal.</span><span class="sxs-lookup"><span data-stu-id="80c3d-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="80c3d-140">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="80c3d-140">Click Edit.</span></span>
17. <span data-ttu-id="80c3d-141">Vouw de sectie Instellingen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="80c3d-142">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-142">Click Add.</span></span>
19. <span data-ttu-id="80c3d-143">Klik in het veld Btw-overschrijving op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="80c3d-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="80c3d-144">Selecteer de eerder gemaakte btw-overschrijving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="80c3d-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="80c3d-145">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="80c3d-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="80c3d-146">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="80c3d-146">Click Save.</span></span>

