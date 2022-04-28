---
title: Algemene problemen oplossen
description: Dit onderwerp bevat algemene informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen apps voor financiële en bedrijfsactiviteiten en Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/07/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 8b5951f9f40179ca0bf31f5cccf1f05a0f968213
ms.sourcegitcommit: 1843235766b6f8cf950a13a310e9f4f2f53c59a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/07/2022
ms.locfileid: "8554594"
---
# <a name="general-troubleshooting"></a>Algemene problemen oplossen

[!include [banner](../../includes/banner.md)]



Dit onderwerp bevat algemene informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen apps voor financiële en bedrijfsactiviteiten en Dataverse.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Dataverse om foutdetails weer te geven

Traceerlogboeken kunnen nuttig zijn bij het oplossen van problemen met live synchronisatie van twee keer wegschrijven tussen Finance and Operations en Dataverse. De logboeken kunnen specifieke informatie bieden voor de teams die technische ondersteuning bieden voor Dynamics 365. In dit artikel wordt beschreven hoe traceerlogboeken kunnen worden ingeschakeld en hoe u deze kunt weergeven. Traceerlogboeken worden beheerd op de Dynamics 365-pagina instellingen en vereisen beheerdersrechten om te wijzigen en weer te geven. 

**Vereiste rol om het traceerlogboek in te schakelen en fouten weer te geven:** systeembeheerder

### <a name="turn-on-the-trace-log"></a>Het traceerlogboek inschakelen
Voer de volgende stappen uit om het traceerlogboek in te schakelen.

1.  Meld u aan bij Dynamics 365 en selecteer **Instellingen** op de navigatiebalk bovenaan. Klik op de pagina **Beheer** op Systemen.
2.  Klik op de pagina Beheer op de optie **Systeeminstellingen**.
3.  Ga naar het tabblad **Aanpassing** en selecteer in het gedeelte voor het traceren van invoegtoepassing en aangepaste werkstroomactiviteit de optie **Alle** in de vervolgkeuzelijst. In dat geval worden alle activiteiten getraceerd en wordt een uitgebreide verzameling gegevens geboden voor de teams die mogelijke problemen moeten controleren.

> [!NOTE]
> Als u de vervolgkeuze instelt op **Uitzondering**, levert dit alleen traceerinformatie op wanneer uitzonderingen (fouten) optreden.

Wanneer deze functie is ingeschakeld, worden de traceerlogboeken voor deze invoegtoepassing verzameld totdat ze handmatig worden uitgeschakeld door terug te keren naar deze locatie en ze **uit** te schakelen.

### <a name="view-the-trace-log"></a>Het traceerlogboek weergeven
Voer de volgende stappen uit om het traceerlogboek weer te geven.

1. Selecteer op de Dynamics 365-pagina de optie **Instellingen** op de navigatiebalk bovenaan. 
2. Selecteer **Traceerlogboek invoegtoepassing** in de sectie **Aanpassingen** van de pagina.
3. U kunt vermeldingen vinden in de lijst met traceerlogboeken, gebaseerd op typenaam en/of berichtnaam.
4. Open de gewenste vermelding om het volledige logboek weer te geven. Het berichtenblok in de sectie Uitvoering biedt beschikbare informatie voor de invoegtoepassing. Indien beschikbaar worden ook uitzonderingsdetails verstrekt. 

U kunt de inhoud van de traceerlogboeken kopiëren en deze in een andere toepassing plakken, zoals Kladblok of andere hulpmiddelen om logboeken of tekstbestanden weer te geven, zodat u gemakkelijker alle inhoud kunt zien. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>De modus Foutopsporing inschakelen om live synchronisatieproblemen in apps voor financiële en bedrijfsactiviteiten op te lossen

**Vereiste rol om de fouten weer te geven:** systeembeheerder

Fouten met twee keer wegschrijven die afkomstig zijn Dataverse, kunnen worden weergegeven in de app voor financiële en bedrijfsactiviteiten. Neem de volgende stappen om uitgebreide logboekregistratie van de fouten in te schakelen:

