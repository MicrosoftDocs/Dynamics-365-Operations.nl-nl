---
title: De levenscyclus van de configuratie van elektronische rapportage (ER) beheren
description: In dit artikel wordt beschreven hoe u de levenscyclus van ER-configuratie (elektronische rapportage) voor de Dynamics 365 Finance-oplossing kunt beheren.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337191"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>De levenscyclus van de configuratie van elektronische rapportage (ER) beheren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u de levenscyclus van [ER-configuraties](general-electronic-reporting.md#Configuration) ([elektronische rapportage](general-electronic-reporting.md)) voor Dynamics 365 Finance kunt beheren.

## <a name="overview"></a>Overzicht

Elektronische rapportage (ER) is een engine die officieel vereiste en land/regio-specifieke elektronische documenten ondersteunt. Over het algemeen wordt er bij ER uitgegaan van een mogelijkheid om de volgende taken voor één elektronisch document uit te voeren. Zie voor meer informatie [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md).

- Een sjabloon voor een elektronisch document ontwerpen:

    - De vereiste gegevensbronnen identificeren die in het document kunnen worden gepresenteerd:

        - Onderliggende gegevens, zoals gegevenstabellen, gegevensentiteiten en klassen.
        - Processpecifieke eigenschappen, zoals uitvoeringsdatum en -tijd en tijdzone.
        - Gebruikersinvoerparameters, opgegeven tijdens uitvoeringstijd door eindgebruiker.

    - De vereiste documentelementen van de bijbehorende topologie definiëren om een definitieve documentindeling op te geven
    - De gewenste stroom van gegevens configureren vanuit geselecteerde gegevensbronnen voor gedefinieerde documentelementen (via gegevensbronbindingen voor documentindelingsonderdelen) en procesbeheerlogica opgeven.

- Een sjabloon beschikbaar maken zodat deze in andere exemplaren kan worden gebruikt:

    - Een documentsjabloon die is gemaakt, transformeren naar een ER-configuratie en de configuratie van het huidige toepassingsexemplaar exporteren als een XML-pakket dat lokaal of in LCS (Lifecycle Services) kan worden opgeslagen.
    - Een ER-configuratie naar een toepassingsdocumentsjabloon transformeren.
    - Een XML-pakket dat lokaal of in LCS is opgeslagen importeren in het huidige exemplaar.

- De sjabloon van een elektronisch document aanpassen:

    - Een sjabloon van LCS naar het huidige exemplaar als een ER-configuratie overbrengen.
    - Een aangepaste versie van een ER-configuratie ontwerpen en een verwijzing naar de basisversie bewaren.

- Een sjabloon met een bepaald bedrijfsproces integreren, zodat deze in de toepassing beschikbaar is:

    - Instellingen zo configureren dat de toepassing een ER-configuratie gaat gebruiken door in een procesgerelateerde parameter naar die configuratie te verwijzen. Raadpleeg bijvoorbeeld de ER-configuratie in een specifieke betalingsmethode van leveranciers om een elektronisch betalingsbericht voor verwerking van facturen te genereren.

- Een sjabloon in een specifiek bedrijfsproces gebruiken:

    - Een ER-configuratie in een specifiek bedrijfsproces uitvoeren. Bijvoorbeeld om een elektronisch betalingsbericht voor verwerking van facturen te genereren wanneer een betalingsmethode is geselecteerd die verwijst naar de ER-configuratie.

## <a name="concepts"></a>Concepten
De volgende rollen en gerelateerde activiteiten zijn gekoppeld aan de levenscyclus van de ER-configuratie.

