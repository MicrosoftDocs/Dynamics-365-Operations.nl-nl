---
title: Problemen tijdens eerste synchronisatie oplossen
description: Dit onderwerp bevat informatie over het oplossen van problemen die kunnen optreden bij de eerste synchronisatie.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 709a3c332bb6d086910b257fee9cdec8d2bc81a2
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941050"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="48cab-103">Problemen tijdens eerste synchronisatie oplossen</span><span class="sxs-lookup"><span data-stu-id="48cab-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="48cab-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="48cab-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="48cab-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen die kunnen optreden bij de eerste synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="48cab-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48cab-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="48cab-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="48cab-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="48cab-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="48cab-108">Controleren op initiële synchronisatiefouten in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="48cab-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="48cab-109">Nadat u de toewijzingssjablonen hebt ingeschakeld, moet de status van de toewijzingen **Wordt uitgevoerd** zijn.</span><span class="sxs-lookup"><span data-stu-id="48cab-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="48cab-110">Als de status **Wordt niet uitgevoerd**, zijn er fouten opgetreden tijdens de initiële synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="48cab-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="48cab-111">Als u de fouten wilt weergeven , selecteert u het tabblad **Details initiële synchronisatie** op de pagina **Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="48cab-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Fout op het tabblad Details initiële synchronisatie](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="48cab-113">U kunt de initiële synchronisatie niet voltooien: 400 Ongeldige aanvraag</span><span class="sxs-lookup"><span data-stu-id="48cab-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="48cab-114">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="48cab-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="48cab-115">Het volgende foutbericht kan worden weergegeven wanneer u probeert de toewijzing en de initiële synchronisatie uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="48cab-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="48cab-116">*(\[Ongeldige aanvraag\], De externe server heeft een fout geretourneerd: (400) Ongeldige aanvraag.), er is een fout opgetreden bij de AX-export*</span><span class="sxs-lookup"><span data-stu-id="48cab-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="48cab-117">Hier volgt een voorbeeld van de volledige foutmelding.</span><span class="sxs-lookup"><span data-stu-id="48cab-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="48cab-118">Als deze fout voortdurend optreedt en u de eerste synchronisatie niet kunt voltooien, voert u de volgende stappen uit om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="48cab-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="48cab-119">Meld u aan bij de virtuele machine (VM) voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="48cab-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="48cab-120">Open Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="48cab-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="48cab-121">Controleer in het deelvenster **Services** of de Microsoft Dynamics 365-raamwerkservice voor gegevens importeren/exporteren wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="48cab-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="48cab-122">Start de service opnieuw als deze is gestopt omdat de initiële synchronisatie dat vereist.</span><span class="sxs-lookup"><span data-stu-id="48cab-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="48cab-123">Fout bij initiële synchronisatie: 403 Verboden</span><span class="sxs-lookup"><span data-stu-id="48cab-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="48cab-124">Mogelijk wordt het volgende foutbericht weergegeven tijdens de initiële synchronisatie:</span><span class="sxs-lookup"><span data-stu-id="48cab-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="48cab-125">*(\[Verboden\], De externe server heeft een fout geretourneerd: (403) Verboden.), er is een fout opgetreden bij de AX-export*</span><span class="sxs-lookup"><span data-stu-id="48cab-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="48cab-126">Volg deze stappen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="48cab-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="48cab-127">Meld u aan bij de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="48cab-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="48cab-128">Verwijder op de pagina **Azure Active Directory-toepassingen** de **DtAppID**-client en voeg deze vervolgens opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="48cab-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-client in de lijst met Azure AD-toepassingen](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="48cab-130">Fouten met verwijzing naar zichzelf of circulaire verwijzingen tijdens initiële synchronisatie</span><span class="sxs-lookup"><span data-stu-id="48cab-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="48cab-131">Er wordt mogelijk een foutberichten als een van uw toewijzingen naar zichzelf verwijst of kringverwijzingen bevat.</span><span class="sxs-lookup"><span data-stu-id="48cab-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="48cab-132">De fouten vallen in deze categorieën:</span><span class="sxs-lookup"><span data-stu-id="48cab-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="48cab-133">Fouten in de tabeltoewijzing Vendors V2–to–msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="48cab-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="48cab-134">Fouten in de tabeltoewijzing Customers V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="48cab-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="48cab-135">Fouten in de tabeltoewijzing Vendors V2–to–msdyn_vendors oplossen</span><span class="sxs-lookup"><span data-stu-id="48cab-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="48cab-136">U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Leveranciers v2** aan **msdyn\_vendors**, als de tabellen bestaande rijen hebben met waarden in de kolommen **PrimaryContactPersonId** en **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="48cab-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="48cab-137">Deze fouten treden op omdat **InvoiceVendorAccountNumber** een kolom is die naar zichzelf verwijst en **PrimaryContactPersonId** een kringverwijzing is in de leverancierstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="48cab-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="48cab-138">De foutberichten die worden weergegeven, hebben de volgende vorm.</span><span class="sxs-lookup"><span data-stu-id="48cab-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="48cab-139">*Kan de GUID voor het veld niet omzetten: \<field\>. De zoekopdracht is niet gevonden: \<value\>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="48cab-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="48cab-140">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="48cab-140">Here are some examples:</span></span>

