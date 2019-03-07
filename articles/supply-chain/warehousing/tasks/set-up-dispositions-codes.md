---
title: Beschikkingscodes instellen
description: Deze procedure is gericht op de instelling van een beschikkingscode die op een mobiel apparaat kan worden gebruikt voor het ontvangstproces van retourorders.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85402e05d55367da5fe89b242ad8eafc727b441e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "324118"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="cd442-103">Beschikkingscodes instellen</span><span class="sxs-lookup"><span data-stu-id="cd442-103">Set up dispositions codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd442-104">Deze procedure is gericht op de instelling van een beschikkingscode die op een mobiel apparaat kan worden gebruikt voor het ontvangstproces van retourorders.</span><span class="sxs-lookup"><span data-stu-id="cd442-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="cd442-105">Beschikkingscodes zijn een verzameling regels die kunnen worden gebruikt wanneer artikelen worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="cd442-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="cd442-106">Bijvoorbeeld, wanneer een werkgebruiker een mobiel apparaat gebruikt om artikelen te ontvangen die beschadigd zijn, moet de gebruiker een beschikkingscode voor de beschadigde artikelen scannen.</span><span class="sxs-lookup"><span data-stu-id="cd442-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="cd442-107">De voorraadstatus van de ontvangen goederen, de werksjabloon en de locatierichtlijn kan worden bepaald aan de hand van de gescande beschikkingscode.</span><span class="sxs-lookup"><span data-stu-id="cd442-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="cd442-108">Voor het inkooporderontvangstproces en het productieordergereedmeldproces is het gebruik van een beschikkingscode optioneel.</span><span class="sxs-lookup"><span data-stu-id="cd442-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="cd442-109">Voor het ontvangstproces van verkooporderretouren is het gebruik van een beschikkingscode, als de artikelen met een mobiel apparaat worden geregistreerd, verplicht.</span><span class="sxs-lookup"><span data-stu-id="cd442-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="cd442-110">Deze taakbegeleiding is gemaakt met het demogegevensbedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="cd442-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="cd442-111">Deze procedure is bedoeld voor de magazijnbeheerder.</span><span class="sxs-lookup"><span data-stu-id="cd442-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="cd442-112">Ga naar Magazijnbeheer > Instellingen > Mobiel apparaat > Beschikkingscodes.</span><span class="sxs-lookup"><span data-stu-id="cd442-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="cd442-113">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="cd442-113">Click New.</span></span>
    * <span data-ttu-id="cd442-114">Maak een nieuwe beschikkingscode om te gebruiken voor klantretouren.</span><span class="sxs-lookup"><span data-stu-id="cd442-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="cd442-115">Typ een waarde in het veld Beschikkingscode.</span><span class="sxs-lookup"><span data-stu-id="cd442-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="cd442-116">Selecteer in het veld Voorraadstatus een voorraadstatus waar er voorraadblokkering is.</span><span class="sxs-lookup"><span data-stu-id="cd442-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="cd442-117">Als u USMF workflow gebruikt, selecteert u 'Blokkeren'.</span><span class="sxs-lookup"><span data-stu-id="cd442-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="cd442-118">U kunt een voorraadstatus aan de beschikkingscode toevoegen om de standaardstatus op de orderregels te overschrijven.</span><span class="sxs-lookup"><span data-stu-id="cd442-118">You can add an inventory status to the disposition code to override the default status that’s on the order lines.</span></span>  
5. <span data-ttu-id="cd442-119">Typ een waarde in het veld Werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="cd442-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="cd442-120">Optioneel: selecteer een werksjablooncode die aan een retourorder is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="cd442-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="cd442-121">Als geen waarde is opgegeven, wordt de werksjabloon opgelost met de standaardregels die in uw systeem zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="cd442-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="cd442-122">Een werksjabloon selecteren beperkt de processen waarmee deze beschikkingscode kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cd442-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="cd442-123">Als een beschikkingscode bijvoorbeeld een werksjabloon met een werkorder van het type inkooporder heeft, kan deze niet worden gebruikt om artikelen te registreren die door klanten worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="cd442-123">For example, if a disposition code has a work template with a work order of type purchase order, it can’t be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="cd442-124">Typ een waarde in het veld Beschikkingscode retourneren.</span><span class="sxs-lookup"><span data-stu-id="cd442-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="cd442-125">De retourbeschikkingscode definieert de rest van het retourorderproces voor de geregistreerde artikelen.</span><span class="sxs-lookup"><span data-stu-id="cd442-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="cd442-126">In dit voorbeeld moet de klant een creditnota ontvangen.</span><span class="sxs-lookup"><span data-stu-id="cd442-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="cd442-127">Voeg een retourbeschikkingscode toe die een actiecredit bevat.</span><span class="sxs-lookup"><span data-stu-id="cd442-127">Add a returns disposition code that contains an action Credit.</span></span>  

