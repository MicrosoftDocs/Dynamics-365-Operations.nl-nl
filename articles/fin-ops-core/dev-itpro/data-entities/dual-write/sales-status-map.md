---
title: De toewijzing voor de statusvelden van de verkooporder instellen
description: In dit onderwerp wordt uitgelegd hoe u de statusvelden voor verkooporders instelt voor twee keer wegschrijven.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829280"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="d7651-103">De toewijzing voor de statusvelden van de verkooporder instellen</span><span class="sxs-lookup"><span data-stu-id="d7651-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7651-104">De velden die de status van de verkooporder aangeven, hebben verschillende opsommingswaarden in Microsoft Dynamics 365 Supply Chain Management en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d7651-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="d7651-105">Aanvullende instellingen zijn vereist om deze velden te kunnen koppelen in twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="d7651-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="d7651-106">Velden in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d7651-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="d7651-107">In Supply Chain Management geven twee velden de status van de verkooporder weer.</span><span class="sxs-lookup"><span data-stu-id="d7651-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="d7651-108">De velden die u moet toewijzen zijn **Status** en **Documentstatus**.</span><span class="sxs-lookup"><span data-stu-id="d7651-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="d7651-109">De opsommingswaarde **Status** geeft de algemene status van de order aan.</span><span class="sxs-lookup"><span data-stu-id="d7651-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="d7651-110">Deze status wordt weergegeven in de orderkop.</span><span class="sxs-lookup"><span data-stu-id="d7651-110">This status is shown on the order header.</span></span>

<span data-ttu-id="d7651-111">De opsommingswaarde **Status** heeft de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="d7651-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="d7651-112">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-112">Open Order</span></span>
- <span data-ttu-id="d7651-113">Geleverd</span><span class="sxs-lookup"><span data-stu-id="d7651-113">Delivered</span></span>
- <span data-ttu-id="d7651-114">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-114">Invoiced</span></span>
- <span data-ttu-id="d7651-115">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="d7651-115">Cancelled</span></span>

<span data-ttu-id="d7651-116">De opsommingswaarde **Documentstatus** geeft het meest recente document aan dat voor de order is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d7651-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="d7651-117">Als de order bijvoorbeeld is bevestigd, is dit document een verkooporderbevestiging.</span><span class="sxs-lookup"><span data-stu-id="d7651-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="d7651-118">Als een verkooporder gedeeltelijk is gefactureerd en de resterende regel is bevestigd, behoudt het document de status **Factuur** omdat de factuur later in het proces wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d7651-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="d7651-119">De opsommingswaarde **Documentstatus** heeft de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="d7651-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="d7651-120">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="d7651-120">Confirmation</span></span>
- <span data-ttu-id="d7651-121">Orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="d7651-121">Picking List</span></span>
- <span data-ttu-id="d7651-122">Pakbon</span><span class="sxs-lookup"><span data-stu-id="d7651-122">Packing Slip</span></span>
- <span data-ttu-id="d7651-123">Factuur</span><span class="sxs-lookup"><span data-stu-id="d7651-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="d7651-124">Velden in Verkoop</span><span class="sxs-lookup"><span data-stu-id="d7651-124">Fields in Sales</span></span>

<span data-ttu-id="d7651-125">In Verkoop geven twee velden de status van de order weer.</span><span class="sxs-lookup"><span data-stu-id="d7651-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="d7651-126">De velden die u moet toewijzen zijn **Status** en **Verwerkingsstatus**.</span><span class="sxs-lookup"><span data-stu-id="d7651-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="d7651-127">De opsommingswaarde **Status** geeft de algemene status van de order aan.</span><span class="sxs-lookup"><span data-stu-id="d7651-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="d7651-128">Het heeft de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="d7651-128">It has the following values:</span></span>

- <span data-ttu-id="d7651-129">Actief</span><span class="sxs-lookup"><span data-stu-id="d7651-129">Active</span></span>
- <span data-ttu-id="d7651-130">Ingediend</span><span class="sxs-lookup"><span data-stu-id="d7651-130">Submitted</span></span>
- <span data-ttu-id="d7651-131">Afgehandeld</span><span class="sxs-lookup"><span data-stu-id="d7651-131">Fulfilled</span></span>
- <span data-ttu-id="d7651-132">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-132">Invoiced</span></span>
- <span data-ttu-id="d7651-133">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="d7651-133">Cancelled</span></span>

