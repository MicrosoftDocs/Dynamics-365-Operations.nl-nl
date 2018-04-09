---
title: "Financiële rapporten proefbalans"
description: In dit artikel worden de standaardrapporten voor proefbalansen beschreven. Hierin worden ook de bouwstenen beschreven die zijn gekoppeld aan deze rapporten, en hoe u de rapporten kunt aanpassen aan uw zakelijke behoeften.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 77e46e8693c65410ac7c44754edcb3c181f2aa18
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="trial-balance-financial-reports"></a>Financiële rapporten proefbalans

[!include[banner](../includes/banner.md)]


In dit artikel worden de standaardrapporten voor proefbalansen beschreven. Hierin worden ook de bouwstenen beschreven die zijn gekoppeld aan deze rapporten, en hoe u de rapporten kunt aanpassen aan uw zakelijke behoeften. 

<a name="default-trial-balance-reports"></a>Standaardrapporten proefbalans
-----------------------------

Drie proefbalansrapporten zijn beschikbaar in Financiële rapportage in Microsoft Dynamics 365 for Finance and Operations.

| Standaardrapport                                 | Functie                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gedetailleerde proefbalans - Standaard               | Verschaft saldogegevens voor alle rekeningen en bevat debet- en creditsaldi, het nettobedrag van deze saldi samen met de transactiedatum, het boekstuk en de journaalomschrijving.                  |
| Overzicht proefbalans – Standaard                | Verschaft saldogegevens voor alle rekeningen en bevat openings- en eindsaldi, debet- en creditsaldi samen met het bijbehorende nettoverschil.                                        |
| Overzicht proefbalansjaar van jaar tot jaar - Standaard | Verschaft saldogegevens voor alle rekeningen en bevat openings- en eindsaldi, debet- en creditsaldi samen met het bijbehorende nettoverschil voor het huidige en het afgelopen jaar. |

## <a name="building-blocks"></a>Bouwstenen
In de financiële rapporten van de proefbalans worden de volgende bouwstenen gebruikt.

| Standaardrapport                                 | Rijdefinitie          | Kolomdefinitie                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Gedetailleerde proefbalans - Standaard               | Proefbalans: standaard | Gedetailleerde proefbalans - Standaard               |
| Overzicht proefbalans – Standaard                | Proefbalans: standaard | Samengevatte proefbalans: standaard                |
| Overzicht proefbalansjaar van jaar tot jaar - Standaard | Proefbalans: standaard | Samengevatte proefbalans van jaar tot jaar: standaard |

### <a name="row-definition"></a>Rijdefinitie

De rijdefinitie, Proefbalans: standaard, bevat één rij die alle hoofdrekeningen bevat. Zo kan iedereen het rapport genereren zonder wijzigingen te hoeven aanbrengen. Wanneer u het rapport weergeeft, zoomt u op één rij in om gegevens over elke rekening te bekijken. U kunt de rijdefinitie wijzigen zodat deze meer details bevat. Als u de rijdefinitie Proefbalans: standaard wilt wijzigen zodat rijen voor alle accounts worden opgenomen, gaat u als volgt te werk.

1.  Klik in het menu **Bewerken** en klik vervolgens op **Rijen invoegen van dimensies**. Met de opdracht **Rijen invoegen van dimensies** kunt u kiezen welke dimensies u in uw rijdefinitie wilt hebben. Voor deze rijdefinitie gaat u **Hoofdrekening** gebruiken.
2.  Zorg ervoor dat **Hoofdrekening** alle en-tekens (&) bevat en klik vervolgens op **OK**.

De rijdefinitie bevat nu alle hoofdrekeningen voor uw standaardrechtspersoon.

### <a name="column-definition"></a>Kolomdefinitie

In elk proefbalansrapport wordt een andere kolomdefinitie gebruikt. Deze kolomdefinities bevatten verschillende typen kolommen om verschillende detailniveaus en financiële gegevens te verschaffen.

-   **Gedetailleerde proefbalans: standaardkolomtypen:**
    -   **DESC**: de omschrijving van de rijdefinitie
    -   **ACCT**: rekeningcodes
    -   **ATTR (3)**: kenmerken:
        -   Transactiedatum
        -   Boekstuk
        -   Journaalomschrijving
    -   **FD**: financiële gegevens die alleen debetbedragen bevatten
    -   **FD**: financiële gegevens die alleen creditbedragen bevatten
    -   **CALC**: het nettoverschil
-   **Samengevatte proefbalans: standaardkolomtypen:**
    -   **ACCT**: rekeningcodes
    -   **DESC**: de omschrijving van de rijdefinitie
    -   **ATTR**: een kernmerk:
        -   Boekstuk
    -   **FD**: de financiële gegevens van het beginsaldo
    -   **FD**: financiële gegevens die alleen debetbedragen bevatten
    -   **FD**: financiële gegevens die alleen creditbedragen bevatten
    -   **CALC**: het nettoverschil
    -   **CALC**: het eindsaldo
-   **Samengevatte proefbalans van jaar tot jaar: standaard:**
    -   **ACCT**: rekeningcodes
    -   **DESC**: de omschrijving van de rijdefinitie
    -   **ATTR**: een kernmerk
        -   Boekstuk
    -   **FD**: de financiële gegevens van het beginsaldo voor het huidige jaar
    -   **FD**: de financiële gegevens die alleen debetbedragen voor het huidige jaar bevatten
    -   **FD**: de financiële gegevens die alleen creditbedragen voor het huidige jaar bevatten
    -   **CALC**: het nettoverschil
    -   **CALC**: het eindsaldo
    -   **FD**: de financiële gegevens die alleen debetbedragen voor het afgelopen jaar bevatten
    -   **FD**: de financiële gegevens die alleen creditbedragen voor het afgelopen jaar bevatten

 

<a name="see-also"></a>Zie ook
--------

[Financiële rapportage](financial-reporting-getting-started.md)

[Financiële rapporten weergeven](view-financial-reports.md)

[Blog met financiële rapportage van Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)




