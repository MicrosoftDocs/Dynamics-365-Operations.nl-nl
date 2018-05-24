---
title: Assortimentsbeheer
description: In dit onderwerp worden de basisconcepten toegelicht van assortimentsbeheer in Microsoft Dynamics 365 for Retail en overwegingen bij de implementatie voor uw project.
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 033968667048faf475b13f8fb95e693dc26935ca
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="assortment-management"></a>Assortimentsbeheer
[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overzicht
Microsoft Dynamics 365 for Retail biedt *assortimenten* waarmee u de productbeschikbaarheid kunt beheren via kanalen. Assortimenten bepalen welke producten beschikbaar zijn in bepaalde winkels en een specifieke periode.

In Retail is een assortiment een toewijzing van een of meer kanalen (of groepen kanalen, wanneer organisatiehiërarchieën worden gebruikt) aan een of meer producten (of groepen producten wanneer categoriehiërarchieën worden gebruikt).

De algehele productsamenstelling van een kanaal wordt bepaald door de gepubliceerde assortimenten die zijn toegewezen aan het kanaal. Daarom kunt u meerdere actieve assortimenten configureren per kanaal.

### <a name="basic-assortment-setup"></a>Basisinstellingen assortimenten
In het volgende voorbeeld wordt een uniek assortiment geconfigureerd voor elke winkel. In dit geval is alleen product 1 beschikbaar in winkel 1, en alleen product 2 in winkel 2.

![Elk product is in één winkel beschikbaar](./media/Managing-assortments-figure1.png)

Als u wilt dat product 2 beschikbaar is in winkel 1, kunt u het product toevoegen aan assortiment 1.

![Product 2 toegevoegd aan assortiment 1](./media/Managing-assortments-figure2.png)

U kunt ook winkel 1 toevoegen aan assortiment 2.

![Winkel 1 toegevoegd aan assortiment 2](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organisatiehiërarchieën
In situaties waarin meerdere kanalen dezelfde productassortimenten delen, kunt u de assortimenten configureren met behulp van de Retail-organisatiehiërarchie voor assortimenten. Wanneer de knooppunten uit deze hiërarchie worden toegevoegd, worden alle kanalen in dat knooppunt en de onderliggende knooppunten opgenomen.

![Organisatiehiërarchie](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Productcategorieën
Aan de productkant kunt u groepen producten op dezelfde manier opnemen door categoriehiërarchieën voor producten te gebruiken. U kunt assortimenten configureren door een of meer hiërarchieknooppunten voor categorieën op te nemen. Het assortiment bevat in dit geval alle producten in dat categorieknooppunt en de onderliggende knooppunten.

![Productcategorieën](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Uitgesloten producten of categorieën
Behalve het opnemen van producten en categorieën in assortimenten kunt u de optie Uitsluiten gebruiken voor het definiëren van specifieke producten of categorieën die moeten worden uitgesloten van assortimenten. In het volgende voorbeeld wilt u alle producten in een bepaalde categorie opnemen, met uitzondering van product 2. In dit geval hoeft u het assortiment niet per product te definiëren of extra categorieknooppunten te maken. U kunt in plaats daarvan alleen de categorie opnemen maar het product uitsluiten.

> [!NOTE]
> Als een product per definitie zowel is opgenomen als is uitgesloten in een of meer assortimenten, wordt het product altijd beschouwd als uitgesloten.

![Uitgesloten product](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Algemene en vrijgegeven producten
Assortimenten worden gedefinieerd op een mondiaal niveau en kunnen kanalen van meerdere rechtspersonen bevatten. De producten en categorieën die zijn opgenomen in assortimenten worden ook door rechtspersonen gedeeld. Echter een product moet worden vrijgegeven voordat het daadwerkelijk kan worden verkocht, besteld, geteld of in het kanaal ontvangen (bijvoorbeeld in het verkooppunt \[POS\]). Ook al kunnen twee winkels in verschillende rechtspersonen een assortiment met dezelfde producten delen, toch zijn de producten alleen beschikbaar als ze zijn vrijgegeven aan deze rechtspersonen.

### <a name="dynamic-and-static-assortments"></a>Dynamische en statische assortimenten
Assortimenten kunnen worden gedefinieerd met kanalen en producten of door organisatie-eenheden en categorieën op te nemen. Assortimenten die verwijzingen naar deze groepen omvatten, worden beschouwd als dynamische assortimenten. Als de definitie of de inhoud van deze groepen verandert terwijl het assortiment actief is, wordt ook de definitie van het assortiment gewijzigd.

Een assortiment is bijvoorbeeld oorspronkelijk gedefinieerd en gepubliceerd zodat dit verwijst naar een categorie producten. Als later meer producten worden toegevoegd aan de categorie, worden deze producten automatisch opgenomen in de definitie van het bestaande assortiment. U hoeft de producten niet handmatig aan het assortiment toe te voegen. Op dezelfde manier wordt, als een organisatie-eenheid wordt toegevoegd aan een ander knooppunt, het assortiment van de organisatie-eenheid automatisch aangepast op basis van deze definitie.

### <a name="stopped-products"></a>Gestopte producten 
U kunt vrijgegeven producten stoppen voor het verkoopproces door een instelling in de **standaardorder**instellingen in te schakelen. Deze instelling wordt meestal gebruikt wanneer een product aan het einde van de levensduur is en niet via een kanaal moet worden verkocht. Assortimenten respecteren deze instelling en gestopte producten worden niet in het assortiment opgenomen, ongeacht de configuratie van het assortiment.

### <a name="blocked-products"></a>Geblokkeerde producten
U kunt de verkoop van een product tijdelijk blokkeren naast het stoppen van de verkoop van een product. U kunt deze instelling configureren op het tabblad **Detailhandel** van een vrijgegeven product. Geblokkeerde producten worden nog steeds in het assortiment opgenomen, maar u ontvangt een bericht in het POS met de melding dat het product niet kan worden verkocht.

### <a name="date-effectivity"></a>Ingangsdatum
Assortimenten hebben een ingangsdatum. Detailhandelaren kunnen daarom configureren wanneer producten wel of niet beschikbaar zijn per kanaal. U kunt assortimenten definiëren en van tevoren publiceren en de begin- en einddatums opgeven. De producten worden automatisch wel of niet beschikbaar op de opgegeven datums.

### <a name="process-assortments-batch-job"></a>Batchtaak Assortimenten verwerken
Assortimenten die zijn gedefinieerd in Retail moeten worden verwerkt voordat ze van kracht worden. Deze verwerking wordt uitgevoerd om de volgende redenen:

- De standaardisering voor assortimentdefinities moet worden aangepast zodat kanalen ze gemakkelijker kunnen verbruiken. Een productmix voor een kanaal kan worden gedefinieerd via meerdere assortimenten die verschillende periodes omvatten. Wanneer deze informatie vooraf wordt berekend op de server, worden de prestaties bij het kanaal verbeterd.
- De producten en kanalen in het assortiment kunnen buiten het assortiment zelf worden gewijzigd. Dynamische assortimenten die verwijzingen naar categorieën of organisatie-eenheden bevatten, moeten periodiek worden verwerkt, zodat ze records opnemen of uitsluiten, op basis van hun huidige toewijzing.

## <a name="implementation-considerations"></a>Implementatieoverwegingen
Overweeg de volgende vereisten voor de uitvoering als u assortimenten voor uw detailhandelsimplementatie plant en beheert:

- **Gegevensreplicatie en databasegrootte**: hoewel assortimenten kunnen voldoen aan de zakelijke behoefte voor het beheren van productbeschikbaarheid, zijn ze ook een belangrijk hulpmiddel voor het beheer van de grootte van kanaal- en offline databases. Goed beheerde assortimenten verminderen de hoeveelheid gegevens die moeten worden verwerkt en gerepliceerd in kanaal- en offline databases. Ze verminderen tevens het aantal records dat moet worden vastgelegd. Bij minder records in deze databases nemen de prestaties toe wanneer u artikelen toevoegt aan een transactie en bij het zoeken en bladeren.
- **Assortimenten met ingangs-/vervaldatum**: een van de meest effectieve hulpmiddelen voor het beheer van het aantal producten in de kanaal- en offline databases is de ingangsdatum van assortimenten. Als u assortimenten met een open einde (zonder vervaldatum) hebt voor seizoensproducten of producten die aan het einde van hun levensduur zijn, zullen deze databases ongelimiteerd groeien. U kunt verschillende benaderingen gebruiken om deze situatie te beheersen. U kunt bijvoorbeeld afzonderlijke assortimenten onderhouden voor seizoensgebonden en producten die altijd beschikbaar zijn.
- **Verkopen en retouren buiten assortimenten**: met deze mogelijkheid kunnen detailhandelaren hun assortimenten effectief beheren, doordat ze het aantal beschikbare producten beperken tot producten die tot de kernproductmix voor de winkel behoren. Hierdoor kunnen detailhandelaren ook situaties verwerken waarin een product per ongeluk is weggelaten uit een assortiment of waarin een product buiten de ingangsdatums voor het assortiment is geretourneerd.

Als productgegevens niet bestaan in de kanaaldatabase, start het POS real-time oproepen naar het hoofkantoor om de vereiste informatie op te halen, zodat het product kan worden verkocht, geretourneerd of op een bestelling kan worden geplaatst. Productgegevens die op deze manier worden opgehaald, zijn alleen beschikbaar tijdens het bereik van deze transactie. Het product wordt niet toegevoegd aan de assortimentdefinitie. Daarom worden volgende real-time aanroepen gestart indien vereist.

