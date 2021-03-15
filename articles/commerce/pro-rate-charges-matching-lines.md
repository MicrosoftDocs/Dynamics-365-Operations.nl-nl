---
title: Toeslagen voor koptekst naar rato verdelen voor overeenkomende verkoopregels
description: In dit onderwerp worden aanvullende mogelijkheden beschreven voor het berekenen en toepassen van automatische toeslagen op Commerce-kanaalorders met behulp van de geavanceerde functie voor automatische toeslagen.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: a05150d8f4c4fa2d50c07c69c5574cdb602a618f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972400"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Toeslagen voor koptekst naar rato verdelen voor overeenkomende verkoopregels


[!include [banner](includes/banner.md)]

Dit onderwerp beschrijft de functionaliteit waarmee automatische toeslagen op koptekstniveau worden gegroepeerd en naar rato worden verdeeld voor Commerce-verkoopregels. Deze functionaliteit is beschikbaar voor transacties die zijn gemaakt op het verkooppunt (POS) in Retail versie 10.0.1 en verkopen die zijn gemaakt in een callcenter in Retail versie 10.0.2.

Deze functionaliteit is alleen beschikbaar als de functie voor [geavanceerde automatische toeslagen](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) is ingeschakeld via de optie op de pagina **Commerce-parameters**. Bovendien kan de verbeterde berekeningsmethode voor automatische toeslagen alleen worden toegepast op verkooporders die zijn gemaakt via Commerce-kanalen (het POS, een callcenter en het platform Dynamics e-Commerce).

Deze nieuwe functionaliteit biedt organisaties meer flexibiliteit in de manier waarop automatische toeslagen op koptekstniveau worden berekend en toegepast op verkooptransacties.

In versies van de app die eerder zijn dan versie 10.0.1, worden automatische toeslagen op koptekstniveau met een specifieke relatie voor leveringsmethode alleen berekend als er een overeenkomst is met de leveringsmethode die is gedefinieerd op de verkooporderkoptekst.

Bijvoorbeeld: automatische toeslagen op koptekstniveau worden gedefinieerd voor leveringsmethode **99** en leveringsmethode **11**. Een verkooporder wordt gemaakt en de leveringsmethode **99** wordt gedefinieerd op de orderkoptekst. Sommige verkoopregels zijn echter zo ingesteld dat ze worden verzonden met behulp van de leveringsmethode **11**. In dit geval worden alleen de toeslagen op koptekstniveau die zijn gekoppeld aan leveringsmethode **99**, meegenomen en toegepast op de verkooporder.

In Commerce hebben de toeslagen op koptekstniveau een extra functie waarmee u een [configuratie van gelaagde toeslagen](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) kunt definiëren die is gebaseerd op de orderwaarde. Bijvoorbeeld: als de orderwaarde tussen 50,00 en 200,00 EUR is, wil een organisatie mogelijk vrachtkosten van 5,00 EUR in rekening brengen. Als de waarde tussen 200,01 en 500,00 EUR ligt, zijn de vrachtkosten echter mogelijk 4,00 EUR.

Sommige organisaties willen de voordelen van de berekening van gelaagde toeslagen die wordt verschaft met de toeslagen op koptekstniveau. In scenario's met gecombineerde leveringsmethoden, wil men er echter ook voor zorgen dat de toeslagen die worden berekend, worden gebaseerd op een overeenkomst met de leveringsmethode die is gedefinieerd op elke verkoopregel.

U kunt automatische toeslagen op koptekstniveau nu zo configureren dat alle leveringsmethoden voor de order worden meegenomen wanneer toeslagen worden berekend. Deze functie vereist een complexere berekeningslogica voor het berekenen van de toeslagen op koptekstniveau. Met deze logica worden alle artikelen gegroepeerd die zijn verzonden met dezelfde leveringsmethode, en die groep wordt behandeld als de berekeningsgroep voor de artikelen wanneer de automatische toeslagen op koptekstniveau worden berekend. Voor artikelen met dezelfde leveringsmethode worden automatische toeslagen berekend op basis van de gecombineerde verkoopwaarde van de artikelen. Op deze manier wordt de juiste laag voor automatische toeslagen bepaald.

