---
title: Kortingen op basis van een betalingsmethode
description: Dit onderwerp bevat een overzicht van de functionaliteit waarmee detailhandelaren kortingen voor specifieke betalingstypen kunnen configureren.
author: bebeale
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 52b9510b2c22157aec27b865115273064bb0e803443306ea20468b93a2ea3ca7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719460"
---
# <a name="tender-based-discounts"></a>Kortingen op basis van een betalingsmethode

[!include [banner](includes/banner.md)]


Dit wordt door detailhandelaren veelvuldig gebruikt voor het uitgeven van persoonlijke merkcreditcards. Het voordeel voor detailhandelaren is dat ze speciale koersen van de banken krijgen. En omdat deze creditcards klanten stimuleren om vaker naar de winkel te komen, hebben ze ook een positieve invloed op de omzet van de detailhandelaar. Detailhandelaren hebben dan ook een drijfveer om het klantgebruik van hun merkcreditcards te verbeteren. Om dit doel te bereiken, bieden ze vaak extra kortingen aan klanten die deze creditcards gebruiken.

Detailhandelaren die geen merkcreditcards aanbieden, willen klanten mogelijk aanmoedigen om met een ander betaalmiddel te betalen, zoals contant, met geschenkbonnen of loyaliteitspunten. Op deze manier kunnen ze onkosten voor de verwerking van creditcardbetalingen verlagen. Detailhandelaren zouden in dat geval korting kunnen geven aan klanten die deze alternatieve betalingsmethoden gebruiken.

In Microsoft Dynamics 365 Commerce kunnen detailhandelaren een kortingspercentage configureren dat wordt toegepast op de desbetreffende regels als de klant betaalt met de betalingsmethode die de voorkeur heeft. De klant kan zelf bepalen of hij een gedeeltelijke of volledige betaling wil doen, en in Commerce wordt het juiste kortingsbedrag vastgesteld. De korting wordt altijd gegeven op het bedrag exclusief btw van de betreffende artikelen.

Kortingen op basis van een betalingsmethode concurreren niet met kortingen op basis van artikelen, zoals periodieke of handmatige kortingen. Deze worden altijd samengesteld na de artikelkortingen. Dus zelfs als een exclusieve periodieke korting op een artikel wordt toegepast, wordt de korting op basis van de betalingsmethode boven op de exclusieve periodieke korting toegepast. En als er een drempelkorting wordt toegepast op de transactie en de korting op basis van de betalingsmethode het totaal doet afnemen tot onder de drempelwaarde, wordt de drempelkorting toch toegepast op de transactie.

Ook al verminderen kortingen op basis van betalingsmethode het subtotaal, dit heeft geen invloed op automatische kosten die op de transactie worden toegepast. Als de leveringskosten bijvoorbeeld als $ 5 zijn omdat het subtotaal hoger is dan $ 100, en de korting op basis van betalingsmethode het bedrag vermindert tot minder dan $ 100, dan zijn de leveringskosten voor de order nog steeds $ 5.


> [!NOTE]
> Kortingen op basis van betalingsmethode worden evenredig verdeeld over de desbetreffende verkoopregels en verminderen het bedrag exclusief btw van de afzonderlijke regels. Als er meerdere kortingen op basis van betalingsmethode voor een betalingsmethode zijn geconfigureerd (bijvoorbeeld contant), wordt alleen de beste korting op basis van betalingsmethode toegepast.

Kortingen op basis van betalingsmethode kunnen alleen worden toegepast op verkoopregels waarvan de prijzen niet zijn vergrendeld. Als er nieuwe verkoopregels aan een order worden toegevoegd, wordt de korting op basis van betalingsmethode alleen tijdens de betaling op de nieuwe verkoopregels toegepast. Tijdens het plaatsen van een klantorder voor ophalen of verzenden wordt de korting op basis van betalingsmethode alleen toegepast op het depositobedrag. Nadat de order is geplaatst, tijdens de uitvoering, zijn de prijzen van de verkoopregels vergrendeld. Daarom wordt er geen korting op basis van betalingsmethode toegepast op een saldo dat is betaald tijdens het ophalen of is geautoriseerd tijdens de verzending. De korting op basis van betalingsmethode kan alleen worden toegepast op het gehele bedrag van een klantorder als de detailhandelaar het hele bedrag als deposito int terwijl de order wordt geplaatst.

> [!IMPORTANT]
> In Commerce zijn kortingen op basis van betalingsmethode momenteel beperkt tot twee betalingstypen: creditcards en contante betaling.

