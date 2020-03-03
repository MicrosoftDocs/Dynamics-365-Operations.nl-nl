---
title: Betalingsmethoden
description: Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd wanneer het systeem wordt ingesteld. In dit artikel wordt beschreven welke betalingstypen u kunt instellen en wordt het proces beschreven voor het instellen hiervan.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6afbddad869c70e4527c49fc5d4b520d7602f825
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022187"
---
# <a name="payment-methods"></a><span data-ttu-id="4e245-104">Betalingsmethoden</span><span class="sxs-lookup"><span data-stu-id="4e245-104">Payment methods</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e245-105">Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd wanneer het systeem wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="4e245-105">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="4e245-106">In dit artikel wordt beschreven welke betalingstypen u kunt instellen en wordt het proces beschreven voor het instellen hiervan.</span><span class="sxs-lookup"><span data-stu-id="4e245-106">This article describes the payment types that you can set up and describes the process for setting them up.</span></span>

<span data-ttu-id="4e245-107">Detailhandelaren kunnen verschillende typen betaling accepteren voor de producten en diensten die ze verkopen.</span><span class="sxs-lookup"><span data-stu-id="4e245-107">Retailers can accept various types of payment in exchange for the products and services that they sell.</span></span> <span data-ttu-id="4e245-108">Hoewel contantbetalingen de meestvoorkomende vorm van betalingen zijn, kunnen detailhandelaren ook betalingen ontvangen in de vorm van cheques, kaarten, tegoedbonnen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="4e245-108">Although cash is the most common form of payment, retailers can also receive payment in the form of checks, cards, vouchers, and so on.</span></span> <span data-ttu-id="4e245-109">Elk betalingstype dat de detailhandelaar accepteert, moet worden geconfigureerd in Dynamics 365 Commerce wanneer het systeem wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="4e245-109">Each payment type that the retailer accepts must be configured in Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="4e245-110">De volgende lijst bevat omschrijvingen van elk betalingstype dat kan worden ingesteld:</span><span class="sxs-lookup"><span data-stu-id="4e245-110">The following list describes each payment type that can be set up:</span></span>

