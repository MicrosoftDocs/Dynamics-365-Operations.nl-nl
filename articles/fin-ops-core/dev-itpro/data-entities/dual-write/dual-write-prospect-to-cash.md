---
title: Prospect naar contant geld in twee keer wegschrijven
description: Dit onderwerp biedt informatie over Prospect naar contant geld in twee keer wegschrijven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b10e5f0fe97e65ad380e85815c56e88a3ce4e303
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443890"
---
# <a name="prospect-to-cash-in-dual-write"></a>Prospect naar contant geld in twee keer wegschrijven

[!include [banner](../../includes/banner.md)]



Een belangrijk doel van de meeste bedrijven is het converteren van prospects naar klanten en vervolgens een langdurige zakelijke relatie met deze klanten te onderhouden. In Microsoft Dynamics 365-apps vindt het proces Prospect naar contant geld plaats via offertes of orderverwerkingswerkstromen en worden de financiële gegevens afgestemd en verantwoord. Dankzij de integratie van prospect-naar-contact met twee keer wegschrijven wordt er een workflow gemaakt die een offerte en een order combineert die afkomstig zijn uit Dynamics 365 Sales of Dynamics 365 Supply Chain Management, en worden de offerte en de order beschikbaar gemaakt in beide apps.

In de app-interfaces hebt u toegang tot de verwerkingsstatus en factuurgegevens in real-time. Hierdoor kunt u functies zoals productvoorraad, voorraadverwerking en uitvoering van Supply Chain Management eenvoudiger beheren, zonder dat u de offertes en orders opnieuw hoeft te maken.

