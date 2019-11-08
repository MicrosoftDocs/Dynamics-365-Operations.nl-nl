---
title: Kosten onderhoudsschema
description: In dit onderwerp worden de kosten van onderhoudsplannen in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b30fa3c142057b43202a8f5a323c0b425865e971
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571318"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="b83a5-103">Kosten onderhoudsschema</span><span class="sxs-lookup"><span data-stu-id="b83a5-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b83a5-104">In Activabeheer kunt u budgetkosten berekenen op regels voor onderhoudsplanning.</span><span class="sxs-lookup"><span data-stu-id="b83a5-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="b83a5-105">Dit is handig als u een overzicht wilt weergeven van verwachte kosten, bijvoorbeeld kosten met betrekking tot geplande onderhoudstaken voor het volgende jaar.</span><span class="sxs-lookup"><span data-stu-id="b83a5-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="b83a5-106">De berekeningen zijn gebaseerd op bestaande regels voor onderhoudsplanning van het type "Onderhoudsplannen" en "Onderhoudsrondes" en "Onderhoudsaanvragen".</span><span class="sxs-lookup"><span data-stu-id="b83a5-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="b83a5-107">Klik **Onderhoudsbeheer** > **Aanvragen** > **Activa** > **Kosten onderhoudsplanning**.</span><span class="sxs-lookup"><span data-stu-id="b83a5-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="b83a5-108">In het dialoogvenster **Kosten onderhoudsplanning** kunt u een **Financiële dimensieset** selecteren als u kosten gegroepeerd in financiële dimensies wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="b83a5-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="b83a5-109">U kunt financiële dimensie sets instellen in **Grootboek** > **Rekeningschema** > **Dimensies** > **Financiële dimensiesets**.</span><span class="sxs-lookup"><span data-stu-id="b83a5-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="b83a5-110">U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor onderhoudsplanning zijn met betrekking tot functionele locaties.</span><span class="sxs-lookup"><span data-stu-id="b83a5-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="b83a5-111">Als u bijvoorbeeld het getal "1" invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle regels voor onderhoudsplanning voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel worden opgeteld op basis van functionele locaties die zich op een lager niveau bevinden.</span><span class="sxs-lookup"><span data-stu-id="b83a5-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="b83a5-112">Als u het getal "0" in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle regels voor onderhoudsplanning weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.</span><span class="sxs-lookup"><span data-stu-id="b83a5-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="b83a5-113">Als u een berekening wilt maken voor specifieke activa, klikt u op **Filteren** in het Sneltabblad **Records die moeten worden opgenomen** en selecteert u de relevante activa.</span><span class="sxs-lookup"><span data-stu-id="b83a5-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="b83a5-114">Indien nodig kunt u ook een **Verwachte begindatum** voor de kostenberekening opgeven of een andere **Status** voor de kostenberekening selecteren.</span><span class="sxs-lookup"><span data-stu-id="b83a5-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="b83a5-115">Klik op **OK** om de kostenberekening te starten.</span><span class="sxs-lookup"><span data-stu-id="b83a5-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="b83a5-116">Klik op het tabblad **Kosten van onderhoudsplanning** > in de actieschermgroepen op **Groeperen op...**, klik op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b83a5-116">On the **Maintenance schedule cost** tab > in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="b83a5-117">De geselecteerde groepsknoppen in het actievenster zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="b83a5-117">The selected action pane group buttons are highlighted.</span></span> <span data-ttu-id="b83a5-118">U kunt knoppen activeren of deactiveren door erop te klikken.</span><span class="sxs-lookup"><span data-stu-id="b83a5-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="b83a5-119">Klik op de knop **kosten berekenen** als u een nieuwe kostenberekening wilt maken.</span><span class="sxs-lookup"><span data-stu-id="b83a5-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="b83a5-120">In de onderstaande afbeelding ziet u de resultaten van de kostenberekening van een onderhoudsschema.</span><span class="sxs-lookup"><span data-stu-id="b83a5-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Figuur 1](media/17-preventive-maintenance.png)

