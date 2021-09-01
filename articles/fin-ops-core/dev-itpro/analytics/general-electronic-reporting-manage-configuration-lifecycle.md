---
title: De levenscyclus van de configuratie van elektronische rapportage (ER) beheren
description: In dit onderwerp wordt beschreven hoe u de levenscyclus van ER-configuratie (elektronische rapportage) voor Microsoft Dynamics 365 Finance kunt beheren.
author: NickSelin
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8b61082cf17707c952b6e07613769a671c349bb8fa92c21e3fe8524ef62dcb2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767774"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>De levenscyclus van de configuratie van elektronische rapportage (ER) beheren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de levenscyclus van ER-configuratie (elektronische rapportage) voor Microsoft Dynamics 365 Finance kunt beheren.

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
Het is raadzaam om ER-configuraties in de ontwikkelingsomgeving te ontwerpen als een afzonderlijk exemplaar van Finance and Operations om de volgende ER-gerelateerde redenen:

- Gebruikers met de rol **Ontwikkelaar elektronische rapportage** of **Functioneel consultant elektronische rapportage** kunnen configuraties bewerken en deze voor testdoeleinden uitvoeren. Dit scenario kan aanroepen veroorzaken van methoden van klassen en tabellen die schadelijk kunnen zijn voor bedrijfsgegevens en de prestaties van het exemplaar.
- Aanroepen van methoden van klassen en tabellen als ER-gegevensbronnen van ER-configuraties worden niet beperkt door invoerpunten en geregistreerde bedrijfsinhoud. Daardoor kunnen gebruikers met de rol **Ontwikkelaar elektronische rapportage** of **Functioneel consultant elektronische rapportage** toegang krijgen tot gevoelige bedrijfsgegevens.

ER-configuraties die zijn ontworpen in de ontwikkelomgeving, kunnen worden [geüpload](#data-persistence-consideration) naar de testomgeving voor de configuratie-evaluatie (juiste procesintegratie, nauwkeurigheid van resultaten en prestaties) en kwaliteitscontrole, zoals nauwkeurigheid van op rollen gebaseerde toegangsrechten, scheiding van taken enzovoort. De functies die de uitwisseling van ER-configuratie mogelijk maken, kunnen voor dit doel worden gebruikt. Bewezen ER-configuraties kunnen worden geüpload naar LCS waar ze kunnen worden gedeeld met serviceabonnees, of [geïmporteerd](#data-persistence-consideration) naar de productieomgeving voor intern gebruik.

![Levenscyclus van ER-configuratie.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Overweging voor gegevenspersistentie

U kunt verschillende [versies](general-electronic-reporting.md#component-versioning) van een [ER-configuratie](general-electronic-reporting.md#Configuration) afzonderlijk [importeren](tasks/er-import-configuration-lifecycle-services.md) in uw Finance-exemplaar. Wanneer een nieuwe versie van een ER-configuratie wordt geïmporteerd, bepaalt het systeem de inhoud van de conceptversie van deze configuratie:

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

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[De afhankelijkheid van ER-configuraties voor andere onderdelen definiëren](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
