---
title: Problemen tijdens eerste synchronisatie oplossen
description: Dit onderwerp bevat informatie over het oplossen van problemen die kunnen optreden bij de eerste synchronisatie.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410076"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="0c3e5-103">Problemen tijdens eerste synchronisatie oplossen</span><span class="sxs-lookup"><span data-stu-id="0c3e5-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c3e5-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="0c3e5-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen die kunnen optreden bij de eerste synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c3e5-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="0c3e5-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0c3e5-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="0c3e5-108">Controleren op initiële synchronisatiefouten in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="0c3e5-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="0c3e5-109">Nadat u de toewijzingssjablonen hebt ingeschakeld, moet de status van de toewijzingen **Wordt uitgevoerd** zijn.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="0c3e5-110">Als de status **Wordt niet uitgevoerd**, zijn er fouten opgetreden tijdens de initiële synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="0c3e5-111">Als u de fouten wilt weergeven , selecteert u het tabblad **Details initiële synchronisatie** op de pagina **Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Tabblad Details initiële synchronisatie](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="0c3e5-113">U kunt de initiële synchronisatie niet voltooien: 400 Ongeldige aanvraag</span><span class="sxs-lookup"><span data-stu-id="0c3e5-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="0c3e5-114">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="0c3e5-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="0c3e5-115">Het volgende foutbericht kan worden weergegeven wanneer u probeert de toewijzing en de initiële synchronisatie uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="0c3e5-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="0c3e5-116">*De externe server heeft een fout geretourneerd: (400 Ongeldige aanvraag.), er is een fout opgetreden bij de AX-export*</span><span class="sxs-lookup"><span data-stu-id="0c3e5-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="0c3e5-117">Hier volgt een voorbeeld van de volledige foutmelding.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="0c3e5-118">Als deze fout voortdurend optreedt en u de eerste synchronisatie niet kunt voltooien, voert u de volgende stappen uit om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="0c3e5-119">Meld u aan bij de virtuele machine (VM) voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="0c3e5-120">Open Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="0c3e5-121">Controleer in het deelvenster **Services** of de Microsoft Dynamics 365-raamwerkservice voor gegevens importeren/exporteren wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="0c3e5-122">Start de service opnieuw als deze is gestopt omdat de initiële synchronisatie dat vereist.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="0c3e5-123">Fout bij initiële synchronisatie: 403 Verboden</span><span class="sxs-lookup"><span data-stu-id="0c3e5-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="0c3e5-124">Mogelijk wordt het volgende foutbericht weergegeven tijdens de initiële synchronisatie:</span><span class="sxs-lookup"><span data-stu-id="0c3e5-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="0c3e5-125">*(\[Verboden\], De externe server heeft een fout geretourneerd: (403) Verboden.), er is een fout opgetreden bij de AX-export*</span><span class="sxs-lookup"><span data-stu-id="0c3e5-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="0c3e5-126">Volg deze stappen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="0c3e5-127">Meld u aan bij de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="0c3e5-128">Verwijder op de pagina **Azure Active Directory-toepassingen** de **DtAppID**-client en voeg deze vervolgens opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Lijst met Azure AD-toepassingen](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="0c3e5-130">Fouten met verwijzing naar zichzelf of circulaire verwijzingen tijdens initiële synchronisatie</span><span class="sxs-lookup"><span data-stu-id="0c3e5-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="0c3e5-131">Er wordt mogelijk een foutberichten als een van uw toewijzingen naar zichzelf verwijst of kringverwijzingen bevat.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="0c3e5-132">De fouten vallen in deze categorieën:</span><span class="sxs-lookup"><span data-stu-id="0c3e5-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="0c3e5-133">Entiteitstoewijzing van Leveranciers V2 aan msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="0c3e5-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="0c3e5-134">Entiteitstoewijzing Klanten V3 aan Accounts</span><span class="sxs-lookup"><span data-stu-id="0c3e5-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="0c3e5-135">Een fout in Leveranciers v2 omzetten in een msdyn_vendors-entiteitstoewijzing</span><span class="sxs-lookup"><span data-stu-id="0c3e5-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="0c3e5-136">U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Leveranciers v2** aan **msdyn_vendors**, als de entiteiten bestaande records hebben met waarden in de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="0c3e5-137">De reden is dat **InvoiceVendorAccountNumber** een veld is dat naar zichzelf verwijst en dat **PrimaryContactPersonId** een kringverwijzing in de leverancierstoewijzing is.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="0c3e5-138">*Kan de GUID voor het veld niet omzetten: <field>. De zoekopdracht is niet gevonden: <value>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity> ?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="0c3e5-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="0c3e5-139">Hier volgen enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="0c3e5-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="0c3e5-140">*Kan de GUID voor het veld niet omzetten: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="0c3e5-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="0c3e5-141">*Kan de GUID voor het veld niet omzetten: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. De zoekopdracht is niet gevonden: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="0c3e5-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="0c3e5-142">Als u records met waarden in deze velden in de entiteit voor de leverancier hebt, volgt u de stappen in de volgende sectie om de initiële synchronisatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="0c3e5-143">Verwijder in de app Finance and Operations de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** uit de toewijzing en sla de wijzigingen op.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="0c3e5-144">Ga naar de pagina voor de toewijzing van twee keer wegschrijven voor **Leveranciers v2 (msdyn_vendors)** en selecteer het tabblad **Entiteits toewijzingen**. Selecteer in het linkerfilter de optie **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="0c3e5-145">Selecteer in het rechterfilter **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="0c3e5-146">Zoek naar **primarycontactperson** om het bronveld **PrimaryContactPersonId** te vinden.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="0c3e5-147">Klik op de knop **Acties** en selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![Zelf- of kringverwijzing 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="0c3e5-149">Herhaal dit om het veld **InvoiceVendorAccountNumber** te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![Zelf- of kringverwijzing 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="0c3e5-151">Sla de wijzigingen in de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="0c3e5-152">Schakel het bijhouden van wijzigingen uit voor de entiteit **Leveranciers v2**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="0c3e5-153">Navigeer naar **Gegevens beheer \> Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="0c3e5-154">Selecteer de entiteit **Leveranciers V2**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="0c3e5-155">Klik op **Opties** in de menubalk en wijzig vervolgens **Wijzigingen bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![Zelf- of kringverwijzing 5](media/selfref_options.png)
    
    4. <span data-ttu-id="0c3e5-157">Klik op **Wijzigingen bijhouden uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-157">Click **Disable Change Tracking**.</span></span>
    
        ![Zelf- of kringverwijzing 6](media/selfref_tracking.png)

3. <span data-ttu-id="0c3e5-159">Voer de eerste synchronisatie uit van de toewijzing van **Leveranciers v2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="0c3e5-160">De eerste synchronisatie moet zonder fouten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="0c3e5-161">Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="0c3e5-162">U moet deze toewijzing synchroniseren als u het veld voor de primaire contactpersoon in de entiteit leveranciers wilt synchroniseren omdat de records voor contactpersonen ook als eerste moeten worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="0c3e5-163">Voeg de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** weer toe aan de toewijzing **Leveranciers v2 (msdyn_vendors)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="0c3e5-164">Voer de eerste synchronisatie opnieuw uit van de toewijzing van **Leveranciers v2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="0c3e5-165">Alle records worden gesynchroniseerd omdat het bijhouden van wijzigingen is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="0c3e5-166">Schakel het bijhouden van wijzigingen in voor de entiteit **Leveranciers v2**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="0c3e5-167">Een fout in Klanten v3 omzetten naar een entiteitstoewijzing voor Accounts</span><span class="sxs-lookup"><span data-stu-id="0c3e5-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="0c3e5-168">U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Klanten v3** aan **Accounts**, als de entiteiten bestaande records hebben met waarden in de velden **ContactPersonID** en **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="0c3e5-169">De reden is dat **InvoiceAccount** een veld is dat naar zichzelf verwijst en dat **ContactPersonID** een kringverwijzing in de leverancierstoewijzing is.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="0c3e5-170">*Kan de GUID voor het veld niet omzetten: <field>. De zoekopdracht is niet gevonden: <value>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity> ?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="0c3e5-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="0c3e5-171">*Kan de GUID voor het veld niet omzetten: primarycontactid.msdyn_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="0c3e5-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="0c3e5-172">*Kan de GUID voor het veld niet omzetten: msdyn_billingaccount.accountnumber. De zoekopdracht is niet gevonden: 1206-1. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="0c3e5-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="0c3e5-173">Als u records met waarden in deze velden in de entiteit voor de klant hebt, volgt u de stappen in de volgende sectie om de initiële synchronisatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="0c3e5-174">U kunt deze methode gebruiken voor alle standaardentiteiten zoals accounts en contactpersonen.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="0c3e5-175">Verwijder in de app Finance and Operations de velden **ContactPersonID** en **InvoiceAccount** uit de toewijzing **Klanten V3 (accounts)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="0c3e5-176">Ga naar de pagina voor de toewijzing van twee keer wegschrijven voor **Klanten v2 (accounts)** en selecteer het tabblad **Entiteits toewijzingen**. Selecteer in het linkerfilter de optie **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="0c3e5-177">Selecteer in het rechterfilter **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="0c3e5-178">Zoek naar **contactperson** om het bronveld **ContactPersonID** te vinden.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="0c3e5-179">Klik op de knop **Acties** en selecteer **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![Zelf- of kringverwijzing 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="0c3e5-181">Herhaal dit om het veld **InvoiceAccount** te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![Zelf- of kringverwijzing](media/cust_selfref4.png)
    
    5. <span data-ttu-id="0c3e5-183">Sla de wijzigingen in de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="0c3e5-184">Schakel het bijhouden van wijzigingen uit voor de entiteit **Klanten v3**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="0c3e5-185">Navigeer naar **Gegevens beheer \> Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="0c3e5-186">Selecteer de entiteit **Klanten V3**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="0c3e5-187">Klik op **Opties** in de menubalk en wijzig vervolgens **Wijzigingen bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![Zelf- of kringverwijzing 5](media/selfref_options.png)
    
    4. <span data-ttu-id="0c3e5-189">Klik op **Wijzigingen bijhouden uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-189">Click **Disable Change Tracking**.</span></span>
    
        ![Zelf- of kringverwijzing 6](media/selfref_tracking.png)

3. <span data-ttu-id="0c3e5-191">Voer de eerste synchronisatie uit voor de toewijzing **Klanten V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="0c3e5-192">De eerste synchronisatie moet zonder fouten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="0c3e5-193">Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="0c3e5-194">Er zijn 2 toewijzingen met dezelfde naam.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="0c3e5-195">Selecteer de naam met de omschrijving **Sjabloon voor twee keer wegschrijven voor sync tussen FO.CDS Vendor Contacts V2 en CDS.Contacts. Vereist nieuw pakket \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="0c3e5-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="0c3e5-196">op het tabblad **Details** van de toewijzing.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="0c3e5-197">Voeg de velden **InvoiceAccount** en **ContactPersonId** weer toe uit de toewijzing **Klanten V3 (Accounts)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="0c3e5-198">Nu maken de velden **InvoiceAccount** en **ContactPersonId** weer deel uit van de live synchronisatiemodus.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="0c3e5-199">In de volgende stap voltooit u de initiële synchronisatie voor deze velden.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="0c3e5-200">Voer de eerste synchronisatie opnieuw uit voor de toewijzing **Klanten V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="0c3e5-201">Omdat het bijhouden van wijzigingen is uitgeschakeld, synchroniseert u de gegevens voor **InvoiceAccount** en **ContactPersonId** van de Finance and Operations-app met Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="0c3e5-202">Voor het synchroniseren van de gegevens voor **InvoiceAccount** en **ContactPersonId** van Common Data Service met Finance and Operations, gebruikt u een gegevensintegratieproject.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="0c3e5-203">Maak in Power Apps een gegevensintegratieproject tussen de entiteiten **Sales.Account** en **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="0c3e5-204">De gegevensrichting moet van Common Data Service naar de Finance and Operations-app gaan.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="0c3e5-205">Omdat **InvoiceAccount** een nieuw kenmerk is voor twee keer wegschrijven, wilt u mogelijk de initiële synchronisatie voor dit kenmerk overslaan.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="0c3e5-206">Zie voor meer informatie [Gegevens integreren in Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="0c3e5-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="0c3e5-207">In de volgende afbeelding ziet u een project waarmee **CustomerAccount** en **ContactPersonId** worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Zelf- of kringverwijzing](media/cust_selfref6.png)

    2. <span data-ttu-id="0c3e5-209">Voeg de bedrijfscriteria toe in het filter aan de kant van Common Data Service, omdat alleen de records die aan filtercriteria voldoen, in de app Finance and Operations worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="0c3e5-210">Klik op het filterpictogram om een filter toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="0c3e5-211">In het dialoogvenster **Query bewerken** kunt u een filterquery als **_msdyn_company_value eq '\<guid\>'** toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="0c3e5-212">Als het filterpictogram niet aanwezig is, maakt u een ondersteuningsticket om aan het gegevensintegratieteam te vragen om de filtermogelijkheid voor uw tenant in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="0c3e5-213">Als u geen filterquery voor **_msdyn_company_value** invoert, worden alle records gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![Zelf- of kringverwijzing](media/cust_selfref7.png)

        <span data-ttu-id="0c3e5-215">Hiermee is de initiële synchronisatie van de records voltooid.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="0c3e5-216">Schakel het bijhouden van wijzigingen in voor de entiteit **Klanten V3** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

