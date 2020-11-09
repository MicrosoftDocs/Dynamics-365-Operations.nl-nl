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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 4d0ca1fb4b7a4964194516544686b6bb7d26e76c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997321"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="23783-103">Problemen tijdens eerste synchronisatie oplossen</span><span class="sxs-lookup"><span data-stu-id="23783-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23783-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="23783-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="23783-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen die kunnen optreden bij de eerste synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="23783-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23783-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="23783-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="23783-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="23783-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="23783-108">Controleren op initiële synchronisatiefouten in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="23783-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="23783-109">Nadat u de toewijzingssjablonen hebt ingeschakeld, moet de status van de toewijzingen **Wordt uitgevoerd** zijn.</span><span class="sxs-lookup"><span data-stu-id="23783-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="23783-110">Als de status **Wordt niet uitgevoerd** , zijn er fouten opgetreden tijdens de initiële synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="23783-110">If the status is **Not running** , errors occurred during initial synchronization.</span></span> <span data-ttu-id="23783-111">Als u de fouten wilt weergeven , selecteert u het tabblad **Details initiële synchronisatie** op de pagina **Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="23783-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Fout op het tabblad Details initiële synchronisatie](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="23783-113">U kunt de initiële synchronisatie niet voltooien: 400 Ongeldige aanvraag</span><span class="sxs-lookup"><span data-stu-id="23783-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="23783-114">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="23783-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="23783-115">Het volgende foutbericht kan worden weergegeven wanneer u probeert de toewijzing en de initiële synchronisatie uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="23783-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="23783-116">*(\[Ongeldige aanvraag\], De externe server heeft een fout geretourneerd: (400) Ongeldige aanvraag.), er is een fout opgetreden bij de AX-export*</span><span class="sxs-lookup"><span data-stu-id="23783-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="23783-117">Hier volgt een voorbeeld van de volledige foutmelding.</span><span class="sxs-lookup"><span data-stu-id="23783-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="23783-118">Als deze fout voortdurend optreedt en u de eerste synchronisatie niet kunt voltooien, voert u de volgende stappen uit om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="23783-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="23783-119">Meld u aan bij de virtuele machine (VM) voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="23783-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="23783-120">Open Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="23783-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="23783-121">Controleer in het deelvenster **Services** of de Microsoft Dynamics 365-raamwerkservice voor gegevens importeren/exporteren wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="23783-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="23783-122">Start de service opnieuw als deze is gestopt omdat de initiële synchronisatie dat vereist.</span><span class="sxs-lookup"><span data-stu-id="23783-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="23783-123">Fout bij initiële synchronisatie: 403 Verboden</span><span class="sxs-lookup"><span data-stu-id="23783-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="23783-124">Mogelijk wordt het volgende foutbericht weergegeven tijdens de initiële synchronisatie:</span><span class="sxs-lookup"><span data-stu-id="23783-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="23783-125">*(\[Verboden\], De externe server heeft een fout geretourneerd: (403) Verboden.), er is een fout opgetreden bij de AX-export*</span><span class="sxs-lookup"><span data-stu-id="23783-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="23783-126">Volg deze stappen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="23783-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="23783-127">Meld u aan bij de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="23783-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="23783-128">Verwijder op de pagina **Azure Active Directory-toepassingen** de **DtAppID** -client en voeg deze vervolgens opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="23783-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-client in de lijst met Azure AD-toepassingen](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="23783-130">Fouten met verwijzing naar zichzelf of circulaire verwijzingen tijdens initiële synchronisatie</span><span class="sxs-lookup"><span data-stu-id="23783-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="23783-131">Er wordt mogelijk een foutberichten als een van uw toewijzingen naar zichzelf verwijst of kringverwijzingen bevat.</span><span class="sxs-lookup"><span data-stu-id="23783-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="23783-132">De fouten vallen in deze categorieën:</span><span class="sxs-lookup"><span data-stu-id="23783-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="23783-133">Fouten in de entiteitstoewijzing Vendors V2–to–msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="23783-133">Errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="23783-134">Fouten in de  entiteitstoewijzing Customers V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="23783-134">Errors in the Customers V3–to–Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="23783-135">Fouten in de entiteitstoewijzing Vendors V2–to–msdyn_vendors oplossen</span><span class="sxs-lookup"><span data-stu-id="23783-135">Resolve errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>

