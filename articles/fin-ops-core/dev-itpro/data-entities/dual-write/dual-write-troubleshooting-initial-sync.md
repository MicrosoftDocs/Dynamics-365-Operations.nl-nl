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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172709"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="735eb-103">Problemen tijdens eerste synchronisatie oplossen</span><span class="sxs-lookup"><span data-stu-id="735eb-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="735eb-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="735eb-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="735eb-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen die kunnen optreden bij de eerste synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="735eb-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="735eb-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="735eb-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="735eb-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="735eb-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="735eb-108">Controleren op initiële synchronisatiefouten in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="735eb-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="735eb-109">Nadat u de toewijzingssjablonen hebt ingeschakeld, moet de status van de toewijzingen **Wordt uitgevoerd** zijn.</span><span class="sxs-lookup"><span data-stu-id="735eb-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="735eb-110">Als de status **Wordt niet uitgevoerd**, zijn er fouten opgetreden tijdens de initiële synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="735eb-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="735eb-111">Als u de fouten wilt weergeven , selecteert u het tabblad **Details initiële synchronisatie** op de pagina **Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="735eb-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Tabblad Details initiële synchronisatie](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="735eb-113">U kunt de initiële synchronisatie niet voltooien: 400 Ongeldige aanvraag</span><span class="sxs-lookup"><span data-stu-id="735eb-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="735eb-114">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="735eb-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="735eb-115">Het volgende foutbericht kan worden weergegeven wanneer u probeert de toewijzing en de initiële synchronisatie uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="735eb-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="735eb-116">*De externe server heeft een fout geretourneerd: (400 Ongeldige aanvraag.), er is een fout opgetreden bij de AX-export*</span><span class="sxs-lookup"><span data-stu-id="735eb-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="735eb-117">Hier volgt een voorbeeld van de volledige foutmelding.</span><span class="sxs-lookup"><span data-stu-id="735eb-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="735eb-118">Als deze fout voortdurend optreedt en u de eerste synchronisatie niet kunt voltooien, voert u de volgende stappen uit om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="735eb-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="735eb-119">Meld u aan bij de virtuele machine (VM) voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="735eb-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="735eb-120">Open Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="735eb-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="735eb-121">Controleer in het deelvenster **Services** of de Microsoft Dynamics 365-raamwerkservice voor gegevens importeren/exporteren wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="735eb-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="735eb-122">Start de service opnieuw als deze is gestopt omdat de initiële synchronisatie dat vereist.</span><span class="sxs-lookup"><span data-stu-id="735eb-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="735eb-123">Fout bij initiële synchronisatie: 403 Verboden</span><span class="sxs-lookup"><span data-stu-id="735eb-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="735eb-124">Mogelijk wordt het volgende foutbericht weergegeven tijdens de initiële synchronisatie:</span><span class="sxs-lookup"><span data-stu-id="735eb-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="735eb-125">*(\[Verboden\], De externe server heeft een fout geretourneerd: (403) Verboden.), er is een fout opgetreden bij de AX-export*</span><span class="sxs-lookup"><span data-stu-id="735eb-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="735eb-126">Volg deze stappen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="735eb-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="735eb-127">Meld u aan bij de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="735eb-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="735eb-128">Verwijder op de pagina **Azure Active Directory-toepassingen** de **DtAppID**-client en voeg deze vervolgens opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="735eb-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Lijst met Azure AD-toepassingen](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="735eb-130">Fouten met verwijzing naar zichzelf tijdens initiële synchronisatie</span><span class="sxs-lookup"><span data-stu-id="735eb-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="735eb-131">Er wordt mogelijk een foutbericht van de volgende strekking weergegeven als een van uw toewijzingen naar zichzelf verwijst:</span><span class="sxs-lookup"><span data-stu-id="735eb-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="735eb-132">*Op Leveranciers v2 verschijnt de volgende fout: record-id: nieuwe record, ErrorMessage: Kan de GUID voor het veld niet omzetten: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. De zoekwaarde is niet gevonden: CN-001. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="735eb-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="735eb-133">Dit type fout treedt op tijdens de initiële synchronisatie van toewijzingen met zelfverwijzingen.</span><span class="sxs-lookup"><span data-stu-id="735eb-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="735eb-134">In het vorige voorbeeld verwijst het veld met de factuurrekening naar de leveranciersentiteit.</span><span class="sxs-lookup"><span data-stu-id="735eb-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="735eb-135">U kunt dit probleem verhelpen door de toewijzing twee maal uit te voeren voordat de initiële synchronisatie is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="735eb-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