- <span data-ttu-id="48cab-141">*Kan de GUID voor het veld niet omzetten: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="48cab-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="48cab-142">*Kan de GUID voor het veld niet omzetten: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber De zoekopdracht is niet gevonden: V24-1. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="48cab-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="48cab-143">Als rijen in de tabel leverancier waarden hebben in de kolommen **PrimaryContactPersonId** en **InvoiceVendorAccountNumber**, volgt u deze stappen om de initiële synchronisatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="48cab-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="48cab-144">Verwijder in de Finance and Operations-app de kolommen **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** uit de toewijzing en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="48cab-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="48cab-145">Selecteer op de pagina voor de toewijzing van twee keer wegschrijven voor **Leveranciers v2 (msdyn\_vendors)**, op het tabblad **Ttabeltoewijzingen** in het linkerfilter de optie **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="48cab-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="48cab-146">Selecteer in het rechterfilter **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="48cab-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="48cab-147">Zoek naar **primarycontactperson** om de bronkolom **PrimaryContactPersonId** te vinden.</span><span class="sxs-lookup"><span data-stu-id="48cab-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="48cab-148">Selecteer **Acties** en vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="48cab-148">Select **Actions**, and then select **Delete**.</span></span>

        ![De kolom PrimaryContactPersonId verwijderen](media/vend_selfref3.png)

    4. <span data-ttu-id="48cab-150">Herhaal deze stappen om de kolom **InvoiceVendorAccountNumber** te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="48cab-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![De kolom InvoiceVendorAccountNumber verwijderen](media/vend-selfref4.png)

    5. <span data-ttu-id="48cab-152">Sla de wijzigingen in de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="48cab-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="48cab-153">Schakel het bijhouden van wijzigingen uit voor de tabel **Leveranciers v2**.</span><span class="sxs-lookup"><span data-stu-id="48cab-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="48cab-154">Selecteer in de werkruimte **Gegevensbeheer** de tegel **Gegevenstabellen**.</span><span class="sxs-lookup"><span data-stu-id="48cab-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="48cab-155">Selecteer de tabel **Leveranciers V2**.</span><span class="sxs-lookup"><span data-stu-id="48cab-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="48cab-156">Selecteer in het actievenster **Opties** en selecteer **Wijzigingen bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="48cab-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![De optie Wijzigingen bijhouden selecteren](media/selfref_options.png)

    4. <span data-ttu-id="48cab-158">Selecteer **Wijzigingen bijhouden uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="48cab-158">Select **Disable Change Tracking**.</span></span>

        ![Selecteer Wijzigingen bijhouden uitschakelen](media/selfref_tracking.png)

