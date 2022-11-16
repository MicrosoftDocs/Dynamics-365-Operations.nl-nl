---
title: Aanvullingsmethoden en hoeveelheidswijziging
description: Dit artikel geeft informatie over aanvullingsmethoden. Daarnaast wordt uitgelegd hoe de meervoudige bestelhoeveelheid voor een product invloed heeft op het resultaat.
author: t-benebo
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e0fe6c1f49bc0f6887f1b29118c1fee7a6222f
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739751"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Aanvullingsmethoden en hoeveelheidswijziging

[!include [banner](../../includes/banner.md)]

Dit artikel geeft informatie over aanvullingsmethoden. Daarnaast wordt uitgelegd hoe de meervoudige bestelhoeveelheid voor een product invloed heeft op het resultaat.

Aanvullingsmethoden worden ook wel methoden voor behoefteplanning en partijgroottebepaling genoemd.

## <a name="coverage-codes"></a>Dekkingscodes

Hoofdplanning kan worden geconfigureerd om verschillende aanvullingsmethoden te gebruiken. De aanvullingsmethoden zijn de technieken die door het systeem worden gebruikt om behoeften aan een product te berekenen. Aanvullingsmethoden worden gedefinieerd met behoefteplanningscodes die u kunt instellen voor de behoefteplanningsgroep of het product.

De volgende dekkingscodes kunnen worden gebruikt:

- **Periode**: de aanvullingsmethode waarmee alle vraag voor een periode in één order voor het product wordt gecombineerd. De order wordt gepland voor de eerste dag van de periode en de hoeveelheid voldoet aan de nettobehoeften gedurende de vastgestelde periode. De periode begint met de eerste vraag naar het product en geldt voor de gedefinieerde duur. De volgende periode begint met de volgende vereisten van het product. De behoefteplanningscode *Periode* wordt vaak gebruikt voor niet te voorspellen afname van de voorraad, producten die variëren per seizoen of producten met hoge kosten. In de volgende afbeelding ziet u een voorbeeld.

    ![Voorbeeld van het gebruik van behoefteplanningscode Periode.](./media/coverage-code-period.png "Voorbeeld van het gebruik van behoefteplanningscode Periode")

- **Vereiste**: in de aanvullingsmethode maakt het systeem een geplande inkoop-, transfer- of productieorder per behoefte voor het product. Deze methode wordt gebruikt voor kostbare producten met een per periodieke vraag. De behoefteplanningscode *Vereiste* wordt vaak gebruikt voor configureerbare producten of op orderscenario's voor producten die op bestelling worden gemaakt. In de volgende afbeelding ziet u een voorbeeld.

    ![Voorbeeld van het gebruik van behoefteplanningscode Vereiste.](./media/coverage-code-requirement.png "Voorbeeld van het gebruik van behoefteplanningscode Vereiste")

- **Min./Max.** : de aanvullingsmethode is gebaseerd op het voorraadniveau. Deze definieert de aanvulling van de voorraad tot een specifiek niveau wanneer het voorspelde niveau van de voorhanden voorraad onder een bepaalde drempel ligt. De aanvullingshoeveelheid is het verschil tussen het maximumniveau en het voorspelde voorhanden niveau. De behoefteplanningscode *Min./Max.* wordt vaak gebruikt voor voorspelbare afname van de voorraad, snellopers of minder dure producten. In de volgende afbeelding ziet u een voorbeeld.

    ![Voorbeeld van het gebruik van behoefteplanningscode Min./Max.](./media/coverage-code-min-max.png "Voorbeeld van het gebruik van behoefteplanningscode Min./Max.")

- **Handmatig**: in de aanvullingsmethode stelt het systeem geen inkoop-, transfer- of productieorders voor het product voor. In plaats daarvan is de planner voor het product verantwoordelijk voor het maken van de vereiste orders voor de aanvulling van het product. De behoefteplanningscode *Handmatig* wordt vaak gebruikt voor producten waar geen door het systeem gegenereerde geplande orders nodig zijn.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Impact van de bestelhoeveelheid vanuit de standaard orderinstellingen

Op de pagina **Standaard orderinstelling** voor een vrijgegeven product kunt u elk van de volgende hoeveelheidsinstellingen opgeven op de sneltabbladen **Inkooporder**, **Voorraad** en **Verkooporder**. (Het sneltabblad **Voorraad** wordt zowel gebruikt voor transferorders als productieorders.)

