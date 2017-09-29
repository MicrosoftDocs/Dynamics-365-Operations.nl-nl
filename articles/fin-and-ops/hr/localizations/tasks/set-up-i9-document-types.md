--- 
title: I-9-documenttypen instellen
description: Deze procedure laat zien hoe u documenttypen kunt bekijken en instellen die voor i-9-verificatie worden gebruikt.
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="00efd-103">I-9-documenttypen instellen</span><span class="sxs-lookup"><span data-stu-id="00efd-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="00efd-104">Deze procedure laat zien hoe u documenttypen kunt bekijken en instellen die voor i-9-verificatie worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="00efd-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="00efd-105">Voordat u de I-9-documenttypen instelt, moet u ook de uitgevende instanties en identificatietypen instellen.</span><span class="sxs-lookup"><span data-stu-id="00efd-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="00efd-106">Het demobedrijf dat wordt gebruikt om deze procedure te maken is USMF. Het bevat voorbeelden van de uitgevende instanties en identificatietypen die nodig zijn om de procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="00efd-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="00efd-107">Ga naar Human Resources > Medewerkers > I-9 > I-9-documenttypen.</span><span class="sxs-lookup"><span data-stu-id="00efd-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="00efd-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="00efd-108">Click New.</span></span>
3. <span data-ttu-id="00efd-109">Typ een waarde in het veld I-9-documenttype.</span><span class="sxs-lookup"><span data-stu-id="00efd-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="00efd-110">Voorbeeld: identiteitskaart voor school.</span><span class="sxs-lookup"><span data-stu-id="00efd-110">Example: School ID.</span></span>  
4. <span data-ttu-id="00efd-111">Selecteer het identificatietype.</span><span class="sxs-lookup"><span data-stu-id="00efd-111">Select the identification type.</span></span>  <span data-ttu-id="00efd-112">Voorbeeld: identiteitskaart voor school</span><span class="sxs-lookup"><span data-stu-id="00efd-112">Example:  School ID</span></span>
    * <span data-ttu-id="00efd-113">Voorbeelden van identificatietypen omvatten een burgerservicenummer (BSN), visumnummer, paspoort nummer of rijbewijs.</span><span class="sxs-lookup"><span data-stu-id="00efd-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="00efd-114">Selecteer de lijst met I-9-documenten die wordt gebruikt voor het documenttype.</span><span class="sxs-lookup"><span data-stu-id="00efd-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="00efd-115">Als onderdeel van het I-9-proces, moeten werknemers documentatie indienen waarmee de identiteit en werkautorisatie wordt aangetoond ten behoeve van de werkgever.</span><span class="sxs-lookup"><span data-stu-id="00efd-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="00efd-116">De website van de Amerikaanse Citizenship and Immigration Services bevat informatie over welke documenten acceptabel zijn en tot welke lijst deze behoren.</span><span class="sxs-lookup"><span data-stu-id="00efd-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="00efd-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="00efd-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="00efd-118">Voer in het veld Formulier het officiële formuliernummer voor het documenttype in.</span><span class="sxs-lookup"><span data-stu-id="00efd-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="00efd-119">Voorbeeld: identiteitskaart voor school.</span><span class="sxs-lookup"><span data-stu-id="00efd-119">Example: School ID.</span></span>
    * <span data-ttu-id="00efd-120">De officiële formuliernummers zijn te vinden op de website van de Amerikaanse Citizenship and Immigration Services.</span><span class="sxs-lookup"><span data-stu-id="00efd-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="00efd-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="00efd-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="00efd-122">Schakel het selectievakje Actief in of uit.</span><span class="sxs-lookup"><span data-stu-id="00efd-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="00efd-123">Stel in het Verlopen veld de datum in op "2019-10-27".</span><span class="sxs-lookup"><span data-stu-id="00efd-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="00efd-124">De vervaldatum is optioneel.</span><span class="sxs-lookup"><span data-stu-id="00efd-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="00efd-125">Selecteer de instantie die het documenttype heeft uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="00efd-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="00efd-126">Voorbeeld: Provincie of gebied</span><span class="sxs-lookup"><span data-stu-id="00efd-126">Example: Province/territory</span></span>
10. <span data-ttu-id="00efd-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="00efd-127">Click Save.</span></span>


