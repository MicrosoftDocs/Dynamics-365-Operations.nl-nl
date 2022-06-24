---
title: Typen diagnose voor niet-conformeringen
description: In dit artikel wordt beschreven hoe u typen diagnoses kunt gebruiken en maken die kunnen worden gebruikt met niet-conformeringen.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b7a051f807c9faab3169d2672d47f663892225
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852442"
---
# <a name="diagnostic-types-for-nonconformances"></a>Typen diagnose voor niet-conformeringen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u typen diagnoses kunt gebruiken en maken die kunnen worden gebruikt met niet-conformeringen.

U gebruikt de pagina **Diagnosetypen** om een classificatie van diagnostische acties te definiëren. Wanneer u vervolgens een correctie voor een niet-conformering maakt, selecteert u een diagnose. Met een correctie wordt opgegeven welk type diagnostische actie moet worden uitgevoerd voor een goedgekeurde niet-conformering en wie de actie moet uitvoeren. Ook worden de aangevraagde voltooiingsdatum en de geplande voltooiingsdatum opgegeven.

## <a name="examples-of-diagnostic-types"></a>Voorbeelden van typen diagnose

U werkt voor een productiebedrijf en verschillende artikelen voldoen niet aan de kwaliteitstests. Die artikelen worden naar een quarantainegebied verplaatst en gemarkeerd als niet-conformeringsproducten. Er wordt in Microsoft Dynamics 365 Supply Chain Management een niet-conformeringsrecord gemaakt om de details bij te houden via probleemoplossing.

In dit geval treden de kwaliteitsproblemen op omdat er lagers zijn in de machine waarin de artikelen worden verpakt, die oververhit zijn geraakt. De correctie voor dit probleem is het vervangen van de onderdelen in de machine.

Wanneer u de typen diagnose configureert, kunt u meerdere records maken, die elk een verschillend type probleem vertegenwoordigen dat de machine kan hebben. U kunt ook één algemeen type diagnose maken dat machinereparatie vertegenwoordigt.

## <a name="create-a-diagnostic-type"></a>Een type diagnose maken

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Typen diagnose**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Diagnose**: voer een unieke id of naam voor het type diagnose in.
    - **Beschrijving**: voer een gedetailleerde beschrijving van het type diagnose in.

1. Sluit de pagina.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van kwaliteitsbeheer](quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen](quality-responsible-workers.md)
- [Quarantainezones voor niet-conformeringen](quality-quarantine-zones.md)
- [Typen problemen voor niet-conformeringen](quality-problem-types.md)
- [Kwaliteitstoeslagen voor niet-conformeringen](quality-charges.md)
- [Bewerkingen voor niet-conformeringen](quality-operations.md)
- [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
