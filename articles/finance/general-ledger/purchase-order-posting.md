---
title: Boeking van inkooporders
description: In dit onderwerp wordt het tabblad Inkooporder van de pagina Voorraadboekingsprofielen beschreven.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 4b36ab9da22da7d4f3e62bd2d2aba2a2ec80e60f
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/24/2022
ms.locfileid: "8802998"
---
# <a name="purchase-order-posting"></a>Boeking van inkooporders

Het tabblad **Inkooporder** op de pagina **Voorraadboekingsprofielen** wordt gebruikt om te bepalen hoe inkooporders naar het grootboek worden geboekt. Twee hoofdactiviteiten worden voor een inkooporder naar het grootboek geboekt: 

- Ontvangst van producten
- Factuur

Als u een fysieke transactie (productontvangstbon) wilt boeken naar het grootboek voor een inkooporder, moeten de volgende selectievakjes zijn ingeschakeld:

- Het selectievakje **Productontvangstbon in grootboek boeken** op de pagina **Parameters voor voorraad- en magazijnbeheer**.
- De selectievakjes **Fysieke voorraad boeken** en **Toerekening van aansprakelijkheid bij productontvangstbon** op de pagina **Artikelmodelgroepen**.

Op de pagina **Voorraadboekingsprofiel** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:

- Kosten van ingekochte ontvangen materialen
- Inkoopuitgave, niet-gefactureerd
- Inkoop, toerekening

Als u een financiële transactie (factuur) wilt boeken naar het grootboek voor een inkooporder, moet er aan de volgende voorwaarden zijn voldaan:

- Het selectievakje **Financiële voorraad boeken** moet zijn ingeschakeld op de pagina **Artikelmodelgroepen** voor het artikel dat op de inkooporderregel is geselecteerd.
- Op de pagina **Voorraadboekingsprofiel** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:
  - Kosten van ingekocht gefactureerd materiaal
  - Inkoopuitgave voor product
  - Inkoopuitgaven voor onkosten
  - Korting (optioneel)

## <a name="fixed-receipt-price-posting"></a>Boeking van vaste ontvangstprijs

U kunt vaste ontvangstprijs gebruiken als standaardkosten voor een product als een alternatief voor het selecteren van de optie **Standaardkosten** in het veld **Voorraadmodel** op de pagina **Artikelmodelgroepen** voor een artikel. Het belangrijkste verschil wanneer **Vaste ontvangstprijs** wordt gebruikt, is dat de huidige kostprijs voor het artikel wordt gebruikt wanneer de voorraadontvangst wordt geboekt. Er is geen kostprijsherwaarderingsproces voor **Vaste ontvangstprijs**. Wanneer een financiële update wordt geboekt, wordt de huidige kostprijs gebruikt bij het boeken. Als er een verschil is tussen de kostprijs die bij ontvangst wordt gebruikt en de factuur, wordt het verschil geboekt naar de winst- en verliesrekeningen van de vaste ontvangstprijs.

Als u een vaste ontvangstprijs voor een product wilt gebruiken, moet u het volgende configureren:

- Schakel op de pagina **Artikelmodelgroepen** de selectievakjes **Fysieke voorraad boeken** en **Vaste ontvangstprijs** in. 
- Schakel op de pagina **Parameters van voorraad- en magazijnbeheer** het selectievakje **Pakbon in grootboek boeken** in.
- Geef op de pagina **Voorraadboekingsprofiel** de hoofdrekeningen voor de volgende boekingstypen op:
  - Winstrekening vaste ontvangstprijs
  - Verliesrekening vaste ontvangstprijs
  - Tegenrekening vaste ontvangstprijs

Ga naar [Vaste ontvangstprijs](/supply-chain/cost-management/fixed-receipt-price.md) voor meer informatie.

## <a name="purchase-charges-and-stock-variation-posting"></a>Boeking van toeslagen op inkoop en voorraadwijziging

Als u van plan bent om rekening te houden met toeslagen op inkoop en voorraadwijzigingen, moet u het volgende doen:

- Schakel op de pagina **Parameters van leveranciers** op het tabblad **Factuur** het selectievakje **Boeken op toeslagrekening in grootboek** in.
- Op de pagina **Artikelmodelgroepen** voor het artikel dat is geselecteerd op de inkooporderregel, schakelt u de selectievakjes **Fysieke voorraad boeken**, **Financiële voorraad boeken** en **Toerekening van aansprakelijkheid bij productontvangstbon** in.
- Schakel op de pagina **Parameters voor inkoopbeheer** het selectievakje **Toeslagen genereren op productontvangstbon** in.
- Schakel op de pagina **Parameters van voorraad- en magazijnbeheer** het selectievakje **Pakbon in grootboek boeken** in.

