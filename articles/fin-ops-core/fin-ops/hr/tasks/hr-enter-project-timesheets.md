---
title: Projectroosters invoeren
description: Met deze procedure kunt u een urenstaat maken met behulp van een leeg urenstaatformulier.
author: andreabichsel
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a600137fc583aef8c85c920ca3cd2949a1a19d
ms.sourcegitcommit: 0cca2f82ae5c91c409e2abbf5867ff4e59ba71d6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/23/2021
ms.locfileid: "5055934"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="51e41-103">Projectroosters invoeren</span><span class="sxs-lookup"><span data-stu-id="51e41-103">Enter project timesheets</span></span>

<span data-ttu-id="51e41-104">Met deze procedure kunt u een urenstaat maken met behulp van een leeg urenstaatformulier.</span><span class="sxs-lookup"><span data-stu-id="51e41-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="51e41-105">U kunt de nieuwe urenstaat baseren op gegevens uit een vorige urenstaat of uit project- en activiteitstoewijzingen op de pagina **Mijn favorieten**.</span><span class="sxs-lookup"><span data-stu-id="51e41-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="51e41-106">Standaard geeft de lijstpagina **Alle urenstaten** al uw urenstaten weer voor de huidige periode.</span><span class="sxs-lookup"><span data-stu-id="51e41-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="51e41-107">U kunt de vervolgkeuzelijst voor het veld **Weergeven** op de pagina **Mijn urenstaten** gebruiken om de lijst van urenstaten te filteren per periode of project, of om urenstaten weer te geven die namens andere medewerkers zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="51e41-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="51e41-108">Het demobedrijf dat wordt gebruikt om deze procedure te maken is USSI.</span><span class="sxs-lookup"><span data-stu-id="51e41-108">The demo data company used to create this procedure is USSI.</span></span>  

1. <span data-ttu-id="51e41-109">Ga in het **navigatievenster** naar **Modules > Projectbeheer en boekhouding > Urenstaten > Mijn urenstaten**.</span><span class="sxs-lookup"><span data-stu-id="51e41-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="51e41-110">Als u een nieuwe urenstaat wilt invoeren, klikt u op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="51e41-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="51e41-111">De vervolgkeuzelijst Resource geeft standaard de medewerker weer die aan de huidige gebruiker is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="51e41-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="51e41-112">Als de gebruiker als gemachtigde is aangewezen, worden de namen opgesomd zodat een gebruiker een urenstaat in hun naam kan invoeren.</span><span class="sxs-lookup"><span data-stu-id="51e41-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="51e41-113">Voer een datum in het veld **Datum** in.</span><span class="sxs-lookup"><span data-stu-id="51e41-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="51e41-114">Als deze optie is geselecteerd, worden nieuwe urenstaatregels gemaakt door de instellingen voor urenstaat te gebruiken die als favorieten zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="51e41-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="51e41-115">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="51e41-115">Click **OK**.</span></span>
5. <span data-ttu-id="51e41-116">Klik op **Nieuwe regel**.</span><span class="sxs-lookup"><span data-stu-id="51e41-116">Click **New line**.</span></span>
6. <span data-ttu-id="51e41-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="51e41-117">In the list, mark the selected row.</span></span> <span data-ttu-id="51e41-118">Het veld **Rechtspersoon** geeft standaard de huidige rechtspersoon weer.</span><span class="sxs-lookup"><span data-stu-id="51e41-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="51e41-119">Klik in het veld **Project** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="51e41-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="51e41-120">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="51e41-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="51e41-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="51e41-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="51e41-122">Klik in het veld **Activiteitsnummer** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="51e41-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="51e41-123">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="51e41-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="51e41-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="51e41-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="51e41-125">Klik in het veld **Categorie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="51e41-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="51e41-126">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="51e41-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="51e41-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="51e41-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="51e41-128">Voer het aantal uren in dat elke dag is gewerkt.</span><span class="sxs-lookup"><span data-stu-id="51e41-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="51e41-129">Voer de uren in een decimale notatie in.</span><span class="sxs-lookup"><span data-stu-id="51e41-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="51e41-130">Als u bijvoorbeeld twee uur en vijftien minuten hebt gewerkt, voert u 2,25 in.</span><span class="sxs-lookup"><span data-stu-id="51e41-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="51e41-131">In **Regeldetails** zijn de volgende opties beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="51e41-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="51e41-132">Voeg informatie toe over belastingen en financiële dimensies op het tabblad **Algemeen** en het tabblad **Financiële dimensies**.</span><span class="sxs-lookup"><span data-stu-id="51e41-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="51e41-133">Voeg opmerkingen toe over de urenstaatregel toe op het tabblad **Opmerking**.</span><span class="sxs-lookup"><span data-stu-id="51e41-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="51e41-134">Klik in het **actievenster** op **Workflow** om het dialoogvenster voor beëindigen te openen.</span><span class="sxs-lookup"><span data-stu-id="51e41-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="51e41-135">Klik op **Aanbieden**.</span><span class="sxs-lookup"><span data-stu-id="51e41-135">Click **Submit**.</span></span>
22. <span data-ttu-id="51e41-136">Klik op **Aanbieden**.</span><span class="sxs-lookup"><span data-stu-id="51e41-136">Click **Submit**.</span></span>

