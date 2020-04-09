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
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138331"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="dcd40-103">Financiële dimensies definiëren</span><span class="sxs-lookup"><span data-stu-id="dcd40-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcd40-104">Deze taakhandleiding toont het toevoegen van een door een entiteit ondersteunde financiële dimensie en een aangepaste financiële dimensie.</span><span class="sxs-lookup"><span data-stu-id="dcd40-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="dcd40-105">De taakbegeleiding gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="dcd40-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="dcd40-106">Een door een entiteit ondersteunde financiële dimensie maken</span><span class="sxs-lookup"><span data-stu-id="dcd40-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="dcd40-107">Ga naar **Navigatievenster > Modules > Grootboek > Rekeningschema > Dimensies > Financiële dimensies**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="dcd40-108">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-108">Click **New**.</span></span>
3. <span data-ttu-id="dcd40-109">Selecteer in het formulierveld **Gebruikerswaarden** een door het systeem gedefinieerde entiteit waarop de financiële dimensie moet worden gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="dcd40-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="dcd40-110">Typ in het veld **Dimensienaam** een waarde om de financiële dimensie te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="dcd40-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="dcd40-111">De naam kan anders zijn dan de door het systeem gedefinieerde entiteit maar kan geen spaties of speciale tekens bevatten.</span><span class="sxs-lookup"><span data-stu-id="dcd40-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="dcd40-112">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-112">Click **Activate**.</span></span> <span data-ttu-id="dcd40-113">Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist.</span><span class="sxs-lookup"><span data-stu-id="dcd40-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="dcd40-114">U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet gebruiken voordat deze is geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="dcd40-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="dcd40-115">Klik in het activeringbericht op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="dcd40-116">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-116">Click **Activate**.</span></span> <span data-ttu-id="dcd40-117">U kunt de activering van een dimensie inplannen om op een specifieke datum en tijd in batch te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="dcd40-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="dcd40-118">Klik in het **actievenster** op **Dimensiewaarden**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="dcd40-119">Sommige dimensiewaarden zijn bedrijfsspecifiek.</span><span class="sxs-lookup"><span data-stu-id="dcd40-119">Some dimension values are company specific.</span></span> <span data-ttu-id="dcd40-120">U kunt controleren of deze bedrijfsspecifiek zijn: als de bedrijfsnaam in de lijst van dimensiewaarden wordt weergeven.</span><span class="sxs-lookup"><span data-stu-id="dcd40-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="dcd40-121">Een aangepaste financiële dimensie maken</span><span class="sxs-lookup"><span data-stu-id="dcd40-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="dcd40-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="dcd40-122">Close the page.</span></span>
2. <span data-ttu-id="dcd40-123">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-123">Click **New**.</span></span>
3. <span data-ttu-id="dcd40-124">Selecteer **Aangepaste dimensie** in het veld **Waarden gebruiken van**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="dcd40-125">Typ in het veld **Dimensienaam** een waarde om de financiële dimensie te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="dcd40-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="dcd40-126">De naam mag geen spaties of speciale tekens bevatten.</span><span class="sxs-lookup"><span data-stu-id="dcd40-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="dcd40-127">U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die u voor dimensiewaarden kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="dcd40-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="dcd40-128">U kunt tekens zoals letters of een koppelteken invoeren die voor elke dimensiewaarde hetzelfde blijven.</span><span class="sxs-lookup"><span data-stu-id="dcd40-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="dcd40-129">U kunt hekjes (#) en invoeren, evenals en-tekens (&) die dienen als tijdelijke aanduidingen voor letters en cijfers die elke keer worden gewijzigd als een dimensiewaarde wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dcd40-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="dcd40-130">Gebruik een hekje (#) als tijdelijke aanduiding voor een cijfer en een en-teken (&) als tijdelijke aanduiding voor een letter.</span><span class="sxs-lookup"><span data-stu-id="dcd40-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="dcd40-131">Voorbeeld: om de waarde van de letters tot CC en drie nummers te beperken, voert u CC-### als opmaakmasker in.</span><span class="sxs-lookup"><span data-stu-id="dcd40-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="dcd40-132">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-132">Click **Activate**.</span></span> <span data-ttu-id="dcd40-133">Bij het activeren van de financiële dimensie wordt de tabel met de financiële dimensienaam bijgewerkt en worden verwijderde dimensies gewist.</span><span class="sxs-lookup"><span data-stu-id="dcd40-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="dcd40-134">U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert, maar u kunt een financiële dimensie niet gebruiken voordat deze is geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="dcd40-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="dcd40-135">Klik op **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-135">Click **Activate**.</span></span> <span data-ttu-id="dcd40-136">U kunt de activering van een dimensie inplannen om op een specifieke datum en tijd in batch te worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="dcd40-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="dcd40-137">Klik in het **actievenster** op **Dimensiewaarden**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="dcd40-138">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="dcd40-138">Click **New**.</span></span>
9. <span data-ttu-id="dcd40-139">Typ in het veld **Dimensiewaarde** een naam om uw waarde van financiële dimensie te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="dcd40-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="dcd40-140">Typ in het veld **Beschrijving** een beschrijving die uw waarde van financiële dimensie beschrijft.</span><span class="sxs-lookup"><span data-stu-id="dcd40-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>

