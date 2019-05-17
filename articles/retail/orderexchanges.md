---
title: Een uitwisseling voor een retourorder configureren en verwerken
description: In dit onderwerp wordt uitgelegd hoe u een uitwisseling voor een retour configureert in Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a0a6a060a1b4a4d5a80c797f61b212a828d2f04
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517038"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="0a9b5-103">Een uitwisseling voor een retourorder configureren en verwerken</span><span class="sxs-lookup"><span data-stu-id="0a9b5-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a9b5-104">In eerdere versies van Microsoft Dynamics 365 for Retail werden retouren van klantorders verwerkt op basis van het retourorderdocument in Retail Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-104">In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</span></span> <span data-ttu-id="0a9b5-105">Het retourorderdocument kan echter alleen worden gebruikt om producten te verwerken die worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="0a9b5-106">De geretourneerde producten worden aangeduid met een negatieve hoeveelheid op de retourorderregels.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="0a9b5-107">De verkopen worden weergegeven met een positieve hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="0a9b5-108">Het retourorderdocument ondersteunt echter geen positieve hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="0a9b5-109">Vanwege deze beperking boden eerdere versies van Retail geen ondersteuning voor scenario's waarin productuitwisselingen werden uitgevoerd met behulp van het retourorderdocument.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="0a9b5-110">Er is echter functionaliteit toegevoegd om scenario's met uitwisselingen voor retourorders te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="0a9b5-111">In Retail wordt in plaats van het retourorderdocument nu het verkooporderdocument gebruikt voor de verwerking van deze typen transacties.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="0a9b5-112">Retail configureren om uitwisseling te ondersteunen voor retourorders</span><span class="sxs-lookup"><span data-stu-id="0a9b5-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="0a9b5-113">Ga als volgt te werk om het systeem zo te configureren dat uitwisseling wordt ondersteund voor retourorders.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="0a9b5-114">Ga naar **Detailhandel \> Instelling van hoofdkantoor \> Parameters \> Detailhandelparameters**.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="0a9b5-115">Stel op het sneltabblad **Klantorders** de optie **Retourorders verwerken als verkooporders** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="0a9b5-116">Voer de taak **Algemene configuratie distributieplanning** (**1110**) uit.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="0a9b5-117">Uitwisselen</span><span class="sxs-lookup"><span data-stu-id="0a9b5-117">Make an exchange</span></span>

<span data-ttu-id="0a9b5-118">Wanneer het systeem is geconfigureerd op de wijze die wordt beschreven in de vorige sectie, selecteert de POS-gebruiker net als in vorige versies van Retail een verkooporder of verkoopfactuur om een retour te verwerken.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="0a9b5-119">Wanneer de retourartikelen zijn toegevoegd aan de winkelwagen, kan de gebruiker echter ook nieuwe verkoopregels toevoegen aan de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="0a9b5-120">Voor deze nieuwe verkoopregels moet de gebruiker alle kenmerken opgeven die vereist zijn om een klantorderregel te verwerken.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="0a9b5-121">Deze kenmerken omvatten de leveringsmethode en afhandelingslocatie.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="0a9b5-122">Het verschuldigde transactiebedrag is het gecombineerde nettobedrag van de retour- en verkooporderregels.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="0a9b5-123">Wanneer voor de transactie wordt betaald, wordt de retourorder geboekt als een verkooporderdocument in Retail Headquarters en worden de retourregels onmiddellijk gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="0a9b5-124">Om beter inzicht te bieden in de verschillende bedragen voor de winkelwagen, zijn er drie nieuwe velden voor bedragen toegevoegd aan de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="0a9b5-125">U kunt de schermontwerper gebruiken om deze nieuwe velden beschikbaar te maken in de POS-gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="0a9b5-126">**Deposito toegepast**: het depositobedrag dat op een transactie wordt toegepast wanneer de gebruiker een klantorder ophaalt.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="0a9b5-127">Als er geen deposito-overschrijving is ingesteld en een deposito van 10 procent is geconfigureerd, is het bedrag in dit veld 90 procent van het totaalbedrag van de klantorder.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="0a9b5-128">**Uitgevoerd bedrag**: het totale bedrag voor regels waarvoor de leveringsmethode was ingesteld op **Uitgevoerd** toen de klantorder werd gemaakt of bewerkt, of tijdens de uitwisseling van een klantorder.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="0a9b5-129">Het bedrag in dit veld is inclusief btw en toeslagen.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="0a9b5-130">**Geretourneerd bedrag**: het totaalbedrag voor regels met negatieve hoeveelheden tijdens de uitwisseling van een klantorder.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="0a9b5-131">Het bedrag in dit veld is inclusief btw en toeslagen.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-131">The amount in this field includes taxes and charges.</span></span>
