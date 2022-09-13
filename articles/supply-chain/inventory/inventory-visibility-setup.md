---
title: Invoegtoepassing Voorraadzichtbaarheid installeren
description: In dit artikel wordt beschreven hoe u de invoegtoepassing Inventory Visibility installeert voor Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: eb17f24b90933dac0f875bb0ef2d5039a240b197
ms.sourcegitcommit: 1ca4ad100f868d518f3634dca445c9878962108e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2022
ms.locfileid: "9388535"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility installeren en instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u de invoegtoepassing Inventory Visibility installeert voor Microsoft Dynamics 365 Supply Chain Management.

U moet de invoegtoepassing voor Voorraadzichtbaarheid installeren met behulp van Microsoft Dynamics Lifecycle Services (LCS). LCS is een portal voor samenwerking die een omgeving en een reeks regelmatig bijgewerkte services biedt waarmee u de toepassingslevensduur van uw apps voor financiën en bedrijfsactiviteiten kunt beheren. Zie voor meer informatie [Lifecycle Services-resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> We raden u aan om deel te nemen aan de gebruikersgroep Invoegtoepassing Voorraadzichtbaarheid, waar u nuttige handleidingen kunt vinden, onze nieuwste updates kunt krijgen en eventuele vragen kunt plaatsen over het gebruik van Voorraadzichtbaarheid. Als u wilt deelnemen, verzendt u een e-mail naar het productteam Voorraadzichtbaarheid op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) en voegt u uw ID van de Supply Chain Management-omgeving toe.

## <a name="inventory-visibility-prerequisites"></a>Vereisten voor Voorraadzichtbaarheid

Voordat u de Voorraadzichtbaarheid kunt installeren, moet u de volgende taken uitvoeren:

- Schaf een LCS-implementatieproject aan met minimaal één geïmplementeerde omgeving.
- Zorg ervoor dat er aan de vereisten voor het instellen van invoegtoepassingen voldaan is. Zie [Overzicht invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor informatie over deze vereisten. Voor Voorraadzichtbaarheid is geen koppeling voor twee keer wegschrijven vereist.

> [!NOTE]
> De landen en regio's die momenteel worden ondersteund, zijn Canada ( CCA, ECA), de Verenigde Staten (WUS, EUS), de Europese Unie (NEU, WEU), het Verenigd Koninkrijk (SUK, WUK), Australië (EAU, SEAU), Japan (EJP, WJP) en Brazilië (SBR, SCUS).

Als u vragen hebt over deze vereisten, neemt u contact op met het productteam van Voorraadzichtbaarheid op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Invoegtoepassing Voorraadzichtbaarheid installeren

Voordat u de invoegtoepassing installeert, registreert u een toepassing en voegt u een clientgeheim toe aan Azure Active Directory (Azure AD) via uw Azure-abonnement. Zie [Een toepassing registreren](/azure/active-directory/develop/quickstart-register-app) en [Een clientgeheim toevoegen](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) voor instructies. Zorg ervoor dat u de waarden **Toepassings-id**, **Clientgeheim** en **Tenant-id** noteert, omdat u ze later nodig hebt.

> [!IMPORTANT]
> Als u meerdere LCS-omgevingen hebt, maakt u een andere Azure AD-toepassing voor elke omgeving. Als u dezelfde toepassings-id en tenant-id gebruikt om de invoegtoepassing Voorraadzichtbaarheid voor verschillende omgevingen te installeren, treedt er een probleem met een token op voor oudere omgevingen. Het gvolg is dat alleen de laatste installatie geldig is.

Nadat u een toepassing geregistreerd hebt en een clientgeheim aan Azure AD hebt toegevoegd, volgt u deze stappen om de invoegtoepassing voor Voorraadzichtbaarheid te installeren.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index).
1. Selecteer op de startpagina het project waar uw omgeving is geïmplementeerd.
1. Selecteer op de projectpagina de omgeving waarin u de invoegtoepassing wilt installeren.
1. Schuif op de omgevingspagina naar beneden tot u de sectie **invoegtoepassingen voor omgeving** ziet in de **Power Platform Integratie**-sectie. Hier kunt u de Dataverse-omgevingsnaam vinden. Bevestig dat de Dataverse-omgevingsnaam de naam is die u wilt gebruiken voor Voorraadzichtbaarheid.

    > [!NOTE]
    > Momenteel worden alleen Dataverse-omgevingen ondersteund die met behulp van LCS gemaakt zijn. Als uw Dataverse-omgeving op een andere manier gemaakt is (bijvoorbeeld door het PowerApps-beheercentrum te gebruiken) en als deze aan uw Supply Chain Management-omgeving gekoppeld is, moet u eerst het toewijzingsprobleem verhelpen voordat u de invoegtoepassing Voorraadzichtbaarheid installeert.
    >
    > Het is mogelijk dat uw omgeving voor twee keer wegschrijven wordt gekoppeld aan een Dataverse-exemplaar terwijl LCS niet is ingesteld voor Power Platform-integratie. Deze onjuiste koppeling kan tot onverwachte gedragingen leiden. De gegevens van de LCS-omgeving kunnen het beste overeenkomen met de gegevens waarmee u verbinding hebt via twee keer wegschrijven zodat dezelfde verbinding kan worden gebruikt door zakelijke gebeurtenissen, virtuele tabellen en invoegtoepassingen. Zie [Koppeling aan een verkeerde instantie](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch) voor informatie over het oplossen van het toewijzingsprobleem. Zodra het toewijzingsprobleem is opgelost, kunt u verdergaan met het installeren van Voorraadzichtbaarheid.

1. Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.

    ![Omgevingspagina in LCS](media/inventory-visibility-environment.png "Omgevingspagina in LCS")

1. Selecteer de koppeling **Een nieuwe invoegtoepassing installeren**. Er wordt een lijst met beschikbare invoegtoepassingen weergegeven.
1. Selecteer **Voorraadzichtbaarheid** in de lijst.
1. Stel daarna de volgende velden in voor uw omgeving:

    - **AAD-toepassing (client) ID** – voer de Azure AD ID in van de toepassingsclient die u eerder aangemaakt en genoteerd hebt.
    - **AAD tenant ID** – Voer de tenant-ID in die u eerder hebt genoteerd.

    ![Pagina voor invoegtoepassingen installeren](media/inventory-visibility-setup.png "Pagina voor invoegtoepassingen instellen")

1. Ga akkoord met de voorwaarden door het selectievakje **Voorwaarden** in te schakelen.
1. Selecteer **Installeren**. De status van de invoegtoepassing wordt weergegeven als **Wordt geïnstalleerd**. Nadat de installatie voltooid is, vernieuwt u de pagina. De status moet worden gewijzigd in **Geïnstalleerd**.
1. Selecteer in Dataverse de sectie **Apps** in het linkernavigatievenster en controleer of de **Voorraadzichtbaarheid** van Power Apps is geïnstalleerd. Als de sectie **Apps** niet bestaat, neemt u contact op met het productteam van Voorraadzichtbaarheid op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Als de installatie van de LCS-pagina meer dan een uur duurt, heeft uw gebruikersaccount waarschijnlijk onvoldoende machtigingen om oplossingen in de Dataverse-omgeving te installeren. Volg deze stappen om het probleem op te lossen:
>
> 1. Annleer de installatie van de invoegtoepassing Voorraadzichtbaarheid via de LCS-pagina.
> 1. Meld u aan bij het [Microsoft 365-beheercentrum](https://admin.microsoft.com) en zorg ervoor dat aan de gebruikersaccount die u wilt gebruiken voor het installeren van de invoegaccount de licentie Dynamics 365 Unified Operations-plan is toegewezen. Wijs indien nodig de licentie toe.
> 1. Meld u aan bij het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com) met de relevante gebruikersaccount. Ga vervolgens als volgt te werk om de invoegtoepassing Voorraadzichtbaarheid te installeren:
>     1. Selecteer de omgeving waar u de invoegtoepassing wilt installeren.
>     1. Selecteer **Dynamics 365-apps**.
>     1. Selecteer **App installeren**.
>     1. Selecteer **Voorraadzichtbaarheid**.
>
> 1. Als de installatie is voltooid, gaat u terug naar de LCS-pagina en probeert u de invoegvoeging **Voorraadzichtbaarheid** opnieuw te installeren.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Voorraadzichtbaarheid instellen in Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Het integratiepakket voor voorraadzichtbaarheid implementeren