- <span data-ttu-id="4e245-111">**Contant**: geld in de fysieke vorm van valuta, zoals bankbiljetten en muntstukken.</span><span class="sxs-lookup"><span data-stu-id="4e245-111">**Cash** – Money in the physical form of currency, such as banknotes and coins.</span></span> <span data-ttu-id="4e245-112">Deze valuta kan de bedrijfsvaluta zijn of de lokale valuta van de winkel.</span><span class="sxs-lookup"><span data-stu-id="4e245-112">This currency can be either the company currency or the store's local currency.</span></span>
- <span data-ttu-id="4e245-113">**Cheque**: een verhandelbaar middel voor betaling van een bepaald bedrag in een bepaalde valuta door een bepaalde bank.</span><span class="sxs-lookup"><span data-stu-id="4e245-113">**Check** – A negotiable instrument that instructs payment of a specific amount of a specific currency, and that is drawn on a specific bank.</span></span> <span data-ttu-id="4e245-114">Een cheque is meestal geldig voor onbepaalde tijd of gedurende zes maanden na uitgifte, tenzij een andere geldigheidsperiode is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="4e245-114">A check is typically valid either indefinitely or for six months after the date of issue, unless another period of validity is specified.</span></span> <span data-ttu-id="4e245-115">De periode varieert, afhankelijk van de bank waar de cheque wordt geïnd.</span><span class="sxs-lookup"><span data-stu-id="4e245-115">This period varies, depending on the bank that the check is drawn on.</span></span> <span data-ttu-id="4e245-116">Er zijn verschillende soorten cheques, zoals cheques aan order, cheques aan balie, cheques aan toonder en cheques op naam.</span><span class="sxs-lookup"><span data-stu-id="4e245-116">There are various kinds of checks, such as order checks, counter checks, bearer checks, and account payee checks.</span></span> <span data-ttu-id="4e245-117">U kunt cheques instellen als een betalingsmethode voor elke winkel.</span><span class="sxs-lookup"><span data-stu-id="4e245-117">You can set up checks as a payment method for each store.</span></span> <span data-ttu-id="4e245-118">Cheques kunnen worden geaccepteerd in de valuta die op het niveau van het bedrijf of de winkel is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="4e245-118">Checks can be accepted in the currency that is defined at either the company level or the store level.</span></span> <span data-ttu-id="4e245-119">U moet cheques instellen als een betalingsmethode voordat u een cheque kunt accepteren als betaling in een winkel.</span><span class="sxs-lookup"><span data-stu-id="4e245-119">You must set up checks as a payment method before you can accept a check as payment in a store.</span></span>
- <span data-ttu-id="4e245-120">**Valuta**: de hoofdvorm van betaling anders dan de standaardvaluta van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="4e245-120">**Currency** – The primary form of payment other than the company's default currency.</span></span> <span data-ttu-id="4e245-121">Munten en bankbiljetten zijn beide vormen van valuta.</span><span class="sxs-lookup"><span data-stu-id="4e245-121">Coins and paper money are both forms of currency.</span></span> <span data-ttu-id="4e245-122">Deze betalingsmethode vertegenwoordigt alle valuta's die worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4e245-122">The currency payment method represents all currency that is used.</span></span> <span data-ttu-id="4e245-123">Voordat u deze betalingsmethode kunt gebruiken, moet u valuta's instellen en wisselgegevens voor de valuta's opgeven.</span><span class="sxs-lookup"><span data-stu-id="4e245-123">Before you can use this payment method, you must set up currencies and specify exchange information for the currencies.</span></span>
- <span data-ttu-id="4e245-124">**Kaart**: Alle typen kaarten die worden gebruikt, zoals betaalpassen en creditcards.</span><span class="sxs-lookup"><span data-stu-id="4e245-124">**Card** – All the kinds of cards that are used, such as debit cards and credit cards.</span></span> <span data-ttu-id="4e245-125">Het is een goed idee om op organisatieniveau maar één kaartbetalingsmethode in te stellen die alle typen kaarten vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="4e245-125">It's a good idea to set up one card payment method at the organization level, to represent every kind of card.</span></span> <span data-ttu-id="4e245-126">Op het niveau van de winkel kan vervolgens een betalingsmethode worden ingesteld voor elke kaart of reeks kaarten die met dezelfde instellingen moet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="4e245-126">Then, at the store level, set up a payment method for each card or set of cards that is processed by using the same settings.</span></span> <span data-ttu-id="4e245-127">U moet instellen om welke kaarten het gaat, met andere woorden betaalpassen en creditcards, voordat u de kaarten in een winkel als betaling kunt accepteren.</span><span class="sxs-lookup"><span data-stu-id="4e245-127">You must set up the manufacturer cards that are available in the market, such as debit cards and credit cards, before you can accept the cards as payment in a store.</span></span>
- <span data-ttu-id="4e245-128">**Creditnota** - Creditnota's die worden uitgegeven of ingewisseld bij het verkooppunt.</span><span class="sxs-lookup"><span data-stu-id="4e245-128">**Credit memo** – Credit memos that are issued or redeemed at the point of sale.</span></span> <span data-ttu-id="4e245-129">De creditnota kan een creditnota of retourcreditnota zijn die is uitgegeven tegen een retourverkoop.</span><span class="sxs-lookup"><span data-stu-id="4e245-129">The credit memo can be a credit or a return credit memo that is issued against a return sale.</span></span> <span data-ttu-id="4e245-130">Als creditnota's slechts gedeeltelijk worden ingewisseld, geeft het programma een nieuwe creditnota uit voor het nieuwe saldo.</span><span class="sxs-lookup"><span data-stu-id="4e245-130">If credit memos are only partially redeemed, the program issues a new credit memo for the new balance.</span></span> <span data-ttu-id="4e245-131">De nieuwe creditnota heeft een nieuw nummer.</span><span class="sxs-lookup"><span data-stu-id="4e245-131">The new credit memo has a new number.</span></span> <span data-ttu-id="4e245-132">Een creditnota kan maar één keer worden gebruikt en alle gebruikte nummers worden in het systeem geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="4e245-132">A credit memo can be used only one time, and the system keeps a record of all the numbers that are used.</span></span> <span data-ttu-id="4e245-133">De record kan op de pagina **Creditnotatabel** worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4e245-133">The record can be viewed on the **Credit memo table** page.</span></span> <span data-ttu-id="4e245-134">Een klant kan geen groter bedrag inwisselen dan de waarde van de creditnota.</span><span class="sxs-lookup"><span data-stu-id="4e245-134">A customer can't redeem more than the value of the credit memo.</span></span>
- <span data-ttu-id="4e245-135">**Geschenkbon**: geschenkbonnen die worden uitgegeven of ingewisseld bij het verkooppunt.</span><span class="sxs-lookup"><span data-stu-id="4e245-135">**Gift Card** – Gift cards that are issued and redeemed at the point of sale.</span></span> <span data-ttu-id="4e245-136">Overbetaling op geschenkbonnen is niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="4e245-136">Overpayment isn't allowed on gift cards.</span></span>
- <span data-ttu-id="4e245-137">**Klantrekening**: betalingen die op het moment van de verkoop kunnen worden afgeschreven van de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="4e245-137">**Customer account** – Payments that can be charged to a customer account at the register at the time of the sale.</span></span> <span data-ttu-id="4e245-138">U kunt deze betalingsmethode ook gebruiken om verkoopinformatie of klantspecifieke kortingen te verzamelen wanneer de klant op een andere manier een betaling doet.</span><span class="sxs-lookup"><span data-stu-id="4e245-138">You can also use this payment method to collect sales information or customer-specific discounts when the customer makes a payment by using another payment method.</span></span> <span data-ttu-id="4e245-139">In dat geval moet u klantspecifieke informatie hebben ingesteld.</span><span class="sxs-lookup"><span data-stu-id="4e245-139">In this case, you must set up customer-specific information.</span></span>
- <span data-ttu-id="4e245-140">**Loyaliteitspunten** : Het aantal punten dat klanten door middel van loyaliteitsprogramma's verzamelt.</span><span class="sxs-lookup"><span data-stu-id="4e245-140">**Loyalty points** – The points that customers accumulate through loyalty programs.</span></span> <span data-ttu-id="4e245-141">Als u loyaliteitsprogramma's maakt, kunnen klanten punten behalen en deze vervolgens op verschillende manieren terugkopen.</span><span class="sxs-lookup"><span data-stu-id="4e245-141">If you create loyalty programs, customers can earn points and then redeem them in various ways.</span></span> <span data-ttu-id="4e245-142">In sommige loyaliteitsprogramma's kunnen klanten bijvoorbeeld loyaliteitspunten terugkopen in de vorm van een korting of deze zelfs gebruiken als vorm van betaling.</span><span class="sxs-lookup"><span data-stu-id="4e245-142">For example, in some loyalty programs, customers can redeem loyalty points in the form of a discount or even use them as a form of payment.</span></span>

