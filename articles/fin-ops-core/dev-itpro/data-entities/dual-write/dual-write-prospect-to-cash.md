---
title: Prospect naar contant geld in twee keer wegschrijven
description: Dit artikel biedt informatie over Prospect naar contant geld in twee keer wegschrijven.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: f44574abddb71e1a994ae60960e8c9c79242aff0
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112107"
---
# <a name="prospect-to-cash-in-dual-write"></a>Prospect naar contant geld in twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

Een belangrijk doel van de meeste bedrijven is het converteren van prospects naar klanten en vervolgens een langdurige zakelijke relatie met deze klanten te onderhouden. In Microsoft Dynamics 365-apps vindt het proces Prospect naar contant geld plaats via offertes of orderverwerkingswerkstromen en worden de financiële gegevens afgestemd en verantwoord. Dankzij de integratie van prospect-naar-contact met twee keer wegschrijven wordt er een workflow gemaakt die een offerte en een order combineert die afkomstig zijn uit Dynamics 365 Sales of Dynamics 365 Supply Chain Management, en worden de offerte en de order beschikbaar gemaakt in beide apps.

In de app-interfaces hebt u toegang tot de verwerkingsstatus en factuurgegevens in real-time. Hierdoor kunt u functies zoals productvoorraad, voorraadverwerking en uitvoering van Supply Chain Management eenvoudiger beheren, zonder dat u de offertes en orders opnieuw hoeft te maken.