<span data-ttu-id="23783-136">U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Leveranciers v2** aan **msdyn\_vendors** , als de entiteiten bestaande records hebben met waarden in de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="23783-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the entities have existing records where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="23783-137">Deze fouten treden op omdat **InvoiceVendorAccountNumber** een veld is dat naar zichzelf verwijst en **PrimaryContactPersonId** een kringverwijzing is in de leverancierstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="23783-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="23783-138">De foutberichten die worden weergegeven, hebben de volgende vorm.</span><span class="sxs-lookup"><span data-stu-id="23783-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="23783-139">*Kan de GUID voor het veld niet omzetten: \<field\>. De zoekopdracht is niet gevonden: \<value\>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="23783-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="23783-140">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="23783-140">Here are some examples:</span></span>

- <span data-ttu-id="23783-141">*Kan de GUID voor het veld niet omzetten: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="23783-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="23783-142">*Kan de GUID voor het veld niet omzetten: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber De zoekopdracht is niet gevonden: V24-1. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="23783-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="23783-143">Als records in de entiteit leverancier waarden hebben in de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** , volgt u deze stappen om de initiële synchronisatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="23783-143">If any records in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="23783-144">Verwijder in de app Finance and Operations de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** uit de toewijzing en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="23783-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="23783-145">Selecteer op de pagina voor de toewijzing van twee keer wegschrijven voor **Leveranciers v2 (msdyn\_vendors)** , op het tabblad **Entiteitstoewijzingen** in het linkerfilter de optie **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="23783-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="23783-146">Selecteer in het rechterfilter **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="23783-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="23783-147">Zoek naar **primarycontactperson** om het bronveld **PrimaryContactPersonId** te vinden.</span><span class="sxs-lookup"><span data-stu-id="23783-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="23783-148">Selecteer **Acties** en vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="23783-148">Select **Actions** , and then select **Delete**.</span></span>

        ![Het veld PrimaryContactPersonId verwijderen](media/vend_selfref3.png)

    4. <span data-ttu-id="23783-150">Herhaal deze stappen om het veld **InvoiceVendorAccountNumber** te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="23783-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![Het veld InvoiceVendorAccountNumber verwijderen](media/vend-selfref4.png)

    5. <span data-ttu-id="23783-152">Sla de wijzigingen in de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="23783-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="23783-153">Schakel het bijhouden van wijzigingen uit voor de entiteit **Leveranciers v2**.</span><span class="sxs-lookup"><span data-stu-id="23783-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="23783-154">Selecteer in de werkruimte **Gegevensbeheer** de tegel **Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="23783-154">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="23783-155">Selecteer de entiteit **Leveranciers V2**.</span><span class="sxs-lookup"><span data-stu-id="23783-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="23783-156">Selecteer in het actievenster **Opties** en selecteer **Wijzigingen bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="23783-156">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![De optie Wijzigingen bijhouden selecteren](media/selfref_options.png)

    4. <span data-ttu-id="23783-158">Selecteer **Wijzigingen bijhouden uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="23783-158">Select **Disable Change Tracking**.</span></span>

        ![Selecteer Wijzigingen bijhouden uitschakelen](media/selfref_tracking.png)

3. <span data-ttu-id="23783-160">Voer de initiële synchronisatie opnieuw uit van de toewijzing **Leveranciers v2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="23783-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="23783-161">De eerste synchronisatie moet zonder fouten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="23783-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="23783-162">Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="23783-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="23783-163">U moet deze toewijzing synchroniseren als u het veld voor de primaire contactpersoon in de entiteit leveranciers wilt synchroniseren, omdat initiële synchronisatie ook moet worden uitgevoerd voor de records voor contactpersonen.</span><span class="sxs-lookup"><span data-stu-id="23783-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact records.</span></span>
5. <span data-ttu-id="23783-164">Voeg de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** weer toe aan de toewijzing **Leveranciers v2 (msdyn\_vendors)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="23783-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="23783-165">Voer de initiële synchronisatie opnieuw uit van de toewijzing **Leveranciers v2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="23783-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="23783-166">Alle records worden gesynchroniseerd omdat het bijhouden van wijzigingen is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="23783-166">Because change tracking is turned off, all the records will be synced.</span></span>
7. <span data-ttu-id="23783-167">Schakel het bijhouden van wijzigingen weer in voor de entiteit **Leveranciers v2**.</span><span class="sxs-lookup"><span data-stu-id="23783-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="23783-168">Fouten oplossen in de entiteitstoewijzing Klanten V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="23783-168">Resolve errors in the Customers V3–to–Accounts entity mapping</span></span>

