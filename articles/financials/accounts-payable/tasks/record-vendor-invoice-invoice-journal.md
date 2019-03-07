---
title: Een leveranciersfactuur in het factuurjournaal registreren
description: Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "348935"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="67fc4-103">Een leveranciersfactuur in het factuurjournaal registreren</span><span class="sxs-lookup"><span data-stu-id="67fc4-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67fc4-104">Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="67fc4-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="67fc4-105">Voorbeelden van dit type factuur zijn onkosten voor levering of services.</span><span class="sxs-lookup"><span data-stu-id="67fc4-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="67fc4-106">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="67fc4-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="67fc4-107">Ga naar Leveranciers > Werkruimten > Leveranciersfactuurregistratie.</span><span class="sxs-lookup"><span data-stu-id="67fc4-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="67fc4-108">Klik op Nieuw factuurjournaal.</span><span class="sxs-lookup"><span data-stu-id="67fc4-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="67fc4-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="67fc4-109">Click New.</span></span>
4. <span data-ttu-id="67fc4-110">Voer in het veld Naam de journaalnaam in of klik op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="67fc4-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="67fc4-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="67fc4-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="67fc4-112">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="67fc4-112">Click Lines.</span></span>
    * <span data-ttu-id="67fc4-113">Voer in het datumveld de boekingsdatum in die Grootboek bijwerkt.</span><span class="sxs-lookup"><span data-stu-id="67fc4-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="67fc4-114">Geef in het veld Rekening de leveranciersrekening op.</span><span class="sxs-lookup"><span data-stu-id="67fc4-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="67fc4-115">Voer in het veld Factuur het factuurnummer in.</span><span class="sxs-lookup"><span data-stu-id="67fc4-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="67fc4-116">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="67fc4-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="67fc4-117">Voer een nummer in het veld Credit in.</span><span class="sxs-lookup"><span data-stu-id="67fc4-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="67fc4-118">Voer in het veld Tegenrekening het rekeningnummer in of klik op de vervolgkeuzeknop om de zoekopdracht te openen</span><span class="sxs-lookup"><span data-stu-id="67fc4-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="67fc4-119">De btw-groep is afkomstig van de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="67fc4-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="67fc4-120">De btw-groep van het artikel is afkomstig van de hoofdrekening die is opgegeven in het veld Tegenrekening.</span><span class="sxs-lookup"><span data-stu-id="67fc4-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="67fc4-121">De vervaldatum wordt berekend aan de hand van de betalingsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="67fc4-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="67fc4-122">De contantkorting is afkomstig van de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="67fc4-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="67fc4-123">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="67fc4-123">Click Post.</span></span>
13. <span data-ttu-id="67fc4-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="67fc4-124">Close the page.</span></span>