<span data-ttu-id="4e245-143">Voor het instellen van betalingsmethoden moet u de volgende taken voltooien.</span><span class="sxs-lookup"><span data-stu-id="4e245-143">To set up payment methods, you must complete the following tasks.</span></span>

1. <span data-ttu-id="4e245-144">Betalingsmethoden instellen voor een organisatie.</span><span class="sxs-lookup"><span data-stu-id="4e245-144">Set up payment methods for an organization.</span></span> <span data-ttu-id="4e245-145">De betalingsmethoden maken die in de gehele organisatie worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="4e245-145">Create the payment methods that are accepted by the whole organization.</span></span>
2. <span data-ttu-id="4e245-146">Kaarttypen en kaartnummers voor de hele organisatie maken.</span><span class="sxs-lookup"><span data-stu-id="4e245-146">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="4e245-147">Als creditcards of betaalpassen worden geaccepteerd, moet u één betalingsmethode maken voor kaarten en vervolgens de typen kaarten en kaartnummers voor de organisatie maken.</span><span class="sxs-lookup"><span data-stu-id="4e245-147">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="4e245-148">Betalingsmethoden voor winkels instellen.</span><span class="sxs-lookup"><span data-stu-id="4e245-148">Set up store payment method.</span></span> <span data-ttu-id="4e245-149">Koppel betalingsmethoden aan elke winkel en voer vervolgens de winkelspecifieke instellingen in voor elke betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="4e245-149">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="4e245-150">Betalingsmethoden via kaart instellen voor winkels.</span><span class="sxs-lookup"><span data-stu-id="4e245-150">Set up card payment methods for stores.</span></span> <span data-ttu-id="4e245-151">Voltooi de kaartinstellingen voor alle kaartbetalingsmethoden die door de winkel worden geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="4e245-151">For any card payment methods that the store accepts, complete the card setup.</span></span>