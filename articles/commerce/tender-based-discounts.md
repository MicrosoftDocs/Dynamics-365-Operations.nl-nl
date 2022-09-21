---
title: Kortingen op basis van een betalingsmethode
description: Dit artikel beschrijft de functionaliteit waarmee detailhandelaren kortingen voor specifieke betalingstypen kunnen configureren in Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: b11145c0c12f973b437ebf87921a5686d217d327
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473775"
---
# <a name="tender-based-discount"></a>Korting op basis van een betalingsmethode

[!include [banner](includes/banner.md)]

Dit artikel beschrijft de functionaliteit waarmee detailhandelaren kortingen voor specifieke betalingstypen kunnen configureren in Microsoft Dynamics 365 Commerce.

Dit wordt door detailhandelaren veelvuldig gebruikt voor het uitgeven van persoonlijke merkcreditcards. Het voordeel voor detailhandelaren is dat ze speciale koersen van de banken krijgen. En omdat deze creditcards klanten stimuleren om vaker naar de winkel te komen, hebben ze ook een positieve invloed op de omzet van de detailhandelaar. Detailhandelaren hebben dan ook een drijfveer om het klantgebruik van hun merkcreditcards te verbeteren. Om dit doel te bereiken, bieden ze vaak extra kortingen aan klanten die deze creditcards gebruiken.

Detailhandelaren die geen merkcreditcards aanbieden, willen klanten mogelijk aanmoedigen om met een ander betaalmiddel te betalen, zoals contant, met geschenkbonnen of loyaliteitspunten. Op deze manier kunnen ze onkosten voor de verwerking van creditcardbetalingen verlagen. Detailhandelaren zouden in dat geval korting kunnen geven aan klanten die deze alternatieve betalingsmethoden gebruiken.

## <a name="tender-based-discount"></a>Korting op basis van een betalingsmethode

Commerce ondersteunt *een korting op basis van betalingsmethode*, zodat detailhandelaren een kortingspercentage kunnen configureren dat wordt toegepast op een transactie als het transactietotaal hoger is dan een specifiek bedrag en de klant betaalt met het voorkeursbetalingstype. De korting is gebaseerd op het niveau, zodat verschillende kortingspercentages kunnen worden gekoppeld aan verschillende bedragdrempels. De klant kan zelf bepalen of hij een gedeeltelijke of volledige betaling wil doen, en in de prijsengine wordt het juiste kortingsbedrag vastgesteld. De korting op basis de betalingsmethode wordt altijd gegeven voor het bedrag vóór de btw op de verkoopregels.

De korting op basis van de betalingsmethode kan alleen worden toegepast op verkoopregels waarvan de prijzen niet zijn vergrendeld, en wordt evenredig verdeeld over de desbetreffende regels. Als er nieuwe verkoopregels aan een order worden toegevoegd, wordt de korting op basis van betalingsmethode alleen tijdens de betaling op de nieuwe verkoopregels toegepast. Wanneer een klantorder wordt geplaatst voor ophalen of levering, wordt de korting op basis van betalingsmethode alleen toegepast op het depositobedrag. Nadat de order is geplaatst, tijdens de uitvoering, zijn de prijzen van de verkoopregels vergrendeld. Er wordt geen korting op basis van betalingsmethode toegepast op een saldo dat is betaald tijdens het ophalen of is geautoriseerd tijdens de verzending. De korting op basis van betalingsmethode kan alleen worden toegepast op het gehele bedrag van een klantorder als de detailhandelaar het hele bedrag als deposito int terwijl de order wordt geplaatst.

Kortingen op basis van betalingsmethode kunnen niet overeenkomen met kortingen op basis van een artikel, zoals eenvoudige kortingen, hoeveelheidskortingen, drempelkortingen, combinatiekortingen en handmatige kortingen. Kortingen op basis van betalingsmethode worden altijd samengesteld boven de kortingen op basis van het artikel. Dus zelfs als een exclusieve korting op een artikel wordt toegepast, kan de korting op basis van de betalingsmethode boven op de exclusieve periodieke korting worden toegepast. En als er een drempelkorting wordt toegepast op de transactie en de korting op basis van de betalingsmethode het totaal doet afnemen tot onder de drempelwaarde, wordt de drempelkorting toch toegepast op de transactie.

