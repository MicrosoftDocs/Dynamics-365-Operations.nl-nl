---
title: Artikelen registreren voor een artikel waarvoor 'basale magazijnen' mogelijk is met een artikelontvangstjournaal
description: Deze procedure toont hoe u artikelen registreert via het artikelontvangstjournaal wanneer u basale magazijnen gebruikt in de module Voorraadbeheer.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1745642dd270e62557b8624cc9daf85d13da044e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982571"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="22883-103">Artikelen registreren voor een artikel waarvoor 'basale magazijnen' mogelijk is met een artikelontvangstjournaal</span><span class="sxs-lookup"><span data-stu-id="22883-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22883-104">Deze procedure toont hoe u artikelen registreert via het artikelontvangstjournaal wanneer u basale magazijnen gebruikt in de module Voorraadbeheer.</span><span class="sxs-lookup"><span data-stu-id="22883-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="22883-105">Dit wordt gewoonlijk uitgevoerd door een ontvangstadministrateur.</span><span class="sxs-lookup"><span data-stu-id="22883-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="22883-106">U kunt deze procedure uitvoeren in het demobedrijf USMF met de voorbeeldwaarden die worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22883-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="22883-107">Als u geen gebruikmaakt van USMF, hebt u een bevestigde inkooporder nodig met een openstaande inkooporderregel voordat u deze guide start.</span><span class="sxs-lookup"><span data-stu-id="22883-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="22883-108">Het artikel op de regel moet worden opgeslagen in voorraad.</span><span class="sxs-lookup"><span data-stu-id="22883-108">The item on the line must be stocked.</span></span> <span data-ttu-id="22883-109">En het artikel moet zijn gekoppeld aan een opslagdimensiegroep, waarbij site en magazijn actief zijn.</span><span class="sxs-lookup"><span data-stu-id="22883-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="22883-110">Koptekst voor artikelontvangstjournaal maken</span><span class="sxs-lookup"><span data-stu-id="22883-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="22883-111">Ga naar Voorraadbeheer > Journaalposten > Artikelontvangst > Artikelontvangst.</span><span class="sxs-lookup"><span data-stu-id="22883-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="22883-112">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="22883-112">Click New.</span></span>
3. <span data-ttu-id="22883-113">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="22883-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="22883-114">Als u USMF gebruikt, kunt u WHS typen.</span><span class="sxs-lookup"><span data-stu-id="22883-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="22883-115">Als u andere gegevens gebruikt, moet het journaal waarvan u de naam kiest de volgende eigenschappen hebben: Orderverzamellocatie controleren moet zijn ingesteld op Nee en Quarantainebeheer moet zijn ingesteld op Nee.</span><span class="sxs-lookup"><span data-stu-id="22883-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="22883-116">Typ een waarde in het veld Pakbon.</span><span class="sxs-lookup"><span data-stu-id="22883-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="22883-117">Dit is de pakbon-id van de pakbon die door de leverancier is uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="22883-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="22883-118">Voeg een uniek nummer toe.</span><span class="sxs-lookup"><span data-stu-id="22883-118">Add a unique number.</span></span>  
5. <span data-ttu-id="22883-119">Selecteer de inkooporder in het veld Nummer.</span><span class="sxs-lookup"><span data-stu-id="22883-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="22883-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="22883-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="22883-121">Regels toevoegen aan artikelontvangstjournaal</span><span class="sxs-lookup"><span data-stu-id="22883-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="22883-122">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="22883-122">Click Functions.</span></span>
2. <span data-ttu-id="22883-123">Klik op Regels maken.</span><span class="sxs-lookup"><span data-stu-id="22883-123">Click Create lines.</span></span>
    * <span data-ttu-id="22883-124">De regels kunnen handmatig in dit journaal worden ingevoerd of automatisch worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="22883-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="22883-125">Hier ziet u hoe deze automatisch kunnen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="22883-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="22883-126">Schakel het selectievakje Hoeveelheid initialiseren in of uit.</span><span class="sxs-lookup"><span data-stu-id="22883-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="22883-127">Hiermee wordt de hoeveelheid op de journaalregels geïnitialiseerd met de hoeveelheid die niet is geregistreerd vanaf de inkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="22883-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="22883-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="22883-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="22883-129">Het journaal boeken</span><span class="sxs-lookup"><span data-stu-id="22883-129">Post the journal</span></span>
1. <span data-ttu-id="22883-130">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="22883-130">Click Post.</span></span>
2. <span data-ttu-id="22883-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="22883-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="22883-132">De productontvangst genereren</span><span class="sxs-lookup"><span data-stu-id="22883-132">Generate the product receipt</span></span>
1. <span data-ttu-id="22883-133">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="22883-133">Click Functions.</span></span>
2. <span data-ttu-id="22883-134">Klik op Productontvangstbon.</span><span class="sxs-lookup"><span data-stu-id="22883-134">Click Product receipt.</span></span>
3. <span data-ttu-id="22883-135">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="22883-135">Click OK.</span></span>

