---
title: Testvariabelen voor kwaliteitsbeheer
description: In dit onderwerp wordt beschreven hoe u testvariabelen maakt die kunnen worden gebruikt voor het kwalitatief testen van kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4495c3d3f8df9f07ec079d8e497a17979abbe3ee
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575867"
---
# <a name="quality-management-test-variables"></a>Testvariabelen voor kwaliteitsbeheer

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u testvariabelen maakt die kunnen worden gebruikt voor het kwalitatief testen van kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.

U moet een testvariabele en de bijbehorende uitkomsten (resultaten) definiëren voor elke kwalitatieve test die is gedefinieerd op de pagina **Tests**. (Voor kwalitatieve tests wordt het veld **Type** op de pagina **Tests** ingesteld op *Optie*.)

U gebruikt de pagina **Testvariabelen** om de mogelijke resultaten in te stellen, te bewerken en weer te geven voor een testvariabele die aan een kwalitatieve test is gekoppeld. Voor elk resultaat kunt u de uitslagstatus *Goedgekeurd* of *Afgekeurd* toewijzen om aan te geven of de test is geslaagd of mislukt wanneer dat resultaat als testresultaat wordt geselecteerd. U gebruikt de pagina **Testgroepen** om een testvariabele en een standaarduitkomst toe te wijzen aan een afzonderlijke kwalitatieve test.

Voor elke testvariabele is het raadzaam om minimaal twee resultaten te definiëren: een resultaat met de uitslagstatus *Goedgekeurd* en een resultaat met de uitslagstatus *Afgekeurd*. Er is geen limiet voor het totale aantal variabelen of resultaten dat kan worden gedefinieerd. Daarnaast kunnen voor meerdere tests dezelfde testvariabelen worden gebruikt om resultaten vast te leggen.

## <a name="examples-of-test-variables"></a>Voorbeelden van testvariabelen

### <a name="example-1"></a>Voorbeeld 1

Een productiebedrijf voert twee tests uit op gefabriceerde materialen. In de ene test is het pH-niveau aan een kleurstrook gekoppeld. Acceptabele pH-niveaus hebben lichtere kleuren en niet-acceptabele pH-niveaus hebben donkerder kleuren. In een andere test worden meerdere visuele inspecties uitgevoerd en kwaliteitsmedewerkers maken gebruik van hun oordeel om te bepalen of het artikel al dan niet door de visuele inspectie komt.

### <a name="example-2"></a>Voorbeeld 2

Een productiebedrijf dat koekjes produceert, maakt gebruik van een inspectietest voor het eindproduct. Deze inspectietest omvat verschillende variabelen. Een van deze variabelen is Smaak met de mogelijke resultaten Goed en Slecht. Een tweede variabele is Kleur met als mogelijke resultaten Te donker, Te licht en Correct.

## <a name="create-a-test-variable"></a>Een testvariabele maken

Volg deze stappen om een testvariabele te maken.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Testvariabelen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Variabele**: voer een unieke id of naam voor de variabele in.
    - **Beschrijving**: voer een gedetailleerde beschrijving voor de variabele in.

1. Selecteer, terwijl de nieuwe rij nog steeds is geselecteerd, de optie **Resultaten** in het actievenster.
1. Selecteer op de pagina **Resultaten van testvariabelen** in het actievenster de optie **Nieuw** om een rij aan het raster toe te voegen. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Resultaat**: voer een unieke id of naam voor het resultaat in.
    - **Beschrijving**: voer een gedetailleerde beschrijving voor het resultaat in.
    - **Resultaat**: selecteer *Goedgekeurd* of *Afgekeurd* om aan te geven of de test is geslaagd of mislukt wanneer het resultaat als testresultaat wordt geselecteerd.

1. Herhaal de vorige stap voor elk extra resultaat. Zorg ervoor dat ten minste één uitkomst de uitslagstatus *Goedgekeurd* heeft en ten minste één resultaat de uitslagstatus *Afgekeurd*.
1. Sluit de pagina's.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Testinstrumenten voor kwaliteitsbeheer](quality-test-instruments.md)
- [Kwaliteitsbeheertests](quality-tests.md)
- [Testgroepen voor kwaliteitsbeheer](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