Ook al verminderen kortingen op basis van betalingsmethode het subtotaal, dit heeft geen invloed op automatische kosten die op de transactie worden toegepast. Als de leveringskosten bijvoorbeeld als $ 5 zijn omdat het subtotaal hoger is dan $ 100, en de korting op basis van betalingsmethode het bedrag vermindert tot minder dan $ 100, dan zijn de leveringskosten voor de order nog steeds $ 5.

De korting op basis van betalingsmethode is momenteel beperkt tot twee betalingstypen: creditcards en contante betaling. Als er meerdere kortingen op basis van betalingsmethode voor een betalingstype zijn geconfigureerd, wordt alleen de beste korting op basis van betalingsmethode toegepast.

## <a name="pos-user-experience"></a>POS-gebruikerservaring

Als een korting op basis van betalingsmethode voor contante betaling is ingesteld en de kassamedewerker op het verkooppunt (POS) de knop **Contante betaling** selecteert voor een contante transactie, wordt de korting op basis van betalingsmethode automatisch toegepast op de transactie. Het verlaagde bedrag wordt vervolgens weergegeven als het saldo. Als de kassamedewerker echter de knop **Vorige** in het betalingsscherm selecteert, wordt de korting verwijderd en wordt het oorspronkelijke bedrag in het transactiescherm weergegeven. De korting op basis van betalingsmethode wordt verwijderd als de betalingsregel ongeldig wordt gemaakt.

Voor creditcardbetalingen kunnen detailhandelaren de korting op basis van betalingsmethode instellen voor een of meer typen creditcards. Het systeem kan echter niet controleren welk type creditcard wordt gebruikt, tenzij de kaart is geautoriseerd. Als de korting wordt toegepast na autorisatie, geldt de betalingsautorisatie voor een groter bedrag, maar wordt er een lager bedrag vastgelegd. Om een dergelijke situatie te voorkomen, ziet de kassamedewerker wanneer een klant met een creditcard betaalt, een dialoogvenster met een overzicht van voorkeurskaarten die de klant extra korting geven. De kassamedewerker kan de klant vervolgens vragen of de klant een van de voorkeurskaarten wil gebruiken om meer korting te krijgen. Als de kassamedewerker een voorkeurskaart selecteert, wordt de korting op basis van betalingsmethode op de transactie toegepast en wordt het verlaagde bedrag in het betalingsvenster weergegeven. De autorisatie geldt dan voor het verlaagde bedrag. Als de klant een andere kaart invoert dan de kaart die de kassamedewerker heeft geselecteerd, wordt een foutbericht weergegeven en wordt de autorisatie ongeldig gemaakt.

## <a name="call-center-user-experience"></a>Gebruikerservaring van callcenter

Wanneer een gebruiker in een callcenter de optie **Voltooien** selecteert, wordt het scherm **Totalen** weergegeven. In eerste instantie bevatten de totalen in dit scherm geen kortingen op basis van betalingsmethode omdat de betalingsmethode nog niet is geselecteerd. Als de gebruiker in het scherm **Betaling toevoegen** de betalingsmethode selecteert waarvoor de korting op basis van betalingsmethode is geconfigureerd, wordt het betalingsbedrag automatisch aangepast, zodat dit het kortingsbedrag weerspiegelt. Net als een klant bij het POS kan de callcenterklant besluiten om de volledige of een gedeeltelijke betaling te doen. Op basis van het betaalde bedrag wordt de korting op basis van betalingsmethode op de verkooporder toegepast.

> [!NOTE]
> Er wordt geen kaartvalidatie uitgevoerd voor callcenterorders. Als de callcentergebruiker bijvoorbeeld de Visa-creditcard selecteert, maar de klant zijn Master Card gebruikt, past het systeem de korting nog steeds toe.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
