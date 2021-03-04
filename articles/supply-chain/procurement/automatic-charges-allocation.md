---
title: Automatische toewijzing van toeslagen
description: Met de toeslagenfunctie in Microsoft Dynamics 365 Supply Chain Management kunt u automatisch toeslagen toewijzen aan inkooporders of verkooporders.
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 818affc7591577b69309928eb9b0e71130884cec
ms.sourcegitcommit: 66ecc6cb36ef4f723c77e09d6a33f9c42f8fa392
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425743"
---
# <a name="automatic-allocation-of-charges"></a>Automatische toewijzing van toeslagen

[!include [banner](../includes/banner.md)]

Op basis van de klant met wie u werkt of het artikel dat u verkoopt, wilt u mogelijk specifieke extra toeslagen toepassen. Met de functie voor *toeslagen* in Microsoft Dynamics 365 Supply Chain Management kunt u automatisch toeslagen toewijzen aan inkooporders of verkooporders.

Automatische toeslagen worden automatisch toegepast wanneer u een verkooporder of inkooporder maakt. U kunt automatische toeslagen definiëren voor specifieke leveranciers, klanten of artikelen, groepen leveranciers of artikelen. U kunt ook automatische toeslagen definiëren die voor alle leveranciers, klanten of artikelen gelden.

## <a name="set-up-charges-codes"></a>Codes voor toeslagen instellen

Als u toeslagen wilt toewijzen, moet u eerst toeslagcodes definiëren.

1. Volg één van deze stappen:

    - Voor inkooporders: ga naar **Leveranciers \> Instelling van toeslagen \> Toeslagcode**.
    - Voor verkooporders: ga naar **Klanten \> Instelling van toeslagen \> Toeslagcode**.

1. Selecteer in het actievenster **Nieuw** om een toeslagcode te maken.
1. Stel in de koptekst van de nieuwe record de volgende velden in:

    - **Toeslagcode**: voer een code in voor de toeslagen.
    - **Beschrijving**: voer een beschrijving van de toeslagen in.
    - **Btw-groep voor artikel**: selecteer een btw-groep voor artikel, indien van toepassing.
    - **Evenredig**: stel deze optie in op *Ja* als u de toeslagen naar rato wilt verdelen. Deze optie is alleen beschikbaar voor verkooporders.
    - **Maximumbedrag**: voer het maximumbedrag in dat is toegestaan voor de toeslagcode. Dit veld wordt gebruikt voor het valideren van toeslagen voor leveranciersfacturen. Het is alleen beschikbaar voor inkooporders.

        > [!NOTE]
        > Als u de functionaliteit voor het valideren van toeslagen voor inkooporders wilt inschakelen, gaat u naar **Leveranciers \> Instellingen \> Paramaters van module Leveranciers**. Stel op het sneltabblad **Factuurvalidatie** in de sectie **Factuurvalidatie** de optie **Factuurvereffeningsvalidatie inschakelen** in op *Ja*.

1. Het sneltabblad **Boeking** bevat de secties **Debet** en **Credit**. Stel de volgende velden in, afhankelijk van het grootboek waarnaar u de toeslagen wilt boeken:

    - **Type**: selecteer het type rekening waarnaar u wilt boeken (*Grootboek*, *Klant* of *Artikel*).
    - **Boeking**: selecteer het type boekingen dat u wilt maken (zoals *Kosten tussenpersoon* of *Vereffening van klant*).
    - **Rekening**: selecteer de rekening waarnaar u de toeslag wilt boeken.

1. Selecteer **Opslaan** in het actievenster.

## <a name="create-charge-groups"></a>Toeslaggroepen maken

Met toeslaggroepen worden automatisch specifieke toeslagen aan een groep klanten of leveranciers toegewezen. In de volgende subsecties wordt beschreven hoe u deze toeslaggroepen kunt maken en toewijzen.

### <a name="charge-groups-for-purchase-orders"></a>Toeslaggroepen voor inkooporders

