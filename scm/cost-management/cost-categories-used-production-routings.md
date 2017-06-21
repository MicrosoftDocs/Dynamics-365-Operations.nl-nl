---
title: "Kostencategorieën die in productieroutering worden gebruikt"
description: "Dit artikel geeft informatie over kostencategorieën die van toepassing zijn op productieomgevingen die routering gebruiken."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 12e712e0a28ada0716d35b7105fb20c354d1bc18
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="cost-categories-used-in-production-routing"></a>Kostencategorieën die in productieroutering worden gebruikt

[!include[banner](../includes/banner.md)]


Dit artikel geeft informatie over kostencategorieën die van toepassing zijn op productieomgevingen die routering gebruiken.

Kostencategorieën hebben betrekking op productieomgevingen die gebruikmaken van routeringen. Ze worden toegewezen aan bronnen voor bedrijfsactiviteiten en aan routeringsbewerkingen om uurkosten te definiëren en kostenbijdragen te segmenteren in de berekende kosten van een gefabriceerd artikel. De kostengroepen die aan kostencategorieën zijn toegewezen classificeren de bijdragen aan fabricagekosten op basis van de bronnen voor bedrijfsactiviteiten en het activiteitstype, zoals voorbereidingstijd en uitvoeringstijd. De gedetailleerdheid van kostengroeptoewijzingen maakt het mogelijk om de productieoverhead te berekenen op basis van routeringsgegevens. 

**Opmerking**: Kostencategorieën hebben binnen productieomgevingen verschillende andere namen, zoals arbeidstariefcodes of machinetariefcodes. 

Elke kostencategorie is gekoppeld aan kostenrecords en is toegewezen aan een kostengroep. Verschillende kostencategorieën zijn vereist om verschillende productiedoeleinden te ondersteunen.

-   Wijs verschillende uurkosten toe, afhankelijk van de bron voor bedrijfsactiviteiten. Bijvoorbeeld kunnen de kosten voor verschillende typen arbeidsvaardigheden, machines, of productiecellen verschillen.
-   Wijs verschillende uurkosten toe aan de voorbereidingstijd of uitvoeringstijd die aan een routeringsbewerking is gekoppeld.
-   Wijs de kosten voor bronnen voor bedrijfsactiviteiten toe op basis van de hoeveelheid uitvoer in plaats van de uurkosten. Gebruik bijvoorbeeld stukwerktarieven om arbeid te betalen.
-   Biedt kostengroepsegmentatie aan van kostenbijdragen in de berekende kosten van een gefabriceerd artikel. U kunt bijvoorbeeld een segmentatie van arbeids- en machinekosten geven.
-   Gebruik de basis van de kostengroep bij berekeningsformules voor overheadkosten, zoals formules voor arbeidsgerelateerde en machinegerelateerde overhead of overhead die is gerelateerd aan voorbereidingstijd en uitvoeringstijd.

Een kostencategorie kan worden toegewezen aan de insteltijd, de verwerkingstijd en de hoeveelheid voor een routebewerking. Wanneer bijvoorbeeld kosten of kostengroepsegmentatie tussen instel- en verwerkingstijd verschillen, moeten verschillende kostencategorieën worden gedefinieerd en hieraan worden toegewezen. Het selectieve gebruik van kostencategorieën voor insteltijd, verwerkingstijd en hoeveelheid kan worden bepaald aan de hand van de routegroep die aan een bewerking is toegewezen. De toewijzing van kostencategorieën aan tijd en hoeveelheid kan worden voorgeschreven door bedrijfsbeleidsregels die worden gedefinieerd op de pagina **Parameters van productiecontrole**. 

Aan elke kostencategorie zijn kosten gekoppeld die zijn gebaseerd op de definitie van kostenrecords binnen een kostenberekeningsversie. Gebruik de pagina **Kostencategorieprijs** om de kostenrecords voor een opgegeven kostprijsberekeningsversie en locatie te definiëren. Wanneer de kostenrecord voor een kostencategorie voor het eerst wordt ingevoerd, heeft het de **In behandeling** en een gewenste ingangsdatum. Als u de kostenrecord activeert, wordt de status bijgewerkt naar **Huidige actief** en de begindatum naar de activeringsdatum. Verschillende kostenrecords staan mogelijk voor verschillende locaties, begindatums of statussen. Voor stuklijstberekeningen voor een datum in de toekomst of in het verleden wordt gebruikgemaakt van kostenrecords die de van toepassing zijnde ingangsdatum hebben. De huidige actieve kostenrecord wordt gebruikt om productieorderkosten te schatten en om de tijd waarover wordt gerapporteerd te waarderen ten opzichte van een productieorder. 

De kostenrecord voor een kostencategorie kan alleen voor de locatie of voor het hele bedrijf gelden. Als u een kostenrecord locatiespecifiek wilt maken, wijst u er een locatie aan toe. Een lege waarde geeft aan dat de kostenrecord geldt voor alle locaties binnen het bedrijf. Omdat bijvoorbeeld de kosten per locatie kunnen verschillen, moeten de kostenrecords als locatiespecifiek worden gedefinieerd. 

Een routeringsbewerking neemt in het algemeen de kostencategorieën over die aan de bron voor bedrijfsactiviteiten of hoofdbewerking zijn toegewezen. Als er een productieorder is gemaakt, wordt de geselecteerde routeversie weerspiegeld in de routeringsbewerkingen binnen de productieroute. U kunt de kostencategorieën negeren die aan de bewerkingen binnen de productieroute zijn toegewezen. 

Bepaalde typen productiewerk zijn mogelijk van toepassing op geraamde projecturen en rapportage. In een dergelijk geval is een kostencategorie vereist voor productie- en projectdoeleinden. Als een kostencategorie is gemarkeerd voor gebruik in projecten, moeten aanvullende projectgerelateerde gegevens worden gedefinieerd.




