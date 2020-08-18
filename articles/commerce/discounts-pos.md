---
title: Kortingen weergeven in POS
description: In dit onderwerp wordt uitgelegd hoe Microsoft Dynamics 365 Commerce verkoopmedewerkers helpt met informatie over promoties en hoe deze kunnen worden gebruikt voor meerverkoop/bijverkoop.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 7531e250580019a1e9892d22fc7761770227c61f
ms.sourcegitcommit: db1a8ffcaebc2896e8f528d7807c54f8597f450e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/29/2020
ms.locfileid: "3638177"
---
# <a name="show-discounts-in-pos"></a>Kortingen weergeven in POS

[!include [banner](includes/banner.md)]

Promoties spelen een belangrijke rol bij het motiveren van klanten die inkoopbeslissingen nemen. Zo kunnen feestdagen bijvoorbeeld het hoogste aantal verkopen voor detailhandelaren genereren, omdat de gehele markt overstroomt van aantrekkelijke acties en kortingen. Als de winkelmedewerkers weten wat de beschikbare promoties zijn, kunnen ze eenvoudig profiteren van deze acties om meer artikelen te verkopen. In dit onderwerp wordt uitgelegd hoe Microsoft Dynamics 365 Commerce verkoopmedewerkers helpt met informatie over promoties en hoe deze kunnen worden gebruikt voor meerverkoop/bijverkoop.

## <a name="learn-about-store-discounts"></a>Meer informatie over winkelKortingen

Commerce bevat een bewerking met de naam "Alle kortingen weergeven". Met deze bewerking worden alle kortingen weergegeven die momenteel van toepassing zijn in een winkel. De bewerking Alle kortingen weergeven kan worden toegewezen aan een knop op het verkooppunt (POS). Deze knop kan worden toegevoegd aan de **Welkomstpagina** of de **Transactiepagina**. In de volgende afbeelding ziet u een voorbeeld van de geopende pagina **Alle kortingen**.

![Pagina Alle kortingen](./media/View_all_discounts.png "Pagina Alle kortingen")

Voor het weergeven van kortingen wordt gezocht naar alle kortingen die overeenkomen met een of meer van de volgende voorwaarden:

- De prijsgroep van de korting komt overeen met de prijsgroep van de winkel.
- De prijsgroep van de korting wordt toegewezen aan een aansluiting of een loyaliteitsprogramma.
- De prijsgroep van de korting wordt toegewezen aan een catalogus die aan de winkel is gekoppeld.

Op de pagina **Alle kortingen** worden slechts enkele kortingen weergegeven, omdat detailhandelaren doorgaans duizenden coupons en bijbehorende kortingen voor unieke klanten maken. Deze pagina is niet bedoeld voor de weergave van klantspecifieke kortingen. Op coupon gebaseerde kortingen worden alleen weergegeven als de optie **Toepassen zonder couponcode** is ingeschakeld in elke coupon. In dat geval kunnen kassiers de waardebon toepassen zonder een waardeboncode of streepjescode in te voeren of te scannen.

Wanneer de optie **Toepassen zonder couponcode** is ingeschakeld, zijn er verschillende scenario's beschikbaar. Kassiers kunnen bijvoorbeeld extra kortingen aan klanten geven om ze tevreden te stellen of vanwege defecte producten. Afgedrukte couponcodes of streepjescodes hoeven niet te worden gedistribueerd naar kassiers. In plaats daarvan kunnen kassiers de knop **Coupon toepassen** selecteren. De coupon wordt vervolgens automatisch toegepast op de transactie. Als er meerdere coupons voor een couponkopregel zijn, selecteert het systeem automatisch de eerste actieve coupon voor de transactie.

Op de pagina **Alle kortingen** kunnen verkoopmedewerkers ook kortingen op trefwoorden zoeken. De zoekactie naar trefwoorden betreft de velden die de kortingsnaam en kortingsomschrijving bevatten. Verkoopmedewerkers kunnen ook op kortingen filteren op basis van of een couponcode vereist is voor een korting.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Meerverkoop/bijverkoop vanwege kortingen

