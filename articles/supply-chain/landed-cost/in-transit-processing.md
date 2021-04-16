---
title: Goederen in transit verwerken
description: In dit onderwerp wordt beschreven hoe u met orders voor goederen in transit werkt. Wanneer een order of reis is ingesteld voor de verwerking van goederen in transit, kunnen goederen worden gefactureerd voordat deze voor verbruik in het magazijn zijn ontvangen.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9a1316de8d79f3ce34bb28812993d096cbd0c2ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823404"
---
# <a name="goods-in-transit-processing"></a>Goederen in transit verwerken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u met orders voor goederen in transit werkt. Dit type order wordt alleen gebruikt door de module **Francoprijzen**. Wanneer een order of reis is ingesteld voor de verwerking van goederen in transit, hoeft u niet te wachten totdat de goederen door het magazijn worden ontvangen voordat u ze kunt factureren. De goederen worden in dit geval gefactureerd wanneer ze het magazijn van de leverancier of de haven van vertrek verlaten en de financiële kosten worden herkend wanneer de reis begint. Met deze functionaliteit kunt u voorraad op de juiste manier in eigendom nemen, omdat goederen vaak eigendom van uw organisatie worden wanneer ze de haven verlaten.

Wanneer orders voor goederen in transit worden gebruikt, worden de financieel bijgewerkte artikelen ontvangen in een interim-magazijn dat ook wel een transitmagazijn wordt genoemd. De goederen blijven vervolgens in dit magazijn totdat ze kunnen worden ontvangen in het uiteindelijke doelmagazijn (dat wil zeggen het magazijn dat is gedefinieerd op de inkoopregel). Ze kunnen niet handmatig worden verwijderd.

Zolang de artikelen in transit zijn, zijn ze niet beschikbaar in de voorraad en kunnen ze niet voor een levering uit de voorraad worden opgehaald. U kunt de voorraad goederen in transit echter wel bekijken. U kunt de goederen ook gebruiken voor de hoofdplanning. In dit geval gebruikt u de bevestigde leveringsdatum op de inkooporderregel als de verwachte datum waarop de voorraad beschikbaar zal zijn voor verbruik.

In de volgende secties worden de instellingen beschreven die zijn vereist om de voorraad en reizen te verwerken aan de hand van het concept en de functionaliteit van goederen in transit.

## <a name="terms-of-delivery"></a>Leveringsvoorwaarden

Wanneer u de module **Francoprijzen** inschakelt, worden de standaardentiteit voor *Leveringsvoorwaarden* uitgebreid voor de ondersteuning van de functie goederen in transit.

Wanneer de optie **Beheer van goederen in transit** is ingesteld op *Ja* voor het record met de leveringsvoorwaarden dat van toepassing is, worden de goederen in het transitmagazijn opgeslagen. Deze actie wordt alleen geactiveerd als de voorraadontvangst niet wordt verwerkt voordat er een factuur is verwerkt. Wanneer de leveringsvoorwaarden voor een order zijn ingesteld voor gebruik van goederen in transit, kunnen gebruikers geen productontvangstbon meer voor de inkooporder boeken. Als ze dat proberen, treedt er een fout op. In het foutbericht wordt aangegeven dat zij de functionaliteit voor goederen in transit moeten gebruiken om door te gaan.

