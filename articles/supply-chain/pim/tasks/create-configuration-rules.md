---
title: Configuratieregels maken
description: Met deze procedure worden configuratieregels gemaakt die kunnen worden gebruikt voor een op dimensies gebaseerde configuratie om bepaalde combinaties van stuklijstregels af te dwingen of te voorkomen.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21cdca1c33b106bd153a436a7fec4f0eeaa0d620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820053"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="b46b4-103">Configuratieregels maken</span><span class="sxs-lookup"><span data-stu-id="b46b4-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b46b4-104">Met deze procedure worden configuratieregels gemaakt die kunnen worden gebruikt voor een op dimensies gebaseerde configuratie om bepaalde combinaties van stuklijstregels af te dwingen of te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="b46b4-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="b46b4-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="b46b4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b46b4-106">Dit is de zevende van acht procedures waarin wordt uitgelegd hoe u combinaties maakt voor een op dimensies gebaseerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="b46b4-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="b46b4-107">Ga naar Productgegevensbeheer > Stuklijsten en formules > Stuklijsten.</span><span class="sxs-lookup"><span data-stu-id="b46b4-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="b46b4-108">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b46b4-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b46b4-109">Zoek en selecteer de stuklijst voor de op dimensies gebaseerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="b46b4-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="b46b4-110">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="b46b4-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="b46b4-111">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b46b4-111">Click Change view.</span></span>
5. <span data-ttu-id="b46b4-112">Klik op Weergave kopteksten.</span><span class="sxs-lookup"><span data-stu-id="b46b4-112">Click Header view.</span></span>
    * <span data-ttu-id="b46b4-113">Open de koptekstweergave om het sneltabblad Configuratieroute te openen.</span><span class="sxs-lookup"><span data-stu-id="b46b4-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="b46b4-114">Vouw de sectie Configuratieroute uit of samen.</span><span class="sxs-lookup"><span data-stu-id="b46b4-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="b46b4-115">Het sneltabblad Configuratieroute moet in de uitgevouwen modus zijn.</span><span class="sxs-lookup"><span data-stu-id="b46b4-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="b46b4-116">Klik op Configuratieregels.</span><span class="sxs-lookup"><span data-stu-id="b46b4-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="b46b4-117">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="b46b4-117">Click New.</span></span>
9. <span data-ttu-id="b46b4-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b46b4-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="b46b4-119">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b46b4-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b46b4-120">De artikelen in de huidige configuratiegroep worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b46b4-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="b46b4-121">Selecteer het artikel dat de voorwaarde in de regel vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="b46b4-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="b46b4-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b46b4-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b46b4-123">Selecteer een optie in het veld Methode.</span><span class="sxs-lookup"><span data-stu-id="b46b4-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="b46b4-124">Het is mogelijk de selectie of deselectie van een artikel uit een andere configuratiegroep af te dwingen.</span><span class="sxs-lookup"><span data-stu-id="b46b4-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="b46b4-125">Klik in het veld Afgeleide groep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b46b4-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b46b4-126">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="b46b4-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b46b4-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b46b4-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b46b4-128">Selecteer de gewenste configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="b46b4-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="b46b4-129">Klik in het veld Afgeleid artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b46b4-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="b46b4-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b46b4-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b46b4-131">Selecteer het artikelnummer dat wordt geselecteerd of gedeselecteerd, afhankelijk van de gekozen methode.</span><span class="sxs-lookup"><span data-stu-id="b46b4-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="b46b4-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b46b4-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]