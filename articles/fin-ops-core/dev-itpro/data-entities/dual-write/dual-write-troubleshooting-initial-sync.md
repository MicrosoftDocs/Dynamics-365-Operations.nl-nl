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
ms.openlocfilehash: a2f0e0cbf0f8710dc020a48506775fa28df9c2d2
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744632"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Problemen tijdens eerste synchronisatie oplossen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse. Dit onderwerp bevat specifieke informatie over het oplossen van problemen die kunnen optreden bij de eerste synchronisatie.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Controleren op initiële synchronisatiefouten in een Finance and Operations-app

Nadat u de toewijzingssjablonen hebt ingeschakeld, moet de status van de toewijzingen **Wordt uitgevoerd** zijn. Als de status **Wordt niet uitgevoerd**, zijn er fouten opgetreden tijdens de initiële synchronisatie. Als u de fouten wilt weergeven , selecteert u het tabblad **Details initiële synchronisatie** op de pagina **Twee keer wegschrijven**.

![Fout op het tabblad Details initiële synchronisatie](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>U kunt de initiële synchronisatie niet voltooien: 400 Ongeldige aanvraag

**Vereiste rol om de fout op te lossen:** systeembeheerder

Het volgende foutbericht kan worden weergegeven wanneer u probeert de toewijzing en de initiële synchronisatie uit te voeren:

*(\[Ongeldige aanvraag\], De externe server heeft een fout geretourneerd: (400) Ongeldige aanvraag.), er is een fout opgetreden bij de AX-export*

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

![DtAppID-client in de lijst met Azure AD-toepassingen](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Fouten met verwijzing naar zichzelf of circulaire verwijzingen tijdens initiële synchronisatie

Er wordt mogelijk een foutberichten als een van uw toewijzingen naar zichzelf verwijst of kringverwijzingen bevat. De fouten vallen in deze categorieën:

- [Fouten in de tabeltoewijzing Vendors V2–to–msdyn_vendors](#error-vendor-map)
- [Fouten in de tabeltoewijzing Customers V3–to–Accounts](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Fouten in de tabeltoewijzing Vendors V2–to–msdyn_vendors oplossen

U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Leveranciers v2** aan **msdyn\_vendors**, als de tabellen bestaande rijen hebben met waarden in de kolommen **PrimaryContactPersonId** en **InvoiceVendorAccountNumber**. Deze fouten treden op omdat **InvoiceVendorAccountNumber** een kolom is die naar zichzelf verwijst en **PrimaryContactPersonId** een kringverwijzing is in de leverancierstoewijzing.

De foutberichten die worden weergegeven, hebben de volgende vorm.

*Kan de GUID voor het veld niet omzetten: \<field\>. De zoekopdracht is niet gevonden: \<value\>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Hieronder volgen een aantal voorbeelden:

- *Kan de GUID voor het veld niet omzetten: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Kan de GUID voor het veld niet omzetten: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber De zoekopdracht is niet gevonden: V24-1. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Als rijen in de tabel leverancier waarden hebben in de kolommen **PrimaryContactPersonId** en **InvoiceVendorAccountNumber**, volgt u deze stappen om de initiële synchronisatie te voltooien.

1. Verwijder in de Finance and Operations-app de kolommen **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** uit de toewijzing en sla de toewijzing op.

    1. Selecteer op de pagina voor de toewijzing van twee keer wegschrijven voor **Leveranciers v2 (msdyn\_vendors)**, op het tabblad **Ttabeltoewijzingen** in het linkerfilter de optie **Finance and Operations apps.Vendors V2**. Selecteer in het rechterfilter **Sales.Vendor**.
    2. Zoek naar **primarycontactperson** om de bronkolom **PrimaryContactPersonId** te vinden.
    3. Selecteer **Acties** en vervolgens **Verwijderen**.

        ![De kolom PrimaryContactPersonId verwijderen](media/vend_selfref3.png)

    4. Herhaal deze stappen om de kolom **InvoiceVendorAccountNumber** te verwijderen.

        ![De kolom InvoiceVendorAccountNumber verwijderen](media/vend-selfref4.png)

    5. Sla de wijzigingen in de toewijzing op.

2. Schakel het bijhouden van wijzigingen uit voor de tabel **Leveranciers v2**.

    1. Selecteer in de werkruimte **Gegevensbeheer** de tegel **Gegevenstabellen**.
    2. Selecteer de tabel **Leveranciers V2**.
    3. Selecteer in het actievenster **Opties** en selecteer **Wijzigingen bijhouden**.

        ![De optie Wijzigingen bijhouden selecteren](media/selfref_options.png)

    4. Selecteer **Wijzigingen bijhouden uitschakelen**.

        ![Selecteer Wijzigingen bijhouden uitschakelen](media/selfref_tracking.png)

3. Voer de initiële synchronisatie opnieuw uit van de toewijzing **Leveranciers v2 (msdyn\_vendors)**. De eerste synchronisatie moet zonder fouten worden uitgevoerd.
4. Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**. U moet deze toewijzing synchroniseren als u de kolom voor de primaire contactpersoon in de tabel leveranciers wilt synchroniseren, omdat initiële synchronisatie ook moet worden uitgevoerd voor de rijen voor contactpersonen.
5. Voeg de kolommen **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** weer toe aan de toewijzing **Leveranciers v2 (msdyn\_vendors)** en sla de toewijzing op.
6. Voer de initiële synchronisatie opnieuw uit van de toewijzing **Leveranciers v2 (msdyn\_vendors)**. Alle rijen worden gesynchroniseerd omdat het bijhouden van wijzigingen is uitgeschakeld.
7. Schakel het bijhouden van wijzigingen weer in voor de tabel **Leveranciers v2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Fouten oplossen in de tabeltoewijzing Klanten V3–to–Accounts

U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Klanten v3** aan **Accounts**, als de tabellen bestaande rijen hebben met waarden in de kolommen **ContactPersonID** en **InvoiceAccount**. Deze fouten treden op omdat **InvoiceAccount** een kolom is die naar zichzelf verwijst en **ContactPersonID** een kringverwijzing in de leverancierstoewijzing is.

De foutberichten die worden weergegeven, hebben de volgende vorm.

*Kan de GUID voor het veld niet omzetten: \<field\>. De zoekopdracht is niet gevonden: \<value\>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Hieronder volgen een aantal voorbeelden:

- *Kan de GUID voor het veld niet omzetten: primarycontactid.msdyn\_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Kan de GUID voor het veld niet omzetten: msdyn\_billingaccount.accountnumber. De zoekopdracht is niet gevonden: 1206-1. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Als rijen in de tabel klant waarden hebben in de kolommen **ContactPersonID** en **InvoiceAccount**, volgt u deze stappen om de initiële synchronisatie te voltooien. U kunt deze methode gebruiken voor alle standaardtabellen zoals **accounts** en **contactpersonen**.

1. Verwijder in de Finance and Operations-app de kolommen **ContactPersonID** en **InvoiceAccount** uit de toewijzing **Klanten V3 (accounts)** en sla de toewijzing op.

    1. Selecteer op de pagina voor de toewijzing van twee keer wegschrijven voor **Klanten v3 (accounts)** op het tabblad **Tabeltoewijzingen** in het linkerfilter de optie **Finance and Operations app.Customers V3**. Selecteer in het rechterfilter **Dataverse.Account**.
    2. Zoek naar **contactperson** om de bronkolom **ContactPersonID** te vinden.
    3. Selecteer **Acties** en vervolgens **Verwijderen**.

        ![De kolom ContactPersonID verwijderen](media/cust_selfref3.png)

    4. Herhaal deze stappen om de kolom **InvoiceAccount** te verwijderen.

        ![De kolom InvoiceAccount verwijderen](media/cust_selfref4.png)

    5. Sla de wijzigingen in de toewijzing op.

2. Schakel het bijhouden van wijzigingen uit voor de tabel **Klanten v3**.

    1. Selecteer in de werkruimte **Gegevensbeheer** de tegel **Gegevenstabellen**.
    2. Selecteer de tabel **Klanten V3**.
    3. Selecteer in het actievenster **Opties** en selecteer **Wijzigingen bijhouden**.

        ![De optie Wijzigingen bijhouden selecteren](media/selfref_options.png)

    4. Selecteer **Wijzigingen bijhouden uitschakelen**.

        ![Selecteer Wijzigingen bijhouden uitschakelen](media/selfref_tracking.png)

3. Voer de eerste synchronisatie opnieuw uit voor de toewijzing **Klanten V3 (Accounts)**. De eerste synchronisatie moet zonder fouten worden uitgevoerd.
4. Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**.

    > [!NOTE]
    > Er zijn twee toewijzingen met dezelfde naam. Selecteer de toewijzing met de volgende omschrijving op het tabblad **Details**: **Sjabloon voor twee keer wegschrijven voor sync tussen FO.CDS Vendor Contacts V2 to CDS.Contacts. Vereist nieuw pakket \[Dynamics365SupplyChainExtended\].**

5. Voeg de kolommen **InvoiceAccount** en **ContactPersonId** weer toe aan de toewijzing **Klanten V3 (Accounts)** en sla de toewijzing op. Nu maken de kolommen **InvoiceAccount** en **ContactPersonId** weer deel uit van de live synchronisatiemodus. In de volgende stap voert u de initiële synchronisatie uit voor deze kolommen.
6. Voer de initiële synchronisatie opnieuw uit voor de toewijzing **Klanten V3 (Accounts)**. Omdat het bijhouden van wijzigingen is uitgeschakeld, worden de gegevens voor **InvoiceAccount** en **ContactPersonId** uit de Finance and Operations-app gesynchroniseerd met Dataverse.
7. Voor het synchroniseren van de gegevens voor **InvoiceAccount** en **ContactPersonId** van Dataverse met de Finance and Operations-app, gebruikt u een gegevensintegratieproject.

    1. Maak in Power Apps een gegevensintegratieproject tussen de tabellen **Sales.Account** en **Finance and Operations apps.Customers V3**. De gegevensrichting moet van Dataverse naar de Finance and Operations-app gaan. Omdat **InvoiceAccount** een nieuw kenmerk is voor twee keer wegschrijven, wilt u mogelijk de initiële synchronisatie voor dit kenmerk overslaan. Zie voor meer informatie [Gegevens integreren in Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).

        In de volgende afbeelding ziet u een project waarmee **CustomerAccount** en **ContactPersonId** worden bijgewerkt.

        ![Gegevensintegratieproject voor het bijwerken van CustomerAccount en ContactPersonId](media/cust_selfref6.png)

    2. Voeg de bedrijfscriteria toe in het filter aan de kant van Dataverse, zodat alleen de rijen die aan de filtercriteria voldoen, in de app Finance and Operations worden bijgewerkt. Klik op de filterknop om een filter toe te voegen. Voeg vervolgens In het dialoogvenster **Query bewerken** een filterquery als **\_msdyn\_company\_value eq '\<guid\>'** toe. 

        > [OPMERKING] Als de filterknop niet aanwezig is, maakt u een ondersteuningsticket om aan het gegevensintegratieteam te vragen om de filtermogelijkheid voor uw tenant in te schakelen.

        Als u geen filterquery voor **\_msdyn\_company\_value** invoert, worden alle rijen gesynchroniseerd.

        ![Een filterquery toevoegen](media/cust_selfref7.png)

    De initiële synchronisatie van de rijen is nu voltooid.

8. Schakel het bijhouden van wijzigingen in voor de tabel **Klanten V3** in de Finance and Operations-app.
