---
title: Sjabloon voor vrije-tekstfacturen toewijzen aan een klant
description: Deze taak geeft aan hoe u een sjabloon voor een vrije-tekstfactuur kunt toewijzen aan een klant.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9535a4678ea0c68227a54cf3c5d1b06b116a288
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916341"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="ee8c5-103">Sjabloon voor vrije-tekstfacturen toewijzen aan een klant</span><span class="sxs-lookup"><span data-stu-id="ee8c5-103">Assign free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee8c5-104">Deze taak geeft aan hoe u een sjabloon voor een vrije-tekstfactuur kunt toewijzen aan een klant.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="ee8c5-105">Deze taak gebruikt het demobedrijf USMF en is bedoeld voor de gebruiker die verantwoordelijk is voor het beheren en verwerken van klantenfacturen.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="ee8c5-106">Ga in het **navigatiedeelvenster** naar **Modules > Klanten > Klanten > Alle klanten.**</span><span class="sxs-lookup"><span data-stu-id="ee8c5-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="ee8c5-107">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ee8c5-108">Klik in het **actievenster** op **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="ee8c5-109">Klik op **Terugkerende facturen**.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="ee8c5-110">Gebruik deze pagina om sjablonen voor vrije-tekstfacturen toe te wijzen aan klanten en op te geven hoe vaak facturen moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="ee8c5-111">Klik op **Nieuw** om een nieuwe sjabloon toe te wijzen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="ee8c5-112">Selecteer in het veld **Sjabloon** de sjabloon voor vrije-tekstfacturen die u wilt toewijzen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="ee8c5-113">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ee8c5-114">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ee8c5-115">Voer in het veld **Begindatum facturering** de datum in waarop de eerste factuur wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="ee8c5-116">Voer in de sectie **Einde terugkeerpatroon** een terugkerende einddatum in.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="ee8c5-117">Selecteer een van de volgende: Geen einddatum: er worden voor onbepaalde tijd facturen gegenereerd totdat de sjabloon wordt verwijderd van de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="ee8c5-118">Einddatum facturering: selecteer deze optie en voor de laatste datum in waarop de factor kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="ee8c5-119">Voer in het veld **Maximum cumulatief bedrag** het maximale cumulatieve bedrag in waarna het genereren van facturen wordt gestopt.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-119">In the **Maximum cummulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="ee8c5-120">Het maximale cumulatieve bedrag invoeren dat kan worden gefactureerd op basis van de geselecteerde sjabloon.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="ee8c5-121">Als u bijvoorbeeld 1000.00 invoert en maandelijkse facturen genereert voor 100,00, stopt het genereren van facturen na de tiende factuur.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="ee8c5-122">Selecteer in de sectie **Terugkerende facturen genereren door de standaardwaarden te gebruiken uit** de sjabloon voor vrije-tekstfacturen of de klantrekening.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="ee8c5-123">Opgeven of de sjabloon voor vrije-tekstfacturen of de klantrekening moet worden gebruikt om de standaardwaarden te bepalen voor taal, boekingsprofiel, btw-groep, btw-groep voor artikelen, lijstcode, land/regio voor levering, valuta, betalingsvoorwaarden, betalingsmethode, betalingsspecificatie, betalingsschema, contantkorting, financiële dimensies en giro-overboekingsstrook bij het maken van facturen.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="ee8c5-124">Selecteer het terugkeerpatroon in het veld **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="ee8c5-125">Dagelijks: selecteer deze optie en geef het aantal dagen op in het veld Per.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="ee8c5-126">Als u bijvoorbeeld 15 invoert, wordt elke vijftien dagen een factuur gegenereerd voor deze klant.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="ee8c5-127">Wekelijks: selecteer deze optie en geef het aantal weken op in het veld Per.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="ee8c5-128">Als u bijvoorbeeld 2 invoert, wordt elke twee weken een factuur gegenereerd voor deze klant.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="ee8c5-129">Maandelijks: selecteer deze optie en geef het aantal maanden op in het veld Per.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="ee8c5-130">Als u bijvoorbeeld 6 invoert, wordt elke zes maanden een factuur gegenereerd voor deze klant.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="ee8c5-131">Jaar: selecteer deze optie en geef het aantal jaren op in het veld Per.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="ee8c5-132">Als u bijvoorbeeld 2 invoert, wordt elke twee jaar een factuur gegenereerd voor deze klant.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="ee8c5-133">Voer een getal in het veld **Per** in.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-133">In the **Per** field, enter a number.</span></span>