Op de pagina **Voorraadboekingsprofiel** moet u de hoofdrekeningen opgeven voor de volgende boekingstypen:

- Inkoopuitgave, niet-gefactureerd
- Inkoopuitgave voor product
- Voorraadwijziging

> [!NOTE]
> Het boekingstype **Toeslagen** wordt niet gebruikt wanneer de parameter **Boeken op toeslagrekening in grootboek** is geselecteerd.

Ga naar [Boekhoudprincipe voor boeken op toeslagrekening](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md) voor meer informatie.

## <a name="sample-posting-profile-configuration"></a>Voorbeeldconfiguratie van boekingsprofiel

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen met voorbeeldhoofdrekeningen en omschrijvingen:

- De kolom **Vereffeningsrekening** geeft aan of het boekingstype een vereffeningsrekening is. Het bedrag dat op deze rekening wordt geboekt, wordt automatisch teruggeboekt wanneer een latere transactie wordt geboekt. 
- In de kolom **P/F** verwijst **P** naar fysieke boeking en **F** naar financiële boeking. 
- De kolom **Volgen** geeft aan of de hoofdrekening voor een bepaald boekingstype gewoonlijk hetzelfde is als een ander boekingstype. De waarde in de kolom geeft het boekingstype aan dat normaal gesproken wordt gebruikt.

> [!NOTE]
> De hoofdrekeningen en hoofdrekeningnamen zijn alleen suggesties. We raden aan<!--note from editor: Via Writing Style Guide.--> dat u samen met uw accountant bepaalt wat de beste configuratie is voor uw bedrijfsbehoeften.


| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | P/F | Volgen | Description |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Kosten van ingekocht ontvangen materiaal | 140100</br>140101 | Materiaalvoorraad</br>Materiaal verzonden niet gefactureerd | Activum | Debet | Ja | W | Kosten van ingekocht gefactureerd materiaal | Gebruikt wanneer een productontvangstbon voor een inkooporder wordt geboekt. De verschuiving op de rekening betreft de Inkoopuitgave, niet-gefactureerd. Het bedrag op deze rekening wordt teruggeboekt wanneer een factuur voor een verkooporder wordt geboekt. |
| Inkoopuitgave, niet-gefactureerd | 600180 | Materiaalontvangstbonnen | Onkosten | Debet | Ja | W | |Gebruikt wanneer een productontvangstbon voor een inkooporder wordt geboekt. Er zijn twee boekstukken gemaakt voor de ontvangst om inkoopprijsafwijkingen bij te houden wanneer de standaardkosten worden gebruikt. De verschuiving op de rekening voor het eerste boekstuk is Inkoop, toerekening. De verschuiving voor het tweede boekstuk is de som van de kosten van ingekocht ontvangen materiaal en de rekeningen voor inkoopprijsafwijkingen. De naar deze rekening geboekte bedragen worden teruggeboekt wanneer een inkooporderfactuur wordt geboekt. |
| Kosten van ingekocht gefactureerd materiaal | 140100 | Materiaalvoorraad | Activum | Debet | Nr. | Vr  |Kosten van ingekocht ontvangen materiaal | Gebruikt wanneer een inkooporderfactuur wordt geboekt. De verschuiving op deze rekening betreft de Inkoopuitgave voor product. Deze rekening vertegenwoordigt de voorraad op uw balans. De rekening die wordt gebruikt, is gewoonlijk dezelfde rekening die wordt gebruikt voor kosten van geleverde eenheden en kosten van eenheden die zijn gefactureerd voor een verkooporder. |
| Inkoopuitgave voor product | 600180 | Materiaalontvangstbon | Onkosten | Credit | Nr. | Vr  | |Gebruikt wanneer een inkooporderfactuur wordt geboekt. De verschuiving op deze rekening betreft de Kosten van ingekochte materialen. Deze rekening vertegenwoordigt de voorraad op uw balans. |
| Winstrekening vaste ontvangstprijs (Inkoop, winstrekening vaste ontvangstprijs*) | 510310 | Afwijking inkoopprijs | Onkosten | Credit | Nr. | Vr | Verliesrekening vaste ontvangstprijs | Gebruikt wanneer een inkooporderfactuur wordt geboekt en er een verschil is tussen de gefactureerde prijs en de standaardkosten voor het artikel. Deze rekening wordt gebruikt wanneer het verschil groter is. De verschuiving op deze rekening betreft Tegenrekening vaste ontvangstprijs. |
| Verliesrekening vaste ontvangstprijs (Inkoop, verliesrekening vaste ontvangstprijs*) | 510310 | Afwijking inkoopprijs | Onkosten | Debet | Nr. | Vr | Winstrekening vaste ontvangstprijs | Gebruikt wanneer een inkooporderfactuur wordt geboekt en er een verschil is tussen de gefactureerde prijs en de standaardkosten voor het artikel. Deze rekening wordt gebruikt wanneer het verschil kleiner is. De verschuiving op deze rekening betreft Tegenrekening vaste ontvangstprijs. |
| Tegenrekening vaste ontvangstprijs (Inkoop, tegenrekening vaste ontvangstprijs*) | 140900 | Voorraadwijziging | Activum | Beide | Nr. | Vr  | |Gebruikt wanneer een inkooporderfactuur wordt geboekt en er een verschil is tussen de gefactureerde prijs en de standaardkosten voor het artikel. Deze rekening is de verschuiving op de winst- en verliesrekeningen voor vaste ontvangstprijs. |
| Kosten | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. | N.v.t. | Deze rekening wordt niet meer gebruikt. Gebruik in plaats daarvan de voorraadwijziging. |
| Voorraadwijziging | 600170 | Voorraadwijziging | Onkosten | Credit | Nr. | Beide | | Deze rekening wordt gebruikt in de volgende gevallen: <ul><li>Als er een verschil is in de eenheidsprijs tussen de productontvangstbon en de factuur.</li><li>Als er toeslagen naar het artikel worden geboekt.</li><li>Als indirecte kosten zijn<!--note from editor: Edit okay?--> toegevoegd aan de ingekochte artikelen. </li><li>De verschuiving op deze rekening betreft Inkoopuitgave, niet-gefactureerd.</li></ul> |
| Inkoop, toerekening | 200140 | Transitorische aankopen | Aansprakelijkheid | Credit | Y | W | |Gebruikt wanneer een productontvangstbon van een inkooporder wordt geboekt en de optie voor toerekening van inkoopbedragen wordt ingeschakeld. |
| Transitorische btw bij ontvangst | 250500 | Toegerekende btw | Aansprakelijkheid | Credit | Y | Beide  | |Deze rekening wordt gebruikt wanneer u de optie **Fysieke btw boeken** selecteert op de pagina **Parameters voor voorraad- en magazijnbeheer** en u een inkooporder met btw hebt. Het bedrag wordt geboekt wanneer u de inkooporder fysiek (productontvangstbon) bijwerkt en wordt tegengeboekt wanneer u de inkooporder financieel (factuur) boekt. |
| Ontvangst van vaste activa (debetrekening van vaste activa*) | 180100 | Materiële vaste activa | Activum | Debet | N | Beide | Beide | Deze rekening wordt gebruikt wanneer u de optie selecteert op de inkooporderregel voor vaste activa. De integratie van de inkooporder is geconfigureerd om het vaste activum bij de productontvangstbon of -factuur aan te schaffen. Ga voor meer informatie over integratie van inkooporders voor vaste activa naar [Activa aanschaffen via inkoop](/fixed-assets/acquire-assets-procurement). |
| Inkoopuitgaven voor onkosten | 618900 | Diverse onkosten | Onkosten | Debet | N | Beide | |Gebruikt bij het boeken van een productontvangstbon of factuur voor een inkooporder waarvoor de artikelen niet op voorraad zijn of waarbij een inkoopcategorie wordt gebruikt. |
| Vooruitbetaling | 132190 | Vooruitbetaalde uitgaven | Activum | Debet | N | Beide | | Gebruikt bij het verwerken van een vooruitbetalingsfactuur op een inkooporder. |


\*Waarden die tussen haakjes worden weergegeven, staan voor de waarde die wordt gebruikt in het veld **Boekingstype** op de pagina **Boekstuktransacties**. U kunt het **Boekingstype** weergeven op de pagina **Boekstuktransacties** op het tabblad **Algemeen**.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Boeking van vaste activa met inkooporders

