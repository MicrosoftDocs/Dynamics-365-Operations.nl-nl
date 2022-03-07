---
title: Problemen met live synchronisatie oplossen
description: Dit onderwerp bevat informatie over het oplossen van problemen met live synchronisatie.
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
ms.openlocfilehash: 2694f48b295ba727870f068e7062f7cdcababdbe
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350783"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Problemen met live synchronisatie oplossen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse. Dit onderwerp bevat specifieke informatie over het oplossen van problemen met live synchronisatie.

> [!IMPORTANT]
> In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD). In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Met live synchronisatie wordt een 403 Verboden-fout gegenereerd wanneer u een rij in een Finance and Operations-app maakt

Mogelijk wordt het volgende foutbericht weergegeven wanneer u een rij in een Finance and Operations-app maakt:

*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"De gebruiker is geen lid van de organisatie.\\"}}\], De externe server heeft een fout geretourneerd: (403) verboden."}}".*

Volg de stappen in [Systeemvereisten en vereisten vooraf](requirements-and-prerequisites.md) om het probleem op te lossen. Om deze stappen te voltooien moeten de gebruikers van de toepassing voor twee keer wegschrijven die in Dataverse gemaakt zijn, beschikken over de rol systeembeheerder. Het standaardteam van eigenaar moet ook de rol systeembeheerder hebben.

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Met live synchronisatie voor een tabel wordt steeds een vergelijkbare fout gegenereerd wanneer u een rij in een Finance and Operations-app maakt

**Vereiste rol om de fout op te lossen:** systeembeheerder

Er wordt een foutbericht van de volgende strekking weergegeven wanneer u tabelgegevens wilt opslaan in een Finance and Operations-app:

*De wijzigingen in de database kunnen niet worden opgeslagen. Werkeenheid kan transactie niet doorvoeren. Kan geen gegevens schrijven in maateenheid van entiteit. Schrijven naar UnitOfMeasureEntity is mislukt met foutbericht Kan niet synchroniseren met maateenheden van entiteit.*

Om het probleem op te lossen moet u ervoor zorgen dat de vereiste verwijzingsgegevens aanwezig zijn in de app Finance and Operations en in Dataverse. Als u als klant in de Finance and Operations-app bijvoorbeeld deel uitmaakt van een specifieke klantengroep, controleert u of de klantengroep ook bestaat in Dataverse.

Voer de volgende stappen uit als er aan beide zijden gegevens voorkomen en u hebt bevestigd dat het probleem niet samenhangt met gegevens:

1. Stop de gerelateerde tabel.
2. Meld u aan bij de Finance and Operations-app en zorg ervoor dat er rijen bestaan voor de tabel die de fout veroorzaakt in de tabellen DualWriteprojectConfiguration en DualWriteprojectFieldConfiguration. Hier ziet u bijvoorbeeld hoe de query eruitziet als de tabel **Klanten** een fout veroorzaakt.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Als er rijen zijn voor de foutieve tabel, zelfs nadat u de tabeltoewijzing hebt gestopt, verwijdert u de rijen die zijn gerelateerd aan de tabel die de fout veroorzaakt. Noteer de kolom **projectnaam** in de tabel DualWriteprojectConfiguration en haal de rij op in de DualWriteprojectFieldConfiguration-tabel door de naam van het project te gebruiken om de rij te verwijderen.
4. Start de tabeltoewijzing. Controleer of de gegevens zonder problemen worden gesynchroniseerd.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Fouten met lees- of schrijfbevoegdheid oplossen wanneer u gegevens maakt in een Finance and Operations-app

Wanneer u gegevens in een Finance and Operations-app maakt, wordt het foutbericht "Ongeldige aanvraag" weergegeven, zoals in het volgende voorbeeld.

![Voorbeeld van foutbericht Ongeldige aanvraag.](media/error_record_id_source.png)

Om het probleem op te lossen moet u de juiste beveiligingsrol toewijzen aan het team van de toegewezen Dynamics 365 Sales- of Dynamics 365 Customer Service-bedrijfseenheid om de ontbrekende bevoegdheid in te schakelen.

1. Zoek in de Finance and Operations-app de bedrijfseenheid die is toegewezen in de verbindingsset Gegevensintegratie.

    ![Organisatietoewijzing.](media/mapped_business_unit.png)

2. Meld u aan bij de omgeving in de modelgestuurde app in Dynamics 365, navigeer naar **Instelling \> Beveiliging** en zoek het team van de toegewezen bedrijfseenheid.

    ![Team van de toegewezen bedrijfseenheid.](media/setting_security_page.png)

3. Open de pagina voor het team voor bewerking en selecteer **Rollen beheren** om het dialoogvenster **Teamrollen beheren** te openen.

    ![De knop Rollen beheren.](media/manage_team_roles.png)

4. Wijs de rol met de bevoegdheid voor lezen/schrijven toe voor de relevante tabellen en selecteer **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Synchronisatie problemen oplossen in een omgeving met een recent gewijzigde Dataverse-omgeving

**Vereiste rol om de fout op te lossen:** systeembeheerder

Mogelijk wordt het volgende foutbericht weergegeven wanneer u gegevens in een Finance and Operations-app maakt:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Kan geen nettolading genereren voor entiteit CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Het maken van de nettolading is mislukt met fout Ongeldige URI: de URI is leeg."}\],"isErrorCountUpdated":true}*

Zo ziet de fout eruit in de modelgestuurde app in Dynamics 365:

*Er is een onverwachte fout opgetreden vanuit de ISV-code. (Fouttype = ClientError) Onverwachte uitzondering in invoegtoepassing: (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: verwerken van entiteitsaccount mislukt - een verbindingspoging is mislukt omdat de verbonden partij niet correct reageert na een bepaalde tijd of de tot stand gebrachte verbinding is mislukt omdat de verbonden host niet heeft gereageerd*

Deze fout treedt op wanneer de Dataverse-omgeving onjuist opnieuw wordt ingesteld op het moment dat u probeert gegevens te maken in de Finance and Operations-app.

Volg deze stappen om het probleem op te lossen.

1. Meld u aan bij de virtuele machine (VM) voor Finance and Operations, open SQL Server Management Studio (SSMS) en zoek naar rijen in de tabel DUALWRITEPROJECTCONFIGURATIONENTITY, waarbij **internalentityname** gelijk is aan **Klanten v3** en **externalentityname** gelijk is aan **accounts**. De query ziet er dan als volgt uit.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Gebruik de projectnaam uit de resultaten van de vorige query om de volgende query uit te voeren.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Controleer of de kolom **externalenvironmentURL** de juiste URL voor Dataverse of de app heeft. Verwijder dubbele rijen die naar de verkeerde Dataverse-URL verwijzen. Verwijder de overeenkomstige rijen uit de tabellen DUALWRITEPROJECTFIELDCONFIGURATION en DUALWRITEPROJECTCONFIGURATION.
4. De tabeltoewijzing stoppen en vervolgens opnieuw starten


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]