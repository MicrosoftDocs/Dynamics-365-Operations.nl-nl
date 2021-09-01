---
title: Toeslagen voor niet-conformeringsbewerkingen
description: In dit onderwerp wordt beschreven hoe u kwaliteitstoeslagen kunt maken die kunnen worden gebruikt met bewerkingen voor een niet-conformering.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c062fecea23017e603c55d11de542942576dba74e0dda07452fd7a91109fe78
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771486"
---
# <a name="charges-for-nonconformance-operations"></a>Toeslagen voor niet-conformeringsbewerkingen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u kwaliteitstoeslagen kunt maken die kunnen worden gebruikt met bewerkingen voor een niet-conformering.

U gebruikt de pagina **Kwaliteitstoeslagen** om de typen toeslagen te definiëren die aan bewerkingen voor een niet-conformering kunnen worden toegevoegd. Met toeslagen kunt u details bijhouden over kosten of toeslagen die u een klant verschuldigd bent voor niet-overeenkomende producten of die een leverancier u verschuldigd is voor niet-overeenkomende producten die u hebt ontvangen. U kunt toeslagen ook gebruiken om kosten bij te houden die vereist zijn voor externe leveranciers of services om een bewerking uit te voeren.

## <a name="examples-of-quality-charges"></a>Voorbeelden van kwaliteitstoeslagen

U werkt voor een productiebedrijf. Uw bedrijf heeft contracten met verschillende leveranciers. Deze contracten geven de standaarden voor de tijdige verzending, schade en productkwaliteit voor artikelen aan. Ook hebben verschillende van uw klanten overeenkomsten met uw bedrijf over retouren, schade en productkwaliteit.

Er wordt een onkostenstructuur gedefinieerd voor elke situatie die wordt opgegeven in het contract. U kunt kwaliteitstoeslagen configureren om de verschillende typen toeslagen aan te geven, zoals *Schade*, *Late verzending* en *Kwaliteit*. Wanneer u vervolgens een niet-conformering maakt, voegt u een of meer bewerkingen toe. Voor elke bewerking selecteert u **Toeslagen** om de details van de kosten te definiëren.

## <a name="create-a-quality-charge"></a>Een kwaliteitstoeslag maken

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Kwaliteitstoeslagen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Toeslagencode**: voer een unieke id of naam voor de kwaliteitstoeslag in.
    - **Beschrijving**: voer een gedetailleerde beschrijving voor de kwaliteitstoeslag in.

1. Sluit de pagina.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>Een kwaliteitscontrole toevoegen aan een bewerking voor een niet-conformering

Zie [Bewerkingen voor niet-conformeringen](quality-operations.md) voor meer informatie over het toevoegen van bewerkingen aan een niet-conformering en het toepassen van toeslagen op deze bewerkingen.

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
