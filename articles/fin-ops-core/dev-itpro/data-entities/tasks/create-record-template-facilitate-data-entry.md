---
title: Een recordsjabloon maken om de invoer van gegevens te vergemakkelijken
description: In dit onderwerp wordt voorgedaan hoe u een recordsjabloon kunt maken, zodat vaak gebruikte veldwaarden niet expliciet moeten worden ingevoerd voor elke nieuwe record.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181928"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="da2da-103">Een recordsjabloon maken om de invoer van gegevens te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="da2da-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da2da-104">In dit onderwerp wordt voorgedaan hoe u een recordsjabloon kunt maken, zodat vaak gebruikte veldwaarden niet expliciet moeten worden ingevoerd voor elke nieuwe record.</span><span class="sxs-lookup"><span data-stu-id="da2da-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="da2da-105">In deze procedure maakt u een nieuwe record voor nieuwe laptops die u wilt laten toevoegen aan uw vaste activa.</span><span class="sxs-lookup"><span data-stu-id="da2da-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="da2da-106">In deze procedure wordt het voorbeeldbedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="da2da-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="da2da-107">Ga in het navigatievenster naar **Modules > Vaste activa > Vaste activa > Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="da2da-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="da2da-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="da2da-108">Select **New**.</span></span>
3. <span data-ttu-id="da2da-109">Typ of selecteer een waarde in het veld **Groep vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="da2da-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="da2da-110">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="da2da-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="da2da-111">Voer bijvoorbeeld **Corporate lead-laptop** in.</span><span class="sxs-lookup"><span data-stu-id="da2da-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="da2da-112">Typ een waarde in het veld **Zoeknaam**.</span><span class="sxs-lookup"><span data-stu-id="da2da-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="da2da-113">Voer bijvoorbeeld **laptop** in.</span><span class="sxs-lookup"><span data-stu-id="da2da-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="da2da-114">Vouw de sectie **Technische informatie** uit.</span><span class="sxs-lookup"><span data-stu-id="da2da-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="da2da-115">Typ waarden in de velden **Merk**, **Model** en **Modeljaar**.</span><span class="sxs-lookup"><span data-stu-id="da2da-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="da2da-116">Selecteer **Opties** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="da2da-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="da2da-117">Selecteer **Recordinfo**.</span><span class="sxs-lookup"><span data-stu-id="da2da-117">Select **Record info**.</span></span>
10. <span data-ttu-id="da2da-118">Selecteer **Gebruikerssjabloon**.</span><span class="sxs-lookup"><span data-stu-id="da2da-118">Select **User template**.</span></span>
11. <span data-ttu-id="da2da-119">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="da2da-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="da2da-120">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="da2da-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="da2da-121">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="da2da-121">Select **OK**.</span></span>
14. <span data-ttu-id="da2da-122">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="da2da-122">Select **Close**.</span></span>
