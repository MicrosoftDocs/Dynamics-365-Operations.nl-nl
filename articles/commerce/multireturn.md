---
title: Artikelen voor meerdere klantorders en facturen retourneren
description: In dit onderwerp wordt de functionaliteit voor het inschakelen van retouren via meerdere klantorders en facturen in Dynamics 365 Commerce beschreven.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4a64794a0e04516441fab628d441640e4d154b8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796883"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="d8f19-103">Artikelen voor meerdere klantorders en facturen retourneren</span><span class="sxs-lookup"><span data-stu-id="d8f19-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="d8f19-104">In dit artikel worden twee functies beschreven die het retourneren van klantorders voor meerdere facturen optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="d8f19-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="d8f19-105">Restituties via meerdere registraties inschakelen</span><span class="sxs-lookup"><span data-stu-id="d8f19-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="d8f19-106">Met deze functie worden meerdere gekoppelde terugbetalingen mogelijk voor dezelfde klantorder.</span><span class="sxs-lookup"><span data-stu-id="d8f19-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="d8f19-107">Ga naar het werkgebied **Functiebeheer** en zoek naar **Restituties via meerdere registraties inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d8f19-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="d8f19-108">Selecteer **Restituties via meerdere orders inschakelen** en klik vervolgens op **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d8f19-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="d8f19-109">De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen</span><span class="sxs-lookup"><span data-stu-id="d8f19-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="d8f19-110">Deze functie zorgt ervoor dat wanneer een order wordt geretourneerd met meerdere facturen, de btw uiteindelijk gelijk is aan het oorspronkelijke aangerekende btw-bedrag.</span><span class="sxs-lookup"><span data-stu-id="d8f19-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="d8f19-111">Ga naar het werkgebied **Functiebeheer** en zoek naar **De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d8f19-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="d8f19-112">Selecteer **De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen** en klik vervolgens op **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d8f19-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="d8f19-113">Retouren verwerken</span><span class="sxs-lookup"><span data-stu-id="d8f19-113">Process returns</span></span>

<span data-ttu-id="d8f19-114">Wanneer deze functies zijn ingeschakeld en de wijzigingen zijn gesynchroniseerd met de winkels, kan de kassamedewerker in de winkel meerdere verkooporders voor een klant selecteren voor retour.</span><span class="sxs-lookup"><span data-stu-id="d8f19-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="d8f19-115">Wanneer de orders zijn geselecteerd, wordt een lijst met alle retourneerbare producten voor alle facturen voor de orders weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d8f19-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="d8f19-116">De kassamedewerker kan vervolgens de te retourneren producten selecteren.</span><span class="sxs-lookup"><span data-stu-id="d8f19-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="d8f19-117">Er wordt één retourorder gemaakt voor de geselecteerde producten.</span><span class="sxs-lookup"><span data-stu-id="d8f19-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="d8f19-118">Als de order volledig is geretourneerd, is het btw-bedrag dat aan de klant is geretourneerd, gelijk aan het oorspronkelijk aangerekende btw-bedrag.</span><span class="sxs-lookup"><span data-stu-id="d8f19-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]