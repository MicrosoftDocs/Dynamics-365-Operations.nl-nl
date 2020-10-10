---
title: Automatisering van incassoproces
description: In dit onderwerp wordt beschreven hoe u strategieën voor het incassoproces instelt waarmee automatisch klantfacturen worden geïdentificeerd waarvoor een e-mailherinnering of incasso-activiteit (zoals een telefoongesprek) vereist is of een aanmaningsbrief naar de klant moet worden verzonden.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: db59bad2ed3caf38f22bd4d6059e57747d1d983f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760515"
---
# <a name="collections-process-automation"></a><span data-ttu-id="88d10-103">Automatisering van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-103">Collections process automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88d10-104">In dit onderwerp wordt beschreven hoe u strategieën voor het incassoproces instelt waarmee automatisch klantfacturen worden geïdentificeerd waarvoor een e-mailherinnering of incasso-activiteit (zoals een telefoongesprek) vereist is of een aanmaningsbrief naar de klant moet worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="88d10-104">This topic describes the process of setting up collections process strategies that automatically identify customer invoices that require an email reminder, collection activity (such as a phone call), or a collection letter to be sent to the customer.</span></span> 

<span data-ttu-id="88d10-105">Organisaties besteden veel tijd aan het doorzoeken van verouderde balansrapporten, klantrekeningen en openstaande facturen om te bepalen met welke klanten contact moet worden opgenomen over een openstaande factuur of een openstaand rekeningsaldo.</span><span class="sxs-lookup"><span data-stu-id="88d10-105">Organizations spend a significant amount of time researching aged balance reports, customer accounts, and open invoices to determine which customers need to be contacted about an open invoice or account balance.</span></span> <span data-ttu-id="88d10-106">Dit onderzoek kost tijd die de incassomedewerker ook had kunnen besteden aan het communiceren met klanten om achterstallige saldi te innen of factuurgeschillen te verhelpen.</span><span class="sxs-lookup"><span data-stu-id="88d10-106">This research takes times away from a collection agent’s time spent communicating with customers to collect past due balances or resolving invoice disputes.</span></span> <span data-ttu-id="88d10-107">Door het incassoproces te automatiseren, kunt u een strategie instellen voor uw incassoproces.</span><span class="sxs-lookup"><span data-stu-id="88d10-107">Collections process automation lets you set up a strategy-based approach to your collection process.</span></span> <span data-ttu-id="88d10-108">Zo kunt u incasso-activiteiten consistent toepassen door aangepaste e-mailherinneringen of een geprogrammeerd proces voor het verzenden van aanmaningen te bieden.</span><span class="sxs-lookup"><span data-stu-id="88d10-108">This helps you apply collection activities consistently by providing customized email reminders, or programmed process for sending collection letters.</span></span> 

## <a name="collections-process-setup"></a><span data-ttu-id="88d10-109">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-109">Collections process setup</span></span>
<span data-ttu-id="88d10-110">U kunt de pagina **Instelling van incassoproces** (**Crediteringen en aanmaningen > Instellingen > Instelling van incassoproces**) gebruiken om een automatisch incassoproces te maken waarmee activiteiten worden gepland, e-mailberichten worden verzonden en klantaanmaningen worden gemaakt en geboekt.</span><span class="sxs-lookup"><span data-stu-id="88d10-110">You can use the **Collections process setup** page (**Credit and collections > Setup > Collections process setup**) to create an automated collections process that will schedule activities, send email messages, and create and post customer collection letters.</span></span> <span data-ttu-id="88d10-111">De processtappen zijn gebaseerd op de leidende of oudste openstaande factuur.</span><span class="sxs-lookup"><span data-stu-id="88d10-111">The process steps are based on the leading or oldest open invoice.</span></span> <span data-ttu-id="88d10-112">In elke stap wordt deze factuur gebruikt om te bepalen welke communicatie of activiteit voor een bepaalde klant moet plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="88d10-112">Each step uses this invoice to determine what communication or activity should take place with a specific customer.</span></span>  