Meerregelkortingen, zoals kwantumkortingen, combinatiekortingen en drempelkortingen, zijn een prima manier om klanten te motiveren om meer producten te kopen om grotere kortingen te krijgen. Daarom vergroten ze ook de omvang van de winkelwagen en de winkelopbrengst van de klant. Deze kortingen kunnen worden gepubliceerd op websites voor e-commerce, sociale media en banners in de winkel.

Maar zelfs wanneer al deze reclamemethoden worden gebruikt, kunnen klanten de kans missen om gebruik te maken van promoties. Om te kunnen zien welke acties van toepassing zijn op een geselecteerde regel of zelfs op de hele winkelwagen, kunnen detailhandelaren de knop voor de bewerking **Beschikbare kortingen weergeven** toevoegen aan het knoppenraster op de pagina **Transactie**. Hierdoor kan een verkoopmedewerker een transactieregel selecteren en vervolgens de knop selecteren om alle beschikbare kortingen voor de geselecteerde regel weer te geven. De verkoopmedewerker kan ook een ander tabblad selecteren om kortingen weer te geven die van toepassing zijn op de gehele transactie. Het is belangrijk te weten dat **Beschikbare kortingen weergeven** de kortingen die al op de verkoopregel zijn toegepast niet weergeeft omdat de kortingsgegevens al worden weergegeven op de verkoopregel. Het doel van dit scenario is alleen de kortingen weer te geven die nog niet zijn toegepast. De uitzondering hierop zijn de kortingen die worden toegepast op basis van een coupon die is gemarkeerd als 'Toepassen zonder couponcode'. Hierdoor kan de verkooppartner eenvoudig de coupon verwijderen die zij hebben toegepast.

Op de pagina **Alle kortingen** worden alleen kortingen weergegeven die niet concurreren met de vereffende kortingen. Dit zorgt ervoor dat, als een verkoopmedewerker een klant op de hoogte stelt over een korting, en de klant de vereiste actie kiest (de klant koopt bijvoorbeeld één artikel meer om 10 procent te krijgen), wordt de korting toegepast op de transactie. Op coupon gebaseerde kortingen worden alleen weergegeven als de optie **Toepassen zonder couponcode** is ingeschakeld.

In een eenvoudig scenario waarin alle kortingen dezelfde prioriteit hebben, is de gelijktijdigheidsmodus voor korting **Samengesteld** en wordt het gelijktijdigheidsbeheer voor de korting ingesteld op **Beste prijs en samengestelde prijs binnen prioriteit, nooit voor verschillende prioriteiten**. Op de pagina **Alle kortingen** worden alle beschikbare kortingen voor een product weergegeven, omdat alle kortingen worden samengesteld en niet met elkaar concurreren.

De volgende illustraties tonen de logica die bepaalt welke kortingen worden weergegeven in geavanceerde scenario's, zoals een scenario waarbij de gelijktijdigheidsmodus voor korting de **Beste prijs** of **Exclusief** is en twee of meer prioriteiten worden gebruikt. In deze scenario's worden de kortingen die worden weergegeven, verder beïnvloed op basis van de vraag of het gelijktijdigheidsbeheer voor de korting is ingesteld op **Beste prijs en samengestelde prijs binnen prioriteit, nooit voor verschillende prioriteiten** of **Beste prijs binnen de prioriteit, altijd samengesteld op basis van prioriteit**.

In de volgende afbeelding wordt de logica weergegeven die wordt gebruikt wanneer het gelijktijdigheidsbeheer voor de korting is ingesteld op **Beste prijs en samengesteld binnen de prioriteit, altijd samengesteld voor alle prioriteiten**.

![Logica voor de beste prijs en samengesteld binnen de prioriteit, nooit samengesteld voor alle prioriteiten](./media/Model_1.png "Logica voor de beste prijs en samengesteld binnen de prioriteit, nooit samengesteld voor alle prioriteiten").

In de volgende afbeelding wordt de logica weergegeven die wordt gebruikt wanneer het gelijktijdigheidsbeheer voor de korting is ingesteld op **Beste prijs alleen binnen de prioriteit, altijd samengesteld op basis van prioriteit**.

![Logica voor de beste prijs alleen binnen de prioriteit, altijd samengesteld op basis van prioriteit](./media/Model_2.png "Logica voor de beste prijs alleen binnen de prioriteit, altijd samengesteld op basis van prioriteit").