1. Voor alle projectconfiguraties in app voor financiële en bedrijfsactiviteiten is er de flag **IsDebugMode** in de tabel **DualWriteProjectConfiguration**.
2. Open de tabel **DualWriteProjectConfiguration** met de Excel-invoegtoepassing. Als u de invoegtoepassing wilt gebruiken, moet u de ontwerpmodus in de Excel-invoegtoepassing van Finance and Operations inschakelen en **DualWriteProjectConfiguration** aan het werkblad toevoegen. Zie [Entiteitsgegevens weergeven en bijwerken met Excel](../../office-integration/use-excel-add-in.md) voor meer informatie.
3. Stel **IsDebugMode** in op **Ja** in het project.
4. Voer het scenario uit dat fouten genereert.
5. De uitgebreide logboeken worden opgeslagen in de tabel **DualWriteErrorLog**.
6. Als u gegevens wilt opzoeken in de tabelbrowser, gebruikt u de volgende koppeling: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog` en vervangt u indien nodig `999`.
7. Voer de update opnieuw na [KB-4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), die beschikbaar is voor platformupdates 37 en later. Als u deze oplossing hebt geïnstalleerd, worden in de foutopsporingsmodus meer logboeken vastgelegd.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Synchronisatiefouten controleren op de virtuele machine voor de app voor financiële en bedrijfsactiviteiten

**Vereiste rol om de fouten weer te geven:** systeembeheerder

1. Meld u aan bij Microsoft Dynamics LCS (LifeCycle Services).
2. Open het LCS-project dat u hebt gekozen voor tests met twee keer wegschrijven.
3. Selecteer de tegel **Cloudomgevingen**.
4. Gebruik Extern bureaublad om u aan te melden bij de virtuele machine (VM) voor de app voor financiële en bedrijfsactiviteiten. Gebruik het lokale account dat wordt weergegeven in LCS.
5. Open Logboeken.
6. Selecteer **Logboeken Toepassingen en Services \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationeel**.
7. Bekijk de lijst met recente fouten.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Landingspagina voor twee keer wegschrijven wordt leeg weergegeven
Bij het openen van de pagina voor twee keer wegschrijven in Microsoft Edge of Google Chrome, wordt de startpagina niet geladen en ziet u een lege pagina of een foutmelding, zoals Er is een fout opgetreden.
In Devtools ziet u een fout in de logboeken van de console:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Failed to read the 'sessionStorage' property from 'Window': Access is denied for this document. at t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) at new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) at jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) at Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) at Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) at vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) at hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

De gebruikersinterface gebruikt sessieopslag van de browser om bepaalde eigenschapswaarden voor het laden van de startpagina op te slaan. Hiervoor moeten cookies van derden zijn toegestaan in de browser voor de site. De fout wijst erop dat de gebruikersinterface geen toegang heeft tot de sessieopslag. Er kunnen twee scenario's zijn waarin dit probleem zich voordoet:

1.  U opent de gebruikersinterface in de incognitomodus van Edge/Chrome en cookies van derden worden geblokkeerd in deze modus.
2.  U hebt cookies van derden geheel geblokkeerd in Edge/Chrome.

### <a name="mitigation"></a>Risicobeperking
Cookies van derden moeten zijn toegestaan in de browserinstellingen.

### <a name="google-chrome-browser"></a>Google Chrome-browser
Eerste optie:
1.  Ga naar instellingen door chrome://settings/ op de adresbalk in te voeren en ga naar Privacy en beveiliging -> Cookies en andere sitegegevens.
2.  Selecteer Alle cookies toestaan. Als u dit niet wilt doen, gaat u naar de tweede optie.

Tweede optie:
1.  Ga naar instellingen door chrome://settings/ op de adresbalk in te voeren en ga naar Privacy en beveiliging -> Cookies en andere sitegegevens.
2.  Als Cookies van derden blokkeren in incognitomodus of Cookies van derden blokkeren is geselecteerd, gaat u naar Sites die altijd cookies mogen gebruiken en klikt u op **Toevoegen**. 
3.  Voeg de sitenaam van uw Finance + Operations-apps toe (https://<uw_FinOp_exemplaar>.cloudax.dynamics.com). Schakel het selectievakje Alle cookies, alleen op deze site in. 

### <a name="microsoft-edge-browser"></a>Microsoft Edge-browser
1.  Ga naar Instellingen -> Sitemachtigingen -> Cookies en sitegegevens.
2.  Schakel Cookies van derden blokkeren uit.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Een andere Dataverse-omgeving (los)koppelen vanuit een app voor financiële en bedrijfsactiviteiten

**De vereiste rol om de omgeving te ontkoppelen**: systeembeheerder voor de app voor financiële en bedrijfsactiviteiten of Dataverse.

1. Meld u aan bij de app voor financiële en bedrijfsactiviteiten.
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

### <a name="google-chrome-browser"></a>Google Chrome-browser

1. Druk op het geopende tabblad op **F12** of selecteer **Ontwikkelhulpprogramma's** om de ontwikkelhulpprogramma's te openen.
2. Open het tabblad **Netwerk** en typ **integ** in het filtertekstvak.
3. Voer uw scenario uit en bekijk de aanvragen die worden vastgelegd.
4. Klik met de rechtermuisknop op de vermeldingen en selecteer **Alles opslaan als een HAR-bestand met inhoud**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge-browser

1. Druk op het geopende tabblad op **F12** of selecteer **Ontwikkelhulpprogramma's** om de ontwikkelhulpprogramma's te openen.
2. Open het tabblad **Netwerk**.
3. Voer uw scenario uit.
4. Selecteer **Opslaan** om de resultaten als HAR-bestand te exporteren.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
