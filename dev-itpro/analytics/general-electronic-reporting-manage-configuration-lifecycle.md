---
title: De levenscyclus van de configuratie van elektronische rapportage beheren
description: In dit onderwerp wordt beschreven hoe de levenscyclus van elektronische rapportage (ER)-configuraties voor de Microsoft Dynamics 365 voor bewerkingen oplossing te beheren.
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>De levenscyclus van de configuratie van elektronische rapportage beheren

In dit onderwerp wordt beschreven hoe de levenscyclus van elektronische rapportage (ER)-configuraties voor de Microsoft Dynamics 365 voor bewerkingen oplossing te beheren.

<a name="overview"></a>Overzicht
--------

Elektronische rapportage (ER) is een engine die officieel vereiste en land/regio-specifieke elektronische documenten in Microsoft Dynamics 365 for Operations ondersteunt. Over het algemeen wordt er bij ER uitgegaan van een mogelijkheid om de volgende taken voor één elektronisch document uit te voeren. Zie voor meer informatie [rapporteren-overzicht elektronisch](general-electronic-reporting.md).

-   Een sjabloon voor een elektronisch document ontwerpen:
    -   De vereiste gegevensbronnen identificeren die in het document kunnen worden gepresenteerd:
        -   Onderliggende Dynamics 365 voor gegevens, bewerkingen, zoals gegevenstabellen, gegevensentiteiten en klassen.
        -   Proces-specifieke eigenschappen, zoals het uitvoeren van datum en tijd en tijdzone.
        -   Gebruikersinvoerparameters, opgegeven door de eindgebruiker tijdens runtime.
    -   De vereiste documentelementen van de bijbehorende topologie definiëren om een definitieve documentindeling op te geven
    -   De gewenste stroom van gegevens configureren vanuit geselecteerde gegevensbronnen voor gedefinieerde documentelementen (via gegevensbronbindingen voor documentindelingsonderdelen) en procesbeheerlogica opgeven.
-   Een sjabloon beschikbaar maken zodat deze in andere Dynamics 365 for Operations-exemplaren kan worden gebruikt:
    -   Een documentsjabloon die in Dynamics 365 for Operations is gemaakt, transformeren naar een ER-configuratie en de configuratie van het huidige Dynamics 365 for Operations-exemplaar exporteren als een XML-pakket dat lokaal of in LCS kan worden opgeslagen.
    -   Een ER-configuratie naar een Dynamics 365 for Operations-documentsjabloon transformeren.
    -   Een XML-pakket dat lokaal of in LCS is opgeslagen importeren in het huidige Dynamics 365 for Operations-exemplaar.
-   De sjabloon van een elektronisch document aanpassen:
    -   Een sjabloon van LCS naar het huidige Dynamics 365 for Operations-exemplaar als een ER-configuratie overbrengen.
    -   Een aangepaste versie van een ER-configuratie ontwerpen en een verwijzing naar de basisversie bewaren.
-   Een sjabloon met een bepaald bedrijfsproces integreren, zodat deze in Dynamics 365 for Operations beschikbaar is:
    -   Dynamics 365 for Operations-instellingen zo configureren dat Dynamics een ER-configuratie gaat gebruiken door in een procesgerelateerde parameter naar die configuratie te verwijzen. Raadpleeg bijvoorbeeld de Emergency Recovery-configuratie in een specifieke rekeningen te betalen betalingsmethode voor het genereren van een elektronische betaling-bericht voor de verwerking van facturen.
-   Een sjabloon in een specifiek bedrijfsproces gebruiken:
    -   De configuratie van een Emergency Recovery in een specifiek bedrijfsproces uitgevoerd. Bijvoorbeeld is voor het genereren van een elektronische betaling-bericht voor de verwerking van facturen wanneer een betalingsmethode die verwijst naar de Emergency Recovery-configuratie ingeschakeld.

## <a name="concepts"></a>Concepten
De volgende rollen en gerelateerde activiteiten zijn gekoppeld aan de levenscyclus van Emergency Recovery-configuratie.

| Rol                                       | Activiteiten                                                      | Omschrijving                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Functioneel consultant elektronische rapportage | De ER-onderdelen (modellen en indelingen) maken en beheren.           | Een business-persoon die ER specifieke domein gegevensmodellen, de vereiste sjablonen voor elektronische documenten ontwerpen ontwerpt en worden deze dienovereenkomstig gebonden.                                                                           |
| Ontwikkelaar elektronische rapportage             | Gegevensmodeltoewijzingen maken en beheren.                          | Een Dynamics 365 voor bewerkingen specialist die u selecteert de vereiste Dynamics 365 voor gegevensbronnen van bewerkingen en koppelt deze aan Emergency Recovery domein-specifieke gegevensmodellen.                                                                 |
| Supervisor boekhouding                      | Procesgerelateerde instellingen configureren die verwijzen naar ER-artefacten. | Bijvoorbeeld een **Accounting supervisor** rol waarmee de instellingen van een Emergency Recovery-configuratie moet worden gebruikt in een bepaalde betalingsmethode voor leveranciers voor rekeningen voor het genereren van een elektronische betaling-bericht voor de verwerking van facturen. |
| Leveranciersadministrateur            | ER-artefacten in een specifiek bedrijfsproces gebruiken.                | Bijvoorbeeld een **Crediteurenadministrateur** rol waarmee berichten van de elektronische betaling moet worden gegenereerd voor verwerking facturen, op basis van de Emergency Recovery-indeling die is geconfigureerd voor een bepaalde betalingswijze.           |

## <a name="er-configuration-development-lifecycle"></a>De levenscyclus van de ER-configuratieontwikkeling
Het is raadzaam om ER-configuraties in de ontwikkelingsomgeving te ontwerpen als een afzonderlijk exemplaar van Dynamics 365 for Operations om de volgende ER-gerelateerde redenen:

-   Gebruikers met de rol **Ontwikkelaar elektronische rapportage** of **Functioneel consultant elektronische rapportage** kunnen configuraties bewerken en deze voor testdoeleinden uitvoeren. Dit scenario kan aanroepen veroorzaken van methoden van klassen en tabellen die schadelijk kunnen zijn voor bedrijfsgegevens en de prestaties van het Dynamics 365 for Operations-exemplaar.
-   Aanroepen van methoden van klassen en tabellen als ER-gegevensbronnen van ER-configuraties worden niet beperkt door Dynamics 365 for Operations-invoerpunten en geregistreerde bedrijfsinhoud. Daardoor kunnen gebruikers met de rol **Ontwikkelaar elektronische rapportage** of **Functioneel consultant elektronische rapportage** toegang krijgen tot gevoelige bedrijfsgegevens.

Emergency Recovery-configuraties die zijn ontworpen in de ontwikkelomgeving kunnen worden geüpload naar de testomgeving voor de beoordeling van de configuratie (juiste integratie, juistheid van de resultaten en prestaties) en de kwaliteitscontrole, zoals de juistheid van de rol op basis van hoeveelheid werk toegangsrechten en scheiding van taken. De functies waarmee de uitwisseling van Emergency Recovery-configuratie kunnen worden gebruikt voor dit doel. Ten slotte kunnen geverifieerde Emergency Recovery-configuraties worden geüpload naar LCS, waar ze worden gedeeld met de service-abonnees, of naar de productieomgeving voor intern gebruik, zoals weergegeven in de volgende afbeelding. ![Emergency Recovery configuratie lifecycle](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Zie ook
--------

[Overzicht van elektronische rapportage](general-electronic-reporting.md)


