---
title: Typen problemen voor niet-conformeringen
description: In dit onderwerp wordt beschreven hoe u probleemtypen voor niet-conformeringen maakt en gebruikt.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26705dd12f478f4ca6046c7265d4ae3cb1d08c69
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568802"
---
# <a name="problem-types-for-nonconformances"></a>Typen problemen voor niet-conformeringen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u probleemtypen voor niet-conformeringen maakt en gebruikt.

U kunt de pagina **Probleemtypen** gebruiken om een classificatie te definiëren van de kwaliteitsproblemen die zich kunnen voordoen voor de verschillende typen niet-conformeringen. Voor elk probleemtype dat u maakt, moet u de typen van niet-conformeringen opgeven waarmee het probleemtype kan worden gebruikt. U kunt de volgende typen niet-conformeringen instellen:

- **Intern**: niet-conformeringen van dit type zijn gerelateerd aan voorhanden voorraad (bijvoorbeeld kwaliteitsorders of quarantaineorders).
- **Klant**: niet-conformeringen van dit type zijn gerelateerd aan verkooporders.
- **Leverancier**: niet-conformeringen van dit type zijn gerelateerd aan inkooporders.
- **Serviceaanvraag**: niet-conformeringen van dit type zijn gerelateerd aan serviceorders.
- **Productie**: niet-conformeringen van dit type zijn gerelateerd aan batchorders of productieorders.
- **Productie van coproducten**: niet-conformeringen van dit type zijn gerelateerd aan batchorders voor coproducten.

Wanneer u een nieuw probleemtype maakt, selecteert u **Niet-conformeringstypen** in het actievenster om een lijst te maken met een of meer niet-conformeringstypen die zijn geautoriseerd voor het probleemtype. Het probleemtype bijvoorbeeld dat is gerelateerd aan een defectcode, kan mogelijk van toepassing zijn op alle niet-conformeringstypen. Een probleemtype dat gerelateerd is aan klachten van klanten, kan echter alleen van toepassing zijn op de niet-conformeringstypen **Klanten** en **Serviceverzoeken**.

## <a name="examples-of-problem-types"></a>Voorbeelden van probleemtypen

Hieronder vindt u enkele voorbeelden van scenario's voor probleemtypen die kunnen worden gebruikt met de verschillende niet-conformeringstypen:

- **Klant**: een klant heeft een klacht ingediend, een klant heeft iets geretourneerd of er is niet voldaan aan de kwaliteitsspecificaties.
- **Leverancier:** het product is beschadigd, er is niet voldaan aan de kwaliteitsspecificaties of het verkeerde product is ontvangen.
- **Serviceaanvraag**: er is niet voldaan aan de kwaliteitsspecificaties, een klant heeft een klacht ingediend of er is machineonderhoud vereist.
- **Productie**: er is niet voldaan aan de kwaliteitsspecificaties, er is machineonderhoud vereist of het product is beschadigd geraakt.
- **Productie van coproducten**: er is niet voldaan aan de kwaliteitsspecificaties, er is machineonderhoud vereist of het product is beschadigd geraakt.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Een probleemtype maken en dit toewijzen aan niet-conformeringstypen

1. Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Probleemtypen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Probleemtype**: voer een unieke id of naam voor het probleemtype in.
    - **Beschrijving**: voer een gedetailleerde beschrijving van het probleemtype in.

1. Selecteer, terwijl de nieuwe rij nog steeds is geselecteerd, de optie **Niet-conformeringstypen** in het actievenster.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Vervolgens stelt u voor de nieuwe rij het veld **Niet-conformeringstype** in op het niet-conformeringstype dat u voor het probleemtype wilt toestaan.
1. Herhaal de vorige stap voor elk extra niet-conformeringstype dat u voor het probleemtype wilt autoriseren.
1. Sluit de pagina's.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van kwaliteitsbeheer](quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen](quality-responsible-workers.md)
- [Quarantainezones voor niet-conformeringen](quality-quarantine-zones.md)
- [Typen diagnosen voor niet-conformeringen](quality-diagnostic-types.md)
- [Kwaliteitstoeslagen voor niet-conformeringen](quality-charges.md)
- [Bewerkingen voor niet-conformeringen](quality-operations.md)
- [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
