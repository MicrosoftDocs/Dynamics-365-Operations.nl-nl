---
title: TDS berekenen voor intercompany-transacties
description: Dit onderwerp beschrijft het proces dat wordt gebruikt om belasting ingehouden op bron (TDS) te berekenen op intercompany-transacties in fasen.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023151"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="32d18-103">TDS berekenen voor intercompany-transacties</span><span class="sxs-lookup"><span data-stu-id="32d18-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32d18-104">Dit onderwerp beschrijft het proces dat wordt gebruikt om belasting ingehouden op bron (TDS) te berekenen op intercompany-transacties in fasen.</span><span class="sxs-lookup"><span data-stu-id="32d18-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="32d18-105">Wanneer een intercompany-inkooporder of -verkooporder wordt gemaakt, wordt de standaard-TDS-groep die voor de klant of leverancier is gedefinieerd gebruikt om het TDS-bedrag te berekenen.</span><span class="sxs-lookup"><span data-stu-id="32d18-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="32d18-106">Het TDS-bedrag wordt geboekt naar de rekening voor terug te vorderen of te betalen nadat de factuur is geboekt.</span><span class="sxs-lookup"><span data-stu-id="32d18-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="32d18-107">Voor de oorspronkelijke inkoop- of verkooporder wordt automatisch een intercompany-verkooporder of -inkooporder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="32d18-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="32d18-108">De standaard-TDS-groep wordt weergegeven op de intercompany-order, zodat TDS kan worden berekend.</span><span class="sxs-lookup"><span data-stu-id="32d18-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="32d18-109">U kunt de TDS-groep wijzigen.</span><span class="sxs-lookup"><span data-stu-id="32d18-109">You can change the TDS group.</span></span> <span data-ttu-id="32d18-110">De factuur kan alleen worden geboekt als het nettofactuurbedrag op de intercompany-order die automatisch wordt gemaakt, overeenkomt met het nettofactuurbedrag op de oorspronkelijke order.</span><span class="sxs-lookup"><span data-stu-id="32d18-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="32d18-111">(Het nettobedrag is het factuurbedrag nadat TDS is ingehouden.)</span><span class="sxs-lookup"><span data-stu-id="32d18-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="32d18-112">Er wordt bijvoorbeeld een verkoopfactuur van 50.000 gemaakt en daar is de TDS-groep van **10%** aan gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="32d18-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="32d18-113">Het geboekte factuurbedrag is 45.000 en het geboekte TDS-bedrag voor de verkoopfactuur is 5.000.</span><span class="sxs-lookup"><span data-stu-id="32d18-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="32d18-114">Er wordt automatisch een inkooporder gemaakt voor de intercompany-verkooporder en de TDS-groep van **10%** wordt eraan gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="32d18-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="32d18-115">Als u de TDS-groep wijzigt in **15%**, kunt u de factuur niet boeken, omdat het nettofactuurbedrag van de intercompany-verkooporder die automatisch is gemaakt, niet gelijk is aan het nettofactuurbedrag van de oorspronkelijke verkooporder.</span><span class="sxs-lookup"><span data-stu-id="32d18-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="32d18-116">Er wordt automatisch een betalingsjournaal geboekt dat voor een intercompany-factuur is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="32d18-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="32d18-117">Dat betalingsjournaal kan alleen worden geboekt als het nettobetalingsbedrag hier overeenkomt met het nettobetalingsbedrag in het oorspronkelijke betalingsjournaal.</span><span class="sxs-lookup"><span data-stu-id="32d18-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
