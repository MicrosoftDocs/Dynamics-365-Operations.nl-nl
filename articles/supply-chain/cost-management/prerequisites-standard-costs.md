---
title: Overzicht van Vereisten voor standaardkosten
description: In dit onderwerp worden de basisstappen voor het gebruik van standaardkosten besproken.
author: AndersGirke
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92f80ecc611e68210e24e59b696724e1bc9c3a06
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809657"
---
# <a name="prerequisites-for-standard-costs-overview"></a><span data-ttu-id="7116e-103">Overzicht van Vereisten voor standaardkosten</span><span class="sxs-lookup"><span data-stu-id="7116e-103">Prerequisites for standard costs overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7116e-104">In dit onderwerp worden de basisstappen voor het gebruik van standaardkosten besproken.</span><span class="sxs-lookup"><span data-stu-id="7116e-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="7116e-105">Volgende stappen zijn afhankelijk van de bedrijfsactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="7116e-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="7116e-106">De stappen verschillen bijvoorbeeld voor een niet-productieomgeving, een productieomgeving waarin routeringen niet worden gebruikt en een productieomgeving met routeringen.</span><span class="sxs-lookup"><span data-stu-id="7116e-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="7116e-107">Voer de onderstaande stappen uit om standaardkosten in te stellen.</span><span class="sxs-lookup"><span data-stu-id="7116e-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="7116e-108">**1. Maak een artikelmodelgroep voor standaardkosten.**</span><span class="sxs-lookup"><span data-stu-id="7116e-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="7116e-109">Gebruik de pagina **Artikelmodelgroepen** om een nieuwe groep voor standaardkosten te maken en om een voorraadmodel van **Standaardkosten** toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="7116e-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="7116e-110">De artikelmodelgroep moet een duidelijke id hebben, zoals **Stdkosten**.</span><span class="sxs-lookup"><span data-stu-id="7116e-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="7116e-111">Schakel de selectievakjes in om aan te geven dat de groep financiële negatieve voorraad moet toestaan en dat deze fysieke voorraad en financiële voorraad moet boeken.</span><span class="sxs-lookup"><span data-stu-id="7116e-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="7116e-112">Deze standaardkostengroep wordt aan artikelen toegewezen.</span><span class="sxs-lookup"><span data-stu-id="7116e-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="7116e-113">**2. Definieer grootboekrekeningen die aan standaardkostprijsafwijkingen zijn gekoppeld.**</span><span class="sxs-lookup"><span data-stu-id="7116e-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="7116e-114">Gebruik de pagina **Rekeningschema** om grootboekrekeningen te definiëren die zijn gekoppeld aan standaardkostprijsafwijkingen.</span><span class="sxs-lookup"><span data-stu-id="7116e-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="7116e-115">Deze grootboekrekeningen moeten worden gedefinieerd voordat ze kunnen worden toegewezen op de pagina **Boeking**.</span><span class="sxs-lookup"><span data-stu-id="7116e-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="7116e-116">De grootboekrekeningen kunnen artikelgroepen en kostengroepen reflecteren.</span><span class="sxs-lookup"><span data-stu-id="7116e-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="7116e-117">**3. Wijs grootboekrekeningen toe aan artikelboekingen die zijn gekoppeld aan standaardkostprijsafwijkingen.**</span><span class="sxs-lookup"><span data-stu-id="7116e-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="7116e-118">Gebruik de pagina **Boeking** om de grootboekrekeningen toe te wijzen die zijn gekoppeld aan standaardkostprijsafwijkingen.</span><span class="sxs-lookup"><span data-stu-id="7116e-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="7116e-119">U kunt een grootboekrekening van een afwijking per artikel (of artikelgroep) en per kostengroep (of kostengroeptype) opgeven of u kunt opgeven dat de grootboekrekening van toepassing is op alle artikelen en kostengroepen.</span><span class="sxs-lookup"><span data-stu-id="7116e-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="7116e-120">Deze opties komen overeen met de kostenrelaties voor tabellen, groepen en alles.</span><span class="sxs-lookup"><span data-stu-id="7116e-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="7116e-121">Voordat u artikelboekingsregels definieert, gebruikt u de pagina **Transactiecombinaties** om kostenrelaties (voor tabellen, groepen en alles) te activeren.</span><span class="sxs-lookup"><span data-stu-id="7116e-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="7116e-122">**4. Definieer voorraadparameters die aan standaardkosten zijn gekoppeld.**</span><span class="sxs-lookup"><span data-stu-id="7116e-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="7116e-123">Gebruik het tabblad **Voorraadboekhouding** op de pagina **Instelling voor boekhoudingbeleid voorraad > Parameters** voor het definiëren van twee kostenbeheerparameters die aan standaardkosten zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="7116e-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="7116e-124">Selecteer in het veld **Kostenanalyse** **Geen** of **Subgrootboek**.</span><span class="sxs-lookup"><span data-stu-id="7116e-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="7116e-125">Als u **Subgrootboek** selecteert, is de kostenanalyse een *actieve* kostenanalyse.</span><span class="sxs-lookup"><span data-stu-id="7116e-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="7116e-126">Een actieve kostenanalyse is cruciaal voor het berekenen, achterhalen en weergeven van kostengroepsegmentatie over een productstructuur op meerdere niveaus voor standaardkostenartikelen.</span><span class="sxs-lookup"><span data-stu-id="7116e-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="7116e-127">Wanneer de kostenanalyse actief is, kunt u voorraad, OHW (onderhanden werk) en kosten van verkochte goederen rapporteren en analyseren per kostengroep op één niveau, meerdere niveaus of totale indeling.</span><span class="sxs-lookup"><span data-stu-id="7116e-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="7116e-128">Wanneer de kostenanalyse actief is en u kosten van een gefabriceerd artikel activeert, wordt de kostengroepsegmentatie opgeslagen in de kostenrecord van het artikel.</span><span class="sxs-lookup"><span data-stu-id="7116e-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="7116e-129">Als u **Geen** selecteert wordt geen kostengroepsegmentatie onderhouden voor standaardkostenartikelen.</span><span class="sxs-lookup"><span data-stu-id="7116e-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="7116e-130">Met andere woorden: de standaardkosten van een gefabriceerd artikel worden berekend en onderhouden als één bedrag zonder kostengroepsegmentatie.</span><span class="sxs-lookup"><span data-stu-id="7116e-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="7116e-131">De kostenbijdragen van gefabriceerde onderdelen worden samengevoegd tot het ene bedrag.</span><span class="sxs-lookup"><span data-stu-id="7116e-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="7116e-132">Selecteer in het veld **Afwijkingen van standaard** **Samengevat** of **Per kostengroep**.</span><span class="sxs-lookup"><span data-stu-id="7116e-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="7116e-133">Als u **Per kostengroep** selecteert, kunt u inkoopprijsafwijkingen en productieafwijkingen per kostengroep identificeren.</span><span class="sxs-lookup"><span data-stu-id="7116e-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="7116e-134">U kunt ook de vier typen productieafwijkingen identificeren: partijgrootte, hoeveelheid, prijs en vervanging.</span><span class="sxs-lookup"><span data-stu-id="7116e-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="7116e-135">Als u **Samengevat** selecteert, kunt u geen afwijkingen per kostengroep identificeren en kunt u niet de vier typen productieafwijkingen identificeren.</span><span class="sxs-lookup"><span data-stu-id="7116e-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="7116e-136">U kunt alleen een samengevatte productieafwijking weergeven.</span><span class="sxs-lookup"><span data-stu-id="7116e-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="7116e-137">Het beleid voor afwijking op standaardkosten werkt onafhankelijk van het kostenanalysebeleid.</span><span class="sxs-lookup"><span data-stu-id="7116e-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="7116e-138">Met andere woorden: u kunt een kostenanalysebeleid van **geen** selecteren en afwijkingen per kostengroep selecteren, zodat productieafwijkingen per kostengroep toch worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="7116e-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="7116e-139">**5. Maak kostprijsberekeningsversies voor standaardkosten.**</span><span class="sxs-lookup"><span data-stu-id="7116e-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="7116e-140">Gebruik de pagina **Instellingen kostprijsberekeningsversie** om een of meer kostprijsberekeningsversies voor standaardkosten te maken.</span><span class="sxs-lookup"><span data-stu-id="7116e-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="7116e-141">Elke kostprijsberekeningsversie moet worden aangegeven door een kostprijsberekeningstype van **standaardkosten** en moet kostengegevens in de inhoud toestaan.</span><span class="sxs-lookup"><span data-stu-id="7116e-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="7116e-142">**6. Bereid een bestaande klant voor om standaardkosten te gebruiken.**</span><span class="sxs-lookup"><span data-stu-id="7116e-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="7116e-143">Klanten die hun bestaande artikelen naar een standaardkostenvoorraadmodel willen wijzigen, moeten de pagina **Standaardkostprijsconversies** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7116e-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="7116e-144">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="7116e-144">Related topics</span></span>
--------

[<span data-ttu-id="7116e-145">Overzicht van standaardkostprijsconversie</span><span class="sxs-lookup"><span data-stu-id="7116e-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="7116e-146">Weblogs</span><span class="sxs-lookup"><span data-stu-id="7116e-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="7116e-147">Community-blogs</span><span class="sxs-lookup"><span data-stu-id="7116e-147">Community blogs</span></span>

- [<span data-ttu-id="7116e-148">Hoe u standaardkosten instelt voor directe materialen in Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7116e-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="7116e-149">Standaard directe arbeidskosten in Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7116e-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]