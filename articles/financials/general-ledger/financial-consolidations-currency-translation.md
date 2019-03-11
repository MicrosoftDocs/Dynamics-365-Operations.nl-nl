---
title: Financiële consolidaties en valutaomzetting
description: Dit onderwerp beschrijft financiële consolidaties en valutaomrekening in het grootboek.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 8427d53bac3216d362b2bf8983a847f069351b3b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "353995"
---
# <a name="financial-consolidations-and-currency-translation"></a>Financiële consolidaties en valutaomzetting

[!include [banner](../includes/banner.md)]

In dit onderwerp maakt u kennis met de benadering die Microsoft Dynamics 365 for Finance and Operations en financiële rapportage gebruiken voor consolidaties. Het beschrijft scenario's voor het rapporteren van meerdere bedrijven, aggregatie, schrapping en minderheidsbelang. Ook wordt uitgelegd hoe u speciale situaties kunt afhandelen, zoals scenario's waarin rechtspersonen verschillende fiscale perioden of verschillende rekeningschema's hebben.

Dit onderwerp is geschreven voor gebruikers en functionele consultants en er wordt vanuit gegaan dat lezers een algemeen begrip van Finance and Operations en Financiële rapportage hebben. Basisinstellingen worden niet behandeld.

> [!NOTE]
> De term *rechtspersoon* wordt gebruikt in Finance and Operations en de term *bedrijf* wordt gebruikt in financiële rapportage. Beide termen worden gebruikt in dit onderwerp. Echter met betrekking tot dit onderwerp is de betekenis ervan hetzelfde.

## <a name="audience"></a>Doelgroep
Dit onderwerp is bedoeld voor gebruikers en toepassingsconsultants die zich bezighouden met financiën en boekhouding, die Finance and Reporting en Financiële rapportage willen gebruiken voor het consolideren van gegevens voor meerdere bedrijven en meerdere valuta´s.

## <a name="approach"></a>Methode
In Finance and Operations wordt een aparte rechtspersoon gebruikt voor de verwerking van een consolidatie. Hiermee is consolidatie van één instantie mogelijk, maar bestaat er ook de mogelijkheid om gegevens uit andere bronnen te halen. Het consolidatieproces moet elke keer worden uitgevoerd wanneer er wijzigingen worden aangebracht in de bronrechtspersonen.

Met Financiële rapportage kunnen meerdere bedrijven worden geconsolideerd tijdens het genereren van rapporten. Hoewel de gegevens worden opgeslagen in een datamart, een versienummer krijgen en kunnen worden geëxporteerd, is elk bronbedrijf de eigenaar en houder van de gegevens. Het rapport kan op elk gewenst moment worden uitgevoerd, zelfs elke minuut (bijvoorbeeld). Deze methode biedt vele extra voordelen, zoals de mogelijkheid om in te zoomen op alle bedrijven en dimensies.

Gebruikers kunnen Online consolideren, Financiële rapportage of een combinatie gebruiken. Hun keuze hangt af van de behoeften van hun bedrijf en de voorkeuren van hun auditoren.

## <a name="consolidations"></a>Consolidaties
De module **Consolidaties** bevat opties voor het consolideren van meerdere rechtspersonen tijdens het consolidatieproces en voor importeren of exporteren van het saldo van een bedrijf. U kunt ook schrappingen instellen en schrappingsjournalen boeken.

## <a name="benefits-of-using-consolidate-online"></a>Voordelen van het gebruik van Online consolideren
Klanten die gebruikmaken van de module **Consolidaties** hebben verschillende voordelen:

