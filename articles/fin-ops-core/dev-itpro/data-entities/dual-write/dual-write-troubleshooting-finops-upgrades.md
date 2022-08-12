---
title: Problemen met upgrades van apps voor financiën en bedrijfsactiviteiten oplossen
description: Dit artikel bevat informatie over het oplossen van problemen met betrekking tot upgrades van apps voor financiën en bedrijfsactiviteiten.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b75034cbc8ca7a24472cfec1ad93d3dfef4a8fdc
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111135"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Problemen met upgrades van apps voor financiën en bedrijfsactiviteiten oplossen

[!include [banner](../../includes/banner.md)]





Dit artikel bevat informatie voor het oplossen van problemen met de integratie van Twee keer wegschrijven tussen apps voor financiën en bedrijfsactiviteiten en Dataverse. Dit onderwerp bevat met name informatie over het oplossen van problemen met betrekking tot upgrades van apps voor financiën en bedrijfsactiviteiten.

> [!IMPORTANT]
> In sommige problemen die in dit artikel worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="database-synchronization-errors"></a>Fouten met databasesynchronisatie

**Vereiste rol om de fout op te lossen:** systeembeheerder

Er wordt mogelijk een foutbericht van de volgende strekking weergegeven wanneer u probeert de tabel **DualWriteProjectConfiguration** te gebruiken om een app voor financiën en bedrijfsactiviteiten bij te werken naar Platform update 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Volg deze stappen om het probleem op te lossen.

1. Meld u aan bij de virtuele machine (VM) voor de app voor financiën en bedrijfsactiviteiten.
2. Open Visual Studio als beheerder en open de Application Object Tree (AOT).
3. Zoek naar **DualWriteprojectConfiguration**.
4. Klik in de AOT met de rechtermuisknop op **DualWriteprojectConfiguration** en selecteer **Toevoegen aan nieuw project**. Selecteer **OK** om het nieuwe project te maken waarin standaardopties worden gebruikt.
5. Klik in Solution Explorer met de rechtermuisknop op **Projecteigenschappen** en stel **Database synchroniseren op build** in op **True**.
6. Maak het project en controleer of de build succesvol is.
7. Selecteer in het menu **Dynamics 365** de optie **Database synchroniseren**.
8. Selecteer **Synchroniseren** om een volledige databasesynchronisatie uit te voeren.
9. Nadat de synchronisatie van de volledige database is geslaagd, voert u de synchronisatiestap voor de Microsoft Dynamics-database in Lifecycle Services (LCS) opnieuw uit en gebruikt u de handmatige upgradescripts als dat van toepassing is, zodat u kunt doorgaan met de update.

## <a name="missing-table-columns-issue-on-maps"></a>Probleem met ontbrekende tabelkolommen in toewijzingen

**Vereiste rol om de fout op te lossen:** systeembeheerder

Op de pagina **Twee keer wegschrijven** kan een foutbericht van de volgende strekking worden weergegeven:

*Ontbrekend bronveld \<field name\> in het schema.*

![Voorbeeld van foutbericht over ontbrekende bronkolommen.](media/error_missing_field.png)

Als u het probleem wilt verhelpen, voert u eerst deze stappen uit om te controleren of de kolommen in de tabel aanwezig zijn.

1. Meld u aan bij de virtuele machine (VM) voor de app voor financiën en bedrijfsactiviteiten.
2. Ga naar **Werkruimten \> Gegevensbeheer**, selecteer de tegel **Raamwerkparameters** en selecteer vervolgens op het tabblad **Tabelinstellingen** de optie **Tabellijst vernieuwen** om de tabellen te vernieuwen.
3. Ga naar **Werkruimten \> Gegevensbeheer**, selecteer het tabblad **Gegevenstabellen** en controleer of de tabel wordt weergegeven. Als de tabel niet wordt weergegeven, meldt u zich aan bij de VM voor de app voor financiën en bedrijfsactiviteiten en controleert u of de tabel beschikbaar is.
4. Open de pagina **Tabeltoewijzing** op de pagina **Twee keer wegschrijven** in de app voor financiën en bedrijfsactiviteiten.
5. Selecteer **Tabellijst vernieuwen** om de kolommen in de tabeltoewijzingen automatisch te vullen.

Als het probleem nog steeds niet is opgelost, voert u de volgende stappen uit.

> [!IMPORTANT]
> Deze stappen begeleiden u bij het verwijderen van een tabel en het toevoegen ervan. U kunt problemen voorkomen door de stappen exact uit te voeren.

1. Ga in de app voor financiën en bedrijfsactiviteiten naar **Werkgebieden \> Gegevensbeheer** en selecteer de tegel **Gegevenstabellen**.
2. Zoek de tabel waarvoor het kenmerk ontbreekt. Klik op **Doeltoewijzing aanpassen** op de werkbalk.
3. Klik in het deelvenster **Fasering aan doel toewijzen** op **Toewijzing genereren**.
4. Open de pagina **Tabeltoewijzing** op de pagina **Twee keer wegschrijven** in de app voor financiën en bedrijfsactiviteiten.
5. Als het kenmerk niet automatisch wordt ingevuld op de toewijzing, voegt u dit handmatig toe door te klikken op de knop **Kenmerk toevoegen** en vervolgens op **Opslaan**. 
6. Selecteer de toewijzing en klik op **Uitvoeren**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
