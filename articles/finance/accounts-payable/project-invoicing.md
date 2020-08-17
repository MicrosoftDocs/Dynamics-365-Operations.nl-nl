---
title: Projectfacturering
description: Dit onderwerp biedt een overzicht van projectfacturen voor tijd- en materiaalprojecten en projecten met een vaste prijs. Het bevat informatie over factuurvoorstellen (voorlopige facturen), factuurbeheer, a conto-facturering, leveranciersfacturering en creditnota's.
author: TaylorVH
manager: AnnBe
ms.date: 07/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2020-07-06
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: eab7523296996709dfe7407c582e61e28b7d4f23
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651587"
---
# <a name="project-invoicing"></a>Projectfacturering

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van projectfacturen voor tijd- en materiaalprojecten en projecten met een vaste prijs. Het bevat informatie over factuurvoorstellen (voorlopige facturen), factuurbeheer, a conto-facturering, leveranciersfacturering en creditnota's.

Aan de hand van het projecttype wordt bepaald welke factureringsmethode moet worden toegepast. Alleen de twee externe projecttypen, Tijd en materiaal en Vaste prijs, kunnen worden gefactureerd. Tijd- en materiaalprojecten en Projecten met een vaste prijs zijn altijd aan een projectcontract gekoppeld.

-   **Projecten met een vaste prijs**: het bedrag van de klantfactuur is gebaseerd op factureringsschema's. Facturering wordt uitgevoerd via een a conto-instelling, ook wel een factureringsschema genoemd. Projecten met een vaste prijs kunnen per project of per projectcontract worden gefactureerd.
-   **Tijd- en materiaalprojecten**: het bedrag van de klantfactuur is gebaseerd op transactieregels die voor projecten zijn ingevoerd. Transacties kunnen per project of per projectcontract worden gefactureerd.

Er zijn drie manieren om Tijd- en materiaalprojecten en Projecten met een vaste prijs te koppelen aan de factuurprojecten:

-   **A conto-facturering**: Tijd- en materiaalprojecten en Projecten met een vaste prijs kunnen op rekening worden gefactureerd. Voor elk projecttype zijn twee verschillende a conto-instellingen vereist.
-   **Facturering in de sectie periodiek**: via de periodieke functies kunnen transacties in projecten worden gefactureerd. De periodieke functies geven een overzicht van transacties die moeten worden gefactureerd.
-   **Door creditnota's in de facturering te gebruiken**: voor zowel tijd- en materiaalprojecten als projecten met een vaste prijs kan een creditnota worden gemaakt.

## <a name="invoice-proposals"></a>Factuurvoorstellen
Voordat u een klantfactuur voor een project maakt, kunt u een voorlopige factuur of factuurvoorstel maken. In een factuurvoorstel kunt u projecttransacties selecteren die in een projectfactuur moeten worden opgenomen. U kunt de factuurdetails vervolgens controleren voordat u de projectfactuur boekt en het naar de klant of andere financieringsbron verstuurt.

### <a name="creating-invoice-proposals"></a>Factuurvoorstellen maken

U kunt factuurvoorstellen maken door handmatig een transactie te kiezen uit een lijst met beschikbare transacties voor een opgegeven project. U kunt tevens factureringsregels instellen die opgeven wanneer automatisch een factuurvoorstel wordt gemaakt. U kunt bijvoorbeeld een factureringsregel maken om een factuurvoorstel te maken wanneer het werk aan een project 25 procent, 50 procent, 75 procent, en 100 procent is voltooid. 

U kunt factuurvoorstellen maken voor de volgende transacties:

-   Uren, onkosten en andere projecttransacties
-   Bedragen die door klanten op eerdere projectfacturen zijn ingehouden.
-   Creditnota's
-   Bedragen die een klant aan u heeft betaald voordat een project wordt gestart.

> [!NOTE]
> Met de functie **Sorteren op resources inschakelen tijdens het maken van een projectfactuurvoorstel** kan de projectaccountant bij het maken van een nieuw projectfactuurvoorstel de projecttransacties die beschikbaar zijn voor facturering op resource sorteren. Het raster waarin de beschikbare projecttransacties worden weergegeven, bevat verschillende velden voor **Resource-id** en **Resource**. Met deze velden kunt u filteren en sorteren op de resourcenaam. Standaard is deze optie uitgeschakeld. De functie kan worden ingeschakeld via de pagina **Functiebeheer** (**Werkruimten > Functiebeheer**). Neem contact op met uw systeembeheerder voor hulp bij het inschakelen van deze functie.

