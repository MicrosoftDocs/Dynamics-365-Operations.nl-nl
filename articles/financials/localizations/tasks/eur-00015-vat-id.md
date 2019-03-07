---
title: EUR-00015 Een btw-id instellen
description: Deze procedure beschrijft de vereisten voor het registreren van de btw-id, zoals het instellen van een registratietype en het toewijzen ervan aan een registratiecategorie.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66ee7215dc21921f9d8e405c3f77d9b5e0b89a9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "371398"
---
# <a name="eur-00015-set-up-vat-id"></a><span data-ttu-id="e1fb8-103">EUR-00015 Een btw-id instellen</span><span class="sxs-lookup"><span data-stu-id="e1fb8-103">EUR-00015 Set up VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1fb8-104">Deze procedure beschrijft de vereisten voor het registreren van de btw-id, zoals het instellen van een registratietype en het toewijzen ervan aan een registratiecategorie.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="e1fb8-105">U kunt extra informatie over registratie-id's en de verwerking van registratie-id, waaronder de vereisten, vinden in het Help-onderwerp Registratie-id's.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="e1fb8-106">Deze informatie is van toepassing op alle Europese landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="e1fb8-107">De taak werd gemaakt met het demobedrijf DEMF met een primair adres van een rechtspersoon in Duitsland.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="e1fb8-108">Deze taak is bedoeld voor systeembeheerders.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-108">This task is intended for system administrators.</span></span> <span data-ttu-id="e1fb8-109">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="e1fb8-110">Ga naar Organisatiebeheer > Globaal adresboek > Registratietypen > Registratietypen.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="e1fb8-111">Klik op Nieuw om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="e1fb8-112">Typ Btw-id in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="e1fb8-113">Typ Btw-nummer in het Veld Omschrijving</span><span class="sxs-lookup"><span data-stu-id="e1fb8-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="e1fb8-114">Typ of selecteer een waarde DEU in het veld Land/regio</span><span class="sxs-lookup"><span data-stu-id="e1fb8-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="e1fb8-115">Selecteer Ja in het veld Uniek.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="e1fb8-116">Schakel dit selectievakje in om te verifiëren of de btw-id uniek is.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="e1fb8-117">Selecteer Ja in het veld Primair voor land/regio.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="e1fb8-118">Schakel dit selectievakje in als de btw-id geldig moet zijn voor alle adressen die tot het opgegeven land/regio behoren.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="e1fb8-119">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-119">Click Create.</span></span>
9. <span data-ttu-id="e1fb8-120">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-120">Click Add.</span></span>
10. <span data-ttu-id="e1fb8-121">Typ of selecteer een waarde ITA in het veld Land/regio</span><span class="sxs-lookup"><span data-stu-id="e1fb8-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="e1fb8-122">Typ ########### in het veld Indeling.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="e1fb8-123">Wanneer u een registratie-id van dit type voor het geselecteerde land of de regio invoert, wordt de registratie-id aan de hand van deze indeling gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="e1fb8-124">Schakel het selectievakje Uniek in.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="e1fb8-125">Schakel dit selectievakje in om te verifiëren of de btw-id uniek is.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="e1fb8-126">Schakel het selectievakje Primair voor land/regio in.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="e1fb8-127">Schakel dit selectievakje in als de btw-id geldig moet zijn voor alle adressen die tot het opgegeven land/regio behoren.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="e1fb8-128">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-128">Click Save.</span></span>
15. <span data-ttu-id="e1fb8-129">Ga naar Organisatiebeheer > Globaal adresboek > Registratietypen > Registratiecategorieën.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="e1fb8-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-130">Click New.</span></span>
17. <span data-ttu-id="e1fb8-131">Typ of selecteer een waarde Btw-id, DEU in het veld Land/regio</span><span class="sxs-lookup"><span data-stu-id="e1fb8-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="e1fb8-132">Selecteer Btw-id in het veld Registratiecategorie.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="e1fb8-133">Wijs het registratietype dat u eerder hebt gemaakt toe aan een vooraf gedefinieerde registratiecategorie.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="e1fb8-134">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-134">Click New.</span></span>
20. <span data-ttu-id="e1fb8-135">Typ of selecteer een waarde Btw-id, ITA in het veld Land/regio</span><span class="sxs-lookup"><span data-stu-id="e1fb8-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="e1fb8-136">Selecteer Btw-id in het veld Registratiecategorie.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="e1fb8-137">Wijs het registratietype dat u hebt gemaakt toe aan een vooraf gedefinieerde registratiecategorie.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="e1fb8-138">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e1fb8-138">Click Save.</span></span>

