---
title: Opslaglimieten van locatie
description: Dit onderwerp beschrijft de functionaliteit voor opslaglimieten van locaties.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e0adb9d05f0db9bbfe6bfbe72564a4e5e839f163
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004568"
---
# <a name="location-stocking-limits"></a>Opslaglimieten van locatie

[!include [banner](../includes/banner.md)]

U kunt de pagina **Opslaglimieten van locatie** (**Magazijnbeheer \> Instellen \> Magazijn \> Opslaglimieten van locatie**) gebruiken om de belastingscapaciteit op magazijnlocaties te beheren zonder dat u de meer geavanceerde processen voor volumetrische berekeningen van fysieke producten hoeft te gebruiken.

Het doel van de opslaglimieten van locaties is om de maximum hoeveelheid te evalueren die een locatie kan bevatten. U kunt de functie instellen op alle drie niveaus, die elk een tabblad hebben op de pagina **Opslaglimieten van locatie**:

- Producten
- Productvarianten
- Containertypen

Voor elk niveau kunt u verschillende veldwaarden definiëren. Het systeem evalueert vervolgens de capaciteit van een specifieke locatie op basis van de waarden **Hoeveelheid** en **Eenheid** voor elke rij. De meest gedetailleerde overeenkomende record wordt eerst geselecteerd. Een rij met een waarde in het veld **Locatieprofiel-id** bijvoorbeeld wordt geëvalueerd vóór een rij met alleen een waarde in het veld **Magazijn**. De resterende capaciteit wordt ook geëvalueerd op basis van de waarde **Hoeveelheid** voor de record voor de opslaglimiet van de locatie die wordt gebruikt.

In de sectie **Producten** van de pagina kunt u de volgende veldwaarden definiëren voor de zoekopdracht naar opslaglimieten voor locaties:

- Magazijn
- Locatieprofiel-id
- Locatie
- Verpakkingsgroottecategorie-id
- artikelnummer
- Eenheid

> [!NOTE]
> U hoeft geen waarde **Eenheid** voor elke record voor de opslaglimiet van de locatie te definiëren. De berekeningen voor de locatiecapaciteit worden gebaseerd op de hoeveelheden van de voorraadeenheid. Als er geen eenheidsomzetting is gedefinieerd voor een waarde die wordt gebruikt, wordt de record voor de opslaglimiet voor de locatie overgeslagen, alsof er een andere waarde **Artikelnummer** voor is gedefinieerd.

## <a name="example--purchase-order-receiving"></a>Voorbeeld: ontvangen van inkoopregel

Dit voorbeeld is gebaseerd op een schone *USMF*-demogegevensset, waarbij de volgende waarden worden ingesteld op het tabblad **Productvarianten** van de pagina **Opslaglimieten van locatie**.

| Magazijn | Locatieprofiel-id | artikelnummer | Grootte | Hoeveelheid | Eenheid |
|-----------|---------------------|-------------|------|----------|------|
| 24        | VERDIEPING               | D0013       | Ma    | 300      | St.   |
| 24        | VERDIEPING               | D0013       | L    | 240      | St.   |
| 24        | VERDIEPING               | D0013       | Z    | 360      | St.   |

Er zijn verschillende productvarianten voor maateenheden ingesteld voor de producten. Deze varianten worden afgestemd op de opslaglimieten van de locatie voor drie pallets (PL):

- **Grootte M:** 1 PL = 100 st. (EA)
- **Grootte L:** 1 PL = 80 st.
- **Grootte S:** 1 PL = 120 st.

Daarom kan elke locatie waar de waarde **Locatieprofiel-id** is ingesteld op *VERDIEPING* *3* *PL* van het artikelnummer *D0013* bevatten.

### <a name="prepare-for-the-example"></a>Voorbeeld voorbereiden

In dit voorbeeld voert u een ontvangststroom voor de inkooporder uit voor twee regels. U moet de demogegevens echter eerst bijwerken op de volgende manier om ervoor te zorgen dat de locaties toestaan dat gemengde artikelen worden opgenomen, alleen de lege locaties *FL-002* tot en met *FL-004* worden gebruikt en er geen open inkomend werk is.

1. Voor locatie *FL-001* wijzigt u de waarde van het veld **Locatieprofiel** van *VERDIEPING* in *FLOOR-05*.
1. Stel voor het locatieprofiel *VERDIEPING* de optie **Gemengde artikelen toestaan** in op *Ja*.
1. Maak een inkooporder met de volgende twee regels.

    | Magazijn | artikelnummer | Grootte | Hoeveelheid | Eenheid |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | Z    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Het voorbeeld verwerken

U ontvangt eerst een hoeveelheid van *4* eenheden *PL* in grootte *S* en controleert de opslagregellocaties voor het werk dat is gemaakt. U ontvangt vervolgens een hoeveelheid van *4* eenheden *PL* in grootte *L* en controleert de opslagregellocaties voor het werk dat is gemaakt.

1. In de magazijn-app meldt u zich aan met *24* als gebruikers-id en *1* als wachtwoord.
1. Selecteer **Inkomend** \> **Inkoop ontvangen**.
1. Ontvang *4* *PL* van artikelnummer *D0013* in grootte *S*.
1. Controleer het wegzetwerk dat is gemaakt. Het volgende resultaat wordt weergegeven:

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Ontvang *4* *PL* van artikelnummer *D0013* in grootte *L*.
1. Controleer het wegzetwerk dat is gemaakt. Het volgende resultaat wordt weergegeven:

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Op basis van de resultaten kunt u concluderen dat het systeem niet de juiste wegzetlocaties heeft toegewezen. Waarom heeft het systeem anders niet meer dan *1* *PL* van grootte *L* toegevoegd aan locatie *FL-003* in de laatste stap, niet *2* *PL*? Dat wil zeggen, waarom is er geen totaal van *3* *PL* voor wegzetten naar die locatie?

Als u deze duidelijke fout wilt uitleggen, moet u de selectiecriteria voor de opslaglimieten van de locatie begrijpen. Het systeem selecteert de meest gedetailleerde overeenkomende record. In dit voorbeeld is de meest gedetailleerde overeenkomende record de regel waar **Grootte** *L*, **Hoeveelheid** *240* en **Eenheid** *EA* is. Omdat u al open werk hebt van de vorige ontvangst van een hoeveelheid van *120* *EA* van grootte *S*, wordt de resterende capaciteit berekend als *240* – *120* = *120* *Ea*. De resterende capaciteit kan daarom slechts *1* *PL* van *80* *EA* bevatten.

> [!NOTE]
> U kunt opslaglimieten van locaties niet gebruiken om bijvoorbeeld de aanvulling van artikelen met verschillende hoeveelheden op dezelfde locatie te beheren. Gebruik in dit geval een *aanvullingssjabloon*.
