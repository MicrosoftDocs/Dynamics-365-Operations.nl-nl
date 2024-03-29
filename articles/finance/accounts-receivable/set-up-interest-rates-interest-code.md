---
title: Rentepercentages instellen voor een rentecode
description: Rentecodes bevatten instellingen die bepalen wanneer kosten voor de rente geheven worden en hoe deze berekend wordt op achterstallige rekeningen.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: kfend
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c1d85e50a8e6f57ed0678fa6169d94152320861
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726067"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a>Rentepercentages instellen voor een rentecode

[!include [banner](../includes/banner.md)]

Rentecodes bevatten instellingen die bepalen wanneer kosten voor de rente geheven worden en hoe deze berekend wordt op achterstallige rekeningen.

U kunt een enkele rentecode instellen en deze toepassen op meerdere klantboekingsprofielen, factureringscodes of op specifieke factuurregels. Als de details van de rentecode veranderen, zullen alle functies die de code gebruiken de wijzigingen automatisch toepassen op nieuwe transacties. U kunt twee typen tarieven instellen voor elke rentecode:
-   Tarieven voor rente-inkomsten - Dit zijn inkomsten die worden gehaald door het aanrekenen van rente op facturen of rentenota's.
-   Tarieven voor rentebetalingen - Deze vormen kosten die betaald worden voor de rente op creditnota's.

Beide tarieftypes kunnen tegelijkertijd en in dezelfde rentecode bestaan. Rentetarieven kunnen worden gebaseerd op drie berekeningstypen:
-   Rente volgens percentage.
-   Rente volgens bedrag.
-   Rente volgens bereik, wat leidt tot een enkel percentage of bedrag.

Wanneer een rentecode wordt gebruikt om rente te berekenen, wordt een afzonderlijke rentecode gemaakt voor elke rentevoet die van toepassing is gedurende de periode dat de betaling de vervaldatum van de transactie heeft overschreden. U gebruikt het tabblad **Inkomsten** op de pagina **Rentecode** om rentepercentages in te stellen voor rente die u verdient door rente aan te rekenen. Gebruik het tabblad **Betalingen** voor het instellen van rentetarieven voor de rente die u betaalt.

## <a name="interest-rates-based-on-a-percentage"></a>Rentevoeten op basis van een percentage
U kunt de rentevoeten instellen die een opgegeven percentage berekenen.

- Rentebedrag is van toepassing op alle valuta's.
- Optionele limieten voor het rentebedrag kunnen worden ingevoerd.
- **Percentage** is geselecteerd in het veld **Rente berekenen op basis van** op de pagina **Rentecodes instellen**.

Als u bijvoorbeeld een rentecode wilt instellen die 5 procent rente aanrekent voor elke twee maanden dat de factuurbetaling voorbij de vervaldatum is, voert u 2 in het veld **Bereken rente elke** in en selecteert u **Maand**.

> [!NOTE] 
> Het nieuwe algoritme voor het berekenen van rentenota's wordt toegevoegd met behulp van Functiebeheer. Als u dit algoritme wilt gebruiken, moet u de functie **(GBL) Toestaan om rente per dag te berekenen als jaarlijks percentage gedeeld door 365** inschakelen. Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie over het inschakelen van de functie.
> 
> De formule voor de berekening van het rentenotabedrag luidt: 
>  
> Bedrag rentenota = Verschuldigd bedrag * Jaarlijks rente % / 365 * Aantal dagen achterstallig
>  
> Deze functie is beschikbaar in versie 10.0.18 of hoger.    
 
## <a name="interest-rates-based-on-amounts"></a>Rentevoeten op basis van bedragen
U kunt de rentevoeten instellen die een opgegeven bedrag berekenen per valuta.
- Een rentebedrag wordt opgegeven voor elke valuta in de rentecode.
- Optionele limieten voor het rentebedrag kunnen worden ingevoerd.
- **Bedrag** is geselecteerd in het veld **Rente berekenen op basis van** op de pagina **Rentecodes instellen**.

Als u bijvoorbeeld een rentecode wilt instellen die 25,00 rente aanrekent voor elke 20 dagen dat de factuurbetaling voorbij de vervaldatum is, voert u 20 in het veld **Bereken rente elke in** en selecteert u **Dag**.

