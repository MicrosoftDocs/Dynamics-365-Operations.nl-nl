---
title: TDS op facturen berekenen met behulp van journalen
description: Dit onderwerp geeft een overzicht van de stappen voor het berekenen van TDS (belasting ingehouden op bron) op verschillende typen facturen.journalen.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023162"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="358b8-103">TDS op facturen berekenen met behulp van journalen</span><span class="sxs-lookup"><span data-stu-id="358b8-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="358b8-104">Dit onderwerp geeft een overzicht van de stappen voor het berekenen van TDS (belasting ingehouden op bron) op verschillende typen facturen.journalen.</span><span class="sxs-lookup"><span data-stu-id="358b8-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="358b8-105">Open om te beginnen de pagina **Algemene journalen** (**Grootboek > Journaalboekingen > Algemene journalen**).</span><span class="sxs-lookup"><span data-stu-id="358b8-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="358b8-106">[![Algemene journalen](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="358b8-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="358b8-107">Maak journaalregels met de journaalformulieren die in de tabel staan.</span><span class="sxs-lookup"><span data-stu-id="358b8-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="358b8-108">Selecteer het rekeningtype en het tegenrekeningtype en voer het bedrag voor de transactie in.</span><span class="sxs-lookup"><span data-stu-id="358b8-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="358b8-109">Op de pagina **Factuurgoedkeuringsjournaal** selecteert u **Boekstukken zoeken** en selecteert u facturen waarop u TDS wilt berekenen.</span><span class="sxs-lookup"><span data-stu-id="358b8-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="358b8-110">Bekijk de facturen die zijn gemaakt op de pagina **Facturenregister** of de pagina **Boekstukken zoeken**.</span><span class="sxs-lookup"><span data-stu-id="358b8-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="358b8-111">Bekijk of wijzig op het tabblad **Algemeen** van de pagina **Journaalboekstuk** in het veld **TDS-groep** de standaard-TDS-groep die voor de leverancier of klant is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="358b8-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="358b8-112">Het TDS-bedrag dat op journaalregels wordt berekend, is gebaseerd op de formule die is gedefinieerd voor de TDS-belastingcodes in het veld **TDS-groep**.</span><span class="sxs-lookup"><span data-stu-id="358b8-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="358b8-113">Wanneer u een TDS-groep selecteert in het veld **TDS-groep**, zijn de velden **Bronbelastinggroep** en **TCS-groep** niet meer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="358b8-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="358b8-114">Het veld **Bronbelastinggroep** is alleen beschikbaar op de pagina **Algemeen journaal**.</span><span class="sxs-lookup"><span data-stu-id="358b8-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="358b8-115">TDS wordt alleen berekend als het selectievakje **Bronbelasting berekenen** is ingeschakeld voor de leverancier of klant op de pagina **Alle leveranciers** of de pagina **Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="358b8-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="358b8-116">Selecteer het tabblad **Belastinggegevens**. Selecteer de alternatieve adressen van een bedrijf die zijn ingesteld voor het bedrijf in dit veld, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="358b8-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="358b8-117">U kunt de bedrijfsnaam bekijken in het veld **Naam**, dat onder de veldgroep **Bedrijfsgegevens** valt.</span><span class="sxs-lookup"><span data-stu-id="358b8-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="358b8-118">Bekijk de soort belastingplichtige waar de leverancier of klant toe hoort in het veld **Soort belastingplichtige** dat onder de veldgroep **Bronbelasting** valt.</span><span class="sxs-lookup"><span data-stu-id="358b8-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="358b8-119">In het veld **Belastingrekeningnummer** (**TAN**) kunt u de TAN van de geselecteerde bedrijfsnaam weergeven die wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="358b8-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="358b8-120">Selecteer **Bronbelasting** in het menu **Bronbelasting** om de pagina **Tijdelijke bronbelastingtransacties** te openen.</span><span class="sxs-lookup"><span data-stu-id="358b8-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="358b8-121">De volgende velden worden weergegeven in het bovenste deelvenster van de pagina **Tijdelijke bronbelastingtransacties**.</span><span class="sxs-lookup"><span data-stu-id="358b8-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="358b8-122">**Totaalbedrag bronbelasting**: het totale TDS-bedrag dat voor de transactie voor de TDS-groep is berekend.</span><span class="sxs-lookup"><span data-stu-id="358b8-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="358b8-123">**Waarde**: het totale percentage dat is gebruikt om TDS voor de transactie te berekenen.</span><span class="sxs-lookup"><span data-stu-id="358b8-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="358b8-124">Het totale percentage is gebaseerd op de formule die is gedefinieerd voor TDS-belastingcodes gekoppeld aan de TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="358b8-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="358b8-125">**Totaal gecorrigeerd bronbelastingbedrag**: het totale gecorrigeerde TDS-bedrag voor alle belastingcodes in de TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="358b8-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="358b8-126">**TDS**: als deze optie is geselecteerd, is er een TDS-groep aan de transactie gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="358b8-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="358b8-127">De velden op de tabbladen **Overzicht**, **Algemeen** en **Correctie** op de pagina **Tijdelijke bronbelastingtransacties** geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="358b8-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="358b8-128">Selecteer **Drempel** om de pagina **Drempel** te openen.</span><span class="sxs-lookup"><span data-stu-id="358b8-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="358b8-129">Bekijk de drempellimiet en uitzonderingsdrempellimiet die is gedefinieerd voor de TDS-belastingcomponent die aan een specifieke TDS-belastingcode is gekoppeld op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="358b8-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="358b8-130">Selecteer **Formuleontwerper** om het formulier **Formuleontwerper** te openen.</span><span class="sxs-lookup"><span data-stu-id="358b8-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="358b8-131">Bekijk de formule die is gedefinieerd voor een specifieke TDS-belastingcode in deze pagina.</span><span class="sxs-lookup"><span data-stu-id="358b8-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="358b8-132">Sluit de pagina's **Formuleontwerper** en **Tijdelijke bronbelastingtransacties** om terug te keren naar de pagina **Journaalboekstuk**.</span><span class="sxs-lookup"><span data-stu-id="358b8-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="358b8-133">Voer de andere vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="358b8-133">Enter the other required details.</span></span> <span data-ttu-id="358b8-134">Valideer en boek het journaal.</span><span class="sxs-lookup"><span data-stu-id="358b8-134">Validate and post the journal.</span></span> <span data-ttu-id="358b8-135">Het TDS-bedrag dat op inkoopfacturen is berekend, wordt naar de leveranciersrekening geboekt.</span><span class="sxs-lookup"><span data-stu-id="358b8-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="358b8-136">Het TDS-bedrag dat is berekend op verkoopfacturen wordt geboekt naar de klantrekening die is gedefinieerd voor elke TDS-belastingcode in de TDS-groep.</span><span class="sxs-lookup"><span data-stu-id="358b8-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="358b8-137">De leveranciers- of klantrekeningen voor TDS-belastingcodes worden gedefinieerd op de pagina **Bronbelastingcodes**.</span><span class="sxs-lookup"><span data-stu-id="358b8-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="358b8-138">Selecteer **Bronbelasting geboekt** om de pagina **Bronbelastingtransacties** te openen.</span><span class="sxs-lookup"><span data-stu-id="358b8-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="358b8-139">In het veld **Waarde** wordt het totale percentage weergegeven dat is gebruikt om TDS voor de transactie te berekenen.</span><span class="sxs-lookup"><span data-stu-id="358b8-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="358b8-140">De velden op de tabbladen **Overzicht**, **Algemeen** en **Bedrag** op de pagina Tijdelijke bronbelastingtransacties geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="358b8-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
