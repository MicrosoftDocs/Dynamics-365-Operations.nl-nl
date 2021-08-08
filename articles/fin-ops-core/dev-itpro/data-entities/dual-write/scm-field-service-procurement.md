---
title: Inkoop integreren tussen Supply Chain Management en Field Service
description: In dit onderwerp wordt beschreven hoe met integratie van twee keer wegschrijven het maken van inkooporders en updates van zowel Supply Chain Management als Field Service worden ondersteund.
author: RamaKrishnamoorthy
ms.date: 11/11/2020
ms.topic: article
audience: Application User
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c29efb885babea833e3c3fde0155e3722f8b77e9
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542386"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Inkoop integreren tussen Supply Chain Management en Field Service

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management biedt krachtige inkoopfunctionaliteit. Dynamics 365 Field Service biedt vergelijkbare functionaliteit waarmee de inkoopprocessen worden ondersteund die aan het serviceproces zijn gekoppeld. De functionaliteit in deze twee apps wordt geïntegreerd via twee keer wegschrijven en de resulterende gebruikstoepassingen voor meerdere functies worden ingeschakeld via tabeltoewijzingen, oplossingslogica, weergaven en formulieren.

Deze integratie ondersteunt het maken van inkooporders en in de meeste gevallen updates van beide apps. Met Supply Chain Management worden echter prijzen, adressen en productontvangstbonnen beheerd. Verschillende krachtige gebruikstoepassingen voor meerdere functies worden ingeschakeld voor organisaties die zowel Field Service als Supply Chain Management gebruiken. Dankzij deze gebruikstoepassingen kan inkoop worden geïnitieerd en getraceerd in beide systemen.

De onderstaande afbeelding bevat de tabellen in beide systemen en laat zien hoe ze aan elkaar worden toegewezen. Inkooporders in Field Service verwijzen naar een *rekening*-rij, terwijl inkooporders in Supply Chain Management naar een *leverancier*-rij verwijzen. Voor de integratie wordt voor twee keer wegschrijven een verwijzing gebruikt om *leverancier*-rijen aan *rekening*-rijen te koppelen. Zie [Model voor geïntegreerde leveranciers](vendor-mapping.md) voor meer informatie.

