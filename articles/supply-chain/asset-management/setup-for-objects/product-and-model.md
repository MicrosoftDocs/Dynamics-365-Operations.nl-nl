---
title: Activafabrikanten en -modellen
description: In dit onderwerp wordt uitgelegd hoe u activafabrikanten en gerelateerde modellen kunt instellen in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cec4f644af4a087464635d9a7ca825eb354747eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259957"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="4caea-103">Activafabrikanten en -modellen</span><span class="sxs-lookup"><span data-stu-id="4caea-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4caea-104">In dit onderwerp wordt uitgelegd hoe u activafabrikanten en gerelateerde modellen kunt instellen in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="4caea-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="4caea-105">Modellen kunnen worden gerelateerd aan activatypen.</span><span class="sxs-lookup"><span data-stu-id="4caea-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="4caea-106">Productmodelrelaties instellen</span><span class="sxs-lookup"><span data-stu-id="4caea-106">Set up product-model relations</span></span>

1. <span data-ttu-id="4caea-107">Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Fabrikant en model**.</span><span class="sxs-lookup"><span data-stu-id="4caea-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="4caea-108">Selecteer **Nieuw** om een nieuw product te maken.</span><span class="sxs-lookup"><span data-stu-id="4caea-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="4caea-109">Voer in het veld **Fabrikant** een naam in voor de activafabrikant.</span><span class="sxs-lookup"><span data-stu-id="4caea-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="4caea-110">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="4caea-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="4caea-111">Selecteer op het sneltabblad **Modellen** de optie **Toevoegen** om een activamodel te maken dat moet worden gerelateerd aan de activafabrikant.</span><span class="sxs-lookup"><span data-stu-id="4caea-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="4caea-112">Voer in het veld **Model** een naam in voor de activamodel.</span><span class="sxs-lookup"><span data-stu-id="4caea-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="4caea-113">Voer in het veld **Beschrijving** een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="4caea-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="4caea-114">Selecteer in het veld **Activatype** het activatype waaraan het model van de fabrikant moet zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="4caea-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4caea-115">U kunt ook relaties instellen voor activatypen, -fabrikanten en -modellen in het zoekveld **Activatypen**.</span><span class="sxs-lookup"><span data-stu-id="4caea-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="4caea-116">Zie [Typen activa](../setup-for-objects/object-types.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4caea-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="4caea-117">Op het sneltabblad **Details** geeft het veld **Modellen** het aantal activamodellen weer dat is ingesteld voor de geselecteerde activafabrikant.</span><span class="sxs-lookup"><span data-stu-id="4caea-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="4caea-118">In het veld **Activa** wordt het aantal activa weergegeven dat de geselecteerde fabrikant gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4caea-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="4caea-119">In het veld **Activa** wordt het aantal objecten weergegeven dat het fabrikantmodel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4caea-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="4caea-120">Een activatype kan geen relaties met modellen van activafabrikanten hebben, kan betrekking hebben op één model van een activafabrikant van activa of kan zijn gerelateerd aan meerdere modellen van activafabrikanten.</span><span class="sxs-lookup"><span data-stu-id="4caea-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="4caea-121">Als een actiatype is gerelateerd aan ten minste één model van een fabrikant, kunnen alleen de combinaties die zijn ingesteld in de zoekopdracht **Fabrikantmodel** worden geselecteerd op die pagina's van Activabeheer waar een combinatie van een activatype, fabrikant en model kan worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="4caea-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="4caea-122">Deze pagina's bevatten **Alle activa**, **Activaserviceniveaus**, **Standaardwaarden voor taaktypen** en **Onderhoudsbudgetregels**.</span><span class="sxs-lookup"><span data-stu-id="4caea-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="4caea-123">Als sommige activatypen niet zijn gerelateerd aan een fabrikantmodel, worden alleen de activatypen en fabrikantmodellen die ook geen relatie hebben met activatypen op de pagina's weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4caea-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="4caea-124">Een fabrikant en model selecteren voor een object</span><span class="sxs-lookup"><span data-stu-id="4caea-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="4caea-125">Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="4caea-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="4caea-126">Selecteer in de kolom **Activum** de koppeling voor het activum.</span><span class="sxs-lookup"><span data-stu-id="4caea-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="4caea-127">De pagina **Details** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4caea-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="4caea-128">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="4caea-128">Select **Edit**.</span></span>
4. <span data-ttu-id="4caea-129">Selecteer op het sneltabblad **Algemeen** waarden in de velden **Fabrikant** en **Model**.</span><span class="sxs-lookup"><span data-stu-id="4caea-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]