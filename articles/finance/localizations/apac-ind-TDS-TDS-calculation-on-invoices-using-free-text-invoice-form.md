---
title: TDS-berekening op facturen van de pagina Vrije-tekstfactuur
description: In dit onderwerp wordt uitgelegd hoe u TDS-belasting op facturen berekent met behulp van de pagina Vrije-tekstfactuur.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023154"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="620c9-103">TDS-berekening op facturen van de pagina Vrije-tekstfactuur</span><span class="sxs-lookup"><span data-stu-id="620c9-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="620c9-104">In dit onderwerp wordt uitgelegd hoe u TDS-belasting op facturen berekent met behulp van de pagina **Vrije-tekstfactuur**.</span><span class="sxs-lookup"><span data-stu-id="620c9-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="620c9-105">Ga naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**.</span><span class="sxs-lookup"><span data-stu-id="620c9-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="620c9-106">[![Pagina Vrije-tekstfactuur](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="620c9-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="620c9-107">Selecteer **Nieuw** om een vrije-tekstfactuur te maken en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="620c9-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="620c9-108">Selecteer het tabblad **Factuur**. In de sectie **Bronbelastinggroep** wordt in het veld **Soort belastingplichtige** de soort belastingplichtige weergegeven waar de leverancier of klant toe hoort.</span><span class="sxs-lookup"><span data-stu-id="620c9-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="620c9-109">Controleer of wijzig in het veld **TDS-groep** de standaard-TDS-groep die voor de klant is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="620c9-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="620c9-110">Wanneer u een waarde selecteert in het veld **TDS-groep**, is het veld **TCS-groep** niet meer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="620c9-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="620c9-111">TDS wordt alleen berekend als de optie **Bronbelasting berekenen** is ingesteld op **Ja** voor de klant op de pagina **Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="620c9-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="620c9-112">Selecteer op het tabblad **Belastinginformatie** kunt u in de sectie **Bedrijfsgegevens** in het veld **Naam** de bedrijfsnaam voor een alternatief adres dat voor het bedrijf is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="620c9-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="620c9-113">In de sectie **Bronbelasting** staat in het veld **Belastingrekeningnummer (TAN)** het belastingrekeningnummer van het geselecteerde bedrijf.</span><span class="sxs-lookup"><span data-stu-id="620c9-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="620c9-114">Maak op het tabblad **Factuurregels** factuurregels en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="620c9-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="620c9-115">In de sectie **Bronbelastinggroep** staat in het veld **Belastingrekeningnummer (TAN)** het belastingrekeningnummer en in het veld **TDS-groep** wordt de TDS-groep getoond.</span><span class="sxs-lookup"><span data-stu-id="620c9-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="620c9-116">Selecteer **Bronbelasting** om de pagina **Tijdelijke bronbelastingtransacties** te openen.</span><span class="sxs-lookup"><span data-stu-id="620c9-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="620c9-117">Het bovenste deel van deze pagina heeft de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="620c9-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="620c9-118">**Totaalbedrag bronbelasting**: het totale TDS-bedrag dat voor de transactie voor de TDS-groep is berekend.</span><span class="sxs-lookup"><span data-stu-id="620c9-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="620c9-119">**Waarde** het totale percentage dat is gebruikt om TDS voor de transactie te berekenen.</span><span class="sxs-lookup"><span data-stu-id="620c9-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="620c9-120">Het totale percentage is gebaseerd op de formule die is gedefinieerd voor de TDS-belastingcodes en is gekoppeld aan de TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="620c9-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="620c9-121">**Totaal gecorrigeerd bronbelastingbedrag**: het totale gecorrigeerde TDS-bedrag voor alle belastingcodes in de TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="620c9-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="620c9-122">**TDS**: een ingeschakeld selectievakje geeft aan dat er een TDS-groep aan de transactie is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="620c9-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="620c9-123">De velden op de tabbladen **Overzicht**, **Algemeen** en **Correctie** geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="620c9-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="620c9-124">Selecteer **Drempel** om de pagina **Drempel** te openen, waar u de drempellimiet kunt bekijken die is gedefinieerd voor de TDS-belastingcomponent die aan een specifieke TDS-belastingcode is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="620c9-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="620c9-125">Selecteer **Formuleontwerper** om de pagina **Formuleontwerper** te openen. Hier kunt u de formule bekijken die voor een specifieke TDS-belastingcode is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="620c9-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="620c9-126">Boek de vrije-tekstfactuur.</span><span class="sxs-lookup"><span data-stu-id="620c9-126">Post the free text invoice.</span></span> <span data-ttu-id="620c9-127">Het TDS-bedrag dat is berekend voor de vrije-tekstfactuur wordt geboekt naar de klantrekening die is gedefinieerd voor elke TDS-belastingcode in de TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="620c9-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="620c9-128">De klantenrekeningen voor TDS-belastingcodes worden gedefinieerd op de pagina **Bronbelastingcodes**.</span><span class="sxs-lookup"><span data-stu-id="620c9-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="620c9-129">Selecteer **Bronbelasting geboekt** om de pagina **Bronbelastingtransacties** te openen.</span><span class="sxs-lookup"><span data-stu-id="620c9-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="620c9-130">In het veld **Waarde** wordt het totale percentage weergegeven dat is gebruikt om TDS voor de transactie te berekenen.</span><span class="sxs-lookup"><span data-stu-id="620c9-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="620c9-131">De velden op de tabbladen **Overzicht**, **Algemeen** en **Bedrag** geven de TDS-bedragen weer die zijn berekend op de factuurregels.</span><span class="sxs-lookup"><span data-stu-id="620c9-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="620c9-132">Controleer de TDS-berekeningsgegevens voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="620c9-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
