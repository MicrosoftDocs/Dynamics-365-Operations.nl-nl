---
title: Bijwerken naar het model voor partij en globaal adresboek
description: In dit artikel wordt beschreven hoe u gegevens voor twee keer wegschrijven kunt upgraden naar het partij- en globale adresboekmodel.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 02ab3675db0d78efa1e4e43188d79bb1e763a713
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111813"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Bijwerken naar het model voor partij en globaal adresboek

[!include [banner](../../includes/banner.md)]



De [Microsoft Azure Data Factory-sjablonen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) helpen u bij het upgraden van de volgende bestaande gegevens met twee keer wegschrijven naar het partij- en globale adresboekmodel: gegevens in de tabellen **Account**, **Contactpersoon** en **Leverancier** en post- en elektronische adressen.

De volgende drie Data Factory-sjablonen zijn beschikbaar. Met de sjablonen worden de gegevens van zowel apps voor financiën en bedrijfsactiviteiten als apps voor Customer Engagement-apps afgestemd.

- **[Partijsjabloon](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Upgrade data to dual-write Party-GAB schema/arm_template.json)**: deze sjabloon helpt bij het bijwerken van gegevens van het type **Partij** en **Contactpersoon** die zijn gekoppeld aan gegevens in de tabellen **Account**, **Contactpersoon** en **Leverancier**.
- **[Sjabloon Postadres van partij](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Upgrade data to dual-write Party-GAB schema/Upgrade to Party Postal Address - GAB/arm_template.json)**: met deze sjabloon kunt u de postadressen bijwerken die zijn gekoppeld aan gegevens in de tabellen **Account**, **Contactpersoon** en **Leverancier**.
- **[Sjabloon Elektronisch adres van partij](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Upgrade data to dual-write Party-GAB schema/Upgrade to Party Electronic Address - GAB/arm_template.json)**: met deze sjabloon kunt u de elektronische adressen bijwerken die zijn gekoppeld aan gegevens in de tabellen **Account**, **Contactpersoon** en **Leverancier**.

Aan het einde van het proces worden de volgende CSV-bestanden (Comma Separated Values) gegenereerd.

| Bestandsnaam | Doel |
|---|---|
| FONewParty.csv | Met dit bestand kunt u nieuwe **Partij**-records maken in de app voor financiën en bedrijfsactiviteiten. |
| ImportFONewPostalAddressLocation.csv | Met dit bestand kunt u nieuwe **Postadreslocatie**-records maken in de app voor financiën en bedrijfsactiviteiten. |
| ImportFONewPartyPostalAddress.csv | Met dit bestand kunt u nieuwe **Partijpostadres**-records maken in de app voor financiën en bedrijfsactiviteiten. |
| ImportFONewPostalAddress.csv | Met dit bestand kunt u nieuwe **Postadres**-records maken in de app voor financiën en bedrijfsactiviteiten. |
| ImportFONewElectronicAddress.csv | Met dit bestand kunt u nieuwe **Elektronische adres**-records maken in de app voor financiën en bedrijfsactiviteiten. |

In dit artikel wordt uitgelegd hoe u de Data Factory-sjablonen kunt gebruiken en uw gegevens kunt upgraden. Als u geen aanpassingen hebt, kunt u de sjablonen ongewijzigd gebruiken. Als u echter aanpassingen hebt voor gegevens van het type **Account**, **Contactpersoon** en **Leverancier**, moet u de sjablonen wijzigen zoals beschreven in dit artikel.

> [!IMPORTANT]
> Er zijn speciale instructies voor het uitvoeren van de sjablonen voor postadressen voor partijen en elektronische adressen voor partijen. U moet eerst de sjabloon voor de partij uitvoeren, daarna de sjabloon voor het postadres van de partij en vervolgens de sjabloon voor het elektronisch adres van de partij. Elke sjabloon is ontworpen om in een afzonderlijke data factory te worden geïmporteerd.