![Gegevensstroom voor Twee keer wegschrijven in Prospect naar contant geld.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Zie [Geïntegreerd klantmodel](customer-mapping.md) voor informatie over klant- en contactintegratie. Zie [Uniforme productervaring](product-mapping.md) voor informatie over productintegratie.

> [!NOTE]
> In Dynamics 365 Sales verwijzen zowel prospect als klant naar een record in de tabel **Account** waar de kolom **RelationshipType** ofwel **Prospect** of **Klant** is. Als uw bedrijfslogica een kwalificatieproces **Account** bevat waarbij de record **Account** wordt gemaakt en eerst als prospect en daarna als klant wordt gekwalificeerd, wordt deze record alleen met de apps voor financiën en bedrijfsactiviteiten gesynchroniseerd als het een klant (`RelationshipType=Customer`) is. Als u wilt dat de rij **Account** wordt gesynchroniseerd als een prospect, hebt u een aangepaste toewijzing nodig om de prospectgegevens te integreren.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

Voordat u verkoopoffertes kunt synchroniseren, moet u de volgende instellingen bijwerken.

### <a name="setup-in-sales"></a>Instellingen in Sales

Ga in Sales naar **Instellingen \> Beheer \> Systeeminstellingen \> Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:

- De systeemoptie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.
- De kolom **Berekeningsmethode korting** is ingesteld op **Regelartikel**.

### <a name="sites-and-warehouses"></a>Locaties en magazijnen

In Supply Chain Management zijn de kolommen **Locatie** en **Magazijn** vereist voor offerteregels en orderregels. Als u de locatie en het magazijn instelt in de standaardorderinstellingen, worden deze kolommen automatisch ingesteld wanneer u een product toevoegt aan een offerteregel of een orderregel. 

### <a name="number-sequences-for-quotations-and-orders"></a>Nummerreeksen voor offertes en orders

De nummerreeksen voor Supply Chain Management en Sales zijn niet verbonden wanneer offertes en orders worden gemaakt en gesynchroniseerd in Sales en Supply Chain Management. Als een verkooporder die in Sales is gemaakt, wordt gesynchroniseerd met Supply Chain Management, heeft deze hetzelfde verkoopordernummer in Supply Chain Management. Om ervoor te zorgen dat het verkoopordernummer niet wordt gedupliceerd, moet u verschillende nummerreekssystemen in de twee apps gebruiken.

De nummerreeks in Supply Chain Management is bijvoorbeeld **1, 2, 3, 4, 5, ...** en de nummer reeks in Sales is **100, 99, 98, ...**. Als u 100 verkooporders maakt in Sales, wordt er uiteindelijk een ordernummer gegenereerd dat al bestaat in Supply Chain Management. Met andere woorden de twee nummerreeksen overlappen elkaar uiteindelijk als verkooporders worden gemaakt in Supply Chain Management en Sales. In plaats daarvan kunt u een nummerreeks gebruiken zoals **F1, F2, F3, ...** in Supply Chain Management en een nummerreeks zoals **C1, C2, C3 ,...** in Sales. Deze nummerreeksen produceren nooit dubbele verkoopordernummers.

## <a name="sales-quotations"></a>Verkoopoffertes

Verkoopoffertes kunnen worden gemaakt in Sales of Supply Chain Management. Als u een offerte maakt in Sales, wordt deze in realtime gesynchroniseerd met Supply Chain Management. Als u een offerte maakt in Supply Chain Management, wordt deze in realtime gesynchroniseerd met Sales. Let op de volgende punten:

+ U kunt een korting toevoegen aan het product op de offerte. In dit geval wordt de korting gesynchroniseerd met Supply Chain Management. De kolommen **Korting**, **Toeslagen** en **Btw** in de koptekst worden bepaald door een configuratie in Supply Chain Management. Deze instelling biedt momenteel geen ondersteuning voor integratietoewijzing. In het huidige ontwerp worden de kolommen **Prijs**, **Korting**, **Toeslagen** en **Btw** bijgehouden en verwerkt in Supply Chain Management.
+ De kolommen **Kortingspercentage**, **Korting** en **Vrachtkosten** zijn in de koptekst van de verkoopofferte alleen-lezenkolommen.
+ De kolommen **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze kolommen wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de tabel wordt gesynchroniseerd.

Als u ook de Field Service-oplossing gebruikt, moet u de parameter **Snel offerteregel maken** opnieuw inschakelen. Als u de parameter opnieuw inschakelt, kunt u doorgaan met het maken van offerteregels met de functie Snel maken.

1. Ga naar uw Dynamics 365 Sales-toepassing.
2. Selecteer het pictogram Instellingen op de navigatiebalk bovenaan.
3. Selecteer **Geavanceerde instellingen**.
4. Kies de optie **Het systeem aanpassen**.
5. Selecteer de menuopdracht **Offerteregel**.
6. Ga naar de sectie **Gegevensservices** en schakel het selectievakje **Snel maken toestaan** in.

## <a name="sales-orders"></a>Verkooporders

Verkooporders kunnen worden gemaakt in Sales of Supply Chain Management. Als u een verkooporder maakt in Sales, wordt deze in realtime gesynchroniseerd met Supply Chain Management. Als u een verkooporder maakt in Supply Chain Management, wordt deze in realtime gesynchroniseerd met Sales. Let op de volgende punten:

+ Ad-hoc-producten in Dynamics 365 Sales worden weergegeven als productcategorieën in Dynamics 365 Supply Chain Management.
+ Berekening en afronding van korting:

    - Het model voor het berekenen van korting in Sales wijkt af van het model voor het berekenen van korting in Supply Chain Management. In Supply Chain Management kan het uiteindelijke kortingsbedrag op een verkoopregel het resultaat zijn van een combinatie van kortingsbedragen en -percentages. Als dit uiteindelijke kortingsbedrag wordt gedeeld door de hoeveelheid op de regel, kan er afronding plaatsvinden. Deze afronding wordt echter niet gebruikt als een afgerond kortingsbedrag per eenheid wordt gesynchroniseerd naar Sales. Het volledige kortingsbedrag op een verkoopregel in Supply Chain Management kan alleen correct worden gesynchroniseerd naar Sales als het volledige bedrag wordt gesynchroniseerd, zonder het te delen door de regelhoeveelheid. Daarom moet u in Sales de berekeningsmethode voor de korting instellen op **Regelartikel**.
    - Als een verkooporderregel vanuit Sales naar Supply Chain Management wordt gesynchroniseerd, wordt het volledige regelkortingsbedrag gebruikt. Omdat in Supply Chain Management geen kolom beschikbaar is waarin het volledige kortingsbedrag voor een regel kan worden opgeslagen, wordt het bedrag gedeeld door de hoeveelheid en opgeslagen in de kolom **Regelkorting**. Afronding die tijdens deze deling plaatsvindt, wordt opgeslagen in de kolom **Verkooptoeslagen** op de verkoopregel.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Voorbeeld: Synchronisatie van Sales naar Supply Chain Management

U hebt de volgende verkooporder:

+ **Sales:** Hoeveelheid = 3, korting per regel = € 10,00
+ **Supply Chain Management:** Hoeveelheid = 3, regel kortingsbedrag = $ 3,33, verkoopkosten = -$ 0,01

Als u de gegevens van Supply Chain Management naar Sales synchroniseert, krijgt u het volgende resultaat:

+ **Supply Chain Management:** Hoeveelheid = 3, regel kortingsbedrag = $ 3,33, verkoopkosten = -$ 0,01
+ **Sales:** Hoeveelheid = 3, korting per regel = = (3 × € 3,33) + € 0,01 = € 10,00

## <a name="dual-write-solution-for-sales"></a>Oplossing Twee keer wegschrijven voor Sales

Nieuwe kolommen zijn toegevoegd aan de tabel **Order** en worden weergegeven op de pagina. De meeste van deze kolommen worden weergegeven op het tabblad **Integratie** in Sales. Zie [De toewijzing voor de statuskolommen van de verkooporder instellen](sales-status-map.md) voor meer informatie over de manier waarop de statuskolommen worden toegewezen.

+ De knoppen **Factuur maken** en **Order annuleren** op de pagina **Verkooporder** zijn verborgen in Sales.
+ De waarde voor **Verkooporderstatus** blijft **Actief** om ervoor te zorgen dat wijzigingen vanuit Supply Chain Management naar de verkooporder in Sales kunnen stromen. U stelt dit gedrag in door de standaardwaarde voor **Statuscode \[Status\]** op **Actief** in te stellen.

## <a name="invoices"></a>Facturen

Verkoopfacturen worden gemaakt in Supply Chain Management en gesynchroniseerd met Sales. Let op de volgende punten:

+ De kolom **Factuurnummer** is aan de tabel **Factuur** toegevoegd en wordt weergegeven op de pagina.
+ De knop **Factuur maken** op de pagina **Verkooporder** is verborgen omdat facturen in Supply Chain Management worden gemaakt en worden gesynchroniseerd naar Sales. De pagina **Factuur** kan niet worden bewerkt omdat facturen vanuit Supply Chain Management worden gesynchroniseerd.
+ De waarde voor **Verkooporderstatus** wordt automatisch in **Gefactureerd** gewijzigd wanneer de bijbehorende factuur vanuit Supply Chain Management is gesynchroniseerd naar Sales. Daarnaast wordt de eigenaar van de verkooporder op basis waarvan de factuur is gemaakt, aangewezen als de eigenaar van de factuur. De eigenaar van de verkooporder kan de factuur dus weergeven.
+ De kolommen **Leveringscondities**, **Leveringsvoorwaarden** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze kolommen wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de tabel wordt gesynchroniseerd.

## <a name="templates"></a>Sjablonen

Prospect naar contact geld omvat een verzameling basistabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

| Apps voor financiën en bedrijfsactiviteiten | Customer Engagement-apps | Description |
|-----------------------------|-----------------------------------|-------------|
[Alle producten](mapping-reference.md#138) | msdyn_globalproducts | |
[Klanten V3](mapping-reference.md#101) | rekeningen | |
[Klanten V3](mapping-reference.md#116) | contacten | |
[Contactpersonen V2](mapping-reference.md#221) | msdyn_contactforparties | |
[CDS-verkooporderkopteksten](mapping-reference.md#217) | salesorders | |
[CDS-verkooporderregels](mapping-reference.md#216) | salesorderdetails | |
[CDS-verkoopoffertekoptekst](mapping-reference.md#215) | offertes | |
[Regels van CDS-verkoopofferte](mapping-reference.md#214) | quotedetails | |
[Vrijgegeven producten V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[Kopteksten van verkoopfacturen V2](mapping-reference.md#118) | facturen | De tabel Kopteksten van verkoopfacturen V2 in de apps voor financiën en bedrijfsactiviteiten bevat facturen voor verkooporders en vrije-tekstfacturen. Er wordt een filter toegepast in Dataverse voor twee keer wegschrijven waarmee alle vrije-tekstfactuurdocumenten worden uitgefilterd. |
[Verkoopfactuurregels V2](mapping-reference.md#117) | factuurdetails | |
[Oorsprongcodes van verkooporder](mapping-reference.md#186) | msdyn_salesorderorigins | |

Zie [Geharmoniseerde productervaring](product-mapping.md) voor informatie over prijslijsten.

## <a name="limitations"></a>Beperkingen

- Retourorders worden niet ondersteund.
- Creditnota's worden niet ondersteund.
- Financiële dimensies moeten worden ingesteld voor de hoofdgegevens, bijvoorbeeld klant en leverancier. Wanneer een klant wordt toegevoegd aan een offerte of verkooporder, worden de financiële dimensies die aan de klantrecordstroom zijn gekoppeld, automatisch aan de order toegevoegd. Op dit moment bevat twee keer wegschrijven geen financiële dimensiegegevens voor hoofdgegevens.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