- **Veelvoud**: geplande orders worden een veelvoud van deze hoeveelheid.

    Als het veld **Veelvoud** bijvoorbeeld is ingesteld op *5*, kan er een order zijn voor een hoeveelheid van 5, 10, 15, 20 enzovoort.

- **Min. bestelhoeveelheid**: geplande orders zijn niet minder dan de opgegeven waarde.

    Als het veld **Min. bestelhoeveelheid** bijvoorbeeld is ingesteld op *10*, wordt een geplande order gemaakt voor een hoeveelheid van tien, zelfs als er slechts vier zijn vereist om aan de vraag te voldoen.

- **Max. bestelhoeveelheid**: geplande orders overschrijden de opgegeven waarde niet. Als de vraag groter is dan de waarde van **Max. bestelhoeveelheid**, worden er meerdere geplande orders gemaakt om deze te dekken.

    Als het veld **Max. bestelhoeveelheid** bijvoorbeeld is ingesteld op *100* en de vraag 450 is, worden er vier geplande orders gemaakt voor een hoeveelheid van 100 en één geplande order voor een hoeveelheid van 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Voorbeelden van aanvulling met de behoefteplanningscode Min./Max.

Als u geen waarde in het veld **Veelvoud** opgeeft voor een product op de pagina **Standaard orderinstelling** en als u de aanvullingsmethode *Min./Max.* gebruikt, wordt de voorraad door de hoofdplanning aangevuld tot een specifiek niveau wanneer het voorspelde niveau van de voorhanden voorraad onder een bepaalde drempel ligt.

Als u een meervoudige hoeveelheid voor een product definieert, wijzigt de aanvullingsmethode *Min./Max.* het gedrag en houdt rekening met de waarde van **Veelvoud**.

Met andere woorden, via de hoofdplanning wordt de voorraad nog steeds aangevuld tot het gedefinieerde maximumniveau wanneer de voorspelde hoeveelheid voor voorhanden voorraad kleiner is dan het gedefinieerde minimumniveau. De aanvullingshoeveelheid moet echter een veelvoud van de waarde van **Veelvoud** zijn.

Als de aanvullingshoeveelheid (het verschil tussen het maximumniveau en het voorspelde voorhanden-voorraadniveau) geen veelvoud van de gedefinieerde meervoudige hoeveelheid is, wordt in de hoofdplanning de eerste mogelijke waarde gebruikt die, samen met het voorspelde voorhanden-voorraadniveau, onder het maximumniveau ligt. Als de som kleiner is dan het minimumniveau, wordt door de hoofdplanning de eerste waarde gebruikt die, samen met de voorspelde voorhanden voorraad, boven het maximumniveau uitkomt.

De volgende subsecties geven enkele voorbeelden die laten zien hoe de meervoudige bestelhoeveelheid voor een product invloed heeft op het resultaat van de *Min./Max.*- aanvullingsmethode.

### <a name="example-1"></a>Voorbeeld 1

Een product heeft de volgende configuratie:

- **Behoefteplanningscode**: *Min./Max.*
- **Minimum:** *15*
- **Maximum:** *22*
- **Veelvoud:** *0*

Er zijn 10 stuks op voorraad voor het product en er is geen andere vraag of aanbod.

Wanneer de hoofdplanning wordt uitgevoerd, wordt een geplande order voor 12 stuks gemaakt om de voorraad aan te vullen tot de maximumhoeveelheid.

### <a name="example-2"></a>Voorbeeld 2

Een product heeft de volgende configuratie:

- **Behoefteplanningscode**: *Min./Max.*
- **Minimum:** *15*
- **Maximum:** *22*
- **Veelvoud:** *5*

Er zijn 10 stuks op voorraad voor het product en er is geen andere vraag of aanbod.

Wanneer de hoofdplanning wordt uitgevoerd, wordt een geplande order voor 10 stuks gemaakt (omdat 15 stuks aanvulling plus 10 stuks van de beschikbare voorraad de maximumhoeveelheid overschrijden).

### <a name="example-3"></a>Voorbeeld 3

Een product heeft de volgende configuratie:

- **Behoefteplanningscode**: *Min./Max.*
- **Minimum:** *21*
- **Maximum:** *24*
- **Veelvoud:** *5*

Er zijn 10 stuks op voorraad voor het product en er is geen andere vraag of aanbod.

Wanneer de hoofdplanning wordt uitgevoerd, wordt de geplande order voor 15 stuks gemaakt (omdat 10 stuks aanvulling plus 10 stuks van de beschikbare voorraad minder zijn dan de minimumhoeveelheid).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
