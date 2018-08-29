---
title: De indirecte wisselkoers opgeven
description: Dit onderwerp biedt algemene informatie over indirecte wisselkoersen in Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="specify-the-cross-rate"></a><span data-ttu-id="6485d-103">De indirecte wisselkoers opgeven</span><span class="sxs-lookup"><span data-stu-id="6485d-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6485d-104">In dit hoofdstuk wordt het doel van een breed tarief uitgelegd en hoe dit brede tarief ingesteld kan worden bij het doen van een betaling via een factuur.</span><span class="sxs-lookup"><span data-stu-id="6485d-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="6485d-105">Gebruik een breed tarief als alle van de volgende criteria van toepassing zijn:</span><span class="sxs-lookup"><span data-stu-id="6485d-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="6485d-106">U vereffent een betaling met een factuur.</span><span class="sxs-lookup"><span data-stu-id="6485d-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="6485d-107">De valuta´s van de betalingsregel en de factuurregel zijn verschillend.</span><span class="sxs-lookup"><span data-stu-id="6485d-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="6485d-108">Geen van beide valuta´s is de valuta voor de boekhouding.</span><span class="sxs-lookup"><span data-stu-id="6485d-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="6485d-109">De indirecte wisselkoers wordt niet gebruikt voor de omrekening van de betalingstransactievaluta naar de boekhoudvaluta van de betaling.</span><span class="sxs-lookup"><span data-stu-id="6485d-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="6485d-110">In plaats daarvan worden de valutakoersen uit de wisselkoerstabellen opgehaald om de waarde te berekenen van het bedrag van de betalingstransactievaluta en het bedrag van de boekhoudvaluta.</span><span class="sxs-lookup"><span data-stu-id="6485d-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="6485d-111">De boekhoudvaluta is bijvoorbeeld USD, de factuurvaluta is CAD en de betalingsvaluta is EUR.</span><span class="sxs-lookup"><span data-stu-id="6485d-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="6485d-112">Met een breed tarief kunt u een wisselkoers invoeren die rechtstreeks tussen CAD en EUR vertaalt, waardoor er niet door USD vertaald hoeft te worden.</span><span class="sxs-lookup"><span data-stu-id="6485d-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="6485d-113">Wanneer u een factuur en een primaire betaling selecteert, kunt u een indirecte wisselkoers invoeren voor de factuurregel.</span><span class="sxs-lookup"><span data-stu-id="6485d-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="6485d-114">De indirecte wisselkoers is de wisselkoers tussen de valuta's voor de desbetreffende transacties, die geldt op de vereffeningsdatum.</span><span class="sxs-lookup"><span data-stu-id="6485d-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="6485d-115">Ga naar een van de volgende pagina's:</span><span class="sxs-lookup"><span data-stu-id="6485d-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="6485d-116">**Klanten > Algemeen > Klanten > Alle klanten**</span><span class="sxs-lookup"><span data-stu-id="6485d-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="6485d-117">**Leveranciers > Algemeen > Leveranciers > Alle leveranciers**</span><span class="sxs-lookup"><span data-stu-id="6485d-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="6485d-118">**Inkoop en sourcing > Algemeen > Leveranciers > Alle leveranciers**</span><span class="sxs-lookup"><span data-stu-id="6485d-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="6485d-119">Selecteer de klant of leverancier van wie u de openstaande transacties vereffent.</span><span class="sxs-lookup"><span data-stu-id="6485d-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="6485d-120">Ga voor een klant op de lijstpagina **Alle klanten** naar **Verzamelen > Openstaande transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="6485d-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="6485d-121">Ga voor een leverancier op de lijstpagina **Alle leveranciers** naar **Factuur > Openstaande transacties vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="6485d-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="6485d-122">Selecteer de transactie die de primaire betaling vormt en klik vervolgens op **Betaling markeren**.</span><span class="sxs-lookup"><span data-stu-id="6485d-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="6485d-123">Het selectievakje in de kolom **Markeren** is ingeschakeld en er wordt een informatiepictogram weergegeven in de kolom **Primaire betaling**.</span><span class="sxs-lookup"><span data-stu-id="6485d-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="6485d-124">Voer in het veld **Indirecte wisselkoers** de wisselkoers in tussen de factuurvaluta en de betalingsvaluta die geldt op de vereffeningsdatum.</span><span class="sxs-lookup"><span data-stu-id="6485d-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 

