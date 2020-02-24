---
title: Rastermogelijkheden
description: Dit onderwerp beschrijft diverse krachtige functies van het rasterbesturingselement. De nieuwe rasterfunctie moet zijn ingeschakeld als u toegang tot deze mogelijkheden wilt hebben.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019711"
---
# <a name="grid-capabilites"></a>Rastermogelijkheden

[!include [banner](../includes/banner.md)]

Het nieuwe rasterbesturingselement biedt een aantal handige en krachtige functies die kunnen worden gebruikt om de productiviteit van gebruikers te verbeteren, interessantere weergaven van uw gegevens te maken en inzicht te krijgen in uw gegevens. In dit artikel worden de volgende mogelijkheden besproken: 

-  Totalen worden berekend
-  Gegevens groeperen
-  Voor het systeem uit typen
-  Wiskundige expressies evalueren 

## <a name="calculating-totals"></a>Totalen worden berekend
In Finance and Operations-apps kunnen gebruikers totalen weergeven onder aan numerieke kolommen in rasters. Deze totalen worden weergegeven in een voettekstsectie onder in het raster. 

### <a name="showing-the-grid-footer"></a>De rastervoettekst weergeven
Elk tabelraster in de Finance and Operations-apps heeft een voettekstgebied onder aan het raster dat waardevolle informatie kan bevatten over de gegevens die worden weergegeven. Deze informatie omvat: 
-  Het aantal geselecteerde rijen in de tabel (wanneer meer dan één record is geselecteerd)
-  Eindtotalen onder aan geconfigureerde numerieke kolommen
-  Het aantal rijen in de gegevensset 

Deze voettekst is standaard verborgen, maar kan gemakkelijk worden ingeschakeld. Als u de voettekst voor een raster wilt weergeven, klikt u met de rechtermuisknop op een kolomkop in het raster en selecteert u de optie **Voettekst weergeven**. Zodra de voettekst voor een bepaald raster is ingeschakeld, wordt die instelling opgeslagen totdat de gebruiker ervoor kiest de voettekst te verbergen, wat kan worden gedaan door met de rechtermuisknop op een kolomkop te klikken en **Voettekst verbergen** te selecteren.  De plaatsing van de actie **Voettekst tonen/verbergen** wordt naar verwachting in een toekomstige update gewijzigd. 

### <a name="specifying-columns-with-totals"></a>Kolommen met totalen opgeven
Momenteel worden er geen kolommen geconfigureerd om standaard totalen weer te geven. In plaats daarvan wordt dit beschouwd als een eenmalige instelactiviteit, vergelijkbaar met het aanpassen van de breedte van kolommen in rasters. Wanneer u hebt opgegeven dat u totalen voor een kolom wilt weergeven, wordt deze instelling de volgende keer dat u de pagina bezoekt, onthouden.  

Er zijn twee manieren om een kolom te configureren voor het weergeven van totalen: 
1.  Klik met de rechtermuisknop op de kolom waarvoor u een totaal wilt bekijken en selecteer **Deze kolom totaliseren**. Met deze actie worden drie dingen gedaan. Eerst wordt de voettekst zichtbaar gemaakt. Ten tweede wordt uw voorkeur opgeslagen voor het bekijken van een totaal voor deze kolom. Ten derde start deze actie een berekening van totalen voor deze kolom en alle andere die u eerder hebt geconfigureerd om totalen weer te geven. De tijd die nodig is om een totaal weer te geven, is rechtstreeks gerelateerd aan de grootte van de gegevensset die u optelt.  

2.  Zodra de voettekst is weergegeven, kunt u op de knop **Totaal weergeven** klikken in het gebied voettekst onder aan de kolom waarvoor u een totaal wilt bekijken. Als er geen geconfigureerde kolommen zijn, wordt de knop **Totaal weergeven** voor alle numerieke kolommen weergegeven. Als er ten minste één kolom is geconfigureerd voor totalen, zijn de knoppen **Totaal weergeven** alleen beschikbaar bij aanwijzen of focus. Met deze actie wordt uw voorkeur voor het bekijken van een totaal in deze kolom opgeslagen voor toekomstige bezoeken aan deze pagina. Deze status wordt aangegeven door het streepje dat in deze kolom in de voettekst wordt weergegeven (of een totaal wordt onmiddellijk weergegeven als de gegevensset klein genoeg is).

