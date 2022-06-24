---
title: Veelgestelde vragen over de kostprijsberekening van voorraad
description: In dit artikel worden antwoorden op enkele veelgestelde vragen over de kostprijsberekening van voorraad in Microsoft Dynamics 365 Supply Chain Management gegeven.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 467839b1d0ca6788a92ae60d46686374d0a58046
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850839"
---
# <a name="inventory-costing-faq"></a>Veelgestelde vragen over de kostprijsberekening van voorraad

[!include [banner](../includes/banner.md)]

In dit artikel worden antwoorden op enkele veelgestelde vragen over de kostprijsberekening van voorraad in Microsoft Dynamics 365 Supply Chain Management gegeven.

## <a name="inventory-close-adjustments-and-recalculation"></a>Afsluiting, aanpassingen en herberekening van voorraad

### <a name="is-the-inventory-close-required"></a>Is voorraadafsluiting verplicht?

Als u de functie voor het archiveren van voorraden wilt gebruiken, is het noodzakelijk dat de voorraad wordt afgesloten. Ook als u de voorraadarchiveringsfunctie niet wilt gebruiken, raden we u sterk aan de voorraad af te sluiten, ongeacht de kostprijsberekeningsmodellen die u gebruikt.

### <a name="how-often-should-the-inventory-close-be-run"></a>Hoe vaak moet de voorraad worden afgesloten?

De voorraadafsluiting moet minimaal één keer per grootboekperiode worden afgesloten. Als uw grootboek bijvoorbeeld is ingesteld op een op kalendermaanden gebaseerde fiscale kalender, moet u de voorraad eenmaal per maand afsluiten.

### <a name="is-the-inventory-recalculation-required"></a>Is voorraadherberekening verplicht?

Nee, de voorraadherberekening is niet verplicht. Als u een periodiek kostprijsberekeningsmodel gebruikt, zoals FIFO (First In, First Out), LIFO (Last In, First Out) of gewogen gemiddelde, moet u zorgvuldig overwegen of u de voorraad opnieuw wilt berekenen. Het kan een nauwkeurigere kostprijsberekening bieden in de geselecteerde heuristische modellen.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Hoe vaak moet de voorraad opnieuw worden berekend?

Als u van plan bent om de voorraad opnieuw te berekenen, raden we u aan om deze dagelijks uit te voeren als batchproces. Als uw organisatie niet vaak de voorraadwaarden hoeft te rapporteren voor periodieke kostprijsberekeningsmodellen, kunt u overwegen de voorraadberekening minder vaak uit te voeren.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Wanneer moet ik de correctie van voorhanden voorraad op de pagina Afsluiten en corrigeren gebruiken?

De correctie van voorhanden voorraad kan alleen worden uitgevoerd nadat een voorraadafsluiting is voltooid. Deze wordt meestal uitgevoerd voor de datum na de laatste afsluiting. Met de voorhanden correctie kan alleen voorraad worden aangepast die op de datum waarop u de correctie uitvoert nog voorhanden is.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Wanneer moet ik de correctie van de voorraadtransactie op de pagina Afsluiten en corrigeren gebruiken?

U moet de voorraadtransactiecorrectie gebruiken voordat u een voorraadafsluiting uitvoert. Deze wordt meestal gebruikt om een onjuiste ontvangst te corrigeren. U kunt de voorraadtransactiecorrectie niet meer boeken nadat een voorraadafsluiting is uitgevoerd en de transactie is vereffend.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Worden retouren van inkooporders op dezelfde manier behandeld als andere uitgiften tijdens de voorraadafsluiting?

Ja. Een inkooporderontvangst is een uitgifte die wordt vereffend met een ontvangst in het heuristische model dat u voor het artikel selecteert. Als u een periodiek kostprijsberekeningsmodel gebruikt, kunt u een markering gebruiken om de heuristische kosten te overschrijven.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Wat gebeurt er met verkooporderretouren tijdens de voorraadafsluiting?

Wanneer u de voorraadafsluiting uitvoert, wordt een retour van een verkooporder behandeld als ontvangst in de voorraad. Uitgiften worden vereffend met de voorraad, op basis van het heuristische model dat u voor het artikel selecteert.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Welke kostprijs wordt gebruikt voor een verkooporderretour?

Wanneer u een retour maakt die is gerelateerd aan een verkooporder, wordt de waarde van het veld **Eenheidsprijs** gekopieerd vanuit de oorspronkelijke verkooporder en wordt het veld **Kostprijs retour** van de retour ingesteld op de gecorrigeerde kostprijs van de oorspronkelijke voorraadtransactie voor de verkooporderregel die wordt geretourneerd. Als de optie **Openstaande waarde** voor de gerelateerde voorraadtransactie is ingesteld op *Ja*, kan de voorraadafsluiting ertoe leiden dat de uitgiftekosten voor de oorspronkelijke verkooporder worden bijgewerkt. Het veld **Kostprijs retour** wordt niet bijgewerkt in dit scenario. Wanneer u echter een pakbon voor een retourorder maakt, controleert het systeem de kostprijs en gebruikt het de bijgewerkte kosten voor de retourvoorraadtransactie.

Voor het retourneren van een standaardkostenartikel dat is gerelateerd aan een verkooporder, gebruikt het systeem de standaardkosten van het tijdstip van de oorspronkelijke verkooporder, zelfs als er nieuwe standaardkosten actief zijn voor het artikel.

Wanneer u een retour maakt die geen verband houdt met een verkooporder, wordt het veld **Kostprijs retour** ingesteld op de actieve artikelprijs voor het artikel op de locatie waarvoor u de retourorder maakt. Als u geen actieve kostprijs hebt in een kostprijsversie voor het artikel, is de waarde 0 (nul). Als u de waarde op 0 (nul) laat staan, ontvangt u een waarschuwing waarin wordt aangegeven dat de retourpartij-id of kostprijs niet is opgegeven.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Wat zijn de verwachte prestaties van de voorraadafsluiting?

Een groot aantal factoren kan invloed hebben op de prestaties van de voorraadafsluiting. Deze factoren omvatten het totale aantal artikelen, het totale aantal transacties in de periode, de voorraadmodellen die u gebruikt en het aantal batchhelpers dat u configureert in de voorraad- en magazijnbeheerparameters. Houd er rekening mee dat de afsluiting enkele minuten tot meerdere uren in beslag kan nemen. Er is geen specifieke richtlijn voor de tijd die de uitvoering van de afsluiting moet kosten. U moet de niet-functionele zakelijke vereisten definiëren voor de prestaties van de voorraadafsluiting en nauw samenwerken met uw partner om de planning voor het uitvoeren van het voorraadafsluitingsproces te definiëren. Als u te maken krijgt met een onverwacht lage prestaties van het voorraadafsluitingsproces, moet u een ondersteuningsticket openen.

## <a name="costing-sheet-and-indirect-costs"></a>Kostenblad en indirecte kosten

### <a name="which-costing-models-support-the-costing-sheet"></a>Welke kostprijsberekeningsmodellen ondersteunen het kostenblad?

Hoewel het kostenblad het meest wordt gebruikt in organisaties die standaardkostprijsberekeningen gebruiken, kunt u het gebruiken met elk kostprijsberekeningsmodel dat beschikbaar is in Supply Chain Management.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Kan ik meerdere kostenbladen hebben voor verschillende delen van mijn organisatie?

Nummer U kunt slechts één kostenblad per rechtspersoon hebben.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Kan ik verschillende kostenbladen voor elke locatie hebben?

Nee, u kunt geen verschillende kostenbladen voor elke locatie hebben. U kunt slechts één kostenblad voor elke rechtspersoon maken. U kunt echter wel het totale aantal knooppunten, kostengroepen of indirecte kostenknooppunten per locatie configureren. Deze configuratie is een handmatig proces en u moet de hiërarchie en artikeltoewijzingen op het kostenblad aanhouden wanneer er organisatorische of operationele wijzigingen plaatsvinden. Als een enkel artikel op meerdere locaties wordt geproduceerd of ingekocht, is er geen mechanisme waarmee u het artikel op de kostenblad voor elke locatie anders kunt behandelen. Houd er rekening mee dat voor alle codes voor indirecte kosten een tarief of toeslag is gedefinieerd in uw kostprijsversie. De kosten die u definieert, zijn altijd locatiespecifiek.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Kan ik versies van het kostenblad deactiveren en activeren?

