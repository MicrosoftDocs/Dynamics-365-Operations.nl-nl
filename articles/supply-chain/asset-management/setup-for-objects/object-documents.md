---
title: Activadocumenten
description: In dit onderwerp worden activadocumenten in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f8bcae99a96ccd83dc4543b1c56007a4263a19b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021674"
---
# <a name="asset-documents"></a><span data-ttu-id="92862-103">Activadocumenten</span><span class="sxs-lookup"><span data-stu-id="92862-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="92862-104">In dit onderwerp worden activadocumenten in Activabeheer uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="92862-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="92862-105">In Activabeheer kunt u documenten zo instellen dat deze automatisch worden gekoppeld aan bijvoorbeeld taaktypen, activafabrikanten, activatypen of activa.</span><span class="sxs-lookup"><span data-stu-id="92862-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="92862-106">Deze functionaliteit is handig wanneer bijgewerkte documentversies worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="92862-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="92862-107">In dat geval hoeft u alleen het bijgewerkte document op de standaardlocatie te plaatsen die u voor uw documenten in Supply Chain Management gebruikt en het document te koppelen aan de activadocumentrecord die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="92862-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="92862-108">Het bijgewerkte document kan vervolgens worden geopend vanuit de menuopties **Alle activa**, **Actieve activa**, **Mijn actieve activa**, **Alle werkorders** en **Actieve werkordertaken**.</span><span class="sxs-lookup"><span data-stu-id="92862-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="92862-109">Bij het proces voor het koppelen van documenten aan een activadocumentrecord wordt gebruikgemaakt van het standaardsysteem voor documentverwerking.</span><span class="sxs-lookup"><span data-stu-id="92862-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="92862-110">**Voorbeeld 1:** een document dat is gerelateerd aan een taaktype kan een procedure voor dat taaktype beschrijven.</span><span class="sxs-lookup"><span data-stu-id="92862-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="92862-111">**Voorbeeld 2:** een document dat is gerelateerd aan een combinatie van een activatype, fabrikant en model kan de standaardhandleiding zijn voor het geselecteerde model van de activafabrikant.</span><span class="sxs-lookup"><span data-stu-id="92862-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="92862-112">Activadocumentrelatie maken</span><span class="sxs-lookup"><span data-stu-id="92862-112">Create asset document relation</span></span>

1. <span data-ttu-id="92862-113">Selecteer **Activabeheer** \> **Instellingen** \> **Activadocumenten**.</span><span class="sxs-lookup"><span data-stu-id="92862-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="92862-114">Selecteer **Nieuw** om een activadocumentrecord te maken.</span><span class="sxs-lookup"><span data-stu-id="92862-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="92862-115">Afhankelijk van hoe specifiek u de documentrelatie witl maken, voert u relevante selecties uit in een of meer van de volgende velden: **Activatype**, **Fabrikant**, **Model**, **Activum**, **Categorie van taaktype**, **Taaktype**, **Variant van taaktype** en **Taakbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="92862-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="92862-116">De opties die beschikbaar zijn in de velden **Variant van taaktype** en **Taakbehoefte** zijn afhankelijk van uw selectie in het veld **Taaktype**.</span><span class="sxs-lookup"><span data-stu-id="92862-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92862-117">Wanneer het systeem zoekt naar documenten die gerelateerd moeten zijn aan een activum of een werkorder, doorloopt Activabeheer alle activadocumentrecords om te controleren op een mogelijke overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="92862-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="92862-118">De meest specifieke combinatie wordt altijd als eerste gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="92862-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="92862-119">Met andere woorden, Activabeheer controleert eerst op een overeenkomst voor het veld **Taakbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="92862-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="92862-120">Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Variant van taaktype**.</span><span class="sxs-lookup"><span data-stu-id="92862-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="92862-121">Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Taaktype** enzovoort.</span><span class="sxs-lookup"><span data-stu-id="92862-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="92862-122">Zoals u kunt zien in de indeling van de pagina **Activadocumenten**, betekent dit gedrag dat Activabeheer elke record van rechts naar links controleert op overeenkomst om de meest specifieke combinatie te vinden.</span><span class="sxs-lookup"><span data-stu-id="92862-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="92862-123">Verschillende documenten zijn mogelijk gerelateerd aan een activum of een werkorder.</span><span class="sxs-lookup"><span data-stu-id="92862-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="92862-124">U kunt het serviceniveau voor een onderhoudsaanvraag of een werkorder naar behoefte bewerken.</span><span class="sxs-lookup"><span data-stu-id="92862-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="92862-125">Selecteer **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="92862-125">Select **Attachments**.</span></span> <span data-ttu-id="92862-126">De standaardpagina **Documentverwerking** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="92862-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="92862-127">Stel de documenten of notities in die aan de activadocumentrecord moeten worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="92862-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="92862-128">Nadat u documenten hebt gekoppeld, wordt in het veld **Bijlagen** het aantal documenten weergegeven dat aan de record is gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="92862-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