3. <span data-ttu-id="48cab-160">Voer de initiële synchronisatie opnieuw uit van de toewijzing **Leveranciers v2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="48cab-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="48cab-161">De eerste synchronisatie moet zonder fouten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="48cab-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="48cab-162">Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="48cab-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="48cab-163">U moet deze toewijzing synchroniseren als u de kolom voor de primaire contactpersoon in de tabel leveranciers wilt synchroniseren, omdat initiële synchronisatie ook moet worden uitgevoerd voor de rijen voor contactpersonen.</span><span class="sxs-lookup"><span data-stu-id="48cab-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="48cab-164">Voeg de kolommen **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** weer toe aan de toewijzing **Leveranciers v2 (msdyn\_vendors)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="48cab-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="48cab-165">Voer de initiële synchronisatie opnieuw uit van de toewijzing **Leveranciers v2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="48cab-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="48cab-166">Alle rijen worden gesynchroniseerd omdat het bijhouden van wijzigingen is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="48cab-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="48cab-167">Schakel het bijhouden van wijzigingen weer in voor de tabel **Leveranciers v2**.</span><span class="sxs-lookup"><span data-stu-id="48cab-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="48cab-168">Fouten oplossen in de tabeltoewijzing Klanten V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="48cab-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="48cab-169">U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Klanten v3** aan **Accounts**, als de tabellen bestaande rijen hebben met waarden in de kolommen **ContactPersonID** en **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="48cab-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="48cab-170">Deze fouten treden op omdat **InvoiceAccount** een kolom is die naar zichzelf verwijst en **ContactPersonID** een kringverwijzing in de leverancierstoewijzing is.</span><span class="sxs-lookup"><span data-stu-id="48cab-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="48cab-171">De foutberichten die worden weergegeven, hebben de volgende vorm.</span><span class="sxs-lookup"><span data-stu-id="48cab-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="48cab-172">*Kan de GUID voor het veld niet omzetten: \<field\>. De zoekopdracht is niet gevonden: \<value\>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="48cab-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="48cab-173">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="48cab-173">Here are some examples:</span></span>

- <span data-ttu-id="48cab-174">*Kan de GUID voor het veld niet omzetten: primarycontactid.msdyn\_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="48cab-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="48cab-175">*Kan de GUID voor het veld niet omzetten: msdyn\_billingaccount.accountnumber. De zoekopdracht is niet gevonden: 1206-1. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="48cab-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="48cab-176">Als rijen in de tabel klant waarden hebben in de kolommen **ContactPersonID** en **InvoiceAccount**, volgt u deze stappen om de initiële synchronisatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="48cab-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="48cab-177">U kunt deze methode gebruiken voor alle standaardtabellen zoals **accounts** en **contactpersonen**.</span><span class="sxs-lookup"><span data-stu-id="48cab-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="48cab-178">Verwijder in de Finance and Operations-app de kolommen **ContactPersonID** en **InvoiceAccount** uit de toewijzing **Klanten V3 (accounts)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="48cab-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="48cab-179">Selecteer op de pagina voor de toewijzing van twee keer wegschrijven voor **Klanten v3 (accounts)** op het tabblad **Tabeltoewijzingen** in het linkerfilter de optie **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="48cab-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="48cab-180">Selecteer in het rechterfilter **Dataverse.Account**.</span><span class="sxs-lookup"><span data-stu-id="48cab-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="48cab-181">Zoek naar **contactperson** om de bronkolom **ContactPersonID** te vinden.</span><span class="sxs-lookup"><span data-stu-id="48cab-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="48cab-182">Selecteer **Acties** en vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="48cab-182">Select **Actions**, and then select **Delete**.</span></span>

        ![De kolom ContactPersonID verwijderen](media/cust_selfref3.png)

    4. <span data-ttu-id="48cab-184">Herhaal deze stappen om de kolom **InvoiceAccount** te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="48cab-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![De kolom InvoiceAccount verwijderen](media/cust_selfref4.png)

    5. <span data-ttu-id="48cab-186">Sla de wijzigingen in de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="48cab-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="48cab-187">Schakel het bijhouden van wijzigingen uit voor de tabel **Klanten v3**.</span><span class="sxs-lookup"><span data-stu-id="48cab-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="48cab-188">Selecteer in de werkruimte **Gegevensbeheer** de tegel **Gegevenstabellen**.</span><span class="sxs-lookup"><span data-stu-id="48cab-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="48cab-189">Selecteer de tabel **Klanten V3**.</span><span class="sxs-lookup"><span data-stu-id="48cab-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="48cab-190">Selecteer in het actievenster **Opties** en selecteer **Wijzigingen bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="48cab-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![De optie Wijzigingen bijhouden selecteren](media/selfref_options.png)

    4. <span data-ttu-id="48cab-192">Selecteer **Wijzigingen bijhouden uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="48cab-192">Select **Disable Change Tracking**.</span></span>

        ![Selecteer Wijzigingen bijhouden uitschakelen](media/selfref_tracking.png)