![Gegevensstroom voor Twee keer wegschrijven in Prospect naar contant geld](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

Voordat u verkoopoffertes kunt synchroniseren, moet u de volgende instellingen bijwerken.

### <a name="setup-in-sales"></a>Instellingen in Sales

Ga in Sales naar **Instellingen \> Beheer \> Systeeminstellingen \> Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:

- De systeemoptie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.
- Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.

### <a name="sites-and-warehouses"></a>Locaties en magazijnen

In Supply Chain Management zijn de velden **Locatie** en **Magazijn** vereist voor offerteregels en orderregels. Als u de locatie en het magazijn instelt in de standaardorderinstellingen, worden deze velden automatisch ingesteld wanneer u een product toevoegt aan een offerteregel of een orderregel. 

### <a name="number-sequences-for-quotations-and-orders"></a>Nummerreeksen voor offertes en orders

De nummerreeksen voor Supply Chain Management en Sales zijn niet verbonden wanneer offertes en orders worden gemaakt en gesynchroniseerd in Sales en Supply Chain Management. Als een verkooporder die in Sales is gemaakt, wordt gesynchroniseerd met Supply Chain Management, heeft deze hetzelfde verkoopordernummer in Supply Chain Management. Om ervoor te zorgen dat het verkoopordernummer niet wordt gedupliceerd, moet u verschillende nummerreekssystemen in de twee apps gebruiken.

De nummerreeks in Supply Chain Management is bijvoorbeeld **1, 2, 3, 4, 5, ...** en de nummer reeks in Sales is **100, 99, 98, ...**. Als u 100 verkooporders maakt in Sales, wordt er uiteindelijk een ordernummer gegenereerd dat al bestaat in Supply Chain Management. Met andere woorden de twee nummerreeksen overlappen elkaar uiteindelijk als verkooporders worden gemaakt in Supply Chain Management en Sales. In plaats daarvan kunt u een nummerreeks gebruiken zoals **F1, F2, F3, ...** in Supply Chain Management en een nummerreeks zoals **C1, C2, C3 ,...** in Sales. Deze nummerreeksen produceren nooit dubbele verkoopordernummers.

## <a name="sales-quotations"></a>Verkoopoffertes

Verkoopoffertes kunnen worden gemaakt in Sales of Supply Chain Management. Als u een offerte maakt in Sales, wordt deze in realtime gesynchroniseerd met Supply Chain Management. Als u een offerte maakt in Supply Chain Management, wordt deze in realtime gesynchroniseerd met Sales. Let op de volgende punten:

+ U kunt een korting toevoegen aan het product op de offerte. In dit geval wordt de korting gesynchroniseerd met Supply Chain Management. De velden **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een configuratie in Supply Chain Management. Deze instelling biedt momenteel geen ondersteuning voor integratietoewijzing. In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** bijgehouden en verwerkt in Supply Chain Management.
+ De velden **Kortingspercentage**, **Korting** en **Vrachtkosten** zijn in de koptekst van de verkoopofferte alleen-lezenvelden.
+ De velden **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

Als u ook de Field Service-oplossing gebruikt, moet u de parameter **Snel offerteregel maken** opnieuw inschakelen. Als u de parameter opnieuw inschakelt, kunt u doorgaan met het maken van offerteregels met de functie Snel maken.
1. Ga naar uw Dynamics 365 Sales-toepassing.
2. Selecteer het pictogram Instellingen op de navigatiebalk bovenaan.
3. Selecteer **Geavanceerde instellingen**.
4. Kies de optie **Het systeem aanpassen**.
5. Selecteer de menuopdracht **Offerteregel**.
6. Ga naar de sectie **Gegevensservices** en schakel het selectievakje **Snel maken toestaan** in.

## <a name="sales-orders"></a>Verkooporders

Verkooporders kunnen worden gemaakt in Sales of Supply Chain Management. Als u een verkooporder maakt in Sales, wordt deze in realtime gesynchroniseerd met Supply Chain Management. Als u een verkooporder maakt in Supply Chain Management, wordt deze in realtime gesynchroniseerd met Sales. Let op de volgende punten:

+ U kunt orders alleen activeren en synchroniseren vanuit Sales als alle producten op de order afkomstig zijn uit Finance and Operations-apps. Er kunnen dus geen toe te voegen producten zijn.
+ Berekening en afronding van korting:

    - Het model voor het berekenen van korting in Sales wijkt af van het model voor het berekenen van korting in Supply Chain Management. In Supply Chain Management kan het uiteindelijke kortingsbedrag op een verkoopregel het resultaat zijn van een combinatie van kortingsbedragen en -percentages. Als dit uiteindelijke kortingsbedrag wordt gedeeld door de hoeveelheid op de regel, kan er afronding plaatsvinden. Deze afronding wordt echter niet gebruikt als een afgerond kortingsbedrag per eenheid wordt gesynchroniseerd naar Sales. Het volledige kortingsbedrag op een verkoopregel in Supply Chain Management kan alleen correct worden gesynchroniseerd naar Sales als het volledige bedrag wordt gesynchroniseerd, zonder het te delen door de regelhoeveelheid. Daarom moet u in Sales de berekeningsmethode voor de korting instellen op **Regelartikel**.
    - Als een verkooporderregel vanuit Sales naar Supply Chain Management wordt gesynchroniseerd, wordt het volledige regelkortingsbedrag gebruikt. Omdat in Supply Chain Management geen veld beschikbaar is waarin het volledige kortingsbedrag voor een regel kan worden opgeslagen, wordt het bedrag gedeeld door de hoeveelheid en opgeslagen in het veld **Regelkorting**. Afronding die tijdens deze deling plaatsvindt, wordt opgeslagen in het veld **Verkooptoeslagen** op de verkoopregel.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Voorbeeld: Synchronisatie van Sales naar Supply Chain Management

U hebt de volgende verkooporder:

+ **Sales:** Hoeveelheid = 3, korting per regel = € 10,00
+ **Supply Chain Management:** Hoeveelheid = 3, regel kortingsbedrag = $ 3,33, verkoopkosten = -$ 0,01

Als u de gegevens van Supply Chain Management naar Sales synchroniseert, krijgt u het volgende resultaat:

+ **Supply Chain Management:** Hoeveelheid = 3, regel kortingsbedrag = $ 3,33, verkoopkosten = -$ 0,01
+ **Sales:** Hoeveelheid = 3, korting per regel = = (3 × € 3,33) + € 0,01 = € 10,00

## <a name="dual-write-solution-for-sales"></a>Oplossing Twee keer wegschrijven voor Sales

Nieuwe velden zijn toegevoegd aan de entiteit **Order** en worden weergegeven op de pagina. De meeste van deze velden worden weergegeven op het tabblad **Integratie** in Sales. Er zijn een paar speciale velden:

+ In het veld **Verwerkingsstatus** wordt de verwerkingsstatus weergegeven van de order in Supply Chain Management. Dit veld is vergrendeld en toont alleen de status van de order vanuit Supply Chain Management. De volgende waarden zijn beschikbaar:

    + **Actief**: de status nadat de order is geactiveerd met de knop **Activeren** in Sales.
    + **Bevestigd**
    + **Geleverd**
    + **Gefactureerd**
    + **Gedeeltelijk geleverd**
    + **Gedeeltelijk gefactureerd**
    + **Opgenomen**
    + **Geannuleerd**

    In de volgende tabel wordt aangegeven hoe de verwerkingsstatus wordt toegewezen aan de waarde van de **CRM-statuscode**.

    | Verwerkingsstatus           | CRM-statuscode    |
    |-----------------------------|--------------------|
    | Actief                      | Nieuw/In behandeling/In wachtstand |
    | Bevestigd/opgenomen            | In uitvoering        |
    | Gedeeltelijk geleverd         | Gedeeltelijk            |
    | Geleverd                   | Gereed           |
    | Gefactureerd/Gedeeltelijk gefactureerd | Gefactureerd           |
    | Geannuleerd                    | Geen geld           |

+ De knoppen **Factuur maken** en **Order annuleren** op de pagina **Verkooporder** zijn verborgen in Sales.
+ De waarde voor **Verkooporderstatus** blijft **Actief** om ervoor te zorgen dat wijzigingen vanuit Supply Chain Management naar de verkooporder in Sales kunnen stromen. U stelt dit gedrag in door de standaardwaarde voor **Statuscode \[Status\]** op **Actief** in te stellen.

## <a name="invoices"></a>Facturen

Verkoopfacturen worden gemaakt in Supply Chain Management en gesynchroniseerd met Sales. Let op de volgende punten:

+ Het veld **Factuurnummer** is aan de entiteit **Factuur** toegevoegd en wordt weergegeven op de pagina.
+ De knop **Factuur maken** op de pagina **Verkooporder** is verborgen omdat facturen in Supply Chain Management worden gemaakt en worden gesynchroniseerd naar Sales. De pagina **Factuur** kan niet worden bewerkt omdat facturen vanuit Supply Chain Management worden gesynchroniseerd.
+ De waarde voor **Verkooporderstatus** wordt automatisch in **Gefactureerd** gewijzigd wanneer de bijbehorende factuur vanuit Supply Chain Management is gesynchroniseerd naar Sales. Daarnaast wordt de eigenaar van de verkooporder op basis waarvan de factuur is gemaakt, aangewezen als de eigenaar van de factuur. De eigenaar van de verkooporder kan de factuur dus weergeven.
+ De velden **Leveringscondities**, **Leveringsvoorwaarden** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

## <a name="templates"></a>Sjablonen

Prospect naar contact geld omvat een verzameling basisentiteitstoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

| Finance and Operations-apps | Modelgestuurde apps in Dynamics 365 | Omschrijving |
|-----------------------------|-----------------------------------|-------------|
| Kopteksten van verkoopfacturen V2    | facturen                          |             |
| Verkoopfactuurregels V2      | factuurdetails                    |             |
| CDS-verkooporderkopteksten     | salesorders                       |             |
| CDS-verkooporderregels       | salesorderdetails                 |             |
| Oorsprongcodes van verkooporder    | msdyn\_salesorderorigins          |             |
| CDS-verkoopoffertekoptekst  | offertes                            |             |
| Regels van CDS-verkoopofferte   | quotedetails                      |             |

Dit zijn de gerelateerde kernentiteitstoewijzingen voor prospect naar contant geld:

+ [Klanten V3 naar accounts](customer-mapping.md#customers-v3-to-accounts)
+ [CDS-contactpersonen V2 naar contactpersonen](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Klanten V3 naar contacts](customer-mapping.md#customers-v3-to-contacts)
+ [Vrijgegeven producten V2 naar msdynsharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Alle producten naar msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Prijslijst](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