### <a name="process-hierarchy"></a><span data-ttu-id="88d10-113">Proceshiërarchie</span><span class="sxs-lookup"><span data-stu-id="88d10-113">Process hierarchy</span></span>
<span data-ttu-id="88d10-114">Elke klantverzameling kan slechts aan één proceshiërarchie worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="88d10-114">Each customer pool can only be assigned to one process hierarchy.</span></span> <span data-ttu-id="88d10-115">De hiërarchiepositie van deze stap geeft aan welk proces prioriteit krijgt als een klant is opgenomen in meerdere verzamelingen waaraan een proceshiërarchie is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="88d10-115">The hierarchy rank of this step identifies which process will take precedence if a customer is included in more than one pool that has a process hierarchy assigned.</span></span> <span data-ttu-id="88d10-116">De verzameling-id bepaalt welke klanten worden toegewezen aan het proces.</span><span class="sxs-lookup"><span data-stu-id="88d10-116">The pool ID determines which customers will be assigned to the process.</span></span> 

<span data-ttu-id="88d10-117">De stille dagen worden gebruikt om ervoor te zorgen dat niet te vaak contact met een klant wordt opgenomen door het geautomatiseerde proces.</span><span class="sxs-lookup"><span data-stu-id="88d10-117">The quiet days are used to ensure that a customer does not get contacted too frequently by the automated process.</span></span>  <span data-ttu-id="88d10-118">Als het aantal stille dagen bijvoorbeeld op twee is ingesteld, wordt door het geautomatiseerde proces gedurende ten minste twee dagen geen contact met de klant gemaakt, ook niet als de oorspronkelijke leidende factuur volledig is vereffend.</span><span class="sxs-lookup"><span data-stu-id="88d10-118">For example, if the quiet days are set to two, a customer will not be contacted by the automated process for at least two days, even if the original leading invoice has been settled in full.</span></span> 

<span data-ttu-id="88d10-119">Als u klanten wilt uitsluiten van de procesautomatisering als het rekeningsaldo of factuursaldo lager is dan een gedefinieerde waarde, stelt u het veld **Uitsluiten van proces** in op **Ja** en voert u de waarde van het bedrag in.</span><span class="sxs-lookup"><span data-stu-id="88d10-119">To exclude customers from the process automation if the account balance or invoice balance is less than a defined value, set the **Exclude from process** field to **Yes** and enter the amount value.</span></span>

## <a name="process-details"></a><span data-ttu-id="88d10-120">Procesgegevens</span><span class="sxs-lookup"><span data-stu-id="88d10-120">Process details</span></span>
<span data-ttu-id="88d10-121">**Beschrijving** wordt gebruikt om het doel of de naam van de stap in de hiërarchie aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="88d10-121">**Description** is used to identify the purpose or name of the step in the hierarchy.</span></span>

<span data-ttu-id="88d10-122">**Actietype** bepaalt of met de stap een activiteit wordt gemaakt, een e-mailbericht wordt verzonden of een aanmaning wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="88d10-122">**Action type** defines if the step will create an activity, send an email, or create a collection letter.</span></span>

<span data-ttu-id="88d10-123">**Bedrijfsdocument** bepaalt welke sjabloon wordt gebruikt om het actietype te maken.</span><span class="sxs-lookup"><span data-stu-id="88d10-123">**Business document** defines the template used to create the action type.</span></span>  <span data-ttu-id="88d10-124">Dit kan een sjabloon voor een activiteit, een e-mailsjabloon of een aanmaning per klant zijn.</span><span class="sxs-lookup"><span data-stu-id="88d10-124">This can be an activity template, an email template, or a collection letter per customer.</span></span> 

<span data-ttu-id="88d10-125">De actietypen kunnen worden gemaakt voor of na de vervaldatum van de factuur, gebaseerd op de instelling die wordt weergegeven in de kolom **Dagen in relatie tot vervaldatum factuur**.</span><span class="sxs-lookup"><span data-stu-id="88d10-125">The action types can be created on either before or after the invoice due date, based on the setting that's displayed in the **Days in relation to the invoice due date** column.</span></span>

<span data-ttu-id="88d10-126">Wanneer u een actietype voor e-mail selecteert, wordt de ontvanger gebruikt om te bepalen of het een contactpersoon voor een klant, verkoopgroep of incassomedewerker is.</span><span class="sxs-lookup"><span data-stu-id="88d10-126">When you select an email action type, the recipient will be used to define if that is a customer, sales group, or collections agent contact.</span></span> <span data-ttu-id="88d10-127">De waarde in het veld **Contactpersoon voor zakelijk doel** bepaalt vervolgens welke contactpersoon van de account van die klant de communicatie ontvangt.</span><span class="sxs-lookup"><span data-stu-id="88d10-127">The value in the **Business purpose contact** field will then determine which contact from that customer's account will receive the communication.</span></span>