3. <span data-ttu-id="48cab-194">Voer de eerste synchronisatie opnieuw uit voor de toewijzing **Klanten V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="48cab-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="48cab-195">De eerste synchronisatie moet zonder fouten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="48cab-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="48cab-196">Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="48cab-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="48cab-197">Er zijn twee toewijzingen met dezelfde naam.</span><span class="sxs-lookup"><span data-stu-id="48cab-197">There are two maps that have the same name.</span></span> <span data-ttu-id="48cab-198">Selecteer de toewijzing met de volgende omschrijving op het tabblad **Details**: **Sjabloon voor twee keer wegschrijven voor sync tussen FO.CDS Vendor Contacts V2 to CDS.Contacts. Vereist nieuw pakket \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="48cab-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="48cab-199">Voeg de kolommen **InvoiceAccount** en **ContactPersonId** weer toe aan de toewijzing **Klanten V3 (Accounts)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="48cab-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="48cab-200">Nu maken de kolommen **InvoiceAccount** en **ContactPersonId** weer deel uit van de live synchronisatiemodus.</span><span class="sxs-lookup"><span data-stu-id="48cab-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="48cab-201">In de volgende stap voert u de initiële synchronisatie uit voor deze kolommen.</span><span class="sxs-lookup"><span data-stu-id="48cab-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="48cab-202">Voer de initiële synchronisatie opnieuw uit voor de toewijzing **Klanten V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="48cab-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="48cab-203">Omdat het bijhouden van wijzigingen is uitgeschakeld, worden de gegevens voor **InvoiceAccount** en **ContactPersonId** uit de Finance and Operations-app gesynchroniseerd met Dataverse.</span><span class="sxs-lookup"><span data-stu-id="48cab-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="48cab-204">Voor het synchroniseren van de gegevens voor **InvoiceAccount** en **ContactPersonId** van Dataverse met de Finance and Operations-app, gebruikt u een gegevensintegratieproject.</span><span class="sxs-lookup"><span data-stu-id="48cab-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="48cab-205">Maak in Power Apps een gegevensintegratieproject tussen de tabellen **Sales.Account** en **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="48cab-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="48cab-206">De gegevensrichting moet van Dataverse naar de Finance and Operations-app gaan.</span><span class="sxs-lookup"><span data-stu-id="48cab-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="48cab-207">Omdat **InvoiceAccount** een nieuw kenmerk is voor twee keer wegschrijven, wilt u mogelijk de initiële synchronisatie voor dit kenmerk overslaan.</span><span class="sxs-lookup"><span data-stu-id="48cab-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="48cab-208">Zie voor meer informatie [Gegevens integreren in Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="48cab-208">For more information, see [Integrate data into Dataverse](/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="48cab-209">In de volgende afbeelding ziet u een project waarmee **CustomerAccount** en **ContactPersonId** worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="48cab-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Gegevensintegratieproject voor het bijwerken van CustomerAccount en ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="48cab-211">Voeg de bedrijfscriteria toe in het filter aan de kant van Dataverse, zodat alleen de rijen die aan de filtercriteria voldoen, in de app Finance and Operations worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="48cab-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="48cab-212">Klik op de filterknop om een filter toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="48cab-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="48cab-213">Voeg vervolgens In het dialoogvenster **Query bewerken** een filterquery als **\_msdyn\_company\_value eq '\<guid\>'** toe.</span><span class="sxs-lookup"><span data-stu-id="48cab-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="48cab-214">[OPMERKING] Als de filterknop niet aanwezig is, maakt u een ondersteuningsticket om aan het gegevensintegratieteam te vragen om de filtermogelijkheid voor uw tenant in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="48cab-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="48cab-215">Als u geen filterquery voor **\_msdyn\_company\_value** invoert, worden alle rijen gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="48cab-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Een filterquery toevoegen](media/cust_selfref7.png)

    <span data-ttu-id="48cab-217">De initiële synchronisatie van de rijen is nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="48cab-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="48cab-218">Schakel het bijhouden van wijzigingen in voor de tabel **Klanten V3** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="48cab-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]