---
title: Naadloos overschakelen naar offline bewerkingen voor cadeaukaarten en creditnota's
description: Dit onderwerp biedt een overzicht van de verbeteringen die een naadloze offline overschakeling biedt voor specifieke betalingstypen.
author: rubendel
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 47867447e6d16a0fb4542c17ab184068300b2c1c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019952"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Naadloos overschakelen naar offline bewerkingen voor cadeaukaarten en creditnota's

[!include [banner](../includes/banner.md)]

Als een POS-apparaat de verbinding met de kanaaldatabase verliest, kunnen de meeste POS-bewerkingen en -transacties doorgaan nadat de kassier een waarschuwingsbericht heeft ontvangen over het verlies van de verbinding. In sommige gevallen hebben transacties echter elementen die afhankelijk zijn van de realtime service en worden deze elementen niet ondersteund wanneer het POS offline is. In dit onderwerp wordt een aantal functies beschreven waarmee u de impact van de verbindingsproblemen in deze scenario's kunt beperken.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Transacties met geschenkbonnen voltooien in offline modus

Interne geschenkbonnen zijn afhankelijk van de realtime service, omdat het saldo van de geschenkbonnen centraal moet worden beheerd in Microsoft Dynamics 365 Commerce Headquarters. Om fraude of andere synchronisatieproblemen te helpen voorkomen, worden geschenkbonnen geblokkeerd zodra ze aan een transactie worden toegevoegd. De vergrendelingsfunctie zorgt ervoor dat een geschenkbon niet tegelijkertijd op meerdere terminals kan worden gebruikt. Wanneer een transactie is afgerond, wordt de geschenkbon bijgewerkt en gedeblokkeerd.

Als de POS-verbinding echter wordt verbroken nadat een geschenkbon aan een transactie is toegevoegd, kan de geschenkbon onbruikbaar worden. Om deze situatie te helpen voorkomen, heeft Dynamics 365 Commerce een parameter waarmee transacties met een geschenkbonregel kunnen worden voltooid als het POS offline is. Wanneer deze parameter is ingeschakeld, worden geschenkbontransacties die offline moeten worden uitgevoerd, samen met offline transacties opgeslagen en worden deze gesynchroniseerd met Commerce Headquarters wanneer de offline transacties worden gesynchroniseerd. Met de synchronisatie wordt de geschenkbon ook ontgrendeld zodat deze kan worden gebruikt op een andere terminal.

Ga naar het tabblad **Boeking** op de pagina **Commerce-parameters** om de functionaliteit voor het voltooien van transacties met geschenkbonnen in te schakelen nadat u bent overgeschakeld naar de offline modus. Ga op dat tabblad naar het sneltabblad **Geschenkbon** en stel **Uitvoeren van transactie met geschenkbon in offline modus toestaan** in op **Ja**.

![Instelling voor offline geschenkbonnen](../media/gift.png)

Commerce-parameters worden doorgaans in de cache opgeslagen. Daarom kan het, nadat de instelling van deze parameter is bijgewerkt en de distributieplanning wordt gestart om de wijziging te synchroniseren met het kanaal, tot 24 uur duren voordat de wijziging van kracht wordt. Als u de wijziging onmiddellijk wilt doorvoeren, moet u Microsoft Internet Information Services (IIS) opnieuw instellen.

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Transacties met creditnota's voltooien in offline modus

Net als interne geschenkbonnen worden creditnota's centraal bijgehouden in Commerce Headquarters. Commerce heeft een parameter waarmee transacties met creditnota's kunnen worden voltooid terwijl het POS offline is. Deze parameter werkt op dezelfde wijze als de parameter voor geschenkbonnen die in de vorige sectie werd genoemd. Wanneer de parameter wordt ingeschakeld, worden transacties met creditnota's die offline moeten worden voltooid, opnieuw gesynchroniseerd met de kanaaldatabase, samen met andere transacties die zijn uitgevoerd terwijl het POS offline was.

Ga naar het tabblad **Boeking** op de pagina **Commerce-parameters** om de functionaliteit voor het voltooien van transacties met creditnota's in te schakelen nadat u bent overgeschakeld naar de offline modus. Ga op dat tabblad naar het sneltabblad **Creditnota** en stel **Uitvoeren van transactie met creditnota in offline modus toestaan** in op **Ja**.

![Instelling voor offline creditnota](../media/creditmemo.png)

Commerce-parameters worden doorgaans in de cache opgeslagen. Daarom kan het, nadat de instelling van deze parameter is bijgewerkt en de distributieplanning wordt gestart om de wijziging te synchroniseren met het kanaal, tot 24 uur duren voordat de wijziging van kracht wordt. Als u de wijziging onmiddellijk wilt doorvoeren, moet u IIS opnieuw instellen.

## <a name="related-topics"></a>Verwante onderwerpen

- [Functionaliteit voor offline verkooppunt (POS)](../pos-offline-functionality.md)
- [Online en offline verkooppuntbewerkingen (POS)](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]