![Toewijzingen voor inkoop.](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Vereisten

Als u Supply Chain Management wilt integreren met Field Service, moet u de volgende onderdelen installeren:

- Field Service versie 8.8.31.60 of hoger voor uitgebreide integratie van inkooporders
- Supply Chain Management versie 10.0.14 of hoger
- Twee keer wegschrijven, om de OneFSSCM-oplossing uit te voeren

## <a name="installation-guidelines"></a>Richtlijnen voor installatie

### <a name="prerequisites"></a>Vereisten

- **Twee keer wegschrijven**: zie [de startpagina van Twee keer wegschrijven](dual-write-home-page.md#dual-write-setup) voor meer informatie.
- **Dynamics 365 Field Service**: zie [Dynamics 365 Field Service installeren](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service) voor meer informatie.

Wanneer deze functies zijn ingeschakeld in Microsoft Dataverse, worden met Twee keer wegschrijven en Field Service verschillende oplossingslagen geïntroduceerd die de omgeving uitbreiden met nieuwe metagegevens, formulieren, weergaven en logica. Deze oplossingen kunnen in elke volgorde worden ingeschakeld, maar meestal installeert u ze in de hier opgegeven volgorde:

1. **Field Service Common**: Field Service Common wordt geïnstalleerd wanneer Field Service in de omgeving wordt geïnstalleerd.
2. **Field Service (Anchor)**: Field Service (Anchor) wordt geïnstalleerd wanneer Field Service in de omgeving wordt geïnstalleerd. 
3. **Supply Chain Management Extended**: Supply Chain Management Extended wordt automatisch geïnstalleerd wanneer Twee keer wegschrijven wordt ingeschakeld in een omgeving. 
4. **OneFSSCM-oplossing**: OneFSSCM wordt automatisch geïnstalleerd door de oplossing (Field Service of Supply Chain Management) die als laatste wordt geïnstalleerd.

    - Als Field Service al in de omgeving is geïnstalleerd en u Twee keer wegschrijven inschakelt, waarmee Supply Chain Management Extended wordt geïnstalleerd, wordt OneFSSCM geïnstalleerd.
    - Als Supply Chain Management Extended al in de omgeving is geïnstalleerd en u Field Service installeert, wordt OneFSSCM geïnstalleerd.

## <a name="initial-synchronization"></a>Initiële synchronisatie

Als u nieuwe inkooporders wilt maken en wilt werken met bestaande inkooporders, moet u de verwijzingsgegevens synchroniseren tussen Supply Chain Management en Dataverse. U gebruikt de oorspronkelijke schrijffunctionaliteit om de tabelrelaties te detecteren en de tabellen te vinden die u voor een bepaalde toewijzing moet inschakelen.

U moet de volgende tabellen synchroniseren:

- Productsjablonen

    Wanneer u de initiële schrijfbewerking uitvoert, krijgt u een volledige lijst met de tabellen die vereist zijn. Dit zijn enkele voorbeelden van deze sjablonen:

    - Alle producten
    - Vrijgegeven producten V2
    - Door Dataverse vrijgegeven verschillende producten

- Vestigingen
- Magazijnen
- Sjablonen voor inkoopcategorieën

    Dit zijn enkele voorbeelden van deze sjablonen:

    - inkoopcategorieën
    - Pro
    - Categoriehiërarchie van product
    - Toewijzingen van productcategorieën

- Leverancierssjablonen, zoals Leverancier V2
- Sjablonen voor contactpersonen, zoals Dataverse Contactpersonen V2
- Medewerkerssjablonen, zoals Medewerker

Synchronisatie van de tabellen zorgt ervoor dat alle documenten (inkooporders en productontvangstbonnen) in Supply Chain Management beschikbaar zijn in Dataverse.

### <a name="account-and-vendor-tables"></a>Tabellen Rekening en Leverancier

Inkooporders in Field Service worden gebaseerd op de tabel Rekening om leveranciers bij te houden. Daarom worden in Dataverse-tabellen voor inkooporders rekeningen gebruikt om leveranciers bij te houden. Met het oog op dit belangrijke verschil moeten de volgende vier werkstromen worden geactiveerd om de rekeningen en leveranciers gesynchroniseerd te houden: 

- Leveranciers maken in tabel Rekeningen
- Leveranciers maken in tabel Leveranciers
- Leveranciers bijwerken in tabel Rekeningen
- Leveranciers bijwerken in tabel Leveranciers

Als OneFSSCM is geïnstalleerd, omdat zowel Field Service als Supply Chain Management Extended zijn geïnstalleerd, worden deze werkstromen automatisch geactiveerd. Als Field Service niet is geïnstalleerd, maar u de inkoopordertabellen wel wilt integreren met Dataverse, moet u deze werkstromen activeren. In beide gevallen moet u er, tenzij u helemaal opnieuw begint, voor zorgen dat alle leveranciers worden gemaakt als rekeningen in Dataverse voordat u inkooporders maakt. Anders kunnen er fouten optreden.

### <a name="initial-synchronization"></a>Initiële synchronisatie

Wanneer aan alle vereisten is voldaan, moet u eerst de volgende sjablonen synchroniseren als u wilt dat bestaande inkooporders en productontvangstbonnen op beide systemen beschikbaar zijn:

- Inkooporderkoptekst V2
- CDS-inkooporderregel
- CDS-inkooporderregel zacht verwijderen
- Ontvangst inkooporder
- Productontvangst inkooporder

## <a name="mappings-with-logic"></a>Toewijzingen met logica

Met de inkoopintegratie wordt de producttoewijzing uitgebreid met de volgende logica om ervoor te zorgen dat de kolom **Producttype Field Service** correct wordt ingesteld in de producttabel in Dataverse:

- Als **Producttype** wordt ingesteld op *Product* en **Artikelmodelgroep, Product in voorraad** wordt ingesteld op *Waar*, wordt **Producttype Field Service** ingesteld op *Voorraad*.
- Als **Producttype** wordt ingesteld op *Product* en **Artikelmodelgroep, Product in voorraad** wordt ingesteld op *Onwaar*, wordt **Producttype Field Service** ingesteld op *Niet-voorraad*.
- Als **Producttype** wordt ingesteld op *Service*, wordt **Producttype Field Service** ingesteld op *Service*.

Daarnaast bevat Dataverse logica waarmee leveranciers aan hun gerelateerde rekeningen worden toegewezen. Met deze logica wordt de standaard factuurleveranciersrekening ingesteld. Bij het maken wordt met de logica van de serverinvoegtoepassing de standaard factuurleveranciersrekening ingesteld op basis van de leverancier die aan de rekening is gerelateerd. De leverancier heeft een verwijzing naar de factuurrekening die wordt gebruikt om deze waarde in te stellen.

## <a name="supported-scenarios"></a>Ondersteunde scenario's

- Inkooporders kunnen door gebruikers van Dataverse worden gemaakt en bijgewerkt. Het proces en de gegevens worden echter bepaald door Supply Chain Management. De beperkingen voor updates van inkooporderkolommen in Supply Chain Management zijn van toepassing wanneer updates afkomstig zijn van Field Service. U kunt bijvoorbeeld een inkooporder niet bijwerken als deze is voltooid. 
- Als de inkooporder wordt beheerd door wijzigingsbeheer in Supply Chain Management, kan een Field Service-gebruiker de inkooporder alleen bijwerken als de goedkeuringsstatus van Supply Chain Management *Concept* is.
- Verschillende kolommen worden alleen door Supply Chain Management beheerd en kunnen niet worden bijgewerkt in Field Service. Als u wilt weten welke kolommen niet kunnen worden bijgewerkt, controleert u de toewijzingstabellen in het product. De meeste kolommen zijn voor het gemak ingesteld op alleen-lezen op Dataverse-pagina's. 

    Zo worden de kolommen voor prijsgegevens beheerd door Supply Chain Management. Supply Chain Management heeft handelsovereenkomsten waarvan Field Service gebruik kan maken. Kolommen, zoals **Eenheidsprijs**, **Korting** en **Nettobedrag**, zijn alleen afkomstig uit Supply Chain Management. Als u ervoor wilt zorgen dat de prijs wordt gesynchroniseerd met Field Service, moet u de functie **Synchroniseren** gebruiken op de pagina's **Inkooporder** en **Product inkooporder** in Dataverse wanneer inkoopordergegevens zijn ingevoerd. Zie [Synchroniseren met de inkoopgegevens op aanvraag van Dynamics 365 Supply Chain Management](#sync-procurement) voor meer informatie.

- De kolom **Totalen** is alleen beschikbaar in Field Service omdat er geen actuele totalen zijn van de inkooporder in Supply Chain Management. De totalen in Supply Chain Management worden berekend op basis van meerdere parameters die niet beschikbaar zijn in Field Service.
- Inkooporderregels waarin alleen een inkoopcategorie wordt opgegeven of waarin het opgegeven product een artikel is van het producttype *Service* of het producttype Field Service, kan alleen worden gestart in Supply Chain Management. De regels worden vervolgens gesynchroniseerd met Dataverse en zijn zichtbaar in Field Service.
- Als alleen Field Service is geïnstalleerd, en Supply Chain Management niet, is de kolom **Magazijn** verplicht voor de inkooporder. Als Supply Chain Management is geïnstalleerd, is dit echter niet nodig, omdat Supply Chain Management inkooporderregels kan bevatten waarin geen magazijn wordt opgegeven in bepaalde situaties.
- Productontvangstbonnen (inkooporderontvangstbonnen in Dataverse) worden beheerd door Supply Chain Management en kunnen niet worden gemaakt vanuit Dataverse als Supply Chain Management is geïnstalleerd. De productontvangstbonnen van Supply Chain Management worden gesynchroniseerd vanuit Supply Chain Management met Dataverse.
- Minderlevering is toegestaan in Supply Chain Management. Met de OneFSSCM-oplossing wordt logica toegevoegd zodat wanneer de productontvangstbonregel (of inkooporderontvangstproduct in Dataverse) wordt gemaakt of bijgewerkt, een voorraadjournaalrij wordt gemaakt in Dataverse om de resterende hoeveelheid die in bestelling is voor scenario's van minderlevering aan te passen.

## <a name="unsupported-scenarios"></a>Niet-ondersteunde scenario's

- Field Service voorkomt dat regels worden toegevoegd aan een geannuleerde inkooporder in Supply Chain Management. Als oplossing kunt u de systeemstatus van de inkooporder wijzigen in Field Service en vervolgens de nieuwe regel toevoegen in Field Service of Supply Chain Management.
- Hoewel inkooprijen van invloed zijn op voorraadniveaus in beide systemen, zorgt deze integratie niet voor de uitlijning van de voorraad in Supply Chain Management en Field Service. Zowel Field Service als Supply Chain Management hebben andere processen waarmee voorraadniveaus worden bijgewerkt. Deze processen vallen buiten de scope van de inkoop.

## <a name="status-management"></a>Statusbeheer

De statuswaarden van inkooporders in Field Service verschillen van de statuswaarden in Supply Chain Management.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Statuswaarden van Field Service-inkooporder en -inkooporderproduct

| Koptekst – systeemstatus | Koptekst - goedkeuringsstatus | Artikelstatus |
|---|---|---|
| <ul><li>Concept</li><li>Ingediend</li><li>Geannuleerd</li><li>Product ontvangen</li><li>Gefactureerd</li></ul> | <ul><li>Null</li><li>Goedgekeurd</li><li>Afgewezen</li></ul> | <ul><li>In behandeling</li><li>Ontvangen</li><li>Geannuleerd</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Statuswaarden van Supply Chain Management-inkooporder en -inkooporderregel

Regelgoedkeuringsstatussen zijn alleen actief wanneer er een regelwerkstroom is.

| Koptekst – documentstatus | Koptekst - goedkeuringsstatus | Regelstatus | Regelgoedkeuringsstatus |
|---|---|---|---|
| <ul><li>Openstaande order (nabestelling)</li><li>Ontvangen</li><li>Gefactureerd</li><li>Geannuleerd</li></ul> | <ul><li>Concept</li><li>Wordt gecontroleerd</li><li>Goedgekeurd</li><li>Afgewezen</li><li>In externe controle</li><li>Bevestigd</li><li>Voltooid </li></ul> | <ul><li>Openstaande order (nabestelling)</li><li>Ontvangen</li><li>Gefactureerd</li><li>Geannuleerd</li></ul> | <ul><li>Niet ingediend</li><li>Wordt gecontroleerd</li><li>Goedgekeurd</li><li>Afgewezen</li></ul> |

De volgende regels worden toegepast op de statuskolommen:

- De status in Supply Chain Management kan niet worden bijgewerkt vanuit Field Service. In sommige gevallen wordt de status in Field Service echter bijgewerkt wanneer de inkooporderstatus in Supply Chain Management wordt gewijzigd.
- Als een inkooporder in Supply Chain Management onder wijzigingsbeheer valt en er een wijziging wordt verwerkt, is de goedkeuringsstatus *Concept* of *Wordt gecontroleerd*. In dit geval wordt de goedkeuringsstatus van Field Service ingesteld op *Null*.
- Als de goedkeuringsstatus van de inkooporder in Supply Chain Management is ingesteld op *Goedgekeurd*, *In externe controle*, *Bevestigd* of *Voltooid*, wordt de goedkeuringsstatus van de inkooporder van Field Service ingesteld op *Goedgekeurd*.
- Als de goedkeuringsstatus van de inkooporder in Supply Chain Management is ingesteld op *Afgewezen*, wordt de goedkeuringsstatus van de inkooporder van Field Service ingesteld op *Afgewezen*.
- Als de status van de documentkoptekst in Supply Chain Management wordt gewijzigd in *Openstaande order (nabestelling)* en de inkooporderstatus van Field Service *Concept* of *Geannuleerd* is, wordt de status van de inkooporder van Field Service gewijzigd in *Verzonden*.
- Als de status van de documentkoptekst in Supply Chain Management wordt gewijzigd in *Geannuleerd* en er geen inkooporderontvangstproducten in Field Service zijn gekoppeld aan de inkooporder (via inkooporderproducten), wordt de systeemstatus van Field Service ingesteld op *Geannuleerd*.
- Als de status van de inkooporderregel in Supply Chain Management *Geannuleerd* is, wordt de status van het inkooporderproduct in Field Service ingesteld op *Geannuleerd*. Als de status van de inkooporderregel in Supply Chain Management wordt gewijzigd van *Geannuleerd* in *Nabestelling*, wordt de status van het productartikel van de inkooporder in Field Service bovendien ingesteld op *In behandeling*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Op verzoek synchroniseren met de Supply Chain Management-inkoopgegevens

Supply Chain Management bevat inkoopgegevens voor de afhandeling van handelsovereenkomsten, kortingen en andere scenario's die gebaseerd zijn op secundaire processen in Supply Chain Management. De inkoopengine gebruikt complexe regels om de beste prijs voor een bepaalde inkooporder te bepalen. Wanneer u twee keer wegschrijven gebruikt, worden gegevens in de twee omgevingen niet altijd synchroon gehouden, met name in scenario's waarin de rij is gemaakt of bijgewerkt vanuit Dataverse en opvolgingsprocessen in Supply Chain Management kunnen worden geactiveerd.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>De inkoopgegevens synchroniseren vanuit Supply Chain Management

1. Ga in Dataverse naar **Voorraad \> Inkooporder**.
2. Selecteer **Nieuw** om een nieuwe inkooporder te maken of selecteer de rij voor een bestaande inkooporder.
3. Vanuit de inkooporder of inkooporderregel.
4. Selecteer **Synchroniseren** in het actievenster.

Alle kolommen van Dataverse en Field Service die worden gedeeld door Supply Chain Management, worden gesynchroniseerd.

Dit zijn de situaties waarin u de functie **Synchroniseren** kunt gebruiken:

- Als u meerdere opeenvolgende wijzigingen in dezelfde rij aanbrengt vanuit Dataverse, voert u de functie **Synchroniseren** uit.
- Als u niet weet of een wijziging de tweede opeenvolgende wijziging vanuit Dataverse is, kan het zinvol zijn om de functie **Synchroniseren** uit te voeren.
- Als u een foutbericht ontvangt over het bijwerken van een waarde vanuit Supply Chain Management, voert u de functie **Synchroniseren** uit en probeert u vervolgens de update opnieuw in Dataverse.

## <a name="cancelling-the-posting-process"></a>Het boekingsproces annuleren

Als het boekingsproces voor de productontvangstbon tijdens de verwerking wordt geannuleerd, wordt er met twee keer wegschrijven mogelijk een rij met productontvangstbonnen gemaakt in Dataverse, maar geen rij met productontvangstbonnen in Supply Chain Management. Dit doet zich voor omdat twee keer wegschrijven geen gedistribueerde transacties ondersteunt.

## <a name="templates"></a>Sjablonen

De volgende sjablonen zijn beschikbaar voor de integratie van inkoopgerelateerde documenten.

| Supply Chain Management | Field Service | Beschrijving |
|---|---|---|
| [Inkooporderkoptekst V2](mapping-reference.md#183) | msdyn\_Purchaseorders | Deze tabel bevat de kolommen die de inkooporderkoptekst vertegenwoordigen. |
| [Entiteit voor inkooporderregel](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | Deze tabel bevat de rijen die de regels op een inkooporder vertegenwoordigen. Het productnummer wordt gebruikt voor synchronisatie. Hiermee wordt het product geïdentificeerd als voorraadeenheid (SKU), inclusief productdimensies. Zie [Uniforme productervaring](product-mapping.md) voor meer informatie over productintegratie met Dataverse. |
| [Koptekst productontvangstbon](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | Deze tabel bevat de kopteksten van de productontvangstbonnen die worden gemaakt wanneer er een productontvangstbon in Supply Chain Management wordt geboekt. |
| [Productontvangstbonregel](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | Deze tabel bevat de regels van de productontvangstbonnen die worden gemaakt wanneer er een productontvangstbon in Supply Chain Management wordt geboekt. |
| [Zacht verwijderde entiteit voor inkooporderregel](mapping-reference.md#182) | msdyn\_purchaseorderproducts | Deze tabel bevat informatie over inkooporderregels die zacht worden verwijderd. Een inkooporderregel in Supply Chain Management kan alleen zacht worden verwijderd als de inkooporder is bevestigd of goedgekeurd als wijzigingsbeheer is ingeschakeld. De rij is aanwezig in de Supply Chain Management-database en is gemarkeerd als **IsDeleted**. Omdat er geen concept van zachte verwijdering bestaat in Dataverse, is het belangrijk dat deze informatie wordt gesynchroniseerd met Dataverse. Op deze manier kunnen regels die zacht worden verwijderd in Supply Chain Management, automatisch worden verwijderd uit Dataverse. In dit geval bevindt de logica voor het verwijderen van een regel in Dataverse zich in Supply Chain Management Extended. |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
