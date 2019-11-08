---
title: Financiële dimensies definiëren
description: Deze taakhandleiding toont het toevoegen van een door een entiteit ondersteunde financiële dimensie en een aangepaste financiële dimensie.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb2dc5df96198f3c9f68fcac70b2e5dcbe8c8832
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175369"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="a0faa-103">Financiële dimensies definiëren</span><span class="sxs-lookup"><span data-stu-id="a0faa-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0faa-104">Deze taakhandleiding toont het toevoegen van een door een entiteit ondersteunde financiële dimensie en een aangepaste financiële dimensie.</span><span class="sxs-lookup"><span data-stu-id="a0faa-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="a0faa-105">De taakbegeleiding gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="a0faa-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="a0faa-106">Een door een entiteit ondersteunde financiële dimensie maken</span><span class="sxs-lookup"><span data-stu-id="a0faa-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="a0faa-107">Ga naar **Navigatievenster > Modules > Grootboek > Rekeningschema > Dimensies > Financiële dimensies**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="a0faa-108">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-108">Click **New**.</span></span>
3. <span data-ttu-id="a0faa-109">Selecteer in het formulierveld **Gebruikerswaarden** een door het systeem gedefinieerde entiteit waarop de financiële dimensie moet worden gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="a0faa-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="a0faa-110">Typ in het veld **Dimensienaam** een waarde om de financiële dimensie te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="a0faa-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="a0faa-111">De naam kan anders zijn dan de door het systeem gedefinieerde entiteit maar kan geen spaties of speciale tekens bevatten.</span><span class="sxs-lookup"><span data-stu-id="a0faa-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="a0faa-112">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-112">Click **Activate**.</span></span> <span data-ttu-id="a0faa-113">Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist.</span><span class="sxs-lookup"><span data-stu-id="a0faa-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="a0faa-114">U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet gebruiken voordat deze is geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="a0faa-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="a0faa-115">Klik in het activeringbericht op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="a0faa-116">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-116">Click **Activate**.</span></span> <span data-ttu-id="a0faa-117">U kunt de activering van een dimensie inplannen om op een specifieke datum en tijd in batch te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a0faa-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="a0faa-118">Klik in het **actievenster** op **Dimensiewaarden**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="a0faa-119">Sommige dimensiewaarden zijn bedrijfsspecifiek.</span><span class="sxs-lookup"><span data-stu-id="a0faa-119">Some dimension values are company specific.</span></span> <span data-ttu-id="a0faa-120">U kunt controleren of deze bedrijfsspecifiek zijn: als de bedrijfsnaam in de lijst van dimensiewaarden wordt weergeven.</span><span class="sxs-lookup"><span data-stu-id="a0faa-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="a0faa-121">Een aangepaste financiële dimensie maken</span><span class="sxs-lookup"><span data-stu-id="a0faa-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="a0faa-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a0faa-122">Close the page.</span></span>
2. <span data-ttu-id="a0faa-123">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-123">Click **New**.</span></span>
3. <span data-ttu-id="a0faa-124">Selecteer **Aangepaste dimensie** in het veld **Waarden gebruiken van**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="a0faa-125">Typ in het veld **Dimensienaam** een waarde om de financiële dimensie te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="a0faa-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="a0faa-126">De naam mag geen spaties of speciale tekens bevatten.</span><span class="sxs-lookup"><span data-stu-id="a0faa-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="a0faa-127">U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die u voor dimensiewaarden kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="a0faa-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="a0faa-128">U kunt tekens zoals letters of een koppelteken invoeren die voor elke dimensiewaarde hetzelfde blijven.</span><span class="sxs-lookup"><span data-stu-id="a0faa-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="a0faa-129">U kunt hekjes (#) en invoeren, evenals en-tekens (&) die dienen als tijdelijke aanduidingen voor letters en cijfers die elke keer worden gewijzigd als een dimensiewaarde wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a0faa-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="a0faa-130">Gebruik een hekje (#) als tijdelijke aanduiding voor een cijfer en een en-teken (&) als tijdelijke aanduiding voor een letter.</span><span class="sxs-lookup"><span data-stu-id="a0faa-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="a0faa-131">Voorbeeld: om de waarde van de letters tot CC en drie nummers te beperken, voert u CC-### als opmaakmasker in.</span><span class="sxs-lookup"><span data-stu-id="a0faa-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="a0faa-132">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-132">Click **Activate**.</span></span> <span data-ttu-id="a0faa-133">Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist.</span><span class="sxs-lookup"><span data-stu-id="a0faa-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="a0faa-134">U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet gebruiken voordat deze is geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="a0faa-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="a0faa-135">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-135">Click **Activate**.</span></span> <span data-ttu-id="a0faa-136">U kunt de activering van een dimensie inplannen om op een specifieke datum en tijd in batch te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a0faa-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="a0faa-137">Klik in het **actievenster** op **Dimensiewaarden**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="a0faa-138">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a0faa-138">Click **New**.</span></span>
9. <span data-ttu-id="a0faa-139">Typ in het veld **Dimensiewaarde** een naam om uw waarde van financiële dimensie te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="a0faa-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="a0faa-140">Typ in het veld **Beschrijving** een beschrijving die uw waarde van financiële dimensie beschrijft.</span><span class="sxs-lookup"><span data-stu-id="a0faa-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>
