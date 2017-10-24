---
title: De taalinstellingen van de POS-toepassing en gebruiker
description: In dit onderwerp wordt beschreven hoe u taalinstellingen wijzigt in Retail Modern POS (MPOS) en Cloud POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabb63aea0da4b264aec8e0cc4d43b3e1014e71b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="695c8-103">De taalinstellingen van de POS-toepassing en gebruiker</span><span class="sxs-lookup"><span data-stu-id="695c8-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="695c8-104">In dit onderwerp wordt beschreven hoe u taalinstellingen wijzigt in Retail Modern POS (MPOS) en Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="695c8-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="695c8-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="695c8-105">Overview</span></span>
========

<span data-ttu-id="695c8-106">Retail Modern POS (MPOS) en Cloud POS ondersteunen omgevingen waar de taalinstellingen en vertalingen tussen de winkel- en de gebruikerinstellingen kunnen verschillen.</span><span class="sxs-lookup"><span data-stu-id="695c8-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="695c8-107">De winkel kan zich bijvoorbeeld bevinden in een regio waar klanten meestal Engels spreken, maar sommige werknemers kunnen er de voorkeur aan geven de toepassing te gebruiken met de Franse vertaling.</span><span class="sxs-lookup"><span data-stu-id="695c8-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="695c8-108">Gegevenstaal</span><span class="sxs-lookup"><span data-stu-id="695c8-108">Data language</span></span>
<span data-ttu-id="695c8-109">Ongeacht de instellingen van de gebruiker gebruiken Retail Modern POS en Cloud POS altijd de taalinstellingen van de winkel om te bepalen welke vertalingen er voor gegevens moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="695c8-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="695c8-110">Dit zorgt ervoor dat alle gebruikers en klanten een consistente ervaring hebben.</span><span class="sxs-lookup"><span data-stu-id="695c8-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="695c8-111">Voorbeelden van de gegevens zijn:</span><span class="sxs-lookup"><span data-stu-id="695c8-111">Examples of data include:</span></span>

-   <span data-ttu-id="695c8-112">Producten</span><span class="sxs-lookup"><span data-stu-id="695c8-112">Products</span></span>
-   <span data-ttu-id="695c8-113">Kenmerken en waarden</span><span class="sxs-lookup"><span data-stu-id="695c8-113">Attributes and values</span></span>
-   <span data-ttu-id="695c8-114">Categorienamen</span><span class="sxs-lookup"><span data-stu-id="695c8-114">Category names</span></span>
-   <span data-ttu-id="695c8-115">Afgedrukte of ge-e-mailde transactieontvangstbewijzen</span><span class="sxs-lookup"><span data-stu-id="695c8-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="695c8-116">Namen betalingsmethodes</span><span class="sxs-lookup"><span data-stu-id="695c8-116">Payment method names</span></span>
-   <span data-ttu-id="695c8-117">Regelweergaveberichten</span><span class="sxs-lookup"><span data-stu-id="695c8-117">Line display messages</span></span>

