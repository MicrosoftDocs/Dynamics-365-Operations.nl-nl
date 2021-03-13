---
title: Btw-overeenkomst en -overschrijvingen
description: Deze procedure laat zien hoe u btw-groepen kunt toewijzen aan kanalen voor handel.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c6e1de5046a3ce5d896ba3686a28d6d474d4268
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020723"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="aac08-103">Btw-overeenkomst en -overschrijvingen</span><span class="sxs-lookup"><span data-stu-id="aac08-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aac08-104">Deze procedure laat zien hoe u btw-groepen kunt toewijzen aan kanalen voor handel.</span><span class="sxs-lookup"><span data-stu-id="aac08-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="aac08-105">Ook wordt het proces doorlopen van het maken van een nieuwe btw-overschrijving en het toewijzen hiervan aan een bestaande groep voor btw-overschrijving.</span><span class="sxs-lookup"><span data-stu-id="aac08-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="aac08-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="aac08-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="aac08-107">Ga naar Retail en Commerce > Kanalen > Winkels > Alle winkels.</span><span class="sxs-lookup"><span data-stu-id="aac08-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="aac08-108">Klik in de lijst op de koppeling Kanaal-id voor "Houston".</span><span class="sxs-lookup"><span data-stu-id="aac08-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="aac08-109">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="aac08-109">Click Edit.</span></span>
    * <span data-ttu-id="aac08-110">Het veld Btw-groep bevat de lijst met btw-groepen voor het huidige bedrijf.</span><span class="sxs-lookup"><span data-stu-id="aac08-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="aac08-111">De huidige toegewezen groep is een algemene btw-groep genaamd "Texas".</span><span class="sxs-lookup"><span data-stu-id="aac08-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="aac08-112">Er zijn ook btw-groepen voor 'Washington' en 'Washington, King County.'</span><span class="sxs-lookup"><span data-stu-id="aac08-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="aac08-113">Btw-groepen kunnen van toepassing zijnde belastingen voor meerdere gemeenten bevatten.</span><span class="sxs-lookup"><span data-stu-id="aac08-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="aac08-114">In het veld Btw-overschrijving kunnen groepen voor btw-overschrijving aan het kanaal worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="aac08-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="aac08-115">Groepen voor btw-overschrijving kunnen worden gebruikt om btw-overschrijvingen te groeperen die werken voor meerdere winkelen.</span><span class="sxs-lookup"><span data-stu-id="aac08-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="aac08-116">In plaats van btw-overschrijvingen handmatig één voor één toe te wijzen, kan de groep worden gemaakt en rechtstreeks aan de kanalen worden toegewezen om tijd te besparen.</span><span class="sxs-lookup"><span data-stu-id="aac08-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="aac08-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="aac08-117">Click Save.</span></span>
5. <span data-ttu-id="aac08-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="aac08-118">Close the page.</span></span>
6. <span data-ttu-id="aac08-119">Ga naar Detailhandel en commerce > Kanaalinstellingen > Btw > Btw-overschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="aac08-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="aac08-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="aac08-120">Click New.</span></span>
8. <span data-ttu-id="aac08-121">Geef in het veld Btw-overschrijving een naam op voor uw nieuwe overschrijving.</span><span class="sxs-lookup"><span data-stu-id="aac08-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="aac08-122">Neem in het veld Omschrijving een beschrijving van de overschrijving op.</span><span class="sxs-lookup"><span data-stu-id="aac08-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="aac08-123">Stel de status in op "Inschakelen".</span><span class="sxs-lookup"><span data-stu-id="aac08-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="aac08-124">Vouw de sectie Overschrijving uit of samen.</span><span class="sxs-lookup"><span data-stu-id="aac08-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="aac08-125">Selecteer een optie in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="aac08-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="aac08-126">Btw-groepen voor artikel kunnen worden gebruikt om de btw te negeren voor specifieke artikelen die bij de groep behoren.</span><span class="sxs-lookup"><span data-stu-id="aac08-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="aac08-127">Zo worden bijvoorbeeld voedingsartikelen meestal anders belast dan harde goederen en hebben waarschijnlijk een eigen btw-groep.</span><span class="sxs-lookup"><span data-stu-id="aac08-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="aac08-128">Btw-groepen zijn groepen belastingen op een bepaald kanaal van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="aac08-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="aac08-129">Als bijvoorbeeld een kanaal zowel aan de detailhandel als business-to-business verkoopt, kunnen verschillende btw-groepen voor artikelen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="aac08-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="aac08-130">Alle relevante belastingen worden dan aan de btw-groep toegewezen.</span><span class="sxs-lookup"><span data-stu-id="aac08-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="aac08-131">U kunt nu de "Vanaf"- en "T/m"-btw of "Vanaf btw-groep" en "T/m btw-groep" selecteren om uw eigen btw-overschrijving te maken.</span><span class="sxs-lookup"><span data-stu-id="aac08-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="aac08-132">Het veld "Vanaf" geeft de btw of btw-groep aan die moet worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="aac08-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="aac08-133">Overschrijving van btw-groep van artikel biedt andere opties dan overschrijving van btw-groep.</span><span class="sxs-lookup"><span data-stu-id="aac08-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="aac08-134">Btw-overschrijvingen kunnen worden ingesteld voor het overschrijven van btw over hele transacties of over specifieke regels in de transactie.</span><span class="sxs-lookup"><span data-stu-id="aac08-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="aac08-135">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="aac08-135">Click Save.</span></span>
14. <span data-ttu-id="aac08-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="aac08-136">Close the page.</span></span>
15. <span data-ttu-id="aac08-137">Ga naar Detailhandel en commerce > Kanaalinstellingen > Btw > Groepen voor btw-overschrijving.</span><span class="sxs-lookup"><span data-stu-id="aac08-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="aac08-138">In deze stap gaat u de nieuw gemaakte btw-overschrijving toewijzen aan de groep voor btw-overschrijving die is toegewezen aan het Houston-kanaal.</span><span class="sxs-lookup"><span data-stu-id="aac08-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="aac08-139">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="aac08-139">Click Edit.</span></span>
17. <span data-ttu-id="aac08-140">Vouw de sectie Instellingen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="aac08-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="aac08-141">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="aac08-141">Click Add.</span></span>
19. <span data-ttu-id="aac08-142">Klik in het veld Btw-overschrijving op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="aac08-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="aac08-143">Selecteer de eerder gemaakte btw-overschrijving in de lijst.</span><span class="sxs-lookup"><span data-stu-id="aac08-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="aac08-144">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="aac08-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="aac08-145">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="aac08-145">Click Save.</span></span>

