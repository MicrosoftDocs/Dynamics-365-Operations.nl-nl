---
title: Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen
description: In dit onderwerp wordt beschreven hoe u werknemers configureert die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956612"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="69680-103">Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="69680-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69680-104">In dit onderwerp wordt beschreven hoe u werknemers configureert die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen.</span><span class="sxs-lookup"><span data-stu-id="69680-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="69680-105">Niet-conformeringen moeten worden goedgekeurd voordat gebruikers kunnen beginnen met het invoeren van details, zoals correcties of bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="69680-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="69680-106">Voordat gebruikers niet-conformeringen kunnen goedkeuren of afwijzen, moet hun gebruikers-id (gebruikersrecord) worden gekoppeld aan een werknemersrecord.</span><span class="sxs-lookup"><span data-stu-id="69680-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="69680-107">U kunt desgewenst werknemers configureren die verantwoordelijk zijn voor de kwaliteit en vervolgens de ene werknemer toestaan om werk goed te keuren namens een andere werknemer.</span><span class="sxs-lookup"><span data-stu-id="69680-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="69680-108">Een gebruiker in staat stellen niet-conformeringen te verwerken</span><span class="sxs-lookup"><span data-stu-id="69680-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="69680-109">Voordat een gebruiker niet-conformeringen kan goedkeuren of afwijzen, moet u de gebruikers-id van die werknemer koppelen aan een werknemersrecord.</span><span class="sxs-lookup"><span data-stu-id="69680-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="69680-110">De goedkeuringsvelden kunnen vervolgens automatisch worden ingesteld en de huidige gebruiker kan automatisch worden ingevuld voor de urenstaat.</span><span class="sxs-lookup"><span data-stu-id="69680-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="69680-111">Voordat de gebruiker de documentnotities kan gebruiken, moet u de documentverwerking activeren in de gebruikersopties voor die gebruiker.</span><span class="sxs-lookup"><span data-stu-id="69680-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="69680-112">Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="69680-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="69680-113">Zoek en open de gebruiker die niet-conformeringen moet kunnen goedkeuren of afwijzen.</span><span class="sxs-lookup"><span data-stu-id="69680-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="69680-114">Stel het veld **Persoon** in op de naam van de werknemer die is gekoppeld aan de huidige gebruikersrecord.</span><span class="sxs-lookup"><span data-stu-id="69680-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="69680-115">Selecteer **Gebruikersopties** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="69680-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="69680-116">Ga naar de pagina **Opties** voor de huidige gebruikersrecord en stel op het tabblad **Voorkeuren** de optie **Documentverwerking inschakelen** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="69680-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="69680-117">Sluit de pagina's.</span><span class="sxs-lookup"><span data-stu-id="69680-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="69680-118">Werknemers definiëren die verantwoordelijk zijn voor de kwaliteit</span><span class="sxs-lookup"><span data-stu-id="69680-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="69680-119">Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitscontrole \> Werknemers die verantwoordelijk zijn voor de kwaliteit**.</span><span class="sxs-lookup"><span data-stu-id="69680-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="69680-120">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="69680-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="69680-121">Selecteer in het veld **Werknemer** de werknemer die kwaliteitsgegevens invoert.</span><span class="sxs-lookup"><span data-stu-id="69680-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="69680-122">Selecteer in het veld **Verantwoordelijke werknemer** de werknemer namens wie de geselecteerde werknemer werk invoert.</span><span class="sxs-lookup"><span data-stu-id="69680-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="69680-123">Wanneer er niet-conformeringen worden gemaakt en bijgewerkt, wordt deze werknemer standaard ingevoerd in de **Werknemer**-velden.</span><span class="sxs-lookup"><span data-stu-id="69680-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69680-124">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="69680-124">Additional resources</span></span>

- [<span data-ttu-id="69680-125">Overzicht van kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="69680-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="69680-126">Beheer van kwaliteit en niet-conformeringen inschakelen</span><span class="sxs-lookup"><span data-stu-id="69680-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="69680-127">Kwaliteitstoeslagen</span><span class="sxs-lookup"><span data-stu-id="69680-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="69680-128">Quarantainezones voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="69680-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="69680-129">Typen diagnosen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="69680-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="69680-130">Kwaliteitstoeslagen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="69680-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="69680-131">Bewerkingen voor niet-conformeringen</span><span class="sxs-lookup"><span data-stu-id="69680-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="69680-132">Kwaliteitsbeheer voor magazijnprocessen</span><span class="sxs-lookup"><span data-stu-id="69680-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