## <a name="interest-rates-based-on-ranges"></a>Rentevoeten op basis van bereiken
U kunt rentevoeten instellen die variëren afhankelijk van het openstaande bedrag, het aantal dagen dat het bedrag vervallen is of het aantal maanden dat het bedrag vervallen is.
-   U kunt het tabblad **Inkomsten per valuta** gebruiken om specifieke rente-instellingen voor elke valuta te definiëren. Hier definieert u ook het bereik.
-   Met de knop **Bereiken** kunt u regels toevoegen voor de bereiken die u wilt instellen. De waarde bij **Van** staat voor het begin van het bereik en de waarde bij **Rentewaarde** staat voor een percentage of bedrag, afhankelijk van de selectie bij **Rente berekenen op basis van** op de pagina **Rentecodes** instellen.

## <a name="example-1-interest-by-range--amount"></a>Voorbeeld 1: Rente volgens bereik = bedrag
U stelt een rentecode in die één keer rente aanrekent voor elke drie maanden dat de factuur voorbij de vervaldatum is. Wilt u de berekening baseren op een percentage rentewaarde, volgens getrapte bedragintervallen. De rentewaarde zal 1 procent zijn voor factuurbedragen tot 1000,00, 2 procent voor bedragen van 1001,00 tot 5000,00 en 3 procent voor bedragen hoger dan 5000,00. U stelt het rentecodeveld als volgt in.

| **Veldnaam**                  | **Veldwaarde** |
|---------------------------------|-----------------|
| **Rentecode**               | 3M%ByAmt        |
| **Bereken rente elke**    | 3/maand         |
| **Rente per bereik**           | Bedrag          |
| **Rente berekenen op basis van** | Percentage      |

U stelt de bereikinformatie als volgt in.

| **Vanaf waarde** | **Rentewaarde** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |


## <a name="example-2-interest-by-range--days"></a>Voorbeeld 2: Rente volgens bereik = Dagen

U stelt een rentecode in die één keer rente aanrekent voor elke 15 dagen dat de factuur voorbij de vervaldatum is. U wilt de berekening baseren op een rentewaarde van een bepaald bedrag, volgens getrapte dagintervallen. De waarde van de rente worden 10,00 per 15 dagen gedurende de eerste 60 dagen 15,00 per 15 dagen van dagen 61-90 en 20,00 per 15 dagen vanaf dag 91 en later. U stelt het rentecodeveld als volgt in.

| **Veldnaam**                  | **Veldwaarde** |
|---------------------------------|-----------------|
| **Rentecode**               | 15DAmtXDay      |
| **Bereken rente elke**    | 15/dag          |
| **Rente per bereik**           | Dagen            |
| **Rente berekenen op basis van** | Bedrag          |

U stelt de bereikinformatie als volgt in.

| **Vanaf waarde** | **Rentewaarde** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |


## <a name="example-3-interest-by-range--months"></a>Voorbeeld 3: Rente volgens bereik = Maanden

U stelt een rentecode in die één keer rente aanrekent voor elke maand dat de factuur voorbij de vervaldatum is. U wilt de berekening baseren op een percentage rentewaarde, volgens getrapte maandintervallen. De waarde van de rente is 1,5 procent per maand voor de eerste drie maanden achterstal, 2,0 procent per maand voor de tweede drie maanden en 2,5 procent per maand voor elke maand voorbij de eerste zes maanden. U stelt het rentecodeveld als volgt in.

| **Veldnaam**                  | **Veldwaarde** |
|---------------------------------|-----------------|
| **Rentecode**               | 1M%ByMth        |
| **Bereken rente elke**    | 1/Maand         |
| **Rente per bereik**           | Maanden          |
| **Rente berekenen op basis van** | Percentage      |

U stelt de bereikinformatie als volgt in.

| **Vanaf waarde** | **Rentewaarde** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2.5                |

## <a name="new-versions"></a>Nieuwe versies
Rentecodes zijn geldig op bepaalde datums. Als u de rentevoet wilt wijzigen, kunt u een **nieuwe versie** maken die vanaf een toekomstige datum geldig is.

Als u verschillende versies wilt bekijken, kunt u de menukeuze **Begindatum** gebruiken om de afsluitdatum te selecteren. U kunt ook **Alle records weergeven** selecteren om alle rentecodes op de pagina weer te geven.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