Als u Supply Chain Management versie 10.0.17 of eerder uitvoert, neemt u contact op met het ondersteuningsteam voor voorraadzichtbaarheid op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) om het pakketbestand op te halen. Implementeer het pakket vervolgens in LCS.

> [!NOTE]
> Als er tijdens de implementatie een fout optreedt omdat de versies niet overeenkomen, moet u het X++-project handmatig in uw ontwikkelomgeving importeren. Maak vervolgens het implementeerbare pakket in uw ontwikkelomgeving en implementeer dit in uw productieomgeving.
>
> De code is opgenomen in Supply Chain Management versie 10.0.18. Als u die versie of een latere versie uitvoert, is implementatie niet vereist.

Zorg ervoor dat de volgende functies zijn ingeschakeld in uw Supply Chain Management-omgeving. (Standaard zijn deze ingeschakeld.)

| Beschrijving van functie | Codeversie | Klasse in-/uitschakelen |
|---|---|---|
| Het gebruik van voorraaddimensies in de tabel InventSum in- of uitschakelen      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Het gebruik van voorraaddimensies in de tabel InventSumDelta in- of uitschakelen | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Integratie van voorraadzichtbaarheid instellen

Nadat u de invoegtoepassing hebt geïnstalleerd, kunt u uw Supply Chain Management-systeem voorbereiden om met de toepassing te werken door de volgende stappen uit te voeren.

1. Open in Supply Chain Management het werkgebied **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** en schakel de volgende functies in:
    - *Integratie van Voorraadzichtbaarheid*: vereist.
    - *Integratie met Voorraadzichtbaarheid met tegenreserveringen*: aanbevolen maar optioneel. Vereist versie 10.0.22 of hoger. Zie [Voorraadzichtbaarheid reserveringen](inventory-visibility-reservations.md) voor meer informatie.

