---
title: Tariefwijzigingen verwerken
description: Verwerk wijzigingen in het vergoedingstarief in Microsoft Dynamics 365 Human Resources wanneer er een wijziging is aangebracht in de instellingen van geschiktheidsregels in een nieuw of bestaand vergoedingsplan.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c87d98a16431805ad652e28e5ca100a4152ad0c6
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466225"
---
# <a name="process-rate-changes"></a><span data-ttu-id="2ebf7-103">Tariefwijzigingen verwerken</span><span class="sxs-lookup"><span data-stu-id="2ebf7-103">Process rate changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2ebf7-104">Verwerk wijzigingen in het vergoedingstarief in Microsoft Dynamics 365 Human Resources wanneer er een wijziging is aangebracht in de instellingen van geschiktheidsregels in een nieuw of bestaand vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="2ebf7-105">Als er een nieuwe geschiktheidsregel wordt gemaakt en aan het plan wordt toegewezen, wordt u door het systeem gevraagd om de geschiktheidscontrole van medewerkers opnieuw uit te voeren om te controleren of medewerkers nu mogelijk in aanmerking komen voor het plan op basis van nieuwe geschiktheidsopties.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="2ebf7-106">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Updateverwerking voor tariefwijziging**.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="2ebf7-107">Geef in het dialoogvenster **Updateproces voor vergoedingstarief uitvoeren** waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="2ebf7-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="2ebf7-108">Veld</span><span class="sxs-lookup"><span data-stu-id="2ebf7-108">Field</span></span> | <span data-ttu-id="2ebf7-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2ebf7-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2ebf7-110">**Inschrijvingsperiode**</span><span class="sxs-lookup"><span data-stu-id="2ebf7-110">**Enrollment period**</span></span> | <span data-ttu-id="2ebf7-111">De inschrijvingsperiode waarvoor de tariefwijzigingen moeten worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="2ebf7-112">Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="2ebf7-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="2ebf7-113">Voer gegevens in voor het proces.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="2ebf7-114">Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="2ebf7-115">Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="2ebf7-116">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-116">Select **OK**.</span></span> <span data-ttu-id="2ebf7-117">Het proces wordt uitgevoerd met de parameters die u instelt.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="2ebf7-118">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ebf7-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]