Als u een fout maakt en geen totaal meer wilt zien in een bepaalde kolom, klikt u met de rechtermuisknop op de kolom en selecteert u **Totaal verbergen** of selecteert u de knop **Totaal verbergen** in de voettekst in die kolom. Deze voorkeur wordt ook opgeslagen voor toekomstige bezoeken aan de pagina. 

### <a name="calculating-totals"></a>Totalen worden berekend
Wanneer een pagina met de voettekst zichtbaar is en de kolommen al zijn geconfigureerd voor totalen, worden de totalen al dan niet weergegeven in de voettekst. Het gedrag is afhankelijk van de grootte van de gegevensset op de pagina. Als de gegevensset voldoende klein is, worden de totalen automatisch weergegeven, samen met het aantal rijen in de gegevensset. Als er streepjes in de voettekst staan onder de kolommen die u voor de totalen hebt geconfigureerd, is de gegevensset te groot voor het systeem om totalen direct weer te geven en is er een expliciete actie nodig om de totalen te berekenen. Klik hiervoor op de knop **Berekenen** in de voettekst of klik met de rechtermuisknop op een kolom waarvoor u een totaal wilt berekenen en selecteer **Deze kolom totaliseren**.  

Als de berekening te lang duurt, kunt u de bewerking annuleren door de knop **Annuleren** te selecteren. Soms is de gegevensset echter te groot voor het berekenen van totalen (een limiet die is ingesteld door uw organisatie) en wordt u in plaats hiervan op de hoogte gesteld om uw gegevens te filteren.

Totalen worden automatisch bijgewerkt wanneer u rijen bijwerkt, verwijdert of maakt in de gegevensset.  

## <a name="grouping-data"></a>Gegevens groeperen
Zakelijke gebruikers moeten vaak ad hoc gegevensanalyse uitvoeren. U kunt dit doen door gegevens te exporteren naar Microsoft Excel en draaitabellen te gebruiken, maar met de functie **Groepering** in tabelrasters kunnen gebruikers hun gegevens op interessante manieren ordenen in Finance and Operations-apps. Aangezien deze functie de functie **Totalen** uitbreidt, kunt u met **Groepering** ook duidelijke inzichten krijgen in de gegevens door subtotalen op te geven op groepsniveau.

Als u deze functie wilt gebruiken, klikt u met de rechtermuisknop op de kolom waarop u wilt groeperen en selecteert u **Groeperen op deze kolom**. Met deze actie sorteert u de gegevens op de geselecteerde kolom, voegt u een nieuwe Groeperen op-kolom toe aan het begin van het raster en voegt u koptekstrijen toe aan het begin van elke groep. Deze koptekstrijen bevatten de volgende informatie over elke groep: 
-  Gegevenswaarde voor de groep 
-  Kolomlabel. Dit is vooral handig wanneer meerdere groeperingsniveaus worden ondersteund.  
-  Aantal gegevensrijen in deze groep
-  Subtotalen voor alle kolommen die zijn geconfigureerd voor weergave van totalen

Als [Opgeslagen weergaven](saved-views.md) is ingeschakeld, kan deze groepering worden opgeslagen als onderdeel van een weergave voor snelle toegang, de volgende keer dat u de pagina bezoekt.  

Als u **Groeperen op deze kolom** selecteert in een andere kolom, wordt de oorspronkelijke groepering vervangen omdat er slechts één groepeerniveau wordt ondersteund in 10.0.9/platformupdate 33.

Als u het groeperen in een raster ongedaan wilt maken, klikt u met de rechtermuisknop op de groepeerkolom en selecteert u **Groepering opheffen**.  


## <a name="evaluating-math-expressions"></a>Wiskundige expressies evalueren
Als productiviteitsbooster kan de gebruiker wiskundige formules invoeren in numerieke cellen in een raster, in plaats van de berekening in een app buiten het systeem te moeten uitvoeren. U kunt bijvoorbeeld **=15\*4** invoeren en met Tab uit het veld gaan. Het systeem evalueert de expressie en slaat de waarde '60' op voor het veld.

Als u wilt dat het systeem een waarde herkent als een expressie, start u de waarde met het gelijkteken (**=**). Zie [Ondersteunde wiskundige symbolen](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols)voor meer informatie over de ondersteunde operators en syntaxis.  
