---
title: Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten
description: In dit onderwerp wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920652"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="ca00f-103">Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten</span><span class="sxs-lookup"><span data-stu-id="ca00f-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca00f-104">In dit onderwerp wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.</span><span class="sxs-lookup"><span data-stu-id="ca00f-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="ca00f-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="ca00f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ca00f-106">De nieuwe productnummernomenclatuur wordt toegewezen aan de productdimensiegroep Kleur en grootte.</span><span class="sxs-lookup"><span data-stu-id="ca00f-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="ca00f-107">Deze taak wordt meestal uitgevoerd door een productontwerper.</span><span class="sxs-lookup"><span data-stu-id="ca00f-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="ca00f-108">Een productvariantnummer-nomenclatuur maken</span><span class="sxs-lookup"><span data-stu-id="ca00f-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="ca00f-109">Ga naar **Productgegevensbeheer \> Instellingen \> Productnomenclatuur**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="ca00f-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-110">Select **New**.</span></span>
1. <span data-ttu-id="ca00f-111">Typ in het veld **Naam** een naam voor de nomenclatuur waaraan u de productdimensiegroep van het doel kunt herkennen, bijvoorbeeld `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="ca00f-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="ca00f-112">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="ca00f-113">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-113">Select **Add**.</span></span>
1. <span data-ttu-id="ca00f-114">Selecteer **Nummer van basismaster**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="ca00f-115">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-115">Select **Add**.</span></span>
1. <span data-ttu-id="ca00f-116">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="ca00f-117">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ca00f-118">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-118">Select **Add**.</span></span>
1. <span data-ttu-id="ca00f-119">Selecteer **Kleur**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-119">Select **Color**.</span></span>
1. <span data-ttu-id="ca00f-120">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-120">Select **Add**.</span></span>
1. <span data-ttu-id="ca00f-121">Selecteer **Tekstconstante**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="ca00f-122">Typ een waarde in het veld **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ca00f-123">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-123">Select **Add**.</span></span>
1. <span data-ttu-id="ca00f-124">Selecteer **Grootte**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-124">Select **Size**.</span></span>
1. <span data-ttu-id="ca00f-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ca00f-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="ca00f-126">De nomenclatuur toewijzen aan een productmodel</span><span class="sxs-lookup"><span data-stu-id="ca00f-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="ca00f-127">Selecteer **Productdimensiegroepen**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="ca00f-128">Selecteer de **productdimensiegroep SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="ca00f-129">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-129">Select **Edit**.</span></span>
4. <span data-ttu-id="ca00f-130">Selecteer **Ja** in het veld **Nomenclatuur gebruiken**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="ca00f-131">Typ of selecteer een waarde in het veld **Productvariantnummer-nomenclatuur**.</span><span class="sxs-lookup"><span data-stu-id="ca00f-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="ca00f-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ca00f-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]