## <a name="business-document-details"></a><span data-ttu-id="88d10-128">Bedrijfsdocumentdetails</span><span class="sxs-lookup"><span data-stu-id="88d10-128">Business document details</span></span>
<span data-ttu-id="88d10-129">De details van bedrijfsdocumenten zijn afhankelijk van het actietype dat is geselecteerd in de procesdetails.</span><span class="sxs-lookup"><span data-stu-id="88d10-129">The business document details will vary based on the action type that's selected in the process details.</span></span>  <span data-ttu-id="88d10-130">Wanneer het actietype een activiteit is, worden de details van de activiteitsjabloon weergegeven.</span><span class="sxs-lookup"><span data-stu-id="88d10-130">When the action type is an activity, the activity template details will be shown.</span></span>  <span data-ttu-id="88d10-131">Deze gegevens omvatten de naam van de activiteitsjabloon, het type activiteit dat wordt gemaakt, het doel van de activiteit, het aantal dagen dat is gepland om de activiteit te voltooien en de details van de activiteit.</span><span class="sxs-lookup"><span data-stu-id="88d10-131">These details include the activity template name, the type of activity that will be created, the purpose of the activity, the number of days scheduled to complete the activity, and the details of the activity.</span></span>  <span data-ttu-id="88d10-132">Deze activiteit wordt vervolgens gekoppeld aan de leidende factuur die de ontvanger vertelt over de actie die nodig is om de activiteit te voltooien.</span><span class="sxs-lookup"><span data-stu-id="88d10-132">This activity will then link to the leading invoice that tells the recipient of the action that’s needed to complete the activity.</span></span>

<span data-ttu-id="88d10-133">Als het actietype een e-mailbericht in de procesgegevens is, bevat deze sectie twee sneltabbladen.</span><span class="sxs-lookup"><span data-stu-id="88d10-133">If the action type is an email in the process details, this section will contain two FastTabs.</span></span>  <span data-ttu-id="88d10-134">Het eerste wordt gebruikt voor het definiëren van de sjabloon-id, e-mailbeschrijving, standaardtaal, de gebruikersnaam die wordt toegewezen aan e-mailberichten die automatisch worden verzonden en het e-mailadres van de gekoppelde afzenders.</span><span class="sxs-lookup"><span data-stu-id="88d10-134">The first is used to define the template ID, email description, default language, the user name that will be assigned to email messages that are automatically sent, and the associated senders email address.</span></span> <span data-ttu-id="88d10-135">Op het tweede sneltabblad kan de hoofdtekst van het e-mailbericht worden gemaakt nadat de waarden in de velden **Taal** en **Onderwerp** zijn opgeslagen via **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="88d10-135">The second will allow the body of the email to be created after the values in the **Language** and **Subject** fields are saved by selecting **Edit**.</span></span>  <span data-ttu-id="88d10-136">Hierdoor wordt een venster geopend waarin HTML-inhoud kan worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="88d10-136">This will open a window that allows HTML content to be uploaded.</span></span> <span data-ttu-id="88d10-137">U kunt ook het bericht typen dat handmatig wordt gemaakt in het vak linksonder in het venster.</span><span class="sxs-lookup"><span data-stu-id="88d10-137">You can also type the message that’s created manually in the lower left box of the window.</span></span>  

> [!Note]
> <span data-ttu-id="88d10-138">U kunt een e-mailbericht van Outlook opslaan met de gewenste hoofdtekst van de communicatie in HTML-indeling.</span><span class="sxs-lookup"><span data-stu-id="88d10-138">An Outlook email can be saved with the desired body of the communication in HTML format.</span></span> <span data-ttu-id="88d10-139">Deze kan vervolgens worden geüpload om de sjabloon te implementeren.</span><span class="sxs-lookup"><span data-stu-id="88d10-139">This can then be uploaded to implement the template.</span></span> <br> <br> <span data-ttu-id="88d10-140">Als het actietype Aanmaning is geselecteerd, bevat het instellingenformulier geen sectie voor bedrijfsdocumentdetails.</span><span class="sxs-lookup"><span data-stu-id="88d10-140">If the action type of collection letter is selected there will not be a business document detail section on the setup form.</span></span>


