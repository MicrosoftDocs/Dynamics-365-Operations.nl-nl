---
title: Inkooporders maken
description: In dit artikel worden het proces en de opties voor het handmatig maken van een inkooporder beschreven.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20b8e00316b45126b028b6d9812a455ef0e53f19
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575507"
---
# <a name="create-purchase-orders"></a>Inkooporders maken

[!include [banner](../includes/banner.md)]

In dit artikel worden het proces en de opties voor het handmatig maken van een inkooporder beschreven.

Als u een inkooporder (IO) maakt, wordt algemene informatie over de gehele order opgegeven in de PO-koptekst, waarna u een of meer IO-regels kunt toevoegen. In dit artikel worden enkele van de meestgebruikte opties beschreven die beschikbaar zijn.  

U kunt ook IO's maken door regels te kopiëren vanuit een ander IO-document of een verkooporder. In dat geval kunt u het teken voor de voorraad omkeren, zoals u het teken op een factuur zou omkeren om aan te geven dat het om een creditering gaat.  

Hoewel u handmatig IO's kunt maken, worden deze meestal gegenereerd vanuit andere processen. Orders kunnen automatisch worden gemaakt op basis van andere documenten, zoals aanvragen. U kunt ze ook maken als onderdeel van het hoofdplanningsproces met behulp van de geplande inkooporders. Als u inkoopovereenkomsten gebruikt, kunt u inkooporders maken met de actie **Vrijgaveorder**. Er zijn ook meer geavanceerde methoden voor het automatisch maken van een inkooporder. Zo kunnen bijvoorbeeld ook orders worden gemaakt wanneer u ketens voor directe levering of intercompany-orderketens gebruikt.

## <a name="creating-a-purchase-order-header"></a>Een koptekst van een inkooporder maken
Wanneer u een nieuwe inkooporder maakt, verschijnt een dialoogvenster waarin u de meest voorkomende gegevens voor de IO-koptekst kunt invoeren. Wanneer u op **OK** klikt om het dialoogvenster te sluiten, wordt de order gemaakt en kunt u vervolgens extra informatie in de koptekst opgeven.  

Het eerste waaraan u moet denken bij het maken van een IO is het type order. Het type **Inkooporder** wordt het meeste gebruikt. Als echter een creditfactuur is vereist, kunt u het type **Geretourneerde order** gebruiken.  

U moet de leverancier opgeven in het veld **Leveranciersrekening**. Voor dit veld kunt u zoeken op de rekening of op de naam van de leverancier. Als een leverancier vanaf meerdere locaties levert, maar een enkele factuurrekening gebruikt, kunt u die factuurrekening selecteren in het veld **Factuurrekening** en vervolgens met andere leveranciersrekeningen gebruiken. Als u een inkooporder moet maken voor producten die niet herhaaldelijk zullen worden besteld, kunt u de optie **Eenmalige leverancier** gebruiken. Met deze optie wordt automatisch een nieuwe leveranciersrekening gemaakt die is gemarkeerd als eenmalige rekening, ter ondersteuning van een later clean-up-proces voor eenmalige rekeningen in de module **Leveranciers**. Wanneer u een leveranciersrekening selecteert, nemen veel velden in de koptekst van de inkooporder standaardwaarden over van de gegevens die zijn gekoppeld aan de leveranciersrekening. Zo worden bijvoorbeeld de standaardlocatie voor bezorging en het magazijn gekopieerd vanuit de leveranciersgegevens. U kunt deze standaardwaarden echter overschrijven als de aankoop is bestemd voor een andere locatie.  

Als de leverancier een referentienummer voor de order heeft verstrekt, kunt u deze informatie opnemen in het veld **Referentie van leverancier**. Voor geretourneerde orders moet u een waarde opgeven in het veld **RMA** om te verwijzen naar de toestemming van de leverancier voor het verwerken van de retourzending.  

Als een inkoopovereenkomst aan de order is gekoppeld, moet u deze informatie opgeven in het veld **Inkoopovereenkomst**.  

De IO-koptekst bevat ook informatie over toeslagen die van toepassing zijn op de gehele order in plaats van op afzonderlijke regels. Toeslagen kunnen automatisch worden toegevoegd aan de order als automatische toeslagen zijn ingesteld voor de leverancier of de toeslagengroep van de leverancier. U kunt toeslagen ook handmatig toevoegen aan de koptekst van de order door op **Toeslagen onderhouden** in het actievenster te klikken.

