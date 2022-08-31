---
title: Zoeken van hoofdgegevens voor btw-berekeningsconfiguratie inschakelen
description: In dit artikel wordt uitgelegd hoe u de zoekfunctie voor hoofdgegevens voor belastingberekening kunt instellen en inschakelen.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f9d882340171173e5e503f8b5e3aa856e8544b0
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306198"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Zoeken van hoofdgegevens voor btw-berekeningsconfiguratie inschakelen 

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u de zoekfunctie voor hoofdgegevens voor belastingberekening kunt instellen en inschakelen. Er is een vervolgkeuzelijst beschikbaar voor het selecteren van waarden in de belastingberekeningsconfiguratie voor velden, zoals **Rechtspersoon**, **Leveranciersrekening**, **Artikelcode** en **Leveringstermijn**. Deze waarden zijn afkomstig uit de verbonden Microsoft Dynamics 365 Finance-omgeving met de Microsoft Dataverse-gegevensbron.

> [!NOTE] 
> De functie voor het opzoeken van hoofdgegevens voor de belastingberekening is optionele functionaliteit. U kunt de volgende stappen overslaan als u de functie **Ondersteuning voor Dataverse-gegevensbronnen van de Belastingdienst** in Regulatory Configuration Service (RCS) uitschakelt. In dat geval is de vervolgkeuzelijst echter niet beschikbaar in de configuratie van de btw-berekening.

Als u de vervolgkeuzelijst in de functieversieconfiguratie van belastingberekening wilt inschakelen, gaat u als volgt te werk.

