---
title: Plannen met resourceselectie op basis van capaciteit
description: In dit artikel wordt de resourceselectie beschreven tijdens onbeperkte capaciteitsplanning wanneer u capaciteiten als bronbehoeften voor een bewerking opgeeft.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4a3c8236183b81ad015b43d7dbf869c177eafd44
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335400"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Planning met resourceselectie op basis van mogelijkheden

[!include [banner](../../includes/banner.md)]

Door resourcebehoeften op te geven voor een bewerking van een productieroute, definieert u wat nodig is om die bewerking uit te voeren. Voor een bewerking kan bijvoorbeeld een specifieke resource of resourcegroep vereist zijn, of een combinatie van vaardigheden of capaciteiten. In dit artikel wordt de resourceselectie beschreven tijdens onbeperkte capaciteitsplanning wanneer u capaciteiten als bronbehoeften voor een bewerking opgeeft.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>De functie voor planning op basis van capaciteit in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Oneindige capaciteitsplanning voor Planningsoptimalisatie* in de werkruimte [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Raadpleeg [Plannen met onbeperkte capaciteit](infinite-capacity-planning.md) voor meer informatie over deze functie.

## <a name="capability-based-scheduling"></a>Op capaciteit gebaseerde planning

Een capaciteit is de mogelijkheid van een bron voor bedrijfsactiviteiten om een bepaalde activiteit uit te voeren. Aan een resource voor bedrijfsactiviteiten kunnen meerdere capaciteiten worden toegewezen en één capaciteit kan aan meerdere resources worden toegewezen. Capaciteiten kunnen worden toegewezen aan allerlei soorten resources zoals hulpmiddelen, leveranciers, machines, locaties en human resources.

Wanneer u capaciteiten als resourcebehoeften opgeeft, kunt u de resourcetoewijzing uitstellen totdat orders worden gepland. In plaats van specifieke resources of resourcegroepen toe te wijzen aan een routebewerking, kunt u de capaciteiten definiëren die nodig zijn voor elke routebewerking. Tijdens de planning matcht het systeem dan de vereiste capaciteiten aan de capaciteiten die zijn gedefinieerd voor de resources. Het systeem selecteert alleen resources die voldoen aan de vereisten.

Als u capaciteiten wilt toewijzen aan een resource voor bewerking, gebruikt u het sneltabblad **Capaciteiten** van de pagina **Resources**. Als u resources wilt toewijzen aan een capaciteit , gebruikt u het sneltabblad **Resources** van de pagina **Bronmogelijkheden**. Beide pagina's zijn bereikbaar via **Productiebeheer \> Instellingen \> Resources** in het navigatiedeelvenster. Beide sneltabbladen bevatten een raster met de resources die zijn gekoppeld aan een geselecteerde resource of capaciteit. Beide sneltabbladen bevatten ook een werkbalk die opties voor het toevoegen, verwijderen en bewerken van rijen in het raster. Het raster bevat de volgende kolommen:

- **Resource** of **Capaciteit** – Selecteer de resource of capaciteit die door de rij wordt toegewezen.
- **Beschrijving** - Voer een korte beschrijving in van de resource of capaciteit.
- **Ingangsdatum** – Geef de eerste datum op waarop de resource- of capaciteitstoewijzing van toepassing is. Tijdens het plannen gebruikt het systeem geen resource of capaciteit met een verlopen capaciteitstoewijzing, zelfs niet als de resource verder aan de vereisten voldoet.
- **Vervaldatum** – Geef de laatste datum op waarop de resource- of capaciteitstoewijzing van toepassing is. Tijdens het plannen gebruikt het systeem geen resource of capaciteit met een verlopen capaciteitstoewijzing, zelfs niet als de resource verder aan de vereisten voldoet.
- **Niveau** – Specificeer het vaardigheidsniveau dat de resource moet hebben voor de capaciteit. Als u vervolgens in **Benodigd minimumniveau** een waarde opgeeft voor de resource- of capaciteitsbehoefte, wordt voor de planning tijdens de selectie van resources rekening gehouden met het vaardigheidsniveau. Het systeem selecteert alleen resources die de vereiste capaciteit hebben op een niveau dat gelijk is aan of hoger is dan het minimumniveau dat in de resourcebehoefte is opgegeven.
- **Prioriteit** - Dit veld wordt nog niet ondersteund door Planningsoptimalisatie. Als u echter de ingebouwde planningsengine gebruikt, kunt u het veld **Prioriteit** in de resource- of capaciteitstoewijzing gebruiken om de resourceprioriteit te definiëren. Als dan *Prioriteit* wordt geselecteerd in het veld **Selectie van primaire resource** op de pagina **Planningsparameters**, wordt de resource met de hoogste prioriteit (de laagste numerieke waarde in het veld **Prioriteit**) als eerste geselecteerd tijdens de planning.

## <a name="example"></a>Voorbeeld

In dit voorbeeld ziet u hoe de planningsengine resources selecteert op basis van de capaciteit.

Een productieroute heeft vijf bewerkingen: *10*, *20*, *30*, *40* en *50*. Voor elke routebewerking is een resource nodig met een andere capaciteit. Voor routebewerking *10* is bijvoorbeeld een resource nodig die de capaciteit heeft om een luidspreker te assembleren (*0050 Spkr Assembly*) en de capaciteit van houtbewerking heeft (*1010 Wood capabilities*). Routebewerking *50* heeft een resource nodig met de capaciteit om een product te verpakken (*0070 Packing capability*).

![Capaciteit gebruikt voor planning.](media/capability-based-scheduling.png "Capaciteit gebruikt voor planning.")

Tijdens het plannen zoekt de engine naar resources die voldoen aan de vereisten van de bewerking. De planningsengine selecteert bijvoorbeeld resource *00101* om bewerking *10* uit te voeren, omdat deze resource de eerste resource is die wordt gevonden en beide vereiste capaciteiten heeft. De planningsengine selecteert resource *00301* om bewerking *50* uit te voeren, omdat deze resource de enige resource is die de verpakcapaciteit heeft.

Kijk naar het effect op dit voorbeeld als vaardigheidsniveaus worden gebruikt:

- Voor bewerking *10* is een minimaal vaardigheidsniveau van *7* vereist voor de capaciteit *0059 Assembly*.
- Resource *00101* heeft een vaardigheidsniveau van *5* voor de capaciteit *0059 Assembly*.
- Resource *00102* heeft een vaardigheidsniveau van *10* voor de capaciteit *0059 Assembly*.

In dit geval wordt tijdens onbeperkte capaciteitsplanning resource *00102* geselecteerd om bewerking *10* uit te voeren omdat deze resource, in tegenstelling tot resource *00101*, over het vereiste vaardigheidsniveau beschikt voor de capaciteit.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
