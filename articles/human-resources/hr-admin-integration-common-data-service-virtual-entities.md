---
title: Virtuele Dataverse-tabellen configureren
description: In dit onderwerp wordt beschreven hoe u virtuele tabellen configureert voor Dynamics 365 Human Resources. Genereer bestaande virtuele tabellen, werk ze bij en analyseer gegenereerde en beschikbare tabellen.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd299b51e38cc30c3e18f3ef9de1f43fa817b840
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112123"
---
# <a name="configure-dataverse-virtual-tables"></a>Virtuele Dataverse-tabellen configureren

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources is een virtuele gegevensbron in Microsoft Dataverse. De gegevensbron biedt volledige bewerkingen voor maken, lezen, bijwerken en verwijderen vanuit Dataverse en Microsoft Power Platform. De gegevens voor virtuele tabellen worden niet opgeslagen in Dataverse, maar in de toepassingsdatabase.

Als u bewerkingen voor maken, lezen, bijwerken en verwijderen voor entiteiten van Human Resources wilt inschakelen vanuit Dataverse, moet u de entiteiten beschikbaar maken als virtuele tabellen in Dataverse. Op deze manier kunt u bewerkingen voor maken, lezen, bijwerken en verwijderen uitvoeren vanuit Dataverse en Microsoft Power Platform op gegevens in Human Resources. De bewerkingen ondersteunen ook de validaties van de volledige bedrijfslogica van Human Resources om de gegevensintegriteit te waarborgen bij het schrijven van gegevens naar de entiteiten.

> [!NOTE]
> Human Resources-entiteiten komen overeen met Dataverse-tabellen. Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Beschikbare virtuele tabellen voor Human Resources

Alle OData-entiteiten (Open Data Protocol) in Human Resources zijn beschikbaar als virtuele tabellen in Dataverse. Ze zijn ook beschikbaar in Power Platform. U kunt nu apps en ervaringen met gegevens rechtstreeks vanuit Human Resources maken met alle mogelijkheden voor maken, lezen, bijwerken en verwijderen, zonder dat u gegevens hoeft te kopiëren of synchroniseren naar Dataverse. U kunt Power Apps-portals gebruiken om extern gerichte websites te maken die samenwerkingsscenario's mogelijk maken voor bedrijfsprocessen in Human Resources.

