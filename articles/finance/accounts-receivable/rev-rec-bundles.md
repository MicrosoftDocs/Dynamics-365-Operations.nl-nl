---
title: Bundels voor opbrengsttoerekening
description: In dit onderwerp wordt de bundelfunctie beschreven die is opgenomen in de functie voor opbrengsttoerekening in Klanten. Een bundel bestaat uit een hoofdartikel en meerdere componentartikelen.
author: kweekley
manager: aolson
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: cf4d03c1a697259899c419ce084b35f4eddf13fe
ms.sourcegitcommit: bd53794cb94f8c1ce29a7d6102119a0975f155e3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142294"
---
# <a name="revenue-recognition-bundles"></a>Bundels voor opbrengsttoerekening

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de bundelfunctie beschreven die is opgenomen in de functie voor opbrengsttoerekening in Klanten. Een bundel bestaat uit een hoofdartikel en meerdere componentartikelen. Het hoofdartikel wordt in een verkooporder ingevoerd, zodat de orderinvoer efficiënter wordt. Het wordt vervolgens echter geëxplodeerd naar de componentartikelen. Interne documenten, zoals de pakbon, bevatten een lijst met de componentartikelen. In externe documenten wordt echter alleen het hoofdartikel weergegeven.

> [!NOTE]
> Microsoft Dynamics 365 Commerce-kanalen, zoals online, POS (Point of Sale) en callcenters, bieden geen ondersteuning voor opbrengsttoerekening (inclusief de bundelfunctionaliteit). Dit geldt ook voor de oplossing Prospect naar contant geld voor Dynamics 365 Supply Chain Management en Dynamics 365 Sales. Artikelen die zijn geconfigureerd voor het gebruik van opbrengsttoerekening mogen niet worden toegevoegd aan orders of transacties die zijn gemaakt in Commerce-kanalen of in de oplossing Prospect naar contant geld.

Als u bundels wilt instellen, moet u de configuratiesleutels voor opbrengsttoerekening invoeren. U kunt echter ook bundels gebruiken als geen opbrengsttoerekening is ingesteld. Andersom kunt u opbrengsttoerekening ook gebruiken als er geen bundels zijn ingesteld. Als opbrengsttoerekening is ingesteld, bepalen de componentartikelen welke opbrengstprijs en welk opbrengstschema bij het factureren van een verkooporder moeten worden gebruikt voor opbrengsttoerekening of -uitstel.

U kunt bundels instellen via de stuklijstfunctionaliteit. Zie [Instellingen opbrengsttoerekening](revenue-recognition-setup.md) voor informatie over het instellen van een bundelartikel. Als het hoofdartikel is gemarkeerd als bundel, wordt het anders behandeld dan andere stuklijstartikelen. Hieronder volgt een overzicht van de verschillen:

- U kunt bundels exploderen door verkooporders te bevestigen. U doet dit door **Verkooporder bevestigen** te selecteren op het tabblad **Verkopen** in het actievenster op de verkooporderpagina. U mag bundelartikelen nooit exploderen door **Stuklijstregel** te selecteren onder **Exploderen** in het menu **Verkooporderregel** op het sneltabblad **Verkooporderregels**. Anders wordt het artikel behandeld als een stuklijst en niet als bundel.
- Een verkooporder die een bundelartikel bevat, moet worden bevestigd voordat de pakbon of factuur wordt gemaakt.
- Wanneer een bundel wordt geëxplodeerd door middel van verkooporderbevestiging, wordt het hoofdartikel geannuleerd en worden de eenheidsprijs en kortingen toegewezen aan de componentartikelen van de bundel.
- Het totaal van de componentartikelen moet altijd gelijk zijn aan de prijs van het hoofdartikel. Daarom gelden er beperkingen ten aanzien van de velden die kunnen worden bijgewerkt of gewijzigd voor componentartikelen. U kunt de eenheidsprijs bijvoorbeeld niet handmatig wijzigen. U kunt de eenheidsprijs ook niet indirect wijzigen door een nieuwe prijsovereenkomst van kracht te laten worden. Om te voorkomen dat een nieuwe prijsovereenkomst wordt gesloten, kunnen voorraaddimensies voor de componentartikelen niet worden gewijzigd.
- Wanneer een extern gericht document, zoals de verkooporderbevestiging of factuur, wordt afgedrukt, wordt het hoofdartikel afgedrukt, niet de componentartikelen.