## <a name="fasttab-reference"></a><span data-ttu-id="88d10-141">Verwijzing sneltabblad</span><span class="sxs-lookup"><span data-stu-id="88d10-141">FastTab reference</span></span>
<span data-ttu-id="88d10-142">In de volgende tabellen worden de pagina's en velden weergegeven waar de opgegeven sneltabbladen kunnen worden geopend. Daarnaast wordt een beschrijving gegeven van de informatie op dat tabblad.</span><span class="sxs-lookup"><span data-stu-id="88d10-142">The following tables list the pages and fields that the specified FastTabs can be accessed from, along with a description of the information in that tab.</span></span> 

### <a name="process-hierarchy"></a><span data-ttu-id="88d10-143">Proceshiërarchie</span><span class="sxs-lookup"><span data-stu-id="88d10-143">Process hierarchy</span></span>

|     <span data-ttu-id="88d10-144">Pagina</span><span class="sxs-lookup"><span data-stu-id="88d10-144">Page</span></span>                                                  |     <span data-ttu-id="88d10-145">Veld</span><span class="sxs-lookup"><span data-stu-id="88d10-145">Field</span></span>                         |     <span data-ttu-id="88d10-146">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88d10-146">Description</span></span>                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     <span data-ttu-id="88d10-147">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-147">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-148">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-148">Process automation</span></span>       |                                   |     <span data-ttu-id="88d10-149">Incassoprocessen maken en beheren op basis van toewijzingen van klantverzamelingen.</span><span class="sxs-lookup"><span data-stu-id="88d10-149">Create and   manage collections processes based on customer pool assignments.</span></span>                                                                                                                             |
|     <span data-ttu-id="88d10-150">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-150">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-151">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-151">Process automation</span></span>       |     <span data-ttu-id="88d10-152">Hiërarchie</span><span class="sxs-lookup"><span data-stu-id="88d10-152">Hierarchy</span></span>                     |     <span data-ttu-id="88d10-153">Definieert de prioriteit van procesautomatisering om een klant toe te wijzen als deze deel uitmaakt van meerdere verzamelingen.</span><span class="sxs-lookup"><span data-stu-id="88d10-153">Defines the   priority of process automation to assign a customer if they belong in multiple pools.</span></span>                                                                                                   |
|     <span data-ttu-id="88d10-154">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-154">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-155">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-155">Process automation</span></span>       |     <span data-ttu-id="88d10-156">Groeps-ID</span><span class="sxs-lookup"><span data-stu-id="88d10-156">Pool ID</span></span>                       |     <span data-ttu-id="88d10-157">Query's waarmee een groep klantrecords wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="88d10-157">Queries that   define a group of customer records.</span></span>                                                                                                                                                        |
|     <span data-ttu-id="88d10-158">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-158">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-159">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-159">Process automation</span></span>       |     <span data-ttu-id="88d10-160">Stiltedagen</span><span class="sxs-lookup"><span data-stu-id="88d10-160">Quiet days</span></span>                    |     <span data-ttu-id="88d10-161">Beperken hoe vaak een processtap kan worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="88d10-161">Limit how frequently a process step can be completed.</span></span> <span data-ttu-id="88d10-162">Als er bijvoorbeeld twee stille dagen zijn ingesteld, wordt de volgende processtap ten minste twee dagen niet uitgevoerd als de leidende factuur verandert.</span><span class="sxs-lookup"><span data-stu-id="88d10-162">For example, if two quiet days are set the next process step will not   occur for at least two days if the leading invoice changes.</span></span>     |
|     <span data-ttu-id="88d10-163">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-163">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-164">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-164">Process automation</span></span>       |     <span data-ttu-id="88d10-165">Uitsluiten van proces</span><span class="sxs-lookup"><span data-stu-id="88d10-165">Exclude from   Process</span></span>        |     <span data-ttu-id="88d10-166">Wanneer **Naar ouderdom gerangschikt saldo van klant kleiner dan** of **Factuurbedrag kleiner dan** wordt geselecteerd, wordt een klant van de procesautomatisering uitgesloten als niet aan de waardecriteria wordt voldaan.</span><span class="sxs-lookup"><span data-stu-id="88d10-166">Selecting either **Customer aging balance less than** or **Invoice amount less than** will exclude a customer from the process automation if the value criteria is not met.</span></span>                                   |

