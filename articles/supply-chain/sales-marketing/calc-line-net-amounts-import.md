---
title: Regelnettobedragen opnieuw berekenen bij het importeren van verkooporders en offertes
description: In dit artikel wordt beschreven of en hoe het systeem regelnettobedragen opnieuw berekent wanneer verkooporders en offertes worden geïmporteerd. Daarnaast wordt uitgelegd hoe u het gedrag in verschillende versies van Microsoft Dynamics 365 Supply Chain Management kunt bepalen.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719329"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Regelnettobedragen opnieuw berekenen bij het importeren van verkooporders en offertes

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven of en hoe het systeem regelnettobedragen opnieuw berekent wanneer verkooporders en offertes worden geïmporteerd. Daarnaast wordt uitgelegd hoe u het gedrag in verschillende versies van Microsoft Dynamics 365 Supply Chain Management kunt bepalen.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>De manier waarop updates van nettoregelbedragen bij het importeren worden berekend

In Supply Chain Management 10.0.23 is [bugfix 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) geïntroduceerd. Dit bugfix heeft de voorwaarden gewijzigd waaronder het veld **Nettobedrag** op een regel kan worden bijgewerkt of opnieuw kan worden berekend wanneer updates van bestaande verkooporders en offertes worden geïmporteerd. In versie 10.0.29 kunt u dit achtervoegsel vervangen door de functie *Nettobedrag per regel berekenen bij import* in te schakelen. Deze functie heeft een vergelijkbaar effect, maar biedt een globale instelling waarmee u zo nodig kunt terugkeren naar het oude gedrag. Hoewel het nieuwe gedrag ervoor zorgt dat het systeem intuïtiever werkt, kan dit onverwachte resultaten opleveren in specifieke scenario's waarin aan alle volgende voorwaarden wordt voldaan:

- Gegevens waarmee bestaande records worden bijgewerkt, worden geïmporteerd via de entiteit *Verkooporderregels V2*, *Regels van verkoopofferte V2* of *Retourorderregels* via Open Data Protocol (OData), inclusief situaties waarin u de functies voor twee keer wegschrijven en importeren/exporteren via Excel en bepaalde integraties van derden gebruikt.
- [Evaluatiebeleid voor handelsovereenkomsten](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) dat van toepassing is, stelt een wijzigingsbeleid in dat updates in het veld **Nettobedrag** op verkooporderregels, verkoopofferteregels en/of retourorderregels beperkt. Voor retourorderregels wordt het veld **Nettobedrag** altijd berekend en kan het niet handmatig worden ingesteld.
- De geïmporteerde gegevens omvatten wijzigingen in het veld **Nettobedrag** op regels of wijzigingen (bijvoorbeeld in de eenheidsprijs, hoeveelheid of korting) die ertoe leiden dat de waarde van het veld **Nettobedrag** op regels opnieuw moet worden berekend voor een of meer bestaande regelrecords.

In deze specifieke scenario's is het effect van het evaluatiebeleid voor handelsovereenkomsten het beperken van updates van het veld **Nettobedrag** op de regel. Deze beperking wordt ook wel een *wijzigingsbeleid* genoemd. Als u nu de gebruikersinterface gebruikt om het veld te bewerken of opnieuw te berekenen, wordt u door het systeem gevraagd te bevestigen of u de wijziging wilt aanbrengen. Wanneer u een record importeert, moet het systeem de keuze echter voor u maken. Vóór versie 10.0.23 wordt het regelnettobedrag altijd ongewijzigd gelaten, tenzij het nettobedrag van de inkomende regel 0 (nul) is. In nieuwere versies wordt het nettobedrag echter altijd bijgewerkt of opnieuw berekend als dat nodig is, tenzij expliciet de instructie wordt gegeven om dit niet te doen. Hoewel het nieuwe gedrag logischer is, kan het problemen voor u veroorzaken als u al processen of integraties uitvoert die het oudere gedrag aannemen. In dit artikel wordt beschreven hoe u het oude gedrag zo nodig kunt herstellen.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Berekeningen van regelnettobedragen in versies 10.0.29 en hoger beheren

In Supply Chain Management versie 10.0.29 is de functie *Nettobedrag per regel berekenen bij import* geïntroduceerd. Met deze functie wordt de optie **Nettobedrag per regel berekenen** toegevoegd aan de pagina **Parameters van module Klanten**. Met deze optie kunt u kiezen uit het nieuwe en oudere gedrag voor het berekenen van de nettobedragen per regel bij het importeren.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>De functie Nettobedrag per regel berekenen bij import in- of uitschakelen

