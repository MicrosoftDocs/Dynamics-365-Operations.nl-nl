---
title: Problemen oplossen met betrekking tot upgrades van Finance and Operations-apps
description: Dit onderwerp bevat informatie over het oplossen van problemen met betrekking tot upgrades van Finance and Operations-apps.
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
ms.openlocfilehash: c76b35ed3af766f42484a118a4a0407d969b5240
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683594"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Problemen oplossen met betrekking tot upgrades van Finance and Operations-apps

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse. Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot upgrades van Finance and Operations-apps.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="database-synchronization-errors"></a>Fouten met databasesynchronisatie

**Vereiste rol om de fout op te lossen:** systeembeheerder

Er wordt mogelijk een foutbericht van de volgende strekking weergegeven wanneer u probeert de entiteit **DualWriteprojectConfiguration** te gebruiken om een Finance and Operations-app bij te werken naar Platform update 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Volg deze stappen om het probleem op te lossen.

1. Meld u aan bij de virtuele machine (VM) voor de Finance and Operations-app.
2. Open Visual Studio als beheerder en open de Application Object Tree (AOT).
3. Zoek naar **DualWriteprojectConfiguration**.
4. Klik in de AOT met de rechtermuisknop op **DualWriteprojectConfiguration** en selecteer **Toevoegen aan nieuw project**. Selecteer **OK** om het nieuwe project te maken waarin standaardopties worden gebruikt.
5. Klik in Solution Explorer met de rechtermuisknop op **Projecteigenschappen** en stel **Database synchroniseren op build** in op **True**.
6. Maak het project en controleer of de build succesvol is.
7. Selecteer in het menu **Dynamics 365** de optie **Database synchroniseren**.
8. Selecteer **Synchroniseren** om een volledige databasesynchronisatie uit te voeren.
9. Nadat de synchronisatie van de volledige database is geslaagd, voert u de synchronisatiestap voor de Microsoft Dynamics-database in Lifecycle Services (LCS) opnieuw uit en gebruikt u de handmatige upgradescripts als dat van toepassing is, zodat u kunt doorgaan met de update.

## <a name="missing-entity-fields-issue-on-maps"></a>Problemen met ontbrekende entiteitsvelden in toewijzingen

**Vereiste rol om de fout op te lossen:** systeembeheerder

Op de pagina **Twee keer wegschrijven** kan een foutbericht van de volgende strekking worden weergegeven:

*Ontbrekend bronveld \<field name\> in het schema.*

![Voorbeeld van foutbericht met ontbrekende bronvelden](media/error_missing_field.png)

Als u het probleem wilt verhelpen, voert u eerst deze stappen uit om te controleren of de velden in de entiteit aanwezig zijn.

1. Meld u aan bij de VM voor de Finance and Operations-app.
2. Ga naar **Werkruimten \> Gegevensbeheer**, selecteer de tegel **Raamwerkparameters** en selecteer vervolgens op het tabblad **Tabelinstellingen** de optie **Entiteitslijst vernieuwen** om de tabellen te vernieuwen.
3. Ga naar **Werkruimten \> Gegevensbeheer**, selecteer het tabblad **Gegevenstabellen** en controleer of de entiteit wordt weergegeven. Als de entiteit niet wordt weergegeven, meldt u zich aan bij de VM voor de Finance and Operations-app en controleert u of de entiteit beschikbaar is.
4. Open de pagina **Tabeltoewijzing** op de pagina **Twee keer wegschrijven** in de Finance and Operations-app.
5. Selecteer **Entiteitslijst vernieuwen** om de velden in de tabeltoewijzingen automatisch te vullen.

Als het probleem nog steeds niet is opgelost, voert u de volgende stappen uit.

> [!IMPORTANT]
> Deze stappen begeleiden u bij het verwijderen van een entiteit en het toevoegen ervan. U kunt problemen voorkomen door de stappen exact uit te voeren.

1. Ga in de Finance and Operations-app naar **Werkruimten \> Gegevensbeheer** en selecteer de tegel **Gegevenstabellen**.
2. Zoek de entiteit waarvoor het kenmerk ontbreekt. Klik op **Doeltoewijzing aanpassen** op de werkbalk.
3. Klik in het deelvenster **Fasering aan doel toewijzen** op **Toewijzing genereren**.
4. Open de pagina **Tabeltoewijzing** op de pagina **Twee keer wegschrijven** in de Finance and Operations-app.
5. Als het kenmerk niet automatisch wordt ingevuld op de toewijzing, voegt u dit handmatig toe door te klikken op de knop **Kenmerk toevoegen** en vervolgens op **Opslaan**. 
6. Selecteer de toewijzing en klik op **Uitvoeren**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]