---
title: Verschillen in gegevens op inkooporderregels
description: U ziet gegevensverschillen of -beschadiging op uw inkooporderregels.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100799"
---
# <a name="purchase-order-line-data-discrepancies"></a>Verschillen in gegevens op inkooporderregels

## <a name="symptoms"></a>Symptomen

Wanneer u de regels van een inkooporder controleert, ziet u een of meer van de volgende problemen:

- Er bestaat een gegevensverschil of -beschadiging in restanten van inkooporderregels (levering of factuur).
- Er is sprake van een beschadiging in een inkooporderregel of koptekststatus.
- U kunt een inkooporder niet factureren omdat u bijvoorbeeld een of meer van de volgende foutberichten ontvangt:

    - Gestopt (fout): de transactie is al geboekt.
    - Kan de hoeveelheid niet factureren omdat er onvoldoende voorraadtransacties met de status Ontvangen zijn.
    - Onvoldoende voorraadtransacties met de status Ingekocht" voor artikel %0 met de hoeveelheid %1.

- U kunt een inkooporder niet voltooien of afsluiten, bijvoorbeeld vanwege een van de volgende problemen:

    - De knop **Voltooien** is niet beschikbaar.
    - U kunt de bestelde hoeveelheid van een inkooporderregel niet annuleren voor een inkooporder met een bevestigde en ontvangen status.

## <a name="cause"></a>Oorzaak

Deze problemen worden meestal veroorzaakt door gegevensbeschadigingen of een verschil in de resterende hoeveelheden voor een of meer inkooporderregels.

## <a name="resolution"></a>Oplossing

U kunt deze problemen meestal oplossen door de inkoopstatus, restanten voor leveringen en/of factuurrestanten voor de relevante inkooporderregels bij te werken, zoals wordt beschreven in de volgende procedure.

1. Ga naar **Inkoopbeheer \> Periodieke taken \> Opschonen \> Inkooporderregels handmatig corrigeren**.
1. Zoek in het veld **Inkooporder** naar de inkooporder die problemen oplevert en selecteer deze.
1. Selecteer een regel waar u een verschil hebt gevonden in de sectie **Inkooporderregels**.
1. Controleer de weergegeven gegevens in de sectie **Voorraadtransacties**. Bij inconsistenties tussen een inkooporderregel en de voorraadtransacties selecteert u een van de volgende opdrachten in het actievenster, afhankelijk van waar u de inconsistenties ziet:

    - **Opnieuw berekenen \> Nog te leveren opnieuw berekenen**: de status van de inkooporderregel en koptekst wordt automatisch bijgewerkt. Deze functie werkt alleen voor inkooporderregels in voorraad (dat wil zeggen regels waarop het artikel een voorradig artikel is). Niet-voorradige artikelen en catch weight-artikelen worden momenteel niet ondersteund.
    - **Opnieuw berekenen \> Nog te factureren opnieuw berekenen**: de status van de inkooporderregel en koptekst wordt automatisch bijgewerkt. Deze functie werkt alleen voor inkooporderregels in voorraad (dat wil zeggen regels waarop het artikel een voorradig artikel is). Niet-voorradige artikelen en catch weight-artikelen worden momenteel niet ondersteund.
    - **Opnieuw berekenen \> Status opnieuw berekenen**: de status van de geselecteerde regel opnieuw berekenen. Deze berekening is gebaseerd op de bestaande logica. Daarom wordt de status van de inkooporderkoptekst zo nodig bijgewerkt op basis van de nieuwe status van de inkooporderregel.

1. Als u nog steeds verschillen aantreft in de resterende hoeveelheden, kunt u de volgende velden gebruiken om deze direct te bewerken:

    - Nog te leveren
    - Nog te leveren voorraad
    - Resterend gedeelte van factuur
    - Restant voorraadfactuur