U kunt kostentransacties in een factuurvoorstel maken. U kunt ook de verkoopprijs wijzigen voor uur-, onkosten-, artikel- en bijzondere-kostentransacties. Als u een factuurvoorstel boekt, worden de bijgewerkte prijzen en transacties toegevoegd aan projectrapporten en de transactiehistorie. 

Als u meerdere klantfacturen wilt maken voor een project, moet u een factuurvoorstel maken voor elke factuur. U kunt bijvoorbeeld, facturen maken op basis van transactietype. Als u uren op één klantfactuur wilt opgeven en artikelen op een andere, moet u afzonderlijke factuurvoorstellen maken voor uurtransacties en kostentransacties. 

U kunt een afzonderlijk factuurvoorstel maken voor elke financieringsbron als een project meer dan één financieringsbron heeft. Op de pagina **Toewijzingen financieringsregels** kunt u het percentage definiëren van het transactiebedrag dat moet worden toegewezen aan elke financieringsbron, en u kunt de bron definiëren waarnaar afrondingsverschillen worden geboekt.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Klantfacturen maken van factuurvoorstellen

Wanneer u een factuurvoorstel maakt en boekt, wordt automatisch een klantfactuur gemaakt voor de transacties die zijn opgenomen in het factuurvoorstel. 

Voordat u een factuurvoorstel boekt, kunt u er transacties aan toevoegen of er transacties uit verwijderen. U kunt bijvoorbeeld onkostentransacties verwijderen die naar een project zijn geboekt maar niet aan de klant kunnen worden aangerekend. 

Als uw organisatie vereist dat factuurvoorstellen worden gecontroleerd voordat ze worden geboekt, moet u het factuurvoorstel mogelijk goedkeuren via de werkstroom 'Projectfactuurvoorstellen controleren' voordat u deze boekt.

### <a name="view-grant-information-on-project-invoice-list-pages"></a>Subsidiegegevens weergeven op de projectfactuurlijstpagina's

Gebruikers in de publieke sector kunnen de **subsidie-id** en de **subsidienaam** toevoegen aan de lijstpagina's **Projectfactuurvoorstellen** en **Projectfacturen**. Deze kolommen worden ingeschakeld met de functie **Subsidiegegevens toevoegen aan lijstpagina's met projectfacturen**. Deze functie is standaard uitgeschakeld en kan worden ingeschakeld in **Werkgebieden > Functiebeheer**. Neem contact op met uw systeembeheerder voor hulp bij het inschakelen van deze functie.

## <a name="on-account-invoicing"></a>Facturering op rekening
Het bedrag dat u op een a conto-factuur invoert voor een project, hangt af van de uren, het voltooiingspercentage en andere factuurvoorwaarden die in het bijbehorende projectcontract zijn gespecificeerd. Het bedrag wordt niet berekend op basis van de uren, artikelen, kosten of toeslagen die voor een project worden geboekt. 

U moet u eerst een op rekening-transactie maken voor een tijd- en materiaalproject of een project met een vaste prijs voordat u die op rekening-transactie aan een projectfactuur kunt toevoegen. Voer op de a conto-transactie het bedrag in dat aan een klant moet worden gefactureerd. Om een projectfactuur te maken voor het bedrag maakt u een voorlopige factuur (factuurvoorstel). Selecteer in het factuurvoorstel de a conto-transactie. U kunt de a-conto-informatie bekijken in het factuurvoorstel voordat u er een projectfactuur voor maakt. 

### <a name="fixed-price-projects"></a>Projecten met een vaste prijs
Voor projecten met een vaste prijs, worden a conto transacties gebaseerd op een vooraf overeengekomen mijlpaal, een leveringseenheid, of een facturering naar rato van voortgang zoals bepaald in een projectcontract. Er wordt één regel gemaakt voor elke betaling die van de projectklant moet worden ontvangen. Geen inhoudingen vereist.

### <a name="time-and-material-projects"></a>Tijd- en materiaalprojecten

Voor tijd- en materiaalprojecten, kunt u aan een klant of een andere financieringsbron een vooruitbetalingsbedrag factureren met een a conto-factuurvoorstel. A conto-transacties invoeren als een regel. U kunt desgewenst extra regels invoeren als inhoudingen om vooruitbetalingen van de klant te compenseren. Om inhoudingsregels te maken voert u vóór het bedrag een minteken in.

