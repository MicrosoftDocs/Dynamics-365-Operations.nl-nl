---
title: Quarantainezones voor niet-conformeringen
description: In dit artikel wordt beschreven hoe u quarantainezones voor niet-conformeringen maakt en gebruikt.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e556d2aa078a76ff4f81b6763535c38ce1cca0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857701"
---
# <a name="quarantine-zones-for-nonconformances"></a>Quarantainezones voor niet-conformeringen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u quarantainezones voor niet-conformeringen maakt en gebruikt.

U kunt de pagina **Quarantainezones** gebruiken om zones te definiëren die kunnen worden toegewezen aan niet-conformeringen. Wanneer u een niet-conformering maakt, kunt u de velden **Quarantainezone** en **Quarantainetype** instellen op het tabblad **Algemeen** van de pagina **Niet-conformeringen**. Het veld **Quarantainezone** geeft gewoonlijk het gebied of de locatie aan waar het artikel zich bevindt. In het veld **Quarantainetype** wordt het artikel gedefinieerd als *Beperkt gebruik* of *Onbruikbaar*.

Wanneer u een niet-conformering of een correctierapport voor een niet-conformering afdrukt, kunt u de quarantainezone weergeven waar het artikel zich bevindt.

U kunt ook een niet-conformeringslabel voor een niet-conformering afdrukken. In dit rapport worden de toegewezen quarantainezone en informatie over gebruik weergegeven als richtlijn voor het verwerken van defect materiaal. De quarantainezones corresponderen mogelijk met voorraadlocaties of bronnen voor bedrijfsactiviteiten.

## <a name="examples-of-quarantine-zones"></a>Voorbeelden van quarantainezones

### <a name="example-1"></a>Voorbeeld 1

U werkt in een elektronicaproductiebedrijf dat onder andere televisies, luidsprekers en mediaspelers produceert en distribueert. In dit geval kunt u een quarantainezone configureren voor elk type product.

### <a name="example-2"></a>Voorbeeld 2

Er worden drie bakken en twee rekken gebruikt voor het opslaan van niet-conforme artikelen. In dit geval kunt u vijf quarantainezones configureren, één voor elke bak en elk rek.

## <a name="create-a-quarantine-zone"></a>Een quarantainezone maken

1. Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Quarantainezones**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Quarantainezone**: geef een unieke id of naam op voor de quarantainezone.
    - **Beschrijving**: voer een gedetailleerde beschrijving voor de quarantainezone in.

1. Sluit de pagina.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van kwaliteitsbeheer](quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen](quality-responsible-workers.md)
- [Probleemtypen voor niet-conformeringen](quality-quarantine-zones.md)
- [Typen diagnosen voor niet-conformeringen](quality-diagnostic-types.md)
- [Kwaliteitstoeslagen voor niet-conformeringen](quality-charges.md)
- [Bewerkingen voor niet-conformeringen](quality-operations.md)
- [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
