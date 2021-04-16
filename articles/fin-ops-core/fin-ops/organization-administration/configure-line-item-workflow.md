---
title: Workflows voor regelitems configureren
description: In dit onderwerp wordt uitgelegd hoe u een workflowelement voor regelartikelen configureert.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84da7080542b4cc2ecc487b0a1331482fb69b998
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747900"
---
# <a name="configure-line-item-workflows"></a><span data-ttu-id="0a1ba-103">Workflows voor regelitems configureren</span><span class="sxs-lookup"><span data-stu-id="0a1ba-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a1ba-104">In dit onderwerp wordt uitgelegd hoe u een workflowelement voor regelartikelen configureert.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="0a1ba-105">Om een element in een workflow voor regelartikelen te configureren, klikt u in de workfloweditor met de rechtermuisknop op het goedkeuringselement en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="0a1ba-106">Met behulp van de volgende procedures kunt dan u de eigenschappen van het element in een workflow voor regelartikelen configureren.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="0a1ba-107">Een naam opgeven voor het element in een workflow voor regelartikelen</span><span class="sxs-lookup"><span data-stu-id="0a1ba-107">Name the line-item workflow element</span></span>

<span data-ttu-id="0a1ba-108">Voer deze stappen uit om een naam op te geven voor het element in een workflow voor regelartikelen.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1. <span data-ttu-id="0a1ba-109">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="0a1ba-110">Geef in het veld **Naam** een unieke naam voor het element in een workflow voor regelartikelen op.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="0a1ba-111">Geef op of dezelfde workflow wordt gebruikt om alle regelartikelen te verwerken</span><span class="sxs-lookup"><span data-stu-id="0a1ba-111">Specify whether the same workflow is used to process all line items</span></span>

<span data-ttu-id="0a1ba-112">Volg deze stappen om op te geven of dezelfde workflow wordt gebruikt om alle regelartikelen in een document te verwerken.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1. <span data-ttu-id="0a1ba-113">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="0a1ba-114">Als dezelfde workflow alle regelartikelen in een document moet verwerken, klikt u op **Eén workflow aanroepen voor alle regelartikelen**.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="0a1ba-115">Selecteer vervolgens de workflow om te gebruiken voor het verwerken van de regelartikelen.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-115">Then select the workflow to use to process the line items.</span></span>
3. <span data-ttu-id="0a1ba-116">Als een specifieke workflow de regelartikelen moet verwerken die aan een specifieke set voorwaarden voldoen, klikt u op **Eén workflow aanroepen voor elk regelartikel**.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="0a1ba-117">Voer deze stappen uit om de set voorwaarden te definiëren:</span><span class="sxs-lookup"><span data-stu-id="0a1ba-117">Then follow these steps to define the set of conditions:</span></span>

    1. <span data-ttu-id="0a1ba-118">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-118">Click **Add**.</span></span>
    2. <span data-ttu-id="0a1ba-119">Selecteer ide voorwaarde in de tabel.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-119">Select the condition in the table.</span></span>
    3. <span data-ttu-id="0a1ba-120">Geef in het tabblad **Voorwaardenaam** een naam op voor de set voorwaarden die u definieert.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4. <span data-ttu-id="0a1ba-121">Klik op **Voorwaarde toevoegen** om een voorwaarde in te voeren.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-121">Click **Add condition** to enter a condition.</span></span>
    5. <span data-ttu-id="0a1ba-122">Geef desgewenst vereiste extra voorwaarden op.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-122">Enter any additional conditions that are required.</span></span>
    6. <span data-ttu-id="0a1ba-123">Klik op **Testen** om te controleren of de door u ingevoerde set voorwaarden correct is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="0a1ba-124">Seelecteer op de pagina **Workflowvoorwaarde testen** in het gebied **Voorwaarde valideren** een record en klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="0a1ba-125">Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="0a1ba-126">Klik op **OK** of **Annuleren** om terug te gaan naar de pagina **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="0a1ba-127">Selecteer op het tabblad **Workflow** de workflow die u wilt gebruiken om regelartikelen te verwerken die aan de set voorwaarden voldoen die u hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="0a1ba-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]