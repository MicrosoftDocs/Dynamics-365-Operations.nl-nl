---
title: De toewijzing instellen voor de verkooporderstatuskolommen
description: In dit onderwerp wordt uitgelegd hoe u de statuskolommen voor verkooporders instelt voor twee keer wegschrijven.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750709"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="e56d0-103">De toewijzing instellen voor de verkooporderstatuskolommen</span><span class="sxs-lookup"><span data-stu-id="e56d0-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e56d0-104">De kolommen die de status van de verkooporder aangeven, hebben verschillende opsommingswaarden in Microsoft Dynamics 365 Supply Chain Management en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e56d0-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="e56d0-105">Aanvullende instellingen zijn vereist om deze kolommen te kunnen koppelen in twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="e56d0-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="e56d0-106">kolommen in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e56d0-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="e56d0-107">In Supply Chain Management geven twee kolommen de status van de verkooporder weer.</span><span class="sxs-lookup"><span data-stu-id="e56d0-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="e56d0-108">De kolommen die u moet toewijzen zijn **Status** en **Documentstatus**.</span><span class="sxs-lookup"><span data-stu-id="e56d0-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="e56d0-109">De opsommingswaarde **Status** geeft de algemene status van de order aan.</span><span class="sxs-lookup"><span data-stu-id="e56d0-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="e56d0-110">Deze status wordt weergegeven in de orderkop.</span><span class="sxs-lookup"><span data-stu-id="e56d0-110">This status is shown on the order header.</span></span>

<span data-ttu-id="e56d0-111">De opsommingswaarde **Status** heeft de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="e56d0-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="e56d0-112">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-112">Open Order</span></span>
- <span data-ttu-id="e56d0-113">Geleverd</span><span class="sxs-lookup"><span data-stu-id="e56d0-113">Delivered</span></span>
- <span data-ttu-id="e56d0-114">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-114">Invoiced</span></span>
- <span data-ttu-id="e56d0-115">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-115">Cancelled</span></span>

<span data-ttu-id="e56d0-116">De opsommingswaarde **Documentstatus** geeft het meest recente document aan dat voor de order is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e56d0-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="e56d0-117">Als de order bijvoorbeeld is bevestigd, is dit document een verkooporderbevestiging.</span><span class="sxs-lookup"><span data-stu-id="e56d0-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="e56d0-118">Als een verkooporder gedeeltelijk is gefactureerd en de resterende regel is bevestigd, behoudt het document de status **Factuur** omdat de factuur later in het proces wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e56d0-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="e56d0-119">De opsommingswaarde **Documentstatus** heeft de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="e56d0-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="e56d0-120">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="e56d0-120">Confirmation</span></span>
- <span data-ttu-id="e56d0-121">Orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="e56d0-121">Picking List</span></span>
- <span data-ttu-id="e56d0-122">Pakbon</span><span class="sxs-lookup"><span data-stu-id="e56d0-122">Packing Slip</span></span>
- <span data-ttu-id="e56d0-123">Factuur</span><span class="sxs-lookup"><span data-stu-id="e56d0-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="e56d0-124">kolommen in Sales</span><span class="sxs-lookup"><span data-stu-id="e56d0-124">columns in Sales</span></span>

<span data-ttu-id="e56d0-125">In Sales geven twee kolommen de status van de order weer.</span><span class="sxs-lookup"><span data-stu-id="e56d0-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="e56d0-126">De kolommen die u moet toewijzen zijn **Status** en **Verwerkingsstatus**.</span><span class="sxs-lookup"><span data-stu-id="e56d0-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="e56d0-127">De opsommingswaarde **Status** geeft de algemene status van de order aan.</span><span class="sxs-lookup"><span data-stu-id="e56d0-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="e56d0-128">Het heeft de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="e56d0-128">It has the following values:</span></span>

- <span data-ttu-id="e56d0-129">Actief</span><span class="sxs-lookup"><span data-stu-id="e56d0-129">Active</span></span>
- <span data-ttu-id="e56d0-130">Ingediend</span><span class="sxs-lookup"><span data-stu-id="e56d0-130">Submitted</span></span>
- <span data-ttu-id="e56d0-131">Afgehandeld</span><span class="sxs-lookup"><span data-stu-id="e56d0-131">Fulfilled</span></span>
- <span data-ttu-id="e56d0-132">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-132">Invoiced</span></span>
- <span data-ttu-id="e56d0-133">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-133">Cancelled</span></span>

