---
title: Toeslagen voor niet-conformeringsbewerkingen
description: In dit onderwerp wordt beschreven hoe u kwaliteitstoeslagen kunt maken die kunnen worden gebruikt met bewerkingen voor een niet-conformering.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956607"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="6f6ed-103">Toeslagen voor niet-conformeringsbewerkingen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f6ed-104">In dit onderwerp wordt beschreven hoe u kwaliteitstoeslagen kunt maken die kunnen worden gebruikt met bewerkingen voor een niet-conformering.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="6f6ed-105">U gebruikt de pagina **Kwaliteitstoeslagen** om de typen toeslagen te definiëren die aan bewerkingen voor een niet-conformering kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="6f6ed-106">Met toeslagen kunt u details bijhouden over kosten of toeslagen die u een klant verschuldigd bent voor niet-overeenkomende producten of die een leverancier u verschuldigd is voor niet-overeenkomende producten die u hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="6f6ed-107">U kunt toeslagen ook gebruiken om kosten bij te houden die vereist zijn voor externe leveranciers of services om een bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="6f6ed-108">Voorbeelden van kwaliteitstoeslagen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-108">Examples of quality charges</span></span>

<span data-ttu-id="6f6ed-109">U werkt voor een productiebedrijf.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-109">You work for a manufacturing company.</span></span> <span data-ttu-id="6f6ed-110">Uw bedrijf heeft contracten met verschillende leveranciers.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="6f6ed-111">Deze contracten geven de standaarden voor de tijdige verzending, schade en productkwaliteit voor artikelen aan.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="6f6ed-112">Ook hebben verschillende van uw klanten overeenkomsten met uw bedrijf over retouren, schade en productkwaliteit.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="6f6ed-113">Er wordt een onkostenstructuur gedefinieerd voor elke situatie die wordt opgegeven in het contract.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="6f6ed-114">U kunt kwaliteitstoeslagen configureren om de verschillende typen toeslagen aan te geven, zoals *Schade*, *Late verzending* en *Kwaliteit*.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="6f6ed-115">Wanneer u vervolgens een niet-conformering maakt, voegt u een of meer bewerkingen toe.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="6f6ed-116">Voor elke bewerking selecteert u **Toeslagen** om de details van de kosten te definiëren.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="6f6ed-117">Een kwaliteitstoeslag maken</span><span class="sxs-lookup"><span data-stu-id="6f6ed-117">Create a quality charge</span></span>

1. <span data-ttu-id="6f6ed-118">Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Kwaliteitstoeslagen**.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="6f6ed-119">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6f6ed-120">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="6f6ed-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6f6ed-121">**Toeslagencode**: voer een unieke id of naam voor de kwaliteitstoeslag in.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="6f6ed-122">**Beschrijving**: voer een gedetailleerde beschrijving voor de kwaliteitstoeslag in.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="6f6ed-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="6f6ed-124">Een kwaliteitscontrole toevoegen aan een bewerking voor een niet-conformering</span><span class="sxs-lookup"><span data-stu-id="6f6ed-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="6f6ed-125">Zie [Bewerkingen voor niet-conformeringen](quality-operations.md) voor meer informatie over het toevoegen van bewerkingen aan een niet-conformering en het toepassen van toeslagen op deze bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="6f6ed-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f6ed-126">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-126">Additional resources</span></span>

- [<span data-ttu-id="6f6ed-127">Overzicht van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="6f6ed-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="6f6ed-128">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="6f6ed-129">Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="6f6ed-130">Quarantainezones voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="6f6ed-131">Typen diagnosen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="6f6ed-132">Kwaliteitstoeslagen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="6f6ed-133">Bewerkingen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="6f6ed-134">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="6f6ed-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