Voer de volgende stappen uit om toeslaggroepen voor inkooporders te maken.

1. Ga naar **Leveranciers \> Instelling van toeslagen \> Toeslaggroep van leveranciers**.
1. Selecteer in het actievenster **Nieuw** om een rij toe te voegen aan het raster en stel vervolgens de volgende velden in:

    - **Toeslaggroep**: voer de naam van de toeslaggroep in.
    - **Beschrijving**: voer een beschrijving van de toeslaggroep in.

1. Selecteer **Opslaan** in het actievenster.
1. Ga naar **Leveranciers \> Leveranciers \> Alle leveranciers** en open een bestaande leverancier of maak een nieuwe leverancier.
1. Stel op het sneltabblad **Standaardwaarden inkooporder** in de sectie **Inkooporder** het veld **Toeslaggroep** in op de toeslaggroep die u zojuist hebt gemaakt.

### <a name="charge-groups-for-sales-orders"></a>Toeslaggroepen voor verkooporders

Voer de volgende stappen uit om toeslaggroepen voor verkooporders te maken.

1. Ga naar **Klanten \> Instelling van toeslagen \> Toeslaggroepen van klanten**.
1. Selecteer in het actievenster **Nieuw** om een rij toe te voegen aan het raster en stel vervolgens de volgende velden in:

    - **Toeslaggroep**: voer de naam van de toeslaggroep in.
    - **Beschrijving**: voer een beschrijving van de toeslaggroep in.

1. Selecteer **Opslaan** in het actievenster.
1. Ga naar **Klanten \> Klanten \> Alle klanten** en open een bestaande klant of maak een nieuwe klant.
1. Stel op het sneltabblad **Standaardwaarden inkooporder** in de sectie **Verkooporder** het veld **Toeslaggroep** in op de toeslaggroep die u zojuist hebt gemaakt.

## <a name="define-auto-charges"></a>Automatische toeslagen definiëren

Nadat uw toeslagcodes zijn ingesteld, voert u de volgende stappen uit om de automatische toeslagen te definiëren.

1. Volg één van deze stappen:

    - Voor inkooporders: ga naar **Inkoopbeheer \> Instellingen \> Toeslagen \> Automatische toeslagen**.
    - Voor verkooporders: ga naar **Klanten \> Instellingen \> Instelling van toeslagen \> Automatische toeslagen**.

1. Selecteer in het lijstvenster in het veld **Niveau** het niveau waarop uw automatische toeslagen van toepassing zijn:

    - *Hoofd*: pas toeslagen toe op de orderkoptekst.
    - *Regel*: pas toeslagen toe op de orderregels.

1. Selecteer een bestaande automatische toeslag om deze te bewerken of selecteer **Nieuw** om een nieuwe automatische toeslag te definiëren.
1. Selecteer in de lijst **Rekeningcode** een van de volgende waarden om het bereik van rekeningen op te geven dat wordt beïnvloed:

    - *Tabel*: wijs toeslagen aan een bepaalde klant of leverancier toe.
    - *Groep*: wijs toeslagen aan een groep diverse toeslagen toe.
    - *Alle*: wijs toeslagen aan alle klanten of leveranciers toe.

1. Selecteer in het veld **Klantrelatie** of **Leveranciersrelatie** een specifieke klant of leverancier als u het veld **Rekeningcode** op *Tabel* instelt. Als u het veld **Rekeningcode** instelt op *Groep*, selecteert u een toeslaggroep voor klant of leverancier.
1. Selecteer in het veld **Artikelcode** een van de volgende waarden om het bereik van artikelen op te geven dat wordt beïnvloed. Alleen wanneer u automatische toeslagen op het regelniveau definieert, kunt u een artikelcode selecteren.

    - *Tabel*: wijs toeslagen aan een bepaald artikel toe.
    - *Groep*: wijs toeslagen toe aan een toeslaggroep van een artikel.
    - *Alle*: wijs toeslagen toe aan alle artikelen.