<span data-ttu-id="e56d0-134">De opsommingswaarde **Verwerkingsstatus** is geïntroduceerd zodat de status nauwkeuriger kan worden toegewezen met Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e56d0-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="e56d0-135">In de volgende tabel wordt de toewijzing van **Verwerkingsstatus** in Supply Chain Management weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e56d0-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="e56d0-136">Verwerkingsstatus</span><span class="sxs-lookup"><span data-stu-id="e56d0-136">Processing Status</span></span>   | <span data-ttu-id="e56d0-137">Status in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e56d0-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="e56d0-138">Documentstatus in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e56d0-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="e56d0-139">Actief</span><span class="sxs-lookup"><span data-stu-id="e56d0-139">Active</span></span>              | <span data-ttu-id="e56d0-140">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-140">Open Order</span></span>                        | <span data-ttu-id="e56d0-141">None</span><span class="sxs-lookup"><span data-stu-id="e56d0-141">None</span></span>                                       |
| <span data-ttu-id="e56d0-142">Bevestigd</span><span class="sxs-lookup"><span data-stu-id="e56d0-142">Confirmed</span></span>           | <span data-ttu-id="e56d0-143">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-143">Open Order</span></span>                        | <span data-ttu-id="e56d0-144">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="e56d0-144">Confirmation</span></span>                               |
| <span data-ttu-id="e56d0-145">Opgenomen</span><span class="sxs-lookup"><span data-stu-id="e56d0-145">Picked</span></span>              | <span data-ttu-id="e56d0-146">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-146">Open Order</span></span>                        | <span data-ttu-id="e56d0-147">Orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="e56d0-147">Picking List</span></span>                               |
| <span data-ttu-id="e56d0-148">Gedeeltelijk geleverd</span><span class="sxs-lookup"><span data-stu-id="e56d0-148">Partially Delivered</span></span> | <span data-ttu-id="e56d0-149">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-149">Open Order</span></span>                        | <span data-ttu-id="e56d0-150">Pakbon</span><span class="sxs-lookup"><span data-stu-id="e56d0-150">Packing Slip</span></span>                               |
| <span data-ttu-id="e56d0-151">Geleverd</span><span class="sxs-lookup"><span data-stu-id="e56d0-151">Delivered</span></span>           | <span data-ttu-id="e56d0-152">Geleverd</span><span class="sxs-lookup"><span data-stu-id="e56d0-152">Delivered</span></span>                         | <span data-ttu-id="e56d0-153">Pakbon</span><span class="sxs-lookup"><span data-stu-id="e56d0-153">Packing Slip</span></span>                               |
| <span data-ttu-id="e56d0-154">Gedeeltelijk gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-154">Partially Invoiced</span></span>  | <span data-ttu-id="e56d0-155">Geleverd</span><span class="sxs-lookup"><span data-stu-id="e56d0-155">Delivered</span></span>                         | <span data-ttu-id="e56d0-156">Factuur</span><span class="sxs-lookup"><span data-stu-id="e56d0-156">Invoice</span></span>                                    |
| <span data-ttu-id="e56d0-157">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-157">Invoiced</span></span>            | <span data-ttu-id="e56d0-158">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-158">Invoiced</span></span>                          | <span data-ttu-id="e56d0-159">Factuur</span><span class="sxs-lookup"><span data-stu-id="e56d0-159">Invoice</span></span>                                    |
| <span data-ttu-id="e56d0-160">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-160">Cancelled</span></span>           | <span data-ttu-id="e56d0-161">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-161">Cancelled</span></span>                         | <span data-ttu-id="e56d0-162">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="e56d0-162">Not applicable</span></span>                             |

<span data-ttu-id="e56d0-163">In de volgende tabel wordt de toewijzing van **Verwerkingsstatus** tussen Verkoop en Supply Chain Management weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e56d0-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="e56d0-164">Verwerkingsstatus</span><span class="sxs-lookup"><span data-stu-id="e56d0-164">Processing Status</span></span>   | <span data-ttu-id="e56d0-165">Status in Verkoop</span><span class="sxs-lookup"><span data-stu-id="e56d0-165">Status in Sales</span></span> | <span data-ttu-id="e56d0-166">Status in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e56d0-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="e56d0-167">Actief</span><span class="sxs-lookup"><span data-stu-id="e56d0-167">Active</span></span>              | <span data-ttu-id="e56d0-168">Actief</span><span class="sxs-lookup"><span data-stu-id="e56d0-168">Active</span></span>          | <span data-ttu-id="e56d0-169">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-169">Open Order</span></span>                        |
| <span data-ttu-id="e56d0-170">Bevestigd</span><span class="sxs-lookup"><span data-stu-id="e56d0-170">Confirmed</span></span>           | <span data-ttu-id="e56d0-171">Ingediend</span><span class="sxs-lookup"><span data-stu-id="e56d0-171">Submitted</span></span>       | <span data-ttu-id="e56d0-172">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-172">Open Order</span></span>                        |
| <span data-ttu-id="e56d0-173">Opgenomen</span><span class="sxs-lookup"><span data-stu-id="e56d0-173">Picked</span></span>              | <span data-ttu-id="e56d0-174">Ingediend</span><span class="sxs-lookup"><span data-stu-id="e56d0-174">Submitted</span></span>       | <span data-ttu-id="e56d0-175">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-175">Open Order</span></span>                        |
| <span data-ttu-id="e56d0-176">Gedeeltelijk geleverd</span><span class="sxs-lookup"><span data-stu-id="e56d0-176">Partially Delivered</span></span> | <span data-ttu-id="e56d0-177">Actief</span><span class="sxs-lookup"><span data-stu-id="e56d0-177">Active</span></span>          | <span data-ttu-id="e56d0-178">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-178">Open Order</span></span>                        |
| <span data-ttu-id="e56d0-179">Gedeeltelijk gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-179">Partially Invoiced</span></span>  | <span data-ttu-id="e56d0-180">Actief</span><span class="sxs-lookup"><span data-stu-id="e56d0-180">Active</span></span>          | <span data-ttu-id="e56d0-181">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="e56d0-181">Open Order</span></span>                        |
| <span data-ttu-id="e56d0-182">Gedeeltelijk gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-182">Partially Invoiced</span></span>  | <span data-ttu-id="e56d0-183">Afgehandeld</span><span class="sxs-lookup"><span data-stu-id="e56d0-183">Fulfilled</span></span>       | <span data-ttu-id="e56d0-184">Geleverd</span><span class="sxs-lookup"><span data-stu-id="e56d0-184">Delivered</span></span>                         |
| <span data-ttu-id="e56d0-185">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-185">Invoiced</span></span>            | <span data-ttu-id="e56d0-186">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-186">Invoiced</span></span>        | <span data-ttu-id="e56d0-187">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-187">Invoiced</span></span>                          |
| <span data-ttu-id="e56d0-188">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-188">Cancelled</span></span>           | <span data-ttu-id="e56d0-189">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-189">Cancelled</span></span>       | <span data-ttu-id="e56d0-190">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="e56d0-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="e56d0-191">Instelling</span><span class="sxs-lookup"><span data-stu-id="e56d0-191">Setup</span></span>