1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor integratie met Voorraadzichtbaarheid**.
1. Open het tabblad **Algemeen** en stel de volgende opties in:
    - **Eindpunt Voorraadzichtbaarheid**: geef de URL van de omgeving op waarin u Voorraadzichtbaarheid uitvoert. Zie [Het service-eindpunt vinden](inventory-visibility-configuration.md#get-service-endpoint) voor meer informatie.
    - **Maximumaantal records in één aanvraag**: stel deze optie in op het maximumaantal records dat in één aanvraag moet worden opgenomen. U moet een positief geheel getal invoeren dat kleiner is dan of gelijk is aan 1000. De standaardwaarde is 512. Het wordt sterk aangeraden de standaardwaarde aan te houden, tenzij u een ander advies hebt gekregen van Microsoft Ondersteuning of er zeker van bent dat u de waarde moet wijzigen.

1. Als u de optionele functie *Integratie van Voorraadzichtbaarheid met tegenreservering* hebt ingeschakeld, opent u het tabblad **Tegenreservering** en stelt u de volgende opties in:
    - **Tegenreservering inschakelen**: stel de optie in op *Ja* om deze functionaliteit in te schakelen.
    - **Modificator voor tegenreservering**: selecteer de status van de voorraadtransactie om reserveringen die zijn gemaakt in Voorraadzichtbaarheid, te compenseren. Met deze instelling wordt de fase van de orderverwerking bepaald waarmee tegenreserveringen worden geactiveerd. De fase wordt door de voorraadtransactiestatus van de order opgevolgd. Selecteer een van de volgende opties:
        - *In bestelling*: voor de status *Op transactie* wordt een aanvraag voor een tegenreservering verzonden wanneer deze wordt gemaakt. De verrekende hoeveelheid is de hoeveelheid van de gemaakte order.
        - *Reserveren*: voor de status *Bestelde transactie reserveren* verzendt een order een tegenreserveringsaanvraag wanneer deze gereserveerd, verzameld, via de pakbon geboekt of gefactureerd wordt. De aanvraag wordt slechts eenmaal voor de eerste stap geactiveerd wanneer het bovengenoemde proces plaatsvindt. De verrekende hoeveelheid is de hoeveelheid waarvoor de status van de voorraadtransactie is gewijzigd van *Besteld* in *Gereserveerd* (of een latere status) op de corresponderende orderregel.

1. Ga naar **Voorraadbeheer \> Periodiek \> Integratie van voorraadzichtbaarheid** en schakel de taak in. Alle gebeurtenissen voor voorraadwijziging van Supply Chain Management worden nu geboekt naar Voorraadzichtbaarheid.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Invoegtoepassing Voorraadzichtbaarheid deïnstalleren

Om de invoegtoepassing voor voorraadzichtbaarheid te verwijderden, volgt u deze stappen:

1. Meld u aan bij Supply Chain Management.
1. Ga naar **Voorraadbeheer \> Periodiek \> Integratie van voorraadzichtbaarheid** en schakel de taak uit.
1. Ga naar LCS en open de pagina voor de omgeving waar u de invoegtoepassing wilt verwijderen (zie ook [De invoegtoepassing voor voorraadzichtbaarheid installeren](#install-add-in)).
1. Selecteer **Verwijderen**.
1. Als u de installatie ongedaan maakt, wordt de invoegtoepassing voor Voorraadzichtbaarheid beëindigd, wordt de invoegtoepassing voor LCS ongedaan gemaakt en worden tijdelijke gegevens verwijderd die in de cache van de invoegtoepassing voor voorraadzichtbaarheid opgeslagen zijn. De primaire voorraadgegevens die in uw Dataverse-abonnement zijn gesynchroniseerd, worden echter niet verwijderd. Voer de rest of deze procedure uit om deze gegevens te verwijderen.
1. Open [Power Apps](https://make.powerapps.com).
1. Selecteer **Omgeving** op de navigatiebalk
1. Selecteer de Dataverse-omgeving die aan uw LCS-omgeving is verbonden.
1. Ga naar **Oplossingen** en verwijder de volgende oplossingen in deze volgorde:
    1. Dynamics 365 Inventory Visibility - Verankering
    1. Dynamics 365 Inventory Visibility - Toepassing
    1. Dynamics 365 Inventory Visibility - Besturingselementen
    1. Dynamics 365 Inventory Visibility - Invoegtoepassingen
    1. Dynamics 365 Inventory Visibility - Basis

    Nadat u deze oplossingen hebt verwijderd, worden de gegevens die in tabellen zijn opgeslagen ook verwijderd.

> [!NOTE]
> Als u een Supply Chain Management-database herstelt nadat u de invoegtoepassing Voorraadzichtbaarheid hebt verwijderd en vervolgens de invoegtoepassing opnieuw wilt installeren, moet u voordat u de invoegtoepassing opnieuw installeert, de oude gegevens van voorraadzichtbaarheid verwijderen die in uw Dataverse-abonnement zijn opgeslagen (zoals is beschreven in de vorige procedure). Op deze manier voorkomt u mogelijke inconsistentieproblemen met gegevens.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a>Gegevens van voorraadzichtbaarheid opschonen in Dataverse voordat de Supply Chain Management-database wordt hersteld

Als u voorraadzichtbaarheid hebt gebruikt en uw Supply Chain Management-database vervolgens herstelt, bevat de herstelde database mogelijk gegevens die niet langer consistent zijn met gegevens die eerder door Voorraadzichtbaarheid zijn gesynchroniseerd met Dataverse. Deze gegevensinconsistentie kan systeemfouten en andere problemen veroorzaken. Het is daarom belangrijk dat u altijd alle gegevens van voorraadzichtbaarheid opschoont uit Dataverse voordat u een Supply Chain Management-database herstelt.

Gebruik de volgende procedure als u een Supply Chain Management-database wilt herstellen:

1. Verwijder de invoegtoepassing Voorraadzichtbaarheid en verwijder alle samenhangende gegevens in Dataverse, zoals beschreven in [De invoegtoepassing Voorraadzichtbaarheid verwijderen](#uninstall-add-in)
1. Herstel uw Supply Chain Management-database, bijvoorbeeld zoals wordt beschreven in [Tijdgebonden databaseherstel (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) of [Tijdgebonden herstel van de productiedatabase naar een sandboxomgeving](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Als u deze nog steeds wilt gebruiken, installeert u de invoegtoepassing Voorraadzichtbaarheid opnieuw en stelt u deze in zoals beschreven in [De invoegtoepassing Voorraadzichtbaarheid installeren](#install-add-in) en [Integratie met voorraadzichtbaarheid instellen](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