## <a name="pos-user-experience"></a>POS-gebruikerservaring

Als de korting op basis van betalingsmethode voor contante betaling is ingesteld en de kassamedewerker op het verkooppunt (POS) een knop selecteert die is toegewezen aan de bewerking Contante betaling, wordt de korting op basis van betalingsmethode automatisch toegepast op de transactie. Het verlaagde bedrag wordt vervolgens weergegeven als het saldo. Als de kassamedewerker echter de knop **Vorige** in het betalingsscherm selecteert, wordt de korting verwijderd en wordt het oorspronkelijke bedrag in het transactiescherm weergegeven. De korting op basis van betalingsmethode wordt verwijderd als de betalingsregel ongeldig wordt gemaakt.

Voor creditcardbetalingen kunnen detailhandelaren de korting op basis van betalingsmethode instellen voor een of meer typen creditcards. Het systeem kan echter niet controleren welk type creditcard wordt gebruikt, tenzij de kaart is geautoriseerd. Als de korting wordt toegepast na autorisatie, geldt de betalingsautorisatie voor een groter bedrag, maar wordt er een lager bedrag vastgelegd.

Om een dergelijke situatie te voorkomen, ziet de kassamedewerker wanneer een klant met een creditcard betaalt, een dialoogvenster met een overzicht van creditcards die de klant extra besparingen geven. De kassamedewerker kan de klant vervolgens vragen of de klant een van de voorkeurskaarten wil gebruiken om meer korting te krijgen. Als de kassamedewerker een voorkeurskaart gebruikt, wordt de korting op basis van betalingsmethode op de transactie toegepast en wordt het verlaagde bedrag in het betalingsvenster weergegeven. De autorisatie geldt dan voor het verlaagde bedrag. Als de klant een andere kaart invoert dan de kaart die de kassamedewerker heeft geselecteerd, wordt een foutbericht weergegeven en wordt de autorisatie ongeldig gemaakt.


## <a name="call-center-user-experience"></a>Gebruikerservaring van callcenter

Wanneer de gebruiker tijdens een order via een callcenter de optie **Voltooien** selecteert, wordt het scherm **Totalen** weergegeven. In eerste instantie bevatten de totalen in dit scherm geen kortingen op basis van betalingsmethode omdat de betalingsmethode nog niet is geselecteerd. Als de gebruiker in het scherm **Betaling toevoegen** de betalingsmethode selecteert waarvoor de korting op basis van betalingsmethode is geconfigureerd, wordt het betalingsbedrag automatisch aangepast, zodat dit het kortingsbedrag weerspiegelt. Net als de klant bij het POS kan de callcenterklant besluiten om de volledige of een gedeeltelijke betaling te doen. Op basis van het betaalde bedrag wordt de korting op basis van betalingsmethode op de verkooporder toegepast.

> [!NOTE]
> Er wordt geen kaartvalidatie uitgevoerd voor callcenterorders. Als de callcentergebruiker bijvoorbeeld de Visa-creditcard selecteert, maar de klant zijn Master Card gebruikt, past het systeem de korting nog steeds toe.

## <a name="exclude-items-from-discounts"></a>Artikelen uitsluiten van kortingen

Detailhandelaren kiezen er vaak voor om bepaalde producten, zoals nieuwe artikelen of veelgevraagde artikelen, uit te sluiten van kortingen. Ze willen misschien echter alsnog kortingen op basis van betalingsmethode toepassen. Een detailhandelaar configureert Commerce bijvoorbeeld zo dat kortingen op basis van betalingsmethode of handmatige kortingen niet zijn toegestaan. Als de klant echter betaalt met de voorkeursbetaalmethode, wordt de korting op basis van betalingsmethode alsnog in Commerce toegepast. Om Commerce op deze manier in te stellen, moeten detailhandelaren naar **Productgegevensbeheer > Producten > Vrijgegeven producten** gaan, het artikel selecteren en op het sneltabblad **Commerce** de opties **Alle kortingen verhinderen** en **Kortingen op basis van betalingsmethode verhinderen** op **Nee** en de opties **Kortingen voorkomen** en **Handmatige kortingen verhinderen** op **Ja** instellen.

> [!NOTE]
> Wanneer de configuratie **Alle kortingen voorkomen** is ingesteld op **Ja**, worden er geen kortingen toegepast op het product. Er worden zelfs geen kortingen op basis van betalingsmethode toegepast.


[!INCLUDE[footer-include](../includes/footer-banner.md)]