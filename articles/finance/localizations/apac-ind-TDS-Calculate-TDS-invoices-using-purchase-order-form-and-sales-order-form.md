---
title: TDS-facturen berekenen met inkooporderformulier en verkooporderformulier
description: Dit onderwerp geeft een overzicht van de stappen voor het berekenen van TDS (belasting ingehouden op bron) op verschillende typen facturen.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023138"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="43884-103">TDS-facturen berekenen met inkooporderformulier en verkooporderformulier</span><span class="sxs-lookup"><span data-stu-id="43884-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43884-104">Dit onderwerp geeft een overzicht van de stappen voor het berekenen van TDS (belasting ingehouden op bron) op verschillende typen facturen met behulp van de pagina's **Inkooporder**, **Inkoopjournaal**, **Afroeporder** en **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="43884-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="43884-105">Maak een inkooporder, inkoopjournaal, afroeporder voor inkoop of een verkooporder op de weergegeven pagina.</span><span class="sxs-lookup"><span data-stu-id="43884-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="43884-106">Voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="43884-106">Enter the required details.</span></span>

2. <span data-ttu-id="43884-107">Op het tabblad **Instellingen** kunt u de soort belastingplichtige van de leverancier of klant.</span><span class="sxs-lookup"><span data-stu-id="43884-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="43884-108">Deze gegevens worden vermeld in het veld **Soort belastingplichtige**, onder de veldgroep **Bronbelastinggroep**.</span><span class="sxs-lookup"><span data-stu-id="43884-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="43884-109">Bekijk of wijzig in het veld **TDS-groep** de standaard-TDS-groep die voor de leverancier of klant is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="43884-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="43884-110">Wanneer u een TDS-groep selecteert in het veld **TDS-groep**, is het veld **TCS-groep** niet meer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="43884-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="43884-111">TDS wordt alleen berekend als het selectievakje **Bronbelasting berekenen** is ingeschakeld voor de leverancier of klant op de pagina **Alle leveranciers** of **Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="43884-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="43884-112">Maak op het tabblad **Regels** artikelrregels en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="43884-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="43884-113">Selecteer het tabblad **Instellingen** (regelniveau) om de TDS-groep weer te geven of te wijzigen die is gedefinieerd op koptekstniveau.</span><span class="sxs-lookup"><span data-stu-id="43884-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="43884-114">De TDS-groep wordt weergegeven in het veld **TDS-groep**, dat zich onder de veldgroep **Bronbelastinggroep** valt.</span><span class="sxs-lookup"><span data-stu-id="43884-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="43884-115">Selecteer het tabblad **Belastinginformatie** en selecteer alternatieve adressen die zijn ingesteld voor de bedrijfsnaam die in dit veld wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="43884-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="43884-116">De bedrijfsnaam wordt weergegeven in het veld **Naam**, dat onder de veldgroep **Bedrijfsgegevens** valt.</span><span class="sxs-lookup"><span data-stu-id="43884-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="43884-117">De TAN van de geselecteerde bedrijfsnaam wordt weergegeven in het veld **Belastingrekeningnummer** (**TAN**) onder de veldgroep **Bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="43884-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="43884-118">Selecteer **Bronbelasting** om de pagina **Tijdelijke bronbelastingtransacties** te openen.</span><span class="sxs-lookup"><span data-stu-id="43884-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="43884-119">Bekijk de volgende velden in het bovenste deelvenster van de pagina **Tijdelijke bronbelastingtransacties**.</span><span class="sxs-lookup"><span data-stu-id="43884-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="43884-120">**Totaalbedrag** **bronbelasting**: het totale TDS-bedrag dat voor de transactie voor de TDS-groep is berekend.</span><span class="sxs-lookup"><span data-stu-id="43884-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="43884-121">**Waarde**: het totale percentage dat is gebruikt om TDS voor de transactie te berekenen.</span><span class="sxs-lookup"><span data-stu-id="43884-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="43884-122">Het totale percentage is gebaseerd op de formule die is gedefinieerd voor TDS-belastingcodes gekoppeld aan de TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="43884-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="43884-123">**Totaal gecorrigeerd bronbelastingbedrag**: het totale gecorrigeerde TDS-bedrag voor alle belastingcodes in de TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="43884-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="43884-124">**TDS**: als deze optie is geselecteerd, is er een TDS-groep aan de transactie gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="43884-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="43884-125">De velden op de tabbladen **Overzicht**, **Algemeen** en **Correctie** op de pagina **Tijdelijke bronbelastingtransacties** geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="43884-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="43884-126">Selecteer **Drempel** om de pagina **Drempel** te openen.</span><span class="sxs-lookup"><span data-stu-id="43884-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="43884-127">Bekijk de drempellimiet die is gedefinieerd voor de TDS-belastingcomponent die aan een specifieke TDS-belastingcode is gekoppeld op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="43884-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="43884-128">Selecteer **Formuleontwerper** om de pagina **Formuleontwerper** te openen.</span><span class="sxs-lookup"><span data-stu-id="43884-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="43884-129">Bekijk de formule die is gedefinieerd voor een specifieke TDS-belastingcode op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="43884-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="43884-130">Boek de factuur.</span><span class="sxs-lookup"><span data-stu-id="43884-130">Post the invoice.</span></span> <span data-ttu-id="43884-131">Het TDS-bedrag dat op inkoopfacturen is berekend, wordt naar de leveranciersrekening geboekt en het TDS-bedrag dat op verkoopfacturen is berekend, wordt geboekt naar de klantrekening die voor elke TDS-belastingcode in de TDS-groep is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="43884-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="43884-132">De leveranciers- of klantrekeningen voor TDS-belastingcodes worden gedefinieerd op de pagina **Bronbelastingcodes**.</span><span class="sxs-lookup"><span data-stu-id="43884-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="43884-133">Selecteer de **Opvraag**-knop **> Factuur > Geboekt met bronbelasting**-knop om de pagina **Bronbelastingtransacties** te openen.</span><span class="sxs-lookup"><span data-stu-id="43884-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="43884-134">U kunt in het veld **Waarde** het totale percentage weergeven dat is gebruikt om TDS voor de transactie te berekenen.</span><span class="sxs-lookup"><span data-stu-id="43884-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="43884-135">In de velden op de tabbladen **Overzicht**, **Algemeen** en **Bedrag** op de pagina **Bronbelastingtransacties** wordt de informatie weergegeven van TDS-gegevens die voor de transactie zijn berekend.</span><span class="sxs-lookup"><span data-stu-id="43884-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="43884-136">Bekijk de TDS-berekeningsgegevens voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="43884-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
