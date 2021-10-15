---
title: Intercompany-orders en -retourorders
description: In dit onderwerp komen intercompany-orders en -retourorders aan de orde.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 103225595e82bdedec6d97e5ebe5b61498377065
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548202"
---
# <a name="intercompany-orders-and-return-orders"></a>Intercompany-orders en -retourorders

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe intercompany-inkooporders, verkooporders, retourorders, inkoopovereenkomsten en verkoopovereenkomsten worden gemaakt en bijgewerkt.

## <a name="about-intercompany-orders"></a>Over intercompany-orders

Wanneer u een intercompany-verkooporder maakt, wordt in Microsoft Dynamics 365 Supply Chain Management automatisch een bijbehorende inkooporder gemaakt. Andersom geldt ook dat er automatisch een bijbehorende intercompany-verkooporder wordt gemaakt als u een intercompany-inkooporder maakt.

Dit geldt voor tweeledige orders (transacties tussen twee gerelateerde bedrijven) en voor de meeste drieledige bedrijven (wanneer een intercompany-transactie voortkomt uit een verkooporder voor een externe klant).

## <a name="intercompany-order-example"></a>Voorbeeld van intercompany-order

U hebt twee gerelateerde bedrijven. Bedrijf A is een verkoopdochtermaatschappij en bedrijf B is een distributie-eenheid. In de volgende scenario's worden automatisch intercompany-verkooporders en -inkooporders gemaakt:

- Wanneer bedrijf A een inkooporder maakt en bedrijf B de leverancier is, wordt er automatisch een intercompany-verkooporder gemaakt in bedrijf B. De tweeledige orderketen bestaat uit een inkooporder in bedrijf A en een intercompany-verkooporder in bedrijf B.
- Wanneer bedrijf B een verkooporder maakt en bedrijf A de klant is, wordt er automatisch een intercompany-inkooporder gemaakt in bedrijf A. De tweeledige orderketen bestaat uit een verkooporder in bedrijf B en een intercompany-inkooporder in bedrijf A.
- Wanneer bedrijf A eerst een verkooporder maakt voor een externe klant, kan er automatisch een inkooporder worden gemaakt in bedrijf A, waarna er automatisch een intercompany-verkooporder wordt gemaakt in bedrijf B. De drieledige orderketen bestaat uit een verkooporder en een inkooporder in bedrijf A en een intercompany-verkooporder in bedrijf B.

## <a name="about-intercompany-return-orders"></a>Over intercompany-retourorders

U kunt intercompany-artikelen op dezelfde manier retour sturen als normale retouren. Bij intercompany-artikelen wordt met de retourorder van de externe klant echter een intercompany-inkooporder gemaakt. Dit leidt er weer toe dat er automatisch een intercompany-verkoopretourorder wordt gemaakt. U kunt een intercompany-artikel ook retourneren zonder retourorder van de externe klant.

Intercompany-retourorders, zoals bijvoorbeeld normale retourorders, worden gestart op de pagina **Retourorder maken**.

In Microsoft Dynamics 365 Supply Chain Management worden intercompany-verkoopovereenkomsten en -inkoopovereenkomsten automatisch bijgewerkt om een geretourneerd artikel weer te geven. De verkoop- of inkoopovereenkomst voor dat artikel wordt automatisch aangepast om de wijziging in de hoeveelheid of het bedrag weer te geven wanneer een artikel wordt geretourneerd.

## <a name="intercompany-return-order-example"></a>Voorbeeld van een intercompany-retourorder

Bedrijf A maakt een inkooporder die is gekoppeld aan een inkoopovereenkomst voor een intercompany-artikel. In bedrijf B wordt automatisch een intercompany-verkooporder gemaakt die is gekoppeld aan de overeenkomstige verkoopovereenkomst. De inkoopovereenkomst en de verkoopovereenkomst zijn gerelateerd als intercompany-overeenkomsten.

Bedrijf A retourneert het intercompany-artikel aan bedrijf B. Bedrijf B maakt een retourorder voor het artikel en in bedrijf A wordt automatisch een inkoopretourorder gemaakt. De toezeggingen van de inkoopovereenkomst en de verkoopovereenkomst die zijn gekoppeld aan de oorspronkelijke orders worden automatisch aangepast zodat de wijzigingen in hoeveelheid of bedrag worden weergegeven.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