1. Selecteer in het veld **Artikelrelatie** een specifiek artikel als u het veld **Artikelcode** hebt ingesteld op *Tabel*. Als u het veld **Artikelcode** hebt ingesteld op *Groep*, selecteert u een toeslaggroep voor artikelen.
1. **Alleen voor verkooporders**: selecteer in het veld **Code van leveringsmethode** een van de volgende waarden om het bereik van de leveringsmethoden op te geven dat wordt beïnvloed:

    - *Tabel*: wijs toeslagen aan een bepaalde leveringsmethode toe.
    - *Groep*: wijs toeslagen aan een groep leveringsmethoden toe.
    - *Alle*: wijs toeslagen aan alle leveringsmethoden toe.

1. **Alleen voor verkooporders**: als u het veld **Code van leveringsmethode** instelt op *Tabel* , moet u een specifieke leveringsmethode selecteren in het veld **Relatie voor leveringsmethode**. Als u **Code van leveringsmethode** instelt op *Groep*, selecteert u een groep leveringsmethoden.
1. Vouw het sneltabblad **Regels** uit om de toeslagen en de toeslagtarieven te definiëren die worden gebruikt wanneer de huidige automatische toeslag wordt toegepast. U kunt de werkbalk op dit sneltabblad gebruiken om zo veel regels toe te voegen als nodig is. Stel voor elke regel de volgende velden in:

    - **Valuta**: selecteer de valuta die moet worden gebruikt om de toeslag te berekenen.
    - **Toeslagcode**: selecteer de code voor de toeslag.
    - **Categorie**: selecteer een van de volgende waarden:

        - *Vast*: de toeslag wordt als een vast bedrag op de regel ingevoerd. Vaste toeslagen kunnen worden gebruikt voor toeslagen zowel in de koptekst als op de orderregels.
        - *Stuks*: de toeslag wordt gebaseerd op de eenheid. Deze toeslagen kunnen alleen op orderregels worden gebruikt. Deze worden weergegeven wanneer u het ordertotaal berekent.
        - *Percentage*: de toeslag wordt als een percentage op de regel ingevoerd. Percentagetoeslagen kunnen worden gebruikt voor toeslagen zowel in de koptekst als op de orderregels.
        - *Intercompany-percentage*: de toeslag wordt ingevoerd als een percentage op de regel voor intercompany-orders. Intercompany-percentagetoeslagen kunnen alleen worden gebruikt op orderregels.
        - *Extern*: de toeslag wordt berekend door een service van derden die is gekoppeld aan een of meer vervoerders.

    - **Waarde van toeslagen**: voer de toeslagwaarde in op basis van de geselecteerde categorie.
    - **Valutacode voor toeslagen**: geef een valuta voor de toeslag op als u een andere valuta wilt gebruiken dan de valuta die u in het veld **Valuta** hebt opgegeven. U kunt alleen een andere valuta gebruiken als het **Debettype** of **Credittype** voor de geselecteerde toeslagcode is ingesteld op *Grootboekrekening* of *Artikel*.
    - **Van-bedrag**: geef een beginbedrag op waarop de automatische toeslag moet worden toegepast. In deze context verwijst het bedrag naar het ordertotaal.
    - **Tot-bedrag**: geef het eindbedrag op waarop de automatische toeslag moet worden toegepast. In deze context verwijst het bedrag naar het ordertotaal.
    - **Btw-groep**: geef een btw-groep op.
    - **Locatie** en **Magazijn**: geef een locatie en magazijn op als toeslagen alleen moeten worden toegepast op een specifieke locatie en specifiek magazijn.
    - **Behouden**: selecteer dit selectievakje om de toeslagtransacties te behouden nadat de facturering is voltooid, zodat de toeslag telkens wordt toegepast wanneer u een nieuwe factuur voor de geselecteerde klantrekening maakt.

