--- 
title: Een productnummer voor vooraf gedefinieerde productvarianten maken
description: In deze taakbegeleiding wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7881701385c802578e5e5c412951a1507efa5acf
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="71e13-103">Een productnummer voor vooraf gedefinieerde productvarianten maken</span><span class="sxs-lookup"><span data-stu-id="71e13-103">Create a product number for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71e13-104">In deze taakbegeleiding wordt aangegeven hoe u een productnummernomenclatuur instelt voor vooraf bepaalde productvarianten, en hoe u deze aan de juiste productdimensiegroep toewijst.</span><span class="sxs-lookup"><span data-stu-id="71e13-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="71e13-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="71e13-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="71e13-106">De nieuwe productnummernomenclatuur wordt toegewezen aan de productdimensiegroep Kleur en grootte.</span><span class="sxs-lookup"><span data-stu-id="71e13-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="71e13-107">Deze taak wordt meestal uitgevoerd door een productontwerper.</span><span class="sxs-lookup"><span data-stu-id="71e13-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="71e13-108">Een productvariantnummer-nomenclatuur maken</span><span class="sxs-lookup"><span data-stu-id="71e13-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="71e13-109">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="71e13-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="71e13-110">Klik op Productnomenclatuur.</span><span class="sxs-lookup"><span data-stu-id="71e13-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="71e13-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="71e13-111">Click New.</span></span>
4. <span data-ttu-id="71e13-112">Typ in het veld Naam een naam voor de nomenclatuur waaraan u de productdimensiegroep van het doel kunt herkennen, bijvoorbeeld Kleur en grootte.</span><span class="sxs-lookup"><span data-stu-id="71e13-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize.</span></span>
5. <span data-ttu-id="71e13-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="71e13-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="71e13-114">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="71e13-114">Click Add.</span></span>
7. <span data-ttu-id="71e13-115">Klik op Nummer van basismaster.</span><span class="sxs-lookup"><span data-stu-id="71e13-115">Click Product master number.</span></span>
8. <span data-ttu-id="71e13-116">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="71e13-116">Click Add.</span></span>
9. <span data-ttu-id="71e13-117">Klik op Tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="71e13-117">Click Text constant.</span></span>
10. <span data-ttu-id="71e13-118">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="71e13-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="71e13-119">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="71e13-119">Click Add.</span></span>
12. <span data-ttu-id="71e13-120">Klik op Kleur.</span><span class="sxs-lookup"><span data-stu-id="71e13-120">Click Color.</span></span>
13. <span data-ttu-id="71e13-121">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="71e13-121">Click Add.</span></span>
14. <span data-ttu-id="71e13-122">Klik op Tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="71e13-122">Click Text constant.</span></span>
15. <span data-ttu-id="71e13-123">Typ een waarde in het veld Tekst.</span><span class="sxs-lookup"><span data-stu-id="71e13-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="71e13-124">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="71e13-124">Click Add.</span></span>
17. <span data-ttu-id="71e13-125">Klik op Grootte.</span><span class="sxs-lookup"><span data-stu-id="71e13-125">Click Size.</span></span>
18. <span data-ttu-id="71e13-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71e13-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="71e13-127">De nomenclatuur toewijzen aan een productmodel</span><span class="sxs-lookup"><span data-stu-id="71e13-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="71e13-128">Klik op Productdimensiegroepen.</span><span class="sxs-lookup"><span data-stu-id="71e13-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="71e13-129">Selecteer de productdimensiegroep SizeCol.</span><span class="sxs-lookup"><span data-stu-id="71e13-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="71e13-130">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="71e13-130">Click Edit.</span></span>
4. <span data-ttu-id="71e13-131">Selecteer Ja in het veld Nomenclatuur gebruiken.</span><span class="sxs-lookup"><span data-stu-id="71e13-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="71e13-132">Typ of selecteer een waarde in het veld Productvariantnummer-nomenclatuur.</span><span class="sxs-lookup"><span data-stu-id="71e13-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="71e13-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71e13-133">Close the page.</span></span>


