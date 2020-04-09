---
title: Een leveranciersfactuur in het factuurjournaal registreren
description: Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140370"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="86c06-103">Een leveranciersfactuur in het factuurjournaal registreren</span><span class="sxs-lookup"><span data-stu-id="86c06-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86c06-104">Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="86c06-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="86c06-105">Voorbeelden van dit type factuur zijn onkosten voor levering of services.</span><span class="sxs-lookup"><span data-stu-id="86c06-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="86c06-106">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="86c06-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="86c06-107">Ga naar **Navigatievenster > Modules > Leveranciers > Werkgebieden > Leveranciersfactuurregistratie**.</span><span class="sxs-lookup"><span data-stu-id="86c06-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="86c06-108">Klik in het **actievenster** op **Nieuw factuurjournaal**.</span><span class="sxs-lookup"><span data-stu-id="86c06-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="86c06-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="86c06-109">Click **New**.</span></span>
4. <span data-ttu-id="86c06-110">Voer in het veld **Naam** de journaalnaam in of klik op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="86c06-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="86c06-111">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="86c06-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="86c06-112">Klik in het **actievenster** op **Regels**.</span><span class="sxs-lookup"><span data-stu-id="86c06-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="86c06-113">Voer in het veld **Datum** de boekingsdatum in waarmee Grootboek wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="86c06-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="86c06-114">Geef in het veld **Rekening** de **Leveranciersrekening** op.</span><span class="sxs-lookup"><span data-stu-id="86c06-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="86c06-115">Voer in het veld **Factuur** het factuurnummer in.</span><span class="sxs-lookup"><span data-stu-id="86c06-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="86c06-116">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="86c06-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="86c06-117">Voer in het veld **Krediet** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="86c06-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="86c06-118">Voer in het veld **Tegenrekening** het rekeningnummer in of klik op de vervolgkeuzeknop om de zoekopdracht te openen</span><span class="sxs-lookup"><span data-stu-id="86c06-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="86c06-119">De **btw-groep** wordt standaard uit de leveranciersrekening opgehaald.</span><span class="sxs-lookup"><span data-stu-id="86c06-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="86c06-120">De **Btw-groep van het artikel** wordt standaard opgehaald uit de hoofdrekening die is opgegeven in het veld **Tegenrekening**.</span><span class="sxs-lookup"><span data-stu-id="86c06-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="86c06-121">De **Vervaldatum** wordt berekend aan de hand van de betalingsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="86c06-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="86c06-122">De **Contantkorting** is afkomstig van de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="86c06-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="86c06-123">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="86c06-123">Click **Post**.</span></span>
13. <span data-ttu-id="86c06-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="86c06-124">Close the page.</span></span>