Als u met gegevens over leveringsvoorwaarden voor goederen in transit wilt werken, gaat u naar **Inkoopbeheer \> Instellen \> Distributie \> Leveringsvoorwaarden**. In de volgende tabel worden de velden beschreven die met de module **Francoprijzen** worden toegevoegd aan de pagina **Leveringsvoorwaarden** ter ondersteuning van de functionaliteit voor goederen in transit. Beide velden worden op het sneltabblad **Algemeen** weergegeven. Zie [Leveringsvoorwaarden (formulier)](https://technet.microsoft.com/library/aa575567.aspx) voor meer informatie over de andere velden op deze pagina.

| Veld | Beschrijving |
|---|---|
| Haven verplicht | Stel deze optie in op *Ja* als een haven verplicht is wanneer de leveringsvoorwaarden van toepassing zijn. |
| Beheer van goederen in transit | Stel deze optie in op *Ja* als u het beheer van goederen in transit wilt gebruiken wanneer de leveringsvoorwaarden van toepassing zijn. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Magazijnen voor goederen in transit en minderlevering

Wanneer u de module **Francoprijzen** inschakelt, wordt de standaardentiteit *magazijnen* uitgebreid om inkooporders te kunnen factureren terwijl de goederen zich in een transitmagazijn bevinden.

Bij Francoprijzen worden twee nieuwe magazijntypen toegevoegd: *goederen in transit* en *minderlevering*. Magazijnen van beide typen kunnen als standaardmagazijn worden geselecteerd. Voor een goede verwerking van orders voor goederen in transit moeten zowel het magazijn voor goederen in transit als het magazijn voor minderlevering zijn geconfigureerd op de pagina **Magazijnen**. Vervolgens moeten voor elk standaardmagazijn dat wordt gebruikt met Francoprijzen en goederen in transit, het magazijn voor goederen in transit en het magazijn voor minderlevering worden geselecteerd voor de beschikbare magazijnen van elk type.

Het magazijntype *goederen in transit* wordt gekoppeld aan uw magazijn voor goederen in transit en dat magazijn wordt gebruikt om de goederen op orders voor goederen in transit te verwerken voordat ze in het definitieve doelmagazijn worden ontvangen. Over het algemeen is één magazijn voor goederen in transit voldoende voor elke locatie als Locatie en Magazijn de enige voorraaddimensies zijn die voor voorraadbeheer worden gebruikt. Als de voorraaddimensie Locatie ook wordt gebruikt, moet er voor elke combinatie van een locatie en magazijn een magazijn voor goederen-in-transit worden ingesteld, zodat ook de standaardlocatie kan worden opgegeven.

Als u wilt werken met instellingen voor goederen in transit voor uw magazijnen, gaat u naar **Voorraadbeheer \> Instellen \> Opsplitsing van voorraad \> Magazijnen**. In de volgende tabel worden de velden beschreven die met de module **Francoprijzen** worden toegevoegd aan de pagina **Magazijnen** ter ondersteuning van de functionaliteit voor goederen in transit. Beide velden worden op het sneltabblad **Algemeen** weergegeven. Zie [Magazijnen (formulier)](https://technet.microsoft.com/library/aa620570.aspx) voor informatie over de andere velden op de pagina.

| Veld | Beschrijving |
|---|---|
| Magazijn voor goederen in transit | Identificeer het magazijn voor goederen in transit dat is gekoppeld aan het hoofdmagazijn. |
| Magazijn voor minderlevering | Identificeer het magazijn voor minderlevering dat is gekoppeld aan het hoofdmagazijn. |

## <a name="posting-rules-for-landed-cost"></a>Regels boeken voor francoprijzen

Met Francoprijzen worden twee nieuwe boekingsregels toegevoegd die u kunt configureren. Deze boekingsregels worden gebruikt om bedragen van directe inkooporderfacturen financieel te boeken om het eigendom van de goederen aan te geven wanneer ze het punt van vertrek verlaten. Dit proces vervangt het concept van *ontvangen maar nog niet gefactureerde goederen*, omdat de goederen worden gefactureerd voordat ze worden ontvangen. <!-- KFM: Add a link to the related scenario when available. -->

Als u wilt werken met boekingsprofielen, gaat u naar **Voorraadbeheer \> Instellen \> Boeken \> Boeken**. Op het tabblad **Inkooporder** zijn de volgende nieuwe boekingsregels beschikbaar:

- **Francoprijzen, goederen in transit**: Geef de boekingsregels voor het beheer van goederen in transit op.
- **Francoprijzen, toerekening van toeslagen**: Geef de boekingsregels op voor de toerekening van de toeslagrekening.

## <a name="goods-in-transit-orders"></a>Orders voor goederen in transit

U kunt orders voor goederen in transit rechtstreeks controleren en beheren in de module **Francoprijzen**. U kunt orders voor goederen in transit direct verwerken op de pagina **Orders voor goederen in transit**. U kunt ook naar de reis gaan die is gekoppeld aan de orders voor goederen in transit en de hele reis, container of folio verwerken. Wanneer u een reis factureert en een order voor goederen in transit maakt, wordt er een nieuwe order voor goederen in transit gemaakt voor elke combinatie van voorraad en voorraaddimensies die aan de inkooporderregel is gekoppeld.

Voor het beheren van goederen in transit wordt in Francoprijzen een procedure met twee stappen gebruikt:

1. Een artikel wordt ontvangen wanneer een voorraadfactuur wordt verwerkt en de status *In transit* krijgt.
1. De order voor goederen in transit wordt verwerkt op de pagina **Orders voor goederen in transit** en vervolgens ontvangen in het magazijn dat is opgegeven op de inkooporder. Op dat moment wordt de status gewijzigd in *Ontvangen*.

Als u wilt werken met orders voor goederen in transit, gaat u naar **Francoprijzen \> Periodieke taken \> Orders voor goederen in transit**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Voorraad ontvangen van het magazijn voor goederen in transit

U kunt op verschillende manieren goederen ontvangen van orders voor goederen in transit, afhankelijk van de instellingen van uw systeem.

### <a name="in-transit-receiving"></a>Goederen in transit ontvangen

U kunt goederen in transit ontvangen vanaf een van de volgende pagina's:

- Selecteer op de pagina **Orders voor goederen in transit** de regel en selecteer vervolgens **Ontvangen** in het actievenster.
- Selecteer of open een reis op de pagina **Alle reizen**. Selecteer vervolgens in het actievenster op het tabblad **Beheren** in de groep **Goederen in transit** de optie **Goederen in transit ontvangen**.
- Selecteer of open een container op de pagina **Alle containers**. Selecteer vervolgens in het actievenster op het tabblad **Beheren** in de groep **Goederen in transit** de optie **Goederen in transit ontvangen**.
- Selecteer of open een folio op de pagina **Alle folio's**. Selecteer vervolgens in het actievenster op het tabblad **Beheren** in de groep **Goederen in transit** de optie **Goederen in transit ontvangen**.

> [!NOTE]
> Het ontvangen van goederen in transit wordt meestal gebruikt in situaties waarin geen locaties en batch-/serienummers worden gebruikt.

### <a name="arrival-journal"></a>Ontvangstjournaal

U kunt goederen ook ontvangen door een ontvangstjournaal te maken. U kunt een ontvangstjournaal rechtstreeks via de pagina Reis maken. De aanbevolen procedures die uw organisatie gebruikt, bepalen of het ontvangstjournaal wordt gebruikt om goederen te ontvangen.

1. Open de reis, container of folio.
1. Selecteer in het Actievenster op het tabblad **Beheren** in de groep **Functies** de optie **Ontvangstjournaal maken**.
1. Stel in het dialoogvenster **Ontvangstjournaal maken** de volgende waarden in:
    - **Hoeveelheid initialiseren**: Stel deze optie in op *Ja* om de hoeveelheid goederen in transit in te stellen. Als u deze optie instelt op *Nee*, wordt er geen standaardhoeveelheid ingesteld op de regels voor goederen in transit.
    - **Maken op basis van goederen in transit**: stel deze optie in op *Ja* als u hoeveelheden uit de geselecteerde regels voor in transit wilt halen voor de geselecteerde reis, container of folio.
    - **Maken op basis van orderregels**: Stel deze optie in op *Ja* om de standaardhoeveelheid in het ontvangstjournaal van de inkooporderregels in te stellen. De standaardhoeveelheid in het ontvangstjournaal kan alleen op deze manier worden ingesteld als de hoeveelheid op de inkooporderregel overeenkomt met de hoeveelheid op de in transit-order.

1. Verwerk het ontvangstjournaal zoals is beschreven in [Artikelontvangsten registreren met een artikelontvangstjournaal](https://technet.microsoft.com/library/aa571129.aspx).

> [!NOTE]
> Het ontvangstjournaal wordt meestal gebruikt in situaties waarin locaties en tracering van batch-/serienummers worden gebruikt, maar magazijnbeheer niet wordt gebruikt.
>
> Standaardontvangstlocaties moeten niet op de orderregels worden opgegeven als er in het ontvangstjournaal een wegzetlocatie wordt opgegeven.

## <a name="warehouse-management"></a>Magazijnbeheer

Wanneer u de module **Francoprijzen** inschakelt, worden meerdere pagina's in de module **Magazijnbeheer** gewijzigd zodat de orderverwerking (met name de verwerking van goederen in transit) kan worden uitgevoerd via de module **Francoprijzen**. In deze sectie worden de velden en processen beschreven die aan de module **Magazijnbeheer** zijn toegevoegd.

### <a name="mobile-device-menu-items"></a>Menuopties voor mobiel apparaat

Goederen kunnen worden ontvangen met behulp van een mobiel apparaat, mits het menu voor mobiele apparaten en de module **Magazijnbeheer** zijn ingesteld om goederen op een order voor goederen in transit te ontvangen. In deze sectie worden de instellingen beschreven die zijn gekoppeld aan de ontvangst van goederen in transit.

Als u mobiele apparaten wilt instellen voor de verwerking van goederen in transit, gaat u naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiele apparaat**.

Met Francoprijzen worden de volgende processen voor het maken van werk aan de menuopties van het mobiele apparaat toegevoegd ter ondersteuning van de verwerking van goederen in transit:

- Artikelontvangst voor goederen in transit
- Artikel van goederen in transit ontvangen en wegzetten

De configuratie-instellingen voor deze processen lijken op de instellingen voor het [ontvangen en het maken van processen voor het maken van wegzetwerk](https://technet.microsoft.com/library/dn553216.aspx). Met het proces *Artikel van goederen in transit ontvangen en wegzetten* wordt echter ook het volgende veld toegevoegd.

- **Container voltooid inschakelen**: Als deze optie is ingesteld op *Ja* wanneer het wegzetwerk is voltooid, biedt de mobiele app Magazijnbeheer een extra optie met de naam **Container voltooid**. Wanneer deze optie is geselecteerd, wordt de werknemer gevraagd te bevestigen dat de container is voltooid. Op dat moment worden alle korte ontvangsten verwerkt als een transactie voor minderlevering.

### <a name="location-directives"></a>Locatie-instructies

Met Francoprijzen wordt een nieuw type werkorder met de naam *Goederen in transit* toegevoegd aan de pagina **Locatie-instructies**. Dit type werkorder moet op dezelfde manier worden geconfigureerd als de [typen werkorders voor inkooporders](https://technet.microsoft.com/library/dn553184.aspx).

### <a name="work-templates"></a>Werksjablonen

Met Francoprijzen wordt een nieuw type werkorder met de naam *Goederen in transit* toegevoegd aan de pagina **Werksjablonen**. Dit type werkorder moet op dezelfde manier worden geconfigureerd als de [werksjablonen voor inkooporders](https://technet.microsoft.com/library/dn553184.aspx).

