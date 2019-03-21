---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (27 februari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b622276000c56a5af1bb258dbc3c6c4a56af4d20
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/08/2019
ms.locfileid: "782834"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-27-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (27 februari 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>Menu-item Aangepaste velden toevoegen aan Systeembeheer

Navigatie naar het menu **Aangepaste velden** is toegevoegd aan het werkgebied **Systeembeheer**.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>Opties voor importeren en maken verbergen voor nieuwe mobiele toepassingen

Momenteel kunnen geen nieuwe mobiele apps in Talent worden gemaakt. De optie voor het maken van nieuwe mobiele ervaringen is verwijderd uit het menu **Mobiele app**.

### <a name="variable-compensation-award-dmf-entity"></a>Toekenning voor variabele compensatie (DMF-entiteit)

In deze versie is nu de DMF-entiteit (Data Management Framework) **Toekenning voor variabele compensatie** beschikbaar voor export.

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>Adressen uit het Verenigd Koninkrijk worden op de pagina Analyses van Personeelsbeheer als Zwitserse adressen weergegeven

In deze versie worden adressen per plaats weergegeven. In deze versie worden problemen gecorrigeerd waarbij visualisaties de locatie van een werknemer verkeerd voorstelden.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>Het Power BI-rapport Personeel bevat een fout wanneer de anciënniteitsdatum van de werknemer op een schrikkeldag valt

Er is een correctie aangebracht in Microsoft Power BI zodat rekening wordt gehouden met anciënniteitsdatums op 29 februari.

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>Vaste compensatie voor werknemers, variabele toekenningen voor werknemers, variabele plannen voor werknemers (inschrijvingen) toestaan voor aangepaste velden

Aangepaste velden kunnen nu worden toegevoegd voor vaste compensatie voor werknemers, variabele toekenningen voor werknemers en variabele plannen voor werknemers (inschrijvingen). Nu kunt u meer informatie over vaste en variabele compensatieplannen voor werknemers bijhouden, naast de informatie die standaard beschikbaar is. Aangepaste velden kunnen worden ingevoerd en bijgewerkt via de gebruikersinterface of via de entiteiten die worden geleverd.

### <a name="other-miscellaneous-bug-fixes"></a>Andere diverse correcties

Deze release bevat andere kleine correcties.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="advanced-compensation-security-fixed-and-variable"></a>Geavanceerde compensatiebeveiliging (vast en variabel)

In veel organisaties kunnen managers voor compensaties en vergoedingen alleen toegang krijgen tot specifieke compensatierecords. Deze records kunnen voor leidinggevenden of regionale werknemers bestemd zijn. Dankzij deze wijziging kan HR de compensatieplannen beheren en onderhouden voor verschillende werknemersgroepen in de organisatie. Met beveiligingsrollen die aan vaste en variabele plannen kunnen worden toegewezen, wordt de toegang bepaald tot deze plannen en de werknemersgegevens die betrekking hebben op de plannen (bijvoorbeeld salaris- en bonusrecords). Alleen de rollen met de opgegeven toegang kunnen compensatie voor deze werknemers verwerken.

### <a name="platform-update-24"></a>Platformupdate 24

Zie voor meer informatie over Microsoft Dynamics 365 for Finance and Operations platformupdate 24 (maart 2019) [Voorbeeldfuncties in Finance and Operations platformupdate 24 (maart 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>Vaste compensatie voor werknemers beschikbaar maken voor toekomstige positietoewijzingen

Vaak hebben werknemers die aan een organisatie worden toegevoegd, een toekomstige begindatum. Dankzij deze wijziging kan een vaste compensatie worden gedefinieerd voor werknemers met toekomstige positietoewijzingen.

## <a name="known-issues"></a>Bekende problemen

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-for-apps-to-finance-and-operations"></a>Wijzigingen in de sjabloon Core HR-integratie (Talent Common Data Service voor Apps tot Finance and Operations)
De sjabloon voor Core HR is bijgewerkt in een 'geavanceerde querysjabloon'. Daarom is de geavanceerde query standaard beschikbaar voor projecten die zijn gemaakt met behulp van deze sjabloon. Bovendien zijn standaardtoewijzingsfuncties alleen zichtbaar in de geavanceerde query-editor. (Standaardtoewijzingsfuncties worden weergegeven als 'FN' in de toewijzingen.)

Zie voor meer informatie over toewijzingsfouten [Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (14 december 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

Als u de nieuwe sjabloon wilt gebruiken, maakt u een nieuw project maken en selecteert u de nieuwe sjabloon voor integratie van Talent.

Voer de volgende stappen uit om uw bestaande sjabloon bij te werken.

1. De volgende toewijzingen bijwerken:

    - **Taakposities aan posities:** verwijder deze toewijzing.
    - **Taakposities aan taaktoewijzing bovenliggende posities:** verwijder deze toewijzing.
    - **Taakposities aan basispositie:** voeg een nieuwe toewijzing van de entiteit **Taakposities**Common Data Service voor Apps aan de entiteit **Basispositie** Finance and Operations toe. Verplaats deze naar positie 7 in de reeks.

        [![Taakposities aan toewijzing basispositie](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **Taakposities aan positiedetails:** voeg een nieuwe toewijzing van de entiteit **Taakposities**Common Data Service voor Apps aan de entiteit **Positiedetails** Finance and Operations toe. Verplaats deze naar positie 8 in de reeks.

        [![Taakposities aan toewijzing positiedetails](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **Taakposities aan positieduur:** voeg een nieuwe toewijzing van de entiteit **Taakposities**Common Data Service voor Apps aan de entiteit **Positieduur** Finance and Operations toe.

        [![Taakposities aan toewijzing positieduur](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **Taakposities aan positiehiërarchieën:** voeg een nieuwe toewijzing van de entiteit **Taakposities**Common Data Service voor Apps aan de entiteit **Positiehiërarchieën** Finance and Operations toe. Selecteer **Geavanceerde query** om uw geavanceerde query beschikbaar te maken voor uw project.

       [![Knop Geavanceerde query](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. Voeg de volgende toewijzingen toe.
    
    [![Toewijzing](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. Selecteer de koppeling **Geavanceerde query en filtering** naast het veld **Zoeken**.  

    3. Zoek de kolom **cdm_parentjobpositionid.cdm_jobpositionnumber** en selecteer de pijl-omlaag rechts van de kolom.

    4. Selecteer in het dialoogvenster dat verschijnt **Leeg verwijderen**.

    5. Selecteer **Kolom toevoegen \> Voorwaardelijke kolom toevoegen** om een standaardwaardetransformatie toe te voegen voor HIERARCHYTYPENAME.

        [![Opdracht Voorwaardelijke kolom toevoegen](./media/Add-column.png)](./media/Add-column.png)

    6. Voer in het dialoogvenster **Voorwaardelijke kolom toevoegen** **HIERARCHYTYPENAME** in als de naam van de nieuwe kolom.
    7. Selecteer in het gedeelte **If** van de voorwaarde, een veld en gebruik **gelijk aan** als de relatie en voer een waarde in. Geef in de gedeelten **Then** en **Otherwise** van de voorwaarde op wat de standaardwaarde moet zijn. In dit geval voert u **Regel** in beide onderdelen in.

        [![Dialoogvenster Voorwaardelijke kolom toevoegen](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. Selecteer **OK** om het dialoogvenster **Geavanceerde query en filtering** te sluiten.
    9. Selecteer op de pagina **Toewijzingstaak** de nieuwe kolom als de bron voor het maken van een andere toewijzing voor HIERARCHYTYPENAME.

        [![Toewijzing](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
