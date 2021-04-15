---
title: Een standaardklant maken
description: In dit onderwerp wordt beschreven hoe u een standaardklant kunt maken die u kunt gebruiken wanneer u een kanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799174"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="886eb-103">Een standaardklant maken</span><span class="sxs-lookup"><span data-stu-id="886eb-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="886eb-104">In dit onderwerp wordt beschreven hoe u een standaardklant kunt maken die u kunt gebruiken wanneer u een kanaal maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="886eb-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="886eb-105">Wanneer u een kanaal maakt, moet u een standaardklant opgeven.</span><span class="sxs-lookup"><span data-stu-id="886eb-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="886eb-106">U kunt eenvoudig een standaardklant maken nadat u eerst de klantgroep en het adresboek van de klant hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="886eb-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="886eb-107">Een klantgroep maken</span><span class="sxs-lookup"><span data-stu-id="886eb-107">Create a customer group</span></span>

<span data-ttu-id="886eb-108">Als er nog geen klantgroepen zijn, kunt u er een maken.</span><span class="sxs-lookup"><span data-stu-id="886eb-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="886eb-109">Voorbeelden zijn groepen die verschillende klantgroepen vertegenwoordigen, zoals groothandel, internet, werknemers, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="886eb-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="886eb-110">Volg deze stappen om een klantgroep te maken.</span><span class="sxs-lookup"><span data-stu-id="886eb-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="886eb-111">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Klanten \> Klantgroepen**.</span><span class="sxs-lookup"><span data-stu-id="886eb-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="886eb-112">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="886eb-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="886eb-113">Voer in het vak **Klantgroep** een klantgroep-id in.</span><span class="sxs-lookup"><span data-stu-id="886eb-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="886eb-114">Voer in het vak **Omschrijving** een passende beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="886eb-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="886eb-115">Voer in het vak **Betalingsvoorwaarden** een toepasselijke waarde in.</span><span class="sxs-lookup"><span data-stu-id="886eb-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="886eb-116">Voer in het vak **Tijd tussen vervaldatum van factuur en betalingsdatum** een toepasselijke waarde in.</span><span class="sxs-lookup"><span data-stu-id="886eb-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="886eb-117">Voer in het vak **Standaardbelastinggroep** een belastinggroep in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="886eb-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="886eb-118">Schakel het selectievakje **Prijzen inclusief btw** in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="886eb-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="886eb-119">Voer in het vak **Standaardreden voor afschrijving** een toepasselijke waarde in, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="886eb-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="886eb-120">De volgende afbeelding geeft een aantal geconfigureerde klantgroepen weer.</span><span class="sxs-lookup"><span data-stu-id="886eb-120">The following image shows several configured customer groups.</span></span>

