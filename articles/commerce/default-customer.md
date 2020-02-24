---
title: Een standaardklant maken
description: In dit onderwerp wordt beschreven hoe u een standaardklant kunt maken die u kunt gebruiken wanneer u een kanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e1087821b357c578993cdd5742399c5ec0ecc95
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001801"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="07e88-103">Een standaardklant maken</span><span class="sxs-lookup"><span data-stu-id="07e88-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="07e88-104">In dit onderwerp wordt beschreven hoe u een standaardklant kunt maken die u kunt gebruiken wanneer u een kanaal maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="07e88-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="07e88-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="07e88-105">Overview</span></span>

<span data-ttu-id="07e88-106">Wanneer u een Retail- of online kanaal maakt, moet u een standaardklant opgeven.</span><span class="sxs-lookup"><span data-stu-id="07e88-106">When creating a retail or online channel, you will need to provide a default customer.</span></span> <span data-ttu-id="07e88-107">U kunt eenvoudig een standaardklant maken nadat u eerst de klantgroep en het adresboek van de klant hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="07e88-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="07e88-108">Een klantgroep maken</span><span class="sxs-lookup"><span data-stu-id="07e88-108">Create a customer group</span></span>

<span data-ttu-id="07e88-109">Als er nog geen klantgroepen zijn, kunt u er een maken.</span><span class="sxs-lookup"><span data-stu-id="07e88-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="07e88-110">Voorbeelden zijn groepen die verschillende klantgroepen vertegenwoordigen, zoals groothandel, internet, werknemers, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="07e88-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="07e88-111">Volg deze stappen om een klantgroep te maken.</span><span class="sxs-lookup"><span data-stu-id="07e88-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="07e88-112">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Klanten \> Klantgroepen**.</span><span class="sxs-lookup"><span data-stu-id="07e88-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="07e88-113">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="07e88-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="07e88-114">Voer in het vak **Klantgroep** een klantgroep-id in.</span><span class="sxs-lookup"><span data-stu-id="07e88-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="07e88-115">Voer in het vak **Omschrijving** een passende beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="07e88-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="07e88-116">Voer in het vak **Betalingsvoorwaarden** een toepasselijke waarde in.</span><span class="sxs-lookup"><span data-stu-id="07e88-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="07e88-117">Voer in het vak **Tijd tussen vervaldatum van factuur en betalingsdatum** een toepasselijke waarde in.</span><span class="sxs-lookup"><span data-stu-id="07e88-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="07e88-118">Voer in het vak **Standaardbelastinggroep** een belastinggroep in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="07e88-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="07e88-119">Schakel het selectievakje **Prijzen inclusief btw** in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="07e88-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="07e88-120">Voer in het vak **Standaardreden voor afschrijving** een toepasselijke waarde in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="07e88-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="07e88-121">De volgende afbeelding geeft een aantal geconfigureerde klantgroepen weer.</span><span class="sxs-lookup"><span data-stu-id="07e88-121">The following image shows several configured customer groups.</span></span>