## <a name="adding-purchase-order-lines"></a>Inkooporderregels toevoegen
IO's kunnen bestemd zijn voor fysieke producten of voor services. Een instelling voor de voorraadmodelgroep bepaalt of een bepaald artikelnummer betrekking heeft op een product of een service. Gewoonlijk wordt het artikel dat wordt ingekocht bepaald door een artikelnummer. Echter, als de order voor producten of diensten is die rechtstreeks worden verbruikt, kunt u ook het artikel opgeven via een inkoopcategorie.  

Inkooporderregels bevatten een groot aantal velden, maar veel van deze velden hebben een standaardwaarde of een waarde die is overgenomen uit de orderkoptekst. Extra velden worden ingesteld bij selectie van een product of dienst. Tot de velden die het meest handmatig worden ingesteld behoren de velden voor artikelnummer, aantal en aangevraagde leveringsdatum. Informatie over prijs per eenheid en kortingen is eveneens erg belangrijk, maar de waarden van deze velden worden vaak bepaald door handelsovereenkomsten of inkoopovereenkomsten.  

Wanneer u een product selecteert, kunt u zoeken op volledige of gedeeltelijke productnaam in plaats van het artikelnummer te gebruiken. Als het product verschillende varianten heeft, zoals verschillende formaten, kunt u een overzicht van de beschikbare varianten bekijken met behulp van de functie **Regels toevoegen** of via de zoekactie die beschikbaar is in het veld **Variantnummer**.  

Vaak moet u verschillende dimensies opgeven voor het artikel dat is geselecteerd op elke inkooporderregel. De dimensies die moeten worden opgegeven, zijn afhankelijk van de dimensiegroepen die zijn toegewezen aan de productmodeldefinitie. Zo zult y bijvoorbeeld vaak een locatie en magazijn moeten opgeven om de locatie aan te geven waar het product moet worden afgeleverd. U identificeert productvarianten door een variantnummer op te geven of door waarden in te voeren voor een of meer productdimensies, zoals kleur, formaat, configuratie of stijl. Via traceringsdimensies, zoals batch- en serienummer, kunt u elke voorraadpartij uniek identificeren. Nadat u een order hebt gemaakt, kunt u de dimensiewaarden voor de order vastleggen met behulp van de actie **Registratie**. Stel bijvoorbeeld dat u een aantal van vijf stuks van een artikel hebt besteld. Later legt u vast dat drie van deze stukken zwart moeten zijn en twee blauw. Deze benadering is een alternatief voor het vastleggen van dimensiegegevens tijdens de aankomstregistratie.  

U kunt de details van de voorraadtransactiestatus voor voorraadproducten controleren. Zo wilt u bijvoorbeeld wellicht de voorhanden voorraad controleren om u te helpen beslissen hoeveel u moet bestellen. Ook wilt u mogelijk de voorraadstatus van een bestelde hoeveelheid controleren om te zien of binnenkomende aankomstregistratie heeft plaatsgevonden.  

Een inkooporderregel die wordt gebruikt voor het retourneren van een product aan de leverancier heeft een negatieve hoeveelheid. U kunt een specifieke partij selecteren voor retourzending door de actie **Reservering** te gebruiken.  

Soms wilt u mogelijk de hoeveelheid die u hebt besteld opsplitsen, zodat verschillende delen ervan op verschillende datums worden geleverd. U kunt deze leveringen instellen met behulp van de actie **Afleveringsschema**, die beschikbaar is in het menu **Inkooporderregel** in de weergave **Regels**.  

Toeslagen kunnen automatisch worden toegevoegd aan inkooporderregels als automatische toeslagen zijn ingesteld voor de leverancier of de toeslagengroep van de leverancier, en voor het artikel of de toeslaggroep van het artikel. Meestal worden toeslagen echter handmatig toegevoegd op het niveau van de orderregel. U kunt een toeslag toevoegen door de pagina **Toeslagen onderhouden** te openen met de actie **Toeslagen onderhouden** in het menu **Financiële items** in de weergave **Regels**. Het voordeel van het toevoegen van toeslagen rechtstreeks op het niveau van de orderregel is dat de toeslag kan worden toegewezen als voorraadkosten. U kunt toeslagcodes instellen voor productkosten door de debetoptie **Artikel** te gebruiken. Dit soort toeslagen moet worden toegewezen vanuit de IO-koptekst aan de regels voordat de order kan worden bevestigd. Zo wilt u bijvoorbeeld mogelijk toeslagen toewijzen op basis van de hoeveelheid op elke regel. De toeslagcategorie heeft eveneens invloed op hoe de toeslagen worden verwerkt. Bij vaste toeslagen, bijvoorbeeld, geeft u een vast bedrag op en procentuele toeslagen worden berekend als een percentage van het nettobedrag voor de orderregel. Inkooporders kunnen worden toegewezen aan een belasting en de belasting kan een schatting bevatten van de verwachte kosten voor het vervoer. U kunt deze onkosten vanuit de belasting terug aan de regels toewijzen.

