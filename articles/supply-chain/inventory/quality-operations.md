---
title: Bewerkingen voor niet-conformeringen
description: In dit artikel wordt beschreven hoe u bewerkingen voor niet-conformeringen maakt en gebruikt.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2e63156dd2b230da7f1ea89e2c2006c1b4f3eeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847986"
---
# <a name="operations-for-nonconformances"></a>Bewerkingen voor niet-conformeringen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u bewerkingen voor niet-conformeringen maakt en gebruikt.

U kunt de pagina **Bewerkingen** gebruiken om een classificaties te definiëren van het werk dat kan worden uitgevoerd voor een goedgekeurde niet-conformering. Wanneer u een gerelateerde bewerking toewijst aan een niet-conformering, kunt u details opgeven, zoals het bijbehorende materiaal, werkuren en diverse toeslagen die zijn vereist om de bewerking uit te voeren. Het systeem gebruikt deze informatie om een de geraamde kosten voor de bewerking te berekenen. De gedetailleerde informatie en de kostenraming dienen ter referentie. De gerelateerde bewerkingen voor kwaliteit verschillen van de bewerkingen die kunnen worden gedefinieerd voor een productieroute.

> [!NOTE]
> Hoewel u kosten, tijd en artikelen kunt bijhouden die in een bewerking worden gebruikt die is gerelateerd aan een niet-conformering, zijn de gegevens die u invoert, alleen ter informatie. De gegevens worden niet automatisch geïntegreerd met het grootboek, het voorraadsubjournaal of de module **Tijd en aanwezigheid**.

## <a name="examples-of-operations"></a>Voorbeelden van bewerkingen

U werkt voor een productiebedrijf. Er is een niet-conformering gemaakt en goedgekeurd voor artikelen die niet zijn geslaagd voor een kwaliteitstest. Er is een correctie gemaakt om aan te geven dat het probleem te maken heeft met een slecht lager in een machine. Er zijn verscheidene stappen vereist om het lager te vervangen en de verantwoordelijkheid voor elke bewerking wordt bijgehouden. De volgende stappen kunnen bijvoorbeeld vereist zijn:

1. De productielijn wordt gestopt en de opschoonroutine wordt uitgevoerd.
1. Onderhoudspersoneel vervangt het lager.
1. Medewerkers van de kwaliteitsgarantie controleren de machine voordat deze weer wordt ingeschakeld.

In dit voorbeeld kunnen de volgende bewerkingen worden gemaakt om het werk aan te geven dat moet worden uitgevoerd:

- De productielijn stoppen.
- De productielijn opschonen.
- Machineonderhoud uitvoeren.
- De machine inspecteren.

## <a name="create-an-operation"></a>Een bewerking maken

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Bewerkingen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Bewerking**: Voer een unieke id of naam voor de bewerking in.
    - **Beschrijving**: voer een gedetailleerde beschrijving van de bewerking in.
    - **Type** als de bewerking alleen kan worden gebruikt voor niet-conformeringen die zijn gerelateerd aan een bepaald type order, selecteert u het ordertype (*Inkooporder* of *Verkooporder*).

1. Sluit de pagina.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van kwaliteitsbeheer](quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Niet-conformeringen maken en verwerken](tasks/create-process-non-conformance.md)
- [Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen](quality-responsible-workers.md)
- [Quarantainezones voor niet-conformeringen](quality-quarantine-zones.md)
- [Typen diagnosen voor niet-conformeringen](quality-diagnostic-types.md)
- [Kwaliteitstoeslagen voor niet-conformeringen](quality-charges.md)
- [Typen problemen voor niet-conformeringen](quality-operations.md)
- [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