<span data-ttu-id="d7651-134">De opsommingswaarde **Verwerkingsstatus** is geïntroduceerd zodat de status nauwkeuriger kan worden toegewezen met Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7651-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="d7651-135">In de volgende tabel wordt de toewijzing van **Verwerkingsstatus** in Supply Chain Management weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d7651-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="d7651-136">Verwerkingsstatus</span><span class="sxs-lookup"><span data-stu-id="d7651-136">Processing Status</span></span>   | <span data-ttu-id="d7651-137">Status in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d7651-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="d7651-138">Documentstatus in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d7651-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="d7651-139">Actief</span><span class="sxs-lookup"><span data-stu-id="d7651-139">Active</span></span>              | <span data-ttu-id="d7651-140">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-140">Open Order</span></span>                        | <span data-ttu-id="d7651-141">None</span><span class="sxs-lookup"><span data-stu-id="d7651-141">None</span></span>                                       |
| <span data-ttu-id="d7651-142">Bevestigd</span><span class="sxs-lookup"><span data-stu-id="d7651-142">Confirmed</span></span>           | <span data-ttu-id="d7651-143">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-143">Open Order</span></span>                        | <span data-ttu-id="d7651-144">Bevestiging</span><span class="sxs-lookup"><span data-stu-id="d7651-144">Confirmation</span></span>                               |
| <span data-ttu-id="d7651-145">Opgenomen</span><span class="sxs-lookup"><span data-stu-id="d7651-145">Picked</span></span>              | <span data-ttu-id="d7651-146">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-146">Open Order</span></span>                        | <span data-ttu-id="d7651-147">Orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="d7651-147">Picking List</span></span>                               |
| <span data-ttu-id="d7651-148">Gedeeltelijk geleverd</span><span class="sxs-lookup"><span data-stu-id="d7651-148">Partially Delivered</span></span> | <span data-ttu-id="d7651-149">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-149">Open Order</span></span>                        | <span data-ttu-id="d7651-150">Pakbon</span><span class="sxs-lookup"><span data-stu-id="d7651-150">Packing Slip</span></span>                               |
| <span data-ttu-id="d7651-151">Geleverd</span><span class="sxs-lookup"><span data-stu-id="d7651-151">Delivered</span></span>           | <span data-ttu-id="d7651-152">Geleverd</span><span class="sxs-lookup"><span data-stu-id="d7651-152">Delivered</span></span>                         | <span data-ttu-id="d7651-153">Pakbon</span><span class="sxs-lookup"><span data-stu-id="d7651-153">Packing Slip</span></span>                               |
| <span data-ttu-id="d7651-154">Gedeeltelijk gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-154">Partially Invoiced</span></span>  | <span data-ttu-id="d7651-155">Geleverd</span><span class="sxs-lookup"><span data-stu-id="d7651-155">Delivered</span></span>                         | <span data-ttu-id="d7651-156">Factuur</span><span class="sxs-lookup"><span data-stu-id="d7651-156">Invoice</span></span>                                    |
| <span data-ttu-id="d7651-157">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-157">Invoiced</span></span>            | <span data-ttu-id="d7651-158">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-158">Invoiced</span></span>                          | <span data-ttu-id="d7651-159">Factuur</span><span class="sxs-lookup"><span data-stu-id="d7651-159">Invoice</span></span>                                    |
| <span data-ttu-id="d7651-160">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="d7651-160">Cancelled</span></span>           | <span data-ttu-id="d7651-161">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="d7651-161">Cancelled</span></span>                         | <span data-ttu-id="d7651-162">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="d7651-162">Not applicable</span></span>                             |

<span data-ttu-id="d7651-163">In de volgende tabel wordt de toewijzing van **Verwerkingsstatus** tussen Verkoop en Supply Chain Management weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d7651-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="d7651-164">Verwerkingsstatus</span><span class="sxs-lookup"><span data-stu-id="d7651-164">Processing Status</span></span>   | <span data-ttu-id="d7651-165">Status in Verkoop</span><span class="sxs-lookup"><span data-stu-id="d7651-165">Status in Sales</span></span> | <span data-ttu-id="d7651-166">Status in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d7651-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="d7651-167">Actief</span><span class="sxs-lookup"><span data-stu-id="d7651-167">Active</span></span>              | <span data-ttu-id="d7651-168">Actief</span><span class="sxs-lookup"><span data-stu-id="d7651-168">Active</span></span>          | <span data-ttu-id="d7651-169">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-169">Open Order</span></span>                        |
| <span data-ttu-id="d7651-170">Bevestigd</span><span class="sxs-lookup"><span data-stu-id="d7651-170">Confirmed</span></span>           | <span data-ttu-id="d7651-171">Ingediend</span><span class="sxs-lookup"><span data-stu-id="d7651-171">Submitted</span></span>       | <span data-ttu-id="d7651-172">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-172">Open Order</span></span>                        |
| <span data-ttu-id="d7651-173">Opgenomen</span><span class="sxs-lookup"><span data-stu-id="d7651-173">Picked</span></span>              | <span data-ttu-id="d7651-174">Ingediend</span><span class="sxs-lookup"><span data-stu-id="d7651-174">Submitted</span></span>       | <span data-ttu-id="d7651-175">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-175">Open Order</span></span>                        |
| <span data-ttu-id="d7651-176">Gedeeltelijk geleverd</span><span class="sxs-lookup"><span data-stu-id="d7651-176">Partially Delivered</span></span> | <span data-ttu-id="d7651-177">Actief</span><span class="sxs-lookup"><span data-stu-id="d7651-177">Active</span></span>          | <span data-ttu-id="d7651-178">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-178">Open Order</span></span>                        |
| <span data-ttu-id="d7651-179">Gedeeltelijk gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-179">Partially Invoiced</span></span>  | <span data-ttu-id="d7651-180">Actief</span><span class="sxs-lookup"><span data-stu-id="d7651-180">Active</span></span>          | <span data-ttu-id="d7651-181">Openstaande order</span><span class="sxs-lookup"><span data-stu-id="d7651-181">Open Order</span></span>                        |
| <span data-ttu-id="d7651-182">Gedeeltelijk gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-182">Partially Invoiced</span></span>  | <span data-ttu-id="d7651-183">Afgehandeld</span><span class="sxs-lookup"><span data-stu-id="d7651-183">Fulfilled</span></span>       | <span data-ttu-id="d7651-184">Geleverd</span><span class="sxs-lookup"><span data-stu-id="d7651-184">Delivered</span></span>                         |
| <span data-ttu-id="d7651-185">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-185">Invoiced</span></span>            | <span data-ttu-id="d7651-186">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-186">Invoiced</span></span>        | <span data-ttu-id="d7651-187">Gefactureerd</span><span class="sxs-lookup"><span data-stu-id="d7651-187">Invoiced</span></span>                          |
| <span data-ttu-id="d7651-188">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="d7651-188">Cancelled</span></span>           | <span data-ttu-id="d7651-189">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="d7651-189">Cancelled</span></span>       | <span data-ttu-id="d7651-190">Geannuleerd</span><span class="sxs-lookup"><span data-stu-id="d7651-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="d7651-191">Instelling</span><span class="sxs-lookup"><span data-stu-id="d7651-191">Setup</span></span>

