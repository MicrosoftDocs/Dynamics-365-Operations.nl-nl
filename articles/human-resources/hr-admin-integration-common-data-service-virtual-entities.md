---
title: Virtuele Common Data Service-entiteiten configureren
description: In dit onderwerp wordt beschreven hoe u virtuele entiteiten configureert voor Dynamics 365 Human Resources. Genereer bestaande virtuele entiteiten, werk ze bij en analyseer gegenereerde en beschikbare entiteiten.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
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
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959570"
---
# <a name="configure-common-data-service-virtual-entities"></a>Virtuele Common Data Service-entiteiten configureren

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources is een virtuele gegevensbron in Common Data Service. De gegevensbron biedt volledige bewerkingen voor maken, lezen, bijwerken en verwijderen vanuit Common Data Service en Microsoft Power Platform. De gegevens voor virtuele entiteiten worden niet opgeslagen in Common Data Service, maar in de toepassingsdatabase. 

Als u bewerkingen voor maken, lezen, bijwerken en verwijderen voor entiteiten van Human Resources wilt inschakelen vanuit Common Data Service, moet u de entiteiten beschikbaar maken als virtuele entiteiten in Common Data Service. Op deze manier kunt u bewerkingen voor maken, lezen, bijwerken en verwijderen uitvoeren vanuit Common Data Service en Microsoft Power Platform op gegevens in Human Resources. De bewerkingen ondersteunen ook de validaties van de volledige bedrijfslogica van Human Resources om de gegevensintegriteit te waarborgen bij het schrijven van gegevens naar de entiteiten.

## <a name="available-virtual-entities-for-human-resources"></a>Beschikbare virtuele entiteiten voor Human Resources

Alle OData-entiteiten (Open Data Protocol) in Human Resources zijn beschikbaar als virtuele entiteiten in Common Data Service. Ze zijn ook beschikbaar in Power Platform. U kunt nu apps en ervaringen met gegevens rechtstreeks vanuit Human Resources maken met alle mogelijkheden voor maken, lezen, bijwerken en verwijderen, zonder dat u gegevens hoeft te kopiëren of synchroniseren naar Common Data Service. U kunt Power Apps-portals gebruiken om extern gerichte websites te maken die samenwerkingsscenario's mogelijk maken voor bedrijfsprocessen in Human Resources.

