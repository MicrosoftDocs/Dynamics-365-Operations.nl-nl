---
title: Transacties detailhandelwinkel bewerken en controleren
description: In dit onderwerp wordt de functionaliteit beschreven voor het bewerken en controleren van winkeltransacties.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
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
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004384"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="9245f-103">Transacties detailhandelwinkel bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="9245f-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="9245f-104">Dynamics 365 Commerce-klanten gebruiken POS-toepassingen (Point of Sale) van dezelfde en andere leveranciers.</span><span class="sxs-lookup"><span data-stu-id="9245f-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="9245f-105">Met de POS-toepassing van dezelfde leverancier worden winkeltransacties uit de kanalen binnengehaald in Headquarters via een batchproces.</span><span class="sxs-lookup"><span data-stu-id="9245f-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="9245f-106">Met toepassingen van derden worden transacties binnengehaald in Headquarters via integratie.</span><span class="sxs-lookup"><span data-stu-id="9245f-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="9245f-107">In beide gevallen moet er nadat transacties zijn binnengehaald in Headquarters, een consistentiecontrole met meerdere validaties op de transacties worden uitgevoerd, zodat het overzicht dat in Headquarters wordt geboekt alleen gevalideerde transacties bevat.</span><span class="sxs-lookup"><span data-stu-id="9245f-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="9245f-108">De validatie van transacties in Commerce kan om verschillende redenen mislukken.</span><span class="sxs-lookup"><span data-stu-id="9245f-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="9245f-109">Een fout in de integratiecode of een fout in de POS-toepassing kan bijvoorbeeld leiden tot inconsistente gegevens. En een gebruikersfout, zoals het verwijderen van een product nadat het is gesynchroniseerd met het kanaal of het afsluiten van een boekperiode zonder dat er transacties voor deze periode worden geboekt, kan inconsistente gegevens veroorzaken.</span><span class="sxs-lookup"><span data-stu-id="9245f-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="9245f-110">Deze transacties worden gemarkeerd en niet opgenomen in de overzichten, maar kunnen het dagelijkse proces verstoren van het boeken van de dagelijkse verkopen naar de financiële gegevens.</span><span class="sxs-lookup"><span data-stu-id="9245f-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="9245f-111">In Commerce kunt u de specifieke detailhandeltransacties die niet worden gevalideerd, bewerken tijdens het controleren van alle wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="9245f-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="9245f-112">Transacties bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="9245f-112">Edit and audit transactions</span></span>