1. [Integratie van Microsoft Power Platform-integratie inschakelen en de Dataverse-omgeving openen.](#enable)
2. [Virtuele entiteiten voor financiën en bedrijfsactiviteiten installeren.](#install)
3. [Een Azure Active Directory-toepassing (Azure AD) registreren.](#register)
4. [App-machtigingen verlenen in apps voor financiën en bedrijfsactiviteiten.](#grant)
5. [De gegevensbron van de virtuele entiteit configureren.](#configure)
6. [Virtuele Dataverse-entiteiten inschakelen.](#virtual)
7. [De verbonden toepassing voor belastingberekening instellen.](#set-up)
8. [Configuratie voor Dataverse-modeltoewijzing importeren en instellen.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>Integratie van Microsoft Power Platform inschakelen en de Dataverse-omgeving openen

De integratie van apps voor financiën en bedrijfsactiviteiten met Microsoft Power Platform kan worden ingeschakeld wanneer u een nieuwe omgeving voor apps voor financiën en bedrijfsactiviteiten maakt in Microsoft Dynamics Lifecycle Services (LCS). Zie [Integratie van Microsoft Power Platform - Overzicht van invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor meer informatie. Als u klaar bent, wordt de naam van een Microsoft Power Platform-omgeving weergegeven in de sectie **Power Platform-integratie**.

1. Zoek in LCS in de omgeving voor financiën en bedrijfsactiviteiten in de sectie **Power Platform-integratie** de waarde voor **Naam omgeving** voor de gekoppelde omgeving en noteer de naam.

    [![Waarde omgevingsnaam.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. Selecteer in het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/environments) op het tabblad **Omgevingen** de omgeving die overeenkomt met de waarde voor **Naam omgeving** waar u een notitie van hebt gemaakt.
3. Zoek op de pagina **Details** de waarde voor **Omgevings-URL** van de Dataverse-omgeving. Maak een notitie van deze waarde, omdat u deze nodig hebt in [Stap 7. De verbonden toepassing voor belastingberekening instellen](#set-up).
4. Zorg ervoor dat u de Dataverse-omgeving in uw browser kunt openen door de waarde voor de **Omgevings-URL** te selecteren.

    [![Dataverse-omgevingspagina.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Houd de Dataverse-omgeving open in uw browser. U hebt deze nodig in [Stap 5. De gegevensbron van de virtuele entiteit configureren](#configure).

Zie [De Microsoft Power Platform-integratie inschakelen](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) voor meer informatie.

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>Virtuele entiteiten voor financiën en bedrijfsactiviteiten installeren

De Dataverse-oplossing voor virtuele entiteiten voor financiën en bedrijfsactiviteiten moet worden geïnstalleerd via de oplossing Microsoft AppSource voor virtuele entiteiten.

1. Zoek in AppSource de [virtuele entiteit voor financiën en bedrijfsactiviteiten](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Selecteer **Nu ophalen**.
3. Voer in het veld **Een omgeving selecteren** de waarde **Naam omgeving** in waarvan u eerder een notitie hebt gemaakt.
4. Schakel de selectievakjes in en selecteer vervolgens **Installeren**.

Wanneer de installatie is voltooid, kunt u de app **Virtuele entiteit voor financiën en bedrijfsactiviteiten** in het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/) vinden onder **Resources** \> **Dynamics 365-apps**.

Zie [De oplossing voor virtuele entiteiten ophalen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) voor meer informatie.

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Een Azure AD-toepassing registreren

U moet een Azure AD-toepassing registreren in dezelfde tenant als die van de apps voor financiën en bedrijfsactiviteiten, zodat deze kunnen worden aangeroepen door Dataverse.

1. Ga in de [Azure-portal](https://portal.azure.com) naar **Azure Active Directory \> App-registraties**.
2. Selecteer **Nieuwe registratie** en voer de volgende gegevens in:

    - **Naam**: voer een unieke naam in.
    - **Accounttype**: voer **Willekeurige Azure AD-map** in (één tenant of meerdere tenants).
    - **Omleidings-URI**: laat dit veld leeg.

3. Selecteer **Registreren**.
4. Noteer de waarde in het veld **Toepassings-id (client)**. U hebt deze later nog nodig.

    [![Id-waarde voor Azure AD-toepassing (client).](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Maak een symmetrische sleutel voor de toepassing.
6. Selecteer **Certificaten en geheimen** in de nieuwe toepassing.
7. Selecteer **Nieuw clientgeheim**.
8. Voer een omschrijving in, selecteer een vervaldatum en selecteer **Opslaan**. Er wordt een sleutel gemaakt en weergegeven. Kopieer de waarde voor later gebruik.

Zie [Azure AD-toepassing registreren](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal) voor meer informatie.

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>App-machtigingen verlenen in apps voor financiën en bedrijfsactiviteiten

Dataverse maakt gebruik van de Azure AD-toepassing die u hebt gemaakt om de apps voor financiën en bedrijfsactiviteiten aan te roepen. Daarom moet de toepassing worden vertrouwd door de apps voor financiën en bedrijfsactiviteiten en worden gekoppeld aan een gebruikersaccount met de juiste rechten. In de apps voor financiën en bedrijfsactiviteiten moet u een speciale servicegebruiker maken die **alleen** rechten heeft voor de functionaliteit van de virtuele entiteit. Deze servicegebruiker mag geen andere rechten hebben. Nadat u deze stap hebt voltooid, kan elke toepassing die het geheim van de Azure AD-toepassing heeft, de omgeving van de apps voor financiën en bedrijfsactiviteiten aanroepen en de functionaliteit van de virtuele entiteit openen.

1. Ga in uw omgeving naar **Systeembeheer** \> **Gebruikers** \> **Gebruikers**.
2. Selecteer **Nieuw** om een nieuwe gebruiker toe te voegen en voer de volgende gegevens in:

    - **Gebruikers-id**: voer **dataverseintegration** of een andere waarde in.
    - **Gebruikersnaam**: voer **dataverse integration** of een andere waarde in.
    - **Provider**: stel dit veld in op **NonAAD.**
    - **E-mail**: voer **dataverseintegration** of een andere waarde in. (De waarde hoeft geen geldig e-mailaccount te zijn.)

3. Wijs de beveiligingsrol **Integratie-app voor virtuele Dataverse-entiteiten** aan de gebruiker toe.
4. Verwijder alle andere rollen, zoals **Systeemgebruiker**.
5. Ga naar **Systeembeheer** \> **Instellingen** \> **Azure Active Directory-toepassingen** om Dataverse te registreren. 
6. Voeg een rij toe en voer vervolgens in het veld **Client-id** de waarde **Id toepassing (client)** in waarvan u eerder een notitie hebt gemaakt.
7. Voer in het veld **Naam** een naam in. Voer bijvoorbeeld **Dataverse-integratie** in.
8. Voer in het veld **Gebruikers-id** de gebruikers-id in die u eerder hebt gemaakt.

Zie voor meer informatie [App-machtigingen verlenen in apps voor financiën en bedrijfsactiviteiten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>De gegevensbron van de virtuele entiteit configureren

U moet Dataverse opgeven met de app-instantie voor financiën en bedrijfsactiviteiten waarmee verbinding moet worden gemaakt.

1. Uw Dataverse-omgeving moet nog steeds open zijn in uw browser vanuit [Stap 1. Integratie van Microsoft Power Platform inschakelen en de Dataverse-omgeving openen](#enable). Selecteer de knop Instellingen (het tandwielsymbool) rechtsboven en selecteer **Geavanceerde instellingen**.

    [![Geavanceerde instellingen in de Dataverse-omgeving openen.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. Selecteer **Beheer** in het vervolgkeuzemenu **Instellingen**.

    [![Beheer.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Selecteer **Gegevensbronnen van virtuele entiteit**.

    [![Gegevensbronnen van virtuele entiteit.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Selecteer de gegevensbron met de naam **Financiën en bedrijfsactiviteiten**.

    [![Gegevensbron voor financiën en bedrijfsactiviteiten.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Voer de volgende gegevens uit eerdere stappen in:

    - **Doel-URL**: voer de URL in waarmee u toegang kunt krijgen tot de apps voor financiën en bedrijfsactiviteiten.
    - **OAuth-URL**: voer `https://login.windows.net/` in.
    - **Tenant-id**: geef uw tenant op. Deze waarde kan de domeinnaam van uw bedrijfse-mail zijn (zoals contoso.com).
    - **AAD-toepassings-id**: voer de eerder gemaakte waarde voor **Id van toepassing (client)** in.
    - **AAD-toepassingsgeheim**: voer het geheim in dat eerder is gegenereerd.
    - **AAD-resource**: voer **00000015-0000-0000-c000-000000000000** in. Deze waarde is de Azure AD-toepassing waarmee apps voor financiën en bedrijfsactiviteiten worden vertegenwoordigd. Dit moet altijd dezelfde waarde zijn.

6. Sla de wijzigingen op.
7. Sluit de pagina om terug te keren naar de pagina **Beheer**, waar u met [Stap 6. Virtuele entiteiten van Dataverse inschakelen](#virtual) begint.

    [![De entiteit afsluiten voor bewerking.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Zie [De gegevensbron van de virtuele entiteit configureren](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source) voor meer informatie.

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>Virtuele Dataverse-entiteiten inschakelen

De zichtbaarheid van de virtuele entiteiten van apps voor financiën en bedrijfsactiviteiten moet worden ingesteld op **Ja** voordat ze kunnen worden verbruikt door de configuratie voor belastingberekening.

> [!NOTE]
> U kunt deze stap overslaan door de aan de belastingberekening gerelateerde virtuele entiteiten met slechts één klik in te schakelen in [Stap 8. De verbonden toepassing voor belastingberekening instellen](#import). Het is echter raadzaam om ten minste één virtuele entiteit handmatig in te schakelen om aan te geven dat de verbinding tussen apps voor financiën en bedrijfsactiviteiten en Dataverse goed tot stand is gekomen.

1. Selecteer in uw Dataverse-omgeving op de pagina **Beheer** de filterknop (trechtersymbool) in de rechterbovenhoek.

    [![Filterknop.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Selecteer in het venster **Geavanceerd zoeken** in het veld **Zoeken naar** de optie **Beschikbare entiteiten voor financiën en bedrijfsactiviteiten**.
3. Voeg de volgende regel toe: **Naam** – **Bevat** – **CompanyInfoEntity**. Selecteer vervolgens **Resultaten**.

    [![Venster Geavanceerd zoeken.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Selecteer **CompanyInfoEntity** in de zoekresultaten, schakel het selectievakje **Zichtbaar** in en selecteer vervolgens **Opslaan**.

    [![Entiteitszichtbaarheid instellen.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Herhaal de voorgaande stappen voor de volgende entiteiten waarnaar in de configuratie van belastingberekening wordt verwezen:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Alleen de eerste 5000 records van een entiteit kunnen worden opgehaald door Dataverse en beschikbaar worden gemaakt in de vervolgkeuzelijst van de configuratie voor belastingberekening.

Zie [Virtuele Microsoft Dataverse-entiteiten inschakelen](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md) voor meer informatie.

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>De verbonden toepassing voor belastingberekening instellen

1. Ga naar **Elektronische rapportage** en selecteer vervolgens in de sectie **Verwante koppelingen** de optie **Verbonden toepassingen**.

    [![Verbonden toepassingen.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

2. Selecteer **Nieuw** om een record toe te voegen en voer de volgende gegevens in.

    - **Naam**: voer een naam in.
    - **Type**: selecteer **Dataverse**.
    - **Toepassing**: voer de waarde voor **Omgevings-URL** van uw Dataverse-omgeving in waarvan u in [Stap 1. Microsoft Power Platform-integratie inschakelen en uw Dataverse-omgeving openen](#enable) een notitie hebt gemaakt.
    - **Tenant**: voer uw tenant in.
    - **Aangepaste URL**: voer uw Dataverse-URL in en voeg **api/data/v9.1** eraan toe.

3. Schakel **Verbinding controleren** in en selecteer vervolgens in het dialoogvenster **Hier klikken om verbinding te maken met geselecteerde externe toepassing**.

    [![De verbinding controleren.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
4. Controleer dat u het bericht 'Geslaagd' ontvangt waarmee wordt aangegeven dat de verbinding met succes tot stand is gekomen.

    [![Succesbericht.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)
    
5. Open in RCS het werkgebied **Functiebeheer** en schakel de volgende functies in:

    - Globalisatiefuncties
    - Ondersteuning voor Dataverse-gegevensbronnen voor elektronische rapportage
    - Ondersteuning voor Dataverse-gegevensbronnen van de Belastingdienst

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>Configuratie voor Dataverse-modeltoewijzing importeren en instellen

Microsoft biedt standaardconfiguraties voor modeltoewijzingen voor entiteiten van apps voor financiën en bedrijfsactiviteiten tot belastingberekening.

1. Ga in RCS naar **Elektronische rapportage**.
2. Selecteer in de sectie **Configuratieproviders** op de tegel voor de **Microsoft**-provider **Opslagplaatsen**.

    [![Opslagplaatsen.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Selecteer de record **Algemene configuratieopslagplaats** en selecteer vervolgens **Openen**.
4. Selecteer onder **Belastinggegevensmodel** \> **Belastingberekeningsgegevensmodel** de configuratie **Dataverse-modeltoewijzing**.
5. Selecteer op het sneltabblad **Versies** een versie die overeenkomt met uw versie van apps voor financiën en bedrijfsactiviteiten en selecteer vervolgens **Importeren**.

    [![De configuratie van de Dataverse-modeltoewijzing importeren](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > De configuratie **Dataverse-modeltoewijzing** geldt alleen voor de hoogste geïmporteerde versie. Daarom moet u geen versie van de configuratie **Dataverse-modeltoewijzing** importeren die hoger is dan de versie van de belastingberekeningsconfiguratie die u wilt implementeren. Als u bijvoorbeeld versie 40.50.225 van de belastingberekeningsconfiguratie wilt implementeren, moet u alleen versie 40.50.13 van de configuratie **Dataverse-modeltoewijzing** importeren. Importeer versie 40.54.14 niet. Anders komt de configuratie niet overeen met het gegevensmodel.

6. Ga terug naar **Elektronische rapportage** en selecteer de tegel **Belastingconfiguraties**.
7. Selecteer de geïmporteerde configuratie **Dataverse-modeltoewijzing** en selecteer vervolgens **Bewerken**.
8. Stel de optie **Standaard voor modeltoewijzing** in op **Ja**.
9. Selecteer in het veld **Verbonden toepassing** de verbonden toepassing die u hebt ingesteld in [Stap 7. De verbonden toepassing voor belastingberekening instellen](#set-up).
10. Stel de optie **Zichtbaarheid virtuele tabel instellen** op **Ja** in als u alle virtuele entiteiten die betrekking hebben op belastingberekening zichtbaar wilt maken.

U hebt nu de instellingen voor de zoekfunctie voor hoofdgegevens voltooid. Een vervolgkeuzelijst voor velden zoals **Rechtspersoon**, **Leverancierrekening**, **Artikelcode** en **Leveringsvoorwaarde** van Dynamics 365 Finance wordt nu ingeschakeld in de instellingen voor **Versie van functie voor belastingberekening**.

[![Vervolgkeuzelijst Rechtspersoon.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
