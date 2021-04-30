---
title: Indextarieven instellen
description: In dit onderwerp wordt uitgelegd hoe u indextarieven instelt. Indextarieven zijn vereist als uw organisatie leasebetalingsbedragen met een set indextarieven koppelt.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40f230a9d69a142b18eb27a2d5e420dbadc600d2
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880955"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="88040-104">Indextarieven instellen</span><span class="sxs-lookup"><span data-stu-id="88040-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88040-105">Als leasebetalingen afhankelijk zijn van een index, kunnen de typen indextarieven worden toegevoegd en bijgehouden in het systeem.</span><span class="sxs-lookup"><span data-stu-id="88040-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="88040-106">Voor het herwaarderen van de leasebetalingen vanuit de pagina **Type indextarief**, gebruikt het herwaarderingsproces het meest recente indextarief van de herwaarderingsdatum.</span><span class="sxs-lookup"><span data-stu-id="88040-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="88040-107">Volg deze stappen om typen indextarieven en indextarieven toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="88040-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="88040-108">Ga naar **Activa leasen \> Instellingen \> Type indextarief**.</span><span class="sxs-lookup"><span data-stu-id="88040-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="88040-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="88040-109">Select **New**.</span></span>
3. <span data-ttu-id="88040-110">Voer in de betreffende velden het tarieftype en de naam van het indextarief in.</span><span class="sxs-lookup"><span data-stu-id="88040-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="88040-111">Selecteer het type indextarief en selecteer **Toevoegen** om een nieuwe waarde voor indextarief toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="88040-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="88040-112">Selecteer de effectieve begindatum van het tarief en selecteer de waarde van het tarief.</span><span class="sxs-lookup"><span data-stu-id="88040-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="88040-113">U moet **Waardeverschil indextarief** of **Waarde indextarief** selecteren als de indextariefmethode.</span><span class="sxs-lookup"><span data-stu-id="88040-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="88040-114">Selecteer de methode **Waardeverschil indextarief** om een nieuwe leasebetaling te berekenen op basis van het verschil tussen het indextarief op de begin datum en het meest recente indextarief.</span><span class="sxs-lookup"><span data-stu-id="88040-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="88040-115">Het indextarief wordt gedefinieerd in het veld **Indextarief (%)**.</span><span class="sxs-lookup"><span data-stu-id="88040-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="88040-116">Selecteer de methode **Waarde indextarief** om de leasebetaling te berekenen met behulp van het percentage dat is opgegeven in het veld **Indextarief (%)**.</span><span class="sxs-lookup"><span data-stu-id="88040-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
