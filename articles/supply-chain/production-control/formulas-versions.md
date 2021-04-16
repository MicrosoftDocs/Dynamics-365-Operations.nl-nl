---
title: Formules en formuleversies
description: Dit onderwerp biedt informatie over formules en formuleversies. Een formule bepaalt de materialen, ingrediënten en uitkomsten van een bepaald proces in procesfabricage. Formules worden gebruikt voor de planning en productie van producten in procesfabricage.
author: cvocph
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule, EcoResProductProdTypeFormulaNoActiveFormulaFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8a168da2309709baaf9f8006880d738f754751d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809105"
---
# <a name="formulas-and-formula-versions"></a>Formules en formuleversies

[!include [banner](../includes/banner.md)]

Een formule bepaalt de materialen, ingrediënten en uitkomsten van een bepaald proces in procesfabricage. In combinatie met de bijbehorende route bepaalt de formule het hele proces in de procesfabricage. Formules worden gebruikt voor de planning en productie van producten in procesfabricage.

Een formule bestaat uit de ingrediënten en hoeveelheden die nodig zijn om een bepaalde hoeveelheid van een formuleartikel te produceren. Afhankelijk van de taak die u uitvoert, zijn formulefuncties toegankelijk vanuit Voorraad- en magazijnbeheer of Productgegevensbeheer.

## <a name="formulas-and-formula-lines"></a>Formules en formuleregels
Een formule bestaat uit een of meer formuleregels. Deze regels vormen de ingrediënten of artikelen die samen de formule vormen. Een formuleregel kan stuklijstartikelen, formuleartikelen, catch weight-artikelen, ingekochte artikelen, coproducten of bijproducten bevatten. Aangezien veel artikelen in meerdere producten worden gebruikt, kunt u een artikel in meerdere formules gebruiken.

Een voorbeeld van een formule is de formule voor een chocoladekoekje. De ingrediënten voor deze formule omvatten meerdere regels, bijvoorbeeld voor bloem, suiker, eieren, boter en chocolade. De formule voor het chocoladekoekje bevat ingrediënten die waarschijnlijk ook in andere formules worden gebruikt. Tijdens het maken van de chocoladekoekjes kan er wat overblijven, bijvoorbeeld kruimels, of worden sommige koekjes misschien te lang of te kort gebakken. Deze artikelen kunnen worden ingesteld als coproducten of bijproducten, afhankelijk van de productiebewerkingen.

Wanneer u een formuleregel maakt, gebruikt u het regeltype om aan te geven hoe het systeem de regel moet verwerken wanneer u hoofdplanning uitvoert en batchorders produceert. Elk regeltype zorgt voor een ander resultaat. In de volgende tabel worden de regeltypen beschreven die u kunt selecteren. 

| Regeltype     | Omschrijving  |
|---------------|--------------|
| Artikel          | Selecteer **Artikel** wanneer het artikel een grondstof of halffabricaat is dat moet worden verzameld in de voorraad, of wanneer het artikel een service is. |
| Phantom       | Selecteer **Phantom** wanneer u formuleartikelen van elk lager niveau op formuleregels wilt exploderen. Wanneer u de batchorder raamt en de formuleartikelen worden geëxplodeerd, worden de componentartikelen als formuleregels weergegeven in de batchorder. Bovendien worden de bijbehorende routes toegevoegd aan de productieroute. Formuleartikelen worden geëxplodeerd op basis van de huidige configuratie. Wanneer u het regeltype **Phantom** gebruikt, kunt u productie- en metingconfiguraties op verschillende formuleniveaus verwerken. Als u **Phantom** voor een product op het sneltabblad **Engineering uitvoeren** van de pagina **Vrijgegeven productdetails** selecteert en dit product vervolgens in een formule gebruikt, wordt het regeltype van de formuleregel gewijzigd in **Phantom**. U kunt **Phantom** niet selecteren voor een catch weight-artikel of artikelen waarvoor het productietype **Coproduct**, **Bijproduct** of **Planningsartikel** is. |
| Getraceerd aanbod | Selecteer **Getraceerd aanbod** om een batchorder, productieorder, kanban, overboekingsorder of inkooporder te maken voor het ingrediënt op de formuleregel. De betreffende order wordt bepaald op basis van de standaardorderinstellingen en het productietype van het ingrediënt, en wordt gemaakt wanneer u de batchorder raamt. De vereiste ingrediënthoeveelheden worden gereserveerd voor de batchorder. |
| Leverancier        | Selecteer **Leverancier** als voor het productieproces een toeleverancier wordt gebruikt en u een subproductie of inkooporder wilt maken voor de toeleverancier. De service of de werkzaamheden die door de toeleverancier worden uitgevoerd, moeten worden gemaakt met een formule- of serviceartikel. U kunt het artikel aan het bovenliggende artikel koppelen als formuleregel. De route dient een bewerking te bevatten die is toegewezen aan de bron voor bedrijfsactiviteiten van de toeleverancier. U kunt deze bewerking aan de formuleregel koppelen door het veld **Bewerkingsnummer** te gebruiken. |

