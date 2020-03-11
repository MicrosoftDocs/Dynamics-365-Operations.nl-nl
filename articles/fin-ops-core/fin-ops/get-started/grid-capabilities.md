---
title: Rastermogelijkheden
description: Dit onderwerp beschrijft diverse krachtige functies van het rasterbesturingselement. De nieuwe rasterfunctie moet zijn ingeschakeld als u toegang tot deze mogelijkheden wilt hebben.
author: jasongre
manager: AnnBe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7136edba828bf97b6e0c8d2a698b884640d680e5
ms.sourcegitcommit: 880f617d1d6e95eccbed762c7ea04398553c2ec0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036260"
---
# <a name="grid-capabilities"></a>Rastermogelijkheden

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Het nieuwe rasterbesturingselement biedt een aantal handige en krachtige functies die kunnen worden gebruikt om de productiviteit van gebruikers te verbeteren, interessantere weergaven van uw gegevens te maken en inzicht te krijgen in uw gegevens. In dit artikel worden de volgende mogelijkheden besproken: 

-  Totalen worden berekend
-  Gegevens groeperen
-  Voor het systeem uit typen
-  Wiskundige expressies evalueren 

## <a name="calculating-totals"></a>Totalen worden berekend
In Finance and Operations-apps kunnen gebruikers totalen weergeven onder aan numerieke kolommen in rasters. Deze totalen worden weergegeven in een voettekstsectie onder in het raster. 

### <a name="showing-the-grid-footer"></a>De rastervoettekst weergeven
Onder aan elk raster in tabelvorm in Finance and Operations-apps bevindt zich een voettekstgebied. In de voettekst kunnen waardevolle gegevens worden weergegeven die betrekking hebben op de gegevens die in het raster worden weergegeven. Hiermee volgen enkele voorbeelden van dergelijke informatie:

- Het aantal geselecteerde rijen in de tabel (wanneer meer dan één record is geselecteerd)
- Eindtotalen onder aan geconfigureerde numerieke kolommen
- Het aantal rijen in de gegevensset 

Deze voettekst is standaard verborgen, maar kan gemakkelijk worden ingeschakeld. Als u de voettekst voor een raster wilt weergeven, klikt u met de rechtermuisknop op een kolomkop in het raster en selecteert u de optie **Voettekst weergeven**. Zodra de voettekst voor een bepaald raster is ingeschakeld, wordt die instelling opgeslagen totdat de gebruiker ervoor kiest de voettekst te verbergen, wat kan worden gedaan door met de rechtermuisknop op een kolomkop te klikken en **Voettekst verbergen** te selecteren.  De plaatsing van de actie **Voettekst tonen/verbergen** wordt naar verwachting in een toekomstige update gewijzigd. 

### <a name="specifying-columns-with-totals"></a>Kolommen met totalen opgeven
Momenteel worden er geen kolommen geconfigureerd om standaard totalen weer te geven. In plaats daarvan wordt dit beschouwd als een eenmalige instelactiviteit, vergelijkbaar met het aanpassen van de breedte van kolommen in rasters. Wanneer u hebt opgegeven dat u totalen voor een kolom wilt weergeven, wordt deze instelling de volgende keer dat u de pagina bezoekt, onthouden.  

Er zijn twee manieren om een kolom te configureren voor het weergeven van totalen: 

- Klik met de rechtermuisknop in de kolom waarvoor u een totaal wilt bekijken en selecteer vervolgens **Deze kolom totaliseren**. Door deze actie worden er drie gebeurtenissen uitgevoerd:

    1. De voettekst wordt weergegeven. 
    2. Uw voorkeur voor het bekijken van een totaal voor deze kolom wordt opgeslagen. 
    3. Er wordt een berekening uitgevoerd van totalen voor deze kolom en alle andere kolommen die u eerder hebt geconfigureerd voor het weergeven van totalen. De tijd die nodig is om een totaal weer te geven, is afhankelijk van de grootte van de gegevensset die u samentelt.

- Nadat de voettekst zichtbaar is geworden, selecteert u **Totaal weergeven** in het voettekstgebied onder aan de kolom waarvoor u een totaal wilt weergeven. Als er geen geconfigureerde kolommen zijn, wordt de knop **Totaal weergeven** beschikbaar voor alle numerieke kolommen. 

    Nadat ten minste één kolom is geconfigureerd voor totalen, zijn de knoppen **Totaal weergeven** alleen beschikbaar bij aanwijzen of focus. Als u **Totaal weergeven** selecteert, wordt uw voorkeur voor het bekijken van totalen in deze kolom opgeslagen, zodat de voorkeur wordt toegepast tijdens toekomstige bezoeken aan de pagina. In de voettekst wordt deze toestand aangegeven via een streepje dat in de kolom wordt weergegeven. (Als de gegevensset klein genoeg is, wordt onmiddellijk een totaal weergegeven.)

