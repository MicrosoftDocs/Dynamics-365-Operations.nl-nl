---
title: De hoeveelheid kan niet worden verlaagd wanneer een verkooporder wordt geannuleerd
description: De hoeveelheid kan niet worden verlaagd wanneer een verkooporder wordt geannuleerd.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3453c83b5e8ead4269a6054167d73a0cd12381ba374b98bc407c01edaa68a1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752629"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>De hoeveelheid kan niet worden verlaagd wanneer een verkooporder wordt geannuleerd

Foutcode: SYS138831

## <a name="symptoms"></a>Symptomen

Het systeem toont het volgende foutbericht:

> De hoeveelheid kan niet worden verlaagd. Het aantal voorraadtransacties in bestelling is te laag omdat naar de hoeveelheid of een deel ervan wordt verwezen door een uitvoerorder of productieorder of is gemarkeerd aan de hand van andere transacties.

## <a name="cause"></a>Oorzaak

Als werk aan een verkooporder is gekoppeld, kunt u de verkooporder pas annuleren als het werk is geannuleerd en omgekeerd. Deze vereiste geldt ook als het werk dat aan de verkooporder is gekoppeld, is afgesloten.

## <a name="resolution"></a>Oplossing

Om dit probleem te verhelpen, voert u de volgende taken uit:

1. Annuleer openstaand werk.
1. Verwijder de lading.
1. Verlaag de verzamelde hoeveelheid.

### <a name="cancel-open-work"></a>Openstaand werk annuleren

Voer de volgende stappen uit om openstaand werk te annuleren.

1. Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.
1. In het veld **Werk-id**, geeft u de id op van het werk dat u wilt annuleren en dat momenteel in **Werkstatus** een waarde heeft zoals *Open*, *Wordt uitgevoerd*, *Geannuleerd*, *Gecombineerd*, or *Afgesloten*.
1. Selecteer **OK**.
1. Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.

### <a name="delete-the-load"></a>De lading verwijderen

Voer de volgende stappen uit om een lading te verwijderen.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Open de relevante verkooporder.
1. Selecteer op het sneltabblad **Verkooporderregels** **Magazijn \> Werkdetails**.
1. Selecteer op de pagina **Werk** in het actievenster op het tabblad **Werk** in de groep **Werk** de optie **Werk annuleren**.
1. Controleer dat het veld **Werkstatus** is ingesteld op *Geannuleerd*.
1. Sluit de pagina **Werk**.
1. Selecteer op de pagina Verkooporderdetails op het sneltabblad **Verkooporderregels** **Magazijn \> Details van lading**.
1. Selecteer in het actievenster **Verwijderen**.
1. Selecteer **Ja** om te bevestigen dat u de lading wilt annuleren.
1. Sluit de pagina **Lading**.

### <a name="reduce-the-picked-quantity"></a>De verzamelde hoeveelheid verlagen

Nadat alle werkzaamheden zijn geannuleerd, voert u de volgende stappen uit om de verzamelde hoeveelheid te verlagen.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Open de relevante verkooporder.
1. Selecteer op het sneltabblad **Verkooporderregels** **Regel bijwerken \> Verzamelen** op de werkbalk.
1. Selecteer op de pagina **Verzamelen** in de sectie **Transacties** de regel waarop het veld **Uitgiftestatus** is ingesteld op *Verzameld*.
1. Selecteer in de sectie **Transacties** **Orderverzamelregel** op de werkbalk.
1. Selecteer in de sectie **Orderverzamelregels** **Alles verzamelen bevestigen** op de werkbalk.
1. Sluit de pagina **Verzamelen**.
1. Selecteer op de pagina Verkooporderdetails in het actievenster op het tabblad **Verkooporder** in de groep **Onderhouden** de optie **Annuleren**.
1. Selecteer **Ja** om te bevestigen dat u de verkooporder wilt annuleren.
