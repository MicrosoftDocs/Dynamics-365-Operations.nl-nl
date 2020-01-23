---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (23 januari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f97462f088fc1a3cb94f2a34204fc09f1cd66fb0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899123"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a><span data-ttu-id="94731-103">Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (23 januari 2019)</span><span class="sxs-lookup"><span data-stu-id="94731-103">What's new or changed in Dynamics 365 Talent - Core HR (January 23, 2019)</span></span>

<span data-ttu-id="94731-104">**Build 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="94731-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="94731-105">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.</span><span class="sxs-lookup"><span data-stu-id="94731-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="94731-106">Wijzigingen</span><span class="sxs-lookup"><span data-stu-id="94731-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="94731-107">Import van vaste compensatie van werknemers werkt niet bij het maken van nieuwe records voor vaste compensatie</span><span class="sxs-lookup"><span data-stu-id="94731-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="94731-108">Er is een wijziging aangebracht in de entiteit voor vaste compensatie van werknemers om het compensatieniveau tijdens het importeren op te halen.</span><span class="sxs-lookup"><span data-stu-id="94731-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="94731-109">Vóór deze release werd een bericht weergegeven dat het niveau vereist was.</span><span class="sxs-lookup"><span data-stu-id="94731-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="94731-110">Het veld Minimumsaldo is verwijderd uit het dialoogvenster voor verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="94731-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="94731-111">Het veld **Minimumsaldo** is verwijderd uit het dialoogvenster **Verlofaanvraag**.</span><span class="sxs-lookup"><span data-stu-id="94731-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="94731-112">Deze wijziging geldt voor alle gebieden waarin verlof kan worden aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="94731-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="94731-113">Gegevensupgrade voor compensatieniveaus wordt niet in alle scenario's bijgewerkt</span><span class="sxs-lookup"><span data-stu-id="94731-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="94731-114">Er is een wijziging aangebracht om het compensatieniveau in plannen voor vaste compensatie bij te werken.</span><span class="sxs-lookup"><span data-stu-id="94731-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="94731-115">Met deze wijziging wordt het compensatieniveau voor vaste plannen ingevuld voor de functie die is toegewezen aan de werknemer.</span><span class="sxs-lookup"><span data-stu-id="94731-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="94731-116">Salarisinformatie op de pagina Wijzigingen beheren is alleen beschikbaar wanneer is aangemeld als systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="94731-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="94731-117">Met deze wijziging kunnen werknemers met de rol Salarisadministrateur toegang krijgen tot de salarisgegevens op de pagina **Tijdlijn van wijzigingen > Wijzigingen beheren** voor de functie.</span><span class="sxs-lookup"><span data-stu-id="94731-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="94731-118">Functievelden worden standaard ingesteld op posities</span><span class="sxs-lookup"><span data-stu-id="94731-118">Job fields default to positions</span></span>
<span data-ttu-id="94731-119">Bij het wijzigen van de functie voor een positie worden functievelden standaard ingesteld op de positie.</span><span class="sxs-lookup"><span data-stu-id="94731-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="94731-120">Een waarschuwingsbericht wordt weergegeven waarin een optie wordt gegeven om de standaardwaarden te accepteren of de bestaande waarden voor deze velden te behouden.</span><span class="sxs-lookup"><span data-stu-id="94731-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="94731-121">Proeftijd en kalender worden niet weergegeven voor werknemers die voor de toekomst zijn aangenomen.</span><span class="sxs-lookup"><span data-stu-id="94731-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="94731-122">Met deze wijziging zijn de velden **Proeftijd** en **Kalender** toegevoegd aan de pagina **Wijzigingen beheren** zodat gegevens voor toekomstige en eerdere werknemers kunnen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="94731-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23-for-finance-and-operations"></a><span data-ttu-id="94731-123">Platformupdate 23 voor Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94731-123">Platform update 23 for Finance and Operations</span></span>
<span data-ttu-id="94731-124">Kleine correcties zijn opgenomen als onderdeel van platformupdate 23 voor Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="94731-124">Minor bug fixes have been included as part of Platform update 23 for Finance and Operations.</span></span> <span data-ttu-id="94731-125">Zie voor meer informatie [Wat is nieuw of gewijzigd in Dynamics 365 Finance and Operations platformupdate 23 (januari 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="94731-125">For more information, see [What's new or changed in Dynamics 365 Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
