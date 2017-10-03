---
title: De levenscyclus van de configuratie van elektronische rapportage beheren
description: In dit onderwerp wordt beschreven hoe u de levenscyclus van ER-configuratie (elektronische rapportage) voor de Microsoft Dynamics 365 for Finance and Operations-oplossing kunt beheren.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b1f5da07ffff5e34d8c73012a1e3c85fe1546fda
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>De levenscyclus van de configuratie van elektronische rapportage beheren

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe u de levenscyclus van ER-configuratie (elektronische rapportage) voor de Microsoft Dynamics 365 for Finance and Operations-oplossing kunt beheren.

<a name="overview"></a>Overzicht
--------

Elektronische rapportage (ER) is een engine die officieel vereiste en land/regio-specifieke elektronische documenten in Microsoft Dynamics 365 for Finance and Operations ondersteunt. Over het algemeen wordt er bij ER uitgegaan van een mogelijkheid om de volgende taken voor één elektronisch document uit te voeren. Zie voor meer informatie [Overzicht elektronische rapportage](general-electronic-reporting.md).

-   Een sjabloon voor een elektronisch document ontwerpen:
    -   De vereiste gegevensbronnen identificeren die in het document kunnen worden gepresenteerd:
        -   Onderliggende Finance and Operations-gegevens, zoals gegevenstabellen, gegevensentiteiten en klassen.
        -   Processpecifieke eigenschappen, zoals uitvoeringsdatum en -tijd en tijdzone.
        -   Gebruikersinvoerparameters, opgegeven tijdens uitvoeringstijd door eindgebruiker.
    -   De vereiste documentelementen van de bijbehorende topologie definiëren om een definitieve documentindeling op te geven
    -   De gewenste stroom van gegevens configureren vanuit geselecteerde gegevensbronnen voor gedefinieerde documentelementen (via gegevensbronbindingen voor documentindelingsonderdelen) en procesbeheerlogica opgeven.
-   Een sjabloon beschikbaar maken zodat deze in andere Finance and Operations-exemplaren kan worden gebruikt:
    -   Een documentsjabloon die in Finance and Operations is gemaakt, transformeren naar een ER-configuratie en de configuratie van het huidige Finance and Operations-exemplaar exporteren als een XML-pakket dat lokaal of in LCS kan worden opgeslagen.
    -   Een ER-configuratie naar een Finance and Operations-documentsjabloon transformeren.
    -   Een XML-pakket dat lokaal of in LCS is opgeslagen importeren in het huidige Finance and Operations-exemplaar.
-   De sjabloon van een elektronisch document aanpassen:
    -   Een sjabloon van LCS naar het huidige Finance and Operations-exemplaar als een ER-configuratie overbrengen.
    -   Een aangepaste versie van een ER-configuratie ontwerpen en een verwijzing naar de basisversie bewaren.
-   Een sjabloon met een bepaald bedrijfsproces integreren, zodat deze in Finance and Operations beschikbaar is:
    -   Instellingen zo configureren dat Finance and Operations een ER-configuratie gaat gebruiken door in een procesgerelateerde parameter naar die configuratie te verwijzen. Raadpleeg bijvoorbeeld de ER-configuratie in een specifieke betalingsmethode van leveranciers om een elektronisch betalingsbericht voor verwerking van facturen te genereren.
-   Een sjabloon in een specifiek bedrijfsproces gebruiken:
    -   Een ER-configuratie in een specifiek bedrijfsproces uitvoeren. Bijvoorbeeld om een elektronisch betalingsbericht voor verwerking van facturen te genereren wanneer een betalingsmethode is geselecteerd die verwijst naar de ER-configuratie.)

## <a name="concepts"></a>Concepten
De volgende rollen en gerelateerde activiteiten zijn gekoppeld aan de levenscyclus van de ER-configuratie.

| Rol                                       | Activiteiten                                                      | Omschrijving                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Functioneel consultant elektronische rapportage | De ER-onderdelen (modellen en indelingen) maken en beheren.           | Een bedrijfspersoon die ER-domeinspecifieke gegevensmodellen ontwerpt, ontwerpt de vereiste sjablonen voor elektronische documenten en verbindt deze dienovereenkomstig.                                                                           |
| Ontwikkelaar elektronische rapportage             | Gegevensmodeltoewijzingen maken en beheren.                          | Een Finance and Operations-specialist die de vereiste Finance and Operations-gegevensbronnen selecteert en deze met ER-domeinspecifieke gegevensmodellen verbindt.                                                                 |
| Supervisor boekhouding                      | Procesgerelateerde instellingen configureren die verwijzen naar ER-artefacten. | Bijvoorbeeld de rol van een **Supervisor boekhouding** waarmee de instellingen van een ER-configuratie in een bepaalde betalingsmethode van leveranciers kunnen worden gebruikt om een elektronisch betalingsbericht voor de verwerking van facturen te genereren. |
| Leveranciersadministrateur            | ER-artefacten in een specifiek bedrijfsproces gebruiken.                | Bijvoorbeeld de rol van een **Leveranciersadministrateur** waarmee elektronische betalingsberichten voor de verwerking van facturen kunnen worden gegenereerd op basis van de ER-indeling die voor een specifieke betalingsmethode wordt geconfigureerd.           |

## <a name="er-configuration-development-lifecycle"></a>De levenscyclus van de ER-configuratieontwikkeling
Het is raadzaam om ER-configuraties in de ontwikkelingsomgeving te ontwerpen als een afzonderlijk exemplaar van Finance and Operations om de volgende ER-gerelateerde redenen:

-   Gebruikers met de rol **Ontwikkelaar elektronische rapportage** of **Functioneel consultant elektronische rapportage** kunnen configuraties bewerken en deze voor testdoeleinden uitvoeren. Dit scenario kan aanroepen veroorzaken van methoden van klassen en tabellen die schadelijk kunnen zijn voor bedrijfsgegevens en de prestaties van het Finance and Operations-exemplaar.
-   Aanroepen van methoden van klassen en tabellen als ER-gegevensbronnen van ER-configuraties worden niet beperkt door Finance and Operations-invoerpunten en geregistreerde bedrijfsinhoud. Daardoor kunnen gebruikers met de rol **Ontwikkelaar elektronische rapportage** of **Functioneel consultant elektronische rapportage** toegang krijgen tot gevoelige bedrijfsgegevens.

ER-configuraties die zijn ontworpen in de ontwikkelomgeving, kunnen worden geüpload naar de testomgeving voor de configuratie-evaluatie (juiste procesintegratie, nauwkeurigheid van resultaten en prestaties) en kwaliteitscontrole, zoals nauwkeurigheid van op rollen gebaseerde toegangsrechten, scheiding van taken enzovoort. De functies die de uitwisseling van ER-configuratie mogelijk maken, kunnen voor dit doel worden gebruikt. Tot slot kunnen bewezen ER-configuraties worden geüpload naar LCS waar ze kunnen worden gedeeld met serviceabonnees, of naar de productieomgeving voor intern gebruik, zoals in de volgende afbeelding wordt getoond. ![Levenscyclus van ER-configuratie](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Zie ook
--------

[Overzicht van elektronische rapportage](general-electronic-reporting.md)



