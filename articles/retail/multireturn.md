---
title: Artikelen voor meerdere klantorders en facturen retourneren
description: In dit onderwerp wordt de functionaliteit voor het inschakelen van retouren via meerdere klantorders en facturen in Microsoft Dynamics 365 for Retail beschreven.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c201311028b11121d626e93859a2b98497c047d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565295"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="09463-103">Artikelen voor meerdere klantorders en facturen retourneren</span><span class="sxs-lookup"><span data-stu-id="09463-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="09463-104">In Dynamics 365 for Finance and Operations versie 10.0 kunnen retouren voor meerdere orders en facturen worden gemaakt terwijl in eerdere versies dan 10.0 retouren slechts op basis van één factuur tegelijk konden worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="09463-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="09463-105">Retail configureren om retouren voor meerdere klantorders en facturen te ondersteunen</span><span class="sxs-lookup"><span data-stu-id="09463-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="09463-106">Ga naar **Detailhandelparameters \> Klantorders**.</span><span class="sxs-lookup"><span data-stu-id="09463-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="09463-107">Schakel de parameter **Retouren voor meerdere orders inschakelen** in.</span><span class="sxs-lookup"><span data-stu-id="09463-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="09463-108">Retouren verwerken</span><span class="sxs-lookup"><span data-stu-id="09463-108">Process returns</span></span>

<span data-ttu-id="09463-109">Wanneer de parameter is ingeschakeld en de wijzigingen zijn gesynchroniseerd met de winkels, kan de kassamedewerker in de winkel meerdere verkooporders voor een klant selecteren voor retour.</span><span class="sxs-lookup"><span data-stu-id="09463-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="09463-110">Wanneer de orders zijn geselecteerd, wordt een lijst met alle retourneerbare producten voor alle facturen voor de orders weergegeven.</span><span class="sxs-lookup"><span data-stu-id="09463-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="09463-111">De kassamedewerker kan vervolgens de te retourneren producten selecteren.</span><span class="sxs-lookup"><span data-stu-id="09463-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="09463-112">Er wordt één retourorder gemaakt voor de geselecteerde producten.</span><span class="sxs-lookup"><span data-stu-id="09463-112">A single return order will be created for all the selected products.</span></span>