- **Diepte van gegevens**: u kunt geconsolideerde rapporten maken die werkelijke en gebudgetteerde gegevens zowel op rekeningniveau als op dimensieniveau samenbrengen.
- **Dynamische consolidaties**: consolidaties kunnen meerdere keren worden verwerkt.
- **Controlecapaciteiten**: dimensies en rekeningen worden beheerd voor analyse en controle, en saldi worden per datum gemaakt.
- **Valutaomrekening**: u kunt de rekeningbereiken en koersen instellen voor omrekening van de valuta voor boekhouding van het bronbedrijf naar de valuta voor boekhouding van het consolidatiebedrijf.
- **Schrappingen in een geconsolideerd bedrijf of eliminatiebedrijf verwerken**: tijdens de consolidatie kunt u schrappingen in één proces verwerken en boeken. U kunt een voorstel ook afzonderlijk uitvoeren.

## <a name="supported-consolidation-scenarios"></a>Ondersteunde consolidatiescenario's
Hier volgen enkele consolidatiescenario's die met Online consolideren worden ondersteund:

- Consolidaties op één niveau voor rechtspersonen
- Consolidaties die betrekking hebben op schrappingen
- Minderheidsbelang (in dit scenario moeten handmatige berekening en invoer in het bedrijf worden gebruikt.)
- Meerdere rekeningschema's voor rechtspersonen
- Verschillende fiscale kalenders voor meerdere rechtspersonen
- Consolidaties die betrekking hebben op meerdere rapportagevaluta's

## <a name="legal-entity-setup"></a>Rechtspersoon instellen
Voordat u een consolidatie verwerkt, moet u de rechtspersoon instellen. U kunt consolidatie zo vaak als nodig is uitvoeren en alle gegevens worden omgerekend van de valuta voor boekhouding van het bronbedrijf naar de valuta die is gedefinieerd voor het consolidatiebedrijf. Daarom moet u voor de volgende organisatiestructuur, als u alle Noord-Amerikaanse bedrijven eerst naar Amerikaanse dollars (USD) en vervolgens naar de euro (EUR), de valuta van het moederbedrijf, moet omrekenen, ten minste twee consolidatiebedrijven hebben.

![Organisatiestructuur](./media/organizational-structure.png "Organisatiestructuur")

In de voorgaande organisatiestructuur moet u een rechtspersoon voor de Noord-Amerikaanse consolidatie hebben, omdat consolidaties altijd van de valuta voor boekhouding van het bronbedrijf naar de valuta van het consolidatiebedrijf worden geconsolideerd. In het voorbeeld worden, als alle bedrijven zijn opgenomen in één consolidatie, de Mexicaanse dochtermaatschappij omgerekend van Mexicaanse peso's (MXN) naar EUR en niet van MXN naar USD naar EUR.

Wanneer u de rechtspersoon maakt, kunt u opgeven of het bedrijf wordt gebruikt voor zowel het consolidatieproces als het schrappingsproces of slechts voor een van deze processen. In de volgende afbeelding wordt het bedrijf voor beide processen gebruikt. Houd er rekening mee dat u geen dagelijkse journalen in een consolidatiebedrijf kunt boeken, maar u kunt ze wel in een eliminatiebedrijf boeken. Daarom wilt u wellicht een afzonderlijk eliminatiebedrijf hebben.

![Rechtspersoon die wordt gebruikt voor zowel consolidatie als schrapping](./media/sep-elimination-company.png "Rechtspersoon die wordt gebruikt voor zowel consolidatie als schrapping")

## <a name="main-accounts-and-consolidation-account-groups"></a>Hoofdrekeningen en consolidatierekeninggroepen
Eén keuze die u moet maken, is hoe u uw rekeningschema wilt consolideren. U hebt drie opties voor het consolideren van hoofdrekeningen tijdens het consolidatieproces.

De eerste optie is het gebruik van de hoofdrekeningen van de bronbedrijven. In dit geval wordt elke rekening van alle bedrijven geconsolideerd. Als bijvoorbeeld Contant geld rekening 100000 in het bedrijf USMF is en rekening 1100 in het bedrijf DEMF, worden beide rekeningen in het consolidatiebedrijf opgenomen. Elke rekening heeft een respectief saldo.