Als u een fout maakt en geen totaal meer wilt zien in een bepaalde kolom, klikt u met de rechtermuisknop op de kolom en selecteert u **Totaal verbergen** of selecteert u de knop **Totaal verbergen** in de voettekst in die kolom. Deze voorkeur wordt ook opgeslagen voor toekomstige bezoeken aan de pagina. 

### <a name="calculating-totals"></a>Totalen worden berekend
Wanneer een pagina met de voettekst zichtbaar is en de kolommen al zijn geconfigureerd voor totalen, worden de totalen al dan niet weergegeven in de voettekst. Het gedrag is afhankelijk van de grootte van de gegevensset op de pagina. Als de gegevensset voldoende klein is, worden de totalen automatisch weergegeven, samen met het aantal rijen in de gegevensset. Als er streepjes in de voettekst staan onder de kolommen die u voor de totalen hebt geconfigureerd, is de gegevensset te groot voor het systeem om totalen direct weer te geven en is er een expliciete actie nodig om de totalen te berekenen. Klik hiervoor op de knop **Berekenen** in de voettekst of klik met de rechtermuisknop op een kolom waarvoor u een totaal wilt berekenen en selecteer **Deze kolom totaliseren**.  

Als de berekening te lang duurt, kunt u de bewerking annuleren door de knop **Annuleren** te selecteren. Soms is de gegevensset echter te groot voor het berekenen van totalen (een limiet die is ingesteld door uw organisatie) en wordt u in plaats hiervan op de hoogte gesteld om uw gegevens te filteren.

Totalen worden automatisch bijgewerkt wanneer u rijen bijwerkt, verwijdert of maakt in de gegevensset.  

## <a name="grouping-data"></a>Gegevens groeperen
Zakelijke gebruikers moeten vaak ad hoc gegevensanalyse uitvoeren. U kunt dit doen door gegevens te exporteren naar Microsoft Excel en draaitabellen te gebruiken, maar met de functie **Groepering** in tabelrasters kunnen gebruikers hun gegevens op interessante manieren ordenen in Finance and Operations-apps. Aangezien deze functie de functie **Totalen** uitbreidt, kunt u met **Groepering** ook duidelijke inzichten krijgen in de gegevens door subtotalen op te geven op groepsniveau.

Als u deze functie wilt gebruiken, klikt u met de rechtermuisknop op de kolom waarop u wilt groeperen en selecteert u **Groeperen op deze kolom**. Met deze actie sorteert u de gegevens op de geselecteerde kolom, voegt u een nieuwe Groeperen op-kolom toe aan het begin van het raster en voegt u 'koptekstrijen' toe aan het begin van elke groep. Deze koptekstrijen bevatten de volgende informatie over elke groep: 
-  Gegevenswaarde voor de groep 
-  Kolomlabel (Deze informatie wordt vooral nuttig wanneer meerdere groeperingsniveaus worden ondersteund.)
-  Aantal gegevensrijen in deze groep
-  Subtotalen voor alle kolommen die zijn geconfigureerd voor weergave van totalen

Als [Opgeslagen weergaven](saved-views.md) is ingeschakeld, kan deze groepering worden opgeslagen als onderdeel van een weergave voor snelle toegang, de volgende keer dat u de pagina bezoekt.  

Als u **Groeperen op deze kolom** selecteert voor een andere kolom, wordt de oorspronkelijke groepering vervangen omdat er slechts één groeperingsniveau wordt ondersteund in versie 10.0.9 met Platform update 33.

Als u het groeperen in een raster ongedaan wilt maken, klikt u met de rechtermuisknop op de groepeerkolom en selecteert u **Groepering opheffen**.  


## <a name="evaluating-math-expressions"></a>Wiskundige expressies evalueren
Ter bevordering van de productiviteit kunnen gebruikers wiskundige formules invoeren in numerieke cellen in een raster. Zij hoeven de berekening niet uit te voeren in een app buiten het systeem. Als u bijvoorbeeld **= 15\*4** invoert en vervolgens op de **tabtoets** drukt om het veld te verlaten, wordt de expressie geëvalueerd en wordt de waarde **60** opgeslagen voor het veld.

Als u wilt dat het systeem een waarde herkent als een expressie, start u de waarde met het gelijkteken (**=**). Zie [Ondersteunde wiskundige symbolen](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols)voor meer informatie over de ondersteunde operators en syntaxis.  
