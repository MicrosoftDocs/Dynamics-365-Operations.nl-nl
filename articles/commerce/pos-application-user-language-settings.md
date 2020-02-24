---
title: Taalinstellingen voor verkooppunttoepassing (POS) en gebruiker
description: In dit onderwerp wordt beschreven hoe u taalinstellingen wijzigt in Modern POS (MPOS) en Cloud POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49bfcaa4c05ea8e6cc6bf0a8f855f2474cea35bc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022186"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="1ad7b-103">Taalinstellingen voor verkooppunttoepassing (POS) en gebruiker</span><span class="sxs-lookup"><span data-stu-id="1ad7b-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ad7b-104">In dit onderwerp wordt beschreven hoe u taalinstellingen wijzigt in Modern POS (MPOS) en Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="1ad7b-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="1ad7b-105">Overview</span></span>
<span data-ttu-id="1ad7b-106">Modern POS (MPOS) en Cloud POS ondersteunen omgevingen waar de taalinstellingen en vertalingen tussen de winkel- en de gebruikerinstellingen kunnen verschillen.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="1ad7b-107">De winkel kan zich bijvoorbeeld bevinden in een regio waar klanten meestal Engels spreken, maar sommige werknemers kunnen er de voorkeur aan geven de toepassing te gebruiken met de Franse vertaling.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="1ad7b-108">Gegevenstaal</span><span class="sxs-lookup"><span data-stu-id="1ad7b-108">Data language</span></span>

<span data-ttu-id="1ad7b-109">Ongeacht de instellingen van de gebruiker gebruiken MPOS en Cloud POS altijd de taalinstellingen van de winkel om te bepalen welke vertalingen er voor gegevens moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="1ad7b-110">Dit zorgt ervoor dat alle gebruikers en klanten een consistente ervaring hebben.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="1ad7b-111">Voorbeelden van de gegevens zijn:</span><span class="sxs-lookup"><span data-stu-id="1ad7b-111">Examples of data include:</span></span>

- <span data-ttu-id="1ad7b-112">Producten</span><span class="sxs-lookup"><span data-stu-id="1ad7b-112">Products</span></span>
- <span data-ttu-id="1ad7b-113">Kenmerken en waarden</span><span class="sxs-lookup"><span data-stu-id="1ad7b-113">Attributes and values</span></span>
- <span data-ttu-id="1ad7b-114">Categorienamen</span><span class="sxs-lookup"><span data-stu-id="1ad7b-114">Category names</span></span>
- <span data-ttu-id="1ad7b-115">Afgedrukte of ge-e-mailde transactieontvangstbewijzen</span><span class="sxs-lookup"><span data-stu-id="1ad7b-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="1ad7b-116">Namen betalingsmethodes</span><span class="sxs-lookup"><span data-stu-id="1ad7b-116">Payment method names</span></span>
- <span data-ttu-id="1ad7b-117">Regelweergaveberichten</span><span class="sxs-lookup"><span data-stu-id="1ad7b-117">Line display messages</span></span>

<span data-ttu-id="1ad7b-118">De taal van de winkel wordt ook gebruikt voor het hoofdscherm voor aanmelding bij POS, aangezien de gebruiker niet bekend is voordat deze zich heeft aangemeld.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="1ad7b-119">Als geen vertaling beschikbaar is voor de taal van de winkel, wordt het POS teruggezet naar de taal van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="1ad7b-120">De taalinstelling van de winkel configureren</span><span class="sxs-lookup"><span data-stu-id="1ad7b-120">Configuring the store's language setting</span></span>

<span data-ttu-id="1ad7b-121">De taalinstelling van de winkel wordt ingesteld vanuit **Alle winkels** op de pagina **Winkel** onder **Algemeen &gt; Landinstellingen &gt; Taal**.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="1ad7b-122">Gebruik de vervolgkeuzelijst om de taal voor elke winkel te kiezen.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="1ad7b-123">Taal gebruikersinterface</span><span class="sxs-lookup"><span data-stu-id="1ad7b-123">User interface language</span></span>

<span data-ttu-id="1ad7b-124">De taalinstellingen van de gebruiker van het POS bepalen welke vertalingen worden gebruikt in de gebruikersinterface van de toepassing.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="1ad7b-125">Dit omvat alle labels en menu's en lijsten die niet als gegevens worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="1ad7b-126">Eén uitzondering hierop is de tekst die op POS-Knoppenrasters wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="1ad7b-127">Deze ondersteunen geen vertalingen, waardoor ze altijd de tekst weergeven die voor de knop is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="1ad7b-128">Om vertaalde knoppen te ondersteunen, moet u afzonderlijke knoppenrasters kopiëren en onderhouden en deze aan de juiste gebruikers toewijzen.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="1ad7b-129">De taalinstelling van de gebruiker configureren</span><span class="sxs-lookup"><span data-stu-id="1ad7b-129">Configuring the user's language setting</span></span>

<span data-ttu-id="1ad7b-130">De taalinstellingen van de gebruiker van het POS kunnen worden ingesteld via **Alle werknemers** op de pagina **Werknemer** onder **Retail en Commerce &gt; Taal**.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="1ad7b-131">Deze instelling wordt niet ingesteld op het hoofdtabblad Profiel. Deze instelling wordt niet gebruikt door POS.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="1ad7b-132">Als de taal van de gebruiker niet is ingesteld of is ingesteld op een taal waarvoor geen vertalingen beschikbaar zijn, stapt het POS weer over op de taal van de winkel.</span><span class="sxs-lookup"><span data-stu-id="1ad7b-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="1ad7b-133">Taal van gebruikersinterface   </span><span class="sxs-lookup"><span data-stu-id="1ad7b-133">UI language</span></span>                | <span data-ttu-id="1ad7b-134">Gegevenstaal (producten, ontvangstindelingen, regelweergave, enzovoort.)</span><span class="sxs-lookup"><span data-stu-id="1ad7b-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1ad7b-135">**Bedrijf**</span><span class="sxs-lookup"><span data-stu-id="1ad7b-135">**Company**</span></span> | <span data-ttu-id="1ad7b-136">Standaard</span><span class="sxs-lookup"><span data-stu-id="1ad7b-136">Default</span></span>                    | <span data-ttu-id="1ad7b-137">Standaard</span><span class="sxs-lookup"><span data-stu-id="1ad7b-137">Default</span></span>                                                       |
| <span data-ttu-id="1ad7b-138">**Winkel**</span><span class="sxs-lookup"><span data-stu-id="1ad7b-138">**Store**</span></span>   | <span data-ttu-id="1ad7b-139">Overschrijft bedrijf</span><span class="sxs-lookup"><span data-stu-id="1ad7b-139">Overrides company</span></span>          | <span data-ttu-id="1ad7b-140">Overschrijft bedrijf</span><span class="sxs-lookup"><span data-stu-id="1ad7b-140">Overrides company</span></span>                                             |
| <span data-ttu-id="1ad7b-141">**Gebruiker**</span><span class="sxs-lookup"><span data-stu-id="1ad7b-141">**User**</span></span>    | <span data-ttu-id="1ad7b-142">Overschrijft opslag of bedrijf</span><span class="sxs-lookup"><span data-stu-id="1ad7b-142">Overrides store or company</span></span> | <span data-ttu-id="1ad7b-143">Nooit</span><span class="sxs-lookup"><span data-stu-id="1ad7b-143">Never</span></span>                                                         |
