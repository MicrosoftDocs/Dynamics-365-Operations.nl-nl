---
title: Sollicitant- en sollicitatiegegevens handmatig invoeren
description: Deze procedure laat zien hoe u handmatig informatie over sollicitanten en hun sollicitatie kunt onderhouden.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea61e3c1d76ade6e0d694b4b521e4be76fc8799d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507712"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="5d1cf-103">Sollicitant- en sollicitatiegegevens handmatig invoeren</span><span class="sxs-lookup"><span data-stu-id="5d1cf-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d1cf-104">Deze procedure laat zien hoe u handmatig informatie over sollicitanten en hun sollicitatie kunt onderhouden.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="5d1cf-105">U kunt persoonlijke gegevens, gespreksdatums en -tijden, verwijzingen, vaardigheden en accommodatieaanvragen voor sollicitanten invoeren en onderhouden.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="5d1cf-106">U kunt ook de status van de sollicitaties van sollicitanten naar vacatures bijwerken en brieven of e-mailberichten opstellen om met sollicitanten te communiceren.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="5d1cf-107">Wanneer u sollicitatieregistratie maakt, wordt er een persoonlijke registratie voor die sollicitant in het globale adresboek gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="5d1cf-108">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="5d1cf-109">Een nieuwe sollicitantrecord maken</span><span class="sxs-lookup"><span data-stu-id="5d1cf-109">Create a new applicant record</span></span>
1. <span data-ttu-id="5d1cf-110">Ga naar Human resources > Werving > Sollicitanten > Sollicitanten.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="5d1cf-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-111">Click New.</span></span>
3. <span data-ttu-id="5d1cf-112">Typ een waarde in het veld Voornaam.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="5d1cf-113">Typ een waarde in het veld Achternaam.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="5d1cf-114">U kunt extra informatie over de sollicitant invoeren als deze beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="5d1cf-115">Zo kunt u bijvoorbeeld de hoogste graad van de sollicitant, de huidige functie of de vorige werkgever van de sollicitant opnemen.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="5d1cf-116">Schakel de uitbreiding van de sectie Contactgegevens om.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="5d1cf-117">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-117">Click Add.</span></span>
7. <span data-ttu-id="5d1cf-118">Typ in het veld Beschrijving de tekst "E-mail voor communicatie".</span><span class="sxs-lookup"><span data-stu-id="5d1cf-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="5d1cf-119">Selecteer een optie in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="5d1cf-120">Typ een waarde in het veld Contactnummer/-adres.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="5d1cf-121">Dit e-mailadres wordt gebruikt om e-mailcommunicatie met de sollicitant te genereren.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="5d1cf-122">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-122">Click Add.</span></span>
11. <span data-ttu-id="5d1cf-123">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="5d1cf-124">Typ een waarde in het veld Contactnummer/-adres.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="5d1cf-125">Persoonlijke gegevens van sollicitant.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="5d1cf-126">U kunt extra persoonlijke gegevens van de sollicitant invoeren, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="5d1cf-127">Dit kan bijvoorbeeld geboortedatum, etnische afkomst, geslacht of burgerlijke staat zijn.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="5d1cf-128">Klik in het actievenster op Competenties.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="5d1cf-129">U kunt het competentieprofiel van de sollicitant invoeren, met inbegrip van diens vaardigheden, beroepservaringen, opleiding, testen of certificaten.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="5d1cf-130">Deze informatie kan worden gebruikt om de vaardigheden van de sollicitant toe te wijzen aan de vaardigheden die zijn gekoppeld aan de functies die zijn gedefinieerd in de gegevens van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="5d1cf-131">Een sollicitatie maken voor de sollicitant</span><span class="sxs-lookup"><span data-stu-id="5d1cf-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="5d1cf-132">Klik op Sollicitaties.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-132">Click Applications.</span></span>
2. <span data-ttu-id="5d1cf-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-133">Click New.</span></span>
3. <span data-ttu-id="5d1cf-134">Klik in het veld Wervingsproject op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5d1cf-135">Door een wervingsproject te selecteren, wordt de sollicitant aan de specifieke vacature gekoppeld die is opgenomen in dat wervingsproject.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="5d1cf-136">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5d1cf-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5d1cf-138">Standaard zijn de taak en de afdeling gebaseerd op het geselecteerde wervingsproject.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="5d1cf-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-139">Click Save.</span></span>
    * <span data-ttu-id="5d1cf-140">Nadat u de sollicitatie hebt opgeslagen, kunt u er documenten aan toevoegen, met inbegrip van de ervaring van de sollicitant, bekroningen en begeleidende brief.</span><span class="sxs-lookup"><span data-stu-id="5d1cf-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

