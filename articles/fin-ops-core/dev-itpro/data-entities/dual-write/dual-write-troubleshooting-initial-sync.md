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
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Problemen tijdens eerste synchronisatie oplossen

[!include [banner](../../includes/banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service. Dit onderwerp bevat specifieke informatie over het oplossen van problemen die kunnen optreden bij de eerste synchronisatie. 

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Controleren op initiële synchronisatiefouten in een Finance and Operations-app

Nadat u de toewijzingssjablonen hebt ingeschakeld, moet de status van de toewijzingen **Wordt uitgevoerd** zijn. Als de status **Wordt niet uitgevoerd**, zijn er fouten opgetreden tijdens de initiële synchronisatie. Als u de fouten wilt weergeven , selecteert u het tabblad **Details initiële synchronisatie** op de pagina **Twee keer wegschrijven**.

![Tabblad Details initiële synchronisatie](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>U kunt de initiële synchronisatie niet voltooien: 400 Ongeldige aanvraag

**Vereiste rol om de fout op te lossen:** systeembeheerder

Het volgende foutbericht kan worden weergegeven wanneer u probeert de toewijzing en de initiële synchronisatie uit te voeren:

*De externe server heeft een fout geretourneerd: (400 Ongeldige aanvraag.), er is een fout opgetreden bij de AX-export*

Hier volgt een voorbeeld van de volledige foutmelding.

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

Als deze fout voortdurend optreedt en u de eerste synchronisatie niet kunt voltooien, voert u de volgende stappen uit om het probleem op te lossen.

1. Meld u aan bij de virtuele machine (VM) voor de Finance and Operations-app.
2. Open Microsoft Management Console. 
3. Controleer in het deelvenster **Services** of de Microsoft Dynamics 365-raamwerkservice voor gegevens importeren/exporteren wordt uitgevoerd. Start de service opnieuw als deze is gestopt omdat de initiële synchronisatie dat vereist.

## <a name="initial-synchronization-error-403-forbidden"></a>Fout bij initiële synchronisatie: 403 Verboden

Mogelijk wordt het volgende foutbericht weergegeven tijdens de initiële synchronisatie:

*(\[Verboden\], De externe server heeft een fout geretourneerd: (403) Verboden.), er is een fout opgetreden bij de AX-export*

Volg deze stappen om het probleem op te lossen.

1. Meld u aan bij de Finance and Operations-app.
2. Verwijder op de pagina **Azure Active Directory-toepassingen** de **DtAppID**-client en voeg deze vervolgens opnieuw toe.

![Lijst met Azure AD-toepassingen](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a>Fouten met verwijzing naar zichzelf tijdens initiële synchronisatie

Er wordt mogelijk een foutbericht van de volgende strekking weergegeven als een van uw toewijzingen naar zichzelf verwijst:

*Op Leveranciers v2 verschijnt de volgende fout: record-id: nieuwe record, ErrorMessage: Kan de GUID voor het veld niet omzetten: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. De zoekwaarde is niet gevonden: CN-001. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Dit type fout treedt op tijdens de initiële synchronisatie van toewijzingen met zelfverwijzingen. In het vorige voorbeeld verwijst het veld met de factuurrekening naar de leveranciersentiteit.

U kunt dit probleem verhelpen door de toewijzing twee maal uit te voeren voordat de initiële synchronisatie is geslaagd.

