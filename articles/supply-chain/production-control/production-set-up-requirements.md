---
title: Behoeften voor productie-instellingen
description: Dit artikel informatie over installatievereisten voordat u met Productiebeheer kunt werken.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b0ccbd1781ccb5aa7f5f62ea86888e1673cb77653af57f6c49319a2b5089ebf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782438"
---
# <a name="production-setup-requirements"></a>Behoeften voor productie-instellingen

[!include [banner](../includes/banner.md)]

Dit artikel informatie over installatievereisten voordat u met Productiebeheer kunt werken. 

Productiebeheer is geïntegreerd met functies in andere modules. Dankzij deze interconnectiviteit kunt u productieorders wijzigen en ervoor zorgen dat deze automatisch worden bijgewerkt in alle andere betrokken processen en berekeningen in het systeem. De volgende instellingsprocessen zijn vermeld in de volgorde waarin deze horen plaats te vinden.

## <a name="required-baseline-setup-in-other-modules"></a>Vereiste basisinstelling in andere modules
Voordat u met de module Productiebeheer gaat werken, moet eerst de informatie in de andere modules worden ingesteld. Deze instelling bevat de volgende taken:

-   Algemene bedrijfsgegevens instellen
-   Het grootboek instellen
-   Artikelgroepen definiëren
-   Grootboekrekeningen voor artikelgroepen instellen
-   Stel de voorraadartikeltabel in Voorraadbeheer in.
-   Maak stuklijsten (BOM's) en BOM-versies in Voorraadbeheer.

## <a name="required-calendar-and-resource-setup"></a>Vereist agenda en broninstelling
Voordat u Productiebeheer gaat gebruiken, opent u eerst Organisatiebeheer en maakt en definieert u in de volgende volgorde de kalender en bronnen voor bedrijfsactiviteiten:

1.  **Werktijdsjablonen** – stel werktijdsjablonen in voor het definiëren van de tijden die beschikbaar zijn voor de productieplanning.
2.  **Kalenders** – Instellen van werktijdkalenders voor het definiëren van de dagen van het jaar die beschikbaar zijn voor productieplanning.
3.  **Resourcegroepen** – Instellen van resourcegroepen voor het groeperen van de bronnen voor bedrijfsactiviteiten om een overzicht te krijgen van de vrije capaciteit wanneer u de planning uitvoert. U hoeft geen resourcegroepen in te stellen voordat u de bronnen voor bedrijfsactiviteiten instelt. Wij raden u echter aan dat u begrijpt hoe bronnen gegroepeerd worden wanneer u Productiebeheer instelt.
4.  **Bronnen** – Instellen van bronnen voor bedrijfsactiviteiten om de bronnen te definiëren die gebruikt worden om het productieproces en capaciteitsplanning te voltooien.

## <a name="required-production-parameters-setup"></a>Vereiste instelling van productieparameters
**Parameters van productiecontrole**– Instellen van de parameters voor de basisproductie om te definiëren hoe het systeem productieorders afhandelt en verwerkt. Definiëren hoe productieorders worden gemaakt, geraamd, gepland en verbruikt. U kunt ook selecteren welke feedback u wilt en hoe de kostprijsboekhouding wordt uitgevoerd.

## <a name="required-journal-name-identification"></a>Vereiste identificatie van journaalnaam
**Productiejournaalnamen** – Geef de productiejournaalnamen op die worden gebruikt om transacties te registreren en te boeken.

## <a name="setup-if-you-use-operations"></a>Instelling als u bewerkingen gebruikt
Bewerkingen zijn de specifieke activiteiten die nodig zijn om een product te fabriceren. **Notitie:** U moet de typen activiteiten kennen die zijn vereist om het artikel te produceren, en de volgorde en prioriteiten van deze activiteiten. Ook moet u weten welke resources betrokken zijn, en hoeveel.

1.  **Bewerkingen** – Stel bewerkingen in voor de taken die moeten worden voltooid om het voltooide artikel te produceren.
2.  **Relaties** – Bewerkingsrelaties instellen om de gedetailleerde eigenschappen vast te stellen. Om bewerkingsrelaties te definiëren, klikt u op **Relaties** op de pagina **Bewerkingen**.

## <a name="setup-if-you-use-routes"></a>Instelling als u routes gebruikt
Als u met routes werkt, moet u bewerkingen definiëren voor elke productieroute die u instelt. De route is het pad dat het artikel van bewerking naar bewerking volgt, van het begin van het productieproces tot aan het einde van het productieproces.

1.  **Kostencategorieën**- Stel kostencategorieën in voor het definiëren van de kosten per uur van de opgegeven processen en insteltijden.
2.  **Kostengroepen** – Stel kostengroepen in voor het maken en muteren van de verschillende typen kostprijsberekeningen.
3.  **Routegroepen**– Stel routegroepen in voor het definiëren van parameters die betrekking op groepen routes hebben. U moet routegroepen instellen vóór het maken van productieroutes.
4.  **Routes** - Stel productieroutes in en definieer standaardinstellingen voor het beheer van de planning, kostprijsberekening en prijzen van routebewerkingen en voor het beheer van voortgangsrapportage.
5.  **Routeversie** – Stel routeversies in voor het inschakelen van artikelvariaties in de productie.

## <a name="optional-advanced-settings"></a>Optionele, geavanceerde instellingen
1.  **Productiegroepen** – Instellen van productiegroepen voor de totstandbrenging van relaties tussen de productieorder en grootboekrekeningen. De grootboekrekeningen worden gebruikt om orders voor rapportage te boeken of te groeperen.
2.  **Productiepools** - Maak productiepools voor het groeperen van productieorders zodat u dringende productieorders kunt verwerken of groepen orders kunt verwijderen en boeken.
3.  **Eigenschappen**– Definieer eigenschappen om speciale kenmerken te maken die u aan bronnen kunt toewijzen voor het beheer van de productievolgorde. Deze kenmerken zijn verbonden met het werktijdsjabloon.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]