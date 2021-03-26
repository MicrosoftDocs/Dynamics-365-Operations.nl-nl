---
title: Een uitwisseling voor een retourorder configureren en verwerken
description: In dit onderwerp wordt uitgelegd hoe u een uitwisseling voor een retour configureert in Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5419c18a510b0d35dabe5329a9557780cb7637b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257118"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="e99c3-103">Een uitwisseling voor een retourorder configureren en verwerken</span><span class="sxs-lookup"><span data-stu-id="e99c3-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e99c3-104">In eerdere versies van Dynamics 365 Commerce werden retouren van klantorders verwerkt op basis van het retourorderdocument in Headquarters.</span><span class="sxs-lookup"><span data-stu-id="e99c3-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="e99c3-105">Het retourorderdocument kan echter alleen worden gebruikt om producten te verwerken die worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e99c3-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="e99c3-106">De geretourneerde producten worden aangeduid met een negatieve hoeveelheid op de retourorderregels.</span><span class="sxs-lookup"><span data-stu-id="e99c3-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="e99c3-107">De verkopen worden weergegeven met een positieve hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="e99c3-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="e99c3-108">Het retourorderdocument ondersteunt echter geen positieve hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="e99c3-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="e99c3-109">Vanwege deze beperking boden eerdere versies van de app geen ondersteuning voor scenario's waarin productuitwisselingen werden uitgevoerd met behulp van het retourorderdocument.</span><span class="sxs-lookup"><span data-stu-id="e99c3-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="e99c3-110">Er is echter functionaliteit toegevoegd om scenario's met uitwisselingen voor retourorders te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="e99c3-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="e99c3-111">In Commerce wordt in plaats van het retourorderdocument nu het verkooporderdocument gebruikt voor de verwerking van deze typen transacties.</span><span class="sxs-lookup"><span data-stu-id="e99c3-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="e99c3-112">Commerce configureren om uitwisseling te ondersteunen voor retourorders</span><span class="sxs-lookup"><span data-stu-id="e99c3-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="e99c3-113">Ga als volgt te werk om het systeem zo te configureren dat uitwisseling wordt ondersteund voor retourorders.</span><span class="sxs-lookup"><span data-stu-id="e99c3-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="e99c3-114">Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters**.</span><span class="sxs-lookup"><span data-stu-id="e99c3-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="e99c3-115">Stel op het sneltabblad **Klantorders** de optie **Retourorders verwerken als verkooporders** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e99c3-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="e99c3-116">Voer de taak **Algemene configuratie distributieplanning** (**1110**) uit.</span><span class="sxs-lookup"><span data-stu-id="e99c3-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="e99c3-117">Uitwisselen</span><span class="sxs-lookup"><span data-stu-id="e99c3-117">Make an exchange</span></span>

<span data-ttu-id="e99c3-118">Wanneer het systeem is geconfigureerd op de wijze die wordt beschreven in de vorige sectie, selecteert de POS-gebruiker net als in vorige versies van de app een verkooporder of verkoopfactuur om een retour te verwerken.</span><span class="sxs-lookup"><span data-stu-id="e99c3-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="e99c3-119">Wanneer de retourartikelen zijn toegevoegd aan de winkelwagen, kan de gebruiker echter ook nieuwe verkoopregels toevoegen aan de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="e99c3-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="e99c3-120">Voor deze nieuwe verkoopregels moet de gebruiker alle kenmerken opgeven die vereist zijn om een klantorderregel te verwerken.</span><span class="sxs-lookup"><span data-stu-id="e99c3-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="e99c3-121">Deze kenmerken omvatten de leveringsmethode en afhandelingslocatie.</span><span class="sxs-lookup"><span data-stu-id="e99c3-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="e99c3-122">Het verschuldigde transactiebedrag is het gecombineerde nettobedrag van de retour- en verkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="e99c3-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="e99c3-123">Wanneer voor de transactie wordt betaald, wordt de retourorder geboekt als een verkooporderdocument in Headquarters en worden de retourregels onmiddellijk gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="e99c3-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="e99c3-124">Om beter inzicht te bieden in de verschillende bedragen voor de winkelwagen, zijn er drie nieuwe velden voor bedragen toegevoegd aan de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="e99c3-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="e99c3-125">U kunt de schermontwerper gebruiken om deze nieuwe velden beschikbaar te maken in de POS-gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="e99c3-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="e99c3-126">**Deposito toegepast**: het depositobedrag dat op een transactie wordt toegepast wanneer de gebruiker een klantorder ophaalt.</span><span class="sxs-lookup"><span data-stu-id="e99c3-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="e99c3-127">Als er geen deposito-overschrijving is ingesteld en een deposito van 10 procent is geconfigureerd, is het bedrag in dit veld 90 procent van het totaalbedrag van de klantorder.</span><span class="sxs-lookup"><span data-stu-id="e99c3-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="e99c3-128">**Uitgevoerd bedrag**: het totale bedrag voor regels waarvoor de leveringsmethode was ingesteld op **Uitgevoerd** toen de klantorder werd gemaakt of bewerkt, of tijdens de uitwisseling van een klantorder.</span><span class="sxs-lookup"><span data-stu-id="e99c3-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="e99c3-129">Het bedrag in dit veld is inclusief btw en toeslagen.</span><span class="sxs-lookup"><span data-stu-id="e99c3-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="e99c3-130">**Geretourneerd bedrag**: het totaalbedrag voor regels met negatieve hoeveelheden tijdens de uitwisseling van een klantorder.</span><span class="sxs-lookup"><span data-stu-id="e99c3-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="e99c3-131">Het bedrag in dit veld is inclusief btw en toeslagen.</span><span class="sxs-lookup"><span data-stu-id="e99c3-131">The amount in this field includes taxes and charges.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]