<span data-ttu-id="23783-169">U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Klanten v3** aan **Accounts** , als de entiteiten bestaande records hebben met waarden in de velden **ContactPersonID** en **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="23783-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the entities have existing records where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="23783-170">Deze foutne treden op omdat **InvoiceAccount** een veld is dat naar zichzelf verwijst en **ContactPersonID** een kringverwijzing in de leverancierstoewijzing is.</span><span class="sxs-lookup"><span data-stu-id="23783-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="23783-171">De foutberichten die worden weergegeven, hebben de volgende vorm.</span><span class="sxs-lookup"><span data-stu-id="23783-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="23783-172">*Kan de GUID voor het veld niet omzetten: \<field\>. De zoekopdracht is niet gevonden: \<value\>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="23783-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="23783-173">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="23783-173">Here are some examples:</span></span>

- <span data-ttu-id="23783-174">*Kan de GUID voor het veld niet omzetten: primarycontactid.msdyn\_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="23783-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="23783-175">*Kan de GUID voor het veld niet omzetten: msdyn\_billingaccount.accountnumber. De zoekopdracht is niet gevonden: 1206-1. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="23783-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="23783-176">Als records in de entiteit klant waarden hebben in de velden **ContactPersonID** en **InvoiceAccount** , volgt u deze stappen om de initiële synchronisatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="23783-176">If any records in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="23783-177">U kunt deze methode gebruiken voor alle standaardentiteiten zoals **accounts** en **contactpersonen**.</span><span class="sxs-lookup"><span data-stu-id="23783-177">You can use this approach for any out-of-box entities, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="23783-178">Verwijder in de app Finance and Operations de velden **ContactPersonID** en **InvoiceAccount** uit de toewijzing **Klanten V3 (accounts)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="23783-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="23783-179">Selecteer op de pagina voor de toewijzing van twee keer wegschrijven voor **Klanten v3 (accounts)** op het tabblad **Entiteitstoewijzingen** in het linkerfilter de optie **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="23783-179">On the dual-write mapping page for **Customers V3 (accounts)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="23783-180">Selecteer in het rechterfilter **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="23783-180">In the right filter, select **Common Data Service.Account**.</span></span>
    2. <span data-ttu-id="23783-181">Zoek naar **contactperson** om het bronveld **ContactPersonID** te vinden.</span><span class="sxs-lookup"><span data-stu-id="23783-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="23783-182">Selecteer **Acties** en vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="23783-182">Select **Actions** , and then select **Delete**.</span></span>

        ![Het veld ContactPersonID verwijderen](media/cust_selfref3.png)

    4. <span data-ttu-id="23783-184">Herhaal deze stappen om het veld **InvoiceAccount** te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="23783-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![Het veld InvoiceAccount verwijderen](media/cust_selfref4.png)

    5. <span data-ttu-id="23783-186">Sla de wijzigingen in de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="23783-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="23783-187">Schakel het bijhouden van wijzigingen uit voor de entiteit **Klanten v3**.</span><span class="sxs-lookup"><span data-stu-id="23783-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="23783-188">Selecteer in de werkruimte **Gegevensbeheer** de tegel **Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="23783-188">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="23783-189">Selecteer de entiteit **Klanten V3**.</span><span class="sxs-lookup"><span data-stu-id="23783-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="23783-190">Selecteer in het actievenster **Opties** en selecteer **Wijzigingen bijhouden**.</span><span class="sxs-lookup"><span data-stu-id="23783-190">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![De optie Wijzigingen bijhouden selecteren](media/selfref_options.png)

    4. <span data-ttu-id="23783-192">Selecteer **Wijzigingen bijhouden uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="23783-192">Select **Disable Change Tracking**.</span></span>

        ![Selecteer Wijzigingen bijhouden uitschakelen](media/selfref_tracking.png)