U kunt de lijst met virtuele entiteiten die in de omgeving zijn ingeschakeld, weergeven en in [Power Apps](https://make.powerapps.com) met de entiteiten gaan werken in de oplossing **Dynamics 365 HR Virtual Entities**.

![Dynamics 365 HR Virtual Entities in Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtuele entiteiten versus natuurlijke entiteiten

Virtuele entiteiten voor Human Resources zijn niet hetzelfde als de natuurlijke Common Data Service-entiteiten die voor Human Resources zijn gemaakt. De natuurlijke entiteiten voor Human Resources worden afzonderlijk gegenereerd en onderhouden in de HCM Common-oplossing in Common Data Service. Met natuurlijke entiteiten worden de gegevens opgeslagen in Common Data Service en is synchronisatie met de Human Resources-toepassingdatabase vereist.

> [!NOTE]
> Zie [Common Data Service-entiteiten](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities) voor een lijst met de natuurlijke Common Data Service-entiteiten voor Human Resources.

## <a name="setup"></a>Instelling

Volg deze instellingsstappen om virtuele entiteiten in uw omgeving in te schakelen. 

### <a name="register-the-app-in-microsoft-azure"></a>De app registreren in Microsoft Azure

U moet de app eerst registreren in de Azure-portal, zodat het Microsoft-identiteitsplatform verificatie- en machtigingsservices kan bieden voor de app en de gebruikers. Ga voor meer informatie over het registreren van apps in Azure naar [Snelstart: Een toepassing registreren bij het Microsoft-identiteitsplatform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Open de [Microsoft Azure-portal](https://portal.azure.com).

2. Selecteer in de lijst Azure-services de optie **App-registraties**.

3. Selecteer **Nieuwe registratie**.

4. Voer in het veld **Naam** een beschrijvende naam voor de app in. Bijvoorbeeld, **Dynamics 365 Human Resources Virtuele entiteiten**.

5. Voer in het veld **URI omleiden** de naamruimte-URL in van uw instantie van Human Resources.

6. Selecteer **Registreren**.

7. Wanneer de registratie is voltooid, wordt in de Azure-portal het deelvenster **Overzicht** van de app-registratie weergegeven met de bijbehorende **Id van toepassing (client)**. Maak nu een notitie van de **Id van toepassing (client)**. U voert deze gegevens in wanneer u [de gegevensbron van de virtuele entiteit configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. Selecteer in het linkernavigatievenster de optie **Certificaten en geheimen**.

9. Selecteer in het gedeelte **Clientgeheimen** van de pagina de optie **Nieuw clientgeheim**.

10. Geef een omschrijving op, selecteer een duur en selecteer **Toevoegen**.

11. Leg de waarde van het geheim vast. U voert deze gegevens in wanneer u [de gegevensbron van de virtuele entiteit configureert](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Maak nu een notitie van de waarde van het geheim. Het geheim wordt nooit meer weergegeven nadat u deze pagina hebt verlaten.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>De Dynamics 365 HR Virtual Entity-app installeren

Installeer de Dynamics 365 HR Virtual Entity-app in uw Power Apps-omgeving om het pakket van de virtuele entiteit te implementeren naar Common Data Service.

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2. Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.

3. Selecteer in het gedeelte **Resources** van de pagina de optie **Dynamics 365-apps**.

4. Selecteer de actie **App installeren**.

5. Selecteer **Dynamics 365 HR Virtual Entity** en selecteer **Volgende**.

6. Controleer en markeer om de servicevoorwaarden te accepteren.

7. Selecteer **Installeren**.

De installatie duurt een paar minuten. Wanneer de installatie is voltooid, gaat u door naar de volgende stappen.

![De Dynamics 365 HR Virtual Entity-app installeren vanuit het Power Platform-beheercentrum](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>De gegevensbron van de virtuele entiteit configureren 

In de volgende stap configureert u de gegevensbron van de virtuele entiteit in de Power Apps-omgeving. 

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2. Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.

3. Selecteer de **Omgevings-URL** in het gedeelte **Details** van de pagina.

4. Selecteer op de **Oplossingsstatushub** het pictogram **Geavanceerd zoeken** in de rechtsbovenhoek van de toepassingspagina.

5. Selecteer op de pagina **Geavanceerd zoeken** in de vervolgkeuzelijst **Zoeken naar** de optie **Finance and Operations Virtual Data Source Configurations**.

6. Selecteer **Resultaten**.

7. Selecteer de record **Microsoft HR-gegevensbron**.

8. Voer de vereiste informatie in voor de gegevensbronconfiguratie.

   - **Doel-URL** : de URL van uw Human Resources-naamruimte.
   - **Tenant-id**: de tenant-id van Azure Active Directory (Azure AD).
   - **AAD-toepassings-id** : de toepassings-id (client) die is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd. U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).
   - **AAD-toepassingsgeheim**: het clientgeheim dat is gemaakt voor de toepassing die in de Microsoft Azure-portal is geregistreerd. U hebt deze gegevens eerder ontvangen tijdens de stap [De app registreren in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

9. Selecteer **Opslaan en sluiten**.

   ![Microsoft HR-gegevensbron](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>App-machtigingen verlenen in Human Resources

Verleen als volgt machtigingen voor de twee Azure AD-toepassingen in Human Resources:

- De app die is gemaakt voor uw tenant in de Microsoft Azure-portal
- De Dynamics 365 HR Virtual Entity-app die is geïnstalleerd in de Power Apps-omgeving 

1. Open in Human Resources de pagina **Azure Active Directory-toepassingen**.

2. Selecteer **Nieuw** om een nieuwe toepassingsrecord te maken.

    - Voer in het veld **Client-id** de client-id in van de app die u in de Microsoft Azure-portal hebt geregistreerd.
    - Voer in het veld **Naam** de naam in van de app die u in de Microsoft Azure-portal hebt geregistreerd.
    - Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.

3. Selecteer **Nieuw** om een tweede toepassingsrecord te maken.

    - **Client-id**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Naam**: Dynamics 365 HR Virtual Entity
    - Selecteer in het veld **Gebruikers-id** de gebruikers-id van een gebruiker met beheerdersmachtigingen in Human Resources en de Power Apps-omgeving.

## <a name="generate-virtual-entities"></a>Virtuele entiteiten genereren

Wanneer het instellen is voltooid, kunt u de virtuele entiteiten selecteren die u in uw Common Data Service-exemplaar wilt genereren en inschakelen.

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2. Selecteer in de lijst **Omgevingen** de Power Apps-omgeving die aan uw Human Resources-exemplaar is gekoppeld.

3. Selecteer de **Omgevings-URL** in het gedeelte **Details** van de pagina.

4. Selecteer in de **Oplossingsstatushub** het pictogram **Geavanceerd zoeken** in de rechtsbovenhoek van de pagina.

5. Selecteer op de pagina **Geavanceerd zoeken** in de vervolgkeuzelijst **Zoeken naar** de optie **Beschikbare HR-entiteiten**.

6. Gebruik de filteropties om naar de entiteit of entiteiten te zoeken die u wilt inschakelen.

7. Selecteer een entiteit in de lijst.

8. Wijzig op de entiteitpagina de eigenschap **Is gegenereerd** in **Ja** voor de entiteit.

9. Sla de entiteitpagina op en sluit de pagina.

> [!NOTE]
> U kunt meerdere virtuele entiteiten tegelijk genereren op de pagina **Meerdere records wijzigen**. Selecteer meerdere records op de pagina en selecteer **Bewerken** op het lint. U kunt vervolgens de eigenschap **Is gegenereerd** wijzigen voor alle geselecteerde records.

![Beschikbare HR-entiteiten](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> Om het proces van het genereren van virtuele entiteiten in toekomstige versies te stroom lijnen, wordt het proces uitgevoerd op een pagina in Human Resources.

## <a name="see-also"></a>Zie ook

[Wat is Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Overzicht van entiteiten](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Overzicht van entiteitsrelaties](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Virtuele entiteiten maken en bewerken die gegevens uit een externe gegevensbron bevatten](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Wat zijn Power Apps-portals?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Overzicht van het maken van apps in Power Apps](https://docs.microsoft.com/powerapps/maker/)