<span data-ttu-id="9245f-113">In Retail versie 10.0.5 zijn contante transacties zoals verkopen en retouren, de enige transacties die kunnen worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="9245f-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="9245f-114">Het bewerken van klantorders of online orders wordt niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="9245f-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="9245f-115">In Retail versie 10.0.6 en hoger wordt het bewerken van beheertransacties voor contanten ook ondersteund.</span><span class="sxs-lookup"><span data-stu-id="9245f-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="9245f-116">Installeer de Dynamics Excel-invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="9245f-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="9245f-117">Ga naar het werkgebied **Financiën van winkel**.</span><span class="sxs-lookup"><span data-stu-id="9245f-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="9245f-118">De tegel **Mislukte transactievalidaties** biedt een vooraf gefilterde weergave van het formulier met de transactie die niet is geslaagd voor een of meer validatieregels.</span><span class="sxs-lookup"><span data-stu-id="9245f-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="9245f-119">Open het formulier.</span><span class="sxs-lookup"><span data-stu-id="9245f-119">Open the form.</span></span> <span data-ttu-id="9245f-120">Klik op de record waarvoor de validatie is mislukt. Klik op **Office-invoegtoepassing** en klik vervolgens op **Geselecteerde transactie bewerken**.</span><span class="sxs-lookup"><span data-stu-id="9245f-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="9245f-121">Een Excel-bestand met de details van de geselecteerde transactie wordt geopend met de volgende werkbladen:</span><span class="sxs-lookup"><span data-stu-id="9245f-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="9245f-122">Regels: dit werkblad bevat de koptekst- en productregels en gerelateerde gegevens voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="9245f-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="9245f-123">Betalingen: dit werkblad bevat de details van de betalingsregels voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="9245f-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="9245f-124">Kortingen: dit werkblad bevat de details over de kortingen voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="9245f-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="9245f-125">Belastingen: dit werkblad bevat de details over de belastingen voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="9245f-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="9245f-126">Toeslagen: dit werkblad bevat de gegevens over de toeslagen voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="9245f-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="9245f-127">In het Excel-bestand wijzigt u de betreffende velden en uploadt u de gegevens weer naar Headquarters met de publicatiefunctionaliteit van de Dynamics Excel-invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="9245f-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="9245f-128">Na de publicatie worden de wijzigingen weergegeven in het systeem.</span><span class="sxs-lookup"><span data-stu-id="9245f-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="9245f-129">Tijdens het publiceren worden er geen validaties uitgevoerd voor wijzigingen door gebruikers.</span><span class="sxs-lookup"><span data-stu-id="9245f-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="9245f-130">U kunt een volledig controlespoor van de wijzigingen bekijken door te klikken op **Audittrail weergeven** in de koptekst **Detailhandelstransactie** voor wijzigingen op koptekstniveau en in de relevante sectie en record op de desbetreffende transactiepagina.</span><span class="sxs-lookup"><span data-stu-id="9245f-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="9245f-131">Alle wijzigingen met betrekking tot verkoopregels worden bijvoorbeeld weergegeven op de pagina **Verkooptransacties**, wijzigingen met betrekking tot betalingen worden weergegeven op de pagina **Betalingstransacties**, enzovoort. De volgende controledetails worden bijgehouden voor de wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="9245f-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="9245f-132">Wijzigingsdatum en -tijd</span><span class="sxs-lookup"><span data-stu-id="9245f-132">Modified date and time</span></span>
   - <span data-ttu-id="9245f-133">Veld</span><span class="sxs-lookup"><span data-stu-id="9245f-133">Field</span></span> 
   - <span data-ttu-id="9245f-134">Oude waarde</span><span class="sxs-lookup"><span data-stu-id="9245f-134">Old value</span></span>
   - <span data-ttu-id="9245f-135">Nieuwe waarde</span><span class="sxs-lookup"><span data-stu-id="9245f-135">New value</span></span>
   - <span data-ttu-id="9245f-136">Gewijzigd door</span><span class="sxs-lookup"><span data-stu-id="9245f-136">Modified by</span></span>

6. <span data-ttu-id="9245f-137">Nadat de wijzigingen zijn aangebracht en gepubliceerd, voert u de optie **Winkeltransacties valideren** opnieuw uit om te controleren of de aangebrachte wijzigingen consistent en geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="9245f-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="9245f-138">U kunt alleen transacties bewerken waarvoor de validatie is mislukt.</span><span class="sxs-lookup"><span data-stu-id="9245f-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="9245f-139">Als u transacties wilt bewerken die zijn gevalideerd, wijzigt u de validatiestatus van de transactie die u wilt wijzigen in **Fout** of **Geen**. Vervolgens kunt u deze bewerken.</span><span class="sxs-lookup"><span data-stu-id="9245f-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="9245f-140">Bulksgewijs bewerken van transacties</span><span class="sxs-lookup"><span data-stu-id="9245f-140">Bulk edit transactions</span></span>