<span data-ttu-id="695c8-118">De taal van de winkel wordt ook gebruikt voor het hoofdscherm voor aanmelding bij POS, aangezien de gebruiker niet bekend is voordat deze zich heeft aangemeld.</span><span class="sxs-lookup"><span data-stu-id="695c8-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="695c8-119">Als geen vertaling beschikbaar is voor de taal van de winkel, wordt het POS teruggezet naar de taal van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="695c8-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="695c8-120">De taalinstelling van de winkel configureren</span><span class="sxs-lookup"><span data-stu-id="695c8-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="695c8-121">De taalinstelling van de winkel wordt ingesteld vanuit **Alle detailhandels** op de pagina **Detailhandel** onder Algemeen &gt; Landinstellingen &gt; Taal.</span><span class="sxs-lookup"><span data-stu-id="695c8-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="695c8-122">**Gebruik de vervolgkeuzelijst om de taal voor elke winkel te kiezen.</span><span class="sxs-lookup"><span data-stu-id="695c8-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="695c8-123">Taal gebruikersinterface</span><span class="sxs-lookup"><span data-stu-id="695c8-123">User interface language</span></span>
<span data-ttu-id="695c8-124">De taalinstellingen van de gebruiker van het POS bepalen welke vertalingen worden gebruikt in de gebruikersinterface van de toepassing.</span><span class="sxs-lookup"><span data-stu-id="695c8-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="695c8-125">Dit omvat alle labels en menu's en lijsten die niet als gegevens worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="695c8-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="695c8-126">Eén uitzondering hierop is de tekst die op POS-Knoppenrasters wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="695c8-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="695c8-127">Deze ondersteunen geen vertalingen, waardoor ze altijd de tekst weergeven die voor de knop is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="695c8-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="695c8-128">Om vertaalde knoppen te ondersteunen, moet u afzonderlijke knoppenrasters kopiëren en onderhouden en deze aan de juiste gebruikers toewijzen.</span><span class="sxs-lookup"><span data-stu-id="695c8-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="695c8-129">De taalinstelling van de gebruiker configureren</span><span class="sxs-lookup"><span data-stu-id="695c8-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="695c8-130">De taalinstellingen van de gebruiker van het POS kunnen worden ingesteld via **Alle werknemers** op de pagina **Werknemer** onder **Detailhandel &gt; Taal**.</span><span class="sxs-lookup"><span data-stu-id="695c8-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="695c8-131">Het wordt niet ingesteld op het hoofdtabblad Profiel. Deze instelling wordt niet gebruikt door POS.</span><span class="sxs-lookup"><span data-stu-id="695c8-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="695c8-132">Als de taal van de gebruiker niet is ingesteld of is ingesteld op een taal waarvoor geen vertalingen beschikbaar zijn, stapt het POS weer over op de taal van de winkel.</span><span class="sxs-lookup"><span data-stu-id="695c8-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="695c8-133">** **</span><span class="sxs-lookup"><span data-stu-id="695c8-133">** **</span></span>       | <span data-ttu-id="695c8-134">**Taal van gebruikersinterface** ** **</span><span class="sxs-lookup"><span data-stu-id="695c8-134">**UI language** ** **</span></span>      | <span data-ttu-id="695c8-135">**Gegevenstaal (producten, ontvangstindelingen, regelweergave, enzovoort.)**</span><span class="sxs-lookup"><span data-stu-id="695c8-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="695c8-136">**Bedrijf**</span><span class="sxs-lookup"><span data-stu-id="695c8-136">**Company**</span></span> | <span data-ttu-id="695c8-137">Standaard</span><span class="sxs-lookup"><span data-stu-id="695c8-137">Default</span></span>                    | <span data-ttu-id="695c8-138">Standaard</span><span class="sxs-lookup"><span data-stu-id="695c8-138">Default</span></span>                                                           |
| <span data-ttu-id="695c8-139">**Winkel**</span><span class="sxs-lookup"><span data-stu-id="695c8-139">**Store**</span></span>   | <span data-ttu-id="695c8-140">Overschrijft bedrijf</span><span class="sxs-lookup"><span data-stu-id="695c8-140">Overrides company</span></span>          | <span data-ttu-id="695c8-141">Overschrijft bedrijf</span><span class="sxs-lookup"><span data-stu-id="695c8-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="695c8-142">**Gebruiker**</span><span class="sxs-lookup"><span data-stu-id="695c8-142">**User**</span></span>    | <span data-ttu-id="695c8-143">Overschrijft opslag of bedrijf</span><span class="sxs-lookup"><span data-stu-id="695c8-143">Overrides store or company</span></span> | <span data-ttu-id="695c8-144">Nooit</span><span class="sxs-lookup"><span data-stu-id="695c8-144">Never</span></span>                                                             |