Als u de module **Vaste activa** gebruikt en van plan bent om vaste activa via inkooporders te kopen, moet u het boekingstype **Ontvangst van vaste activa** configureren op het tabblad **Inkooporder** van de pagina **Voorraadboekingsprofiel**. Ga voor meer informatie naar [Integratie van vaste activa](/fixed-assets/fixed-asset-integration.md) en [Activa maken en aanschaffen via Leveranciers](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Boeking van vooruitbetalingsfactuur voor inkooporders

Als u van plan bent om de functie **Vooruitbetalingsfactuur** te gebruiken voor inkooporders, moet het boekingstype **Vooruitbetaling** worden geselecteerd op het tabblad **Inkooporder** op de pagina **Voorraadboekingsprofiel**. Ga voor meer informatie naar [Vooruitbetalingsfacturen versus vooruitbetalingen](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Boeking van opdracht tot inkoop en bevestiging van inkooporder

Opdracht tot inkoop en inkooporderbevestigingen kunnen ook worden geconfigureerd om voorvorderingen en vorderingen naar het grootboek te boeken. Deze boekingen worden bepaald door een boekingsdefinitie. Ga voor meer informatie naar [Informatie over inkoopordervorderingen](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Boeking van inkoopcategorieën

Als alternatief voor het instellen van de voorraadboeking voor alle artikelen, een groep artikelen of één artikel kunt u categorieën instellen en de boeking in het grootboek beheren per inkoopcategorie. Ga naar [Voorbeeldboekingsprofielconfiguratie](#sample-posting-profile-configuration) eerder in dit onderwerp voor meer informatie over het instellen van categorieën en het toewijzen van categorieën aan producten.

Wanneer u categorieën gebruikt met inkooporders of leveranciersfacturen, moet de categoriehiërarchie worden toegewezen aan het type **Hiërarchie van inkoopcategorieën** op de pagina **Roltoewijzingen categoriehiërarchie**.

### <a name="vendor-invoices-with-procurement-categories"></a>Leveranciersfacturen met inkoopcategorieën

Als uw organisatie inkooporders gebruikt voor bepaalde aankopen en niet voor andere, kunt u facturen die betrekking hebben op niet-inkooporders op verschillende manieren verwerken. Dit omvat het gebruik van journalen in **Leveranciers** of door de pagina **Leveranciersfacturen in behandeling** die wordt gebruikt om facturen voor inkooporders te genereren. Wanneer u facturen maakt voor facturen die niet aan inkooporders zijn gerelateerd, moet u inkoopcategorieën maken voor elk type onkosten. U moet de categorie aan de juiste onkostenrekening toevoegen op de pagina **Voorraadboekingsprofielen**.

Het exacte aantal categorieën is afhankelijk van het aantal onkostenrekeningen dat u gebruikt om uw facturen te boeken. U hebt ten minste één inkoopcategorie nodig voor elke hoofdrekening waarbij u niet-inkooporderfacturen declareert. Er kunnen veel categorieën worden gebruikt voor één hoofdrekening. Dit kan nuttig zijn voor bruikbaarheid, doorzoekbaarheid en rapportage van de typen onkosten die u gebruikt.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Voordelen van het gebruik van inkoopcategorieën voor leveranciersfacturen

Sommige voordelen van het gebruik van inkoopcategorieën voor leveranciersfacturen zijn:

- Consistente gebruikerservaring: wanneer u inkoopcategorieën configureert voor alle onkosten die niet gerelateerd zijn aan inkooporders, kunnen gebruikers worden getraind in één factureringsproces met de pagina **Leveranciersfacturen in behandeling**.
- Verbeterde rapportage-ervaring: wanneer u inkoopcategorieën configureert voor alle onkosten die niet gerelateerd zijn aan inkooporders, analyseert het rapport voor inkoopuitgaven de uitgaven per leverancier, categorie en meer.
- Consistente werkstroom: wanneer u **Leveranciersfacturen in behandeling** gebruikt om alle facturen te verwerken, kunt u met behulp van één werkstroom een consistent werkstroom- en goedkeuringsproces maken.

## <a name="consignment-inventory-posting"></a>Boeking van consignatievoorraad

Bij consignatievoorraad wordt dezelfde grootboekboeking gebruikt als andere ingekochte artikelen. Het belangrijkste verschil is dat wanneer de voorraad wordt ontvangen, er geen grootboektransacties worden vastgelegd. Als u eigendom wilt overdragen naar de organisatie wanneer een journaal voor **Wijziging in voorraadeigendom** wordt geboekt, wordt een boekstuk gegenereerd om de kosten van het artikel vast te leggen. Ga naar [Consignatie instellen](/supply-chain/inventory/consignment.md) voor meer informatie.
