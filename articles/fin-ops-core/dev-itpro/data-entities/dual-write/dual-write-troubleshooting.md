---
title: Algemene problemen oplossen
description: Dit onderwerp bevat informatie voor het oplossen van algemene problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: bcedb9f6e8fb15210512ed6a376d4329759593e4
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781169"
---
# <a name="general-troubleshooting"></a>Algemene problemen oplossen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp bevat informatie voor het oplossen van algemene problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Dataverse om foutdetails weer te geven

**Vereiste rol om het traceerlogboek in te schakelen en fouten weer te geven:** systeembeheerder

Voer de volgende stappen uit om het traceerlogboek in te schakelen.

1. Meld u aan bij de app voor klantbetrokkenheid, open de pagina **Instellignen** en selecteer vervolgens onder **Systeem** de optie **Beheer**.
2. Selecteer op de pagina **Beheer** de optie **Systeeminstellingen**.
3. Ga naar het tabblad **Aanpassen** en selecteer in de kolom **Traceren van invoegtoepassing en aangepaste werkstroomactiviteit** **Alle** om het traceerlogboek voor invoegtoepassingen in te schakelen. Als u traceerlogboeken alleen wilt vastleggen wanneer er uitzonderingen optreden, kunt u in plaats daarvan **Uitzondering** selecteren.


Voer de volgende stappen uit om het traceerlogboek weer te geven.

1. Meld u aan bij de app voor klantbetrokkenheid, open de pagina **Instellingen** en selecteer vervolgens onder **Aanpassing** de optie **Traceerlogboek invoegtoepassing**.
2. Zoek de traceerlogboeken waarvoor de kolom **Type naam** is ingesteld op **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Dubbelklik op een item om het volledige logboek weer te geven en controleer vervolgens op het sneltabblad **Uitvoering** de tekst **Bericht blokkeren**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>De modus Foutopsporing inschakelen om live synchronisatieproblemen in Finance and Operations-apps op te lossen

**Vereiste rol om de fouten weer te geven:** systeembeheerder

Fouten met twee keer wegschrijven die afkomstig zijn uit Dataverse, kunnen worden weergegeven in de  Finance and Operations-app. Neem de volgende stappen om uitgebreide logboekregistratie van de fouten in te schakelen:

1. Alle projectconfiguraties in Finance and Operations-apps hebben een vlag **IsDebugMode** in de tabel **DualWriteprojectConfiguration**.
2. Open de tabel **DualWriteProjectConfiguration** met de Excel-invoegtoepassing. Als u de invoegtoepassing wilt gebruiken, moet u de ontwerpmodus in de Excel-invoegtoepassing van Finance and Operations inschakelen en de **DualWriteprojectConfiguration** aan het werkblad toevoegen. Zie [Entiteitsgegevens weergeven en bijwerken met Excel](../../office-integration/use-excel-add-in.md) voor meer informatie.
3. Stel **IsDebugMode** in op **Ja** in het project.
4. Voer het scenario uit dat fouten genereert.
5. De uitgebreide logboeken worden opgeslagen in de tabel **DualWriteErrorLog**.
6. Als u gegevens wilt opzoeken in de tabelbrowser, gebruikt u de volgende koppeling: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog` en vervangt u indien nodig `999`.
7. Voer de update opnieuw na [KB-4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), die beschikbaar is voor platformupdates 37 en later. Als u deze oplossing hebt geïnstalleerd, worden in de foutopsporingsmodus meer logboeken vastgelegd.  

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

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Netwerktracering inschakelen en opslaan, zodat traceringen kunnen worden gekoppeld aan ondersteuningstickets

Het ondersteuningsteam moet mogelijk netwerktraceringen controleren om bepaalde problemen op te lossen. Voer de volgende stappen uit om een netwerktracering te maken:

### <a name="chrome"></a>Chrome

1. Druk op het geopende tabblad op **F12** of selecteer **Ontwikkelhulpprogramma's** om de ontwikkelhulpprogramma's te openen.
2. Open het tabblad **Netwerk** en typ **integ** in het filtertekstvak.
3. Voer uw scenario uit en bekijk de aanvragen die worden vastgelegd.
4. Klik met de rechtermuisknop op de vermeldingen en selecteer **Alles opslaan als een HAR-bestand met inhoud**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Druk op het geopende tabblad op **F12** of selecteer **Ontwikkelhulpprogramma's** om de ontwikkelhulpprogramma's te openen.
2. Open het tabblad **Netwerk**.
3. Voer uw scenario uit.
4. Selecteer **Opslaan** om de resultaten als HAR-bestand te exporteren.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
