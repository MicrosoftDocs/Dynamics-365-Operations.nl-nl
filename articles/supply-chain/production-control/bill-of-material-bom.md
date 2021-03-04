---
title: Stuklijsten en formules
description: Dit onderwerp bevat informatie over stuklijsten en formules, die een centraal deel uitmaken van de definitie van producten en productvarianten.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace, ProdBOM, ProdJournalTransBOM, ProdBOMCurrent, PmfBOMDesignerEditCoBy, ProdJournalPickingListLineSummary, ProdBOMOverview, PmfCoReqPlanning, EcoResProductProdTypeFormulaNoActiveFormulaFormPart, EcoResItemsMissingActiveRouteVersionFormPart, EcoResItemsProdTypeBOMExpiringBOMFormPart, BOMDesignerBOMVersion, BOMExpandPurch, BOMChangeLine, BOMExpandSales, EcoResItemsProdTypeBOMExpiringRouteFormPart, EngChgEcmBomDesigner, EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmBOMCopyDialog, EngChgEcmBomDesignerEditBom, BOMDesignerFilterDialog, BOMDesignerFilterDialog, BOMPartOf, BOMSetupReportFinish, EcoResItemsMissingActiveBOMVersionFormPart, BOMIdLookup, EcoResProductProdTypeFormulaNoActiveRouteFormPart, BOMExpandPurchRFQ, EngChgCaseRouteTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b226dd61c758cf17c8e4784ec22d2628145c1836
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425511"
---
# <a name="bills-of-materials-and-formulas"></a>Stuklijsten en formules

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over stuklijsten en formules, die een centraal deel uitmaken van de definitie van producten en productvarianten. Met stuklijsten en formules worden de benodigde materialen of ingrediënten voor een specifiek product opgegeven. Met formules worden ook de coproducten en bijproducten opgegeven die worden ontvangen in een specifieke productiecontext. 

<a name="bills-of-materials"></a>Stuklijsten
------------------

Met een stuklijst worden de onderdelen gedefinieerd die vereist zijn om een product te produceren. De onderdelen kunnen grondstoffen, halffabrikaten of ingrediënten zijn. In sommige gevallen kan naar services worden verwezen in een stuklijst. Met stuklijsten worden gewoonlijk de *materiaalresources* beschreven die zijn vereist.  

Wanneer een stuklijst met een route of een productiestroom wordt gecombineerd waarmee de bewerkingen en resources worden omschreven die zijn vereist om een product te maken, vormt de stuklijst de basis voor het berekenen van de kostenraming van het product.  

Een stuklijst een afzonderlijke entiteit die aan de hand van de volgende informatie wordt beschreven:

-   Stuklijst-ID
-   Stuklijstnaam
-   De stuklijstregels waarmee de onderdelen en ingrediënten worden beschreven
-   De stuklijstversies waarmee het product en de periode worden gedefinieerd waarvoor de stuklijst kan worden gebruikt

Met één stuklijst wordt één niveau beschreven dat door een unieke ID wordt geïdentificeerd. Onderdelen kunnen hun eigen stuklijsten hebben waarnaar met stuklijstversies wordt verwezen. U kunt de volledige hiërarchie van stuklijsten voor een specifiek product in de stuklijstontwikkelaar weergeven en bewerken.

### <a name="formulas-co-products-and-by-products"></a>Formules, co- en bijproducten

Een formule is een subtype van stuklijst, dat meestal voor procesproductie wordt gebruikt. Naast onderdelen en ingrediënten worden ook co- en bijproducten beschreven met een formule. In de werkelijke versie is voor de definitie van coproducten en bijproducten voor de formule de formuleversie vereist. Een formule wordt meestal gedefinieerd voor één specifiek eindproduct (een formule of planningsartikel) dat in de formuleversie wordt gedefinieerd.

### <a name="boms-in-the-product-lifecycle"></a>Stuklijsten in de productlevenscyclus

In de productlevenscyclus kunnen veel stuklijsttypen om diverse redenen worden gemaakt:

-   **Conceptstuklijst**: deze stuklijst geeft een conceptraming van vereiste materialen in een vroege ontwerpfase en helpt u een ruwe kostenraming te geven van kosten en geschatte productkenmerken. Deze stuklijst wordt gewoonlijk niet gebruikt in Enterprise Resource Planning (ERP).
-   **Technische stuklijst**: deze stuklijst wordt gewoonlijk gebruikt wanneer u producten ontwerpt die op bestaande productportfolio's zijn gebaseerd. De technische stuklijsten worden gemaakt om het ontwerpproces te vereenvoudigen en complexe producten te groeperen in technische modules. Voor eenvoudige producten kunnen technische stuklijsten voor het werkelijke productieproces worden gebruikt. Voor andere producten moet de technische stuklijst echter naar een werkelijke productiestuklijst worden geconverteerd. Technische stuklijsten worden meestal voorgesteld door phantoms in de stuklijsthiërarchie. Hoewel technische stuklijsten voor de planning en de uitvoering van productiebewerkingen kunnen worden gebruikt, kan deze werkwijze tot ondoelmatigheden leiden, met name in herhaalde bewerkingen waarin veel orders worden gemaakt.
-   **Planningstuklijst**: deze stuklijst wordt gebruikt om planning voor materiaalbehoeften uit te voeren. De vraag van onderdelen en ingrediënten wordt berekend op basis van de vraag van de eindproducten. Net als kostprijsberekeningsstuklijsten kan met planningsstuklijsten een specifieke combinatie van materiaal worden vertegenwoordigd die in een periode wordt gebruikt.
-   **Productiestuklijst**: dit is de werkelijke stuklijst die voor een specifieke productie wordt gebruikt. Bij een productiestuklijst moet rekening worden gehouden met de werkelijke resources waarmee het product wordt geproduceerd. Wanneer een productieorder, een batchorder of een kanban wordt gemaakt, worden de meerdere niveaus van stuklijsten die worden vertegenwoordigd door phantoms, samengevouwen in één niveau en over de bewerkingen voor de order verdeeld.
-   **Kostprijsberekeningsstuklijst**: deze stuklijst wordt gebruikt om de kostenraming van een product te berekenen. U kunt bijvoorbeeld een kostprijsberekeningsstuklijst gebruiken wanneer standaardkosten worden gebruikt of de geschatte geplande kosten van een bepaald product worden berekend. De kostprijsberekeningsstuklijsten kunnen naar een specifieke combinatie van materialen en resources verwijzen die naar verwachting worden gebruikt. Daarom kunt u de kostprijsberekeningsstuklijst gebruiken om een representatieve kostenraming voor een periode te maken en afwijkingen in de loop van de tijd helpen voorkomen.

De stuklijsttypen die daadwerkelijk in een implementatie worden gebruikt, zijn afhankelijk van de implementatie, en ook van de zakelijke scenario's en vereisten. In eenvoudige implementaties kunnen een planningsstuklijst, een productiestuklijst en een kostprijsberekeningsstuklijst als één stuklijst worden gemodelleerd. In omgevingen waarin frequente technische wijzigingen en meerdere alternatieve routes voorkomen, is waarschijnlijk een grotere set van stuklijsttypen vereist.

### <a name="approval-of-boms-and-formulas"></a>Goedkeuring van stuklijsten en formules

Elke stuklijst en formule kunnen afzonderlijk worden goedgekeurd of afgekeurd. Doorgaans vindt goedkeuring van een stuklijst of formule plaats wanneer de eerste relevante stuklijstversie wordt goedgekeurd. In bepaalde zakelijke scenario's kunnen deze goedkeuringen echter verschillende stappen in het proces betreffen en betrekking hebben op verschillende proceseigenaren.  

Als een stuklijst niet-goedgekeurd is, zijn alle gerelateerde stuklijstversies ook niet-goedgekeurd.

## <a name="bom-and-formula-versions"></a>Stuklijst- en formuleversies
Als u een specifieke stuklijst of een formule wilt koppelen aan een productvariant die kan worden geproduceerd, moet u een stuklijstversie of een formuleversie maken. De geldigheid van stuklijstversies en formuleversies kan per periode, hoeveelheid, locatie, specifieke productdimensies en andere criteria worden beperkt. Formuleversies hebben aanvullende belangrijke kenmerken, zoals opbrengst, co- en bijproductdefinities en de kostenverdelingsinstructies voor de formule.

### <a name="approval-of-bom-and-formula-versions"></a>Goedkeuring van stuklijst- en formuleversies

Voordat een stuklijstversie in de planning of het productieproces kan worden gebruikt, moet deze worden goedgekeurd. Wanneer een stuklijstversie wordt goedgekeurd, kan de gerelateerde stuklijst ook worden goedgekeurd. Dit is afhankelijk van de selectie van de gebruiker en verificatierechten. Een stuklijstversie kan worden alleen worden goedgekeurd als de gerelateerde stuklijst zelf is goedgekeurd.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Activering van de standaardstuklijst of formuleversie

Als u een specifieke stuklijst of een formule wilt instellen als de standaardstuklijstversie of -formuleversie die door hoofdplanning wordt gebruikt of waarmee productieorders worden gemaakt, moet u de versie activeren. Wanneer een versie is geactiveerd, wordt de uniekheid van de versie voor de opgegeven beperkingen (bijvoorbeeld periode, locatie of hoeveelheid) gecontroleerd. U krijgt een foutbericht weergegeven als de versie die u probeert te activeren, in conflict is met een versie die al actief is. U moet de conflicterende versie vervolgens deactiveren of de versiebeperkingen (meestal de periode) wijzigen om een dubbelzinnige activering te voorkomen.