## <a name="prerequisites"></a>Vereisten

Aan de volgende vereisten moet zijn voldaan om een upgrade naar het partij- en globale adresboekmodel te kunnen uitvoeren:

+ U moet over een [Azure-abonnement](https://portal.azure.com/) beschikken.
+ U moet toegang tot de [sjablonen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) hebben.
+ U moet een bestaande klant voor twee keer wegschrijven zijn.

## <a name="prepare-for-the-upgrade"></a>Upgrade voorbereiden

Voor een upgrade moet u de volgende voorbereidingen treffen:

+ **Volledige synchronisatie:** de omgeving Finance and Operations en de omgeving voor klantbetrokkenheid bevinden zich beide in volledig gesynchroniseerde toestand voor de tabellen **Account (klant)**, **Contactpersoon** en **Leverancier**.
+ **Integratiesleutels:** de tabellen **Account (klant)**, **Contactpersoon** en **Leverancier** in apps voor klantbetrokkenheid gebruiken de integratiesleutels die met het product worden meegeleverd. Als u de integratiesleutels hebt aangepast, moet u de sjabloon aanpassen.
+ **Partijnummer:** alle records uit de tabellen **Account (klant)**, **Contactpersoon** en **Leverancier** die worden bijgewerkt, hebben een partijnummer. Records zonder partijnummer worden genegeerd. Als u deze records wilt upgraden, voegt u er een partijnummer aan toe voordat u het upgradeproces start.
+ **Systeemstoring:** tijdens het upgradeproces moet u de client voor financiële en bedrijfsactiviteiten en de omgeving voor klantbetrokkenheid offline halen.
+ **Momentopname**: maak een momentopname van zowel de apps voor financiën en bedrijfsactiviteiten als Customer Engagement-apps. U kunt vervolgens de momentopnamen om de vorige toestand te herstellen als dat nodig is.

## <a name="deployment"></a>Implementatie

1. Download de sjablonen van [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Meld u aan bij de [Azure-portal](https://portal.azure.com/).
3. Maak een [resourcegroep](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Maak een [opslagaccount](/azure/storage/common/storage-account-create?tabs=azure-portal) in de resourcegroep die u hebt gemaakt.
5. Maak een [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in de resourcegroep die u hebt gemaakt.
6. Open de data factory en selecteer de tegel **Schrijven en controleren**.
7. Selecteer op het tabblad **Beheren** **ARM-sjabloon**.
8. Selecteer **ARM-sjabloon importeren** om de sjabloon **Partij** te importeren.
9. Importeer de sjabloon in de data factory. Voer de volgende waarden in voor **Projectdetails** en **Exemplaardetails**.

    | Veld | Waarde |
    |---|---|
    | Abonnement | Het Azure-abonnement |
    | Resourcegroep | Geef de resource op waaronder de opslagaccount is gemaakt. |
    | Regio | De regio |
    | Fabrieksnaam | De fabrieksnaam |
    | FO Linked Service_service Principal Key | De sleutel van de toepassing |
    | Azure Blob Storage_connection String | De verbindingsreeks voor Azure Blob Storage |
    | Dynamics Crm Linked Service_password | Het wachtwoord voor het gebruikersaccount dat u opgeeft als gebruikersnaam |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | Informatie (domeinnaam of tenant-id) over de tenant waaronder de toepassing zich bevindt |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | De client-id van de toepassing |
    | Dynamics Crm Linked Service_properties_type Properties_username | De gebruikersnaam die wordt gebruikt om verbinding te maken met Dynamics 365 |

    Zie de volgende onderwerpen voor meer informatie:

    - [Een Resource Manager-sjabloon handmatig een niveau verhogen voor elke omgeving](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Eigenschappen van gekoppelde service](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Gegevens kopiëren met Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Valideer na de implementatie de gegevenssets, gegevensstroom en gekoppelde service van de data factory.

    ![Gegevenssets, gegevensstroom en gekoppelde service.](media/data-factory-validate.png)

11. Ga naar **Beheren**. Selecteer **Gekoppelde service** onder **Verbindingen**. Selecteer vervolgens **DynamicsCrmLinkedService**. Voer in het dialoogvenster **Gekoppelde service bewerken (Dynamics CRM)** de volgende waarden in.

    | Veld | Waarde |
    |---|---|
    | Name | DynamicsCrmLinkedService |
    | Beschrijving | Gekoppelde services om verbinding te maken met CRM-exemplaar om entiteitengegevens op te halen |
    | Verbinding maken via integratieruntime | AutoResolvelntegrationRuntime |
    | Implementatietype | Online |
    | Service-URI | `https://<organization-name>.crm[x].dynamics.com` |
    | Verificatietype | Office365 |
    | Gebruikersnaam | |
    | Wachtwoord of Azure Key Vault | Wachtwoord |
    | Wachtwoord | |

## <a name="prepare-to-run-the-data-factory-templates"></a>De Data Factory-sjablonen voorbereiden voor uitvoering

In deze sectie worden de instellingen beschreven die vereist zijn voordat u de Data Factory-sjablonen Postadres partij en Elektronisch adres partij kunt uitvoeren.

### <a name="setup-to-run-the-party-postal-address-template"></a>Instellingen voor het uitvoeren van de sjabloon Postadres partij

1. Meld u aan bij apps voor klantbetrokkenheid en ga naar **Instellingen** \> **Persoonlijke instellingen**. Configureer vervolgens op het tabblad **Algemeen** de tijdzone-instelling voor de systeembeheerderaccount. De tijdzone moet in UTC (Coordinated Universal Time) zijn om de datums 'geldig vanaf' en 'geldig tot' van postadressen van apps voor financiën en bedrijfsactiviteiten te kunnen bijwerken.

    ![Tijdzone-instelling voor de systeembeheerderaccount.](media/ADF-1.png)

2. Maak in Data Factory, op het tabblad **Beheren** onder **Algemene parameters**, de volgende algemene parameter.

    | Nummer | Name | Type | Waarde |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | tekenreeks | Met deze parameter wordt een serienummer als voorvoegsel aan nieuwe postadressen toegevoegd. Zorg ervoor dat u een tekenreeks opgeeft die geen conflict veroorzaakt met postadressen in apps voor financiën en bedrijfsactiviteiten en Customer Engagement-apps. Gebruik bijvoorbeeld **ADF-PAD-**. |

    ![Algemene parameter PostalAddressIdPrefix die op het tabblad Beheren is gemaakt.](media/ADF-2.png)

3. Wanneer u gereed bent, selecteert u **Alles publiceren**.

    ![Knop Alles publiceren.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Instellingen voor het uitvoeren van de sjabloon Elektronisch adres partij

1. Maak in Data Factory, op het tabblad **Beheren** onder **Algemene parameters**, de volgende algemene parameters.

    | Nummer | Name | Type | Waarde |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Deze parameter bepaalt welke primaire systeemadressen bij conflicten worden vervangen. Als de waarde **waar** is, vervangen de primaire adressen in apps voor financiën en bedrijfsactiviteiten de primaire adressen in Customer Engagement-apps. Als de waarde **onwaar** is, vervangen de primaire adressen in Customer Engagement-apps de primaire adressen in apps voor financiën en bedrijfsactiviteiten. |
    | 2 | ElectronicAddressIdPrefix | tekenreeks | Met deze parameter wordt een serienummer als voorvoegsel aan nieuwe elektronische adressen toegevoegd. Zorg ervoor dat u een tekenreeks opgeeft die geen conflict veroorzaakt met elektronische adressen in apps voor financiën en bedrijfsactiviteiten en Customer Engagement-apps. Gebruik bijvoorbeeld **ADF-EAD-**. |

    ![Algemene parameters IsFOSource en ElectronicAddressIdPrefix worden gemaakt op het tabblad Beheren.](media/ADF-4.png)

2. Wanneer u gereed bent, selecteert u **Alles publiceren**.

## <a name="run-the-templates"></a>De sjablonen uitvoeren

1. Stop de volgende toewijzingen voor twee keer wegschrijven voor **Partij**, **Account**, **Contactpersoon** en **Leverancier** die gebruikmaken van de apps voor financiën en bedrijfsactiviteiten:

    + CDS-partijen (msdyn_parties) 
    + Klanten V3 (rekeningen)
    + Klanten V3(contacts)
    + CDS-contactpersonen V2(contacts)
    + CDS-contactpersonen V2(contacts)
    + Leverancier V2 (msdyn_vendor)
    + Contactpersonen V2 (msdyn_contactforparties)
    + CDS-postadreslocaties partij (msdyn_partypostaladdresses)
    + Historie van CDS-postadres V2 (msdyn_postaladdresses)
    + CDS-postadreslocaties (msdyn_postaladdresscollections)
    + Partijcontacten V3 (msdyn_partyelectronicaddresses)

2. Zorg ervoor dat de kaarten worden verwijderd uit de tabel **msdy_dualwriteruntimeconfig** in Dataverse.
3. Installeer [de oplossingen voor twee keer wegschrijven naar Partij en Globaal adresboek](https://aka.ms/dual-write-gab) uit AppSource.
4. Als de volgende tabellen gegevens bevatten in de app voor financiën en bedrijfsactiviteiten, moet u **Initiële synchronisatie** uitvoeren:

    + Aanhef
    + Persoonlijke karaktertypen
    + Afsluiting
    + Titels contactpersoon
    + Besluitvormingsrollen
    + Loyaliteitsniveaus

5. Schakel in de app voor klantbetrokkenheid de volgende invoegtoepassingsstappen uit:

    + Account bijwerken

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update van account
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update van account

    + Contactpersoon bijwerken

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update van contactpersoon
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update van contactpersoon

    + msdyn_party bijwerken

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update van msdyn_party

    + msdyn_vendor bijwerken

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update van msdyn_vendor

    + Customeraddress

        + Maken

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: maken van customeraddress

        + Bijwerken

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: bijwerken van customeraddress

        + Verwijderen

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: verwijderen van customeraddress

    + msdyn_partypostaladdress

        + Maken

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: maken van msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: maken van msdyn_partypostaladdress

        + Bijwerken

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: bijwerken van msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: bijwerken van msdyn_partypostaladdress

    + msdyn_postaladdress

        + Maken

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: maken van msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: maken van msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: maken van msdyn_postaladdress

        + Bijwerken

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: bijwerken van msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: bijwerken van msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Maken

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: maken van msdyn_partyelectronicaddress

        + Bijwerken

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: bijwerken van msdyn_partyelectronicaddress

        + Verwijderen

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: verwijderen van msdyn_partyelectronicaddress

6. Schakel in de app voor klantbetrokkenheid de volgende werkstromen uit:

    + Leveranciers maken in tabel Accounts
    + Leveranciers maken in tabel Accounts
    + Leveranciers van het type Persoon maken in de tabel Contactpersonen
    + Leveranciers van het type Persoon maken in tabel Leveranciers
    + Leveranciers bijwerken in tabel Accounts
    + Leveranciers bijwerken in tabel Leveranciers
    + Leveranciers van het type Persoon bijwerken in tabel Contactpersonen
    + Leveranciers van het type Persoon bijwerken in tabel Leveranciers

7. Voer in de data factory de sjabloon uit door **Trigger nu** te selecteren zoals wordt weergegeven in de volgende illustratie. Het kan enkele uren duren voordat dit proces is voltooid, afhankelijk van het gegevensvolume.

    ![De sjabloon uitvoeren.](media/data-factory-trigger.png)

    > [!NOTE]
    > Als u aanpassingen hebt voor **Account**, **Contactpersoon** en **Leverancier**, moet u de sjabloon wijzigen.

8. Importeer de nieuwe records voor **Partij** in de app voor financiën en bedrijfsactiviteiten.

    1. Download het bestand **FONewParty.csv** vanuit Azure Blob Storage. Het pad is **partybootstrapping/output/FONewParty.csv**.
    2. Converteer het bestand **FONewParty.csv** naar een Excel-bestand en importeer het Excel-bestand in de app voor financiën en bedrijfsactiviteiten. Als de CSV-import voor u werkt, kunt u ook het CSV-bestand rechtstreeks importeren. Het kan enkele uren duren voordat deze stap is voltooid, afhankelijk van het gegevensvolume. Meer informatie vindt u in [Overzicht van gegevensimport- en exporttaken](../data-import-export-job.md).

    ![De Dataverse-partijrecords importeren.](media/data-factory-import-party.png)

9. Voer in de data factory na elkaar de sjabloon voor het postadres van de partij en de sjabloon voor het elektronische adres van de partij uit.

    + Met de sjabloon voor het postadres van de partij wordt een upsert uitgevoerd van alle postadresrecords in de app voor klantbetrokkenheid en worden deze aan bijbehorende records van het type **Account**, **Contactpersoon** en **Leverancier** gekoppeld. Daarnaast worden drie CSV-bestanden gegenereerd: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv en ImportFONewPostalAddress.csv.
    + Met de sjabloon voor het elektronische adres van de partij wordt een upsert uitgevoerd van alle elektronische adressen in de app voor klantbetrokkenheid en worden deze aan bijbehorende records van het type **Account**, **Contactpersoon** en **Leverancier** gekoppeld. Daarnaast wordt één CSV-bestand gegenereerd: ImportFONewElectronicAddress.csv.

    ![De sjablonen voor het postadres van de partij en het elektronische adres van de partij uitvoeren.](media/ADF-7.png)

10. Als u de app voor financiën en bedrijfsactiviteiten met deze gegevens wilt bijwerken, moet u de CSV-bestanden converteren naar een Excel-werkmap en deze [importeren in de app voor financiën en bedrijfsactiviteiten](../data-import-export-job.md). Als de CSV-import voor u werkt, kunt u ook de CSV-bestanden rechtstreeks importeren. Het kan enkele uren duren voordat deze stap is voltooid, afhankelijk van het volume.

    ![Geslaagde import.](media/ADF-8.png)

11. Schakel in de app voor klantbetrokkenheid de volgende invoegtoepassingsstappen in:

    + Account bijwerken

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update van account
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update van account

    + Contactpersoon bijwerken

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update van contactpersoon
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update van contactpersoon

    + msdyn_party bijwerken

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update van msdyn_party

    + msdyn_vendor bijwerken

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update van msdyn_vendor

    + msdyn_partypostaladdress

        + Maken

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: maken van msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: maken van msdyn_partypostaladdress

        + Bijwerken

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: bijwerken van msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: bijwerken van msdyn_partypostaladdress

    + msdyn_postaladdress

        + Maken

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: maken van msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: maken van msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: maken van msdyn_postaladdress

        + Bijwerken

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: bijwerken van msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: bijwerken van msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Maken

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: maken van msdyn_partyelectronicaddress

        + Bijwerken

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: bijwerken van msdyn_partyelectronicaddress

        + Verwijderen

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: verwijderen van msdyn_partyelectronicaddress

12. Activeer in de app voor klantbetrokkenheid de volgende werkstromen als u deze eerder hebt gedeactiveerd:

    + Leveranciers maken in tabel Accounts
    + Leveranciers maken in tabel Accounts
    + Leveranciers van het type Persoon maken in de tabel Contactpersonen
    + Leveranciers van het type Persoon maken in tabel Leveranciers
    + Leveranciers bijwerken in tabel Accounts
    + Leveranciers bijwerken in tabel Leveranciers
    + Leveranciers van het type Persoon bijwerken in tabel Contactpersonen
    + Leveranciers van het type Persoon bijwerken in tabel Leveranciers

13. Aan de record **Partij** gerelateerde toewijzingen uitvoeren, zoals beschreven in [Partij en globaal adresboek](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Uitleg van de Data Factory-sjablonen

In dit gedeelte doorloopt u de stappen in elke Data Factory-sjabloon.

### <a name="steps-in-the-party-template"></a>Stappen in de partijsjabloon

1. In stap 1 tot en met 6 wordt bepaald welke bedrijven zijn ingeschakeld voor twee keer wegschrijven en wordt een filterclausule hiervoor gemaakt.
2. In stappen 7-1 tot en met 7-9 worden gegevens opgehaald uit de app voor financiën en bedrijfsactiviteiten en de Customer Engagement-app en worden die gegevens gefaseerd voor een upgrade.
3. In stappen 8 tot en met 9 wordt het partijnummer voor records van het type **Account**, **Contactpersoon** en **Leverancier** vergeleken voor de app voor financiën en bedrijfsactiviteiten en de Customer Engagement-app. Records zonder partijnummer worden overgeslagen.
4. In stap 10 worden u twee CSV-bestanden gegenereerd voor de partijrecords die moeten worden gemaakt in de Customer Engagement-app en de app voor financiën en bedrijfsactiviteiten.

    - **FOCDSParty.csv**: dit bestand bevat alle partijrecords van beide systemen, ongeacht of het bedrijf is ingeschakeld voor twee keer wegschrijven.
    - **FONewParty.csv**: dit bestand bevat een subset van de partijrecords waarvan Dataverse zich bewust is (bijvoorbeeld accounts van het type **Prospect**).

5. In stap 11 worden de partijen in de app voor klantbetrokkenheid gemaakt.
6. In stap 12 worden de globaal unieke id's (GUID's) van de partijen opgehaald vanuit de app voor klantbetrokkenheid en worden deze zodanig gefaseerd dat zij in de volgende stappen kunnen worden gekoppeld aan records van het type **Account**, **Contactpersoon** en **Leverancier**.
7. In stap 13 worden de records **Account**, **Contactpersoon** en **Leverancier** aan partij-GUID's gekoppeld.
8. In stappen 14-1 tot en met 14-3 worden de records **Account**, **Contactpersoon** en **Leverancier** bijgewerkt in de app voor klantbetrokkenheid met partij-GUID's.
9. In stappen 15-1 tot en met 15-3 worden records **Contactpersoon voor partij** voorbereid voor records **Accounct**, **Contactpersoon** en **Leverancier**.
10. In stappen 16-1 tot en met 16-7 worden verwijzingsgegevens opgehaald, zoals een aanhef en typen persoonlijke tekens, en aan records **Contactpersoon voor partij** gekoppeld.
11. In stap17 worden de records **Contactpersoon voor partij** samengevoegd voor records **Accounct**, **Contactpersoon** en **Leverancier**.
12. In stap 18 worden de records **Contactpersoon voor partij** geïmporteerd in de app voor klantbetrokkenheid.

### <a name="steps-in-the-party-postal-address-template"></a>Stappen in de sjabloon Postadres partij

1. In stappen 1-1 tot en met 1-10 worden gegevens opgehaald uit de app voor financiën en bedrijfsactiviteiten en de Customer Engagement-app en worden die gegevens gefaseerd voor een upgrade.
2. In stap 2 worden de postadresgegevens in de app voor financiën en bedrijfsactiviteiten gedenormaliseerd door het postadres en het postadres van de partij samen te voegen.
3. In stap 3 worden de adresgegevens voor accounts, contactpersonen en leveranciers gededupliceerd samengevoegd vanuit de app voor klantbetrokkenheid.
4. In stap 4 worden CSV-bestanden voor de app voor financiën en bedrijfsactiviteiten gemaakt om nieuwe adresgegevens te maken die zijn gebaseerd op adressen van accounts, contactpersonen en leveranciers.
5. In stap 5-1 worden CSV-bestanden gemaakt voor de Customer Engagement-app, waarmee alle adresgegevens kunnen worden gemaakt op basis van de app voor financiën en bedrijfsactiviteiten en de Customer Engagement-app.
6. In stap 5-2 worden de CSV-bestanden geconverteerd naar de importindeling van de app voor financiën en bedrijfsactiviteiten voor handmatige import.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. In stap 6 worden de gegevens van de postadresverzameling geïmporteerd in de app voor klantbetrokkenheid.
8. In stap 7 worden de gegevens van de postadresverzameling opgehaald vanuit de app voor klantbetrokkenheid.
9. In stap 8 worden klantadresgegevens gemaakt en aan een postadresverzamelings-id gekoppeld.
10. In stappen 9-1 tot en met 9-2 worden partij- en postadresinzamelings-id's gekoppeld aan postadressen en partijpostadressen.
11. In stappen 10-1 tot en met 10-3 worden klantadressen, postadressen en partijpostadressen geïmporteerd in de app voor klantbetrokkenheid.

### <a name="steps-in-the-party-electronic-address-template"></a>Stappen in de sjabloon Elektronisch adres partij

1. In stappen 1-1 tot en met 1-5 worden gegevens opgehaald uit de app voor financiën en bedrijfsactiviteiten en de Customer Engagement-app en worden die gegevens gefaseerd voor een upgrade.
2. In stap 2 worden elektronische adressen in de app voor klantbetrokkenheid geconsolideerd vanuit account-, contactpersoon- en leveranciersentiteiten.
3. In stap 3 worden primaire elektronische adresgegevens van de Customer Engagement-app en de app voor financiën en bedrijfsactiviteiten samengevoegd.
4. In stap 4 worden CSV-bestanden gemaakt.

    - Maak nieuwe elektronische adresgegevens voor de app voor financiën en bedrijfsactiviteiten op basis van account-, contactpersoon- en leveranciersadressen.
    - Maak nieuwe elektronische adresgegevens voor de Customer Engagement-app op basis van elektronisch adres, account-, contactpersoon- en leveranciersadressen in de app voor financiën en bedrijfsactiviteiten.

5. In stap 5-1 worden elektronische adressen geïmporteerd in de app voor klantbetrokkenheid.
6. In stap 5-2 worden CSV-bestanden gemaakt om primaire adressen voor accounts en contactpersonen bij te werken in de app voor klantbetrokkenheid.
7. In stappen 6-1 tot en met 6-2 worden accounts en primaire contactpersoonadressen geïmporteerd in de app voor klantbetrokkenheid.

## <a name="troubleshooting"></a>Problemen oplossen

1. Als het proces mislukt, voert u de data factory opnieuw uit. Begin vanaf de mislukte activiteit.
2. Sommige bestanden die door de data factory worden gegenereerd kunnen worden gebruikt om gegevens te valideren.
3. De data factory wordt uitgevoerd op basis van CSV-bestanden. Daarom kan een komma in een veldwaarde van invloed zijn op de resultaten. U moet alle komma's uit veldwaarden verwijderen.
4. Het tabblad **Controle** bevat informatie over alle stappen en gegevens die zijn verwerkt. Hier kunt u een specifieke stap selecteren voor foutopsporing.

    ![Tabblad Controle.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Meer informatie over de sjabloon

Zie [leesmij-bestand Opmerkingen voor Azure Data Factory-sjabloon](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) voor meer informatie over de sjabloon.