U kunt de lijst met virtuele tabellen die in de omgeving zijn ingeschakeld, weergeven en in [Power Apps](https://make.powerapps.com) met de tabellen gaan werken in de oplossing **Dynamics 365 HR Virtual Tables**.

![Dynamics 365 HR Virtual Tables in Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtuele tabellen versus native tabellen

Virtuele tabellen voor Human Resources zijn niet hetzelfde als de native Dataverse-tabellen die voor Human Resources zijn gemaakt. 

De native tabellen voor Human Resources worden afzonderlijk gegenereerd en onderhouden in de HCM Common-oplossing in Dataverse. Met native tabellen worden de gegevens opgeslagen in Dataverse en is synchronisatie met de Human Resources-toepassingdatabase vereist.

> [!NOTE]
> Zie [Dataverse-tabellen](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities) voor een lijst met de native Dataverse-tabellen voor Human Resources.

## <a name="setup"></a>Instelling

Volg deze instellingsstappen om virtuele tabellen in uw omgeving in te schakelen.

### <a name="enable-virtual-tables-in-human-resources"></a>Virtuele tabellen in Human Resources inschakelen

Eerst moet u virtuele tabellen inschakelen in de werkruimte **Functiebeheer**.

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Selecteer de tegel **Functiebeheer**.

3. Selecteer **Ondersteuning van virtuele tabellen voor HR in Dataverse** en selecteer **Inschakelen**.

Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het in- en uitschakelen van previewfuncties.

### <a name="register-the-app-in-microsoft-azure"></a>De app registreren in Microsoft Azure

U moet uw Human Resources-exemplaar registreren in de Azure-portal, zodat het Microsoft-identiteitsplatform verificatie- en machtigingsservices kan bieden voor de app en de gebruikers. Ga voor meer informatie over het registreren van apps in Azure naar [Snelstart: Een toepassing registreren bij het Microsoft-identiteitsplatform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Open de [Microsoft Azure-portal](https://portal.azure.com).

2. Selecteer in de lijst Azure-services de optie **App-registraties**.

3. Selecteer **Nieuwe registratie**.

4. Voer in het veld **Naam** een beschrijvende naam voor de app in. Bijvoorbeeld, **Dynamics 365 Human Resources Virtuele tabellen**.

5. Voer in het veld **URI omleiden** de naamruimte-URL in van uw instantie van Human Resources.

6. Selecteer **Registreren**.

7. Wanneer de registratie is voltooid, wordt in de Azure-portal het deelvenster **Overzicht** van de app-registratie weergegeven met de bijbehorende **Id van toepassing (client)**. Maak nu een notitie van de **Id van toepassing (client)**. U voert deze gegevens in wanneer u [de gegevensbron van de virtuele tabel configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. Selecteer in het linkernavigatievenster de optie **Certificaten en geheimen**.

9. Selecteer in het gedeelte **Clientgeheimen** van de pagina de optie **Nieuw clientgeheim**.

10. Geef een omschrijving op, selecteer een duur en selecteer **Toevoegen**.

11. Leg de waarde van het geheim vast. U voert deze gegevens in wanneer u [de gegevensbron van de virtuele tabel configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Maak nu een notitie van de waarde van het geheim. Het geheim wordt nooit meer weergegeven nadat u deze pagina hebt verlaten.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>De Dynamics 365 HR Virtual Table-app installeren

Installeer de Dynamics 365 HR Virtual Table-app in uw Power Apps-omgeving om het pakket van de virtuele tabel te implementeren naar Dataverse.

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2. Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.

3. Selecteer in het gedeelte **Resources** van de pagina de optie **Dynamics 365-apps**.

4. Selecteer de actie **App installeren**.

5. Selecteer **Dynamics 365 HR Virtual Table** en selecteer **Volgende**.

6. Controleer en markeer om de servicevoorwaarden te accepteren.

7. Selecteer **Installeren**.

De installatie duurt een paar minuten. Wanneer de installatie is voltooid, gaat u door naar de volgende stappen.

![De Dynamics 365 HR Virtual Table-app installeren vanuit het Power Platform-beheercentrum](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a>De gegevensbron van de virtuele tabel configureren 

In de volgende stap configureert u de gegevensbron van de virtuele tabel in de Power Apps-omgeving. 

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2. Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.

3. Selecteer de **Omgevings-URL** in het gedeelte **Details** van de pagina.

4. Selecteer op de **Oplossingsstatushub** het pictogram **Geavanceerd zoeken** in de rechtsbovenhoek van de toepassingspagina.

5. Selecteer op de pagina **Geavanceerd zoeken** in de vervolgkeuzelijst **Zoeken naar** de optie **Finance and Operations Virtual Data Source Configurations**.

6. Selecteer **Resultaten**.

7. Selecteer de record **Microsoft HR-gegevensbron**.

8. Voer de vereiste informatie in voor de gegevensbronconfiguratie:

   - **Doel-URL** : de URL van uw Human Resources-naamruimte. De doel-URL heeft het volgende formaat:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Bijvoorbeeld:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Vergeet niet het "**/**"-teken aan het einde van de URL toe te voegen om te voorkomen dat er een fout optreedt.

   - **Tenant-id**: de tenant-id van Azure Active Directory (Azure AD).

   - **AAD-toepassings-id** : de toepassings-id (client) die is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd. U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD-toepassingsgeheim**: het clientgeheim dat is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd. U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft HR-gegevensbron](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Selecteer **Opslaan en sluiten**.

### <a name="grant-app-permissions-in-human-resources"></a>App-machtigingen verlenen in Human Resources

Verleen als volgt machtigingen voor de twee Azure AD-toepassingen in Human Resources:

- De app die is gemaakt voor uw tenant in de Microsoft Azure-portal
- De Dynamics 365 HR Virtual Table-app die is geïnstalleerd in de Power Apps-omgeving 

1. Open in Human Resources de pagina **Azure Active Directory-toepassingen**.

2. Selecteer **Nieuw** om een nieuwe toepassingsrecord te maken.

    - Voer in het veld **Client-id** de client-id in van de app die u in de Microsoft Azure-portal hebt geregistreerd.
    - Voer in het veld **Naam** de naam in van de app die u in de Microsoft Azure-portal hebt geregistreerd.
    - Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.

3. Selecteer **Nieuw** om een tweede toepassingsrecord te maken.

    - **Client-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Naam**: Dynamics 365 HR Virtual Table
    - Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.

## <a name="generate-virtual-tables"></a>Virtuele tabellen genereren

Wanneer het instellen is voltooid, kunt u de virtuele tabellen selecteren die u in uw Dataverse-exemplaar wilt genereren en inschakelen.

1. Open in Human Resources de pagina **Integratie met Dataverse**.

2. Selecteer het tabblad **Virtuele tabellen**.

> [!NOTE]
> De wisselknop **Virtuele tabellen inschakelen** wordt automatisch ingesteld op **Ja** als alle vereiste instellingen zijn voltooid. Als de wisselknop is ingesteld op **Nee**, controleert u de stappen in vorige secties van dit document om ervoor te zorgen dat alle vereiste instellingen worden voltooid.

3. Selecteer de tabel of tabellen die u wilt genereren in Dataverse.

4. Selecteer **Genereren/vernieuwen**.

![Integratie met Dataverse](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a>Status van het genereren van tabellen controleren

Virtuele tabellen worden gegenereerd in Dataverse via een asynchroon achtergrondproces. Updates in de procesweergave in het actiecentrum. Details over het proces, waaronder foutlogboeken, worden weergegeven op de pagina **Procesautomatiseringen**.

1. Open in Human Resources de pagina **Procesautomatiseringen**.

2. Selecteer het tabblad **Achtergrondprocessen**.

3. Selecteer **Achtergrondproces voor asynchrone bewerking van controle van virtuele tabel**.

4. Selecteer **Meest recente resultaten weergeven**.

In het uitschuifvenster worden de meest recente uitvoeringsresultaten voor het proces weergegeven. U kunt het logboek voor het proces weergeven, inclusief eventuele fouten die worden geretourneerd van Dataverse.

## <a name="see-also"></a>Zie ook

[Wat is Dataverse?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Tabellen in Dataverse](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Overzicht van tabelrelaties](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Virtuele tabellen maken en bewerken die gegevens uit een externe gegevensbron bevatten](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Wat zijn Power Apps-portals?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Overzicht van het maken van apps in Power Apps](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]