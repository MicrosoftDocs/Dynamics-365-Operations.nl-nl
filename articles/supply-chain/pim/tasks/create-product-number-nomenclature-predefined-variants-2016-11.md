---
title: Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten
description: In dit onderwerp wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a4ad70a87cd8c6cab2e9853f4f6c52f574d318a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257408"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="fe0a2-103">Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten</span><span class="sxs-lookup"><span data-stu-id="fe0a2-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe0a2-104">In dit onderwerp wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="fe0a2-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fe0a2-106">De nieuwe productnummernomenclatuur wordt toegewezen aan de productdimensiegroep Kleur en grootte.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="fe0a2-107">Deze taak wordt meestal uitgevoerd door een productontwerper.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="fe0a2-108">Een productvariantnummer-nomenclatuur maken</span><span class="sxs-lookup"><span data-stu-id="fe0a2-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="fe0a2-109">Selecteer **Definitie van productvariantmodel**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="fe0a2-110">Selecteer **Nomenclatuur voor productnummers**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="fe0a2-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-111">Select **New**.</span></span>
4. <span data-ttu-id="fe0a2-112">Typ in het veld **Naam** een naam voor de nomenclatuur waaraan u de productdimensiegroep van het doel kunt herkennen, bijvoorbeeld `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="fe0a2-113">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="fe0a2-114">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-114">Select **Add**.</span></span>
7. <span data-ttu-id="fe0a2-115">Selecteer **Nummer van basismaster**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="fe0a2-116">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-116">Select **Add**.</span></span>
9. <span data-ttu-id="fe0a2-117">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="fe0a2-118">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="fe0a2-119">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-119">Select **Add**.</span></span>
12. <span data-ttu-id="fe0a2-120">Selecteer **Kleur**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-120">Select **Color**.</span></span>
13. <span data-ttu-id="fe0a2-121">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-121">Select **Add**.</span></span>
14. <span data-ttu-id="fe0a2-122">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="fe0a2-123">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="fe0a2-124">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-124">Select **Add**.</span></span>
17. <span data-ttu-id="fe0a2-125">Selecteer **Grootte**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-125">Select **Size**.</span></span>
18. <span data-ttu-id="fe0a2-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="fe0a2-127">De nomenclatuur toewijzen aan een productmodel</span><span class="sxs-lookup"><span data-stu-id="fe0a2-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="fe0a2-128">Selecteer **Productdimensiegroepen**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="fe0a2-129">Selecteer de **productdimensiegroep SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="fe0a2-130">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-130">Select **Edit**.</span></span>
4. <span data-ttu-id="fe0a2-131">Selecteer **Ja** in het veld **Nomenclatuur gebruiken**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="fe0a2-132">Typ of selecteer een waarde in het veld **Productvariantnummer-nomenclatuur**.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="fe0a2-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="fe0a2-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]