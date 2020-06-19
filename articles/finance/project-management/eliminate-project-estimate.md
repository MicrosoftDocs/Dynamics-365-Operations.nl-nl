---
title: Een projectraming elimineren
description: Dit onderwerp bevat informatie over het verwijderen van een projectraming nadat deze is voltooid.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410206"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="d9014-103">Een projectraming elimineren</span><span class="sxs-lookup"><span data-stu-id="d9014-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9014-104">Projectramingen bieden de financiële weergave voor werk dat is geraamd en gepland voor een project.</span><span class="sxs-lookup"><span data-stu-id="d9014-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="d9014-105">Indien u voor een project met ramingen wilt werken, moet u het project aan een ramingsproject koppelen.</span><span class="sxs-lookup"><span data-stu-id="d9014-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="d9014-106">Een ramingsproject is altijd gebaseerd op een bestaand project, maar meerdere projecten kunnen verwijzen naar één ramingsproject.</span><span class="sxs-lookup"><span data-stu-id="d9014-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="d9014-107">Alleen projecten met een vaste prijs en investeringsprojecten kunnen aan ramingsprojecten worden gekoppeld, en deze projecten moeten bij dezelfde projectgroep als het ramingsproject horen.</span><span class="sxs-lookup"><span data-stu-id="d9014-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="d9014-108">Als u een ramingsproject wilt schrappen, moet het voltooid zijn.</span><span class="sxs-lookup"><span data-stu-id="d9014-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="d9014-109">In de volgende stappen wordt uitgelegd hoe u een raming kunt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d9014-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="d9014-110">Ga naar **Projectbeheer en boekhouding** > **Alle projecten** en open het project.</span><span class="sxs-lookup"><span data-stu-id="d9014-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="d9014-111">Selecteer op het tabblad **Beheren** de optie **Ramingen** en selecteer op de pagina **Raming** de optie **Schrappen**.</span><span class="sxs-lookup"><span data-stu-id="d9014-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="d9014-112">Stel op de pagina **Raming schrappen** op het tabblad **Algemeen** de volgende opties in:</span><span class="sxs-lookup"><span data-stu-id="d9014-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="d9014-113">**Periodecode**: de periodecode selecteren om de juiste ramingsprojecten te kiezen.</span><span class="sxs-lookup"><span data-stu-id="d9014-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="d9014-114">**Ramingsdatum**: de juiste ramingsdatum voor schrapping selecteren.</span><span class="sxs-lookup"><span data-stu-id="d9014-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="d9014-115">**Elimineren met OHW-waarschuwingen**: schakel deze optie in als u een melding wilt weergeven wanneer een raming wordt geschrapt die is gekoppeld aan onderhanden werk (OHW).</span><span class="sxs-lookup"><span data-stu-id="d9014-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="d9014-116">Wanneer deze optie niet is ingeschakeld, kan de raming niet worden geschrapt wanneer er niet-geraamde transacties bestaan.</span><span class="sxs-lookup"><span data-stu-id="d9014-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="d9014-117">Deze optie is alleen beschikbaar als schrapping wordt toegepast op een ramingsproject.</span><span class="sxs-lookup"><span data-stu-id="d9014-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="d9014-118">Dit veld is niet beschikbaar als u periodieke boekingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d9014-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="d9014-119">Deze instelling werkt met de instellingen op het tabblad **Raming** op de pagina **Projectparameters** en in de veldengroep **Schrapping toestaan als niet-geraamde transacties bestaan**.</span><span class="sxs-lookup"><span data-stu-id="d9014-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="d9014-120">**Fase instellen op Gereed**: schakel deze optie in om de fase van het ramingsproject in te stellen op **Gereed** nadat u de schrapping hebt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d9014-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="d9014-121">**Ramingslijst afdrukken**: de gegevens selecteren die u wilt opnemen wanneer de ramingslijst wordt afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="d9014-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="d9014-122">**Infologboek weergeven**: schakel deze optie in om het infologboek weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d9014-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="d9014-123">**Boekingsdatum**: kies de grootboekboekingsdatum van de raming.</span><span class="sxs-lookup"><span data-stu-id="d9014-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="d9014-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9014-124">Select **OK**.</span></span>
5. <span data-ttu-id="d9014-125">Nadat het schrappingsproces is voltooid, wordt het geschrapte ramingsproject weergegeven met een negatieve waarde.</span><span class="sxs-lookup"><span data-stu-id="d9014-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="d9014-126">Als u niet van plan bent om een raming te schrappen, kunt u de geschrapte raming selecteren en **Schrapping omkeren**.</span><span class="sxs-lookup"><span data-stu-id="d9014-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
