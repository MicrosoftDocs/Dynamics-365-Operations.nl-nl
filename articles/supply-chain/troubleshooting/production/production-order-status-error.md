---
title: Fout bij het wijzigen van status van Gereedgemeld in Beëindigd
description: Er wordt mogelijk een foutbericht weergegeven wanneer u de status van een productieorder wijzigt van Gereedgemeld in Beëindigd. Op deze pagina wordt uitgelegd hoe u het probleem oplost.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476018"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Fout bij het wijzigen van status van productieorder van Gereedgemeld in Beëindigd

## <a name="symptoms"></a>Symptomen

Wanneer de status van een productieorder wordt gewijzigd van Gereedgemeld in Beëindigd, worden de volgende foutberichten weergegeven:

> Conflict tijdens bijwerken. De standaardkosten komen niet overeen met de financiële voorraadwaarde na het bijwerken.

> Er is een kritieke fout opgetreden in functie InventCostMovement. checkVariance.

## <a name="cause"></a>Oorzaak

Dit probleem treedt op omdat de onderliggende gegevens zijn gewijzigd door een ander proces. Tijdens het proces wordt geprobeerd de gegevens maximaal vijf keer bij te werken. Als het conflict na vijf pogingen nog steeds optreedt, wordt een van de bovenstaande foutberichten weergegeven.

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. Als u het probleem wilt verhelpen, hervat u de batchtaak. De uitvoering wordt voltooid.

Als de batchtaak na het hervatten steeds mislukt, controleert u of de afrondingsprecisie voor de standaardvaluta van het grootboek voldoet aan de afronding die is toegepast op waarden in de tabel InventSum. Als de afrondingsprecisie is gewijzigd in een niet-compatibele waarde, moet u de waarde waarschijnlijk terugzetten naar een compatibele waarde. Zoek naar **ModifiedDateTime**. In dit geval geeft de waarde meestal aan dat de afrondingsprecisie onlangs is gewijzigd.
