---
title: Algemene journaalverwerking
description: In dit artikel worden de mogelijkheden beschreven in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, waarmee algemene journaalverwerking eenvoudiger wordt en die ook helpen waarborgen dat de juiste gegevens worden vastgelegd en dat er geen inbreuk wordt gemaakt op de interne controle.
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 68da281cb4793ed83f70c68d061d327aa8a8c772
ms.contentlocale: nl-nl
ms.lasthandoff: 08/01/2017

---

# <a name="general-journal-processing"></a><span data-ttu-id="5f9e2-103">Algemene journaalverwerking</span><span class="sxs-lookup"><span data-stu-id="5f9e2-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5f9e2-104">In dit artikel worden de mogelijkheden beschreven in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, waarmee algemene journaalverwerking eenvoudiger wordt en die ook helpen waarborgen dat de juiste gegevens worden vastgelegd en dat er geen inbreuk wordt gemaakt op de interne controle.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="5f9e2-105">Journaalnamen</span><span class="sxs-lookup"><span data-stu-id="5f9e2-105">Journal names</span></span>

<span data-ttu-id="5f9e2-106">Een van de belangrijkste in te stellen gebieden is Journaalnamen.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="5f9e2-107">Het is verstandig om specifieke journaalnamen te definiëren voor elk doel, zoals intercompany, correctie toerekening en correctie van fouten.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="5f9e2-108">U kunt elke journaalnaam aanpassen om invoer van gegevens voor elk doel gemakkelijker en veiliger te maken.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="5f9e2-109">Op de pagina **Journaalnamen** kunt u de volgende elementen instellen:</span><span class="sxs-lookup"><span data-stu-id="5f9e2-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="5f9e2-110">**Goedkeuring workflow** - Om interne controle te verhogen, definieert u journaalworkflows die materiaallimieten vastleggen voor controle- en goedkeuringsstappen, op basis van criteria zoals totale debetbedrag wordt gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="5f9e2-111">U stelt workflows voor de algemene journalen in op de pagina **Grootboekworkflows**.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="5f9e2-112">**Standaardwaarden** - Selecteer standaardwaarden voor tegenrekeningen, valuta en financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="5f9e2-113">**Journaalcontrole** - U kunt beperkingen instellen op het bedrijf en het rekeningtype, en ook de segmentwaarden.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="5f9e2-114">**Voorbeelden**</span><span class="sxs-lookup"><span data-stu-id="5f9e2-114">**Examples**</span></span>