Hoewel er geen uitgebreide versiegeschiedenis voor het kostenblad wordt bijgehouden, kunt u wijzigingen aanbrengen in het kostenblad en deze vervolgens opslaan en valideren wanneer u klaar bent. Er is geen mechanisme waarmee u kunt teruggaan naar een oudere versie van het kostenblad of de wijzigingen kunt bekijken die in het kostenblad zijn aangebracht. Als u wijzigingen aanbrengt die u vervolgens niet wilt doorvoeren, kunt u de pagina sluiten zonder de wijzigingen op te slaan en te valideren. U wordt dan gevraagd of u de wijzigingen wilt negeren.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Kan ik indirecte kosten maken voor elk artikel?

In het kostenblad kunt u code voor indirecte kosten maken waarbij het veld **Type knooppunt** is ingesteld op *Toeslag*, *Tarief* of *Op basis van uitvoereenheid*. U kunt vervolgens het tarief of de toeslag definiëren voor een specifiek artikelnummer. Voeg op het sneltabblad **Tarief** of **Toeslag** een rij toe aan het raster. Stel het veld **Geldig voor** in op *Tabel* en geef in het veld **Relatie** het specifieke artikelnummer op.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Kan ik indirecte kosten maken die geen verband houden met een bepaald artikel?

Ja. U kunt een code voor indirecte kosten maken waarbij het veld **Type knooppunt** is ingesteld op *Op basis van uitvoereenheid*. U kunt vervolgens het veld **Subtype** instellen op *Hoeveelheid*, *Gewicht* of *Volume* om de hoeveelheid, het gewicht of het volume op te geven van het artikel dat u produceert. Het tarief dat u opgeeft op het sneltabblad **Tarief** wordt toegepast op het subtype dat u hebt geselecteerd. Stel bijvoorbeeld het veld **Subtype** in op *Hoeveelheid* en **Tarief** op *1,00 USD* en maak vervolgens een productie- of batchorder voor een hoeveelheid van 10. In dit geval wordt 10,00 USD als indirecte kosten toegevoegd aan het eindproduct.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Kan ik het kostenblad gebruiken om mijn productiekosten te splitsen in uren en materialen?

Ja. U kunt knooppunten **Totaal** in uw kostenblad maken om de kosten te scheiden op basis van elke gewenste groepering. U kunt bijvoorbeeld één knooppunt **Totaal** met de naam *Uur* maken en een ander knooppunt met de naam *Materialen*. Voeg onder het knooppunt **Uur** elke codegroep toe die aan uw uren is gerelateerd. Voeg onder het knooppunt **Materialen** elke kostengroep toe die aan uw materialen is gerelateerd.

## <a name="dimension-groups"></a>Dimensiegroepen

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Kan ik kosten beheren op batch- of serienummerniveau?

Ja, als u een periodiek kostprijsberekeningsmodel gebruikt, zoals FIFO, LIFO, LIFO-datum, gewogen gemiddelde of datum gewogen gemiddelde, kunt u de optie **Financiële voorraad** voor de dimensie **Batchnummer** of **Serienummer** in de traceringsdimensiegroep inschakelen om kosten op een gedetailleerd niveau bij te houden.

### <a name="can-i-manage-costs-at-the-location-level"></a>Kan ik kosten beheren op locatieniveau?

Nee, u kunt de optie **Financiële voorraad** niet inschakelen voor de dimensie **Locatie** in de opslagdimensiegroep. Als uw organisatie kosten gedetailleerder moet bijhouden, kunt u overwegen of u virtuele magazijnen kunt maken en vervolgens de optie **Financiële voorraad** selecteren voor de dimensie **Magazijn** in de opslagdimensiegroep.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Moet ik de optie Magazijnbeheerprocessen gebruiken inschakelen voor de opslagdimensiegroep?

Als u de geavanceerde magazijnbeheerfuncties in de toekomst wilt gebruiken, moet u de optie **Magazijnbeheerprocessen gebruiken** inschakelen. Nadat u een opslagdimensiegroep hebt opgeslagen, kunt u de instelling van de optie **Magazijnbeheerprocessen gebruiken** niet meer wijzigen. Als u later de processen voor magazijnbeheer wilt gebruiken, moet u een nieuw magazijn maken waarvoor de optie is ingeschakeld. Er is geen geautomatiseerd proces dat u kunt gebruiken om alle voorraad van het ene magazijn naar het andere magazijn te verplaatsen of om gerelateerde configuraties naar een nieuw magazijn te kopiëren.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Kan ik de magazijnbeheerprocessen voor de opslagdimensiegroep ook inschakelen als ik geen geavanceerde magazijnopslag wil gebruiken?

