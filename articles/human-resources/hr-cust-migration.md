---
title: Dynamics 365 Human Resources-klantmigratie naar de infrastructuur voor financiën en bedrijfsactiviteiten
description: In dit artikel wordt de klantmigratie van Microsoft Dynamics 365 Human Resources naar de infrastructuur voor financiën en bedrijfsactiviteiten beschreven.
author: twheeloc
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9680c2d1caa08c15aed325f4153aac6eae63c3
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831715"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources-klantmigratie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Klantmigratie is een lift-and-shift-migratie (verplaatsing) van een klantendatabase naar de infrastructuur voor financiën en bedrijfsactiviteiten. Hiervoor worden hulpmiddelen voor automatische migratie gebruikt. Het resultaat is een nieuwe omgeving voor apps voor financiën en bedrijfsactiviteiten waarin de Human Resources-database van de klant wordt gebruikt.

## <a name="prerequisites"></a>Vereisten

### <a name="user-access-and-permissions"></a>Gebruikerstoegang en -machtigingen

- De gebruiker van Microsoft Dynamics Lifecycle Services moet de rol **Organisatiebeheerder** hebben.
- De gebruiker moet [Azure DevOps-projecten kunnen maken](/azure/devops/organizations/projects/create-project) of een bestaand Azure DevOps-project kunnen gebruiken.
- De gebruiker moet toegang hebben om een [Azure DevOps-beveiligingstoken voor persoonlijke toegang te maken](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) of een token hebben dat kan worden gebruikt.

### <a name="dataverse-environment-backup-sandbox"></a>Back-up van Dataverse-omgeving (sandbox)

 - Optioneel maar aan te raden: vernieuwe de bestaande sandbox-omgeving voor Human Resources door een kopie van de productieomgeving voor Human Resources te gebruiken.
 - Maak een nieuwe Dataverse-omgeving met het Power Platform-beheercentrum.
 - Kopieer de bestaande Dataverse-omgeving, die aan de zelfstandige Human Resources-app is gekoppeld, naar de omgeving die u in de vorige stap hebt gemaakt.

