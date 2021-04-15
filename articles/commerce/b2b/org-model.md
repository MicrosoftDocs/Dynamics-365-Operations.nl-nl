---
title: Hiërarchieën voor organisatiemodellering voor B2B-organisaties maken
description: In dit onderwerp wordt beschreven hoe u hiërarchieën voor organisatiemodellen maakt voor B2B-organisaties (business-to-business).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799824"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="ab892-103">Hiërarchieën voor organisatiemodellering voor B2B-organisaties maken</span><span class="sxs-lookup"><span data-stu-id="ab892-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab892-104">In dit onderwerp wordt beschreven hoe u hiërarchieën voor organisatiemodellen maakt voor B2B-organisaties (business-to-business) in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab892-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ab892-105">In Commerce Headquarters worden zakenpartnerorganisaties vertegenwoordigd door klant- en klanthiërarchie-entiteiten.</span><span class="sxs-lookup"><span data-stu-id="ab892-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="ab892-106">De organisatie van zakenpartners en haar gebruikers worden weergegeven als klanten en klanthiërarchieën worden gebruikt om die klanten aan elkaar te koppelen.</span><span class="sxs-lookup"><span data-stu-id="ab892-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="ab892-107">Wanneer een aanvraag van een zakenpartner voor toegang tot een B2B-e-commercesite wordt goedgekeurd, worden de volgende acties uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="ab892-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="ab892-108">Er worden twee nieuwe klantrecords in het systeem gemaakt: een klantrecord **Organisatietype** voor de organisatie van de zakenpartner en een klantrecord **Type persoon** voor de aanvrager (dat wil zeggen, de zakenpartnergebruiker die de aanvraag heeft ingediend).</span><span class="sxs-lookup"><span data-stu-id="ab892-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="ab892-109">Er wordt een nieuw klanthiërarchierecord gemaakt onder **Klant \> Klanthiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="ab892-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="ab892-110">Deze record heeft de volgende kopteksteigenschappen:</span><span class="sxs-lookup"><span data-stu-id="ab892-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="ab892-111">**Klanthiërarchie-id**: een unieke id voor de klanthiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ab892-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="ab892-112">Deze id gebruikt de nummerreeks die is gedefinieerd in gedeelde parameters voor Commerce in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ab892-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="ab892-113">**Naam**: de naam van de organisatie van de zakenpartner, zoals is opgegeven in de aanvraag voor onboarding.</span><span class="sxs-lookup"><span data-stu-id="ab892-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="ab892-114">**Doel**: deze eigenschap is ingesteld op de vooraf gedefinieerde waarde **B2B-organisatie**.</span><span class="sxs-lookup"><span data-stu-id="ab892-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="ab892-115">**Organisatie**: de klant-id van de zakenpartner.</span><span class="sxs-lookup"><span data-stu-id="ab892-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="ab892-116">Hieronder vindt u de details van de klanthiërarchierecord:</span><span class="sxs-lookup"><span data-stu-id="ab892-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="ab892-117">De klantrecord van de aanvrager is gekoppeld aan de klanthiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ab892-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="ab892-118">De rol van beheerder is gekoppeld aan de aanvrager.</span><span class="sxs-lookup"><span data-stu-id="ab892-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="ab892-119">Wanneer de beheerder meer gebruikers toevoegt aan de organisatie van de zakenpartner op een B2B-site, wordt er een nieuwe klantrecord voor elke gebruiker gemaakt in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ab892-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="ab892-120">Deze klantrecord wordt ook toegevoegd aan de relevante klanthiërarchierecord voor de zakenpartner en heeft de rol van een 'gebruiker'.</span><span class="sxs-lookup"><span data-stu-id="ab892-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="ab892-121">In de meeste gevallen moeten de bijbehorende eigenschapswaarden van alle klantrecords in een hiërarchie overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="ab892-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="ab892-122">Omdat alle gebruikers van zakenpartners bijvoorbeeld gelijksoortige prijzen voor producten moeten hebben, moeten hun prijsgroep en gekoppelde configuraties overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="ab892-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="ab892-123">Deze consistentie wordt echter niet door het systeem afgedwongen.</span><span class="sxs-lookup"><span data-stu-id="ab892-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="ab892-124">De relevante gebruikers van Commerce Headquarters moeten er daarom voor zorgen dat de eigenschapswaarden en configuraties overeenkomen voor alle klanten in een bepaalde hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="ab892-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="ab892-125">Gebruikers van Commerce Headquarters kunnen de eigenschapswaarden voor alle klantrecords in de hiërarchie naast elkaar bekijken.</span><span class="sxs-lookup"><span data-stu-id="ab892-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="ab892-126">Selecteer de relevante eigenschappen van de klantrecords door de tabbladnamen te selecteren in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="ab892-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="ab892-127">Gebruikers kunnen de eigenschapswaarden rechtstreeks vanuit deze weergave weergeven en bewerken.</span><span class="sxs-lookup"><span data-stu-id="ab892-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="ab892-128">Als u ook alle waarden van de beheerderklantrecord wilt toepassen op alle gebruikersklantrecords, selecteert u **Overschrijven** in de klanthiërarchiedetails.</span><span class="sxs-lookup"><span data-stu-id="ab892-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab892-129">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="ab892-129">Additional resources</span></span>

[<span data-ttu-id="ab892-130">Een B2B-e-commercesite instellen</span><span class="sxs-lookup"><span data-stu-id="ab892-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="ab892-131">Gebruikers van zakenpartners op B2B-sites voor e-commerce beheren</span><span class="sxs-lookup"><span data-stu-id="ab892-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="ab892-132">De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites</span><span class="sxs-lookup"><span data-stu-id="ab892-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="ab892-133">De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites</span><span class="sxs-lookup"><span data-stu-id="ab892-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]