De tweede optie bestaat eruit een standaardrekening voor consolidatie op te geven op de pagina **Hoofdrekeningen**. De rekening wordt vervolgens toegewezen aan de consolidatierekening. Deze optie kan handig zijn wanneer u verschillende rekeningschema's hebt of moet toewijzen aan een rekeningschema dat is gedefinieerd door het hoofdkantoor.

![Standaardconsolidatierekening opgegeven op de pagina Hoofdrekeningen](./media/main-accounts.png "Standaardconsolidatierekening opgegeven op de pagina Hoofdrekeningen")

De derde optie is het gebruik van consolidatierekeninggroepen. U kunt zoveel consolidatierekeninggroepen als nodig zijn definiëren. Vervolgens wijst u op de pagina **Aanvullende consolidatierekeningen** de hoofdrekening uit het rekeningschema toe aan de rekening die u nodig hebt voor die groep.

![Toewijzing op de pagina Aanvullende consolidatierekeningen](./media/additional-consolidation-accounts.png "Toewijzing op de pagina Aanvullende consolidatierekeningen")

## <a name="consolidating-online"></a>Online consolideren
Zie voor informatie over het invoeren van details van online consolidaties [Online consolideren](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Consolidatietransacties beheren
Als u de resultaten van de consolidatie wilt bekijken, hebt u meerdere opties:

- Genereer een financieel rapport voor het consolidatiebedrijf.
- Controleer de lijstpagina **Proefbalans** in het consolidatiebedrijf.
- Geef in de lijst met consolidatietransacties op de pagina **Consolidaties** de saldi weer die per datum zijn gemaakt voor elk bronbedrijf voor elke periode.

    ![Consolidatietransacties op de pagina Consolidaties](./media/managing-consolidation-transactions.png "Consolidatietransacties op de pagina Consolidaties")

Als u de consolidatie opnieuw wilt uitvoeren, kunt u de consolidatie gewoon verwerken. U kunt ook eerst **Transacties verwijderen** op de pagina **Consolidaties** selecteren.

## <a name="consolidate-with-import"></a>Consolidatie met import
De functionaliteit Consolidatie met import werkt net als de functionaliteit Online consolideren. Wanneer u de rechtspersonen selecteert, bladert u naar het bronbestand dat de gegevens bevat.

## <a name="export-company-balances"></a>Saldi exportbedrijf
De functionaliteit Bedrijfssaldi exporteren werkt ook net als de functionaliteit Online consolideren. Wanneer u de rechtspersonen selecteert, stelt u een bestandspad voor de uitvoer in.

## <a name="elimination-rules"></a>Schrappingregels
U kunt een schrappingsregel maken als u intercompany-transacties schrapt. U kunt ook een handmatige schrappingsvermelding uitvoeren in een bedrijf dat is aangewezen als eliminatiebedrijf. Als u een schrappingsregel maakt, hebt u twee opties voor de schrappingsmethode: **Nettowijziging** en **Vast**.

### <a name="set-up-elimination-rules"></a>Schrappingregels instellen
Wanneer u schrappingsregels in Finance and Operations instelt, kunt u een financiële dimensie maken die speciaal voor schrapping wordt gebruikt. De meeste klanten noemen deze financiële dimensie **Handelspartner** of iets dergelijks. Als u besluit geen financiële dimensie te gebruiken, moet u ervoor zorgen dat u hoofdrekeningen hebt die alleen voor intercompany-transacties worden gebruikt.

De instellingen voor schrappingen vindt u in het gedeelte **Instellen** van de module **Consolidaties**. Nadat u een omschrijving voor de regel hebt ingevoerd, moet u het bedrijf selecteren waarnaar het schrappingsjournaal wordt geboekt. Voor het bedrijf dat u selecteert, moet **Gebruiken voor proces voor financiële schrapping** zijn ingeschakeld in de instellingen van de rechtspersoon.

U kunt indien nodig de datum instellen waarop de schrappingsregel van kracht wordt en de datum waarop deze verloopt. U moet de optie **Actief** instellen op **Ja** als u wilt dat de schrappingsregel beschikbaar is in het schrappingsvoorstelproces. Selecteer een journaalnaam van het type **Schrapping**.

![Basiseigenschappen van een schrappingsregel](./media/ledger-elimination-rule-journal.png "Basiseigenschappen van een schrappingsregel")

Nadat u de basiseigenschappen hebt gedefinieerd, selecteert u **Regels** om de werkelijke verwerkingsregels te definiëren. Er zijn twee opties voor schrappingen: u kunt het bedrag van de nettowijziging verwijderen of een vast bedrag definiëren.

Selecteer de bronrekeningen. U kunt een sterretje (\*) als jokerteken gebruiken. Zo worden met **1\*** alle rekeningen die beginnen met een **1** als bron van gegevens voor de toewijzing geselecteerd.

Nadat u de bronrekeningen hebt geselecteerd, gebruikt u het veld **Rekeningspecificatie** om de rekening op te geven die van het doelbedrijf wordt gebruikt. Selecteer **Bron** als u dezelfde hoofdrekening wilt gebruiken die is gedefinieerd in de bronrekening. Als u **Door gebruiker gedefinieerd** selecteert, moet u een doelrekening opgeven.

![Pagina Schrappingsregel regel grootboek](./media/ledger-elimination-rule-line.png "Pagina Schrappingsregel regel grootboek")

Het veld **Dimensiespecificatie** werkt net als het veld **Rekeningspecificatie**. Selecteer **Bron** als u dezelfde dimensies in het doelbedrijf en het bronbedrijf wilt gebruiken. Als u **Door gebruiker gedefinieerd** selecteert, moet u de dimensies opgeven in het doelbedrijf door **Doeldimensies** te selecteren. Selecteer vervolgens brondimensies en de financiële dimensies en waarden die worden gebruikt als bron van de schrapping.

### <a name="process-elimination-transactions"></a>Schrappingstransacties verwerken
Er zijn twee manieren om schrappingstransacties te verwerken. De transactie kan worden verwerkt tijdens het online consolidatieproces of u kunt een schrappingsjournaal maken en het schrappingsvoorstelproces uitvoeren. Deze sectie is gericht op de tweede optie.

Selecteer in een bedrijf dat is gedefinieerd als een eliminatiebedrijf **Schrappingsjournaal** in de module **Consolidaties**. Selecteer **Regels** als u de journaalnaam hebt geselecteerd. Als u het voorstel wilt uitvoeren, selecteert u **Voorstellen** \> **Schrappingsvoorstel**.

Selecteer het bedrijf dat de bron is van de geconsolideerde gegevens en selecteer vervolgens de regel die u wilt verwerken. Voer de begin- en einddatums in om het datumbereik te definiëren dat wordt doorzocht op schrappingsbedragen. Geef in het veld **Boekingsdatum GB** de datum op waarop het journaal naar het grootboek moet worden geboekt. Nadat u **OK** hebt geselecteerd, kunt u de bedragen bekijken en het journaal boeken.

> [!NOTE]
> Het schrappingsjournaal bevat de bedragen voor rekeningwaarden in de valuta van de oorspronkelijke transacties, niet in de valuta voor boekhouding. Als u de bedragen in het schrappingsjournaal bekijkt, vindt u dit gedrag mogelijk verwarrend.

Zie voor meer informatie en voorbeelden [Schrappingsregels](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Valutaherwaardering in een consolidatiebedrijf
Wanneer u gegevens van een valuta voor boekhouding naar een andere valuta consolideert, moet u herwaardering van de valuta alsnog uitvoeren als er een wijziging in wisselkoersen is, zodat de rekeningsaldi correct worden geherwaardeerd. Als u de gegevens aanvankelijk consolideert, gebruikt u het tabblad **Valutaomrekening** om de oorspronkelijke wisselkoersen te selecteren die voor omrekening moeten worden gebruikt tijdens het consolidatieproces. Nadat een nieuwe wisselkoers (bijvoorbeeld in de volgende maand) is ingevoerd, moet u de rekeningsaldo's herwaarderen. De ongerealiseerde winsten of verliezen worden vervolgens bijgewerkt op basis van de nieuwe wisselkoers en datum.

Zie voor meer informatie over de herwaardering van valuta in een consolidatiebedrijf [Herwaardering van valuta in een consolidatiebedrijf](currency-revaluation-consolidation-company.md).

Zie voor meer informatie over de werking van herwaardering van valuta in de module **Grootboek** [Herwaardering van vreemde valuta voor grootboek](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Aanvullende gegevens
- Alle boekingslagen worden geconsolideerd wanneer de consolidatie wordt verwerkt.
- Schrappingsjournalen kunnen alleen naar de huidige laag worden geboekt.
- Alleen operationele saldi worden geconsolideerd. Daarom moet u om beginsaldi te zien, nog steeds een jaarafsluiting in het consolidatiebedrijf uitvoeren.
- U kunt een dagelijks journaal in een eliminatiebedrijf boeken, maar niet in een consolidatiebedrijf.

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Voordelen van het gebruik van Financiële rapportage voor financiële consolidaties en valutaomrekening of ter aanvulling van Online consolideren voor geconsolideerde rapportage
Klanten die Financiële rapportage voor financiële consolidaties en valutaomrekening gebruiken of ter aanvulling van Online consolideren voor geconsolideerde rapportage, hebben verschillende voordelen:

- **Diepte van gegevens**: u kunt geconsolideerde rapporten maken die werkelijke en gebudgetteerde gegevens zowel op rekeningniveau als op dimensieniveau samenbrengen. Voor Finance and Operations bevatten deze gegevens gegevens van zowel budgetbeheer als budgetplanning.
- **Dynamische consolidaties**: consolidaties kunnen op elk gewenst moment en op elk niveau in de organisatiehiërarchie worden uitgevoerd.
- **Controlecapaciteiten controleren**: alle dimensies, rekeningen en transactiedetails worden beheerd voor analyse en controle. Financiële rapportage biedt bovendien volledige drill-back aan de oorspronkelijke transactie in alle rechtspersonen die worden geconsolideerd.
- **Gestroomlijnde valutaomrekening**: na de minimale instelling in Finance and Operations kunt u elk rapport van Financiële rapportage omzetten in elke valuta voor rapportage die is ingesteld. Daarnaast kunt u een onbeperkt aantal rapportagevaluta´s instellen.
- **Schrappingen boeken bij de bron**: u kunt een schrappingsrapport maken en afdrukken om schrappingstransacties te verifiëren. Vervolgens kunt u alle nieuwe schrappingen boeken als standaard intercompany-transacties. U kunt ook een rechtspersoon voor schrapping gebruiken voor elke transactie die u niet in uw rechtspersonen wilt.

## <a name="supported-consolidation-scenarios"></a>Ondersteunde consolidatiescenario's
Hier volgen enkele consolidatiescenario's die in Financiële rapportage worden ondersteund:

- Consolidaties op één niveau en meerdere niveaus voor rechtspersonen
- Consolidaties waarin organisatiestructuren worden gebruikt die worden gemaakt van rechtspersonen
- Consolidaties die betrekking hebben op schrappingen
- Minderheidsbelang
- Meerdere rekeningschema's voor rechtspersonen
- Verschillende fiscale kalenders voor meerdere rechtspersonen
- Consolidaties die betrekking hebben op meerdere rapportagevaluta's
- Bedrijfseenheidsconsolidaties

## <a name="generating-consolidated-financial-statements"></a>Geconsolideerde financiële overzichten genereren
Zie voor informatie over scenario's waarin u mogelijk geconsolideerde financiële overzichten genereert [Geconsolideerde financiële overzichten genereren](./generating-consolidated-financial-statements.md).