Wanneer u bijwerkt naar versie 10.0.29, is de functie *Nettobedrag per regel berekenen bij import* standaard ingeschakeld en wordt de nieuwe optie **Nettobedrag per regel berekenen** in eerste instantie ingesteld op *Ja*. De instelling *Ja* komt overeen met het nieuwe standaardgedrag. Dit komt overeen met het systeemgedrag wanneer de functie is uitgeschakeld, behalve voor de functionaliteit van de parameter [CalculateLineAmount](#CalculateLineAmount), zoals later in dit artikel wordt beschreven. De instelling *Geen* komt overeen met het systeemgedrag vóór versie 10.0.23 en wordt met name geleverd ter ondersteuning van oudere integratiescenario's.

Beheerders kunnen de functie *Nettobedrag per regel berekenen bij import* in- of uitschakelen via het [werkgebied Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>De optie Nettobedrag per regel berekenen instellen

Wanneer de functie *Nettobedrag per regel berekenen bij import* is ingeschakeld, kunt u de optie **Nettobedrag per regel berekenen** als volgt instellen.

1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
1. Stel op het tabblad **Prijzen** op het sneltabblad **Berekening nettobedrag per regel via integratie** de optie **Nettobedrag per regel berekenen** in op een van de volgende waarden:

    - *Ja*: het systeem berekent de regelbedragen altijd opnieuw en werkt deze bij wanneer dat nodig is. (Het evaluatiebeleid voor handelsovereenkomsten wordt genegeerd.)
    - *Nee*: als het bestaande of inkomende nettobedrag voor een regel 0 (nul) is, wordt de waarde voor die regel opnieuw berekend op basis van andere waarden (zoals de eenheidsprijs, hoeveelheid en korting). Als het bestaande of inkomende nettobedrag verschilt van 0 (nul) en er een wijzigingsbeleid is ingesteld voor het veld **Nettobedrag** op de regel, wordt het veld niet opnieuw berekend of bijgewerkt, zelfs niet wanneer inkomende wijzigingen in de regelprijs, hoeveelheid en/of korting zouden impliceren dat het regeltotaal opnieuw moeten worden berekend. Dit gedrag komt overeen met dat van versie 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>De invloed van de functie Nettobedrag per regel berekenen bij import op de parameter CalculateLineAmount

Wanneer de functie *Nettobedrag per regel berekenen bij import* is ingeschakeld, heeft de waarde van de parameter `CalculateLineAmount` voor de tabellen `SalesLine` en `SalesQuotationLine` geen effect. In plaats daarvan wordt het gedrag globaal bepaald door de optie **Nettobedrag per regel berekenen** die in de vorige sectie is beschreven. Wanneer de functie is ingeschakeld, moet u geen conclusies trekken op basis van de waarde van `CalculateLineAmount`.

Wanneer de functie *Nettobedrag per regel berekenen bij import* is uitgeschakeld, werkt de parameter `CalculateLineAmount` voor de tabellen `SalesLine` en `SalesQuotationLine` zoals in Supply Chain Management-versies 10.0.23 tot en met 10.0.28, zoals wordt beschreven in de volgende sectie.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Berekeningen van nettobedragen per regel in versies 10.0.28 en lager beheren

Toen [bugfix 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) in versie 10.0.23 werd geïntroduceerd, werd het mogelijk om op te geven hoe elke relevante gegevensentiteit zich zou moeten gedragen wanneer een nettobedrag per regel werd bewerkt of opnieuw moest worden berekend vanwege andere wijzigingen (zoals een bijgewerkte artikelprijs). U kon dit gedrag bepalen door de nieuwe parameter `CalculateLineAmount` voor elke regel in te stellen op een van de volgende waarden in het geïmporteerde bestand:

- **`CalculateLineAmount` = *1*** – Het veld **Nettobedrag** op de regel wordt altijd opnieuw berekend en bijgewerkt, ongeacht of er een wijzigingsbeleid is ingesteld voor het veld en ongeacht de waarde van het nettobedrag van de inkomende of bestaande regel.
- **`CalculateLineAmount` = *0*** – Als het bestaande of inkomende nettobedrag voor een regel 0 (nul) is, wordt de waarde voor die regel opnieuw berekend op basis van andere waarden (zoals de eenheidsprijs, hoeveelheid en korting). Als het bestaande of inkomende nettobedrag verschilt van 0 (nul) en er een wijzigingsbeleid is ingesteld in het veld **Nettobedrag** op de regel, wordt het veld niet opnieuw berekend of bijgewerkt.  

Het systeemgedrag is afhankelijk van uw versie van Supply Chain Management:

- In versie 10.0.22 gedraagt het systeem zich altijd gedragen alsof `CalculateLineAmount` op *0* is ingesteld en het is niet mogelijk om het systeem zich zo te laten gedragen alsof `CalculateLineAmount` is ingesteld op *1*.
- In versies 10.0.23 tot en met 10.0.28 gedraagt het systeem zich alsof `CalculateLineAmount` is ingesteld op *1* voor alle regels waarbij het niet expliciet is ingesteld op *0* in het importbestand.
