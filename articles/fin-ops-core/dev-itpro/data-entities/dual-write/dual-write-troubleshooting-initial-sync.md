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

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Fouten met verwijzing naar zichzelf of circulaire verwijzingen tijdens initiële synchronisatie

Er wordt mogelijk een foutberichten als een van uw toewijzingen naar zichzelf verwijst of kringverwijzingen bevat. De fouten vallen in deze categorieën:

- [Entiteitstoewijzing van Leveranciers V2 aan msdyn_vendors](#error-vendor-map)
- [Entiteitstoewijzing Klanten V3 aan Accounts](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Een fout in Leveranciers v2 omzetten in een msdyn_vendors-entiteitstoewijzing

U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Leveranciers v2** aan **msdyn_vendors**, als de entiteiten bestaande records hebben met waarden in de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber**. De reden is dat **InvoiceVendorAccountNumber** een veld is dat naar zichzelf verwijst en dat **PrimaryContactPersonId** een kringverwijzing in de leverancierstoewijzing is.

*Kan de GUID voor het veld niet omzetten: <field>. De zoekopdracht is niet gevonden: <value>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity> ?$select=<field>&$filter=<field> eq <value>*

Hier volgen enkele voorbeelden:

- *Kan de GUID voor het veld niet omzetten: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Kan de GUID voor het veld niet omzetten: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. De zoekopdracht is niet gevonden: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Als u records met waarden in deze velden in de entiteit voor de leverancier hebt, volgt u de stappen in de volgende sectie om de initiële synchronisatie te voltooien.

1. Verwijder in de app Finance and Operations de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** uit de toewijzing en sla de wijzigingen op.

    1. Ga naar de pagina voor de toewijzing van twee keer wegschrijven voor **Leveranciers v2 (msdyn_vendors)** en selecteer het tabblad **Entiteits toewijzingen**. Selecteer in het linkerfilter de optie **Finance and Operations apps.Vendors V2**. Selecteer in het rechterfilter **Sales.Vendor**.

    2. Zoek naar **primarycontactperson** om het bronveld **PrimaryContactPersonId** te vinden.
    
    3. Klik op de knop **Acties** en selecteer **Verwijderen**.
    
        ![Zelf- of kringverwijzing 3](media/vend_selfref3.png)
    
    4. Herhaal dit om het veld **InvoiceVendorAccountNumber** te verwijderen.
    
        ![Zelf- of kringverwijzing 4](media/vend-selfref4.png)
    
    5. Sla de wijzigingen in de toewijzing op.

2. Schakel het bijhouden van wijzigingen uit voor de entiteit **Leveranciers v2**.

    1. Navigeer naar **Gegevens beheer \> Gegevensentiteiten**.
    
    2. Selecteer de entiteit **Leveranciers V2**.
    
    3. Klik op **Opties** in de menubalk en wijzig vervolgens **Wijzigingen bijhouden**.
    
        ![Zelf- of kringverwijzing 5](media/selfref_options.png)
    
    4. Klik op **Wijzigingen bijhouden uitschakelen**.
    
        ![Zelf- of kringverwijzing 6](media/selfref_tracking.png)

3. Voer de eerste synchronisatie uit van de toewijzing van **Leveranciers v2 (msdyn_vendors)**. De eerste synchronisatie moet zonder fouten worden uitgevoerd.

4. Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**. U moet deze toewijzing synchroniseren als u het veld voor de primaire contactpersoon in de entiteit leveranciers wilt synchroniseren omdat de records voor contactpersonen ook als eerste moeten worden gesynchroniseerd.

5. Voeg de velden **PrimaryContactPersonId** en **InvoiceVendorAccountNumber** weer toe aan de toewijzing **Leveranciers v2 (msdyn_vendors)** en sla de toewijzing op.

6. Voer de eerste synchronisatie opnieuw uit van de toewijzing van **Leveranciers v2 (msdyn_vendors)**. Alle records worden gesynchroniseerd omdat het bijhouden van wijzigingen is uitgeschakeld.

7. Schakel het bijhouden van wijzigingen in voor de entiteit **Leveranciers v2**.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Een fout in Klanten v3 omzetten naar een entiteitstoewijzing voor Accounts

U kunt de volgende initiële synchronisatiefouten tegenkomen bij de toewijzing van **Klanten v3** aan **Accounts**, als de entiteiten bestaande records hebben met waarden in de velden **ContactPersonID** en **InvoiceAccount**. De reden is dat **InvoiceAccount** een veld is dat naar zichzelf verwijst en dat **ContactPersonID** een kringverwijzing in de leverancierstoewijzing is.

*Kan de GUID voor het veld niet omzetten: <field>. De zoekopdracht is niet gevonden: <value>. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity> ?$select=<field>&$filter=<field> eq <value>*

- *Kan de GUID voor het veld niet omzetten: primarycontactid.msdyn_contactpersonid. De zoekopdracht is niet gevonden: 000056. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Kan de GUID voor het veld niet omzetten: msdyn_billingaccount.accountnumber. De zoekopdracht is niet gevonden: 1206-1. Probeer deze URL's om te controleren of de verwijzingsgegevens bestaan: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Als u records met waarden in deze velden in de entiteit voor de klant hebt, volgt u de stappen in de volgende sectie om de initiële synchronisatie te voltooien. U kunt deze methode gebruiken voor alle standaardentiteiten zoals accounts en contactpersonen.

1. Verwijder in de app Finance and Operations de velden **ContactPersonID** en **InvoiceAccount** uit de toewijzing **Klanten V3 (accounts)** en sla de toewijzing op.

    1. Ga naar de pagina voor de toewijzing van twee keer wegschrijven voor **Klanten v2 (accounts)** en selecteer het tabblad **Entiteits toewijzingen**. Selecteer in het linkerfilter de optie **Finance and Operations app.Customers V3**. Selecteer in het rechterfilter **Common Data Service.Account**.

    2. Zoek naar **contactperson** om het bronveld **ContactPersonID** te vinden.
    
    3. Klik op de knop **Acties** en selecteer **Verwijderen**.
    
        ![Zelf- of kringverwijzing 3](media/cust_selfref3.png)
    
    4. Herhaal dit om het veld **InvoiceAccount** te verwijderen.
    
        ![Zelf- of kringverwijzing](media/cust_selfref4.png)
    
    5. Sla de wijzigingen in de toewijzing op.

2. Schakel het bijhouden van wijzigingen uit voor de entiteit **Klanten v3**.

    1. Navigeer naar **Gegevens beheer \> Gegevensentiteiten**.
    
    2. Selecteer de entiteit **Klanten V3**.
    
    3. Klik op **Opties** in de menubalk en wijzig vervolgens **Wijzigingen bijhouden**.
    
        ![Zelf- of kringverwijzing 5](media/selfref_options.png)
    
    4. Klik op **Wijzigingen bijhouden uitschakelen**.
    
        ![Zelf- of kringverwijzing 6](media/selfref_tracking.png)

3. Voer de eerste synchronisatie uit voor de toewijzing **Klanten V3 (Accounts)**. De eerste synchronisatie moet zonder fouten worden uitgevoerd.

4. Voer de eerste synchronisatie uit voor de toewijzing **CDS Contactpersonen V2 (contacts)**. Er zijn 2 toewijzingen met dezelfde naam. Selecteer de naam met de omschrijving **Sjabloon voor twee keer wegschrijven voor sync tussen FO.CDS Vendor Contacts V2 en CDS.Contacts. Vereist nieuw pakket \[Dynamics365SupplyChainExtended\].** op het tabblad **Details** van de toewijzing.

5. Voeg de velden **InvoiceAccount** en **ContactPersonId** weer toe uit de toewijzing **Klanten V3 (Accounts)** en sla de toewijzing op. Nu maken de velden **InvoiceAccount** en **ContactPersonId** weer deel uit van de live synchronisatiemodus. In de volgende stap voltooit u de initiële synchronisatie voor deze velden.

6. Voer de eerste synchronisatie opnieuw uit voor de toewijzing **Klanten V3 (Accounts)**. Omdat het bijhouden van wijzigingen is uitgeschakeld, synchroniseert u de gegevens voor **InvoiceAccount** en **ContactPersonId** van de Finance and Operations-app met Common Data Service.

7. Voor het synchroniseren van de gegevens voor **InvoiceAccount** en **ContactPersonId** van Common Data Service met Finance and Operations, gebruikt u een gegevensintegratieproject.

    1. Maak in Power Apps een gegevensintegratieproject tussen de entiteiten **Sales.Account** en **Finance and Operations apps.Customers V3**. De gegevensrichting moet van Common Data Service naar de Finance and Operations-app gaan.  Omdat **InvoiceAccount** een nieuw kenmerk is voor twee keer wegschrijven, wilt u mogelijk de initiële synchronisatie voor dit kenmerk overslaan. Zie voor meer informatie [Gegevens integreren in Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        In de volgende afbeelding ziet u een project waarmee **CustomerAccount** en **ContactPersonId** worden bijgewerkt.

        ![Zelf- of kringverwijzing](media/cust_selfref6.png)

    2. Voeg de bedrijfscriteria toe in het filter aan de kant van Common Data Service, omdat alleen de records die aan filtercriteria voldoen, in de app Finance and Operations worden bijgewerkt. Klik op het filterpictogram om een filter toe te voegen. In het dialoogvenster **Query bewerken** kunt u een filterquery als **_msdyn_company_value eq '\<guid\>'** toevoegen. Als het filterpictogram niet aanwezig is, maakt u een ondersteuningsticket om aan het gegevensintegratieteam te vragen om de filtermogelijkheid voor uw tenant in te schakelen. Als u geen filterquery voor **_msdyn_company_value** invoert, worden alle records gesynchroniseerd.

        ![Zelf- of kringverwijzing](media/cust_selfref7.png)

        Hiermee is de initiële synchronisatie van de records voltooid.

8. Schakel het bijhouden van wijzigingen in voor de entiteit **Klanten V3** in de Finance and Operations-app.