| Rol                                       | Activiteiten                                                      | Omschrijving |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Functioneel consultant elektronische rapportage | De ER-onderdelen (modellen en indelingen) maken en beheren.           | Een bedrijfspersoon die ER-domeinspecifieke gegevensmodellen ontwerpt, ontwerpt de vereiste sjablonen voor elektronische documenten en verbindt deze dienovereenkomstig. |
| Ontwikkelaar elektronische rapportage             | Gegevensmodeltoewijzingen maken en beheren.                          | Een specialist die de vereiste Finance-gegevensbronnen selecteert en deze met ER-domeinspecifieke gegevensmodellen verbindt. |
| Supervisor boekhouding                      | Procesgerelateerde instellingen configureren die verwijzen naar ER-artefacten. | Bijvoorbeeld de rol van een **Supervisor boekhouding** waarmee de instellingen van een ER-configuratie in een bepaalde betalingsmethode van leveranciers kunnen worden gebruikt om een elektronisch betalingsbericht voor de verwerking van facturen te genereren. |
| Leveranciersadministrateur            | ER-artefacten in een specifiek bedrijfsproces gebruiken.                | Bijvoorbeeld de rol van een **Leveranciersadministrateur** waarmee elektronische betalingsberichten voor de verwerking van facturen kunnen worden gegenereerd op basis van de ER-indeling die voor een specifieke betalingsmethode wordt geconfigureerd. |

## <a name="er-configuration-development-lifecycle"></a>De levenscyclus van de ER-configuratieontwikkeling
Het is raadzaam om ER-configuraties in de ontwikkelingsomgeving te ontwerpen als een afzonderlijk exemplaar van Finance + Operations om de volgende ER-gerelateerde redenen:

- Gebruikers met de rol **Ontwikkelaar elektronische rapportage** of **Functioneel consultant elektronische rapportage** kunnen configuraties bewerken en deze voor testdoeleinden uitvoeren. Dit scenario kan aanroepen veroorzaken van methoden van klassen en tabellen die schadelijk kunnen zijn voor bedrijfsgegevens en de prestaties van het exemplaar.
- Aanroepen van methoden van klassen en tabellen als ER-gegevensbronnen van ER-configuraties worden niet beperkt door invoerpunten en geregistreerde bedrijfsinhoud. Daardoor kunnen gebruikers met de rol **Ontwikkelaar elektronische rapportage** of **Functioneel consultant elektronische rapportage** toegang krijgen tot gevoelige bedrijfsgegevens.

