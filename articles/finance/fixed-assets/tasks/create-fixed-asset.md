---
title: Een vast activum maken
description: In dit onderwerp wordt uitgelegd hoe u een nieuwe record voor vaste activa kunt maken op de lijstpagina Vaste activa.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 481bdb55b813dad5366f382ae35d8345b0e67d9f
ms.sourcegitcommit: a9efbd69f2670fd6ba0ad0babf304fc206d01249
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2020
ms.locfileid: "4442191"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="aa31e-103">Een vast activum maken</span><span class="sxs-lookup"><span data-stu-id="aa31e-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa31e-104">In dit onderwerp wordt uitgelegd hoe u een nieuwe record voor vaste activa kunt maken op de lijstpagina **Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="aa31e-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="aa31e-105">Het activumnummer wordt toegewezen op basis van de nummerreeks die is toegewezen aan de groep met vaste activa.</span><span class="sxs-lookup"><span data-stu-id="aa31e-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="aa31e-106">Als u de sjabloon voor vaste activa gebruikt om activa te importeren via de invoegtoepassing Microsoft Excel of als u een andere importtaak gebruikt, worden automatisch records voor vaste activa gemaakt en wordt het activanummer verhoogd.</span><span class="sxs-lookup"><span data-stu-id="aa31e-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="aa31e-107">Voer de volgende stappen uit om handmatig een activarecord te maken.</span><span class="sxs-lookup"><span data-stu-id="aa31e-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="aa31e-108">Ga naar **Navigatievenster \> Modules \> Vaste activa \> Vaste activa \> Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="aa31e-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="aa31e-109">Selecteer **Nieuw** in het **Actievenster**.</span><span class="sxs-lookup"><span data-stu-id="aa31e-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="aa31e-110">Typ of selecteer een waarde in het veld **Groep vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="aa31e-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="aa31e-111">Het veld **Nummer** wordt standaard ingevuld als u de functionaliteit **Vaste activa automatisch nummeren** in de parameters **Vaste activa** en de **vaste-activagroep** hebt ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="aa31e-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="aa31e-112">Zo niet, dan moet u een uniek nummer invoeren om het vaste activum te identificeren.</span><span class="sxs-lookup"><span data-stu-id="aa31e-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="aa31e-113">Voer een waarde in het veld **Naam** in.</span><span class="sxs-lookup"><span data-stu-id="aa31e-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="aa31e-114">Voer aanvullende informatie in die uw bedrijf voor dit activum nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="aa31e-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="aa31e-115">Selecteer **Boeken** in het **Actievenster**.</span><span class="sxs-lookup"><span data-stu-id="aa31e-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="aa31e-116">Voer in het veld **Verwervingsdatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="aa31e-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="aa31e-117">Voer een nummer in het veld **Aanschafprijs** in.</span><span class="sxs-lookup"><span data-stu-id="aa31e-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="aa31e-118">Voer aanvullende informatie in die uw bedrijf voor dit boek nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="aa31e-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="aa31e-119">Voer aanvullende informatie in die uw bedrijf voor de resterende boeken nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="aa31e-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="aa31e-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="aa31e-120">Close the page.</span></span>

<span data-ttu-id="aa31e-121">U kunt vaste activa ook importeren met de Excel-invoegtoepassing of door een importtaak uit te voeren vanuit de werkruimte **Gegevensbeheer**.</span><span class="sxs-lookup"><span data-stu-id="aa31e-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="aa31e-122">Voer voordat u de import uitvoert de waarden voor vereiste velden in de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="aa31e-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="aa31e-123">Als u het nummer van de vaste activa niet hebt gedefinieerd in de sjabloon van de Excel-invoegtoepassing of in Gegevensbeheer, wordt een nummer voor vaste activa gemaakt voor elk geïmporteerd activum en wordt de nummerreeks voor elk geïmporteerd activum automatisch verhoogd.</span><span class="sxs-lookup"><span data-stu-id="aa31e-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="aa31e-124">Als u echter activa importeert en activanummers definieert in de sjabloon, wordt de nummerreeks **niet** automatisch verhoogd.</span><span class="sxs-lookup"><span data-stu-id="aa31e-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="aa31e-125">In dit geval moet een beheerder de nummerreeks mogelijk handmatig bijwerken.</span><span class="sxs-lookup"><span data-stu-id="aa31e-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="aa31e-126">Als u het nummer voor vaste activa in de sjabloon van de Excel-invoegtoepassing hebt gedefinieerd, wordt het gedefinieerde nummer voor vaste activa gebruikt en wordt de nummerreeks verhoogd.</span><span class="sxs-lookup"><span data-stu-id="aa31e-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="aa31e-127">Nadat de afschrijving is geboekt, worden de velden **In gebruik genomen** en **Uitvoeringsdatum afschrijving** vergrendeld op de pagina **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="aa31e-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="aa31e-128">Bovendien worden beide velden niet bijgewerkt vanuit de gegevensentiteit.</span><span class="sxs-lookup"><span data-stu-id="aa31e-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="aa31e-129">De vaste-activarecord wordt niet verwijderd als er transacties naar het gekoppelde boek worden geboekt of als het nieuwe vaste activum op een journaalregel wordt ingevoerd maar niet wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="aa31e-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 