Nadat de juiste toeslagen op koptekstniveau zijn verkregen voor de verkooporderregels die worden verzonden met dezelfde leveringsmethode, worden de berekende toeslagen omgeslagen tot het niveau van de verkoopregel. Omdat deze toeslagen op regelniveau zijn en niet op koptekstniveau, wordt een specifiekere koppeling gemaakt tussen het artikel en de toeslagwaarde die ervoor is berekend. Dit gedrag kan handig zijn in scenario´s waarin sprake is van een gedeeltelijke retour, waarbij een organisatie slechts een gedeelte van de toeslag wil restitueren in plaats van de gehele toeslag wanneer slechts bepaalde artikelen worden geretourneerd.

## <a name="scenarios"></a>Scenario's

In de volgende twee voorbeeldscenario's wordt uitgelegd hoe deze toeslagen worden berekend wanneer de nieuwe functionaliteit wordt gebruikt en wanneer deze niet wordt gebruikt.

### <a name="scenario-1"></a>Scenario 1

In dit scenario wordt uitgelegd wat er gebeurt als de optie **Naar rato verdelen voor overeenkomende verkoopregels** is ingesteld op **Nee** in de instellingen voor automatische toeslagen. (De werking is gelijk aan de werking van toeslagen op koptekstniveau in eerdere appversies dan versie 10.0.1.)

In dit scenario heeft de organisatie de toeslagen op koptekstniveau voor relatie voor leveringsmethode **99** en relatie voor leveringsmethode **11** gedefinieerd. Er worden geen automatische toeslagen geconfigureerd voor leveringsmethode **21**.

![Automatische toeslagen voor leveringsmethode 99 wanneer verdeling naar rato voor overeenkomende regels is uitgeschakeld](media/99_disabled.png)

![Automatische toeslagen voor leveringsmethode 11 wanneer verdeling naar rato voor overeenkomende regels is uitgeschakeld](media/11_disabled.png)

Een verkooporder wordt gemaakt in het callcenter en de leveringsmethode wordt ingesteld op **99**. Deze order bevat vijf artikelen. Twee orderregels zijn geconfigureerd voor het gebruik van leveringsmethode **99**, twee regels zijn geconfigureerd voor het gebruik van leveringsmethode **11**, en één regel is geconfigureerd voor het gebruik van leveringsmethode **21**, zoals weergegeven in de volgende tabel.

| Artikel  | Regelhoeveelheid | Bezorgingsmodus | Prijs per eenheid |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | € 10            |
| 81332 | 1             | 99            | $ 50            |
| 81333 | 2             | 11            | € 30            |
| 81334 | 3             | 99            | € 10            |
| 81334 | 3             | 21            | € 5             |

In dit scenario wordt de gehele order geëvalueerd op basis van de tabel voor automatische toeslagen voor leveringsmethode **99**. Het volledige totaal van alle verkoopregels wordt gebruikt om een overeenkomende laag in de configuratie van automatische toeslagen te bepalen, en deze toeslagen worden toegepast op het niveau van de orderkoptekst. In dit voorbeeld is het ordertotaal € 165,00 en de vrachtkosten van € 15,00 worden toegepast op de orderkoptekst. Automatische toeslagen die worden geconfigureerd voor leveringsmethode **11**, worden nooit toegepast of er wordt nooit naar verwezen.

In dit scenario wordt als een klant enkele artikelen op de order retourneert en als de [code voor toeslagen zo is geconfigureerd dat deze wordt gerestitueerd](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), de totale toeslag op koptekstniveau systematisch toegepast op de restitutie, zelfs als slechts enkele artikelen worden geretourneerd.

### <a name="scenario-2"></a>Scenario 2

In dit scenario zijn toeslagen op koptekstniveau gedefinieerd voor relatie voor leveringsmethode **99** en relatie voor leveringsmethode **11**. De optie **Naar rato verdelen voor overeenkomende verkoopregels** is echter ingesteld op **Ja** voor deze tabellen met automatische toeslagen.

![Automatische toeslagen voor leveringsmethode 99 wanneer verdeling naar rato voor overeenkomende regels is ingeschakeld](media/99_enabled.png)

![Automatische toeslagen voor leveringsmethode 11 wanneer verdeling naar rato voor overeenkomende regels is ingeschakeld](media/11_enabled.png)

In dit scenario wordt dezelfde verkooporder gebruikt die vijf regels bevat. De leveringsmethode op de orderkoptekst is ingesteld op **99**, maar de leveringsmethode voor elk artikel op de verkooporder is geconfigureerd, zoals in de volgende tabel wordt weergegeven.

| Artikel  | Regelhoeveelheid | Bezorgingsmodus | Prijs per eenheid |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | € 10            |
| 81332 | 1             | 99            | $ 50            |
| 81333 | 2             | 11            | € 30            |
| 81334 | 3             | 99            | € 10            |
| 81334 | 3             | 21            | € 5             |