<span data-ttu-id="5f9e2-115">U kunt een journaalnaam alleen gebruiken voor correcties.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="5f9e2-116">In dit geval kunt u opgeven dat alleen het rekeningtype **Grootboek** geldig is voor alle bedrijven.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="5f9e2-117">[![Rekeningtypen voor journaalcontrole](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="5f9e2-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="5f9e2-118">Een journaalnaam kan alleen worden gebruikt voor een specifiek segment of voor een bereik voor hoofdrekeningen.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="5f9e2-119">[![Journaalcontrolesegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="5f9e2-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="5f9e2-120">De optie **Automatische omkering** is beschikbare in algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="5f9e2-121">U hebt bijvoorbeeld een toerekeningscorrectie waar het werkelijke document nog niet van is verwerkt, zoals in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="5f9e2-122">[![Omkering van algemeen journaal](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="5f9e2-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="5f9e2-123">De Microsoft Excel-invoegtoepassing voor journaalboeking biedt een extra niveau van automatisering en maakt gegevensinvoer eenvoudiger.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="5f9e2-124">De actie **Regels openen in Excel** is beschikbaar op de pagina's **Algemeen journaal** en **Journaalboekstuk**.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="5f9e2-125">Op de pagina **Periodieke journalen** kunt u terugkerende journalen instellen om journaalverwerking te automatiseren.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="5f9e2-126">U kunt boekstuksjablonen gebruiken op elk gewenst moment.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="5f9e2-127">Op de pagina **Algemene journalen** vindt u de acties **Opslaan** en **Boekstuksjabloon selecteren** op de pagina **Journaalboekstuk** onder **Functies** voor de boekstukregels.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="5f9e2-128">Verwante instellingen</span><span class="sxs-lookup"><span data-stu-id="5f9e2-128">Related setup</span></span>
<span data-ttu-id="5f9e2-129">De volgende instellingen zijn niet specifiek voor algemene journalen, maar helpen te garanderen dat de gegevensinvoer juist en eenvoudig is.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="5f9e2-130">Hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="5f9e2-130">Main account</span></span>

<span data-ttu-id="5f9e2-131">De instelling van de hoofdrekening biedt veel opties voor algemene journaalverwerking:</span><span class="sxs-lookup"><span data-stu-id="5f9e2-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="5f9e2-132">**DC/CR-behoefte** - Gebruik deze optie als een hoofdrekening is beperkt tot debet- of credittransacties.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="5f9e2-133">De instelling wordt geverifieerd wanneer een journaal is gevalideerd of geboekt.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="5f9e2-134">**Standaardtegenrekening**</span><span class="sxs-lookup"><span data-stu-id="5f9e2-134">**Default offset account**</span></span>
-   <span data-ttu-id="5f9e2-135">**Uitgesteld** - Stel een hoofdrekening uit voor gegevensinvoer over alle bedrijven of voor een bepaald bedrijf/bepaalde rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="5f9e2-136">**Handmatige invoer niet toestaan** - Voorkom dat gebruikers handmatig een waarde voor de rekening in journalen kunnen invoeren.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="5f9e2-137">**Standaard/Valuta valideren**</span><span class="sxs-lookup"><span data-stu-id="5f9e2-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="5f9e2-138">**Overschrijvingen rechtspersoon** - Deze instelling is specifiek voor het opgegeven bedrijf of de opgegeven rechtspersoon:</span><span class="sxs-lookup"><span data-stu-id="5f9e2-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="5f9e2-139">**Standaard/Btw valideren**</span><span class="sxs-lookup"><span data-stu-id="5f9e2-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="5f9e2-140">**Standaarddimensie** - **Niet vast** of **Vaste waarde**.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="5f9e2-141">**Vaste waarde** helpt om ervoor te zorgen dat alle boekingen voor deze hoofdrekening altijd elke dimensie gebruiken die is ingesteld op **Vast**.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="5f9e2-142">**Boekingsvalidatie**</span><span class="sxs-lookup"><span data-stu-id="5f9e2-142">**Posting validation**</span></span>
    -   <span data-ttu-id="5f9e2-143">**Gebruikersvalidatie** - Deze optie bepaalt welke gebruikers naar een hoofdrekening kunnen boeken.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="5f9e2-144">**Validatie van boekingstype** - Deze optie bepaalt welke boekingstypen voor een hoofdrekening zijn toegestaan.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="5f9e2-145">Boekhoudingsstructuren en geavanceerde regelsstructuren</span><span class="sxs-lookup"><span data-stu-id="5f9e2-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="5f9e2-146">Boekhoudingsstructuren en geavanceerde regelsstructuren zijn uiterst belangrijk voor het garanderen dat de gegevens die vereist zijn voor financiële rapportage en prestatie-opvolging worden vastgelegd tijdens de verwerking van het algemeen journaal en eventuele documentatie.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="5f9e2-147">Met boekhoudingsstructuren en geavanceerde regelsstructuren kunt u de gegevensinvoerervaring aanpassen.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="5f9e2-148">U kunt ervoor dat gegevens alleen kunnen worden ingevoerd voor financiële dimensies die in elke situatie relevant zijn, en u kunt ook de behoefte afdwingen dat altijd verplichte en juiste gegevens worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="5f9e2-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="5f9e2-149">Zie de volgende onderwerpen voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="5f9e2-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="5f9e2-150">[Planning: rekeningschema](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="5f9e2-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="5f9e2-151">Geavanceerde regels voor journalen maken</span><span class="sxs-lookup"><span data-stu-id="5f9e2-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="5f9e2-152">Een journaalboeking maken met een sjabloon</span><span class="sxs-lookup"><span data-stu-id="5f9e2-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="5f9e2-153">Journalen maken en valideren</span><span class="sxs-lookup"><span data-stu-id="5f9e2-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="5f9e2-154">Periodieke journalen boeken</span><span class="sxs-lookup"><span data-stu-id="5f9e2-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="5f9e2-155">Grootboektoewijzingsjournaal verwerken</span><span class="sxs-lookup"><span data-stu-id="5f9e2-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