### <a name="process-details"></a><span data-ttu-id="88d10-167">Procesgegevens</span><span class="sxs-lookup"><span data-stu-id="88d10-167">Process details</span></span>
|     <span data-ttu-id="88d10-168">Pagina</span><span class="sxs-lookup"><span data-stu-id="88d10-168">Page</span></span>                                                  |     <span data-ttu-id="88d10-169">Veld</span><span class="sxs-lookup"><span data-stu-id="88d10-169">Field</span></span>                                         |      <span data-ttu-id="88d10-170">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88d10-170">Description</span></span>                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     <span data-ttu-id="88d10-171">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-171">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-172">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-172">Process automation</span></span>       |                                                   |     <span data-ttu-id="88d10-173">De stappen definiëren die zijn uitgevoerd op basis van de leidende factuur.</span><span class="sxs-lookup"><span data-stu-id="88d10-173">Define the steps   taken based on the leading invoice.</span></span>                                                                                                |
|                                                           |     <span data-ttu-id="88d10-174">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88d10-174">Description</span></span>                                   |     <span data-ttu-id="88d10-175">Vrije-tekstveld dat wordt gebruikt om een naam en/of beschrijving van de stap op te geven.</span><span class="sxs-lookup"><span data-stu-id="88d10-175">Free text   field used for providing a name and/or description of the step.</span></span>                                                                           |
|                                                           |     <span data-ttu-id="88d10-176">Actietype</span><span class="sxs-lookup"><span data-stu-id="88d10-176">Action type</span></span>                                   |     <span data-ttu-id="88d10-177">Activiteit, e-mail of aanmaning die wordt gemaakt door de processtap.</span><span class="sxs-lookup"><span data-stu-id="88d10-177">Activity,   email, or collection letter that will be created by the process step.</span></span>                                                                     |
|                                                           |     <span data-ttu-id="88d10-178">Bedrijfsdocument</span><span class="sxs-lookup"><span data-stu-id="88d10-178">Business   document</span></span>                           |     <span data-ttu-id="88d10-179">De activiteit of e-mailsjabloon die tijdens de processtap wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="88d10-179">Defines the   activity or email template that is used during the process step.</span></span>                                                                        |
|                                                           |     <span data-ttu-id="88d10-180">Wanneer</span><span class="sxs-lookup"><span data-stu-id="88d10-180">When</span></span>                                          |     <span data-ttu-id="88d10-181">Definieert of de processtap vóór of na de vervaldatum van de leidende factuur plaatsvindt, in combinatie met het veld **Dagen in relatie tot vervaldatum factuur**.</span><span class="sxs-lookup"><span data-stu-id="88d10-181">Defines if   the process step will occur before or after the leading invoice due date   along with the **Days in relation to invoice due date** field.</span></span>        |
|                                                           |     <span data-ttu-id="88d10-182">Dagen in relatie tot vervaldatum factuur</span><span class="sxs-lookup"><span data-stu-id="88d10-182">Days in   relation to invoice due date</span></span>        |     <span data-ttu-id="88d10-183">In combinatie met het veld **Wanneer** wordt hiermee de timing van de processtap aangegeven.</span><span class="sxs-lookup"><span data-stu-id="88d10-183">Together   with the **When** field it identifies the timing of the process step.</span></span>                                                                          |
|                                                           |     <span data-ttu-id="88d10-184">Ontvanger</span><span class="sxs-lookup"><span data-stu-id="88d10-184">Recipient</span></span>                                     |     <span data-ttu-id="88d10-185">Geeft aan of een e-mailbericht wordt verzonden naar een contactpersoon voor een klant, verkoopgroep of incassomedewerker.</span><span class="sxs-lookup"><span data-stu-id="88d10-185">Identifies   if an email will be sent to a Customer, Sales group, or Collections Agent contact.</span></span>                                                   |
|                                                           |     <span data-ttu-id="88d10-186">Contactpersoon voor zakelijke doel</span><span class="sxs-lookup"><span data-stu-id="88d10-186">Business   purpose contact</span></span>                    |     <span data-ttu-id="88d10-187">Bepaalt welk e-mailadres van de geadresseerde wordt gebruikt bij e-mailcommunicatie.</span><span class="sxs-lookup"><span data-stu-id="88d10-187">Determines   which recipient’s email address is used in email communications.</span></span>                                                                                 |