Omdat de configuratie voor automatische toeslagen is ingesteld op verdeling naar rato voor overeenkomende verkoopregels, worden de volgende berekeningsstappen uitgevoerd.

1. Alle artikelen met dezelfde leveringsmethode worden gegroepeerd en de totale productwaarde van de artikelen in de groep wordt berekend.

    **Leveringsmethode 11**

    - Artikel 81331, hoeveelheid 1 = € 10
    - Artikel 81333, de hoeveelheid 2 = netto € 60 (€ 30 per eenheid)
    - **Totale productwaarde voor leveringsmethode 11 = € 70**

    **Leveringsmethode 99**

    - Artikel 81332, hoeveelheid 1 = € 50
    - Artikel 81334, hoeveelheid 3 = € 30 netto
    - **Totale productwaarde voor leveringsmethode 99 = € 80**

    **Leveringsmethode 21**

    - Artikel 81334, hoeveelheid 3 = € 15 netto
    - **Totale productwaarde voor leveringsmethode 21 = € 15**

2. Er wordt gezocht naar de configuratie van automatische toeslagen op koptekstniveau die overeenkomt met de instellingen voor klant en leveringsmethode voor elke groep artikelen. Als de configuratie wordt gevonden, wordt gezocht in de gelaagde configuratie om de toeslagen te vinden die moeten worden toegepast, gebaseerd op de totale productwaarde van artikelen in de leveringsmethodegroep.

    **Leveringsmethode 11**

    - Totale productwaarde = € 70
    - **Toeslagwaarde = € 7**

    **Leveringsmethode 99**

    - Totale productwaarde = € 80
    - **Toeslagwaarde = € 15**

    **Leveringsmethode 21**

    - Totale productwaarde = € 15
    - **Toeslagwaarde = € 0** (er zijn geen automatische toeslagen geconfigureerd voor deze combinatie van klant en leveringsmethode.)

    ![Toeslagen van leveringsmethode 11 vallen in de gemarkeerde laag](media/step2mode11.png)

    ![Toeslagen van leveringsmethode 99 vallen in de gemarkeerde laag](media/step2mode99.png)

3. De toeslagwaarde die moet worden toegepast op elke regel, wordt berekend op basis van de logica van verdeling naar rato waarin de proportionele waarde van de regel in verhouding tot de totale productwaarde van de groep wordt meegenomen.

    **Leveringsmethode 11**

    - Toeslagwaarde = € 7
    - Productwaarde groep = € 70
    - Waarde regel 1 = € 10 (= 14,2857 % van de groepswaarde)
    - Waarde regel 3 = € 60 (= 85,7143 % van de groepswaarde)
    - **Regeltoeslag voor regel 1 = € 1**
    - **Regeltoeslag voor regel 3 = € 6**

    **Leveringsmethode 99**

    - Toeslagwaarde = € 15
    - Productwaarde groep = € 80
    - Waarde regel 2 = € 50 (= 62,5 % van de groepswaarde)
    - Waarde regel 4 = € 30 (= 37,5 % van de groepswaarde)
    - **Regeltoeslag voor regel 2 = € 9,38**
    - **Regeltoeslag voor regel 4 = € 5,62**

    **Leveringsmethode 21**

    - Toeslagwaarde = € 0
    - Productwaarde groep = € 15
    - Waarde regel 5 = € 15 (= 100 % van de groepswaarde)
    - **Regeltoeslag voor regel 5 = € 0**

Daarom wordt in dit voorbeeld aan artikel 81334 vrachtkosten van € 5,62 toegewezen. U kunt deze toeslagen bekijken op de pagina **Toeslagen onderhouden** voor de verkoopregel. In de volgende afbeelding ziet u hoe de pagina er voor artikel 81334 uitziet.

![Naar rato verdeelde toeslagen op verkoopregel voor artikel 81334](media/proratedlinecharge.png)

Wanneer deze berekeningsmethode wordt gebruikt in een scenario van een gedeeltelijke retourzending en als de toeslagcode restitueerbaar is, wordt alleen het deel van de toeslag dat is toegewezen aan die regel, gerestitueerd wanneer het artikel wordt geretourneerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Geavanceerde automatische toeslagen voor meerdere kanalen](omni-auto-charges.md)

[Automatische toeslagen per kanaal inschakelen en configureren](auto-charges-by-channel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]