<span data-ttu-id="d7651-192">Om de toewijzing voor de statusvelden van verkooporders in te stellen, moet u de kenmerken **IsSOPIntegrationEnabled** en **isIntegrationUser** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="d7651-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="d7651-193">Volg deze stappen als u het kenmerk **IsSOPIntegrationEnabled** wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="d7651-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="d7651-194">Ga in een browser naar `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="d7651-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="d7651-195">Vervang **\<test-name\>** door de koppeling van uw bedrijf met Verkoop.</span><span class="sxs-lookup"><span data-stu-id="d7651-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="d7651-196">Zoek **organizationid** op de pagina die is geopend en noteer de waarde.</span><span class="sxs-lookup"><span data-stu-id="d7651-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizationid zoeken](media/sales-map-orgid.png)

3. <span data-ttu-id="d7651-198">Open de browserconsole in Verkoop en voer het volgende script uit.</span><span class="sxs-lookup"><span data-stu-id="d7651-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="d7651-199">Gebruik de waarde van **organizationid** uit stap 2.</span><span class="sxs-lookup"><span data-stu-id="d7651-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-code in de browserconsole](media/sales-map-script.png)

4. <span data-ttu-id="d7651-201">Controleer of **IsSOPIntegrationEnabled** is ingesteld op **true**.</span><span class="sxs-lookup"><span data-stu-id="d7651-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="d7651-202">Gebruik de URL uit stap 1 om de waarde te controleren.</span><span class="sxs-lookup"><span data-stu-id="d7651-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled ingesteld op true](media/sales-map-integration-enabled.png)

<span data-ttu-id="d7651-204">Volg deze stappen als u het kenmerk **isIntegrationUser** wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="d7651-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="d7651-205">Ga in Verkoop naar **Instelling \> Aanpassen \> Het systeem aanpassen**. Selecteer **Gebruikersentiteit** en open **Formulier \> Gebruiker**.</span><span class="sxs-lookup"><span data-stu-id="d7651-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Het gebruikersformulier openen](media/sales-map-user.png)

2. <span data-ttu-id="d7651-207">Zoek in Veldverkenner **Integratiegebruikersmodus** en dubbelklik erop om deze toe te voegen aan het formulier.</span><span class="sxs-lookup"><span data-stu-id="d7651-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="d7651-208">Sla de wijziging op.</span><span class="sxs-lookup"><span data-stu-id="d7651-208">Save your change.</span></span>

    ![Het veld Integratiegebruikersmodus toevoegen aan het formulier](media/sales-map-field-explorer.png)

3. <span data-ttu-id="d7651-210">Ga in Verkoop naar **Instelling \> Beveiliging \> Gebruikers** en wijzig de weergave van **Ingeschakelde gebruikers** in **Toepassingsgebruikers**.</span><span class="sxs-lookup"><span data-stu-id="d7651-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![De weergave wijzigen van Ingeschakelde gebruikers in Toepassingsgebruikers](media/sales-map-enabled-users.png)

4. <span data-ttu-id="d7651-212">Selecteer de twee items voor **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="d7651-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Lijst met toepassingsgebruikers](media/sales-map-user-mode.png)

5. <span data-ttu-id="d7651-214">Wijzig de waarde van het veld **Integratiegebruikersmodus** in **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d7651-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![De waarde van het veld Integratiegebruikersmodus wijzigen in Ja](media/sales-map-user-mode-yes.png)

<span data-ttu-id="d7651-216">Uw verkooporders zijn nu toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d7651-216">Your sales orders are now mapped.</span></span>
