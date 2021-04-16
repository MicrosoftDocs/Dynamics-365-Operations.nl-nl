---
title: Algemene problemen oplossen
description: Dit onderwerp bevat informatie voor het oplossen van algemene problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse.
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
ms.openlocfilehash: 8c2ae3368db47363a65e8ecd6317bb0432829802
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748820"
---
# <a name="general-troubleshooting"></a>Algemene problemen oplossen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dit onderwerp bevat informatie voor het oplossen van algemene problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Wanneer u het pakket voor twee keer wegschrijven probeert te installeren met het hulpprogramma Package Deployer, worden er geen beschikbare oplossingen weergegeven

Sommige versies van het hulpprogramma Package Deployer zijn niet compatibel met het oplossingspakket voor twee keer wegschrijven. Als u het pakket wilt installeren, moet u [versie 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) of hoger van het hulpprogramma Package Deployer gebruiken.

Nadat u het hulpprogramma Package Deployer hebt geïnstalleerd, installeert u het oplossingspakket door de volgende stappen uit te voeren.

1. Download het meest recente bestand met het oplossingspakket van Yammer.com. Nadat het zipbestand met het pakket is gedownload, klikt u erop met de rechtermuisknop en selecteert u **Eigenschappen**. Schakel het selectievakje **Deblokkeren** in en selecteer vervolgens **Toepassen**. Als het selectievakje **Deblokkeren** niet wordt weergeven, is het zipbestand al gedeblokkeerd en kunt u deze stap overslaan.

    ![Dialoogvenster Eigenschappen](media/unblock_option.png)

2. Pak het zipbestand uit en kopieer alle bestanden in de map **Dynamics365FinanceAndOperationsCommon. PackageDeployer.2.0.438**.

    ![Inhoud van de map Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. Plak alle gekopieerde bestanden in de map **Tools** van het hulpprogramma Package Deployer. 
4. Voer **PackageDeployer.exe** uit om de Dataverse-omgeving te selecteren en de oplossingen te installeren.

    ![Inhoud van de map Tools](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Dataverse om foutdetails weer te geven

**Vereiste rol om het traceerlogboek in te schakelen en fouten weer te geven:** systeembeheerder

Voer de volgende stappen uit om het traceerlogboek in te schakelen.

1. Meld u aan bij de modelgestuurde-app in Dynamics 365, open de pagina **Instellingen** en selecteer vervolgens onder **Systeem** de optie **Beheer**.
2. Selecteer op de pagina **Beheer** de optie **Systeeminstellingen**.
3. Ga naar het tabblad **Aanpassen** en selecteer in de kolom **Traceren van invoegtoepassing en aangepaste werkstroomactiviteit** **Alle** om het traceerlogboek voor invoegtoepassingen in te schakelen. Als u traceerlogboeken alleen wilt vastleggen wanneer er uitzonderingen optreden, kunt u in plaats daarvan **Uitzondering** selecteren.


Voer de volgende stappen uit om het traceerlogboek weer te geven.

1. Meld u aan bij de modelgestuurde-app in Dynamics 365, open de pagina **Instellingen** en selecteer vervolgens onder **Systeem** de optie **Traceerlogboek invoegtoepassing**.
2. Zoek de traceerlogboeken waarvoor de kolom **Type naam** is ingesteld op **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Dubbelklik op een item om het volledige logboek weer te geven en controleer vervolgens op het sneltabblad **Uitvoering** de tekst **Bericht blokkeren**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>De modus Foutopsporing inschakelen om live synchronisatieproblemen in Finance and Operations-apps op te lossen

**Vereiste rol om de fouten weer te geven**: fouten van systeembeheerder met Twee keer wegschrijven die zijn ontstaan in Dataverse, kunnen worden weergegeven in de Finance and Operations-app. In sommige gevallen is de volledige tekst van het foutbericht niet beschikbaar omdat het bericht te lang is of persoonlijke identificatie gegevens (PII) bevat. U kunt uitgebreide logboekregistratie voor fouten inschakelen door de volgende stappen uit te voeren.

1. Alle projectconfiguraties in Finance and Operations-apps hebben een eigenschap **IsDebugMode** in de tabel **DualWriteprojectConfiguration**. Open de tabel **DualWriteProjectConfiguration** met de Excel-invoegtoepassing.

    > [!TIP]
    > Een eenvoudige manier om de tabel te openen is om de **ontwerp** modus in de Excel-invoegtoepassing in te schakelen en vervolgens **DualWriteprojectConfigurationEntity** toe te voegen aan het werkblad. Zie [Tabelgegevens in Excel openen en bijwerken via de Excel-invoegtoepassing](../../office-integration/use-excel-add-in.md) voor meer informatie.

2. Stel de eigenschap **IsDebugMode** in op **Ja** voor het project.
3. Voer het scenario uit dat fouten genereert.
4. De uitgebreide logboeken zijn beschikbaar in de tabel DualWriteErrorLog. Als u gegevens wilt opzoeken in de tabelbrowser, gebruikt u de volgende URL (vervang **XXX** waar van toepassing):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Synchronisatiefouten controleren op de virtuele machine voor de Finance and Operations-app

**Vereiste rol om de fouten weer te geven:** systeembeheerder

1. Meld u aan bij Microsoft Dynamics LCS (LifeCycle Services).
2. Open het LCS-project dat u hebt gekozen voor tests met twee keer wegschrijven.
3. Selecteer de tegel **Cloudomgevingen**.
4. Gebruik extern bureaublad om u aan te melden bij de virtuele machine (VM) voor de Finance and Operations-app. Gebruik het lokale account dat wordt weergegeven in LCS.
5. Open Logboeken.
6. Selecteer **Logboeken Toepassingen en Services \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationeel**.
7. Bekijk de lijst met recente fouten.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Een Dataverse-omgeving ontkoppelen en een andere omgeving uit een Finance and Operations-app koppelen

**De vereiste rol om de omgeving te ontkoppelen:** systeembeheerder voor de Finance and Operations-app of Dataverse.

1. Meld u aan bij de Finance and Operations-app.
2. Ga naar **Werkruimten \> Gegevensbeheer** en selecteer de tegel **Twee keer wegschrijven**.
3. Selecteer alle actieve toewijzingen en vervolgens **Stoppen**.
4. Selecteer **Koppeling met omgeving verbreken**.
5. Selecteer **Ja** om de bewerking te bevestigen.

U kunt nu een nieuwe omgeving koppelen.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Informatieformulier met verkooporderregel kan niet worden weergegeven 

Wanneer u een verkooporder maakt in Dynamics 365 Sales, kunt u door te klikken op **+ Producten toevoegen** worden omgeleid naar het formulier Dynamics 365 Project Operations-orderregel. U kunt vanuit dat formulier niet het **informatieformulier** over de verkooporderregel weergeven. De optie voor **informatie** wordt niet weergegeven in de vervolgkeuzelijst onder **Nieuwe orderregel**. Dit gebeurt omdat Project Operations in uw omgeving is geïnstalleerd.

Ga als volgt te werk om de optie voor het formulier **Informatie** opnieuw in te schakelen:
1. Ga naar de tabel **Orderregel**.
2. Zoek het formulier **Informatie** onder het knooppunt met formulieren. 
3. Selecteer het formulier **Informatie** en klik op **Beveiligingsrollen inschakelen**. 
4. Wijzig de beveiligingsinstelling in **Weergeven aan iedereen**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]