---
title: Een sjabloonstuklijst maken
description: Met verschillende methoden kunt u een sjabloonstuklijst maken.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470757"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="b4f56-103">Een sjabloonstuklijst maken</span><span class="sxs-lookup"><span data-stu-id="b4f56-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b4f56-104">Met de onderstaande methoden kunt u een sjabloonstuklijst maken.</span><span class="sxs-lookup"><span data-stu-id="b4f56-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="b4f56-105">Voor alle methoden zijn de velden **Datum vanaf** en **Datum t/m** optioneel en dienen ze alleen ter informatie.</span><span class="sxs-lookup"><span data-stu-id="b4f56-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="b4f56-106">Handmatig een sjabloonstuklijst maken</span><span class="sxs-lookup"><span data-stu-id="b4f56-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="b4f56-107">Ga naar **Servicebeheer** \> **Instellen** \> **Serviceobjecten** \> **Sjabloonstuklijsten**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="b4f56-108">Selecteer **Nieuw** om het formulier **Sjabloonstuklijst maken** te openen.</span><span class="sxs-lookup"><span data-stu-id="b4f56-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="b4f56-109">Selecteer onder **Stuklijstregels kopiëren uit verwijzing** de optie **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="b4f56-110">Selecteer in het veld **Artikelnummer** een artikel van het type **Stuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="b4f56-111">Voer in het veld **Naam** een naam voor de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="b4f56-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="b4f56-112">Voer in de velden **Datum vanaf** en **Datum t/m** een datuminterval in waarin de sjabloonstuklijst actief is.</span><span class="sxs-lookup"><span data-stu-id="b4f56-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="b4f56-113">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-113">Select **OK**.</span></span>

<span data-ttu-id="b4f56-114">Er is een nieuwe lege sjabloonstuklijst gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b4f56-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="b4f56-115">Een sjabloonstuklijst maken op basis van een andere sjabloonstuklijst</span><span class="sxs-lookup"><span data-stu-id="b4f56-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="b4f56-116">Selecteer **Servicebeheer** \> **Instellen** \> **Serviceobjecten** \> **Sjabloonstuklijsten**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="b4f56-117">Selecteer **Nieuw** om het formulier **Sjabloonstuklijst maken** te openen.</span><span class="sxs-lookup"><span data-stu-id="b4f56-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="b4f56-118">Selecteer onder **Stuklijstregels kopiëren uit verwijzing** de optie **Sjabloonstuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="b4f56-119">Selecteer in het veld **Referentienummer** een bestaande sjabloonstuklijst die u naar uw nieuwe sjabloonstuklijst wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="b4f56-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="b4f56-120">Voer in het veld **Naam** een naam voor de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="b4f56-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="b4f56-121">Voer in de velden **Datum vanaf** en **Datum t/m** een datuminterval in waarin de sjabloonstuklijst actief is.</span><span class="sxs-lookup"><span data-stu-id="b4f56-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="b4f56-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-122">Select **OK**.</span></span>

<span data-ttu-id="b4f56-123">Er is een nieuwe sjabloonstuklijst gemaakt met regels die overeenkomen met de regels in de oorspronkelijke sjabloonstuklijst.</span><span class="sxs-lookup"><span data-stu-id="b4f56-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="b4f56-124">Een sjabloonstuklijst maken op basis van een artikelstuklijst</span><span class="sxs-lookup"><span data-stu-id="b4f56-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="b4f56-125">Selecteer **Servicebeheer** \> **Instellen** \> **Serviceobjecten** \> **Sjabloonstuklijsten**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="b4f56-126">Selecteer **Nieuw** om het formulier **Sjabloonstuklijst maken** te openen.</span><span class="sxs-lookup"><span data-stu-id="b4f56-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="b4f56-127">Selecteer onder **Stuklijstregels kopiëren uit verwijzing** de optie **Stuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="b4f56-128">Selecteer in het veld **Referentienummer** een stuklijstversie.</span><span class="sxs-lookup"><span data-stu-id="b4f56-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="b4f56-129">Er wordt een artikel van het type stuklijst naar het veld **Artikelnummer** gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="b4f56-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="b4f56-130">Voer in het veld **Naam** een naam voor de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="b4f56-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="b4f56-131">Voer in de velden **Datum vanaf** en **Datum t/m** een datuminterval in waarin de sjabloonstuklijst actief is.</span><span class="sxs-lookup"><span data-stu-id="b4f56-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="b4f56-132">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-132">Select **OK**.</span></span>

<span data-ttu-id="b4f56-133">Er is een nieuwe sjabloonstuklijst gemaakt met regels die overeenkomen met de regels van de stuklijst die wordt vermeld in **Stuklijsten**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="b4f56-134">Een sjabloonstuklijst maken op basis van een productiestuklijst</span><span class="sxs-lookup"><span data-stu-id="b4f56-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="b4f56-135">Selecteer **Servicebeheer** \> **Instellen** \> **Serviceobjecten** \> **Sjabloonstuklijsten**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="b4f56-136">Selecteer **Nieuw** om het formulier **Sjabloonstuklijst maken** te openen.</span><span class="sxs-lookup"><span data-stu-id="b4f56-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="b4f56-137">Selecteer onder **Stuklijstregels kopiëren uit verwijzing** de optie **Productie**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="b4f56-138">Selecteer in het veld **Referentienummer** een productiestuklijst.</span><span class="sxs-lookup"><span data-stu-id="b4f56-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="b4f56-139">Voer in het veld **Naam** een naam voor de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="b4f56-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="b4f56-140">Voer in de velden **Datum vanaf** en **Datum t/m** een datuminterval in waarin de sjabloonstuklijst actief is.</span><span class="sxs-lookup"><span data-stu-id="b4f56-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="b4f56-141">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-141">Select **OK**.</span></span>

<span data-ttu-id="b4f56-142">Er is een nieuwe sjabloonstuklijst gemaakt met regels die overeenkomen met de regels van de stuklijst die wordt vermeld in **Stuklijst**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4f56-143">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b4f56-143">See also</span></span>

[<span data-ttu-id="b4f56-144">Sjabloonstuklijsten</span><span class="sxs-lookup"><span data-stu-id="b4f56-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]