## <a name="bundles-on-sales-orders"></a>Bundels in verkooporders

Voor het demobedrijf USMF zijn de volgende bundelinstellingen geconfigureerd. Alle instellingen voor opbrengsttoerekening, zoals de instelling van opbrengstschema's, zijn verwijderd uit de artikelen die in dit scenario zijn opgenomen.

**Hoofdartikel:** Laptopbundel

- **Componentartikel:** een hoeveelheid van 1 van artikel 1000
- **Componentartikel:** een hoeveelheid van 1 van artikel S0021
- **Componentartikel:** een hoeveelheid van 1 van artikel Ondersteuning

De *basisverkoopprijs* van de componentartikelen is een essentieel onderdeel van de instellingen van de componenten. De basisverkoopprijs wordt gedefinieerd op het sneltabblad **Verkopen** van een artikel. Deze prijs wordt gebruikt om de toewijzingsfactor te berekenen wanneer de eenheidsprijs van het hoofdartikel wordt toegewezen aan de componentartikelen. De verkoopprijzen in de handelsovereenkomst worden nooit gebruikt voor dit doel.

Voor de componentartikelen worden de volgende basisverkoopprijzen gedefinieerd:

- **1000:** $ 1900,00
- **S0021:** $ 150,00
- **Ondersteuning:** $ 500,00

Er wordt een verkooporder ingevoerd voor de klant US-004, Cave Wholesales. Er wordt alleen een regel ingevoerd voor het bundelartikel Laptop. De standaardeenheidsprijs voor de bovenliggende regel kan van een groot aantal plekken worden overgenomen, zoals de handelsovereenkomst of de basisverkoopprijs. In dit voorbeeld is $ 2300 handmatig ingevoerd als de eenheidsprijs.

[![Het bundelartikel Laptop in een verkooporder](./media/bundle-01.png)](./media/bundle-01.png)

Omdat de verkooporder een bundel bevat, moet deze worden bevestigd. In het bevestigingsvenster worden de componenten van de bundel weergegeven.

[![Het dialoogvenster Verkooporder bevestigen waarin de componentartikelen worden weergegeven](./media/bundle-02.png)](./media/bundle-02.png)

In het afgedrukte bevestigingsrapport wordt echter alleen het hoofdartikel van de bundel weergegeven omdat dat rapport het extern gerichte, voor de klant bestemde document is.

[![Bevestigingsrapport waarin alleen het hoofdartikel wordt weergegeven](./media/bundle-03.png)](./media/bundle-03.png)

Als de verkooporder is bevestigd, wordt het hoofdartikel nog steeds weergegeven in de verkooporder, maar is de status gewijzigd in **Geannuleerd**. Daarnaast wordt het nettobedrag bijgehouden in het veld **Nettobedrag bundel**. Dit bedrag is vereist om de factuur af te drukken omdat de factuur het hoofdartikel bevat en niet de componentartikelen.

Het totaal van de componentartikelen moet gelijk zijn aan de waarde voor **Nettobedrag bundel** van het hoofdartikel omdat die waarde het bedrag is dat op de afgedrukte factuur voor de klant staat. Om er zeker van te zijn dat de factuur overeenkomt met de bedragen die naar het grootboek worden geboekt, kunnen de componentartikelen slechts beperkt worden bewerkt. De locatie en het magazijn kunnen bijvoorbeeld niet worden gewijzigd omdat deze wijzigingen tot een prijswijziging kunnen leiden op basis van een handelsovereenkomst.

De eenheidsprijs van de regel voor het hoofdartikel wordt op de volgende manier toegewezen aan de componenten:

**Totale basisverkoopprijzen uit componenten:** $ 1900 + $ 500 + $ 150 = $ 2550

- **Component 1:** $ 2300 × (1900 ÷ 2550) = $ 1713,73
- **Component 2:** $ 2300 × (500 ÷ 2550) = $ 450,98
- **Component 3:** $ 2300 × (150 ÷ 2550) = $ 135,29

Het totaal van de onderdelen moet gelijk zijn aan $ 2300 en dat is ook zo ($ 1713,73 + $ 450,98 + $ 135,29 = $ 2300).

Als voor alle componentartikelen wijzigingen vereist zijn, kan het hoofdartikel worden verwijderd. In dit geval worden de componentartikelen ook verwijderd. Het hoofdartikel kan vervolgens opnieuw worden toegevoegd en de vereiste bewerkingen kunnen worden uitgevoerd voordat de verkooporder wordt bevestigd.

[![Bundelartikel waarvoor wijzigingen in de componentartikelen zijn aangebracht](./media/bundle-04.png)](./media/bundle-04.png)

Wanneer de verkooporder wordt verzameld en verpakt, bevatten de documenten alleen de componenten van de bundel. De pakbon en factuur moeten een volledige bundel bevatten. Anders kunnen ze niet worden geboekt. In het dialoogvenster worden bijvoorbeeld drie componentartikelen weergegeven. Als u een van deze artikelen probeert te verwijderen, ontvangt u een foutbericht waarin wordt aangegeven dat alle producten in de bundel moeten worden verzonden voordat ze kunnen worden gefactureerd.

Een bundel moet als volledige bundel worden verzonden en gefactureerd. Als u de hoeveelheid van artikel 1000 wijzigt in 4, maar de hoeveelheid van 5 voor de andere componentartikelen ongewijzigd laat, kunnen de pakbon en factuur bijvoorbeeld niet worden geboekt.

Een gedeeltelijke hoeveelheid kan alleen worden verzonden en gefactureerd als de hoeveelheid wordt verminderd voor alle componenten van de bundel. Stel dat een hoeveelheid van 5 van het bundelartikel Laptop wordt ingevoerd in een verkooporder. Nadat de verkooporder is bevestigd, worden de drie componentartikelen in de verkooporder weergegeven en is de hoeveelheid van elk 5. Tijdens verzending en facturering wordt de hoeveelheid standaard ingesteld op 5 voor elke component. U kunt de hoeveelheid echter voor alle drie de componentartikelen instellen op 3. In dit geval worden drie volledige bundels verzonden en gefactureerd. De overige twee bundelartikelen (een hoeveelheid van twee van elk van de drie componentartikelen) kunnen later worden verzonden en gefactureerd.

De laatste stap is het factureren van de verkooporder. Tijdens het factureren worden de componentartikelen weergegeven in het factuurvenster.

[![Het factuurvenster waarin de componentartikelen worden weergegeven](./media/bundle-06.png)](./media/bundle-06.png)

Op de afgedrukte factuur wordt echter alleen het hoofdartikel weergegeven.
 
[![Afgedrukte factuur waarop alleen het hoofdartikel wordt weergegeven](./media/bundle-07.png)](./media/bundle-07.png)

Het factuurjournaal dat na het boeken wordt gemaakt, bevat geen hoofdartikel uit de bundel omdat dat artikel de status **Geannuleerd** heeft.

[![Factuurjournaal dat niet het hoofdartikel bevat](./media/bundle-08.png)](./media/bundle-08.png)

Het is belangrijk dat het factuurjournaal niet het hoofdartikel uit de bundel bevat omdat de processen die worden uitgevoerd nadat de factuur is geboekt, worden gebaseerd op dat factuurjournaal. Als u een creditnota maakt via het tabblad **Verkopen** in het actievenster, bevat de gemaakte creditnota bijvoorbeeld wel de componentartikelen, maar niet het hoofdartikel.

[![Creditnota die wel de componentartikelen bevat, maar niet het hoofdartikel](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]