ER-configuraties die zijn ontworpen in de ontwikkelomgeving, kunnen worden [geüpload](#data-persistence-consideration) naar de testomgeving voor de configuratie-evaluatie (juiste procesintegratie, nauwkeurigheid van resultaten en prestaties) en kwaliteitscontrole, zoals nauwkeurigheid van op rollen gebaseerde toegangsrechten, scheiding van taken enzovoort. De functies die de uitwisseling van ER-configuratie mogelijk maken, kunnen voor dit doel worden gebruikt. Bewezen ER-configuraties kunnen worden geüpload naar LCS waar ze kunnen worden gedeeld met serviceabonnees, of [geïmporteerd](#data-persistence-consideration) naar de productieomgeving voor intern gebruik.

![Levenscyclus van ER-configuratie.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Overweging voor gegevenspersistentie

U kunt verschillende versies van een [ER-configuratie](general-electronic-reporting.md#Configuration) afzonderlijk [importeren](tasks/er-import-configuration-lifecycle-services.md) in uw Finance-exemplaar. Wanneer een nieuwe versie van een ER-configuratie wordt geïmporteerd, bepaalt het systeem de inhoud van de conceptversie van deze configuratie:

- Wanneer de geïmporteerde versie lager is dan de hoogste versie van deze configuratie in het huidige exemplaar van Finance, blijft de inhoud van de conceptversie van deze configuratie ongewijzigd.
- Wanneer de geïmporteerde versie hoger is dan een andere versie van deze configuratie in het huidige exemplaar van Finance, wordt de inhoud van de geïmporteerde versie naar de conceptversie van deze configuratie gekopieerd, waarin u de laatst voltooide versie kunt bewerken.

Als deze configuratie eigendom is van de configuratie [provider](general-electronic-reporting.md#Provider) die momenteel is geactiveerd, is de conceptversie van deze configuratie zichtbaar op het sneltabblad **Versies** van de pagina **Configuraties** (**Organisatiebeheer** > **Elektronische rapportage** > **Configuraties**). U kunt de conceptversie van de configuratie selecteren en de inhoud ervan [wijzigen](er-quick-start2-customize-report.md#ConfigureDerivedFormat) met behulp van de relevante ER-ontwerper. Wanneer de conceptversie van een ER-configuratie hebt bewerkt, komt de inhoud niet meer overeen met de inhoud van de hoogste versie van deze configuratie in het huidige exemplaar van Finance. Om te voorkomen dat uw wijzigingen verloren gaan, wordt een fout weergegeven dat de import niet kan worden voortgezet omdat de versie van deze configuratie hoger is dan de hoogste versie van deze configuratie in het huidige exemplaar van Finance. Wanneer dit zich voordoet, bijvoorbeeld bij de indelingsconfiguratie **X**, wordt de fout **Indeling 'X'-versie niet voltooid** weergegeven.

Als u de wijzigingen die u in de conceptversie hebt aangebracht ongedaan wilt maken, selecteert u in het sneltabblad **Versies** de hoogste voltooide of gedeelde versie van uw ER-configuratie in Finance en selecteert u vervolgens de optie **Deze versie ophalen**. De inhoud van de geselecteerde versie wordt naar de conceptversie gekopieerd.

## <a name="applicability-consideration"></a>Overweging van toepasbaarheid

Wanneer u een nieuwe versie van een ER-configuratie ontwerpt, kunt u de [afhankelijkheid](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) van andere softwareonderdelen definiëren. Deze stap wordt beschouwd als een vereiste voor het beheren van de download van de versie van deze configuratie uit een ER-opslagplaats of een extern XML-bestand en voor eventueel verder gebruik van de versie. Wanneer u een nieuwe versie van een ER-configuratie probeert te importeren, gebruikt het systeem de geconfigureerde vereisten om te bepalen of de versie kan worden geïmporteerd.

In sommige gevallen wilt u mogelijk dat het systeem de geconfigureerde vereisten negeert wanneer u nieuwe versies van ER-configuraties importeert. Volg deze stappen als u wilt dat het systeem de vereisten tijdens het importeren negeert.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel de optie **Controle tijdens importeren van productupdates en vereiste versiecontrole overslaan** in op **Ja**.

    > [!NOTE]
    > Deze parameter specifiek is voor de gebruiker en het bedrijf.

## <a name="dependencies-on-other-components"></a>Afhankelijkheden van andere onderdelen

ER-configuraties kunnen worden geconfigureerd als [afhankelijk](er-download-configurations-global-repo.md#import-filtered-configurations) van andere configuraties. U kunt bijvoorbeeld een ER-[gegevensmodel](er-overview-components.md#data-model-component)configuratie [importeren](er-download-configurations-global-repo.md) uit de Algemene opslagplaats in uw [Microsoft Regulatory Configuration Services (RCS)](../../../finance/localizations/rcs-overview.md) of Dynamics 365 Finance-instantie en vervolgens een nieuwe ER-[indeling](er-overview-components.md#format-component)sconfiguratie aanmaken die is [afgeleid](er-quick-start2-customize-report.md#DeriveProvidedFormat) van de geïmporteerde ER-gegevensmodelconfiguratie. De configuratie van de afgeleide ER-indeling is afhankelijk van de basisconfiguratie van het ER-gegevensmodel.

![Configuratie van de afgeleide ER-indeling op de pagina Configuraties.](./media/ger-configuration-lifecycle-img1.png)

Wanneer u klaar bent met het ontwerpen van de indeling, kunt u de status van uw oorspronkelijke versie van de configuratie van de ER-indeling wijzigen van **Concept** in **Voltooid**. U kunt vervolgens de voltooide versie van de configuratie van de ER-indeling delen door deze te [publiceren](../../../finance/localizations/rcs-global-repo-upload.md) naar de Algemene opslagplaats. Vervolgens kunt u de Algemene opslagplaats openen vanuit elke andere cloud-instantie van RCS of Finance. Vervolgens kunt u elke versie van de ER-configuratie importeren die van toepassing is op de toepassing van de Algemene opslagplaats in die toepassing.

![Gepubliceerde configuratie van ER-indeling op de pagina Opslagplaats van configuratie.](./media/ger-configuration-lifecycle-img2.png)

Wanneer u op basis van de configuratieafhankelijkheid de er-indelingsconfiguratie selecteert in de Algemene opslagplaats om deze te importeren in een nieuw geïmplementeerde RCS- of financiën-exemplaar, wordt de basisgegevensmodelconfiguratie automatisch gevonden in de Algemene opslagplaats en geïmporteerd samen met de geselecteerde ER-indelingsconfiguratie als de basisconfiguratie.

U kunt de versie van uw ER-indelingsconfiguratie ook exporteren vanuit de huidige instantie van RCS of Finance en deze lokaal opslaan als een XML-bestand.

![Een versie van een ER-indelingsconfiguratie exporteren als XML-bestand op de pagina Configuratie.](./media/ger-configuration-lifecycle-img3.png)

Wanneer u in versies van Finance **vóór versie 10.0.29** probeert om de versie van de ER-indelingsconfiguratie te importeren vanuit dat XML-bestand of vanuit een andere opslagplaats dan de algemene opslagplaats in een nieuw geïmplementeerde instantie van RCS of Finance die nog geen ER-configuraties bevat, treedt de volgende uitzondering op om u ervan op de hoogte te stellen dat er geen basisconfiguratie kan worden verkregen:

> Resterende niet-opgeloste verwijzingen<br>
Verwijzing van het object '\<imported configuration name\>' naar het object 'Base' (\<globally unique identifier of the missed base configuration\> ,\<version of the missed base configuration\>) kan niet tot stand worden gebracht

![De versie van de ER-indelingsconfiguratie importeren op de pagina Opslagplaats van configuratie.](./media/ger-configuration-lifecycle-img4.gif)

Wanneer u in **versie 10.0.29 of later** probeert dezelfde configuratie te importeren zal het ER-framework, als er geen basisconfiguratie kan worden gevonden in de huidige instantie van de toepassing of de bronopslagplaats die op dit moment wordt gebruikt (indien van toepassing), automatisch proberen de naam van de ontbrekende basisconfiguratie te vinden in de cache van de Algemene opslagplaats. De naam en de globally unique identifier (GUID) van de ontbrekende basisconfiguratie worden vervolgens gebruikt in de tekst van de uitzondering die optreedt.

> Resterende niet-opgeloste verwijzingen<br>
Verwijzing van het object '\<imported configuration name\>' naar het object 'Base' (\<name of the missed base configuration\> \<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>) kan niet tot stand worden gebracht

![Uitzondering op de pagina Configuratie-opslagplaats als de basisconfiguratie niet kan worden gevonden.](./media/ger-configuration-lifecycle-img5.png)

U kunt de opgegeven naam gebruiken om de basisconfiguratie op te zoeken en deze vervolgens handmatig importeren.

> [!NOTE]
> Deze nieuwe optie werkt alleen als ten minste één gebruiker reeds bij de Algemene opslagplaats is aangemeld met de pagina [Configuratie-opslagplaatsen](er-download-configurations-global-repo.md#open-configurations-repository) of een van de [zoek](er-extended-format-lookup.md)velden voor algemene opslagplaats in de huidige instantie van Finance en wanneer de inhoud van de algemene opslagplaats in de cache is opgeslagen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[De afhankelijkheid van ER-configuraties voor andere onderdelen definiëren](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