![Klantengroepen](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="886eb-122">Een nieuw adresboek voor een klant maken</span><span class="sxs-lookup"><span data-stu-id="886eb-122">Create a customer address book</span></span>

<span data-ttu-id="886eb-123">Een klant moet aan een adresboek zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="886eb-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="886eb-124">Als er nog geen is gemaakt, moet u er een maken.</span><span class="sxs-lookup"><span data-stu-id="886eb-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="886eb-125">Volg deze stappen om een nieuw klantadresboek te maken.</span><span class="sxs-lookup"><span data-stu-id="886eb-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="886eb-126">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Kanaalinstellingen \> Adresboeken**.</span><span class="sxs-lookup"><span data-stu-id="886eb-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="886eb-127">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="886eb-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="886eb-128">Voer in het vak **Naam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="886eb-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="886eb-129">Voer in het vak **Omschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="886eb-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="886eb-130">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="886eb-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="886eb-131">In de volgende afbeelding ziet u een voorbeeld van een adresboek.</span><span class="sxs-lookup"><span data-stu-id="886eb-131">The following image shows an example address book.</span></span>

![Adresboek](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="886eb-133">Een standaardklant maken</span><span class="sxs-lookup"><span data-stu-id="886eb-133">Create a default customer</span></span>

<span data-ttu-id="886eb-134">Volg deze stappen om een standaardklant te maken.</span><span class="sxs-lookup"><span data-stu-id="886eb-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="886eb-135">Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Klanten \> Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="886eb-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="886eb-136">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="886eb-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="886eb-137">Selecteer 'Persoon' in de vervolgkeuzelijst **Type**.</span><span class="sxs-lookup"><span data-stu-id="886eb-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="886eb-138">Selecteer in de vervolgkeuzelijst **Klantrekening** een rekeningnummer of voer dit in (bijvoorbeeld '100001').</span><span class="sxs-lookup"><span data-stu-id="886eb-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="886eb-139">Selecteer of typ in de vervolgkeuzelijst **Voornaam** een naam (bijvoorbeeld 'Standaard').</span><span class="sxs-lookup"><span data-stu-id="886eb-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="886eb-140">Selecteer of typ in de vervolgkeuzelijst **Tweede voornaam** een naam (bijvoorbeeld 'Retail').</span><span class="sxs-lookup"><span data-stu-id="886eb-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="886eb-141">Selecteer of typ in de vervolgkeuzelijst **Achternaam** een naam (bijvoorbeeld 'Klant').</span><span class="sxs-lookup"><span data-stu-id="886eb-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="886eb-142">Selecteer of typ in de vervolgkeuzelijst **Valuta** een valuta (bijvoorbeeld 'EUR').</span><span class="sxs-lookup"><span data-stu-id="886eb-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="886eb-143">Selecteer in de vervolgkeuzelijst **Valuta** de zojuist gemaakte klantgroep.</span><span class="sxs-lookup"><span data-stu-id="886eb-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="886eb-144">Selecteer in de vervolgkeuzelijst **Adresboeken** een bestaand adresboek van de klant.</span><span class="sxs-lookup"><span data-stu-id="886eb-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="886eb-145">Selecteer **Opslaan** en ga terug naar het scherm met klantgegevens voor de nieuwe klant.</span><span class="sxs-lookup"><span data-stu-id="886eb-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="886eb-146">Het is niet nodig om een adres voor een standaardklant toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="886eb-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="886eb-147">In de volgende afbeelding ziet u hoe een klant wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="886eb-147">The following image shows an example of customer creation.</span></span>

![Een standaardklant maken](media/default-customer-creation.png)

<span data-ttu-id="886eb-149">In de volgende afbeelding wordt de configuratie van een standaardklant weergegeven.</span><span class="sxs-lookup"><span data-stu-id="886eb-149">The following image shows a default customer configuration.</span></span>

![Voorbeeld van klantconfiguratie](media/default-customer-configuration1.png)

<span data-ttu-id="886eb-151">De meeste standaardwaarden in het detailscherm van de klant kunnen blijven staan, maar twee waarden moeten worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="886eb-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="886eb-152">Vouw in het scherm met klantgegevens de **Standaardwaarden verkooporders** uit.</span><span class="sxs-lookup"><span data-stu-id="886eb-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="886eb-153">Selecteer in de vervolgkeuzelijst **Site** een vooraf geconfigureerde site of voer deze in.</span><span class="sxs-lookup"><span data-stu-id="886eb-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="886eb-154">Selecteer in de vervolgkeuzelijst **Magazijn** een vooraf geconfigureerd magazijn of voer dit in.</span><span class="sxs-lookup"><span data-stu-id="886eb-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="886eb-155">In de volgende afbeelding ziet u hoe een klant wordt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="886eb-155">The following image shows an example customer configuration.</span></span>

![Voorbeeld van klantconfiguratie](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="886eb-157">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="886eb-157">Additional resources</span></span>

[<span data-ttu-id="886eb-158">Overzicht van kanalen</span><span class="sxs-lookup"><span data-stu-id="886eb-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="886eb-159">Vereisten voor het instellen van kanalen</span><span class="sxs-lookup"><span data-stu-id="886eb-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