1. **Alleen voor verkooporders**: als u gelaagde toeslagen wilt berekenen, raadpleegt u [Gelaagde toeslagen op verkooporders](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) voor informatie.

## <a name="allocate-charges-from-the-header-to-a-line"></a>Toeslagen van de koptekst aan een regel toewijzen

Met de volgende procedure wordt aangegeven hoe u toeslagen op koptekstniveau kunt toewijzen aan een regel. Voordat u deze procedure start, moet u al een toeslag op koptekstniveau hebben van het type *Vast bedrag* en een order waarop deze kosten worden toegepast. Bovendien moet de order al minimaal één regelartikel bevatten.

1. Open de inkooporder of toeslagorder.
1. Voer een van de volgende stappen uit in het actievenster:

    - Voor inkooporders: selecteer op het tabblad **Aankoop** in de groep **Toeslagen** de optie **Toeslagen toewijzen**.
    - Voor verkooporders: selecteer op het tabblad **Verkoop** in de groep **Toeslagen** de optie **Toeslagen toewijzen**.

1. Stel in het dialoogvenster **Toeslagen toewijzen aan orderregels** de volgende velden in:

    - **Toewijzing van toeslagen**: selecteer een van de volgende waarden om op te geven hoe de toeslagen moeten worden toegewezen:

        - *Nettobedrag*: wijs toeslagen toe op basis van elk regelbedrag ten opzichte van het totale nettobedrag.
        - *Hoeveelheid*: wijs toeslagen toe op basis van het aantal eenheden voor elke regel ten opzichte van het totale aantal eenheden.
        - *Per regel*: wijs toeslagen gelijkmatig toe aan het totaal aantal regels.

    - **Toeslagen aan regels toewijzen**: selecteer een waarde om op te geven of toeslagen aan alle regels moeten worden toegewezen, alleen aan positieve regels of alleen aan negatieve regels.
    - **Alles toewijzen**: schakel dit selectievakje in als u toeslagen aan orderregels wilt toewijzen zelfs als de toeslagcode een ander debettype heeft dan *Artikel*.
    - **Ontvangen**: schakel dit selectievakje in als u toeslagen alleen wilt toewijzen aan ontvangen orderregels.
    - **Opgeslagen in voorraad**: schakel dit selectievakje in als u toeslagen alleen wilt toewijzen aan orderregels die op voorraad zijn.
    - **Selecties weergeven en specifieke regels wissen**: schakel dit selectievakje in om specifieke regels van deze toewijzing uit te sluiten. Wanneer u dit selectievakje inschakelt, wordt het raster **Regels kiezen die u wilt uitsluiten van toewijzing** geopend. Dit raster bevat alleen regels die overeenkomen met de criteria die zijn gedefinieerd door de instellingen **Toeslagen aan regels toewijzen** en **Opgeslagen in voorraad**. Als u bijvoorbeeld *Positieve regels* in het veld **Toeslagen aan regels toewijzen** instelt en het selectievakje **Opgeslagen in voorraad** inschakelt, worden alleen regels die zowel positief als op voorraad zijn weergegeven in het raster. Bovendien filtert het raster automatisch alle regels waarvoor de volledige hoeveelheid al is ontvangen. Terwijl het raster is geopend, schakelt u het selectievakje **Opnemen** uit voor elke regel die moet worden uitgesloten van toewijzing. 

        > [!IMPORTANT]
        > Wanneer u werkt met het raster **Regels kiezen die u wilt uitsluiten van toewijzing**, moet u het raster geopend laten totdat u **Toewijzen** selecteert. Als u het raster sluit voordat u **Toewijzen** selecteert, gaan de instellingen in het raster verloren. Daarom worden toeslagen toegewezen op basis van de criteria die u eerder hebt gedefinieerd.

1. Selecteer **Toewijzen** om uw instellingen toe te passen en het dialoogvenster te sluiten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]