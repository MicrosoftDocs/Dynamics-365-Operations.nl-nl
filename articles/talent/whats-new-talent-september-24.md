---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (24 september 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 94950fbe5c1aad3dfbd3de59d1bcb47337ff68ea
ms.openlocfilehash: aeb75fe4c775b9003c6429de536498f495224098
ms.contentlocale: nl-nl
ms.lasthandoff: 09/24/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a><span data-ttu-id="eb8b0-103">Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (24 september 2018)</span><span class="sxs-lookup"><span data-stu-id="eb8b0-103">What's new or changed in Dynamics 365 for Talent Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eb8b0-104">**Build 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="eb8b0-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="eb8b0-105">In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="eb8b0-106">Valuta toegevoegd aan Vergoedingen</span><span class="sxs-lookup"><span data-stu-id="eb8b0-106">Currency added to Benefits</span></span>

<span data-ttu-id="eb8b0-107">Vergoedingsplannen zijn bijgewerkt om de valuta van de vergoeding te bevatten.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="eb8b0-108">Dit nieuwe veld is ook beschikbaar in Vergoedingen waarvoor medewerker zich heeft ingeschreven.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="eb8b0-109">Dit nieuwe veld maakt deel uit van de beveiligingsbevoegdheden Vergoedingen onderhouden en Een lijst met vergoedingen weergeven.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="eb8b0-110">Proces voor betaling naar rato bijwerken – Verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="eb8b0-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="eb8b0-111">Organisaties kennen vrije tijd verschillend toe, afhankelijk van wanneer werknemers in dienst treden of het bedrijf verlaten.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="eb8b0-112">Voor sommige werknemers die de organisatie verlaten, moet de toekenning mogelijk op de ontslagdatum eindigen terwijl voor anderen het toerekeningsproces op de laatste gewerkte dag wordt beëindigd.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="eb8b0-113">Deze wijzigingen bieden organisaties de mogelijkheid om te kiezen wanneer de inschrijving moet worden beëindigd tijdens het ontslagproces.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="eb8b0-114">Deze nieuwe opties maken deel uit van de bevoegdheden Een werknemer ontslaan en Een medewerker ontslaan vanuit de Selfservice manager.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="eb8b0-115">Andere wijzigingen</span><span class="sxs-lookup"><span data-stu-id="eb8b0-115">Other changes</span></span>

<span data-ttu-id="eb8b0-116">Deze versie bevat verschillende aanvullende correcties.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="eb8b0-117">Bekend probleem</span><span class="sxs-lookup"><span data-stu-id="eb8b0-117">Known Issue</span></span>

-   <span data-ttu-id="eb8b0-118">**Probleem:** als een nieuwe bijlage wordt toegevoegd aan een werknemer, zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar. **Oplossing:** voordat u de pagina van de bijlage opent, controleert u of de feitenblokken op de pagina **Werknemer** zijn gesloten.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="eb8b0-119">Als de feitenblokken zijn gesloten wanneer de pagina **Werknemer** wordt geladen, worden de knoppen voor bijlagen ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="eb8b0-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="eb8b0-120">(Dit probleem wordt opgelost in de volgende platformupdate.)</span><span class="sxs-lookup"><span data-stu-id="eb8b0-120">(This issue will be fixed in the next platform update.)</span></span>

