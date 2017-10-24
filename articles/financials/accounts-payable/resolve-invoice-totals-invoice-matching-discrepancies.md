---
title: Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="da7fe-102">Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen</span><span class="sxs-lookup"><span data-stu-id="da7fe-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="da7fe-103">Een type factuurvereffeningsvalidatie is de factuurtotalenvereffening.</span><span class="sxs-lookup"><span data-stu-id="da7fe-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="da7fe-104">Om op te geven dat het systeem factuurvereffening voor totalen moet uitvoeren, stelt u op de pagina **Parameters van module Leveranciers** op het tabblad **Factuurvalidatie** u de optie **Factuurtotalen vereffenen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="da7fe-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="da7fe-105">U kunt factuurtotaalvergelijking gebruiken om te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil.</span><span class="sxs-lookup"><span data-stu-id="da7fe-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="da7fe-106">Er worden zes totalen vergeleken op de **Totale factuurvereffeningsgegevens** pagina.</span><span class="sxs-lookup"><span data-stu-id="da7fe-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="da7fe-107">Indien een van de totalen afwijkt van het verwachte corresponderende inkoopordertotaal, wordt een matchingverschil gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="da7fe-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="da7fe-108">Om de factuur met verschillende totalen in te zien, klikt u in de werkruimte op in de **Leveranciersfactuurregistratie** op de regel **Facturen in behandeling**.</span><span class="sxs-lookup"><span data-stu-id="da7fe-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="da7fe-109">Klik vervolgens in het actievenster op het tabblad **Controleren** op **Vereffeningsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="da7fe-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="da7fe-110">Als vereffeningsverschillen zijn gevonden, worden waarschuwende pictogrammen naast het factuurbedrag weergegeven.</span><span class="sxs-lookup"><span data-stu-id="da7fe-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="da7fe-111">U kunt meer details over de totalen weergeven door de vergelijkingsgegevens van de factuurtotalen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="da7fe-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="da7fe-112">Nadat u het verschil hebt aangegeven, kunt u contact opnemen met de leverancier als u denkt dat de informatie op de factuur niet klopt.</span><span class="sxs-lookup"><span data-stu-id="da7fe-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="da7fe-113">Afhankelijk van de uitkomst van dat gesprek kan de leverancier een van de volgende dingen doen:</span><span class="sxs-lookup"><span data-stu-id="da7fe-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="da7fe-114">Accepteer het prijsverschil en boek de factuur die matchingverschillen bevat.</span><span class="sxs-lookup"><span data-stu-id="da7fe-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="da7fe-115">Uw systeem kan worden ingesteld om goedkeuring te vereisen voordat kan worden geboekt als er vereffeningsverschillen zijn.</span><span class="sxs-lookup"><span data-stu-id="da7fe-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="da7fe-116">In dit geval moet u het vereffeningverschil goedkeuren en kunt u desgewenst een goedkeuringopmerking invoeren.</span><span class="sxs-lookup"><span data-stu-id="da7fe-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="da7fe-117">U kunt vervolgens de factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="da7fe-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="da7fe-118">Het factuurbedrag met het juiste bedrag corrigeren en de factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="da7fe-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="da7fe-119">Een volledig credit aan de leverancier vragen en om een nieuwe, gecorrigeerde factuur verzoeken.</span><span class="sxs-lookup"><span data-stu-id="da7fe-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="da7fe-120">Zie voor meer informatie [Uitzonderingen onderzoeken of oplossen](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="da7fe-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