## <a name="formula-versions"></a>Formuleversies
Wanneer u een nieuwe formule maakt, moet u een formuleversie maken voordat u de formuleregelartikelen met hun specifieke eigenschappen toevoegt. Elke formule moet minimaal één versie hebben. De knop **Goedgekeurd** voor een formuleversie wordt pas beschikbaar als er een versierecord is opgeslagen. Elke formuleversierecord is gekoppeld aan een of meer coproducten en bijproducten die kunnen worden geproduceerd als u het eindproduct produceert. Veel producten kunnen van dezelfde ingrediënten worden gemaakt, in verschillende batchgroottes, in veelvouden of met behulp van verschillende opbrengsten. U kunt zoveel versies van een formule maken als nodig is.

Voor het beheer van meerdere actieve formuleversies gebruikt u effectieve datumbereiken of velden met een vanaf-hoeveelheid. Er kunnen alleen meerdere actieve formuleversies bestaan als het datumbereik en de vanaf-hoeveelheid elkaar niet overlappen.

In tegenstelling tot stuklijsten, waarbij één stuklijst vaak is gekoppeld aan meerdere stuklijstversies, bestaat er doorgaans slechts één formuleversie per formule. Houd er rekening mee dat slechts één formuleversie kan worden geactiveerd voor de behoefteplandimensies en hoeveelheid voor een bepaald product. Er kunnen echter ook veel formuleversies om andere redenen bestaan en u kunt deze handmatig selecteren wanneer u een batchorder maakt.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Formules en formuleversies goedkeuren en activeren
Zowel formules als formuleversies moeten worden goedgekeurd voordat ze kunnen worden gebruikt voor planning en productie. Formules worden doorgaans geactiveerd voordat ze worden gebruikt. Tijdens de productie kunt u echter een formuleversie selecteren die is goedgekeurd, maar nog niet geactiveerd.

Als u een formule of formuleversie wilt beveiligen, kunt u de parameters **Bewerken blokkeren** en **Verwijdering van goedkeuring blokkeren** op de pagina **Parameters van productiebeheer** instellen.

Als u **Bewerken blokkeren** selecteert en de formule is goedgekeurd, kunnen de velden in de formuleregels niet worden verwijderd of bewerkt. Als u de goedkeuring van de formule verwijdert, kunt u de formuleregels weer verwijderen en wijzigen. U kunt ook nieuwe formules en formuleversies maken.

Als u **Verwijdering van goedkeuring blokkeren** selecteert, kunt u de goedkeuring van een goedgekeurde formule of formuleversie niet verwijderen. U kunt wel nieuwe formules en formuleversies maken en de activering van de formuleversie verwijderen.

U kunt meer controleniveaus toevoegen met behulp van de functionaliteit voor elektronische handtekeningen. Wanneer een gebruiker zo is ingesteld dat een elektronische handtekening vereist is op het moment van goedkeuring van de formule, dan wordt de pagina **Handtekening** weergegeven wanneer de formule is geactiveerd. De gebruiker moet gemachtigd zijn om elektronisch te ondertekenen en het certificaat moet worden gevalideerd voordat de wijziging kan worden doorgevoerd. Als de handtekening niet kan worden geverifieerd, wordt de goedkeuring of verwijdering van goedkeuring geweigerd en wordt de wijziging ongedaan gemaakt.

## <a name="use-the-scalable-feature"></a>De functie Schaalbaar gebruiken
De functie Schaalbaar is alleen beschikbaar als alle artikelonderdelen in de formule zijn ingesteld op **Variabel verbruik**. De functie is niet beschikbaar als artikelonderdelen zijn ingesteld op **Vast verbruik** of **Stapverbruik**. Als u deze functie gebruikt, resulteert een wijziging in een ingrediënt in een formule tevens in een aanpassing van de hoeveelheid van de andere ingrediënten die u selecteert. De grootte van de formule wordt eveneens gecorrigeerd. Op dezelfde manier wordt de hoeveelheid van alle schaalbare ingrediënten gewijzigd als u de formulegrootte wijzigt. Deze functie is specifiek bedoeld voor het maken en onderhouden van formules. Er wordt niet aangegeven of de hoeveelheid van een ingrediënt wordt aangepast voor een batchorder.

## <a name="use-step-consumption"></a>Stapverbruik gebruiken
Bij stapverbruik hoeft u geen hoeveelheid op het tabblad **formuleregel** op te geven voor een ingrediënt. In plaats daarvan is Stapverbruik zo geconfigureerd dat er waarden voor **Van serie** en **Hoeveelheid** moeten worden opgegeven. Op basis van de informatie in de record Stap per reeks wordt gegarandeerd dat de hoeveelheid in de batchorder wordt geselecteerd. Stapverbruik is handig als het materiaalverbruik niet lineair is met betrekking tot de grootte van de batchorder en de vereiste alleen wordt verhoogd als een specifieke drempelhoeveelheid wordt bereikt. Als u deze functie wilt inschakelen voor een nieuwe formule, wijzigt u onder de groep **Verbruiksberekening** de formule-instelling voor het desbetreffende ingrediënt van **Standaard** in **Stap**. U geeft deze verbruiksmethode op het tabblad **Instelling** van de pagina **Formuleregel** op.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]