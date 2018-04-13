---
title: Overzicht van inkooporders
description: Dit artikel bevat algemene informatie over inkooporders (IO's) en koppelingen naar aanvullende artikelen die zijn gerelateerd aan de verschillende fasen die een IO doorloopt.
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ee9baefc95c24d23edca8438792c9648f77e1bdf
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-order-overview"></a>Overzicht van inkooporders

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

Dit artikel bevat algemene informatie over inkooporders (IO's) en koppelingen naar aanvullende artikelen die zijn gerelateerd aan de verschillende fasen die een IO doorloopt.

Een inkooporder (IO) is een document dat een overeenkomst met een leverancier voor het kopen van goederen of diensten vertegenwoordigt. Het document helpt ook bij het bijhouden van productontvangsten die plaatsvinden op basis van de order en, later, bij de administratieve afhandeling van facturen van leveranciers die de leverancier in rekening brengt op basis van de order.  

De pagina **Inkooporders** bevat een overzicht van de beschikbare orders en biedt u de mogelijkheid deze orders te wijzigen. Wanneer u een inkooporder opent, kunt u de **koptekstweergave** selecteren. Deze bevat gegevens die slechts één keer voor elke inkooporder worden opgegeven, zoals de details van de leverancier. U kunt ook de **regelweergave** selecteren, waarin u orderregels kunt wijzigen. Normaal gesproken schakelt u tussen deze twee weergaven terwijl u inkooporders wijzigt. Toeslagen worden niet rechtstreeks vermeld op de pagina **Inkooporders**, maar kunnen worden geopend via de menu's op de orderkoptekst en -regels.  

Er zijn vele rapporten waarin u informatie over inkooporders, productontvangstbonnen en leveranciersfacturen kunt bekijken. Deze rapporten zijn te vinden in de modules **Inkoop en sourcing** en **Leveranciers**.  

In de werkruimten **Voorbereiding van inkooporder** en **Inkooporderontvangst en opvolging** kunt u lijsten weergeven van inkooporders in de verschillende statussen die zij hebben bereikt. Zij bieden ook een overzicht van de acties die moeten worden uitgevoerd. De werkruimte **Voorbereiding van inkooporder** is gericht op het maken en bekijken van inkooporders, het verwerken van de order door middel van goedkeuring en het bevestigen hiervan bij de leverancier. Het werkgebied **Inkooporderontvangst en opvolging** is gericht op het verwerken van de ontvangst van goederen of diensten tegen inkooporders. Hier vindt u lijsten met overzichten van ontvangsten die achterstallig zijn, of die binnenkort moeten worden geleverd door de leverancier. Deze werkruimten worden niet gebruikt om de gerelateerde ontvangstactiviteiten uit te voeren die plaatsvinden in het magazijn. Deze activiteiten worden uitgevoerd met behulp van pagina's in de modules **Voorraadbeheer** en **Magazijnbeheer**. Verwerking van facturen van leveranciers moet worden uitgevoerd met behulp van de werkruimte **Leveranciersfactuurregistratie** en betalingen moeten worden gedaan met behulp van de werkruimte **Leveranciersbetalingen**.  

De volgende artikelen bieden een overzicht van de verschillende fasen die een inkooporder doorloopt:

-   [Inkooporder maken](purchase-order-creation.md)
-   [Goedkeuring en bevestiging van inkooporder](purchase-order-approval-confirmation.md)
-   [Productontvangst tegen inkooporders](product-receipt-against-purchase-orders.md)
-   [Overzicht van leveranciersfacturen](../../financials/accounts-payable/vendor-invoices-overview.md)

## <a name="types-of-purchase-orders"></a>Typen inkooporders
Er zijn drie typen inkooporders. Wanneer u een inkooporder maakt, moet u het type opgeven. U kunt een standaardordertype voor nieuwe orders instellen op de pagina **Parameters voor inkoop en sourcing**.

| Inkoopordertype        | Beschrijving                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Journaal        | Gebruik dit type om een conceptorder te maken. Dit type heeft geen effect op de voorradige hoeveelheden en genereert geen voorraadtransacties. De inkoopjournaalregels worden niet opgenomen in de hoofdplanning.                                                                                                       |
| Inkooporder | Gebruik dit type om inkooporders te maken wanneer orders worden bevestigd bij een leverancier en als de orders via ontvangst en facturering worden verwerkt voordat de leverancier is betaald. Dit type inkooporder komt het meeste voor.                                                                          |
| Geretourneerde order | Gebruik dit type wanneer u goederen naar de leverancier terugstuurt. Dit type order vereist dat u het RMA-nummer (autorisatie voor retournering van materiaal) opgeeft dat de leverancier u geeft. U geeft het RMA-nummer op het tabblad **Algemeen** van de inkooporder op. De oderregels moeten negatieve hoeveelheden hebben. |

## <a name="purchase-order-statuses"></a>Statussen van inkooporders
Inkooporders bevatten verschillende statusvelden die de voortgang van de order aangeven. Al deze velden worden weergegeven in de **koptekstweergave** van de order en een aantal hiervan zijn ook zichtbaar in het rasteroverzicht van alle orders. Het veld **Status** geeft de status voor hoeveelheden op de order weer. De volgende waarden zijn beschikbaar:

-   **Openstaande order** – Orders zijn gemaakt en hoeveelheden zijn besteld.
-   **Ontvangen** – Enkele van de hoeveelheden zijn ontvangen, maar ze zijn nog niet gefactureerd.
-   **Gefactureerd** – De volledige hoeveelheid op de order is gefactureerd. **Opmerking:** als een order *gedeeltelijk* is gefactureerd, is zowel de status **Ontvangen** als de status **Gefactureerd** passend. Daarom heeft de order nog steeds de status **Openstaande order**.
-   **Geannuleerd** – Een order is bevestigd, maar later geannuleerd. Daarom geeft deze status aan dat er niet langer geopende hoeveelheden voor de order zijn.

Het veld **Documentstatus** helpt u om snel de voortgang van de order te controleren in termen van documenten die zijn verwerkt. Het bevat de status van het meest recente document dat voor de order is voltooid. De volgende waarden zijn beschikbaar:

-   **Geen** – Er is nog geen document voor de order verwerkt.
-   **Inkooponderzoek** – Er is een inkooponderzoek gegenereerd en de order is in afwachting van feedback van de leverancier.
-   **Inkooporder** – De bevestiging van de order is verwerkt.
-   **Productontvangstbon** – De ontvangst van producten is verwerkt voor de order.
-   **Factuur** – Er is een factuur gemaakt voor de order.

Het veld **Goedkeuringsstatus** wordt gebruikt wanneer een inkooporder een controleproces of workflow doorloopt. De volgende waarden zijn beschikbaar:

-   **Concept**, **Wordt gecontroleerd** en **Afgewezen** – Deze statussen worden alleen gebruikt wanneer een goedkeuringsworkflow wordt gebruikt voor de inkooporder.
-   **Goedgekeurd** – Deze status is toegewezen aan orders die de goedkeuringsworkflow hebben voltooid. Orders die zijn gemaakt zonder gebruik van een goedkeuringsworkflow, krijgen onmiddellijk de status **Goedgekeurd**.
-   **Bij externe herziening** – dDeze status wordt gebruikt in scenario's waarin een inkooponderzoek is verzonden naar de leverancier, zodat de leverancier de voorwaarden van de inkooporder kan bevestigen. Deze status wordt ook gebruikt in het proces dat wordt geïnitieerd door de actie **Bevestigingsaanvraag**. De leverancier wordt bij dit proces gevraagd om voorwaarden van de inkooporder te bevestigen door verbinding met uw systeem en registratie van de bevestiging of afwijzing van de order.
-   **Bevestigd** – Deze status wordt toegekend nadat de order is bevestigd. Deze status is meestal de laatste goedkeuringsstatus die wordt toegewezen aan een order.


<a name="see-also"></a>Zie ook
--------

[Inkooporder maken](purchase-order-creation.md)

[Goedkeuring en bevestiging van inkooporder](purchase-order-approval-confirmation.md)

[Productontvangst tegen inkooporders](product-receipt-against-purchase-orders.md)

[Overzicht van leveranciersfacturen](../../financials/accounts-payable/vendor-invoices-overview.md)