<span data-ttu-id="9245f-141">In Retail versie 10.0.6 en hoger wordt de optie voor het bulksgewijs bewerken van transacties op overzichtsniveau ondersteund.</span><span class="sxs-lookup"><span data-stu-id="9245f-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="9245f-142">Gebruik de invoegtoepassing Excel om een overzicht te openen met transacties die u wilt wijzigen met behulp van stap 1-3 hierboven.</span><span class="sxs-lookup"><span data-stu-id="9245f-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="9245f-143">Kies een van de onderstaande opties.</span><span class="sxs-lookup"><span data-stu-id="9245f-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="9245f-144">**Contante transacties bewerken**.</span><span class="sxs-lookup"><span data-stu-id="9245f-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="9245f-145">Met deze optie kunt u alle contante transacties bewerken die in het overzicht zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="9245f-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="9245f-146">De volgende Excel-werkbladen zijn beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="9245f-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="9245f-147">**Transactie**: dit werkblad bevat alle informatie op koptekstniveau voor de verkooptransacties.</span><span class="sxs-lookup"><span data-stu-id="9245f-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="9245f-148">**Verkooptransactie**: dit werkblad bevat alle informatie op regelniveau voor de verkooptransacties.</span><span class="sxs-lookup"><span data-stu-id="9245f-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="9245f-149">**Betalingstransacties**: dit werkblad bevat alle informatie over betalingsregels voor de verkooptransacties.</span><span class="sxs-lookup"><span data-stu-id="9245f-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="9245f-150">**Kortingstransacties**: dit werkblad bevat alle informatie over kortingsregels voor de verkooptransacties.</span><span class="sxs-lookup"><span data-stu-id="9245f-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="9245f-151">**Belastingtransacties**: dit werkblad bevat alle informatie over belastingregels voor de verkooptransacties.</span><span class="sxs-lookup"><span data-stu-id="9245f-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="9245f-152">**Toeslagtransacties**: dit werkblad bevat alle informatie over toeslagregels voor de verkooptransacties.</span><span class="sxs-lookup"><span data-stu-id="9245f-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="9245f-153">**Transacties voor beheer van contant geld bewerken**.</span><span class="sxs-lookup"><span data-stu-id="9245f-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="9245f-154">Met deze optie kunt u alle beheertransacties voor contant geld bewerken die in het overzicht zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="9245f-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="9245f-155">De volgende Excel-werkbladen zijn beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="9245f-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="9245f-156">**Transactie**: dit werkblad bevat alle informatie op het koptekstniveau voor de beheertransacties van contant geld.</span><span class="sxs-lookup"><span data-stu-id="9245f-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="9245f-157">**Banktransacties betalingsmethode**: dit werkblad bevat alle transactiedetails voor bankstortingen.</span><span class="sxs-lookup"><span data-stu-id="9245f-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="9245f-158">**Kluistransacties betalingsmethode**: dit werkblad bevat alle transactiedetails voor kluisstortingen.</span><span class="sxs-lookup"><span data-stu-id="9245f-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="9245f-159">**Kascontrole**: dit werkblad bevat alle transactiedetails voor kascontroles.</span><span class="sxs-lookup"><span data-stu-id="9245f-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="9245f-160">**Inkomsten-/uitgaventransacties**: dit werkblad bevat alle details van de transactieregels voor inkomsten en uitgaven.</span><span class="sxs-lookup"><span data-stu-id="9245f-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="9245f-161">**Betalingstransacties**: dit werkblad bevat alle betalingsgerelateerde informatie voor de bewerking **Factuur betalen** en over inkomsten-/uitgaventransacties.</span><span class="sxs-lookup"><span data-stu-id="9245f-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="9245f-162">Er worden geen validaties uitgevoerd wanneer u in bulk bewerkte transacties publiceert.</span><span class="sxs-lookup"><span data-stu-id="9245f-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="9245f-163">U moet ervoor zorgen dat alle bewerkingen juist zijn en dat de betrouwbaarheid van de gegevens in de werkbladen behouden blijft.</span><span class="sxs-lookup"><span data-stu-id="9245f-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="9245f-164">Als u bijvoorbeeld de transactiedatum wilt wijzigen voor scenario's waarin de fiscale of voorraadperiode voor de openstaande transacties wordt gesloten, moet u de datum wijzigen in alle Excel-werkbladen die de kolom **Werkdatum** bevatten.</span><span class="sxs-lookup"><span data-stu-id="9245f-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="9245f-165">Als u transacties wilt valideren nadat deze zijn bewerkt, gebruikt u **Transacties opnieuw valideren** op de pagina **Overzichten**.</span><span class="sxs-lookup"><span data-stu-id="9245f-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>