![Klantengroepen](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="07e88-123">Een nieuw adresboek voor een klant maken</span><span class="sxs-lookup"><span data-stu-id="07e88-123">Create a customer address book</span></span>

<span data-ttu-id="07e88-124">Een klant moet aan een adresboek zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="07e88-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="07e88-125">Als er nog geen is gemaakt, moet u er een maken.</span><span class="sxs-lookup"><span data-stu-id="07e88-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="07e88-126">Volg deze stappen om een nieuw klantadresboek te maken.</span><span class="sxs-lookup"><span data-stu-id="07e88-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="07e88-127">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Kanaalinstellingen \> Adresboeken**.</span><span class="sxs-lookup"><span data-stu-id="07e88-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="07e88-128">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="07e88-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="07e88-129">Voer in het vak **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="07e88-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="07e88-130">Voer in het vak **Omschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="07e88-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="07e88-131">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="07e88-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="07e88-132">In de volgende afbeelding ziet u een voorbeeld van een adresboek.</span><span class="sxs-lookup"><span data-stu-id="07e88-132">The following image shows an example address book.</span></span>

![Adresboek](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="07e88-134">Een standaardklant maken</span><span class="sxs-lookup"><span data-stu-id="07e88-134">Create a default customer</span></span>

<span data-ttu-id="07e88-135">Volg deze stappen om een standaardklant te maken.</span><span class="sxs-lookup"><span data-stu-id="07e88-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="07e88-136">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Klanten \> Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="07e88-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="07e88-137">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="07e88-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="07e88-138">Selecteer 'Persoon' in de vervolgkeuzelijst **Type**.</span><span class="sxs-lookup"><span data-stu-id="07e88-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="07e88-139">Selecteer in de vervolgkeuzelijst **Klantrekening** een rekeningnummer of voer dit in (bijvoorbeeld '100001').</span><span class="sxs-lookup"><span data-stu-id="07e88-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="07e88-140">Selecteer of typ in de vervolgkeuzelijst **Voornaam** een naam (bijvoorbeeld 'Standaard').</span><span class="sxs-lookup"><span data-stu-id="07e88-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="07e88-141">Selecteer of typ in de vervolgkeuzelijst **Tweede voornaam** een naam (bijvoorbeeld 'Retail').</span><span class="sxs-lookup"><span data-stu-id="07e88-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="07e88-142">Selecteer of typ in de vervolgkeuzelijst **Achternaam** een naam (bijvoorbeeld 'Klant').</span><span class="sxs-lookup"><span data-stu-id="07e88-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="07e88-143">Selecteer of typ in de vervolgkeuzelijst **Valuta** een valuta (bijvoorbeeld 'EUR').</span><span class="sxs-lookup"><span data-stu-id="07e88-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="07e88-144">Selecteer in de vervolgkeuzelijst **Valuta** de zojuist gemaakte klantgroep.</span><span class="sxs-lookup"><span data-stu-id="07e88-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="07e88-145">Selecteer in de vervolgkeuzelijst **Adresboeken** een bestaand adresboek van de klant.</span><span class="sxs-lookup"><span data-stu-id="07e88-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="07e88-146">Selecteer **Opslaan** en ga terug naar het scherm met klantgegevens voor de nieuwe klant.</span><span class="sxs-lookup"><span data-stu-id="07e88-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="07e88-147">Het is niet nodig om een adres voor een standaardklant toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="07e88-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="07e88-148">In de volgende afbeelding ziet u hoe een klant wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="07e88-148">The following image shows an example of customer creation.</span></span>

![Een standaardklant maken](media/default-customer-creation.png)

<span data-ttu-id="07e88-150">In de volgende afbeelding wordt de configuratie van een standaardklant weergegeven.</span><span class="sxs-lookup"><span data-stu-id="07e88-150">The following image shows a default customer configuration.</span></span>

![Voorbeeld van klantconfiguratie](media/default-customer-configuration1.png)

<span data-ttu-id="07e88-152">De meeste standaardwaarden in het detailscherm van de klant kunnen blijven staan, maar twee waarden moeten worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="07e88-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="07e88-153">Vouw in het scherm met klantgegevens de **Standaardwaarden verkooporders** uit.</span><span class="sxs-lookup"><span data-stu-id="07e88-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="07e88-154">Selecteer in de vervolgkeuzelijst **Site** een vooraf geconfigureerde site of voer deze in.</span><span class="sxs-lookup"><span data-stu-id="07e88-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="07e88-155">Selecteer in de vervolgkeuzelijst **Magazijn** een vooraf geconfigureerd magazijn of voer dit in.</span><span class="sxs-lookup"><span data-stu-id="07e88-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="07e88-156">In de volgende afbeelding ziet u hoe een klant wordt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="07e88-156">The following image shows an example customer configuration.</span></span>

![Voorbeeld van klantconfiguratie](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="07e88-158">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="07e88-158">Additional resources</span></span>

[<span data-ttu-id="07e88-159">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="07e88-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="07e88-160">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="07e88-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