### <a name="product-change-with-case-management"></a>Productwijziging met casebeheer

De productwijzigingscase voor goedkeuring en activering van nieuwe of gewijzigde stuklijsten en stuklijstversies biedt een gemakkelijke manier om een overzicht van de stuklijstversiebeperkingen te bekijken. U kunt ook alle stuklijsten en formules goedkeuren en activeren die verbonden zijn met een specifieke wijziging voor één activeringsdatum.

### <a name="alternative-bom-versions"></a>Alternatieve stuklijstversies

Soms wordt de actieve stuklijstversie of formuleversie niet gebruikt in prognoses, verkoop of een bovenliggend product. In dit geval kunt u een specifieke goedgekeurde stuklijst selecteren als onderdeel van de behoefte (prognoseregel, verkoopregel of stuklijstregel) als er een goedgekeurde stuklijstversie of formuleversie voor de alternatieve stuklijst of formule bestaat.  

Wanneer de geplande orders, productieorders of kanbans worden gemaakt, kan de planner of de werkvloersupervisor alle goedgekeurde stuklijstversies gebruiken die op de aangevraagde geplande productiedatum geldig zijn om te plannen voor een specifiek product of een bepaald product te produceren. De stuklijstversie die wordt gebruikt, hoeft niet als de standaardstuklijstversie te worden geactiveerd.

## <a name="bom-and-formula-lines"></a>Stuklijst- en formuleregels
Een stuklijstregel wordt gemaakt voor elk materiaal, elke service of elk ingrediënt. Met de regel wordt het geplande verbruik van de opgegeven productvariant gedefinieerd en worden ook de verschillende kenmerken gedefinieerd die aan het geplande verbruik zijn gekoppeld.  

Stuklijstregels kunnen de volgende regeltypen hebben: **Artikel**,**Phantom**, **Getraceerd aanbod**, **Leverancier**.

### <a name="item"></a>Artikel

Selecteer het regeltype **Artikel** voor materialen of services die direct worden verbruikt en die geen verdere explosie of getraceerd aanbod vereisen.

### <a name="phantom"></a>Phantom

Selecteer het regeltype **Phantom** wanneer u stuklijstartikelen van elk lager niveau op de stuklijstregel wilt exploderen. In de hoofdplanning, in geplande kostenberekening of bij raming van een productieorder waarin stuklijstregels van het type **Phantom** worden gebruikt, wordt de bovenliggende stuklijstregel die verwijst naar een productvariant die een phantom-stuklijst heeft, vervangen door de onderdeelartikelen die als stuklijstregels in die stuklijst worden weergegeven, zoals bepaald door de toepasselijke actieve stuklijstversie van die productvariant. Als de productvariant een toepasselijke actieve route heeft, worden de bewerkingen van die route samengevoegd in de bovenliggende route.  

Houd er rekening mee dat phantoms meestal worden gebruikt om het engineeringproces te vereenvoudigen. Uitgebreid gebruik van phantom-stuklijsten op veel niveaus heeft een effect op prestaties, met name in productiescenario's waarin veel herhaalde bewerkingen plaatsvinden. Ter verbetering van de prestaties moet u diepe hiërarchieën van phantoms voorkomen. Gebruik in plaats daarvan vooraf geëxplodeerde productiestuklijsten en routes.

### <a name="pegged-supply"></a>Getraceerd aanbod

Selecteer het regeltype **Getraceerd aanbod** wanneer u een subproductie maakt, een gebeurteniskanban voor een stuklijstregel of een directe inkooporder voor een productvariant waarnaar de stuklijstregel verwijst. De subproductie, de gebeurteniskanban of de inkooporder wordt gemaakt wanneer u de productieorder raamt. De vereiste artikelhoeveelheden worden automatisch gereserveerd voor de productieorder voor verbruik.

### <a name="vendor"></a>Leverancier

Selecteer het regeltype **Leverancier** als in het productieproces een toeleverancier wordt gebruikt en u automatisch een subproductie of inkooporder wilt maken voor de toeleverancier.  

**Opmerking over uitbestede bewerkingen in een stuklijst:** de service die wordt verleend of het werk dat wordt uitgevoerd door de toeleverancier, moet als serviceartikel worden gemaakt dat in voorraad wordt bijgehouden. U moet het serviceartikel koppelen aan het bovenliggende artikel als een stuklijstregel. De route dient een bewerking te bevatten die is toegewezen aan de bron voor bedrijfsactiviteiten van de toeleverancier.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]