## <a name="purchase-order-actions"></a>Inkooporderacties
Nadat u de koptekst en regels aan de inkooporder hebt toegevoegd, moet u vaak extra stappen voltooien voordat de order klaar is voor bevestiging. Omdat er zoveel opties beschikbaar zijn, vindt u het misschien handig om [Actie zoeken](../../fin-ops-core/fin-ops/get-started/action-search.md) te gebruiken om het gewenste menu-item te zoeken.  

U kunt producten op de order zodanig configureren dat zij bijkomende artikelen hebben. Bijkomende artikelen zijn producten die samen met andere producten moeten of kunnen worden gekocht. Bijkomende producten kunnen gratis worden toegevoegd als begeleidende producten, of u kunt zelf beslissen of u ze wilt toevoegen aan de order of niet. U kunt de bijkomende artikelen bekijken na elke orderregel die is toegevoegd. Waarschijnlijk vindt u het echter handiger om relevante bijkomende artikelen te controleren en toe te voegen voor alle orderregels via de pagina **Bijkomende artikelen**, die u vanuit het actievenster kunt openen.  

Kortingen worden meestal toegevoegd aan regels zodra zij zijn gemaakt. Een paar kortingen gelden echter voor de gehele order:

-   De actie **Totale korting** berekent het totale kortingspercentage dat wordt toegepast op de volledige order. Verwar deze korting niet met het percentage van de korting voor contante betaling. Contantkortingen worden toegepast wanneer de factuur wordt betaald en zijn afhankelijk van de betalingsvereffening vóór een specifieke datum.
-   Als een korting voor meerdere regels van toepassing is, moet u de actie **Meerregelkorting** gebruiken om deze te berekenen en toe te wijzen aan de order. Meerregelkortingen zijn kortingen die kunnen worden aangeboden als een mix van producten op de order een gezamenlijke drempelwaarde overschrijdt. Slechts enkele bedrijven gebruiken dit soort korting.

Toeslagen die een toeslagcode hebben die gebruikmaakt van het debettype **artikel** moeten worden toegewezen aan het regelniveau voordat de order kan worden bevestigd. Mogelijk vindt u het handig om deze toeslagen toe te wijzen op het niveau van de koptekst, zodat u het totale bedrag van de toeslag kunt opgeven. In dat geval moet de toeslag echter vervolgens worden toegewezen aan elke regel voordat de order kan worden bevestigd. U kunt de actie **Toeslagen toewijzen** gebruiken om bedragen van toeslagen die zijn toegewezen op het koptekstniveau te verdelen over de orderregels. Toeslagen kunnen worden opgesplitst op basis van het nettobedrag van elke regel, afhankelijk van de hoeveelheid die is besteld of gelijkmatig verdeeld over de orderregels. Nadat u toeslagen aan de regels hebt toegewezen, wordt de toeslag verwijderd uit de orderkop.  

Inkooporders kunnen zodanig worden geconfigureerd dat budgetfondsen moeten worden toegewezen aan de order voordat deze kan worden verwerkt. In dat geval kunt u de actie **Budgetcontrole** gebruiken om het budget toe te wijzen.  

Mogelijk moet u de voltooiing van een inkooporder uitstellen. Zo hebt u bijvoorbeeld mogelijk meer informatie nodig over producten of diensten of hebt u toestemming voor de besteding nodig. Er zijn verschillende manieren om een order te vertragen. Zo kunt u bijvoorbeeld wachten met het bevestigen van de bestelling. Ook kunt u, als een werkstroom voor wijzigingsbeheer wordt gebruikt, de order niet indienen voor goedkeuring. Als u alle orders voor een bepaalde leverancier moet blokkeren, kunt u ook de leverancier markeren als **In wachtstand** voor verwerking in het leveranciermodel. Er zijn tevens omstandigheden die mogelijk de verwerking van de order kunnen voorkomen. Zo kan bijvoorbeeld de verwerking worden voorkomen als de kredietlimieten zijn overschreden of als vereiste budgetfondsen niet beschikbaar zijn.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van inkooporders](purchase-order-overview.md)

[Inkooporders goedkeuren en bevestigen](purchase-order-approval-confirmation.md)

[Productontvangst tegen inkooporders](product-receipt-against-purchase-orders.md)

[Overzicht van Leveranciersfacturen](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]