---
title: Contante denominaties voor het verkooppunt (POS) configureren
description: Contante denominaties voor bankbiljetten en munten kunnen worden gedefinieerd in de backoffice voor gebruik in het POS door kassiers, verkoopmedewerkers en managers in de winkel.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e3a5f9a73bdee50e3e7c68125144c3b43305efa8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961554"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="9b6bc-103">Contante denominaties voor het verkooppunt (POS) configureren</span><span class="sxs-lookup"><span data-stu-id="9b6bc-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9b6bc-104">Contante denominaties voor bankbiljetten en munten kunnen worden gedefinieerd in de backoffice voor gebruik in het POS door kassiers, verkoopmedewerkers en managers in de winkel.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="9b6bc-105">Deze denominaties kunnen worden gebruikt om te helpen bij het tellen van contant geld bij kascontroles aan het einde van de dag of voor snelle offertes.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="9b6bc-106">Denominaties definiëren</span><span class="sxs-lookup"><span data-stu-id="9b6bc-106">Define denominations</span></span>

<span data-ttu-id="9b6bc-107">De denominaties worden per winkel ingesteld via **Instellen** \> **Contantdeclaratie** van de pagina voor winkeleigenschappen.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-107">The denominations are set up per store on the **Set up** \> **Cash declaration** option from the store property page.</span></span>

![De optie Contantdeclaratie](./media/image1-denomination.png)

<span data-ttu-id="9b6bc-109">Denominaties definiëren:</span><span class="sxs-lookup"><span data-stu-id="9b6bc-109">To define a denomination:</span></span>

1. <span data-ttu-id="9b6bc-110">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-110">Click **New**.</span></span>
1. <span data-ttu-id="9b6bc-111">Geef het type op (munt of biljet).</span><span class="sxs-lookup"><span data-stu-id="9b6bc-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="9b6bc-112">Geef het bedrag op (waarde).</span><span class="sxs-lookup"><span data-stu-id="9b6bc-112">Specify the amount (value).</span></span>

![De pagina Denominaties contantdeclaratie](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="9b6bc-114">Het functionaliteitsprofiel configureren</span><span class="sxs-lookup"><span data-stu-id="9b6bc-114">Configure the functionality profile</span></span>

<span data-ttu-id="9b6bc-115">Bij de betaling met contant geld in POS kan de gebruiker kan de denominaties gebruiken om snel het bedrag in te voeren dat is betaald door de klant.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="9b6bc-116">U kunt de twee opties voor het weergeven van de denominatie in het POS configureren in het functionaliteitsprofiel.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="9b6bc-117">**Groter of gelijk aan het verschuldigde bedrag**: standaard worden door het POS alleen denominaties weergegeven die groter zijn dan het verschuldigde bedrag, wat one-touch offertes mogelijk maakt.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="9b6bc-118">Als het verschuldigde bedrag bijvoorbeeld $7,50 is, geeft het POS de volgende denominaties weer: $10, $20, $50 en $100.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="9b6bc-119">Als een van deze bedragen wordt aangeraakt, wordt de verkoop automatisch aangeboden voor dat bedrag.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="9b6bc-120">De biljetten van $1 en $5 worden niet weergegeven omdat deze bedragen kleiner dan het te betalen bedrag.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="9b6bc-121">**Alle denominaties**: selecteer deze optie om altijd alle denominaties in POS weer te geven, ongeacht het betaalde bedrag.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="9b6bc-122">Dit betekent dat de gebruiker een combinatie van biljetten kan gebruiken voor het verschuldigde bedrag.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="9b6bc-123">Als het verschuldigde bedrag bijvoorbeeld $25,00 is, kan de gebruiker $20 en $5 kiezen voor het voltooien van de verkoop.</span><span class="sxs-lookup"><span data-stu-id="9b6bc-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>