## <a name="invoice-control"></a>Factuurbeheer
Met factuurbeheer kunt u zowel gefactureerde als niet-gefactureerde transacties volgen en die transacties analyseren met behulp van offertes zodat u een beeld krijgt van het verloop van uw projecten, vanaf de offerte tot aan voltooiing. U kunt zien welke transacties naar een bepaald project zijn geladen en welke regels zijn gefactureerd. Het is ook mogelijk om de afzonderlijke transacties weer te geven zodat u deze kunt corrigeren nadat ze zijn geboekt.

## <a name="invoicing-fixed-price-projects"></a>Projecten met een vaste prijs factureren
Om Projecten met een vaste prijs te factureren moet u een factureringsschema definiëren en de factureringsprocedure voltooien.

### <a name="billing-schedule"></a>Factureringsplanning

U kunt projecten met een vaste prijs factureren op een factureringsschema. Het factureringsschema wordt gedefinieerd in de vorm van één of meer mijlpalen voor het project. Voor elke mijlpaal kunt u een specifieke datum, verkoopvaluta, een verkoopprijs en activiteit definiëren. 

U kunt bijvoorbeeld het volgende factureringsschema instellen:

-   20 procent wanneer het projectcontract wordt ondertekend
-   30 procent na de eerste levering
-   15 procent na de tweede levering
-   35 procent na de laatste levering

### <a name="invoicing-procedure"></a>Factureringsprocedure

Wanneer de mijlpaalbetalingen kunnen worden gefactureerd, gebruikt u de procedure voor de facturering van op rekening-bedragen.

## <a name="vendor-invoicing"></a>Leveranciersfacturering
Wanneer u een artikel van een leverancier bestelt en het artikel aan een project toewijst, bepaalt de eigenschap die u voor de inkooporderregel voor dat artikel selecteert of het ingekochte artikel aan een klant wordt gefactureerd. Als u standaardregeleigenschappen instelt, worden deze weergegeven voor het artikel op de inkooporderregel (**Regeldetails > Project > Bedragen van regeleigenschap**). Er zijn twee manieren om de regeleigenschap te wijzigen:

-   De klant van het project voor het artikel factureren. Hiervoor stelt u de regeleigenschap voor het artikel in op een toerekenbare waarde op de inkooporder en factureert u vervolgens de klant door de juiste projectfactureringsmethode te gebruiken.
-   De klant van het project niet voor het artikel factureren. Hiertoe selecteert u niet de regeleigenschap **Toerekenbaar** op de inkooporderregel voor het artikel. U kunt de inkooporder vervolgens factureren en verder hoeft u niets te doen.

> [!NOTE] 
> Het vrijgeven van inhoudingsregels is standaard niet-toerekenbaar. Dit betekent dat de mogelijkheid om een factuurvoorstel te maken voor de vrijgegeven inhouding niet is ingeschakeld.

## <a name="credit-notes"></a>Creditnota's
Als een bedrag op een klantfactuur een negatieve waarde heeft, wordt de factuur geclassificeerd als creditnota. Wanneer het document wordt afgedrukt, heeft het de titel "Creditnota". 

Als u een creditnota maakt om een bedrag te crediteren dat eerder is gefactureerd, moet u dit bedrag eerst voor creditering selecteren. Vervolgens maakt u een creditnota. Hiervoor geldt dezelfde procedure als voor het maken van een gewone klantfactuur. U selecteert dus de transacties die eerder op een klantfactuur zijn geboekt en maakt en boekt vervolgens een creditnotavoorstel. 

Hetzelfde document kan transacties bevatten die zijn geselecteerd voor creditering, credittransacties en transacties die zijn geboekt. Afhankelijk van of het totale bedrag positief of negatief is, wordt het document geclassificeerd als een factuur of creditnota. 

Als u een gefactureerd bedrag wilt crediteren, moet u dit bedrag eerst voor creditering selecteren en vervolgens een creditnota maken. U maakt een creditnota met dezelfde methode als voor het maken van een klantfactuur. 

U kunt een klantfactuur met een negatieve waarde maken. Dit wordt een factuur die wordt geclassificeerd als creditnota. Om een creditnota te maken en af te drukken moet u de transacties selecteren die eerder voor een klantfactuur zijn geboekt en vervolgens de transacties bewerken. Tenzij het primaire adres van de rechtspersoon Duitsland is, wordt de titel van de factuur "Correctiefactuur".



