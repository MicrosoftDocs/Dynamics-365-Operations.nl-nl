---
title: Nummerreeksen instellen op een individuele basis
description: In dit onderwerp wordt uitgelegd hoe op een individuele basis nummerreeksen kunnen worden ingesteld.
author: sericks007
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 818e641d19444e94a287134b68b25d52a05021d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189862"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a><span data-ttu-id="b49ef-103">Nummerreeksen instellen op een individuele basis</span><span class="sxs-lookup"><span data-stu-id="b49ef-103">Set up number sequences on an individual basis</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b49ef-104">In dit onderwerp wordt uitgelegd hoe op een individuele basis nummerreeksen kunnen worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="b49ef-104">This topic explains how to set up number sequences on an individual basis.</span></span> <span data-ttu-id="b49ef-105">Nummerreeksen worden gebruikt om leesbare, unieke identificaties te maken voor hoofdgegevensrecords en transactierecords die deze nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="b49ef-105">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="b49ef-106">Een hoofdgegevens- of transactieregistratie die een identificatie nodig heeft wordt een verwijzing genoemd.</span><span class="sxs-lookup"><span data-stu-id="b49ef-106">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="b49ef-107">Voordat u nieuwe registraties voor een verwijzing kunt maken, moet u een nummerreeks instellen en deze aan de verwijzing koppelen.</span><span class="sxs-lookup"><span data-stu-id="b49ef-107">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="b49ef-108">U kunt alle vereiste nummerreeksen tegelijkertijd instellen met de wizard **Nummerreeksen instellen** of u kunt individuele nummerreeksen maken of wijzigen met de pagina **Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="b49ef-108">You can set up all required number sequences at the same time by using the **Set up number sequences** wizard, or you can create or modify individual number sequences by using the **Number sequences** page.</span></span>

