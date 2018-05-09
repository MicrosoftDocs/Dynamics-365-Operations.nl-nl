---
title: Een order vanuit een andere winkel verzenden
description: In dit onderwerp wordt de verzendfunctie Toeslag beschreven.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2796ef1a9c312f86c878dd72fa26dcb45c88ed88
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="1f161-103">Een order vanuit een andere winkel verzenden</span><span class="sxs-lookup"><span data-stu-id="1f161-103">Ship an order from a different store</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f161-104">Met de verzendfunctie Toeslag in Dynamics 365 for Retail kunnen klantorders in de ene winkel worden geplaatst en vanuit een andere winkel worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="1f161-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="1f161-105">Klantorders in de POS-client (Point Of Sale) ondersteunen meerdere afhandelingsopties.</span><span class="sxs-lookup"><span data-stu-id="1f161-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="1f161-106">Enkele voorbeelden van afhandelingsopties:</span><span class="sxs-lookup"><span data-stu-id="1f161-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="1f161-107">Ophalen uit dezelfde locatie op een andere datum.</span><span class="sxs-lookup"><span data-stu-id="1f161-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="1f161-108">Ophalen uit een andere locatie op dezelfde of een andere datum.</span><span class="sxs-lookup"><span data-stu-id="1f161-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="1f161-109">Verzenden vanuit het standaardmagazijn van verzending die is toegewezen aan de winkel en op een bepaalde datum leveren.</span><span class="sxs-lookup"><span data-stu-id="1f161-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="1f161-110">Met de verzendfunctie Toeslag worden de volgende POS-bewerkingen gebruikt: Alle producten verzenden en Geselecteerde producten verzenden.</span><span class="sxs-lookup"><span data-stu-id="1f161-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="1f161-111">Hierdoor kan de medewerker van de winkel de verzendlocatie selecteren waar de order of orderregel kan worden afgehandeld.</span><span class="sxs-lookup"><span data-stu-id="1f161-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="1f161-112">Standaard is de verzendlocatie het magazijn van verzending dat is gekoppeld aan de winkel.</span><span class="sxs-lookup"><span data-stu-id="1f161-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="1f161-113">De medewerker van de winkel kan deze locatie echter wijzigen en een winkel selecteren die is gedefinieerd in de winkellocatorgroep die aan de winkel is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1f161-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="1f161-114">De mogelijkheid om afleveradressen te selecteren, blijft ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="1f161-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="1f161-115">De verzendmethoden die kunnen worden gebruikt om te voldoen aan de orderregel zijn gebaseerd op de configuratie van geldige leveringsmethoden voor producten en adressen.</span><span class="sxs-lookup"><span data-stu-id="1f161-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="1f161-116">Omdat de regels over geldige leveringsmethoden alleen worden beheerd in Detailhandel Hoofdkantoor, voert de POS-client een real-time aanroep uit om de geldige leveringsmethoden voor een verzendregel op te halen.</span><span class="sxs-lookup"><span data-stu-id="1f161-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