### <a name="business-process-activity-template-details"></a><span data-ttu-id="88d10-188">Details van activiteitensjabloon voor bedrijfsproces</span><span class="sxs-lookup"><span data-stu-id="88d10-188">Business process activity template details</span></span> 
|     <span data-ttu-id="88d10-189">Pagina</span><span class="sxs-lookup"><span data-stu-id="88d10-189">Page</span></span>                                                  |     <span data-ttu-id="88d10-190">Veld</span><span class="sxs-lookup"><span data-stu-id="88d10-190">Field</span></span>                     |      <span data-ttu-id="88d10-191">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88d10-191">Description</span></span>                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     <span data-ttu-id="88d10-192">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-192">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-193">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-193">Process automation</span></span>       |                               |     <span data-ttu-id="88d10-194">De sectie van het instellingsproces waarmee de details van de activiteitensjabloon worden aangegeven.</span><span class="sxs-lookup"><span data-stu-id="88d10-194">Section of   the setup process that identifies the details of the activity template.</span></span>                                                                      |
|     <span data-ttu-id="88d10-195">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-195">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-196">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-196">Process automation</span></span>       |     <span data-ttu-id="88d10-197">Activiteitensjabloon</span><span class="sxs-lookup"><span data-stu-id="88d10-197">Activity   template</span></span>       |     <span data-ttu-id="88d10-198">Identificeert het type, het doel en het aantal dagen voor voltooiing en biedt details over de activiteit die wordt gemaakt tijdens een activiteitenprocesstap.</span><span class="sxs-lookup"><span data-stu-id="88d10-198">Identifies   the type, purpose, number of days to complete, and provides details about the   activity that will be created during an activity process step.</span></span>       |

### <a name="business-document-email-template-details"></a><span data-ttu-id="88d10-199">Details van e-mailsjabloon voor bedrijfsdocument</span><span class="sxs-lookup"><span data-stu-id="88d10-199">Business document email template details</span></span> 
|     <span data-ttu-id="88d10-200">Pagina</span><span class="sxs-lookup"><span data-stu-id="88d10-200">Page</span></span>                                                  |     <span data-ttu-id="88d10-201">Veld</span><span class="sxs-lookup"><span data-stu-id="88d10-201">Field</span></span>     |      <span data-ttu-id="88d10-202">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88d10-202">Description</span></span>                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     <span data-ttu-id="88d10-203">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-203">Collections   process setup</span></span> <br> <span data-ttu-id="88d10-204">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-204">Process automation</span></span>       |               |     <span data-ttu-id="88d10-205">Identificeert de e-mail beschrijving, de standaardtaal, de afzendernaam en het e-mailadres dat wordt gemaakt tijdens een e-mailprocesstap.</span><span class="sxs-lookup"><span data-stu-id="88d10-205">Identifies   the email description, default language, senders name, and email address that will be   created during an email process step.</span></span>        |


### <a name="collections-history"></a><span data-ttu-id="88d10-206">Aanmaningshistorie</span><span class="sxs-lookup"><span data-stu-id="88d10-206">Collections history</span></span> 
|     <span data-ttu-id="88d10-207">Pagina</span><span class="sxs-lookup"><span data-stu-id="88d10-207">Page</span></span>                              |     <span data-ttu-id="88d10-208">Veld</span><span class="sxs-lookup"><span data-stu-id="88d10-208">Field</span></span>     |      <span data-ttu-id="88d10-209">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88d10-209">Description</span></span>                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     <span data-ttu-id="88d10-210">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-210">Collections   process setup</span></span>       |               |     <span data-ttu-id="88d10-211">De recente historie van de geselecteerde proceshiërarchie.</span><span class="sxs-lookup"><span data-stu-id="88d10-211">View the   recent history for the selected process hierarchy.</span></span>     |

