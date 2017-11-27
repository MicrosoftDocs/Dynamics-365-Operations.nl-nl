---
title: Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen
description: U kunt factuurtotaalvergelijking gebruiken om te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18250a735d0421daa90b923504aeb94b5003a6a7
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="6af66-103">Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen</span><span class="sxs-lookup"><span data-stu-id="6af66-103">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6af66-104">Een type factuurvereffeningsvalidatie is de factuurtotalenvereffening.</span><span class="sxs-lookup"><span data-stu-id="6af66-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="6af66-105">Om op te geven dat het systeem factuurvereffening voor totalen moet uitvoeren, stelt u op de pagina **Parameters van module Leveranciers** op het tabblad **Factuurvalidatie** u de optie **Factuurtotalen vereffenen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6af66-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="6af66-106">U kunt factuurtotaalvergelijking gebruiken om te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil.</span><span class="sxs-lookup"><span data-stu-id="6af66-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="6af66-107">Er worden zes totalen vergeleken op de **Totale factuurvereffeningsgegevens** pagina.</span><span class="sxs-lookup"><span data-stu-id="6af66-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="6af66-108">Indien een van de totalen afwijkt van het verwachte corresponderende inkoopordertotaal, wordt een matchingverschil gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="6af66-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="6af66-109">Om de factuur met verschillende totalen in te zien, klikt u in de werkruimte op in de **Leveranciersfactuurregistratie** op de regel **Facturen in behandeling**.</span><span class="sxs-lookup"><span data-stu-id="6af66-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="6af66-110">Klik vervolgens in het actievenster op het tabblad **Controleren** op **Vereffeningsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="6af66-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="6af66-111">Als vereffeningsverschillen zijn gevonden, worden waarschuwende pictogrammen naast het factuurbedrag weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6af66-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="6af66-112">U kunt meer details over de totalen weergeven door de vergelijkingsgegevens van de factuurtotalen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="6af66-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="6af66-113">Nadat u het verschil hebt aangegeven, kunt u contact opnemen met de leverancier als u denkt dat de informatie op de factuur niet klopt.</span><span class="sxs-lookup"><span data-stu-id="6af66-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="6af66-114">Afhankelijk van de uitkomst van dat gesprek kan de leverancier een van de volgende dingen doen:</span><span class="sxs-lookup"><span data-stu-id="6af66-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="6af66-115">Accepteer het prijsverschil en boek de factuur die matchingverschillen bevat.</span><span class="sxs-lookup"><span data-stu-id="6af66-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="6af66-116">Uw systeem kan worden ingesteld om goedkeuring te vereisen voordat kan worden geboekt als er vereffeningsverschillen zijn.</span><span class="sxs-lookup"><span data-stu-id="6af66-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="6af66-117">In dit geval moet u het vereffeningverschil goedkeuren en kunt u desgewenst een goedkeuringopmerking invoeren.</span><span class="sxs-lookup"><span data-stu-id="6af66-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="6af66-118">U kunt vervolgens de factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="6af66-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="6af66-119">Het factuurbedrag met het juiste bedrag corrigeren en de factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="6af66-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="6af66-120">Een volledig credit aan de leverancier vragen en om een nieuwe, gecorrigeerde factuur verzoeken.</span><span class="sxs-lookup"><span data-stu-id="6af66-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="6af66-121">Zie voor meer informatie [Uitzonderingen onderzoeken of oplossen](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="6af66-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