<span data-ttu-id="e56d0-192">Om de toewijzing voor de statuskolommen van verkooporders in te stellen, moet u de kenmerken **IsSOPIntegrationEnabled** en **isIntegrationUser** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="e56d0-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="e56d0-193">Volg deze stappen als u het kenmerk **IsSOPIntegrationEnabled** wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="e56d0-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="e56d0-194">Ga in een browser naar `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="e56d0-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="e56d0-195">Vervang **\<test-name\>** door de koppeling van uw bedrijf met Verkoop.</span><span class="sxs-lookup"><span data-stu-id="e56d0-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="e56d0-196">Zoek **organizationid** op de pagina die is geopend en noteer de waarde.</span><span class="sxs-lookup"><span data-stu-id="e56d0-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizationid zoeken](media/sales-map-orgid.png)

3. <span data-ttu-id="e56d0-198">Open de browserconsole in Verkoop en voer het volgende script uit.</span><span class="sxs-lookup"><span data-stu-id="e56d0-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="e56d0-199">Gebruik de waarde van **organizationid** uit stap 2.</span><span class="sxs-lookup"><span data-stu-id="e56d0-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-code in de browserconsole](media/sales-map-script.png)

4. <span data-ttu-id="e56d0-201">Controleer of **IsSOPIntegrationEnabled** is ingesteld op **true**.</span><span class="sxs-lookup"><span data-stu-id="e56d0-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="e56d0-202">Gebruik de URL uit stap 1 om de waarde te controleren.</span><span class="sxs-lookup"><span data-stu-id="e56d0-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled ingesteld op true](media/sales-map-integration-enabled.png)

<span data-ttu-id="e56d0-204">Volg deze stappen als u het kenmerk **isIntegrationUser** wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="e56d0-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="e56d0-205">Ga in Sales naar **Instelling \> Aanpassing \> Het systeem aanpassen**. Selecteer **Gebruikerstabel** en open **Formulier \> Gebruiker**.</span><span class="sxs-lookup"><span data-stu-id="e56d0-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Het gebruikersformulier openen](media/sales-map-user.png)

2. <span data-ttu-id="e56d0-207">Zoek in Veldverkenner **Integratiegebruikersmodus** en dubbelklik erop om deze toe te voegen aan het formulier.</span><span class="sxs-lookup"><span data-stu-id="e56d0-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="e56d0-208">Sla de wijziging op.</span><span class="sxs-lookup"><span data-stu-id="e56d0-208">Save your change.</span></span>

    ![De kolom Integratiegebruikersmodus toevoegen aan het formulier](media/sales-map-field-explorer.png)

3. <span data-ttu-id="e56d0-210">Ga in Verkoop naar **Instelling \> Beveiliging \> Gebruikers** en wijzig de weergave van **Ingeschakelde gebruikers** in **Toepassingsgebruikers**.</span><span class="sxs-lookup"><span data-stu-id="e56d0-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![De weergave wijzigen van Ingeschakelde gebruikers in Toepassingsgebruikers](media/sales-map-enabled-users.png)

4. <span data-ttu-id="e56d0-212">Selecteer de twee items voor **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="e56d0-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Lijst met toepassingsgebruikers](media/sales-map-user-mode.png)

5. <span data-ttu-id="e56d0-214">Wijzig de waarde van de kolom **Integratiegebruikersmodus** in **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e56d0-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![De waarde van de kolom Integratiegebruikersmodus wijzigen in Ja](media/sales-map-user-mode-yes.png)

<span data-ttu-id="e56d0-216">Uw verkooporders zijn nu toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e56d0-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]