### <a name="collection-process-assignment"></a><span data-ttu-id="88d10-212">Toewijzing van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-212">Collection process assignment</span></span>
|     <span data-ttu-id="88d10-213">Pagina</span><span class="sxs-lookup"><span data-stu-id="88d10-213">Page</span></span>                              |     <span data-ttu-id="88d10-214">Veld</span><span class="sxs-lookup"><span data-stu-id="88d10-214">Field</span></span>     |      <span data-ttu-id="88d10-215">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88d10-215">Description</span></span>                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     <span data-ttu-id="88d10-216">Instelling van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-216">Collections   process setup</span></span>       |               |     <span data-ttu-id="88d10-217">Klanten weergeven die aan een incassoproces zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="88d10-217">View   customers assigned to a collections process.</span></span>  
|     <span data-ttu-id="88d10-218">Handmatige toewijzing</span><span class="sxs-lookup"><span data-stu-id="88d10-218">Manual assignment</span></span>               |               |     <span data-ttu-id="88d10-219">Klanten weergeven die handmatig aan een proces zijn toegewezen of klanten selecteren die aan een proces moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="88d10-219">View customers that have been manually assigned to a process or select customers to be assigned to a process.</span></span> |
|     <span data-ttu-id="88d10-220">Preview procestoewijzing</span><span class="sxs-lookup"><span data-stu-id="88d10-220">Preview process assignment</span></span>      |               |     <span data-ttu-id="88d10-221">Een voorbeeld weergeven van de klanten die aan een strategie worden toegewezen wanneer deze wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="88d10-221">Preview the customers that will be assigned to a strategy when it is run.</span></span>   |
|     <span data-ttu-id="88d10-222">Preview van klanttoewijzing</span><span class="sxs-lookup"><span data-stu-id="88d10-222">Preview customer assignment</span></span>     |               |     <span data-ttu-id="88d10-223">De strategie weergeven waaraan een bepaalde klant is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="88d10-223">View the strategy that a specific customer is assigned.</span></span>    |
 
### <a name="parameters"></a><span data-ttu-id="88d10-224">Parameters</span><span class="sxs-lookup"><span data-stu-id="88d10-224">Parameters</span></span>
|     <span data-ttu-id="88d10-225">Pagina</span><span class="sxs-lookup"><span data-stu-id="88d10-225">Page</span></span>                                                                  |     <span data-ttu-id="88d10-226">Veld</span><span class="sxs-lookup"><span data-stu-id="88d10-226">Field</span></span>                                             |      <span data-ttu-id="88d10-227">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88d10-227">Description</span></span>                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     <span data-ttu-id="88d10-228">Parameters van module Klanten > Automatisering van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-228">Accounts   receivable parameters > Collections process automation</span></span>     |     <span data-ttu-id="88d10-229">Percentage klanten per batchtaak</span><span class="sxs-lookup"><span data-stu-id="88d10-229">Percentage   of customers per batch task</span></span>          |     <span data-ttu-id="88d10-230">Instellen om het aantal batchtaken per automatiseringsproces te bepalen.</span><span class="sxs-lookup"><span data-stu-id="88d10-230">Setting to   determine the number of batch tasks per automation process.</span></span>                                          |
|     <span data-ttu-id="88d10-231">Parameters van module Klanten > Automatisering van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-231">Accounts   receivable parameters > Collections process automation</span></span>     |     <span data-ttu-id="88d10-232">Aanmaningen automatisch boeken</span><span class="sxs-lookup"><span data-stu-id="88d10-232">Post   Collection letters automatically</span></span>           |     <span data-ttu-id="88d10-233">Actietypen voor aanmaningen boeken de brief tijdens het automatiseren.</span><span class="sxs-lookup"><span data-stu-id="88d10-233">Collection   letter action types will post the letter during the automation.</span></span>                                      |
|     <span data-ttu-id="88d10-234">Parameters van module Klanten > Automatisering van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-234">Accounts   receivable parameters > Collections process automation</span></span>     |     <span data-ttu-id="88d10-235">Activiteiten maken voor automatisering</span><span class="sxs-lookup"><span data-stu-id="88d10-235">Create   activities for automation</span></span>                |     <span data-ttu-id="88d10-236">Activiteiten maken en sluiten voor actietypen voor niet-activiteiten om alle geautomatiseerde stappen voor een rekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="88d10-236">Create and   close activities for non-activity action types to view all automated steps   taken on an account.</span></span>        |
|     <span data-ttu-id="88d10-237">Parameters van module Klanten > Automatisering van incassoproces</span><span class="sxs-lookup"><span data-stu-id="88d10-237">Accounts   receivable parameters > Collections process automation</span></span>     |     <span data-ttu-id="88d10-238">Aantal dagen om automatisering van incassoproces te behouden</span><span class="sxs-lookup"><span data-stu-id="88d10-238">Days to keep   collections process automation</span></span>     |     <span data-ttu-id="88d10-239">Het aantal dagen dat de incassogeschiedenis wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="88d10-239">Defines the   number of days collections history is stored.</span></span>                                                       |