3. <span data-ttu-id="23783-194">Voer de eerste synchronisatie opnieuw uit voor de toewijzing **Klanten V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="23783-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="23783-195">De eerste synchronisatie moet zonder fouten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="23783-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="23783-196">Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="23783-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23783-197">Er zijn twee toewijzingen met dezelfde naam.</span><span class="sxs-lookup"><span data-stu-id="23783-197">There are two maps that have the same name.</span></span> <span data-ttu-id="23783-198">Selecteer de toewijzing met de volgende omschrijving op het tabblad **Details** : **Sjabloon voor twee keer wegschrijven voor sync tussen FO.CDS Vendor Contacts V2 to CDS.Contacts. Vereist nieuw pakket \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="23783-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="23783-199">Voeg de velden **InvoiceAccount** en **ContactPersonId** weer toe uit de toewijzing **Klanten V3 (Accounts)** en sla de toewijzing op.</span><span class="sxs-lookup"><span data-stu-id="23783-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="23783-200">Nu maken de velden **InvoiceAccount** en **ContactPersonId** weer deel uit van de live synchronisatiemodus.</span><span class="sxs-lookup"><span data-stu-id="23783-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="23783-201">In de volgende stap voert u de initiële synchronisatie uit voor deze velden.</span><span class="sxs-lookup"><span data-stu-id="23783-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="23783-202">Voer de initiële synchronisatie opnieuw uit voor de toewijzing **Klanten V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="23783-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="23783-203">Omdat het bijhouden van wijzigingen is uitgeschakeld, worden de gegevens voor **InvoiceAccount** en **ContactPersonId** uit de Finance and Operations-app gesynchroniseerd met Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="23783-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Common Data Service.</span></span>
7. <span data-ttu-id="23783-204">Voor het synchroniseren van de gegevens voor **InvoiceAccount** en **ContactPersonId** van Common Data Service met de Finance and Operations-app, gebruikt u een gegevensintegratieproject.</span><span class="sxs-lookup"><span data-stu-id="23783-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="23783-205">Maak in Power Apps een gegevensintegratieproject tussen de entiteiten **Sales.Account** en **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="23783-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="23783-206">De gegevensrichting moet van Common Data Service naar de Finance and Operations-app gaan.</span><span class="sxs-lookup"><span data-stu-id="23783-206">The data direction must be from Common Data Service to the Finance and Operations app.</span></span> <span data-ttu-id="23783-207">Omdat **InvoiceAccount** een nieuw kenmerk is voor twee keer wegschrijven, wilt u mogelijk de initiële synchronisatie voor dit kenmerk overslaan.</span><span class="sxs-lookup"><span data-stu-id="23783-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="23783-208">Zie voor meer informatie [Gegevens integreren in Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="23783-208">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="23783-209">In de volgende afbeelding ziet u een project waarmee **CustomerAccount** en **ContactPersonId** worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="23783-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Gegevensintegratieproject voor het bijwerken van CustomerAccount en ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="23783-211">Voeg de bedrijfscriteria toe in het filter aan de kant van Common Data Service, zodat alleen de records die aan de filtercriteria voldoen, in de app Finance and Operations worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="23783-211">Add the company criteria in the filter on the Common Data Service side, so that only records that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="23783-212">Klik op de filterknop om een filter toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="23783-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="23783-213">Voeg vervolgens In het dialoogvenster **Query bewerken** een filterquery als **\_msdyn\_company\_value eq '\<guid\>'** toe.</span><span class="sxs-lookup"><span data-stu-id="23783-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="23783-214">[OPMERKING] Als de filterknop niet aanwezig is, maakt u een ondersteuningsticket om aan het gegevensintegratieteam te vragen om de filtermogelijkheid voor uw tenant in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="23783-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="23783-215">Als u geen filterquery voor **\_msdyn\_company\_value** invoert, worden alle records gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="23783-215">If you don't enter a filter query for **\_msdyn\_company\_value** , all the records will be synced.</span></span>

        ![Een filterquery toevoegen](media/cust_selfref7.png)

    <span data-ttu-id="23783-217">De initiële synchronisatie van de records is nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="23783-217">The initial synchronization of the records is now completed.</span></span>

8. <span data-ttu-id="23783-218">Schakel het bijhouden van wijzigingen in voor de entiteit **Klanten V3** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="23783-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
