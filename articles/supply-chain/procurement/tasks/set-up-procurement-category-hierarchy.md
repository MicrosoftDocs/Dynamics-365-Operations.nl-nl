---
title: Een hiërarchie van aanschaffingscategorieën instellen
description: Deze procedure laat zien hoe u nieuwe knooppunten in een hiërarchie van aanschaffingscategorieën maakt en hoe u een aanschaffingscategorie configureert die in een aanschaffingsproces moet worden gebruikt.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7010a1c612b9b3884c675f578657d951da06c38
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995277"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="88d66-103">Een hiërarchie van aanschaffingscategorieën instellen</span><span class="sxs-lookup"><span data-stu-id="88d66-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88d66-104">Deze procedure laat zien hoe u nieuwe knooppunten in een hiërarchie van aanschaffingscategorieën maakt en hoe u een aanschaffingscategorie configureert die in een aanschaffingsproces moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="88d66-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="88d66-105">Deze taken worden meestal uitgevoerd door een inkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="88d66-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="88d66-106">Voordat u deze procedure kunt starten, moet er een categoriehiërarchie van het type Inkoop zijn.</span><span class="sxs-lookup"><span data-stu-id="88d66-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="88d66-107">Als u een demobedrijf gebruikt, kunt u deze procedure in het bedrijf USMF uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="88d66-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="88d66-108">Een nieuwe inkoopcategorie toevoegen</span><span class="sxs-lookup"><span data-stu-id="88d66-108">Add a new procurement category</span></span>
1. <span data-ttu-id="88d66-109">Ga naar het **Navigatievenster > Modules > Inkoop en bronnen > Uitlevering > Aanschaffingscategorieën**.</span><span class="sxs-lookup"><span data-stu-id="88d66-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="88d66-110">Klik in het actievenster op **Categoriehiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="88d66-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="88d66-111">De huidige hiërarchie van aanschaffingscategorieën wordt weergegeven aan de linkerkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="88d66-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="88d66-112">U gaat de hiërarchie wijzigen.</span><span class="sxs-lookup"><span data-stu-id="88d66-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="88d66-113">Klik in het actievenster op **Nieuw categorieknooppunt**.</span><span class="sxs-lookup"><span data-stu-id="88d66-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="88d66-114">Het systeem selecteert standaard het bovenste knooppunt.</span><span class="sxs-lookup"><span data-stu-id="88d66-114">The system selects the top node by default.</span></span> <span data-ttu-id="88d66-115">Als u deze procedure als taakbegeleiding uitvoert, kunt u op de knop Ontgrendelen klikken en een ander bovenliggend knooppunt selecteren om uw nieuw knooppunt in te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="88d66-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="88d66-116">Zodra dat is gedaan, vergrendelt u de taakbegeleiding opnieuw en klikt u op het categorieknooppunt Nieuw.</span><span class="sxs-lookup"><span data-stu-id="88d66-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="88d66-117">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="88d66-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="88d66-118">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="88d66-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="88d66-119">In het veld **Beschrijvende naam** typt u een waarde.</span><span class="sxs-lookup"><span data-stu-id="88d66-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="88d66-120">De beschrijvende naam is optioneel.</span><span class="sxs-lookup"><span data-stu-id="88d66-120">The friendly name is optional.</span></span> <span data-ttu-id="88d66-121">Deze wordt in categoriezoekopdrachten met de categorienaam weergegeven.</span><span class="sxs-lookup"><span data-stu-id="88d66-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="88d66-122">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="88d66-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="88d66-123">Producten aan uw nieuwe aanschaffingscategorie toevoegen</span><span class="sxs-lookup"><span data-stu-id="88d66-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="88d66-124">Ga naar **Inkoop en sourcing > Uitlevering > Inkoopcategorieën**.</span><span class="sxs-lookup"><span data-stu-id="88d66-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="88d66-125">Selecteer het knooppunt dat u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="88d66-125">Select the node you just added.</span></span> <span data-ttu-id="88d66-126">Als u de procedure als taakbegeleiding uitvoert, moet u de taakbegeleiding wellicht ontgrendelen om het knooppunt te selecteren.</span><span class="sxs-lookup"><span data-stu-id="88d66-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="88d66-127">Schakel de uitbreiding van de sectie **Producten** om.</span><span class="sxs-lookup"><span data-stu-id="88d66-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="88d66-128">Klik op **Toevoegen** om producten te koppelen aan de aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="88d66-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="88d66-129">Selecteer de producten die u wilt toevoegen aan de aanschaffingscategorie.</span><span class="sxs-lookup"><span data-stu-id="88d66-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="88d66-130">Selecteer de pijl om de producten aan de tabel **Geselecteerd** toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="88d66-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="88d66-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="88d66-131">Select **OK**.</span></span>
