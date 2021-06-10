---
title: Bijwerken naar het model voor partij en globaal adresboek
description: In dit onderwerp wordt beschreven hoe u gegevens voor twee keer wegschrijven kunt upgraden naar het partij- en globale adresboekmodel.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112668"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Bijwerken naar het model voor partij en globaal adresboek

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Met de [Microsoft Azure Data Factory-sjabloon](https://aka.ms/dual-write-gab-adf) kunt u bestaande tabelgegevens voor **Account**, **Contactpersoon** en **Leverancier** met twee keer wegschrijven upgraden naar het partij- en globale adresboekmodel. Met de sjabloon worden de gegevens van zowel Finance and Operations-apps als Customer Engagement-applicaties afgestemd. Aan het einde van het proces worden de velden **Partij** en **Contactpersoon** gemaakt voor **partijrecords** en gekoppeld aan **account-**, **contactpersoon-** en **leveranciers** records in klantbetrokkenheidstoepassingen. Er wordt een .csv-bestand (`FONewParty.csv`) gegenereerd om nieuwe **Partij**-records te maken in de Finance and Operations-app . Dit onderwerp bevat instructies voor het gebruik van de Data Factory-sjabloon en het upgraden van uw gegevens.

Als u geen aanpassingen hebt, kunt u de sjabloon ongewijzigd gebruiken. Als u aanpassingen hebt voor **Account**, **Contactpersoon** en **Leverancier**, moet u de sjabloon wijzigen met behulp van de volgende instructies.

> [!NOTE]
> Met de sjabloon wordt alleen een upgrade uitgevoerd op de **Partij**-gegevens . In een toekomstige release zullen post- en elektronische adressen worden opgenomen.

## <a name="prerequisites"></a>Vereisten

De volgende vereisten zijn vereist om een upgrade naar het partij- en globale adresboekmodel uit te voeren:

+ [Azure-abonnement](https://portal.azure.com/)
+ [Toegang tot de sjabloon](https://aka.ms/dual-write-gab-adf)
+ U moet een bestaande klant voor twee keer wegschrijven zijn.

## <a name="prepare-for-the-upgrade"></a>Upgrade voorbereiden
Ter voorbereiding op de upgrade zijn de volgende activiteiten nodig:

+ **Volledig gesynchroniseerd**: beide omgevingen zijn volledig gesynchroniseerd voor **Account (klant)**, **Contactpersoon** en **Leverancier**.
+ **Integratiesleutels:** de tabellen **Account (klant)**, **Contactpersoon** en **Leverancier** in apps voor klantbetrokkenheid gebruiken de integratiesleutels die met het product worden verzonden. Als u de integratiesleutels hebt aangepast, moet u de sjabloon aanpassen.
+ **Partijnummer**: alle records van **Account (klant)**, **Contactpersoon** en **Leverancier** die worden bijgewerkt, hebben een **partijnummer**. Records zonder **partijnummer** worden genegeerd. Als u deze records wilt upgraden, voegt u er een **partijnummer** aan toe voordat u het upgradeproces start.
+ **Systeemstoring**: tijdens het upgradeproces moet u de omgevingen van Finance and Operations en Customer Engagement offline halen.
+ **Momentopname**: maak momentopnames van zowel Finance and Operations- als Customer Engagement-apps. Gebruik de momentopnamen om de vorige status te herstellen als dat nodig is.

## <a name="deployment"></a>Implementatie

1. Download de sjabloon van [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).

2. Meld u aan bij [Microsoft Azure](https://portal.azure.com/).

3. Maak een [resourcegroep](/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Maak een [opslagaccount](/azure/storage/common/storage-account-create?tabs=azure-portal) in de resourcegroep die u hebt gemaakt.

5. Maak een [data factory](/azure/data-factory/quickstart-create-data-factory-portal) boven de resourcegroep die u hebt gemaakt.

6. Open de data factory en selecteer de tegel **Author & Monitor**.

7. Selecteer op het tabblad **Beheren** **ARM-sjabloon**.

8. Selecteer **ARM-sjabloon importeren** om de **partijsjabloon** te importeren.

9. Importeer de sjabloon in de data factory. Voer de volgende waarden in voor **Projectdetails** en **Exemplaardetails**.

    Veld | Waarde
    ---|---
    Abonnement | Azure-abonnement
    Resourcegroep | Geef dezelfde resource op waaronder een opslagaccount wordt gemaakt.
    Regio | Geef regio op.
    Fabrieksnaam | Geef de fabrieksnaam op.
    FO Linked Service_service Principal Key | Geef de sleutel van de toepassing op.
    Azure Blob Storage_connection String | Azure Blob storage connection string.
    Dynamics Crm Linked Service_password | Het wachtwoord voor het gebruikersaccount dat u hebt opgegeven als gebruikersnaam.
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | Geef de tenant (domeinnaam of tenant-id) op waaronder de toepassing zich bevindt.
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | Geef de client-id van de toepassing op.
    Dynamics Crm Linked Service_properties_type Properties_username | De gebruikersnaam om verbinding te maken met Dynamics 365.

    Raadpleeg de volgende onderwerpen voor meer informatie: 
    
    - [Een Resource Manager-sjabloon handmatig een niveau verhogen voor elke omgeving](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Eigenschappen van gekoppelde service](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Gegevens kopiëren met Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Valideer na de implementatie de gegevenssets, gegevensstroom en gekoppelde service van de data factory.

   ![Gegevenssets, gegevensstroom en gekoppelde service](media/data-factory-validate.png)

11. Navigeer naar **Beheren**. Selecteer **Gekoppelde service** onder **Verbindingen**. Selecteer **DynamicsCrmLinkedService**. Voer in het formulier **Gekoppelde service bewerken (Dynamics CRM)** de volgende waarden in.

    Veld | Waarde
    ---|---
    Naam | DynamicsCrmLinkedService
    Beschrijving | Gekoppelde services om verbinding te maken met CRM-exemplaar om entiteitengegevens op te halen
    Verbinding maken via integratieruntime | AutoResolvelntegrationRuntime
    Implementatietype | Online
    Service-URI | `https://<organization-name>.crm[x].dynamics.com`
    Verificatietype | Office365
    Gebruikersnaam |
    Wachtwoord of Azure Key Vault | Wachtwoord
    Wachtwoord |

## <a name="run-the-template"></a>De sjabloon uitvoeren

1. Stop de volgende toewijzingen voor twee keer wegschrijven voor **Account**, **Contactpersoon** en **Leverancier** met de Finance and Operations-app.

    + Klanten V3 (rekeningen)
    + Klanten V3(contacts)
    + CDS-contactpersonen V2(contacts)
    + CDS-contactpersonen V2(contacts)
    + Leverancier V2 (msdyn_vendor)

2. Zorg ervoor dat de kaarten worden verwijderd uit de tabel `msdy_dualwriteruntimeconfig` in Dataverse.

3. Installeer [de oplossingen voor twee keer wegschrijven naar Partij en Globaal adresboek](https://aka.ms/dual-write-gab) uit AppSource.

4. Als de volgende tabellen gegevens bevatten in de Finance and Operations-app, moet u **Initiële synchronisatie** uitvoeren.

    + Aanhef
    + Persoonlijke karaktertypen
    + Afsluiting
    + Titels contactpersoon
    + Besluitvormingsrollen
    + Loyaliteitsniveaus

5. Schakel in de Customer Engagement-app de volgende invoegtoepassingsstappen uit.

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

6. Schakel in de app voor klantbetrokkenheid de volgende werkstromen uit:

    + Leveranciers maken in tabel Accounts
    + Leveranciers maken in tabel Accounts
    + Leveranciers van het type Persoon maken in de tabel Contactpersonen
    + Leveranciers van het type Persoon maken in tabel Leveranciers
    + Leveranciers bijwerken in tabel Accounts
    + Leveranciers bijwerken in tabel Leveranciers
    + Leveranciers van het type Persoon bijwerken in tabel Contactpersonen
    + Leveranciers van het type Persoon bijwerken in tabel Leveranciers

7. Voer in de data factory de sjabloon uit door **Trigger nu** te selecteren zoals wordt weergegeven in de volgende afbeelding. Dit proces kan enkele uren duren op basis van het gegevensvolume.

    ![Triggeruitvoering](media/data-factory-trigger.png)

    > [!NOTE]
    > Als u aanpassingen hebt voor **Account**, **Contactpersoon** en **Leverancier**, moet u de sjabloon wijzigen.

8. Importeer de **nieuwe records voor Partij** in de Finance and Operations-app.

    + Download het bestand `FONewParty.csv` vanuit Azure Blob Storage. Het pad is `partybootstrapping/output/FONewParty.csv`.
    + Converteer het bestand `FONewParty.csv` naar een Excel-bestand en importeer het Excel-bestand in de Finance and Operations-app. Als de CSV-import voor u werkt, kunt u het CSV-bestand direct importeren. Afhankelijk van het gegevensvolume kan het importeren enkele uren duren. Meer informatie vindt u in [Overzicht van gegevensimport- en exporttaken](../data-import-export-job.md).

    ![De partijrecords van Dataverse importeren](media/data-factory-import-party.png)

9. Schakel in de Customer Engagement-apps de volgende invoegtoepassingsstappen in:

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

10. Activeer in de apps voor klantbetrokkenheid de volgende werkstromen als u ze in vorige stappen hebt uitgeschakeld:

    + Leveranciers maken in tabel Accounts
    + Leveranciers maken in tabel Accounts
    + Leveranciers van het type Persoon maken in de tabel Contactpersonen
    + Leveranciers van het type Persoon maken in tabel Leveranciers
    + Leveranciers bijwerken in tabel Accounts
    + Leveranciers bijwerken in tabel Leveranciers
    + Leveranciers van het type Persoon bijwerken in tabel Contactpersonen
    + Leveranciers van het type Persoon bijwerken in tabel Leveranciers

11. Voer de **partij**-gerelateerde kaarten uit, zoals wordt aangegeven in [Partij en globaal adresboek](party-gab.md).

## <a name="troubleshooting"></a>Problemen oplossen

1. Als het proces mislukt, moet u de data factory opnieuw starten vanaf de mislukte activiteit.
2. Sommige bestanden worden gegenereerd door de data factory. U kunt deze gebruiken om gegevens te valideren.
3. De data factory wordt uitgevoerd op basis van csv-bestanden met door komma's gescheiden waarden. Als er een veldwaarde is met komma's, kan dit invloed hebben op de resultaten. U moet de komma's verwijderen.
4. Het tabblad **Controle** bevat informatie over alle stappen en verwerkte gegevens. Hier kunt u een specifieke stap selecteren voor foutopsporing.

    ![Tabblad Controle](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Meer informatie over de sjabloon

U kunt extra informatie over de sjabloon vinden in het [leesmij-bestand Opmerkingen voor Azure Data Factory-sjabloon ](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