Ja, zelfs als u niet van plan bent de geavanceerde magazijnbeheerfuncties te gebruiken, kunt u de optie **Magazijnbeheerprocessen gebruiken** voor de opslagdimensiegroep inschakelen. Als u transacties wilt maken en verwerken, moet u de minimale configuratie voltooien, zoals reserveringshiërarchieën en eenheidsvolgordegroepen. De instellingen voor geavanceerde magazijnen worden echter meestal genegeerd wanneer u ordervervangingslijsten, pakbonnen en productontvangstbonnen handmatig verwerkt (bijvoorbeeld op de verkooporder- en inkooporderpagina's).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Wanneer moet ik de optie Fysieke voorraad inschakelen voor een opslag- of traceringsdimensiegroep?

U moet de optie **Fysieke voorraad** inschakelen voor opslag- en traceringsdimensiegroepen wanneer u gedetailleerde voorraadrecords op basis van die dimensie moet bijhouden. Doorgaans wordt elke dimensie die actief is ook fysiek gevolgd. Daarom wordt elke ontvangst, uitgifte of verplaatsing van de voorraad door de geselecteerde dimensie bijgehouden. Als een dimensie niet verplicht is (bijvoorbeeld de nummerplaat), kunt u de opties **Lege ontvangst is toegestaan** en **Lege uitgifte is toegestaan** inschakelen om gebruikers voorraad te laten ontvangen, uitgeven of verplaatsen, zelfs als de dimensie niet is opgegeven.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Wanneer moet ik de optie Financiële voorraad inschakelen voor een opslag- of traceringsdimensiegroep?

U moet de optie **Financiële voorraad** inschakelen voor opslag- en traceringsdimensiegroepen wanneer u gedetailleerde financiële records op basis van die dimensie moet bijhouden. De **locatiedimensies** worden altijd financieel bijgehouden, terwijl andere dimensies optioneel zijn voor financiële tracering. Als u een periodiek kostprijsberekeningsmodel gebruikt, zoals FIFO, LIFO of gewogen gemiddelde, en de optie **Financiële voorraad** voor een dimensie inschakelt, geeft u aan dat u alleen vereffeningen maakt wanneer de ontvangst en uitgifte dezelfde dimensiewaarden hebben. Als u bijvoorbeeld de optie **Financiële voorraad** voor de dimensie **Magazijn** inschakelt, komen in elk magazijn andere kosten voor en kunnen ontvangsten en uitgiften van verschillende magazijnen niet worden vereffend.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Kan ik wijzigingen aanbrengen in een product-, opslag- of traceringsdimensiegroep nadat er transacties zijn?

Nadat u een artikelmodelgroep hebt gemaakt, kunt u de instelling van de velden **In behoefteplan opnemen volgens dimensie**, **Voor inkoopprijzen** en **Voor verkoopprijzenvelden** wijzigen als het selectievakje **Actief** is ingeschakeld voor een dimensie in de artikelmodelgroep. Andere wijzigingen zijn niet toegestaan. U kunt bijvoorbeeld de opties **Actief**, **Lege uitgifte is toegestaan**, **Lege ontvangst is toegestaan**, **Fysieke voorraad** en **Financiële voorraad** niet in- of uitschakelen.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Kan ik de product-, opslag- of traceringsdimensiegroep voor een vrijgegeven product wijzigen?

Als de voorhanden voorraad voor een product 0 (nul) is en de optie **Openstaande waarde** op *Nee* is ingesteld voor alle voorraadtransacties, kunt u de opslag- en traceringsdimensiegroepen wijzigen op de vrijgegeven productiepagina. U kunt de productdimensiegroep niet wijzigen als de record is gemaakt.

## <a name="item-model-groups"></a>Artikelmodelgroepen

### <a name="when-should-i-enable-the-stocked-product-option"></a>Wanneer moet ik de optie Product in voorraad inschakelen?

U moet de optie **Product in voorraad** inschakelen voor elk artikel dat in de voorraad wordt bijgehouden. Wanneer deze optie is ingeschakeld, worden gedetailleerde voorraadtransacties gebruikt om de ontvangst en uitgifte van het artikel bij te houden. Deze optie wordt bijvoorbeeld meestal ingeschakeld voor elk tastbaar artikel dat u in het magazijn houdt. U moet deze optie ook inschakelen als u van plan bent om een niet-tastbaar artikel, zoals een serviceartikel, toe te voegen aan uw stuklijsten of formules. Als u de optie **Product in voorraad** niet inschakelt, worden er geen voorraadtransacties bijgehouden in het subgrootboek voor de voorraad en worden de kosten van de artikelen meestal in uw grootboek opgevoerd. Deze optie wordt vaak gebruikt, bijvoorbeeld voor winkelbenodigdheden of diensten die niet in uw stuklijsten of formules zijn opgenomen.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Wanneer moet ik de optie Fysieke voorraad boeken inschakelen?

De optie **Fysieke voorraad boeken** wordt meestal ingeschakeld wanneer de optie **Product in voorraad** is ingeschakeld. Als u deze optie inschakelt, wordt de fysieke update van het artikel in de voorraadtransactie bijgehouden. Deze optie wordt gebruikt in combinatie met parameters in Leveranciers, Klanten en Productiebeheer om op te geven dat een boekstuk moet worden gemaakt met de fysieke update. U schakelt deze optie doorgaans in wanneer u wilt dat het grootboek wordt bijgewerkt wanneer u de voorraad fysiek bijwerkt. Als Supply Chain Management niet uw registratiesysteem voor financiële gegevens is, wilt u deze optie mogelijk uitschakelen.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Wanneer moet ik de optie Financiële voorraad boeken inschakelen?

De optie **Financiële voorraad boeken** wordt meestal ingeschakeld wanneer de optie **Product in voorraad** is ingeschakeld. Deze optie wordt gebruikt in combinatie met parameters in Leveranciers, Klanten en Productiebeheer om op te geven dat een boekstuk moet worden gemaakt met de financiële update. U schakelt deze optie doorgaans in wanneer u wilt dat het grootboek wordt bijgewerkt wanneer u de voorraad financieel bijwerkt (bijvoorbeeld door verkooporders en inkooporders te factureren of een productieorder te beëindigen). Als Supply Chain Management niet uw registratiesysteem voor financiële gegevens is, wilt u deze optie mogelijk uitschakelen.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Wanneer moet ik de optie Boeken op rekening voor uitgestelde opbrengst bij levering inschakelen?

Met de optie **Boeken op rekening voor uitgestelde opbrengst bij levering** kunt u aangeven of u de opbrengst in het grootboek wilt toerekenen wanneer u een pakbon voor een verkooporder boekt. Deze optie wordt meestal gebruikt wanneer u een lange vertraging hebt tussen de pakbon en factuur op een verkooporder of wanneer het niet mogelijk is om alle verkooporders in de periode te factureren. U schakelt deze optie meestal uit als u uw verkooporderfacturen direct na het boeken van de pakbon boekt. Op deze manier voorkomt u dat er extra grootboekboekingen worden gegenereerd die onmiddellijk worden omgekeerd wanneer u een verkooporder factureert.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Wanneer moet ik de optie Toerekening van aansprakelijkheid bij productontvangstbon inschakelen?

In de meeste organisaties wilt u de optie **Toerekening van aansprakelijkheid bij productontvangstbon** inschakelen voor alle artikelmodelgroepen, ongeacht of u een product in voorraad hebt of een product dat niet in voorraad is. Deze optie wordt gebruikt om een toerekening naar het grootboek te boeken op basis van de productontvangstbonprijs. Aangezien er meestal vertraging is tussen het boeken van de productontvangstbon voor een inkooporder en het boeken van de factuur, moeten de meeste organisaties de aansprakelijkheid op de balans verantwoorden om te voldoen aan lokale regelgeving, zoals algemeen geaccepteerde boekhoudkundige praktijken. Als Supply Chain Management niet uw registratiesysteem voor financiële gegevens is, wilt u deze optie mogelijk uitschakelen. Als uw organisatie aanschaffingscategorieën voor inkooporders gebruikt, kunt u de toerekeningsvereiste beheren door de optie **Inkoopkosten samenvoegen voor ontvangst** in te schakelen voor de categoriebeleidsregel op de pagina **Inkoopbeleid**.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Hoe voorkom ik dat een gebruiker een productontvangstbon van een inkooporder kan boeken als een ontvangstregistratie nog niet is geboekt?

U kunt voorkomen dat een gebruiker een productontvangstbon van een inkooporder kan boeken als de registratie van de inkooporder nog niet heeft plaatsgevonden. Daarvoor moet u de optie **Registratievereisten** voor de artikelmodelgroep inschakelen. Deze optie wordt meestal gebruikt in organisaties die een ontvangstproces in twee stappen gebruiken of in gevallen waarin u een batch- of serienummer moet registreren, bijvoorbeeld voor de artikelen die u ontvangt. De optie **Registratievereisten** is van toepassing op *alle* voorraadontvangstbonnen voor een artikel, niet alleen op inkooporders. De optie is bijvoorbeeld van toepassing op een voorraadjournaal met een positieve hoeveelheid en een productieorderrapport als een gereedgemeld journaal.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Hoe voorkom ik dat een gebruiker een factuur van een inkooporder kan boeken als een productontvangst nog niet is geboekt?

U kunt voorkomen dat een gebruiker een factuur van een inkooporder kan boeken als de productontvangst voor een inkooporder nog niet heeft plaatsgevonden. Daarvoor moet u de optie **Ontvangstvereisten** voor de artikelmodelgroep inschakelen. Deze optie wordt meestal gebruikt in organisaties die vereisen dat ontvangsten fysiek worden toegerekend in het grootboek voor toerekeningen. De optie **Ontvangstvereisten** is van toepassing op *alle* voorraadontvangstbonnen voor een artikel, niet alleen op inkooporders. De optie is bijvoorbeeld van toepassing op een voorraadjournaal met een positieve hoeveelheid en een productieorderrapport als een gereedgemeld journaal. Als uw organisatie aanschaffingscategorieën voor inkooporders gebruikt, kunt u de vereiste voor een ontvangst beheren door de optie **Ontvangstvereisten** in te schakelen voor de categoriebeleidsregel op de pagina **Inkoopbeleid**.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Hoe voorkom ik dat een gebruiker een pakbon van een verkooporder kan boeken als nog geen orderverzamellijst voor de verkooporder is geboekt?

U kunt voorkomen dat een gebruiker een pakbon of factuur van een verkooporder kan boeken als de registratie van de orderverzamellijst voor de verkooporder nog niet heeft plaatsgevonden. Daarvoor moet u de optie **Orderverzamelvereisten** voor de artikelmodelgroep inschakelen. Deze optie wordt meestal gebruikt in organisaties die een fysiek orderverzamelproces in het magazijn uitvoeren (bijvoorbeeld door het mobiele magazijnapparaat te gebruiken om de order te verzamelen). De optie **Orderverzamelvereisten** is van toepassing op *alle* voorraaduitgiften voor een artikel, niet alleen op verkooporders. De optie is bijvoorbeeld van toepassing op een voorraadjournaal met een negatieve hoeveelheid en een orderverzamellijstjournaal voor een productieorder.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Hoe voorkom ik dat een gebruiker een factuur van een verkooporder kan boeken als de pakbon van de verkooporder nog niet is geboekt?

U kunt voorkomen dat een gebruiker een factuur van een verkooporder kan boeken als de registratie van de pakbon voor de verkooporder nog niet heeft plaatsgevonden. Daarvoor moet u de optie **Inhoudingsvereisten** voor de artikelmodelgroep inschakelen. Deze optie wordt meestal gebruikt in organisaties die een fysiek verpakkingsproces uitvoeren in het magazijn (bijvoorbeeld door de mobiele app Warehouse Management te gebruiken om te verpakken of door een document te genereren dat wordt opgenomen bij de artikelen die worden verzonden). De optie **Inhoudingsvereisten** is van toepassing op *alle* voorraaduitgiften voor een artikel, niet alleen op verkooporders. De optie is bijvoorbeeld van toepassing op een voorraadjournaal met een negatieve hoeveelheid en een orderverzamellijstjournaal voor een productieorder.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Kan ik voorkomen dat geregistreerde artikelen worden verkocht?

Wanneer een artikel is geregistreerd in uw voorraad in Supply Chain Management, is de hoeveelheid fysiek beschikbaar om in het systeem te worden uitgegeven. Als artikelen die zijn geregistreerd, maar nog niet zijn ontvangen, *niet* beschikbaar moeten zijn voor uitgifte naar verkoop- of productieorders, kunt u bijvoorbeeld de functies voor voorraadstatus, voorraadblokkering, kwaliteitsorders, quarantaineorders of reserveringen gebruiken om het bedrijfsproces te beheren.

## <a name="production-costing"></a>Kostprijsberekening productie

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Kan ik één kostprijsberekeningsmodel voor grondstoffen en een ander kostprijsberekeningsmodel voor eindproducten gebruiken?

Ja, u kunt verschillende kostprijsberekeningsmodellen gebruiken voor elk artikel. Het is niet ongebruikelijk voor fabrikanten om een periodiek kostprijsberekeningsmodel voor grondstoffen en standaardkosten voor halffabricaten en eindproducten te gebruiken.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Hoe kan ik overheadkosten en machinekosten scheiden?

Om overheadkosten van uw machinekosten te halen, moet u op basis van uw bedrijfsbehoeften resources en resourcegroepen maken voor elke machine. Elke resource of resourcegroep kan aan kostencategorieën worden toegewezen om de kosten van de machine te beheren. Elke kostencategorie kan worden gekoppeld aan een kostengroep en elke kostengroep kan worden gebruikt als basis voor het berekenen van de indirecte kosten op het kostenblad.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Hoe reken ik kosten toe die betrekking hebben op het verbruik van energie (bijvoorbeeld water, energie of gasverbruik) op het kostenblad?

U kunt kosten met betrekking tot het energieverbruik meestal op twee manieren toerekenen:

- Maak een regel in de stuklijst of formule. Normaal gesproken wordt deze regel gemaakt als serviceartikel en kunt u de maateenheid opgeven die u verbruikt in verhouding tot de hoeveelheid die u produceert. Op deze manier kan de gebruiker tijdens het productieproces een ander bedrag verbruiken. U kunt de artikelen automatisch verbruiken op basis van de waarde die u selecteert in het veld **Backflushing**.
- Maak een post voor indirecte kosten op uw kostenblad. Deze methode wordt meestal gebruikt om de totale kosten van uw energieverbruik toe te wijzen in uw productieproces. U kunt de kostengroep en de absorptiebasis bijvoorbeeld gebruiken om het verbruik te schalen op basis van materialen of arbeid in uw route.

U moet de beste optie selecteren op basis van uw rapportage-, afstemmings- en operationele vereisten.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Kan ik resourcedetails in de stuklijst of formule vastleggen?

Resourcedetails kunnen alleen in een routebewerking worden vastgelegd. Hoewel u een serviceartikel kunt maken voor een resource en kosten kunt toewijzen om de kostenberekening voor een eindproduct te verhogen, is deze benadering niet aan te raden. In plaats daarvan raden we u aan een eenvoudige route te maken met één regel om de resourcekosten bij te houden en de activiteit zo te configureren dat deze automatisch wordt verbruikt aan het begin of einde van de productieorder.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Kan ik de berekeningsdetails weergeven als de kosten handmatig worden ingevoerd?

Nummer Als u de prijs handmatig op de pagina **Artikelprijs** invoert, zijn de knoppen **Berekeningsdetails weergeven** en **Berekeningsdetails rapporteren** niet beschikbaar. Als u de knop **Kostenvergaring per kostengroep** selecteert voor een kostprijs die handmatig is ingevoerd, wordt een samengevatte regel weergegeven en worden alle kosten getotaliseerd naar het voltooide artikel.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Berekent het systeem afwijkingen voor een productieorder wanneer ik de kosten handmatig invoer?

Ja, het systeem berekent afwijkingen wanneer u handmatig standaardkosten invoert. Wanneer u echter handmatig standaardkosten invoert in plaats van deze te berekenen, worden alle verbruikte materialen, routes en indirecte kosten in de productieorder als een vervangingsafwijking beschouwd. Als er extra afwijkingen zijn, zoals verbruik van extra materialen of arbeid, worden deze ook geregistreerd als afwijkingen van de productiestuklijst. Het wordt daarom ten zeerste aanbevolen om altijd een berekening uit te voeren voor artikelen met een stuklijst, route of indirecte kosten.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Hoe kan ik de afwijkingen van een subproductieorder naar de bovenliggende productieorder overbrengen?

Wanneer u een periodiek kostprijsberekeningsmodel gebruikt, zoals FIFO, LIFO of gewogen gemiddelde, worden de kosten van een subproductie toegerekend in het heuristische model dat u voor de artikelen hebt geselecteerd. Als u de werkelijke kostprijsberekening wilt weten, kunt u overwegen het markeringsprincipe te gebruiken om aan te geven welke subproductie wordt uitgegeven aan een bovenliggende productieorder. U kunt ook de optie **Financiële voorraad** gebruiken voor de dimensie **Batch** of  **Serienummer**, bijvoorbeeld in de traceringsdimensiegroep.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Wat is de invloed van het wisprincipe op verbruik?

Het wisprincipe in een stuklijst, formule of routeregel bepaalt de timing en techniek die wordt gebruikt om het artikel of de arbeid te verbruiken. Als u *Starten* selecteert, wordt het artikel of de arbeid automatisch verbruikt wanneer u de productieorder start. Als u *Voltooien* selecteert, wordt het artikel of de arbeid automatisch verbruikt wanneer u de productieorder als voltooid meldt. Als u *Handmatig* selecteert, moet een gebruiker handmatig materialen verzamelen of de tijd registreren in een taak- of routekaartjournaal. Voor stuklijsten en formules is ook een optie *Beschikbaar op locatie* beschikbaar. Als u deze optie selecteert, worden de artikelen automatisch verbruikt nadat ze naar de productielocatie zijn overgebracht.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Hoe moet ik kostenberekeningen uitvoeren als ik stuklijsten van meerdere niveaus of formules heb?

In het algemeen is het raadzaam om te beginnen op het laagste niveau van uw stuklijsten of formules voor de berekening. Als u gemakkelijker wilt filteren wanneer u een groot aantal kostenberekeningen wilt uitvoeren, kunt u berekeningsgroepen gebruiken om producten te kunnen scheiden. Het is ook raadzaam om de periodieke taak *Stuklijstniveaus bijwerken* uit te voeren voordat u met een groot aantal kostenberekeningen begint. Elke organisatie moet de combinatie van producten overwegen en een strategie definiëren die voldoet aan de specifieke behoeften van uw product en stuklijst- of formulestructuren.

## <a name="transfer-order-costing"></a>Kostprijsberekening voor transferorders

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Is er een manier om vracht toe te wijzen aan transferorderkosten?

U kunt toeslagen aan een transferorder toevoegen om kosten toe te voegen. Met de toeslagencode worden de debet en credit bepaald voor de toeslagen die u toevoegt. U moet eerst toeslagencodes maken in de module **Voorraadbeheer**. Als u een toeslag aan een transferorder wilt toevoegen, selecteert u **Toeslagen** op de transferorderregel waaraan u een toeslag wilt toevoegen.

## <a name="variances"></a>Afwijkingen

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Kan ik afwijkingen anders behandelden op basis van de locatie of het magazijn?

Er is geen optie om afwijkingsrekeningen per locatie te configureren. Wanneer u de standaardkostprijsberekening gebruikt voor een vrijgegeven product, kunt u op de pagina **Boeking** de hoofdrekening selecteren die wordt gebruikt voor boekingen van standaardkostenafwijkingen. U kunt ervoor kiezen om de rekeningen te configureren voor één artikel, een groep artikelen of alle artikelen. U kunt ook één kostengroep, een groep kostengroepen of alle kostengroepen configureren.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Kan ik afwijkingen als gevolg van valutawisselkoersen scheiden van andere typen afwijkingen?

Als een afwijking het resultaat is van een valutawisselkoersverschil tussen de inkooporderprijs en de standaardkosten voor een artikel, kan het wisselkoersverschil niet worden gescheiden van andere afwijkingen.

## <a name="reporting"></a>Rapportage

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Hoeveel configuraties voor voorraadwaardenrapporten kan ik maken en gebruiken?

Er is geen limiet aan het aantal configuraties voor voorraadwaardenrapporten dat u kunt maken. U moet uw specifieke rapportagevereisten evalueren en het aantal configuraties maken dat u nodig hebt om aan deze vereisten te voldoen. U hebt ten minste één configuratie voor voorraadwaardenrapporten nodig om het rapport of de optie voor rapportopslag uit te voeren.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Kan ik het voorraadwaardenrapport gebruiken om de kosten van een artikel in elk magazijn te analyseren?

Ja. U kunt de optie **Weergeven** of **Totaal** inschakelen voor elke dimensie **Magazijn** in de configuratie voor voorraadwaardenrapporten. Het rapport bevat echter alleen waarden voor dimensies waarvoor de optie **Financiële voorraad** is ingeschakeld voor de opslagdimensiegroep. Voor andere dimensies worden alleen lege kolommen weergegeven. Zie [Voorbeelden en logica voorraadwaardenrapporten](inventory-value-report-examples.md) voor meer informatie.

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Hoe kan ik de voorraadhoeveelheid vanaf een specifieke datum weergeven met het gewogen gemiddelde?

U kunt het rapport **Naar ouderdom rangschikken van voorraad** gebruiken dat een kolom **Gemiddelde eenheidskosten** bevat die de waarde van de voorraad vanaf een bepaalde datum toont. Zie [Voorbeelden en logica voorraadverouderingsrapporten](inventory-aging-report.md) voor meer informatie.

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Hoe kan ik zien welke ontvangsttransacties worden vereffend met een uitgiftetransactie?

U kunt de vereffeningen voor een voorraadtransactie weergeven door **Vereffeningen** of **Kostenverkenner** te selecteren op het tabblad **Voorraad** in het actievenster van de pagina **Voorraadtransactie** of **Voorraadtransactiedetails**. Als u een ontvangst selecteert om de uitgiften weer te geven die betrekking hebben op de transactie, worden de details niet weergegeven in de kostenverkenner. Details worden alleen weergegeven als u een uitgiftetransactie selecteert.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Hoe toont het voorraadwaardenrapport artikelen met een positieve fysieke hoeveelheid en een negatieve financiële waarde?

In het voorraadwaardenrapport worden de fysieke en financiële bedragen en hoeveelheden in hun eigen kolommen gescheiden. De waarden die in het rapport worden weergegeven, zijn de waarden vanaf het datumbereik dat u tijdens het maken van het rapport hebt geselecteerd. Welk overzichtsniveau wordt weergegeven, is afhankelijk van de instellingen die u hebt geselecteerd. Als een artikel transacties heeft die fysiek zijn ontvangen en financieel zijn uitgegeven, worden de hoeveelheden en waarden onafhankelijk opgeteld. Als u ervoor hebt gekozen om het detailniveau als transacties weer te geven, worden rijen voor elke ontvangst en uitgifte afzonderlijk weergegeven en worden respectievelijk de fysieke en financiële hoeveelheden en bedragen weergegeven. Zie [Voorbeelden en logica voorraadwaardenrapporten](inventory-value-report-examples.md) voor meer informatie.

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Wat is de impact van opslag- en traceringsdimensiegroepen op het voorraadwaardenrapport?

Als u de optie **Financiële waarde** inschakelt voor een dimensie in een opslag- of traceringsdimensiegroep, kunt u de optie **Weergeven** of **Totaal** selecteren voor de dimensie in de configuratie voor voorraadwaardenrapporten. Als u de optie **Weergeven** of **Totaal** selecteert voor een dimensie waarbij de optie **Financiële waarde** niet is geselecteerd, is de kolom leeg in de rapportuitvoer. Als u de optie **Financiële waarde** hebt ingeschakeld voor een dimensie in een opslag- of traceringsdimensiegroep en u de optie **Weergeven** of **Totaal** niet selecteert in de configuratie voor voorraadwaardenrapporten, worden de waarden voor de geselecteerde dimensies samengevat waar ze financieel gevolgd worden.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Kan ik de ingesloten Power BI-rapporten aanpassen voor kostprijsberekening?

Ja, gebruikers met de juiste beveiligingsmachtigingen kunnen het canvas voor rapportontwerpen voor elk ingesloten Power BI-rapport bijwerken in Supply Chain Management. Zie [Ingesloten rapporten in Analytische werkgebieden aanpassen](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md) voor meer informatie.

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Waar kan ik het afschrift van de variantieanalyse bekijken?

U kunt het afschrift van de variantieanalyse openen door naar **Kostenbeheer \> Query's en rapporten \> Voorraadboekhouding - analyserapporten** of **Kostenbeheer \> Query's en rapporten \> Productieboekhouding - analyserapporten** te gaan. Met beide opties wordt hetzelfde rapport geopend en het rapport heeft hetzelfde gedrag.

## <a name="item-prices-and-default-costs"></a>Artikelprijzen en standaardkosten

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Kan ik de kosten voor elke productvariant bijhouden?

Ja. U kunt de optie **Kostprijs per variant gebruiken** op het sneltabblad **Kosten beheren** van de pagina **Vrijgegeven product** inschakelen om prijzen per productvariant in te schakelen. (Deze optie is alleen beschikbaar voor productmodellen.) Vervolgens kunt u op de pagina **Artikelprijs** (die u kunt openen via de pagina **Kostprijsversie** of **Vrijgegeven product**) de optie **Weergave van dimensies** selecteren om op te geven of u de dimensie **Configuratie**, **Grootte**, **Kleur** of **Stijl** wilt weergeven. Als u de instellingen wilt opslaan en de geselecteerde dimensies standaard wilt gebruiken wanneer u de pagina opent, moet u de optie **Instellingen opslaan** inschakelen en vervolgens **OK** selecteren. U kunt de dimensies alleen invoeren voor artikelen waarvoor de dimensies actief zijn in de productdimensiegroep.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Kan ik de kosten voor elk magazijn bijhouden?

Nee, u kunt de artikelprijs niet per magazijn bijhouden. U kunt echter handelsovereenkomsten voor inkoop- of verkoopprijzen per magazijn bijhouden. Selecteer eerst de optie **Voor inkoopprijzen** of **Voor verkoopprijzen** voor de dimensie op de pagina **Opslagdimensiegroep**. Wanneer u vervolgens het handelsovereenkomstjournaal maakt en de regels voor de dimensies opent, selecteert u **Voorraad \> Weergavedimensies** om te selecteren welke dimensie in het raster moet worden weergegeven. Als u de instellingen wilt opslaan en de geselecteerde dimensies standaard wilt gebruiken wanneer u de pagina opent, moet u de optie **Instellingen opslaan** inschakelen en vervolgens **OK** selecteren. U kunt de dimensies alleen invoeren voor artikelen waarvoor de dimensies actief zijn in de productdimensiegroep.

### <a name="what-are-price-charges"></a>Wat zijn prijstoeslagen?

Met prijstoeslagen kunt u een vast bedrag toevoegen aan de eenheidsprijs van de artikelprijs of handelsovereenkomst. Wanneer u een bedrag in het veld **Prijstoeslagen** opgeeft, kunt u ook een waarde invoeren in het veld **Hoeveelheid toeslagen**. De prijstoeslagen worden afgeschreven voor de opgegeven hoeveelheid toeslagen. Schakel de optie **Inbegrepen in eenheidsprijs** in als u de prijstoeslagen in de eenheidsprijs voor het artikel wilt opnemen. Deze optie wordt altijd ingeschakeld voor standaardkosten.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Hoe moet ik prijzen configureren voor artikelen die in meerdere valuta's worden aangeschaft?

Als u een standaardprijs in het veld **Inkoopprijs** op de pagina **Vrijgegeven product** invoert, wordt ervan uitgegaan dat deze is vermeld in de valuta voor boekhouding van het grootboek voor de rechtspersoon waarin u zich bevindt. Zo wordt ook aangenomen dat de valuta van een ingevoerde inkoopprijs in een kostprijsberekeningsversie waarbij het veld **Prijstype** is ingesteld op *Inkoop* de valuta voor boekhouding van uw rechtspersoon is. Wanneer u een inkooporder maakt voor een leverancier met een andere valuta, wordt de valuta automatisch van de valuta voor boekhouding naar de transactievaluta omgerekend met behulp van de wisselkoers die u opgeeft in het veld **Wisselkoerstype valuta voor boekhouding** in het grootboek.

Wanneer u een handelsovereenkomstjournaal maakt, kunt u op elke regel de valuta opgeven voor de prijs. U kunt handelsovereenkomsten maken voor meerdere valuta's, specifieke leveranciers en vele andere combinaties van factoren. Als u een inkooporder maakt waarbij er een handelsovereenkomst bestaat voor de valuta die u hebt geselecteerd, gebruikt het systeem de handelsovereenkomst met de overeenkomende valuta. Wanneer u transacties, zoals productontvangstbonnen of facturen, boekt, wordt het bedrag omgerekend naar de valuta voor boekhouding van het grootboek op basis van de wisselkoers voor valuta voor boekhouding die u in het grootboek opgeeft.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Hoe moet ik kosten configureren voor artikelen die in meerdere valuta's worden aangeschaft?

Kosten kunnen niet in meer dan één valuta worden geconfigureerd. De kosten die u opgeeft voor de artikelprijs of standaardkosten die u in het veld **Prijs** op het sneltabblad **Kosten beheren** van de pagina **Vrijgegeven product** opgeeft, worden altijd weergegeven in de valuta voor boekhouding van het grootboek voor de rechtspersoon die u hebt geselecteerd.

Als uw organisatie gebruikmaakt van standaardkostprijsberekening, moet u een strategie opgeven voor het definiëren van de kosten wanneer er meerdere valuta's zijn. U moet ook een proces definiëren voor het regelmatig bijwerken van de kosten, zodat het aantal geboekte afwijkingen wordt beperkt.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Kan ik de instelling voor Winst op de pagina Kostengroep gebruiken om verkoopprijzen te berekenen?

Ja, u kunt met de instelling voor **Winst** op de pagina **Kostengroep** een percentage toevoegen wanneer verkoopprijzen worden berekend via een kostenberekening. Zie voor meer informatie [Stuklijstberekeningen](bom-calculations.md).

## <a name="marking"></a>Markering

### <a name="how-does-marking-affect-periodic-costing-models"></a>Wat is de invloed van markeren op periodieke kostprijsberekeningsmodellen?

Als u een periodiek kostprijsberekeningsmodel gebruikt, zoals FIFO, LIFO of gewogen gemiddelde, en u een ontvangsttransactie hebt gemarkeerd voor een uitgiftetransactie, wordt het heuristische model van het artikel genegeerd tijdens het voorraadafsluitingsproces. In plaats daarvan gebruikt het systeem de werkelijke kosten van de ontvangst voor de kosten van de uitgifte.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Wat gebeurt er tijdens de voorraadafsluiting wanneer ik markering gebruik?

Wanneer u ontvangsten en uitgiften markeert, worden de transacties vereffend die gezamenlijk zijn gemarkeerd. Wanneer markering wordt gebruikt om de vereffening te maken, wordt het veld **Principe** op de pagina **Vereffening** ingesteld op *Markeren*. Als een transactie wordt gemarkeerd voordat deze fysiek of financieel wordt bijgewerkt, gebruikt de uitgifte de kosten van de gemarkeerde ontvangst in plaats van de lopende gemiddelde kosten. Als de transacties na de financiële update worden gemarkeerd, worden de uitgiftekosten tijden het proces voor voorraadafsluiting en -correctie aangepast aan de ontvangstkosten.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Kan ik transacties handmatig markeren als ik standaardkostprijsberekening of een zwevend gemiddelde gebruik?

Nee, u kunt ontvangsten of uitgiften niet handmatig markeren wanneer u standaardkostprijsberekening of een zwevend gemiddelde gebruikt. Als transacties (bijvoorbeeld rechtstreekse levering of intercompany-orders) automatisch worden gemarkeerd, blijft de markeringsrecord staan en wordt deze als een harde reservering gebruikt. Wanneer u echter een standaardkostprijsberekening of een zwevend gemiddelde gebruikt, heeft de markering van records geen effect op de kosten van de artikelen.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Wat is de invloed van markeren op de winst- en verliesrekening?

Wanneer u een uitgiftetransactie voor een ontvangst markeert, komen de kosten voor de uitgifte overeen met de geselecteerde ontvangst. Wanneer u de uitgifte fysiek en financieel boekt, heeft de boeking gevolgen voor rekeningen **Kosten van verkochte goederen, geleverd** en **Kosten van verkochte goederen, gefactureerd** die u opgeeft in het voorraadboekingsprofiel. Als een transactie wordt gemarkeerd na de fysieke of financiële update, wordt door het proces *Voorraad afsluiten en aanpassen* een correctie gemaakt met een overeenkomend boekstuk waarmee de rekening **Kosten van verkochte goederen, gefactureerd** wordt gecorrigeerd en de verrekening wordt doorgevoerd met de rekening ie u opgeeft bij **Kosten van eenheden, gefactureerd** (voorraad).

### <a name="how-does-marking-affect-master-planning"></a>Wat is de invloed van markeren op de hoofdplanning?

Het tabblad **Standaardupdate** op de pagina **Parameters hoofdplanning** bevat een veld met de naam **Markering bijwerken**. De optie die u hier selecteert, wordt gebruikt wanneer u een geplande order fiatteert die door de hoofdplanning wordt gegenereerd. De volgende opties zijn beschikbaar:

- *Nee*: het systeem voert geen markering uit.
- *Standaard*: het systeem markeert ontvangsten tegen uitgiften op basis van de tracering van de behoefte. Een behoefteorder wordt aan de hand van een afhandelingsorder gemarkeerd. Als er hoeveelheid overblijft in de afhandeling, wordt de afhandelingsorder niet gemarkeerd.
- *Uitgebreid*: zowel de behoefteorders als afhandelingsorders worden gemarkeerd, ongeacht of er hoeveelheid in de afhandelingsorder blijft openstaan.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Negatieve voorraad

### <a name="when-should-i-allow-physical-negative-inventory"></a>Wanneer moet ik fysieke negatieve voorraad toestaan?

In het algemeen is het aan te raden dat u fysieke negatieve voorraad toestaat, omdat er in het magazijn niet minder dan 0 (nul) van een tastbaar artikel aanwezig kan zijn. De bedrijfsprocessen van sommige industrieën en zakelijke scenario's kunnen echter activiteiten beperken die vereisen dat de voorraad fysiek negatief wordt. Zo willen detailhandelaren de verkoop van een artikel dat bij de kassa wordt gebracht mogelijk niet voorkomen, zelfs niet als in het systeem wordt aangegeven dat er geen artikelen beschikbaar zijn. Verwerkingsfabrikanten bieden een ander voorbeeld. Voor deze fabrikanten kan het verbruikte bedrag hoger zijn dan het aanbevolen bedrag in de formule. Het verbruik kan in plaats van nauwkeurig ook geraamd zijn, zodat het verbruik hoger is dan de hoeveelheid op een bepaalde locatie, zoals een tank.

Waar mogelijk moet u het bedrijfsproces evalueren en proberen het te verbeteren zodat de voorraad niet negatief kan zijn. Als u negatieve voorraad moet toestaan, moet u een duidelijk bedrijfsproces hebben voor het corrigeren van de negatieve voorraad, omdat dit een nadelige invloed kan hebben op de kostprijs.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Wanneer moet ik financiële negatieve voorraad toestaan?

Over het algemeen is het raadzaam dat de meeste organisaties financiële negatieve voorraad toestaan. (In de meeste gevallen worden inkooporderfacturen niet verwerkt voordat u de artikelen kunt verzenden.) U moet deze optie inschakelen wanneer u specifieke bedrijfsprocessen hebt waarvoor de verkoopprijs de uiteindelijke kosten van een inkooporder moet weerspiegelen. Deze vereiste kan bijvoorbeeld van toepassing zijn in een maken op bestelling-industrie of in specifieke regio's waar deze volgens de wet verplicht is.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Wat gebeurt er met de kosten van mijn uitgiften als de voorraad negatief is?

Wanneer de voorraad voor uw artikel negatief is en u meer artikelen uitgeeft dan u fysiek hebt, gebruikt het systeem de standaardartikelprijs om het lopende gemiddelde te berekenen als u een periodiek kostprijsberekeningsmodel gebruikt, zoals FIFO, LIFO of gewogen gemiddelde. Als er geen standaardprijs voor het artikel is opgegeven, geeft het systeem de voorraad uit met een waarde van 0 (nul). Door dit gedrag kunnen toekomstige berekeningen van het lopende gemiddelde of het zwevende gemiddelde onnauwkeurig zijn.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Kan ik voorkomen dat artikelen worden verzameld, verpakt of verkocht in verkoop- en productieorders als er onvoldoende voorhanden voorraad is?

Ja. Het wordt aangeraden de optie **Fysieke negatieve voorraad** voor de artikelmodelgroep uit te schakelen om te voorkomen dat artikelen worden verzameld, verpakt of verkocht in verkoop- en productieorders.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Kan ik voorkomen dat artikelen worden gefactureerd voor een verkooporder als er geen inkooporders voor hetzelfde artikel zijn gefactureerd?

Ja. Het wordt aangeraden de optie **Financiële negatieve voorraad** voor de artikelmodelgroep uit te schakelen om te voorkomen dat artikelen worden gefactureerd als geen inkooporders zijn gefactureerd voor hetzelfde artikel.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Wat is de invloed van negatieve voorraad op financiële ratio's zoals de brutowinstmarge?

Wanneer u toestaat dat uw voorraad negatief wordt, kunnen de voorraadwaarde in uw balans en de kosten van verkochte goederen in uw winst- en verliesrekening te laag zijn, vooral als er geen standaardprijs voor uw artikelen is geconfigureerd. Daarom kunnen de financiële rapportage en ratio's, zoals brutowinstmarges, te groot zijn omdat de kosten niet juist zijn. Als u een periodiek kostprijsberekeningsmodel gebruikt, zoals FIFO, LIFO of gewogen gemiddelde, kan de waarde van de uitgiften worden gecorrigeerd wanneer u het proces voor voorraadafsluiting en -correctie uitvoert nadat de negatieve voorraadhoeveelheden zijn gecorrigeerd. Als u echter een zwevend gemiddelde gebruikt, kunnen de afzonderlijke transacties niet opnieuw worden geherwaardeerd.

### <a name="how-should-i-correct-negative-inventory"></a>Hoe corrigeer ik negatieve voorraad?

Wij raden u aan negatieve voorraad regelmatig te controleren en te corrigeren wanneer uw organisatie- of bedrijfsvereisten bepalen dat uw voorraad negatief mag worden. U kunt de voorraadwaarden corrigeren door een cyclustelling uit te voeren, een correctie te boeken of een verplaatsingsjournaal te boeken. Als u de onverwachte winsten in de voorraad in een bepaalde grootboekrekening moet verantwoorden, moet u een verplaatsingsjournaal gebruiken. Als u dit niet doet en het proces voor cyclustelling of voorraadcorrectie gebruikt, wordt de voorraadcorrectie geboekt naar de rekening **Voorraadontvangst** en de verschuiving naar de rekening **Voorraaduitgave, winst** die u opgeeft in het voorraadboekingsprofiel.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Moet ik een nieuw artikel maken als mijn voorraad negatief is geworden en ik een zwevend gemiddelde gebruik?

Nummer Als uw organisatie toestaat dat de voorraad fysiek negatief wordt en u een zwevend gemiddelde gebruikt als voorraadmodel, gebruikt het systeem de volgorde voor terugvalkosten die is toegewezen op de pagina **Parameters voor voorraad- en magazijnbeheer** om te bepalen hoe de kosten aan uw uitgiften worden toegewezen. Over het algemeen is het raadzaam om te voorkomen dat uw voorraad fysiek negatief wordt. Zie de andere vragen in de sectie [Negatieve voorraad](#negative-inventory) van dit artikel voor meer informatie.

## <a name="not-stocked-products"></a>Niet-voorradige producten

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Kan ik orderverzamellijsten voor verkooporders boeken voor niet-voorradige producten?

Wanneer u een orderverzamellijst genereert voor een verkooporder die artikelen bevat die zich in een artikelmodelgroep bevinden die niet op voorraad is, worden er geen regels weergegeven voor die artikelen die niet op voorraad zijn. U kunt de mobiele app Warehouse Management niet gebruiken om niet-voorradige artikelen te verwerken

Wanneer u een pakbon genereert voor een verkooporder die artikelen bevat die zich in een artikelmodelgroep bevinden die niet voorradig zijn, stelt u het veld **Hoeveelheid** in op *Gepickt aantal en producten niet in voorraad* om de niet-voorradige artikelen op te nemen bij het genereren van documenten. Als u *Alle* selecteert, worden alleen artikelen in voorraad opgenomen in de pakbon.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Moet ik een niet-voorradig product of een categorie (verkoop- of inkoopcategorie) gebruiken?

De keuze tussen een product dat niet in voorraad is en een categorie, hangt af van uw specifieke bedrijfsbehoeften. Producten die niet op voorraad zijn, bieden over het algemeen meer controle over standaardwaarden, zoals hoeveelheden en prijzen op inkoop- en verkooporders. Daarom krijgen producten die niet in voorraad zijn de voorkeur in gevallen waarin hetzelfde product of dezelfde service meer dan één keer wordt gekocht of verkocht. Categorieën komen van pas in scenario's waarin de prijs, artikelen, omschrijvingen en dergelijke inconsistent zijn van transactie naar transactie. Categorieën kunnen ook voor elk product worden gebruikt om het type product te classificeren dat wordt verkocht of ingekocht.

## <a name="service-items"></a>Artikelen van het type Service

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Wat is het verschil tussen een serviceartikel en een product dat niet op voorraad is?

Een serviceartikel is een producttype Wanneer u een nieuw vrijgegeven product maakt, kunt u het veld **Producttype** instellen op *Artikel* of *Service*. *Artikel* wordt doorgaans geselecteerd om aan te geven dat het artikel tastbaar is terwijl *Service* meestal wordt geselecteerd om aan te geven dat het artikel immaterieel is.

Vrijgegeven producten kunnen voorradig of niet-voorradig zijn, ongeacht of het een artikel of serviceproduct is. De instelling voor voorradig of niet-voorradig wordt beheerd door de artikelmodelgroep die u selecteert voor het vrijgegeven product. Wanneer u een artikelgroep selecteert die niet op voorraad is, worden er bijvoorbeeld geen voorraadtransacties voor de gerelateerde verkoop- of inkooporder gemaakt.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Kan ik niet-voorradige artikelen in een stuklijst opnemen?

Nee, u kunt geen vrijgegeven product opnemen dat is gekoppeld aan een artikelmodelgroep waarvoor de optie **Opgeslagen in voorraad** is uitgeschakeld in een stuklijst of formule. Het maakt niet uit of het veld **Producttype** is ingesteld op *Artikel* of *Service*. Alleen artikelen die op voorraad zijn, kunnen worden opgenomen op stuklijst- of formuleregels.

## <a name="costing-modelspecific-questions"></a>Specifieke vragen over het kostprijsmodel

### <a name="which-costing-model-should-i-use"></a>Welk kostprijsmodel moet ik gebruiken?

Welke kostenmodellen u moet selecteren, is afhankelijk van uw bedrijfsbehoeften. Voordat u een kostprijsmodel selecteert dat u wilt gebruiken in Supply Chain Management, moet u controleren of het model is toegestaan volgens lokale regelgeving. We raden u aan om uw selectie te valideren bij een gecertificeerde boekhouder in uw regio.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Kan ik meer dan één kostprijsmodel in mijn organisatie gebruiken?

Ja. Er geldt geen limiet voor het aantal artikelmodelgroepen of kostprijsmodellen dat u in Supply Chain Management kunt selecteren.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Kan ik meer dan één kostprijsmodel voor elk artikel gebruiken?

Nummer U kunt slechts één kostprijsmodel selecteren voor elk vrijgegeven product. Dit gedrag wordt beheerd door de artikelmodelgroep. Als u meerdere kostprijsmodellen moet gebruiken om te rapporteren over voorraadwaarden, moet u overwegen de invoegvoeging Algemene voorraadboekhouding te gebruiken.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Welke kostprijsmethodologie moet ik gebruiken wanneer ik productie-uitvoering gebruik?

Welke kostenmodellen u moet selecteren, is afhankelijk van uw bedrijfsbehoeften. Het gebruik van een kostprijsmodel biedt geen specifieke voor- of nadelen wanneer uw organisatie ook productie-uitvoering gebruikt.

### <a name="when-is-fefo-used"></a>Wanneer wordt FEFO gebruikt?

FEFO (First Expired, First Out) is geen kostprijsmethodologie. In plaats daarvan is het een reserveringstechniek die vaak wordt gebruikt in productieorganisaties. U kunt FEFO-reserveringen voor een artikelmodelgroep inschakelen door de optie **Gecontroleerde FEFO-datum** te activeren en vervolgens een waarde te selecteren in het veld **Orderverzamelcriteria**.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Zijn er prestatievoordelen verbonden aan de selectie van bepaalde kostprijsmodellen?

Over het algemeen heeft het geselecteerde kostprijsmodel voor een artikel een minimale invloed op de algehele prestaties van het systeem. De hoeveelheid tijd die nodig is om de voorraadafsluiting of herberekening uit te voeren, kan echter worden beïnvloed door het geselecteerde voorraadkostprijsmodel. Als u bijvoorbeeld gebruikmaakt van standaardkosten of een zwevend gemiddelde, heeft het proces voor het afsluiten van voorraad een minimale invloed op het systeem omdat niet elke voorraadtransactie wordt bijgewerkt en er geen vereffeningen worden gemaakt. Een periodiek kostprijsmodel, zoals FIFO, LIFO of gewogen gemiddelde, kan de tijd die nodig is om het voorraadafsluitingsproces af te ronden echter verhogen. Het proces voor het afsluiten van voorraad kan langer duren wanneer u een hoge waarde invoert in het veld **Het maximale aantal toegestane herhalingen per artikel** of een lage waarde in het veld **Toegestaan minimumbedrag** voor het proces *Voorraad afsluiten*.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Wanneer moet ik de optie Vaste ontvangstprijs gebruiken?

Wanneer u het selectievakje **Vaste ontvangstprijs** voor een artikel inschakelt op de pagina **Artikelmodelgroep**, wordt de ontvangstprijs gebruikt als standaardkosten voor de voorraadontvangst. Als er een verschil is tussen de inkoopprijs en de standaardartikelkostprijs die voor een product zijn geconfigureerd, wordt het verschil geboekt naar de rekening **Winstrekening vaste ontvangstprijs** of **Verliesrekening vaste ontvangstprijs** en de verschuiving naar de rekening **Tegenrekening vaste ontvangstprijs**. (Al deze rekeningen worden opgegeven op de pagina **Boeking**.)

Schakel het selectievakje **Vaste ontvangstprijs** in wanneer u een periodiek kostprijsmodel gebruikt, zoals FIFO, LIFO of gewogen gemiddelde, en u vereist dat een inkoopprijsafwijking in het grootboek wordt bijgehouden als de prijs van een ontvangst verschilt van de standaardartikelkosten.

### <a name="moving-average"></a>Zwevend gemiddelde

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Is gewogen gemiddelde hetzelfde als een zwevend gemiddelde?

De termen gewogen gemiddelde, zwevend gemiddelde en lopend gemiddelde worden vaak als synoniemen van elkaar gebruikt. Van deze termen is zwevend gemiddelde het enige officiële kostprijsmodel dat beschikbaar is in Supply Chain Management. Hoewel gewogen gemiddelde geen officieel kostprijsmodel is, is dit de techniek die wordt gebruikt wanneer u een periodiek kostprijsmodel gebruikt, zoals FIFO, LIFO of zwevend gemiddelde. De term lopend gemiddelde wordt niet in Supply Chain Management gebruikt en heeft mogelijk verschillende connotaties in andere systemen.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Hoe kan ik het verschil tussen de ontvangstprijs van het product en de factuurprijs opvangen wanneer ik een zwevend gemiddelde gebruik?

Wanneer u een zwevend gemiddelde gebruikt, worden de fysieke kosten (ontvangstprijs) gebruikt om het zwevende gemiddelde te berekenen voor alle uitgiftetransacties. Als er een verschil is tussen de fysieke kosten (ontvangstprijs) en de financiële kosten (factuurprijs), wordt het verschil automatisch naar de hoofdrekening geboekt die is opgegeven voor het boekingstype **Prijsverschil voor zwevend gemiddelde** op het tabblad **Voorraad** van de pagina **Voorraadboekingsprofiel**.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Waar wordt het prijsverschil voor het zwevende gemiddelde in het grootboek weergegeven?

Als er een prijsverschil is tussen de boeking van een fysieke update en een financiële update voor een ontvangst, wordt het verschil naar de hoofdrekening geboekt die is opgegeven voor het boekingstype **Prijsverschil voor zwevend gemiddelde** op het tabblad **Voorraad** van de pagina **Voorraadboekingsprofiel**. Zie [Zwevend gemiddelde](moving-average.md) voor meer informatie.

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Wat gebeurt er als er een uitgifte vóór de ontvangst is als ik een zwevend gemiddelde gebruik?

Meestal kan er een uitgifte zijn vóór de ontvangst, omdat u fysieke negatieve voorraad toestaat voor de artikelmodelgroep of omdat de uitgifte wordt geantedateerd. Zie de sectie [Negatieve voorraad](#negative-inventory) in dit artikel voor meer informatie.

Als u transacties antedateert, raden we u aan om uw bedrijfsproces en bewerkingen zorgvuldig te overwegen om te bepalen of er een manier is om dit scenario te vermijden. Als u een transactie antedateert voor een artikel dat een zwevend gemiddelde gebruikt, wordt het huidige zwevende gemiddelde toegewezen aan de transactie. Latere uitgiften worden niet gecorrigeerd. Zie [Zwevend gemiddelde](moving-average.md) voor meer informatie over het zwevende gemiddelde met geantedateerde transacties.

### <a name="standard-costing"></a>Standaardkostprijsberekening

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Wat is het verschil tussen de standaardkostprijsberekening en de vaste ontvangstprijs?

Voor standaardkostprijsberekeningen moet u een artikelprijs definiëren en de kosten activeren in een kostprijsberekeningsversie. Deze kosten worden voor alle ontvangsten en uitgiften gebruikt. Afwijkingen voor de ontvangsten in voorraad worden geregistreerd in het grootboek met behulp van de standaardrekeningen voor kostenafwijkingen die u opgeeft op het tabblad **Standaardkosten** van de pagina **Voorraadboekingsprofiel**.

Wanneer u echter een vaste ontvangstprijs gebruikt, staan alleen de kosten voor ontvangsten vast en worden de kosten gebruikt die u op het sneltabblad **Kosten beheren** van de pagina **Vrijgegeven product** hebt opgegeven. Verschillen tussen de standaardkosten en de inkooporderprijs zorgen ervoor dat de afwijking in de inkoopprijs wordt geboekt naar de winst- en verliesrekeningen voor de vaste ontvangstprijs. Voor uitgiften wordt geen vaste ontvangstprijs gebruikt. In plaats daarvan worden uitgiften gewaardeerd op het zwevende gemiddelde op het moment van boeken (tenzij u markering gebruikt) en ze worden geherwaardeerd naar het heuristische model dat u selecteert wanneer u de voorraad afsluit.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Kan ik FEFO-reserveringen gebruiken met standaardkostprijsberekeningen?

Ja, u kunt FEFO-reserveringen in een artikelmodelgroep gebruiken wanneer u standaardkostprijsberekening selecteert. MET FEFO-reserveringen wordt de reserveringslogica beheerd die wordt gebruikt voor de fysieke verwerking van de artikelen, terwijl met standaardkostprijsberekening de fysieke en financiële kosten van een artikel worden geregeld.

### <a name="can-i-upload-pending-prices"></a>Kan ik prijzen in behandeling uploaden?

Ja, u kunt de Excel-invoegtoepassing of Data Management Framework gebruiken om een prijs in behandeling te uploaden. We raden u aan om de volgende entiteiten te gebruiken:

- Artikelprijzen in behandeling (V2)
- Eenheidskosten in behandeling voor kostprijscategorie van route
- Berekeningsfactoren van kostenbladknooppunt (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Hoe vaak kan ik de standaardkosten voor een artikel bijwerken?

Er is geen limiet voor de frequentie waarmee u nieuwe standaardkosten kunt activeren. Als u nieuwe kosten activeert voor een artikel op dezelfde dag dat de laatste kosten zijn geactiveerd, gebruikt het systeem de meest recente geactiveerde kosten voor nieuwe transacties of updates (zoals updates van bestaande transacties).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Kan ik geactiveerde kosten deactiveren of verwijderen?

Nee, u kunt geactiveerde kosten niet deactiveren of verwijderen. Als u kosten incorrect hebt geactiveerd, kunt u nieuwe kosten activeren die de juiste kosten hebben.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Worden er berekeningsgroepen gebruikt bij standaardkostprijsberekeningen?

Berekeningsgroepen kunnen bij elk artikel worden gebruikt, ongeacht de artikelmodelgroep die u hebt gekozen. De berekeningsgroepen worden gebruikt tijdens het totaliseren of berekenen van kosten om de instellingen te bepalen die moeten worden gebruikt voor de artikelen waarvoor u de berekening uitvoert. Zie [Stuklijstberekeningsgroepen](bom-calculation-groups.md) voor meer informatie over berekeningsgroepen.

### <a name="when-should-i-use-a-planned-costing-version"></a>Wanneer moet ik een geplande kostprijsberekeningsversie gebruiken?

Kostprijsberekeningsversies kunnen het type *Standaardkosten* of *Geplande kosten* bevatten. Het type *Standaardkosten* wordt gebruikt voor de kosten die actief zijn in het systeem en worden geboekt in transacties. Het type *Geplande kosten* wordt gebruikt voor het uitvoeren van simulaties van kosten en heeft geen invloed op de transactiekosten.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Kunnen de totale kosten van de ene entiteit worden overgeboekt naar een andere entiteit als de verkoopkosten?

Er is geen geautomatiseerde manier om kosten van het ene bedrijf naar het andere te kopiëren. Verder is er geen manier om kosten van een inkoopprijs automatische naar een verkoopprijs te kopiëren. Als uw organisatie een van deze taken moet uitvoeren, moet u overwegen of u Data Management Framework kunt gebruiken om de gegevens uit uw kostprijsberekeningsversie te exporteren en naar een ander bedrijf te uploaden, als verkoopprijs in de kostprijsberekeningsversie of als een handelsovereenkomst. Handmatige bewerkingen van de bestanden zijn mogelijk vereist.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Wat is de beste manier om geplande kosten naar een standaardkostprijsberekeningsversie te kopiëren?

Met de knop **Kopiëren** op de pagina **Kostprijsberekeningsversies** kunt u artikelprijzen, kostencategorieprijzen of indirecte kosten van de ene kostprijsberekeningsversie naar de andere kopiëren.
