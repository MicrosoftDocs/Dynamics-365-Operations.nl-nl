---
title: EUR-00015 Een partij zoeken door middel van het btw-id
description: Deze procedure laat zien hoe u een partij-zoekopdracht uitvoert met een registratie-id.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 401971b6f146f1df028291ba0f691ccac5f1966d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408310"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="3249d-103">EUR-00015 Een partij zoeken door middel van het btw-id</span><span class="sxs-lookup"><span data-stu-id="3249d-103">EUR-00015 Party search using VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3249d-104">Deze procedure laat zien hoe u een partij-zoekopdracht uitvoert met een registratie-id.</span><span class="sxs-lookup"><span data-stu-id="3249d-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="3249d-105">Voordat u deze procedure kunt uitvoeren, moet u btw-id's instellen en invoeren voor leveranciers, klanten of rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="3249d-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="3249d-106">Deze procedure is van toepassing op alle Europese landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="3249d-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="3249d-107">De procedure is gemaakt met het demobedrijf DEMF met een primair adres in Duitsland.</span><span class="sxs-lookup"><span data-stu-id="3249d-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="3249d-108">Deze procedure is bedoeld voor een beheerder van leveranciers of klanten.</span><span class="sxs-lookup"><span data-stu-id="3249d-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="3249d-109">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="3249d-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="3249d-110">Ga naar Organisatiebeheer > Globaal adresboek > Globaal adresboek.</span><span class="sxs-lookup"><span data-stu-id="3249d-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="3249d-111">Klik op Zoeken op registratie-id.</span><span class="sxs-lookup"><span data-stu-id="3249d-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="3249d-112">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3249d-112">Click Add.</span></span>
4. <span data-ttu-id="3249d-113">Typ of selecteer een waarde in het veld Registratietype.</span><span class="sxs-lookup"><span data-stu-id="3249d-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="3249d-114">Selecteer bijvoorbeeld Btw-id als u partijen wilt vinden met een registratie-id van het type Btw-id.</span><span class="sxs-lookup"><span data-stu-id="3249d-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="3249d-115">Typ of selecteer een waarde in het veld Land/regio.</span><span class="sxs-lookup"><span data-stu-id="3249d-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="3249d-116">Voer bijvoorbeeld DEU in.</span><span class="sxs-lookup"><span data-stu-id="3249d-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="3249d-117">Typ een waarde in het veld Registratienummer.</span><span class="sxs-lookup"><span data-stu-id="3249d-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="3249d-118">Klik op Zoeken..</span><span class="sxs-lookup"><span data-stu-id="3249d-118">Click Find.</span></span>
    * <span data-ttu-id="3249d-119">Alle partijen met die registratie-id worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3249d-119">All parties with that registration ID will be displayed.</span></span>  

