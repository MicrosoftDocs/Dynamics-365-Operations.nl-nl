---
title: Status van transport instellen
description: In dit onderwerp wordt beschreven hoe u de statuswaarden kunt bepalen die gebruikers aan transporten kunt toewijzen.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500881"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="72343-103">Status van transport instellen</span><span class="sxs-lookup"><span data-stu-id="72343-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="72343-104">Op de pagina **Transportstatussen** kunt u de set statuswaarden instellen die gebruikers kunnen toewijzen aan transporten.</span><span class="sxs-lookup"><span data-stu-id="72343-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="72343-105">Gebruikers kunnen statuswaarden voor transporten toewijzen aan alle niveaus van een transport: transport, verzendcontainer, folio, inkooporder en artikel (inkoopregels en transferorderregels).</span><span class="sxs-lookup"><span data-stu-id="72343-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="72343-106">Deze worden voor twee doelen gebruikt:</span><span class="sxs-lookup"><span data-stu-id="72343-106">They are used for two purposes:</span></span>

- <span data-ttu-id="72343-107">De gebruiker informeren over de status van transport, verzendcontainer, folio, inkooporder of artikel (inkoopregels en transferorderregels).</span><span class="sxs-lookup"><span data-stu-id="72343-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="72343-108">Het gebruik beperken van het kostengebied door wijziging of verwijdering te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="72343-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="72343-109">Als u uw transportstatussen wilt instellen, gaat u naar **Francoprijzen \> Instellen \> Transportstatussen**.</span><span class="sxs-lookup"><span data-stu-id="72343-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="72343-110">Hier kunt u statussen toevoegen, verwijderen en bewerken met de knoppen in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="72343-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="72343-111">Elk kostengebied heeft een eigen set en hiërarchie van transportstatussen.</span><span class="sxs-lookup"><span data-stu-id="72343-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="72343-112">Daarom moet u op de pagina **Transportstatussen**, in het veld **Kostengebied**, eerst het kostengebied selecteren waarvoor u transportstatussen wilt weergeven of maken.</span><span class="sxs-lookup"><span data-stu-id="72343-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="72343-113">Stel vervolgens voor elke transportstatus de velden in die in de volgende tabel worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="72343-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="72343-114">De status van een transport kan ook automatisch door systeemgebeurtenissen worden gewijzigd, zoals regels die zijn vastgesteld met behulp van het traceringscontrolecentrum.</span><span class="sxs-lookup"><span data-stu-id="72343-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="72343-115">Veld</span><span class="sxs-lookup"><span data-stu-id="72343-115">Field</span></span> | <span data-ttu-id="72343-116">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="72343-116">Description</span></span> |
|---|---|
| <span data-ttu-id="72343-117">Reisstatus</span><span class="sxs-lookup"><span data-stu-id="72343-117">Voyage status</span></span> | <span data-ttu-id="72343-118">Voer de naam van de transportstatus in.</span><span class="sxs-lookup"><span data-stu-id="72343-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="72343-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="72343-119">Description</span></span> | <span data-ttu-id="72343-120">Voer een beschrijving van de transportstatus in.</span><span class="sxs-lookup"><span data-stu-id="72343-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="72343-121">Wijzigen</span><span class="sxs-lookup"><span data-stu-id="72343-121">Modify</span></span> | <span data-ttu-id="72343-122">Schakel dit selectievakje in als gebruikers transporten met deze status mogen wijzigen.</span><span class="sxs-lookup"><span data-stu-id="72343-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="72343-123">Delete</span><span class="sxs-lookup"><span data-stu-id="72343-123">Delete</span></span> | <span data-ttu-id="72343-124">Schakel dit selectievakje in als gebruikers transporten met deze status mogen verwijderen.</span><span class="sxs-lookup"><span data-stu-id="72343-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="72343-125">Verplicht</span><span class="sxs-lookup"><span data-stu-id="72343-125">Mandatory</span></span> | <span data-ttu-id="72343-126">Schakel dit selectievakje in om de transportstatus verplicht te maken, zodat deze niet kan worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="72343-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="72343-127">Ouder</span><span class="sxs-lookup"><span data-stu-id="72343-127">Parent</span></span> | <span data-ttu-id="72343-128">Gebruik dit veld om een hiërarchie tussen de statuswaarden te bepalen.</span><span class="sxs-lookup"><span data-stu-id="72343-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="72343-129">Transportstatussen kunnen alleen in neerwaartse richting in de hiërarchie worden gewijzigd (handmatig of automatisch), van een bovenliggende status naar een van de onderliggende statussen.</span><span class="sxs-lookup"><span data-stu-id="72343-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="72343-130">U hoeft alleen de specifieke transportstatussen in te stellen die uw organisatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="72343-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="72343-131">Standaard transportstatussen zijn onder andere *Bevestigd*, *Goederen in transit*, *Ontvangen*, *Gereed voor kostprijsberekening* en *Kostprijs berekend*.</span><span class="sxs-lookup"><span data-stu-id="72343-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="72343-132">Er kunnen echter ook andere statussen aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="72343-132">However, other statuses might be present.</span></span>
