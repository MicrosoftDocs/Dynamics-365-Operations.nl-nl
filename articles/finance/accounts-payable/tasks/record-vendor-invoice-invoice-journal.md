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
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177222"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="49241-103">Een leveranciersfactuur in het factuurjournaal registreren</span><span class="sxs-lookup"><span data-stu-id="49241-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49241-104">Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="49241-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="49241-105">Voorbeelden van dit type factuur zijn onkosten voor levering of services.</span><span class="sxs-lookup"><span data-stu-id="49241-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="49241-106">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="49241-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="49241-107">Ga naar **Navigatievenster > Modules > Leveranciers > Werkgebieden > Leveranciersfactuurregistratie**.</span><span class="sxs-lookup"><span data-stu-id="49241-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="49241-108">Klik in het **actievenster** op **Nieuw factuurjournaal**.</span><span class="sxs-lookup"><span data-stu-id="49241-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="49241-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="49241-109">Click **New**.</span></span>
4. <span data-ttu-id="49241-110">Voer in het veld **Naam** de journaalnaam in of klik op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="49241-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="49241-111">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="49241-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="49241-112">Klik in het **actievenster** op **Regels**.</span><span class="sxs-lookup"><span data-stu-id="49241-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="49241-113">Voer in het veld **Datum** de boekingsdatum in waarmee Grootboek wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="49241-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="49241-114">Geef in het veld **Rekening** de **Leveranciersrekening** op.</span><span class="sxs-lookup"><span data-stu-id="49241-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="49241-115">Voer in het veld **Factuur** het factuurnummer in.</span><span class="sxs-lookup"><span data-stu-id="49241-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="49241-116">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="49241-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="49241-117">Voer in het veld **Krediet** een numerieke waarde in.</span><span class="sxs-lookup"><span data-stu-id="49241-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="49241-118">Voer in het veld **Tegenrekening** het rekeningnummer in of klik op de vervolgkeuzeknop om de zoekopdracht te openen</span><span class="sxs-lookup"><span data-stu-id="49241-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="49241-119">De **btw-groep** wordt standaard uit de leveranciersrekening opgehaald.</span><span class="sxs-lookup"><span data-stu-id="49241-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="49241-120">De **Btw-groep van het artikel** wordt standaard opgehaald uit de hoofdrekening die is opgegeven in het veld **Tegenrekening**.</span><span class="sxs-lookup"><span data-stu-id="49241-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="49241-121">De **Vervaldatum** wordt berekend aan de hand van de betalingsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="49241-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="49241-122">De **Contantkorting** is afkomstig van de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="49241-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="49241-123">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="49241-123">Click **Post**.</span></span>
13. <span data-ttu-id="49241-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="49241-124">Close the page.</span></span>

