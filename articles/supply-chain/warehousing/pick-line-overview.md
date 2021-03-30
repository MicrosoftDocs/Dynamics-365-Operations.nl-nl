---
title: Een menuoptie voor een mobiel apparaat instellen om een overzicht van orderverzamelregels te bieden
description: In dit onderwerp wordt uitgelegd hoe u kunt definiëren wanneer een lijst met alle werkregels wordt weergegeven voor magazijnmedewerkers die magazijnwerk op een mobiel apparaat verwerken. Deze mogelijkheid kan handig zijn voor magazijnmedewerkers die vaak een overzicht van de orderverzamelregels in een werkorder nodig hebben zodat ze de orderverzamelvolgorde kunnen optimaliseren.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 22e724b60ec5cc8bf39a520022f43784d3a328eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232906"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="444de-104">Een menuoptie voor een mobiel apparaat instellen om een overzicht van orderverzamelregels te bieden</span><span class="sxs-lookup"><span data-stu-id="444de-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="444de-105">In dit onderwerp wordt uitgelegd hoe u opties kunt configureren die betrekking hebben op het overzicht van orderverzamelregels voor menuopties van mobiele apparaten die worden gebruikt om werkzaamheden voor het verzamelen van orders te verwerken.</span><span class="sxs-lookup"><span data-stu-id="444de-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="444de-106">Met het overzicht van orderverzamelregels kunnen magazijnmedewerkers een lijst met alle werkregels bekijken die betrekking hebben op de huidige taak, en kunnen ze een selectie maken in die lijst.</span><span class="sxs-lookup"><span data-stu-id="444de-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="444de-107">Met deze mogelijkheid kunnen medewerkers de orderverzamelvolgorde optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="444de-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="444de-108">De functie bevat opties waarmee de standaardknop **Overslaan** wordt vervangen waarmee medewerkers de regels een voor een in een vaste volgorde kunnen doorlopen.</span><span class="sxs-lookup"><span data-stu-id="444de-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="444de-109">(De mogelijkheid om die knop te gebruiken is echter nog steeds beschikbaar.)</span><span class="sxs-lookup"><span data-stu-id="444de-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="444de-110">Beheerders kunnen elke menuoptie afzonderlijk configureren om te bepalen hoe, wanneer en waar de magazijnapp het overzicht van orderverzamelregels laat zien.</span><span class="sxs-lookup"><span data-stu-id="444de-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="444de-111">De functie Overzicht van werkorderverzamelregels inschakelen</span><span class="sxs-lookup"><span data-stu-id="444de-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="444de-112">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="444de-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="444de-113">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="444de-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="444de-114">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="444de-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="444de-115">**Module:** _Magazijnbeheer_</span><span class="sxs-lookup"><span data-stu-id="444de-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="444de-116">**Functienaam:** _Overzicht van werkorderverzamelregels_</span><span class="sxs-lookup"><span data-stu-id="444de-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="444de-117">Menuopties configureren om een lijst met alle werkregels weer te geven</span><span class="sxs-lookup"><span data-stu-id="444de-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="444de-118">Als u een menuoptie voor een mobiel apparaat wilt instellen om een overzicht van orderverzamelregels te bieden, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="444de-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="444de-119">Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.</span><span class="sxs-lookup"><span data-stu-id="444de-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="444de-120">Selecteer of maak een menuoptie die verband houdt met werkorderverzameling en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="444de-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="444de-121">**Modus:** *werk*</span><span class="sxs-lookup"><span data-stu-id="444de-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="444de-122">**Bestaand werk gebruiken:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="444de-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="444de-123">**Bestuurd door:** *Door gebruiker bestuurd* of *Door systeem bestuurd*</span><span class="sxs-lookup"><span data-stu-id="444de-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="444de-124">Zie voor meer informatie over het maken van menuopties en het gebruik van de verschillende instellingen die beschikbaar zijn op de pagina **Menuopties voor mobiel apparaat** [Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="444de-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="444de-125">Configureer op het sneltabblad **Algemeen** de functie door het veld **Lijst met werkregels weergeven** op een van de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="444de-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="444de-126">**Alleen op aanvraag weergeven** : medewerkers kunnen ervoor kiezen de lijst met orderverzamelregels te bekijken door de knop **Ga verder naar** in de magazijnapp te selecteren.</span><span class="sxs-lookup"><span data-stu-id="444de-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="444de-127">**Weergeven aan het begin van elke verzameling**: medewerkers zien de lijst telkens wanneer ze een orderverzamelregel starten of voltooien.</span><span class="sxs-lookup"><span data-stu-id="444de-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="444de-128">Ze kunnen de lijst ook opnieuw bekijken door de knop **Ga verder naar** in de magazijnapp te selecteren.</span><span class="sxs-lookup"><span data-stu-id="444de-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="444de-129">**Alleen weergeven bij het begin van de eerste verzameling**: medewerkers zien de lijst telkens wanneer ze nieuwe orderverzamelingswerkzaamheden starten, maar niet na elke regel.</span><span class="sxs-lookup"><span data-stu-id="444de-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="444de-130">Ze kunnen de lijst ook opnieuw bekijken door de knop **Ga verder naar** in de magazijnapp te selecteren.</span><span class="sxs-lookup"><span data-stu-id="444de-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="444de-131">**Nooit weergeven**: de standaardknop **Overslaan** wordt weergegeven in de magazijnapp en de weergave van de lijst met werkregels is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="444de-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="444de-132">Met de knop **Overslaan** kunnen medewerkers de regels een voor een in een vaste volgorde doorlopen.</span><span class="sxs-lookup"><span data-stu-id="444de-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="444de-133">Ze kunnen de lijst ook zo vaak als nodig is doorlopen, totdat alle regels zijn verwerkt.</span><span class="sxs-lookup"><span data-stu-id="444de-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="444de-134">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="444de-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="444de-135">Als u het veld **Lijst met werkregels weergeven** instelt op een willekeurige waarde behalve *Nooit weergeven*, wordt de knop **Veldenlijst** in het actievenster beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="444de-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="444de-136">Selecteer **Veldenlijst** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="444de-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="444de-137">Configureer op de pagina **Veldenlijst** de informatie die in de magazijnapp voor elke regel in de lijst wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="444de-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="444de-138">Het veld **Primair besturingselement** wordt altijd ingesteld op *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="444de-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="444de-139">Daarom begint elke rij in de lijst met een regelnummer.</span><span class="sxs-lookup"><span data-stu-id="444de-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="444de-140">Gebruik de resterende **Weergaveveld**-velden om desgewenst maximaal zeven extra weergavevelden toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="444de-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="444de-141">Selecteer de naam van een werkregelveld in elk **Weergaveveld**-veld.</span><span class="sxs-lookup"><span data-stu-id="444de-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="444de-142">Op elke regel wordt vervolgens een waarde voor dat veld weergegeven.</span><span class="sxs-lookup"><span data-stu-id="444de-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="444de-143">De waarden worden weergegeven in de volgorde die u hier selecteert.</span><span class="sxs-lookup"><span data-stu-id="444de-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="444de-144">U kunt sommige velden van **Weergaveveld** leeg laten als u niet alle zeven waarden nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="444de-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="444de-145">Selecteer **Opslaan** in het actievenster en sluit de pagina **Veldenlijst**.</span><span class="sxs-lookup"><span data-stu-id="444de-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]