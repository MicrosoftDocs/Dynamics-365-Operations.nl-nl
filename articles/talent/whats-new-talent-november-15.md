---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (15 november 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a><span data-ttu-id="03e50-103">Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (15 november 2018)</span><span class="sxs-lookup"><span data-stu-id="03e50-103">What's new or changed in Dynamics 365 for Talent Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03e50-104">**Build 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="03e50-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="03e50-105">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.</span><span class="sxs-lookup"><span data-stu-id="03e50-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="03e50-106">Andere wijzigingen/oplossingen</span><span class="sxs-lookup"><span data-stu-id="03e50-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="03e50-107">Kan de huidige positie van een werknemer niet wijzigen in een toekomstige open positie</span><span class="sxs-lookup"><span data-stu-id="03e50-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="03e50-108">Er is een wijziging doorgevoerd om positiewijzigingen mogelijk te maken wanneer de positie alleen in de toekomst beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="03e50-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="03e50-109">De positie wordt niet weergegeven bij het maken van een nieuwe werknemer</span><span class="sxs-lookup"><span data-stu-id="03e50-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="03e50-110">Er is een wijziging doorgevoerd om alle openstaande posities weer te geven die beschikbaar zijn voor toewijzing wanneer er nieuwe werknemers worden aangenomen in Talent.</span><span class="sxs-lookup"><span data-stu-id="03e50-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="03e50-111">Dit zijn ook historische posities of posities met een toekomstige datum.</span><span class="sxs-lookup"><span data-stu-id="03e50-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="03e50-112">Posities worden nu correct weergegeven op basis van de begindatum van het dienstverband.</span><span class="sxs-lookup"><span data-stu-id="03e50-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="03e50-113">De ontslagdatum wordt weergegeven op basis van gebruikersinstellingen</span><span class="sxs-lookup"><span data-stu-id="03e50-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="03e50-114">Er is een wijziging doorgevoerd in de lijst met vroegere werknemers om eventuele tijdzoneverschillen met de voorkeurstijdzone van werknemers bij het weergeven van de ontslagdatum te compenseren.</span><span class="sxs-lookup"><span data-stu-id="03e50-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="03e50-115">De koppelingen Aan mij toegewezen werkitems bevatten niet de juiste informatie</span><span class="sxs-lookup"><span data-stu-id="03e50-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="03e50-116">Met deze wijziging wordt bij navigatie naar de details van de afzonderlijke werkitems in de lijst de juiste informatie voor het geselecteerde item weergegeven.</span><span class="sxs-lookup"><span data-stu-id="03e50-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="03e50-117">Dit probleem trad alleen op bij geavanceerde beveiligingsopties.</span><span class="sxs-lookup"><span data-stu-id="03e50-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="03e50-118">Bekend probleem</span><span class="sxs-lookup"><span data-stu-id="03e50-118">Known issue</span></span>

- <span data-ttu-id="03e50-119">**Probleem**: bij het toevoegen van een nieuwe bijlage aan een werknemer zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="03e50-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="03e50-120">**Tijdelijke oplossing:** voordat u de bijlagepagina opent, controleert u of de feitenvakken op de pagina **Werknemer** zijn gesloten.</span><span class="sxs-lookup"><span data-stu-id="03e50-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="03e50-121">Als de feitenvakken worden gesloten wanneer de pagina **Werknemer** wordt geladen, worden de bijlageknoppen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="03e50-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="03e50-122">(Dit probleem wordt opgelost in de volgende platformupdate.)</span><span class="sxs-lookup"><span data-stu-id="03e50-122">(This issue will be fixed in the next platform update.)</span></span>