1. <span data-ttu-id="b49ef-109">Ga naar **Navigatiedeelvenster > Modules > Organisatiebeheer > Nummerreeksen > Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="b49ef-109">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="b49ef-110">Selecteer **Nummerreeksen selecteren**.</span><span class="sxs-lookup"><span data-stu-id="b49ef-110">Select **Number sequence**.</span></span>
3. <span data-ttu-id="b49ef-111">Typ een waarde in het veld **Nummerreekscode**.</span><span class="sxs-lookup"><span data-stu-id="b49ef-111">In the **Number sequence code** field, type a value.</span></span>
4. <span data-ttu-id="b49ef-112">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="b49ef-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b49ef-113">Selecteer op het sneltabblad **Bereikparameters** een bereik voor de nummerreeks en selecteer bereikwaarden in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="b49ef-113">On the **Scope parameters** FastTab, select a scope for the number sequence and select scope values from the drop-down list.</span></span> <span data-ttu-id="b49ef-114">De scope bepaalt welke organisaties de nummerreeks gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b49ef-114">The scope defines which organizations use the number sequence.</span></span> <span data-ttu-id="b49ef-115">Bovendien kunnen nummerreeksen die een ander bereik hebben dan **Gedeeld**, segmenten hebben die overeenkomen met hun bereik.</span><span class="sxs-lookup"><span data-stu-id="b49ef-115">In addition, number sequences that have a scope other than **Shared** can have segments that correspond to their scope.</span></span> <span data-ttu-id="b49ef-116">Een nummerreeks met een bereik van **Rechtspersoon** kan bijvoorbeeld een segment voor rechtspersoon hebben.</span><span class="sxs-lookup"><span data-stu-id="b49ef-116">For example, a number sequence with a scope of **Legal entity** can have a legal entity segment.</span></span> <span data-ttu-id="b49ef-117">Zie [Overzicht van nummerreeksen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview) voor meer informatie over bereiken.</span><span class="sxs-lookup"><span data-stu-id="b49ef-117">For more information about scopes, see [Number sequence overview](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview).</span></span> 
6. <span data-ttu-id="b49ef-118">Vouw de sectie **Segmenten** uit.</span><span class="sxs-lookup"><span data-stu-id="b49ef-118">Expand the **Segments** section.</span></span>
    - <span data-ttu-id="b49ef-119">Definieer de notatie voor de nummerreeks door segmenten toe te voegen, te verwijderen en opnieuw te ordenen.</span><span class="sxs-lookup"><span data-stu-id="b49ef-119">Define the format for the number sequence by adding, removing, and rearranging segments.</span></span>  
    - <span data-ttu-id="b49ef-120">De nummerreeksen van alle bereiken kunnen *constante segmenten* en *alfanumerieke segmenten* bevatten.</span><span class="sxs-lookup"><span data-stu-id="b49ef-120">Number sequences of all scopes can contain *Constant segments* and *Alphanumeric segments*.</span></span> <span data-ttu-id="b49ef-121">Constante segmenten bevatten een set alfanumerieke tekens die niet veranderen.</span><span class="sxs-lookup"><span data-stu-id="b49ef-121">Constant segments contain a set of alphanumeric characters that do not change.</span></span> <span data-ttu-id="b49ef-122">Gebruik dit segmenttype om een koppelteken of andere scheidingstekens toe te voegen tussen nummerreekssegmenten.</span><span class="sxs-lookup"><span data-stu-id="b49ef-122">Use this segment type to add a hyphen or other separators between number sequence segments.</span></span> <span data-ttu-id="b49ef-123">De alfanumerieke segmenten bevatten een combinatie van hekjes (#) en ampersands (&).</span><span class="sxs-lookup"><span data-stu-id="b49ef-123">Alphanumeric segments contain a combination of number signs (#) and ampersands (&).</span></span> <span data-ttu-id="b49ef-124">Deze tekens stellen letters en cijfers voor die omhoog gaan telkens als een nummer uit de reeks wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b49ef-124">These characters represent letters and numbers that increment every time that a number from the sequence is used.</span></span> <span data-ttu-id="b49ef-125">Gebruik een hekje (#) om stijgende nummers aan te geven en een en-teken (&) om stijgende letters aan te geven.</span><span class="sxs-lookup"><span data-stu-id="b49ef-125">Use a number sign (#) to indicate incrementing numbers and an ampersand (&) to indicate incrementing letters.</span></span> <span data-ttu-id="b49ef-126">De indeling `#####_2014` maakt bijvoorbeeld de reeks `00001_2014`, `00002_2014` enzovoort.</span><span class="sxs-lookup"><span data-stu-id="b49ef-126">For example, the format `#####_2014` creates the sequence `00001_2014`, `00002_2014`, and so on.</span></span> <span data-ttu-id="b49ef-127">Er moet ten minste één alfanumeriek segment zijn.</span><span class="sxs-lookup"><span data-stu-id="b49ef-127">At least one alphanumeric segment must be present.</span></span> <span data-ttu-id="b49ef-128">Bereiksegmenten, zoals bedrijf of rechtspersoon, zijn niet verplicht.</span><span class="sxs-lookup"><span data-stu-id="b49ef-128">Scope segments, such as company or legal entity, are not required.</span></span> <span data-ttu-id="b49ef-129">Als u geen bereiksegmenten in de indeling opneemt, worden getallen nog steeds voor de geselecteerde verwijzing per bereik gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="b49ef-129">However, if you do not include scope segments in the format, numbers for the selected reference are still generated per scope.</span></span>  
7. <span data-ttu-id="b49ef-130">Vouw de sectie **Verwijzingen** uit.</span><span class="sxs-lookup"><span data-stu-id="b49ef-130">Expand the **References** section.</span></span> <span data-ttu-id="b49ef-131">Selecteer het documenttype of registratie waaraan u deze nummerreeks wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="b49ef-131">Select the document type or record to assign this number sequence to.</span></span> <span data-ttu-id="b49ef-132">Deze stap is optioneel voor reeksen die voor speciale gebruikspatronen van toepassingen worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="b49ef-132">This step is optional for sequences that are defined for special application usage patterns.</span></span> <span data-ttu-id="b49ef-133">In deze gevallen wordt een nieuw nummer gegenereerd met de waarde van een nummerreekscode of ID zonder een verwijzing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b49ef-133">In these scenarios, a new number is generated by using the value of a number sequence code or ID, without using a reference.</span></span> <span data-ttu-id="b49ef-134">Een voorbeeld van een gebruikspatroon voor speciale toepassingen is een reeks boekstukken die voor specifieke journaalnamen wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b49ef-134">An example of a special application usage pattern is a voucher series that is used for specific journal names.</span></span> <span data-ttu-id="b49ef-135">We raden het gebruik van zulke patronen echter niet aan.</span><span class="sxs-lookup"><span data-stu-id="b49ef-135">However, we do not recommend that you use such patterns.</span></span>  
8. <span data-ttu-id="b49ef-136">Vouw de sectie **Algemeen** uit.</span><span class="sxs-lookup"><span data-stu-id="b49ef-136">Expand the **General** section.</span></span> <span data-ttu-id="b49ef-137">Geef op het sneltabblad Algemeen op of de nummerreeks handmatig is en doorlopend of niet-doorlopend.</span><span class="sxs-lookup"><span data-stu-id="b49ef-137">On the General FastTab, specify whether the number sequence is manual, and continuous or non-continuous.</span></span> <span data-ttu-id="b49ef-138">Voer ook de laagste en hoogste nummers in die in de nummerreeks kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b49ef-138">In addition, enter the lowest and highest numbers that can be used in the number sequence.</span></span> <span data-ttu-id="b49ef-139">Een niet-doorlopende nummerreeks wijzigen in een doorlopende nummerreeks wordt niet aanbevolen.</span><span class="sxs-lookup"><span data-stu-id="b49ef-139">We do not recommend changing a non-continuous number sequence to a continuous number sequence.</span></span> <span data-ttu-id="b49ef-140">De nummerreeks zal niet echt continu worden.</span><span class="sxs-lookup"><span data-stu-id="b49ef-140">The number sequence will not be truly continuous.</span></span> <span data-ttu-id="b49ef-141">Deze wijziging kan ook overtredingen van dubbele sleutels veroorzaken in de database.</span><span class="sxs-lookup"><span data-stu-id="b49ef-141">This change may also cause duplicate key violations in the database.</span></span> <span data-ttu-id="b49ef-142">Doorlopende nummerreeksen hebben bovendien een grotere invloed op de prestaties.</span><span class="sxs-lookup"><span data-stu-id="b49ef-142">In addition, continuous number sequences have a larger effect on performance.</span></span>   
9. <span data-ttu-id="b49ef-143">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b49ef-143">Click **Save**.</span></span>
