---
title: Btw-diensten instellen
description: Belastingdiensten zijn entiteiten waaraan geïncasseerde btw moet worden aangegeven en betaald.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 63b1b023181e1ead16571102c524a61edfdabdca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441887"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="8c523-103">Btw-diensten instellen</span><span class="sxs-lookup"><span data-stu-id="8c523-103">Set up sales tax authorities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c523-104">Belastingdiensten zijn entiteiten waaraan geïncasseerde btw moet worden aangegeven en betaald.</span><span class="sxs-lookup"><span data-stu-id="8c523-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="8c523-105">U kunt btw rechtstreeks of via een hiervoor gemaakte leverancierrekening aan de belastingdienst betalen.</span><span class="sxs-lookup"><span data-stu-id="8c523-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="8c523-106">Als u dit doet, kan het bedrijf werken met de gebruikelijke betalingsroutines om de belastingdienst op tijd te betalen.</span><span class="sxs-lookup"><span data-stu-id="8c523-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="8c523-107">Als u de belastingdienst niet als leverancier instelt, moet iemand op de desbetreffende vervaldatum handmatig een betaling aan de belastingdienst voorbereiden.</span><span class="sxs-lookup"><span data-stu-id="8c523-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="8c523-108">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8c523-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="8c523-109">Ga naar Belasting > Indirecte belastingen > Btw > Btw-diensten.</span><span class="sxs-lookup"><span data-stu-id="8c523-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="8c523-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8c523-110">Click New.</span></span>
3. <span data-ttu-id="8c523-111">Typ een waarde in het veld Btw-dienst.</span><span class="sxs-lookup"><span data-stu-id="8c523-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="8c523-112">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="8c523-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8c523-113">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="8c523-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8c523-114">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8c523-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8c523-115">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8c523-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8c523-116">Selecteer de rapportindeling voor uw land/regio als deze beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="8c523-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="8c523-117">Als de rapportindelingen niet aan de vereisten van de belastingdienst voldoen, gebruikt u de standaardindeling.</span><span class="sxs-lookup"><span data-stu-id="8c523-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="8c523-118">Voer waarden in het formulier Afronding en afrondingsvelden in om op te geven hoe de totale te betalen btw moet worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="8c523-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="8c523-119">Alle afrondingsverschillen worden naar de ingestelde rekeningen voor automatische transacties in het grootboek geboekt.</span><span class="sxs-lookup"><span data-stu-id="8c523-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="8c523-120">Voer een nummer in het veld Afronden in.</span><span class="sxs-lookup"><span data-stu-id="8c523-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="8c523-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8c523-121">Click Save.</span></span>