> [!NOTE]
> Wanneer u een database toevoegt, moet u ervoor zorgen dat de optie **Dynamics 365-apps inschakelen** is ingesteld op **Ja**. Zie [Een Power Platform-omgeving voorbereiden](hr-cust-migration.md#prepare-a-power-platform-environment) voor gedetailleerde informatie.

### <a name="dataverse-capacity"></a>Dataverse-capaciteit

1. Gebruik de pagina **Overzicht** in het Power Platform-beheercentrum om te controleren of de [Dataverse-opslag](/power-platform/admin/finance-operations-storage-capacity) voldoende beschikbare capaciteit voor de omgevingskopie heeft.
2. Als er onvoldoende capaciteit beschikbaar is, gebruikt u de [richtlijnen voor het vrij maken van opslagruimte](/power-platform/admin/free-storage-space) om het totale verbruik te verminderen. Klanten kunnen ook [extra opslagcapaciteit toevoegen](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Klantmigratieproces

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Een Lifecycle Services-project maken voor de migratie van Human Resources

De eerste stap is het maken van een nieuw implementatieproject voor financiën en bedrijfsactiviteiten in Lifecycle Services. De klant heeft dan een bestaand Lifecycle Services-project in Human Resources. De bestaande Human Resources-omgevingen worden gemigreerd naar het nieuwe implementatieproject voor financiën en bedrijfsactiviteiten.

Ga als volgt te werk om een nieuw project te maken.

1. Meld u aan bij Lifecycle Services als de globale beheerder of de aangewezen gebruiker van het serviceaccount.
2. Selecteer op de startpagina van Lifecycle Services de optie **Maken/nieuw (+)**.
3. Selecteer apps voor financiën en bedrijfsactiviteiten als het product.
4. Selecteer in het veld **Projectdoel** de optie **Implementatie**.
5. Voer een projectnaam en -beschrijving in.
6. In het veld **Aangepast projecttype** selecteert u **Migratie van Microsoft Dynamics 365 Human Resources**.
7. Schakel het selectievakje in om de voorwaarden te accepteren.
8. Selecteer **Maken**.

Nadat u een nieuw Lifecycle Services-project hebt gemaakt, voert u de volgende stappen uit om het project te configureren.

1. Selecteer **Onboarding voor project** om de projectonboarding te voltooien. Zie [Projectonboarding](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md) voor meer informatie.

    - Selecteer dezelfde regio als uw huidige omgevingen. Deze selectie heeft geen invloed op migratie.
    - Selecteer **Overige** voor oudere systemen.

2. Voltooi de projectinstellingen. Als onderdeel van deze stap moet u de SharePoint Online-bibliotheek, Azure DevOps en Azure-verbindingen configureren, indien nodig. Zie voor meer informatie [Gebruikershandleiding Lifecycle Services (LCS)](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Klanten kunnen een bestaand Azure DevOps-project en het bijbehorende beveiligingstoken voor persoonlijke toegang gebruiken. Als een bestaand project wordt gebruikt, zijn de configuraties die bij het project horen automatisch beschikbaar en kunnen ze op nauwkeurigheid worden gecontroleerd.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Een sandbox-omgeving voor Human Resources migreren

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Voorbereiden om de sandbox-omgeving te migreren

Nadat een nieuw Lifecycle Services-project is gemaakt en het onboardingproces voor het project is voltooid, bent u klaar om uw eerste omgeving te migreren. Voordat u dit proces start, is het raadzaam om de sandbox-omgeving te vernieuwen die u vanuit uw productieomgeving op de zelfstandige infrastructuur wilt migreren.

#### <a name="prepare-a-power-platform-environment"></a>Een Power Platform-omgeving voorbereiden

> [!NOTE]
> Deze stap is alleen van toepassing op migratie van de sandbox-omgeving. Wanneer u de productieomgeving migreert, wordt de bestaande Power Platform-beheercentrumomgeving die aan de productieomgeving is gekoppeld, verplaatst. Wanneer u een database toevoegt, moet u ervoor zorgen dat de knop **Dynamics 365-apps inschakelen** is ingesteld op **Ja**. 

- Maak in het Power Platform-beheercentrum [een omgeving met een database](/power-platform/admin/create-environment#create-an-environment-with-a-database) om te gebruiken voor de sandbox-migratie of selecteer een bestaande omgeving.
- [Kopieer een omgeving](/power-platform/admin/copy-environment) om de Power Platform-omgeving te vernieuwen die voor toewijzing wordt gebruikt.

#### <a name="migrate-the-sandbox-environment"></a>De sandbox-omgeving migreren

1. Meld u aan bij Lifecycle Services als de globale beheerder of de aangewezen gebruiker van het serviceaccount.

    > [!NOTE]
    > Het wordt aangeraden om een benoemde gebruikersaccount te gebruiken. De aangemelde gebruiker moet de beveiligingsrol **Projecteigenaar** of **Omgevingsmanager** hebben in het zelfstandige Lifecycle Services-project in Human Resources.

2. Open het nieuwe Human Resources-migratieproject.
3. Controleer en voltooi de toepasselijke fasen van de migratiemethodologie en de projectonboarding.
4. Selecteer in het projectdashboard in het deelvenster **Standaard: standaardacceptatietest** de optie **HR migreren**.
5. Selecteer in het deelvenster **Omgeving selecteren om te migreren** het juiste Lifecycle Services-project en de oorspronkelijke Human Resources-omgeving (in uw zelfstandige Human Resources-brontoepassing).
6. Schakel **Toewijzen aan nieuwe Power Platform-omgeving** in en selecteer de juiste Power Platform-omgeving. Selecteer **Volgende**.
7. Voltooi de wizard **Implementatie-instellingen (financiën en bedrijfsactiviteiten – sandbox)** om details en aanmelding van klanten te bevestigen en selecteer **Implementeren**.

De omgevingsstatus duidt de voortgang aan. De status wordt gewijzigd van **Laden** in **Bezig met implementeren** en vervolgens in **Geïmplementeerd**.

> [!NOTE]
> Het productievenster is pas beschikbaar als de controlelijst voor gereedheid voor het go-live-project is voltooid. Zie [Voorbereiden voor go-live](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) voor meer informatie.

#### <a name="considerations-and-assumptions"></a>Overwegingen en veronderstellingen

Een sandbox-omgeving voor Human Resources bestaat in een Lifecycle Services-project voor de tenant die de volgende kenmerken heeft:

- De sandbox-omgeving voor Human Resources is niet aan een bestaande samengevoegde omgeving gekoppeld. Er kan slechts één migratie tegelijk worden uitgevoerd voor een bepaalde Human Resources-omgeving.
- Hoeveel sandbox-omgevingen tegelijk zijn toegestaan, is afhankelijk van de Human Resources-licenties. Als er voldoende licenties zijn aangeschaft voor de tenant, worden er extra sandbox-omgevingen weergegeven in het deelvenster **Omgevingen** van het project.
- Migraties moeten worden uitgevoerd naar omgevingen van hetzelfde type. Dit wil zeggen dat u alleen een migratie tussen sandbox-omgevingen en tussen productieomgevingen kunt uitvoeren.

    > [!NOTE]
    > Er wordt bij het bepalen van de productie- of sandbox-status alleen rekening gehouden met Human Resources-omgevingstypen. Als de omgevingen incorrect zijn gecategoriseerd (dus als een productieomgeving is gemarkeerd als een sandbox-omgeving of andersom), kunt u contact opnemen met ondersteuning.

- Als de migratie niet lukt, wordt er een foutbericht weergegeven en wordt de knop **Verwijderen** beschikbaar. Met deze knop kunt u de mislukte migratie verwijderen. Vervolgens kunt u de omgeving opnieuw migreren.

#### <a name="validate-the-sandbox-migration"></a>De sandbox-migratie valideren

Nadat de sandbox-migratie is voltooid, maakt u een gedetailleerd testplan om alle bedrijfsprocessen te controleren en af te tekenen.

Valideer voordat u begint met het testen de volgende gegevens:

- Bevestig dat de gemigreerde omgeving toegankelijk is via de URL die wordt gegenereerd.
- Bevestig dat gebruikers toegang hebben tot de gemigreerde sandbox.
- Controleer of de Dataverse-omgeving die aan de gemigreerde werkomgeving is gekoppeld, toegankelijk is.
- Voer steekproefsgewijze controles op verschillende gegevens uit om te bevestigen dat de meest recente gegevens beschikbaar zijn.
- Voltooi de belangrijke bedrijfsprocessen voor validatie.
- Bevestig dat uw beveiligingsbeleid van toepassing is.
- Bevestig dat batchtaken zijn geactiveerd zoals verwacht.

U hebt geen Extern bureaublad-toegang tot de gemigreerde sandbox. U kunt zelfservicefuncties en -hulpmiddelen gebruiken om de volgende acties uit te voeren voor uw Tier 2+-sandbox-omgevingen:

- Toegang krijgen tot de [Azure SQL-database](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Toegang krijgen tot [logboekbestanden](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- [Perfmon-tools](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools) gebruiken.
- De [onderhoudsmodus in- of uitschakelen](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Services [opnieuw starten](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- [Regression Suite Automation Tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool) configureren.

Zie [Veelgestelde vragen voor self-service implementatie](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md) voor meer informatie.

### <a name="migrate-a-human-resources-production-environment"></a>Een Human Resources-productieomgeving migreren

Nadat u klaar bent met het migreren en valideren van een sandbox-omgeving, volgt u deze stappen om de productieomgeving te migreren.

#### <a name="prerequisites"></a>Vereisten

- De abonnementsschatting moet worden voltooid.
- De [evaluatie van de gereedheid](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) voor de go-live gereedheid moet worden voltooid.
- De gebruiker die de productiemigratie in Lifecycle Services start, moet de rol Systeembeheerder hebben op het Power Platform. 

#### <a name="migrate-the-production-environment"></a>De productieomgeving migreren

1. Meld u aan bij Lifecycle Services als de globale beheerder of de aangewezen gebruiker van het serviceaccount.

    > [!NOTE]
    > Het wordt aangeraden om een benoemde gebruikersaccount te gebruiken. De aangemelde gebruiker moet de beveiligingsrol **Projecteigenaar** of **Omgevingsmanager** hebben in het Lifecycle Services-project.

2. Open het nieuwe Human Resources-migratieproject.
3. Controleer en voltooi de toepasselijke fasen van de migratiemethodologie en projectonboarding.
4. Selecteer in het projectdashboard in het deelvenster **Productie** de optie **HR migreren**.
5. Selecteer in het deelvenster **Omgeving selecteren om te migreren** het juiste Lifecycle Services-project en de oorspronkelijke Human Resources-omgeving (in uw zelfstandige Human Resources-brontoepassing). Selecteer **Volgende**.
6. Voltooi de wizard **Implementatie-instellingen (financiën en bedrijfsactiviteiten – sandbox)** om details en aanmelding van klanten te bevestigen en selecteer **Implementeren**.

De omgevingsstatus duidt de implementatievoortgang aan. De status wordt gewijzigd van **Laden** in **Bezig met implementeren** en vervolgens in **Geïmplementeerd**.

#### <a name="post-migration-considerations"></a>Overwegingen na integratie

- Pas de nieuwste [kwaliteitsupdates](/fin-ops-core/fin-ops/get-started/quality-updates) toe op u omgevingen.
- Als u [virtuele tabellen](hr-admin-integration-common-data-service-virtual-entities.md) gebruikt, moet u de eindpunten opnieuw configureren.
- Configureer de integratie van twee keer wegschrijven opnieuw. Beoordeel welke entiteiten moeten worden ingeschakeld.
- U kunt virtuele tabellen gebruiken om twee keer wegschrijven voor integratie te vervangen.

#### <a name="dual-write-integration"></a>Integratie van twee keer wegschrijven

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>De integratie van twee keer wegschrijven voor Microsoft Power Platform instellen

1. Ga naar het Power Platform-beheercentrum en selecteer **Omgevingen** in de navigatie links.
2. Selecteer de eerder gekopieerde/vernieuwde omgeving en bevestig dat de status **Gereed** is.
3. Ga naar Lifecycle Services en bevestig dat de status van het migratieproject **Geïmplementeerd** is.
4. Selecteer onder de gemigreerde omgeving de optie **Volledige details** om aanvullende details te bekijken [en een toepassing voor twee keer wegschrijven in te stellen](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. Schakel in het deelvenster **Configuratie van toepassing voor twee keer wegschrijven** het selectievakje in om de toewijzing en synchronisatie van gegevens tussen databases toe te staan. Selecteer vervolgens **Configureren**.
6. Wanneer u via een bericht wordt geïnformeerd over een geslaagde configuratie voor twee keer wegschrijven, selecteert u **OK**.
7. U kunt de voortgang van de configuratie in de details controleren.
8. Wanneer de configuratie is voltooid, selecteert u **Koppelen aan Power Platform-omgeving** om de beschikbare gegevensentiteiten te synchroniseren.
9. Wanneer de status aangeeft dat de omgevingen aan elkaar zijn gekoppeld, gaat u naar het Power Platform-beheercentrum om de juiste gegevensentiteiten te controleren en te selecteren.
10. Selecteer In het linkerdeelvenster **Dynamics 365-apps \> Resources**.
11. Bevestig dat de status van de Human Resources-app voor twee keer wegschrijven **Ingeschakeld** is.
12. Selecteer de Human Resources-app voor twee keer wegschrijven en selecteer vervolgens **Installeren**.
13. Selecteer in het deelvenster **Dynamics 365 Human Resources-app voor twee keer wegschrijven installeren** de omgeving waarin u het pakket wilt installeren.
14. Schakel dit selectievakje in om akkoord te gaan met de servicevoorwaarden en selecteer **Installeren**.
15. In de omgeving van de Dynamics 365 app wordt de status **Bezig met installeren** terwijl de installatie wordt uitgevoerd. Deze wordt bijgewerkt naar **Geïnstalleerd** wanneer de installatie is voltooid.

##### <a name="review-and-apply-a-dual-write-solution"></a>Een oplossing voor twee keer wegschrijven controleren en toepassen

1. Ga in de nieuwe omgeving voor financiën en bedrijfsactiviteiten naar **Gegevensbeheer \> Twee keer wegschrijven**.
2. Selecteer **Oplossing toepassen**.
3. Selecteer in het deelvenster **Geïnstalleerde Dynamics-oplossingen**, **Kernentiteitstoewijzingen voor toepassingen voor twee keer wegschrijven** en **Dynamics 365 Human Resources-toewijzingen**. Selecteer **Toepassen**. Er wordt een bericht weergegeven dat de oplossing wordt toegepast. Nadat de oplossing is toegepast, worden alle beschikbare tabeltoewijzingen weergegeven.
4. Controleer de beschikbare tabeltoewijzingen om de integratie te selecteren en uit te voeren met behulp van Twee keer wegschrijven.
5. Wanneer u de Twee keer wegschrijven-integratie voor het eerst voor tabeltoewijzingen gebruikt, moet u het selectievakje **Initiële synchronisatie** inschakelen. Als er een bestaande integratie is vanuit de Human Resources-bronomgeving, hoeft u het selectievakje **Initiële synchronisatie** niet in te schakelen wanneer u de integratie voor tabeltoewijzingen uitgevoerd.

#### <a name="recommended-practices"></a>Aanbevolen praktijken

Deze sectie bevat aanbevelingen voor het migreren van de zelfstandige infrastructuur naar de infrastructuur voor financiën en bedrijfsactiviteiten.

- U wordt sterk aangeraden om samen te werken met uw Microsoft Dynamics-partner voor de migratie van uw Human Resources-omgeving.
- Plan voldoende tijd om volledige acceptatietests voor gebruikers (UAT: Full User Acceptance Testing) uit te voeren voor de gemigreerde omgeving.
- Plan en documenteer de gedetailleerde stappen om integraties naar de gemigreerde omgeving te migreren.
- Maak een gedetailleerde controlelijst maken om een overzicht van het wijzigingsproces voor uw migratie te bieden.
- Plan de juiste hoeveelheid uitvaltijd voor uw bedrijf terwijl u de migratie doet.
- We raden klanten die in FastTrack zijn gekwalificeerd sterk aan samen te werken met hun FastTrack-oplossingsarchitect bij het migratieproces.
- Het wordt sterk aangeraden uw sandbox-omgeving in de zelfstandige infrastructuur te vernieuwen voordat u de eerste migratie uitvoert. Deze vernieuwing moet ook de Dataverse-omgeving omvatten die is verbonden met de omgeving waarnaar u wilt migreren.
- U wordt sterk aangeraden een serviceaccount te gebruiken wanneer u uw Lifecycle Services-project implementeert, migreert en maakt.
- Plan de upgrade van de sandbox-omgeving voor UAT-validatie in de laatste versie van algemene beschikbaarheid (GA). Zie voor meer informatie deze [overwegingen](hr-infrastructure-merge.md#considerations).
