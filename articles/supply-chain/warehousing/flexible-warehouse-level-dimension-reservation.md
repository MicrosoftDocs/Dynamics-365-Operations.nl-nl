---
title: Flexibel reserveringsbeleid voor dimensies op magazijnniveau
description: In dit artikel wordt het beleid voor voorraadreservering beschreven waarmee bedrijven die batch-getraceerde producten verkopen en hun logistiek uitvoeren als WMS-bewerkingen, specifieke batches kunnen reserveren voor klantverkooporders, hoewel de reserveringshiërarchie die aan de producten is gekoppeld, reservering van specifieke batches niet toestaat.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fb42d4ccd2d8797a34f6351caf7dedbc1e957fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885807"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Flexibel reseveringsbeleid voor dimensies op magazijnniveau

[!include [banner](../includes/banner.md)]

Wanneer een hiërarchie voor voorraadreservering van het type *Batch-onder\[locatie\]* is gekoppeld aan producten, kunnen bedrijven die batch-getraceerde producten verkopen en hun logistiek uitvoeren als bewerkingen die zijn ingeschakeld voor het Microsoft Dynamics 365 WMS (Warehouse Management System), geen specifieke batches van die producten reserveren voor klantverkooporders.

Op vergelijkbare wijze kunnen specifieke nummerplaten niet worden gereserveerd voor producten op verkooporders wanneer deze producten zijn gekoppeld aan de standaardreserveringshiërarchie.

In dit artikel wordt het beleid voor voorraadreservering beschreven waarmee deze bedrijven specifieke batches of nummerplaten kunnen reserveren, zelfs wanneer de producten zijn gekoppeld aan een *Batch-onder\[locatie\]* reserveringshiërarchie.

## <a name="inventory-reservation-hierarchy"></a>Hiërarchie voor voorraadreservering

In deze sectie wordt de bestaande hiërarchie voor voorraadreservering samengevat.

De voorraadreserveringshiërarchie schrijft voor dat de vraagorder voor opslagdimensies de verplichte dimensies van de site-, magazijn- en voorraadstatus bevat. Met andere woorden, de verplichte dimensies zijn alle dimensies boven de locatiedimensie in de reserveringshiërarchie, terwijl de magazijnlogica verantwoordelijk is voor het toewijzen van een locatie aan de gevraagde hoeveelheden en het reserveren van de locatie. In de interacties tussen de vraagorder en de magazijnbewerkingen wordt verwacht dat de vraagorder aangeeft van waaruit de order moet worden verzonden (dat wil zeggen welke locatie en welk magazijn). In het magazijn wordt vervolgens vertrouwd op de magazijnlogica om de vereiste hoeveelheid in het magazijn te vinden.

Om het operationele model van het bedrijf weer te geven, zijn de traceringsdimensies (batch- en serienummers) echter flexibeler. Een hiërarchie voor voorraadreservering kan rekening houden met scenario's waarin de volgende voorwaarden van toepassing zijn:

- Het bedrijf is afhankelijk van zijn magazijnbewerkingen om het picken te beheren van hoeveelheden met batch- of serienummers *nadat* de hoeveelheden zijn gevonden in de magazijnopslagruimte. Dit model wordt vaak *Batch-onder\[locatie\]* of *Serienummer-onder\[locatie\]* genoemd. Dit wordt meestal gebruikt wanneer de batch- of serienummer-id van een product niet van belang is voor de klanten die de vraag bij het verkopende bedrijf plaatsen.
- Het bedrijf is afhankelijk van zijn magazijnbewerkingen om het picken te beheren van hoeveelheden met batch- of serienummers *voordat* de hoeveelheden zijn gevonden in de magazijnopslagruimte. Als batch- of serienummers nodig zijn als onderdeel van de orderspecificatie van een klant, worden deze vastgelegd in de vraagorder en mogen de magazijnbewerkingen waarmee de hoeveelheden in het magazijn worden gevonden deze niet wijzigen. Dit model wordt *Batch-boven\[locatie\]* of *Serienummer-boven\[locatie\]* genoemd. Omdat de dimensies boven locatie de specifieke vereisten zijn voor de eisen waaraan moet worden voldaan, wordt deze niet toegewezen door de magazijnlogica. Deze dimensies **moeten** altijd worden opgegeven op de vraagorder of in de bijbehorende reserveringen.

In deze scenario's is de uitdaging dat slechts één reserveringshiërarchie kan worden toegewezen aan elk vrijgegeven product. Daarom kan voor verwerking van getraceerde artikelen door het WMS, nadat de hiërarchietoewijzing bepaalt wanneer het batch- of serienummer moet worden gereserveerd (wanneer de vraagorder wordt opgenomen of tijdens het picken in het magazijn), deze timing niet worden gewijzigd op ad-hocbasis.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Flexibele reservering voor artikelen met batchtracering

### <a name="business-scenario"></a>Bedrijfsscenario

In dit scenario gebruikt een bedrijf een voorraadstrategie waarin eindproducten worden bijgehouden met batchnummers. In dit bedrijf wordt ook de WMS-werkbelasting gebruikt. Omdat deze werkbelasting goede logica bevat voor het plannen en uitvoeren van magazijnpick- en verzendbewerkingen voor artikelen met batchnummers, worden de meeste gerede artikelen gekoppeld aan een voorraadreserveringshiërarchie van het type *Batch-onder\[locatie\]*. Het voordeel van dit type operationele instelling is dat beslissingen (in feite reserveringsbeslissingen) over welke batches moeten worden gepickt en waar deze in het magazijn moeten worden geplaatst, worden uitgesteld totdat de magazijnpickbewerkingen beginnen. Ze worden niet genomen wanneer de order van de klant wordt geplaatst.

Hoewel de reserveringshiërarchie *Batch-onder\[locatie\]* de bedrijfsdoelstellingen van het bedrijf goed vervult, vereisen veel van de vaste klanten van het bedrijf dezelfde batch als ze eerder kochten, wanneer ze producten opnieuw bestellen. Daarom zoekt het bedrijf naar flexibiliteit in de manier waarop de batchreserveringsregels worden verwerkt, zodat, afhankelijk van de vraag van de klant naar hetzelfde artikel, de volgende werking optreedt:

- Een batchnummer kan worden geregistreerd en gereserveerd wanneer de order wordt opgenomen door de verkoopverwerker en kan niet worden gewijzigd tijdens magazijnbewerkingen en/of door andere vraag worden gebruikt. Dit gedrag helpt te garanderen dat het bestelde batchnummer naar de klant wordt verzonden.
- Als het batchnummer niet van belang is voor de klant, kunnen de magazijnbewerkingen een batchnummer bepalen tijdens het pickwerk, nadat de registratie en de reservering van de verkooporder zijn uitgevoerd.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Reserveren van een specifieke batch in de verkooporder toestaan

Voor de gewenste flexibiliteit in het batchreserveringsgedrag voor artikelen die zijn gekoppeld aan de voorraadreserveringshiërarchie *Batch-onder\[locatie\]* moeten voorraadbeheerders het selectievakje **Reservering op vraagorder toestaan** inschakelen voor het niveau **Batchnummer** op de pagina **Voorraadreserveringshiërarchieën**.

![De voorraadreserveringshiërarchie flexibel maken.](media/Flexible-inventory-reservation-hierarchy.png)

Wanneer het **Batchnummer**-niveau in de hiërarchie wordt geselecteerd, worden alle dimensies boven dat niveau en omhoog via het **Locatie**-niveau automatisch geselecteerd. (Standaard zijn alle dimensies boven het **Locatie**-niveau vooraf geselecteerd.) Dit gedrag weerspiegelt de logica waarbij alle dimensies in het bereik tussen het batchnummer en de locatie ook automatisch worden gereserveerd wanneer u een specifiek batchnummer op de orderregel reserveert.

> [!NOTE]
> Het selectievakje **Reservering op vraagorder toestaan** is alleen van toepassing op reserveringshiërarchieniveaus die onder de magazijnlocatiedimensie liggen.
>
> **Batchnummer** en **Nummerplaat** zijn de enige niveaus in de hiërarchie die openstaan voor het flexibele reserveringsbeleid. Met andere woorden, u kunt het selectievakje **Reservering op vraagorder toestaan** niet inschakelen voor de niveaus **Locatie** of **Serienummer**.
>
> Als uw reserveringshiërarchie de serienummerdimensie bevat (die altijd onder het niveau **Batchnummer** moet liggen) en als u batchspecifieke reservering voor het batchnummer hebt ingeschakeld, blijft het systeem de reservering van serienummers en pickbewerkingen verwerken op basis van de regels die van toepassing zijn op het reserveringsbeleid *Serienummer-onder\[locatie\]*.

U kunt op elk moment batchreservering toestaan voor een bestaande reserveringshiërarchie van het type *Batch-onder\[locatie\]* in uw implementatie. Deze wijziging heeft geen invloed op reserveringen en open magazijnwerkzaamheden die zijn gemaakt voordat de wijziging plaatsvond. Het selectievakje **Reservering op vraagorder toestaan** kan echter niet worden gewist als voorraadtransacties van het uitgiftetype **Besteld en gereserveerd**, **Fysiek gereserveerd** of **Besteld** bestaan voor een of meer artikelen die aan die reserveringshiërarchie zijn gekoppeld.

> [!NOTE]
> Als de bestaande reserveringshiërarchie van een artikel geen batchspecificatie op de order toestaat, kunt u deze opnieuw toewijzen aan een reserveringshiërarchie die batchspecificatie toestaat, mits de structuur van het hiërarchieniveau in beide hiërarchieën hetzelfde is. Gebruik de functie **Reserveringshiërarchie wijzigen voor artikelen** om de nieuwe toewijzing uit te voeren. Deze wijziging kan relevant zijn wanneer u flexibele batchreservering wilt voorkomen voor een subset van batch-getraceerde artikelen, maar wel wilt toestaan voor de rest van de productportefeuille.

Ongeacht of u het selectievakje **Reservering op vraagorder toestaan** hebt ingeschakeld, als u geen specifiek batchnummer voor het artikel wilt reserveren op een orderregel, geldt toch standaardlogica voor magazijnbewerkingen die geldig is voor een reserveringshiërarchie van het type *Batch-onder\[locatie\]* .

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Een specifiek batchnummer reserveren voor een klantorder

Nadat de reserveringshiërarchie *Batch-onder\[locatie\]* van een batch-getraceerd artikel is ingesteld om reservering van specifieke batchnummers op verkooporders toe te staan, kunnen verkooporderverwerkers klantorders voor hetzelfde artikel op een van de volgende manieren opnemen, afhankelijk van de aanvraag van de klant:

- **Ordergegevens invoeren zonder batchnummer**: deze benadering moet worden gebruikt wanneer de batchspecificatie van het product niet van belang is voor de klant. Alle bestaande processen die zijn gekoppeld aan de verwerking van een order van dit type, blijven ongewijzigd. Er zijn geen extra overwegingen vereist van de kant van de gebruikers.
- **Ordergegevens invoeren en een specifiek batchnummer reserveren**: deze benadering moet worden gebruikt wanneer de klant een specifieke batch aanvraagt. Normaal gesproken vragen klanten om een specifieke batch bij het opnieuw bestellen van een product dat ze eerder hebben gekocht. Dit type batchspecifieke reservering wordt ook wel *order-toegezegde reservering* genoemd.

De volgende set regels is geldig wanneer hoeveelheden worden verwerkt en een batchnummer wordt toegezegd aan een specifieke order:

- Als u reservering van een specifiek batchnummer voor een artikel wilt toestaan onder het reserveringsbeleid *Batch-onder\[locatie\]*, moeten alle dimensies tot aan de locatie worden gereserveerd. Dit bereik omvat meestal de nummerplaatdimensie.
- Locatie-instructies worden niet gebruikt wanneer het pickwerk wordt gemaakt voor een verkoopregel die gebruikmaakt van order-toegezegde batchreservering.
- Tijdens magazijnverwerking van werk voor order-toegezegde batches mag de gebruiker noch het systeem het batchnummer wijzigen. (Deze verwerking bevat uitzonderingsafhandeling.)

In het volgende voorbeeld wordt de end-to-end-stroom weergegeven.

## <a name="example-scenario-batch-number-allocation"></a>Voorbeeldscenario: batchnummertoewijzing

Voor dit voorbeeld moeten demogegevens worden geïnstalleerd en moet u het **USMF**-voorbeeldgegevensbedrijf gebruiken.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Een hiërarchie voor voorraadreservering instellen om batch-specifieke reservering toe te staan

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Voorraad \> Reserveringshiërarchie**.
2. Selecteer **Nieuw**.
3. Geef in het veld **Naam** een naam op (bijvoorbeeld **BatchFlex**).
4. Voer in het veld **Beschrijving** een beschrijving in (bijvoorbeeld **Batch onder flexibel**).
5. Selecteer in het veld **Geselecteerd** **Serienummer** en **Eigenaar** en selecteer vervolgens de pijl naar links om deze naar het veld **Beschikbaar** te verplaatsen.
6. Selecteer **OK**.
7. Schakel in de rij voor dimensieniveau **Batchnummer** het selectievakje **Reservering op vraagorder toestaan** in. De niveaus **Nummerplaat** en **Locatie** worden automatisch geselecteerd en u kunt de selectievakjes hiervoor niet uitschakelen.
8. Selecteer **Opslaan**.

### <a name="create-a-new-released-product"></a>Een nieuw vrijgegeven product maken

1. Stel de drie hoofdgegevensparameters van het product in met behulp van de volgende waarden:

    - Selecteer **Mag** in het veld **Opslagdimensiegroep**.
    - Selecteer **Batch-Fy** in het veld **Traceringsdimensiegroep**.
    - Selecteer **BatchFlex** in het veld **Reserveringshiërarchie**.

2. Maak twee batchnummers, bijvoorbeeld **B11** en **B22**.
3. Voeg artikelhoeveelheden toe aan voorhanden voorraad met behulp van de volgende waarden.

    | Magazijn | Batchnummer | Locatie | Nummerplaat | Hoeveelheid |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Geen          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Verkooporderdetails invoeren

1. Ga naar **Verkoop en marketing** \> **Verkooporders** \> **Alle verkooporders**.
2. Selecteer **Nieuw**.
3. Voer in de verkooporderkop in het veld **Klantrekening** **US-003** in.
4. Voeg een regel toe voor het nieuwe artikel en voer **10** in als hoeveelheid. Zorg dat het veld **Magazijn** is ingesteld op **24**.
5. Selecteer op het sneltabblad **Verkooporderregels** **Voorraad** en selecteer vervolgens in de groep **Onderhouden** **Batchreservering**. De pagina **Batchreservering** toont een lijst met batches die beschikbaar zijn voor reservering voor de orderregel. Voor dit voorbeeld wordt een hoeveelheid van **20** weergegeven voor batchnummer **B11** en een hoeveelheid van **10** voor batchnummer **B22**. De pagina **Batchreservering** kan niet worden geopend vanaf een regel als het artikel op die regel is gekoppeld aan de reserveringshiërarchie *Batch-onder\[locatie\]*, tenzij deze is ingesteld voor het toestaan van batchspecifieke reservering.

    > [!NOTE]
    > Als u een specifieke batch voor een verkooporder wilt reserveren, moet u de pagina **Batchreservering** gebruiken.
    >
    > Als u het batchnummer rechtstreeks op de verkooporderregel invoert, gedraagt het systeem zich alsof u een specifieke batchwaarde hebt ingevoerd voor een artikel dat onderworpen is aan het reserveringsbeleid *Batch-onder\[locatie\]*. Wanneer u de regel opslaat, wordt er een waarschuwingsbericht weergegeven. Als u bevestigt dat het batchnummer direct op de orderregel moet worden opgegeven, wordt de regel niet verwerkt door de normale magazijnbeheerlogica.
    >
    > Als u de hoeveelheid reserveert via de pagina **Reservering**, wordt er geen specifieke batch gereserveerd en volgt de uitvoering van de magazijnbewerkingen voor de regel de regels die van toepassing zijn onder het reserveringsbeleid voor *Batch-onder\[locatie\]*.

    Over het algemeen werkt en communiceert deze pagina op dezelfde manier als waarop deze werkt en communiceert met artikelen die een bijbehorende reserveringshiërarchie hebben van het type *Batch-boven\[locatie\]*. De volgende uitzonderingen zijn echter van toepassing:

    - Op het sneltabblad **Batchnummers toegezegd aan bronregel** worden de batchnummers weergegeven die zijn gereserveerd voor de orderregel. De batchwaarden in het raster worden in de loop van de afhandelingscyclus van de orderregel weergegeven, inclusief de magazijnverwerkingsfasen. Op het sneltabblad **Overzicht** wordt reguliere orderregelreservering (dat wil zeggen reservering die wordt uitgevoerd voor de dimensies boven het niveau **Locatie**) weergegeven in het raster tot het punt wanneer het magazijnwerk wordt gemaakt. De werkentiteit neemt vervolgens de regelreservering over en de regelreservering wordt niet meer op de pagina weergegeven. Het sneltabblad **Batchnummers toegezegd aan bronregel** helpt garanderen dat de verkooporderverwerker de batchnummers op een willekeurig moment tijdens de levenscyclus, tot aan facturering, kan weergeven die zijn toegezegd aan de order van de klant.
    - Een gebruiker kan niet alleen een specifieke batch reserveren, maar ook handmatig de specifieke locatie en de nummerplaat van de batch selecteren in plaats van deze automatisch te laten selecteren door het systeem. Deze mogelijkheid houdt verband met het ontwerp van het order-toegezegde batchreserveringsmechanisme. Zoals eerder gezegd, wanneer een batchnummer is gereserveerd voor een artikel onder het reserveringsbeleid *Batch-onder\[locatie\]*, moeten alle dimensies tot aan de locatie worden gereserveerd. Daarom bevat magazijnwerk de opslagdimensies die zijn gereserveerd door de gebruikers die met de orders hebben gewerkt en dit vertegenwoordigt mogelijk niet altijd een artikelopslagplaatsing die handig is of zelfs mogelijk is voor pickbewerkingen. Als orderverwerkers bekend zijn met de magazijnbeperkingen, willen ze mogelijk handmatig de specifieke locaties en de nummerplaten selecteren wanneer ze een batch reserveren. In dat geval moet de gebruiker de functie **Dimensies weergeven** gebruiken in de koptekst van de pagina en moet deze de locatie en de nummerplaat toevoegen aan het raster op het sneltabblad **Overzicht**.

6. Selecteer op de pagina **Batchreservering** de regel voor batch **B11** en selecteer vervolgens **Regel reserveren**. Er is geen speciale logica voor het toewijzen van locaties en nummerplaten tijdens automatische reservering. U kunt de hoeveelheid handmatig invoeren in het veld **Reservering**. Op het sneltabblad **Batchnummers toegezegd aan bronregel** wordt batch **B11** weergegeven als **Toegezegd**.

    ![Een specifiek batchnummer toezeggen aan een verkooporderregel op de pagina Batchreservering.](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > De reservering van de hoeveelheid op een verkooporderregel kan in meerdere batches worden uitgevoerd. Evenzo kan de reservering van dezelfde batch worden uitgevoerd voor meerdere locaties en nummerplaten (als nummerplaten voor de locaties zijn ingeschakeld).
    >
    > Reservering van een specifieke batch voor de hoeveelheid op een verkooporderregel kan ook gedeeltelijk zijn. De totale hoeveelheid van 100 eenheden kan bijvoorbeeld worden gereserveerd, zodat een specifieke batch wordt toegezegd aan 20 eenheden, terwijl 80 eenheden worden gereserveerd op locatie- en magazijnniveau voor elke beschikbare batch. In dit geval worden pickbewerkingen door het WMS verwerkt met behulp van twee afzonderlijke werkregels.

7. Ga naar **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**. Selecteer uw artikel en selecteer vervolgens **Voorraad beheren** \> **Weergeven** \> **Transacties**.

    ![Order-toegezegde reservering als voorraadtransactietype.](media/Inventory-transactions-for-order-committed-reservation.png)

8. De voorraadtransacties van het artikel controleren die betrekking hebben op de reservering van de verkooporderregel.

    - Een transactie waarbij het veld **Verwijzing** is ingesteld op **Verkooporder** en het veld **Uitgifte** is ingesteld op **Fysiek gereserveerd**, vertegenwoordigt de orderregelreservering voor de voorraaddimensies boven het niveau **Locatie**. Volgens de hiërarchie voor voorraadreservering van het artikel zijn deze dimensies de locatie, het magazijn en de voorraadstatus.
    - Een transactie waarbij het veld **Verwijzing** is ingesteld op **Order-toegezegde reservering** en het veld **Uitgifte** is ingesteld op **Fysiek gereserveerd**, vertegenwoordigt de orderregelreservering voor de specifieke batch en alle voorraaddimensies erboven. Volgens de hiërarchie voor voorraadreservering van het artikel zijn deze dimensies batchnummer en locatie. In dit voorbeeld is de locatie **Bulk-001**.

9. Selecteer in de verkooporderkop **Magazijn** \> **Acties** \> **Vrijgave naar magazijn**. De orderregel bevindt zich nu in een wave en er worden een belasting en werk gemaakt.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Magazijnwerk controleren en verwerken dat order-toegezegde batchnummers heeft

1. Selecteer op het sneltabblad **Verkooporderregels** **Magazijn** \> **Werkdetails**.

    Het werk waarmee de pickbewerking wordt afgehandeld voor batchhoeveelheden die zijn toegezegd aan de verkooporder, heeft de volgende kenmerken:

    - Voor het maken van werk gebruikt het systeem werksjablonen, maar geen locatierichtlijnen. Alle standaardinstellingen die zijn gedefinieerd voor werksjablonen, zoals een maximaal aantal pickregels of een specifieke maateenheid, worden toegepast om te bepalen wanneer nieuw werk moet worden gemaakt. De regels die zijn gekoppeld aan locatierichtlijnen voor het identificeren van picklocaties, worden echter niet meegerekend, omdat alle voorraaddimensies al worden opgegeven door de order-toegezegde reservering. Deze voorraaddimensies omvatten de dimensies op het opslagniveau van het magazijn. Daarom neemt het werk deze dimensies over zonder locatierichtlijnen te hoeven raadplegen.
    - Het batchnummer wordt niet weergegeven op de pickregel (zoals het geval is voor de werkregel die is gemaakt voor een artikel met een bijbehorende *Batch-boven\[locatie\]* reserveringshiërarchie). In plaats daarvan worden het 'van'-batchnummer en alle andere opslagdimensies weergegeven in de werkvoorraadtransactie van de werkregel waarnaar wordt verwezen vanuit de gekoppelde voorraadtransacties.

        ![Magazijnvoorraadtransactie voor werk dat afkomstig is uit order-toegezegde reservering.](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Nadat werk is gemaakt, wordt de voorraadtransactie van het artikel waarvan het veld **Referentie** is ingesteld op **Order-toegezegde reservering**, verwijderd. De voorraadtransactie waarbij het veld **Verwijzing** is ingesteld op **Werk**, bevat nu de fysieke reservering van alle voorraaddimensies van de hoeveelheid.

        Magazijnbewerkingen kunnen op de gebruikelijke manier doorgaan met het verwerken van de uitvoering van het werk. De instructies op het mobiele apparaat geven de werknemer echter opdracht om een specifiek batchnummer te picken. In magazijnomgevingen waarin locaties door nummerplaten worden beheerd, kan een werknemer nadat deze een locatie heeft bereikt waar dezelfde batch op meerdere nummerplaten is opgeslagen, een nummerplaat kiezen die nog niet is gereserveerd (bijvoorbeeld door een andere order toegezegde reservering of werk dat afkomstig is van een reservering van dat type).

        Als het niet praktisch is om te picken vanuit de locatie die op de werkregel is opgegeven, kunnen de magazijnoperators een van de volgende acties gebruiken om het picken van de specifieke batch via een handigere locatie om te leiden:

        - De standaardactie **Overschrijven locatie** op een mobiel apparaat (op voorwaarde dat de instelling **Overschrijven van orderverzamellocatie toestaan** voor de magazijnmedewerker is ingeschakeld)
        - De actie **Locatie wijzigen** op de pagina **Werklijstdetails**. 

2. Voltooi het picken en plaatsen van het werk op het mobiele apparaat.

    De hoeveelheid van **10** voor batchnummer **B11** wordt nu gepickt voor de verkooporderregel en geplaatst op de **Baydoor**-locatie. Het is nu klaar om te worden geladen op de vrachtwagen en naar het adres van de klant te worden verzonden.

## <a name="flexible-license-plate-reservation"></a>Reservering van een flexibele nummerplaat

### <a name="business-scenario"></a>Bedrijfsscenario

In dit scenario maakt een bedrijf gebruik van magazijnbeheer en werkverwerking en verwerkt het de ladingplanning op het niveau van afzonderlijke pallets/containers buiten Supply Chain Management voordat het werk wordt gemaakt. Deze containers worden weergegeven in de vorm van nummerplaten in de voorraaddimensies. Voor deze benadering moeten specifieke nummerplaten vooraf worden toegewezen aan verkooporderregels voordat het verzamelwerk wordt uitgevoerd. Het bedrijf zoekt flexibiliteit op in de manier waarop de reserveringsregels voor nummerplaten worden afgehandeld, zodat de volgende werking optreedt:

- Een nummerplaat kan worden geregistreerd en gereserveerd wanneer de order wordt opgenomen door de verkoopverwerker en kan niet door andere vraag worden gebruikt. Dit gedrag helpt te garanderen dat de nummerplaat die was gepland, naar de klant wordt verzonden.
- Als de nummerplaat nog niet aan een verkooporderregel is toegewezen, kunnen magazijnmedewerkers tijdens het verzamelwerk een nummerplaat selecteren, nadat de registratie en reservering van de verkooporder zijn voltooid.

### <a name="turn-on-flexible-license-plate-reservation"></a>Flexibele reservering van nummerplaten inschakelen

Voordat u de functie voor flexibele reservering van nummerplaten kunt gebruiken, moeten twee functies zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functies te controleren en deze zo nodig in te schakelen. U moet de functies in de volgende volgorde inschakelen:

1. **Functienaam:** *Flexibel reserveringsbeleid voor dimensies op magazijnniveau*
1. **Functienaam:** *Flexibele reservering van order-toegezegde nummerplaten*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Reserveer een specifieke nummerplaat op de verkooporder

Als u de reservering van nummerplaten voor een order wilt inschakelen, moet u het selectievakje **Reservering op vraagorder toestaan** inschakelen voor het niveau van de **nummerplaat** op de pagina **Voorraadreserveringshiërarchieën** voor de hiërarchie die aan het relevante artikel is gekoppeld.

![Pagina Voorraadreserveringshiërarchieën voor een flexibele nummerplaatreserveringshiërarchie.](media/Flexible-LP-reservation-hierarchy.png)

U kunt de reservering van licentieplaten voor de order op elk punt in uw implementatie inschakelen. Deze wijziging heeft geen invloed op reserveringen of open magazijnwerk die zijn gemaakt voordat de wijziging plaatsvond. U kunt het selectievakje **Reservering op vraagorder toestaan** echter niet wissen als er open, uitgaande voorraadtransacties met de uitgiftestatus *In bestelling*, *Besteld en gereserveerd* of *Fysiek gereserveerd* bestaan voor een of meer artikelen die aan die reserveringshiërarchie zijn gekoppeld.

Zelfs als het selectievakje **Reservering op vraagorder toestaan** is ingeschakeld voor het niveau **Nummerplaat**, is het toch *niet* mogelijk een specifieke nummerplaat te reserveren voor de order. In dit geval geldt de standaardmagazijnbewerkingslogica die geldig is voor de reserveringshiërarchie.

Als u een specifieke nummerplaat wilt reserveren, moet u een proces [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) gebruiken. In de toepassing kunt u deze reservering rechtstreeks vanuit een verkooporder uitvoeren met behulp van de optie **Orders-toegezegde reserveringen per nummerplaat** van de opdracht **Openen in Excel**. In de entiteitgegevens die worden geopend in de Excel-invoegtoepassing moet u de volgende gegevens over de reservering invoeren en vervolgens **Publiceren** selecteren om de gegevens terug te sturen naar Supply Chain Management:

- Verwijzing (alleen de waarde *Verkooporder* wordt ondersteund.)
- Het ordernummer (de waarde kan worden afgeleid van de partij)
- Partij-ID
- Nummerplaat
- Hoeveelheid

Als u een specifieke nummerplaat moet reserveren voor een batch-getraceerd artikel, gebruikt u de pagina **Batchreservering**, zoals beschreven in de sectie [Verkooporderdetails invoeren](#sales-order-details).

Wanneer de verkooporderregel die gebruikmaakt van een order-toegezegde nummerplaatreservering, wordt verwerkt door magazijnbewerkingen, worden er geen locatie-instructies gebruikt.

Als een magazijnwerkitem bestaat uit regels die gelijk zijn aan een volledige pallet en nummerplaat-toegezegde hoeveelheden hebben, kunt u het verzamelproces optimaliseren met behulp van een menuopdracht van het mobiele apparaat, waarbij de optie **Verwerken per nummerplaat** is ingesteld op *Ja*. Een magazijnmedewerker kan vervolgens een nummerplaat scannen om een verzameling te voltooien in plaats van de artikelen uit het werk een voor een te scannen.

![Menuopdracht van mobiel apparaat waarbij de optie Verwerken per nummerplaat is ingesteld op Ja.](media/Handle-by-LP-menu-item.png)

Omdat de functionaliteit **Verwerken per nummerplaat** geen ondersteuning biedt voor werkzaamheden die meerdere pallets omvatten, is het beter om een afzonderlijk werkitem te hebben voor verschillende nummerplaten. Als u deze aanpak wilt gebruiken, voegt u het veld **Order-toegezegde nummerplaat-id** als werkkoptekstopsplitsing toe op de pagina **Werksjabloon**.

> [!NOTE]
> Voor het proces van het maken van order-toegezegde werkzaamheden wordt er een waarde voor een order-toegezegde voorraaddimensie toegewezen aan de regels voor orderverzameling en kan de waarde van de nummerplaat niet rechtstreeks worden weergegeven. Alleen het proces *Door gebruiker bestuurd* wordt ondersteund bij het instellen van een menuopdracht voor een mobiel apparaat.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Voorbeeldscenario: een order-toegezegde nummerplaatreservering instellen en verwerken

Dit scenario toont hoe u een order-toegezegde nummerplaatreservering instelt en verwerkt.

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Dit scenario verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Supply Chain Management worden geleverd. Als u dit scenario wilt doorlopen met de waarden die hier worden gebruikt, moet u werken in een omgeving waar de demogegevens zijn geïnstalleerd. U moet ook de rechtspersoon **USMF** instellen voordat u begint.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Een hiërarchie voor voorraadreservering maken die nummerplaatreservering toestaat

1. Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> Reserveringshiërarchie**.
1. Selecteer **Nieuw**.
1. Voer in het veld **Naam** een waarde in (bijvoorbeeld *FlexibeleLP*).
1. Voer in het veld **Beschrijving** een waarde in (bijvoorbeeld *Flexibele LP-reservering*).
1. Selecteer in de lijst **Geselecteerd** **Batchnummer**, **Serienummer** en **Eigenaar**.
1. Selecteer de knop **Verwijderen** ![terugwaartse pijl.](media/backward-button.png) om de geselecteerde records naar de lijst **Beschikbaar** te verplaatsen.
1. Selecteer **OK**.
1. Schakel in de rij voor dimensieniveau **Nummerplaat** het selectievakje **Reservering op vraagorder toestaan** in. Het niveau **Locatie** wordt automatisch geselecteerd en u kunt het selectievakje hiervoor niet uitschakelen.
1. Selecteer **Opslaan**.

### <a name="create-two-released-products"></a>Twee vrijgegeven producten maken

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Nieuw vrijgegeven product** de volgende waarden in:

    - **Productnummer:** *Artikel1*
    - **Artikelnummer:** *Artikel1*
    - **Artikelmodelgroep:** *FIFO*
    - **Artikelgroep:** *Audio*
    - **Opslagdimensiegroep:** *Artikelen*
    - **Traceringsdimensiegroep:** *Geen*
    - **Reserveringshiërarchie:** *FlexibeleLP*

1. Selecteer **OK** om het product te maken en het dialoogvenster te sluiten.
1. Het nieuwe product wordt geopend. Stel op het sneltabblad **Magazijn** het veld **Eenheidvolgordegroep-id** in op de waarde *ea*.
1. Herhaal de vorige stappen om een tweede product met dezelfde instellingen te maken, maar stel de velden **Productnummer** en **Artikelnummer** in op *Artikel2*.
1. Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Weergeven** de optie **Terhanden voorraad**. Selecteer vervolgens **Hoeveelheidscorrectie**.
1. Pas de voorhanden voorraad van de nieuwe artikelen aan zoals is opgegeven in de volgende tabel.

    | Artikel  | Magazijn | Locatie | Nummerplaat | Hoeveelheid |
    |-------|-----------|----------|---------------|----------|
    | Artikel1 | 24        | FL-010   | LP01          | 10       |
    | Artikel1 | 24        | FL-011   | LP02          | 10       |
    | Artikel2 | 24        | FL-010   | LP01          | 5        |
    | Artikel2 | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > U moet de twee nummerplaten maken en locaties gebruiken voor gemengde artikelen, zoals *FL-010* en *FL-011*.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Een verkooporder maken en een specifieke nummerplaat reserveren

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw**.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *24*

1. Selecteer **OK** om het dialoogvenster **Verkooporder maken** te sluiten en de nieuwe verkooporder te maken.
1. Voeg op het sneltabblad **Verkooporderregels** een regel toe met de volgende instellingen:

    - **Artikelnummer:** *Artikel1*
    - **Hoeveelheid:** *10*

1. Voeg een tweede verkooporderregel met de volgende instellingen toe:

    - **Artikelnummer:** *Artikel2*
    - **Hoeveelheid:** *5*

1. Selecteer **Opslaan**.
1. Noteer op het sneltabblad **Regeldetails** op het tabblad **Instellen** de **partij-id**-waarde voor elke regel. Deze waarden zijn vereist tijdens de reservering van specifieke nummerplaten.

    > [!NOTE]
    > Als u een specifieke nummerplaat wilt reserveren, moet u de gegevensentiteit **Order-toegezegde reserveringen per nummerplaat** gebruiken. Als u een batch-getraceerd artikel wilt reserveren op een specifieke nummerplaat, kunt u ook de pagina **Batchreservering** gebruiken, zoals beschreven in de sectie [Verkooporderdetails invoeren](#sales-order-details).
    >
    > Als u de nummerplaat rechtstreeks op de verkooporderregel invoert en deze naar het systeem bevestigt, wordt magazijnbeheerverwerking niet voor de regel gebruikt.

1. Selecteer **Openen in Microsoft Office**, selecteer **Orders-toegezegde reserveringen per nummerplaat** en download het bestand.
1. Open het gedownloade bestand in Excel en selecteer **Bewerken inschakelen** om de invoegtoepassing voor Excel in te schakelen.
1. Als u de Excel-invoegtoepassing voor het eerst uitvoert, selecteert u **Deze invoegtoepassing vertrouwen**.
1. Als u wordt gevraagd om u aan te melden, selecteert u **Aanmelden**. Vervolgens meldt u zich aan met de referenties waarmee u zich ook hebt aangemeld bij Supply Chain Management.
1. Als u een artikel op een specifieke nummerplaat wilt reserveren, selecteert u in de Excel-invoegtoepassing **Nieuw** om een reserveringsregel toe te voegen en stelt u de volgende waarden in:

    - **Partij-id:** voer de **partij-id**-waarde in die u hebt gevonden voor de verkooporderregel voor *Artikel1*.
    - **Nummerplaat:** *LP02*
    - **Gereserveerde voorraadhoeveelheid:** *10*

1. Selecteer **Nieuw** om nog een reserveringsregel toe te voegen en stel de volgende waarden in:

    - **Partij-id:** voer de **partij-id**-waarde in die u hebt gevonden voor de verkooporderregel voor *Artikel2*.
    - **Nummerplaat:** *LP02*
    - **Gereserveerde voorraadhoeveelheid:** *5*

1. Selecteer **Publiceren** in de Excel-invoegtoepassing om de gegevens terug te sturen naar Supply Chain Management.

    > [!NOTE]
    > De reserveringsregel wordt alleen in het systeem weergegeven als het publiceren zonder fouten is voltooid.

1. Ga terug naar Supply Chain Management. 
1. Als u de reservering van het artikel wilt controleren, selecteert u op het sneltabblad **Verkooporderregels** in het menu **Voorraad** **Onderhouden \> Reservering**. Zoals u ziet, is voor de verkooporderregel voor *Artikel1* voorraad van *10* gereserveerd en voor de verkooporderregel voor *Artikel2* voorraad van *5*.
1. Als u voorraadtransacties wilt controleren die zijn gerelateerd aan verkooporderregelreservering, selecteert u op het sneltabblad **Verkooporderregels** in het menu **Voorraad** **Weergeven \> Transacties**. U ziet dat er twee transacties zijn die zijn gerelateerd aan de reservering: een waarbij het veld **Verwijzing** is ingesteld op *Verkooporder* en een waar het veld **Verwijzing** is ingesteld op *Order-toegezegde reservering*.

    > [!NOTE]
    > Een transactie waarbij het veld **Verwijzing** is ingesteld op *Verkooporder* vertegenwoordigt de orderregelreservering voor de voorraaddimensies boven het niveau **Locatie** (site, magazijn en voorraadstatus). Een transactie waarbij het veld **Verwijzing** is ingesteld op *Order-toegezegde reservering* vertegenwoordigt de orderregelreservering voor de specifieke nummerplaat en locatie.

1. Als u de verkooporder wilt vrijgeven, selecteert u in het actievenster op het tabblad **Magazijn** in de groep **Acties** **Vrijgeven aan magazijn**.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Magazijnwerkzaamheden controleren en verwerken waaraan order-toegezegde nummerplaten zijn toegewezen

1. Selecteer op het sneltabblad **Verkooporderregels** in het menu **Magazijn** **Werkgegevens**.

    Wanneer de reservering wordt uitgevoerd voor een specifieke batch, gebruikt het systeem geen locatie-instructies wanneer het werk wordt gemaakt voor de verkooporder die gebruikmaakt van nummerplaatreservering. Omdat de order-toegezegde reservering alle voorraaddimensies opgeeft, inclusief de locatie, hoeven er geen locatierichtlijnen te worden gebruikt, omdat deze voorraaddimensies net in het werk zijn ingevoerd. Deze worden weergegeven in de sectie **Van voorraaddimensies** op de pagina **Werkvoorraadtransacties**.

    > [!NOTE]
    > Nadat het werk is gemaakt, wordt de voorraadtransactie van het artikel waarvan het veld **Referentie** is ingesteld op *Order-toegezegde reservering*, verwijderd. De voorraadtransactie waarbij het veld **Verwijzing** is ingesteld op *Werk*, bevat nu de fysieke reservering voor alle voorraaddimensies van de hoeveelheid.

1. Voltooi op het mobiele apparaat het verzamelen en zet het werk weg met behulp van een menuoptie waarbij het selectievakje **Verwerken per nummerplaat** is ingeschakeld.

    > [!NOTE]
    > Met de functionaliteit **Verwerken per nummerplaat** kunt u de volledige nummerplaat verwerken. Als u een deel van de nummerplaat moet verwerken, kunt u deze functionaliteit niet gebruiken.
    >
    > We raden aan afzonderlijke werkzaamheden voor elke nummerplaat te laten genereren. Als u dit wilt bereiken, gebruikt u de functie **Opsplitsingen voor werkkoptekst** op de pagina **Werksjabloon**.

    De nummerplaat *LP02* wordt nu verzameld voor verkooporderregels en weggezet op de locatie *Baydoor*. Het is nu klaar om te worden geladen en naar de klant te worden verzonden.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Afhandeling van uitzonderingen van magazijnwerk dat aan orders toegezegde batchnummers heeft

Magazijnwerk voor picken van order-toegezegde batchnummers valt onder dezelfde standaardverwerking van uitzonderingen en acties als regulier werk. In het algemeen kan het openstaande werk of de openstaande werkregel worden geannuleerd, kan het worden onderbroken omdat de locatie van een gebruiker vol is, kan het kort worden verzameld en kan het worden bijgewerkt als gevolg van een verplaatsing. De gepickte hoeveelheid werk die al is voltooid, kan ook worden verminderd of het werk kan ongedaan worden gemaakt.

De volgende hoofdregel wordt toegepast op al deze acties voor afhandeling van uitzonderingen: het batchnummer dat voor de klant is gereserveerd, kan nooit worden vervangen door een ander batchnummer, maar de opslagdimensies (locatie en nummerplaat) ervan kunnen worden gewijzigd via een handmatige update door de gebruiker of door een automatische update door het systeem. De automatische update is gebaseerd op dezelfde willekeurige toewijzing van opslagdimensies die is toegepast toen een specifieke batch automatisch werd gereserveerd, maar er geen opslagdimensies zijn opgegeven.

### <a name="example-scenario"></a>Voorbeeldscenario

Een voorbeeld van dit scenario is een situatie waarin picken van eerder uitgevoerd werk ongedaan wordt gemaakt met de functie **Opgenomen hoeveelheid reduceren**. In dit voorbeeld wordt ervan uitgegaan dat u de stappen in [Voorbeeldscenario: batchnummertoewijzing](#Example-batch-allocation) al hebt voltooid. Dit voorbeeld gaat verder.

1. Ga naar **Magazijnbeheer** \> **Ladingen** \> **Actieve ladingen**.
2. Selecteer de belasting die in verband met de verzending van uw verkooporder is gemaakt.
3. Selecteer op het sneltabblad **Orderregels laden** **Opgenomen hoeveelheid reduceren**.
4. Selecteer op de pagina **Opgenomen hoeveelheid reduceren** in het veld **Naar locatie verplaatsen** **FL-001**.
5. Selecteer in het veld **Verplaatsen naar nummerplaat** **LP33**.
6. Geef **10** op in het raster in het veld **Opname voorraadhoeveelheid opheffen**.
7. Selecteer **OK**.

Dit zijn de resultaten van de actie voor het ongedaan maken van het picken:

- De status van het eerder gesloten werk wordt ingesteld op **Geannuleerd**.
- Nieuw werk van het type **Voorraadmutatie** wordt gemaakt voor de niet-gepickte hoeveelheid van **10** voor batchnummer **B11**. Dit werk staat voor de mutatie van de **Baydoor**-locatie naar nummerplaat **LP33** op locatie **FL-001**. De status wordt ingesteld op **Afgesloten**.
- Het systeem reserveert het batchnummer dat oorspronkelijk is besteld en wijst de locatie- en de nummerplaat-id toe. (Dit proces komt overeen met het uitvoeren van de functie **Regel reserveren** voor de orderregel voor een opgegeven batchnummer). Het resultaat is dat batch **B11** wordt weergegeven als toegezegd op het sneltabblad **Batchnummers toegezegd aan bronregel** van de pagina **Batchreservering** en het veld **Reservering** de hoeveelheid **10** voor batchnummer **B11** bevat. Bovendien wordt het veld **Locatie** ingesteld op **FL-001** en wordt het veld **Nummerplaat** ingesteld op **LP11**. (U kunt deze velden aan het raster toevoegen als ze niet zichtbaar zijn.)

De volgende tabellen bevatten een overzicht waarin wordt aangegeven hoe het systeem order-toegezegde batchreservering verwerkt voor specifieke magazijnacties. Als u de inhoud in de tabellen wilt interpreteren, gaat u ervan uit dat elke magazijnactie wordt uitgevoerd in de context van bestaand magazijnwerk dat afkomstig is van een order-toegezegde batchreservering, of dat de uitvoering van elke magazijnactie van invloed is op werk van dat type.

> [!NOTE]
> In deze tabellen geeft de kolom 'Batchhoeveelheid is beschikbaar' aan of een batchhoeveelheid beschikbaar is naast de hoeveelheid die al is gereserveerd voor de huidige order-toegezegde reserveringen of die al is gereserveerd door het magazijnwerk dat afkomstig is uit reserveringen van dat type.

#### <a name="override-the-pick-location-on-the-open-work"></a>De picklocatie voor het openstaande werk negeren

<table>
<thead>
<tr>
<th>Belangrijke instellingsparameter</th>
<th>Batchhoeveelheid is beschikbaar</th>
<th>Belangrijke gebruikersstappen</th>
<th>Magazijnwerk</th>
<th>Order-toegezegde batchreservering</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>De optie <strong>Overschrijven van orderverzamellocatie toestaan</strong> is ingeschakeld voor de werknemer.</td>
<td>Ja</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Locatie overschrijven</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk start.</li>
<li>Selecteer <strong>Voorstellen</strong>.</li>
<li>Bevestig de nieuwe locatie die is voorgesteld op basis van de beschikbaarheid van de batchhoeveelheid.</li>
</ol>
</td>
<td>Voor het huidige werk gebeuren de volgende acties:
<ul>
<li>De locatie op de pickregel wordt bijgewerkt naar de nieuwe locatie. (Als de locatie door nummerplaten wordt beheerd, wordt een willekeurige nummerplaat toegewezen aan de werkvoorraadtransactie en kan de werknemer elke nummerplaat kiezen die beschikbare hoeveelheid heeft.)</li>
<li>Als de hoeveelheid wordt aangetroffen op meer dan één nummerplaat op de nieuwe locatie, wordt de oorspronkelijke pickregel opgesplitst in meerdere regels, zodat deze overeenkomt met elke nummerplaat.</li>
</ul>
</td>
<td>Niet van toepassing</td>
</tr>
<tr>
<td>Nee</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Locatie overschrijven</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk start.</li>
<li>Voer handmatig een locatie in.</li>
</ol>
</td>
<td>De actie <strong>Overschrijven locatie</strong> is niet mogelijk. Dit mislukt en er wordt een fout gegenereerd.</td>
<td>Niet van toepassing</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Knop Volledig: een werkregel opsplitsen vanwege een overloop op de gebruikerslocatie

<table>
<thead>
<tr>
<th>Belangrijke instellingsparameter</th>
<th>Batchhoeveelheid is beschikbaar</th>
<th>Belangrijke gebruikersstappen</th>
<th>Magazijnwerk</th>
<th>Order-toegezegde batchreservering</th>
</tr>
</thead>
<tbody>
<tr>
<td>De optie <strong>Splitsing van werk toestaan</strong> is ingeschakeld in de menuoptie op het mobiele apparaat.</td>
<td>Niet van toepassing</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Volledig</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk verwerkt.</li>
<li>Voer in het veld <strong>Verzamelhoeveelheid</strong> een gedeeltelijke hoeveelheid van de vereiste pick in om de volledige capaciteit aan te geven.</li>
</ol>
</td>
<td>
<ul>
<li>Bij het huidige werk wordt de hoeveelheid bijgewerkt naar de resterende hoeveelheid die moet worden gepickt.</li>
<li>Nieuw werk voor de gepickte hoeveelheid wordt gemaakt en afgesloten.</li>
</ul></td>
<td>Niet van toepassing</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>De gepickte hoeveelheid voltooid werk (vanuit een belasting) reduceren

<table>
<thead>
<tr>
<th>Belangrijke instellingsparameter</th>
<th>Batchhoeveelheid is beschikbaar</th>
<th>Belangrijke gebruikersstappen</th>
<th>Magazijnwerk</th>
<th>Order-toegezegde batchreservering</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Niet van toepassing</td>
<td>Ja</td>
<td>
<ol>
<li>Open de pagina <strong>Opgenomen hoeveelheid reduceren</strong> vanaf de belastingsregel.</li>
<li>Voer de volledige hoeveelheid in waarvan picken moet worden opgeheven.</li>
<li>Selecteer een locatie/nummerplaat voor 'verplaatsen naar'.</li>
</ol>
</td>
<td>
<ul> 
<li>Werk dat aan de belastingsregel is gekoppeld, wordt geannuleerd.</li>
<li>Nieuw werk voor de voorraadmutatie wordt gemaakt en afgesloten.</li>
</ul>
</td>
<td>De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd. Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</td>
</tr>
<tr>
<td>Nee</td>
<td>Zie de vorige rij.</td>
<td>Zie de vorige rij.</td>
<td>De hoeveelheid wordt opnieuw gereserveerd voor dezelfde batch en voor dezelfde locatie en nummerplaat (als de locatie door nummerplaten wordt beheerd) die tijdens het opheffen van picken zijn ingevoerd.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Een artikel in een magazijn verplaatsen

> [!NOTE]
> Deze magazijnactie is alleen van toepassing op mutaties van het type **Proces van werkaanmaak** en niet op verplaatsing via sjabloon.

<table>
<thead>
<tr>
<th>Belangrijke instellingsparameter</th>
<th>Batchhoeveelheid is beschikbaar</th>
<th>Belangrijke gebruikersstappen</th>
<th>Magazijnwerk</th>
<th>Order-toegezegde batchreservering</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>De optie <strong>Mutatie van voorraad met gekoppeld werk toestaan</strong> is ingeschakeld voor de werknemer.</td>
<td>Ja</td>
<td>
<ol>
<li>Start een mutatie in de mobiele app Magazijnbeheer.</li>
<li>Voer een 'van'- en een 'naar'-locatie in.</li>
</ol></td>
<td>
<ul>
<li>In al het bestaande werk dat door de mutatie wordt beïnvloed, wordt de picklocatie bijgewerkt naar de nieuwe 'naar'-locatie.</li>
<li>Nieuw werk voor de voorraadmutatie wordt gemaakt en afgesloten.</li>
</ul>
</td>
<td>Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsverplaatsing vanuit de opgegeven locatie, worden voor dezelfde batch opnieuw gereserveerd. Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</td>
</tr>
<tr>
<td>Nee</td>
<td>Zie de vorige rij.</td>
<td>Zie de vorige rij.</td>
<td>Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsverplaatsingen vanuit de opgegeven locatie, worden opnieuw gereserveerd voor dezelfde batch en voor de nieuwe 'naar'-locatie en nummerplaat (als de locatie door nummerplaten wordt beheerd).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>De gepickte hoeveelheid voltooid werk (vanuit een belasting of een wave) omkeren

<table>
<thead>
<tr>
<th>Belangrijke instellingsparameter</th>
<th>Batchhoeveelheid is beschikbaar</th>
<th>Belangrijke gebruikersstappen</th>
<th>Magazijnwerk</th>
<th>Order-toegezegde batchreservering</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Niet van toepassing</td>
<td>Ja</td>
<td>
<ol>
<li>De pagina <strong>Werk omkeren</strong>.</li>
<li>Selecteer op de aanvraagpagina de optie <strong>Artikelen op huidige locatie laten</strong>.</li>
</ol>
</td>
<td>Al het werk dat aan de belasting is gekoppeld, wordt geannuleerd.</td>
<td>De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd. Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</td>
</tr>
<tr>
<td>Nee</td>
<td>Zie de vorige rij.</td>
<td>Zie de vorige rij.</td>
<td>De hoeveelheid wordt opnieuw gereserveerd voor dezelfde batch en voor de locatie en de nummerplaat waar de hoeveelheid was achtergelaten bij omkering.</td>
</tr>
<tr>
<td>Ja</td>
<td>
<ol>
<li>De pagina <strong>Werk omkeren</strong>.</li>
<li>Selecteer op de aanvraagpagina de optie <strong>Artikelen aan deze locatie toewijzen</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Het huidige werk wordt geannuleerd.</li>
<li>Nieuw werk voor de voorraadmutatie wordt gemaakt en afgesloten.</li>
</ul>
</td>
<td>De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd. Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</td>
</tr>
<tr>
<td>Nee</td>
<td>Zie de vorige rij.</td>
<td>Zie de vorige rij.</td>
<td>De hoeveelheid wordt opnieuw gereserveerd voor dezelfde batch en voor de locatie en de nummerplaat waaraan de hoeveelheid was toegewezen bij omkering.</td>
</tr>
<tr>
<td>Ja/nee</td>
<td>
<ol>
<li>De pagina <strong>Werk omkeren</strong>.</li>
<li>Selecteer op de aanvraagpagina de optie <strong>Artikelen naar deze locatie verplaatsen</strong>.</li>
</ol>
</td>
<td>Omkering wordt niet ondersteund.</td>
<td>Niet van toepassing</td>
</tr>
<tr>
<td>Ja/nee</td>
<td>
<ol>
<li>De pagina <strong>Werk omkeren</strong>.</li>
<li>Selecteer op de aanvraagpagina de optie <strong>Artikelen verplaatsen op basis van locatie-instructies</strong>.</li>
</ol>
</td>
<td>Omkering wordt niet ondersteund. </td>
<td>Niet van toepassing</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Een hoeveelheid kort picken: de hoeveelheid registreren als fysiek niet gevonden op de locatie/nummerplaat terwijl u het pickwerk uitvoert

<table>
<thead>
<tr>
<th>Belangrijke instellingsparameter</th>
<th>Batchhoeveelheid is beschikbaar</th>
<th>Belangrijke gebruikersstappen</th>
<th>Magazijnwerk</th>
<th>Order-toegezegde batchreservering</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Geen</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Nee</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Korte verzameling</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk uitvoert.</li>
<li>Typ <strong>0</strong> (nul) in het veld <strong>Orderverzamelhoeveelheid</strong>.</li>
<li>Voer in het veld <strong>Reden</strong> de tekst <strong>Geen hertoewijzing</strong> in.</li>
</ol>
</td>
<td>
<ul>
<li>Het huidige werk wordt gesloten en de gepickte hoeveelheid is 0 (nul).</li>
<li>Er wordt een voorraadtransactie van het type <strong>Tellen</strong> en het uitgiftetype <strong>Verkocht</strong> gemaakt om de correctie voor te stellen.</li>
</ul>
</td>
<td>De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd. Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</td>
</tr>
<tr>
<td>Nee</td>
<td>Zie de vorige rij.</td>
<td>
<ul>
<li>De korte-verzamelactie mislukt en er treedt een fout op.</li>
<li>Het huidige werk blijft geopend.</li>
</ul>
</td>
<td>Niet van toepassing</td>
</tr>
<tr>
<td rowspan='2'>Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Geen</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Ja</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Korte verzameling</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk uitvoert.</li>
<li>Typ <strong>0</strong> (nul) in het veld <strong>Orderverzamelhoeveelheid</strong>.</li>
<li>Voer in het veld <strong>Reden</strong> de tekst <strong>Geen hertoewijzing</strong> in.</li>
</ol>
</td>
<td>
<ul>
<li>Het huidige werk wordt gesloten en de gepickte hoeveelheid is 0 (nul).</li>
<li>Er wordt een voorraadtransactie van het type <strong>Tellen</strong> en het uitgiftetype <strong>Verkocht</strong> gemaakt om de correctie voor te stellen.</li>
</ul>
</td>
<td>Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsaanpassing vanuit de korte-verzamellocatie, worden voor dezelfde batch opnieuw gereserveerd. Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</td>
</tr>
<tr>
<td>Nee</td>
<td>Zie de vorige rij.</td>
<td>Zie de vorige rij.</td>
<td>Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsaanpassing vanuit de korte-verzamellocatie, worden verwijderd.</td>
</tr>
<tr>
<td>Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Handmatig</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Nee/ja</strong>. Bovendien wordt de <strong>Handmatige artikelhertoewijzing toestaan</strong> ingeschakeld voor de werknemer.</td>
<td>Ja</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Korte verzameling</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk uitvoert.</li>
<li>Typ <strong>0</strong> (nul) in het veld <strong>Korte-verzamelhoeveelheid</strong>.</li>
<li>Selecteer in het veld <strong>Reden</strong> de optie <strong>Kort orderverzamelen met handmatige hertoewijzing</strong>.</li>
<li>Selecteer de locatie/nummerplaat in de lijst.</li>
</ol>
</td>
<td>
<ul>
<li>Voor het huidige werk gebeuren de volgende acties:
<ul>
<li>Het pickregel wordt gesloten en de gepickte hoeveelheid is 0 (nul).</li>
<li>De opslagregel wordt geannuleerd.</li>
<li>Er wordt een nieuwe pickregel gemaakt. Er wordt gebruikgemaakt van de locatie/nummerplaat die de gebruiker heeft geselecteerd.</li>
<li>Er wordt een nieuwe opslagregel gemaakt.</li>
</ul>
</li>
<li>Er wordt een voorraadtransactie van het type <strong>Tellen</strong> en het uitgiftetype <strong>Verkocht</strong> gemaakt om de correctie voor te stellen.</li>
</ul>
</td>
<td>Niet van toepassing</td>
</tr>
<tr>
<td>Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Handmatig</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Nee</strong>. Bovendien wordt de <strong>Handmatige artikelhertoewijzing toestaan</strong> ingeschakeld voor de werknemer.</td>
<td>Nee</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Korte verzameling</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk uitvoert.</li>
<li>Typ <strong>0</strong> (nul) in het veld <strong>Korte-verzamelhoeveelheid</strong>.</li>
<li>Selecteer in het veld <strong>Reden</strong> de optie <strong>Kort orderverzamelen met handmatige hertoewijzing</strong>.</li>
</ol>
</td>
<td>De korte-verzamelactie mislukt en er treedt een fout op.</td>
<td>Niet van toepassing</td>
</tr>
<tr>
<td>Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Handmatig</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Ja</strong>. Bovendien wordt de <strong>Handmatige artikelhertoewijzing toestaan</strong> ingeschakeld voor de werknemer.</td>
<td>Nee</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Korte verzameling</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk uitvoert.</li>
<li>Typ <strong>0</strong> (nul) in het veld <strong>Korte-verzamelhoeveelheid</strong>.</li>
<li>Selecteer in het veld <strong>Reden</strong> de optie <strong>Kort orderverzamelen met handmatige hertoewijzing</strong>.</li>
<li>Selecteer de locatie/nummerplaat in de lijst.</li>
</ol>
</td>
<td>
<ul>
<li>Voor het huidige werk gebeuren de volgende acties:
<ul>
<li>Het pickregel wordt gesloten en de gepickte hoeveelheid is 0 (nul).</li>
<li>De opslagregel wordt geannuleerd.</li>
</ul>
</li>
<li>Er wordt een voorraadtransactie van het type <strong>Tellen</strong> en het uitgiftetype <strong>Verkocht</strong> gemaakt om de correctie voor te stellen.</li>
</ul>
</td>
<td>Alle bestaande reserveringen die worden beïnvloed door de hoeveelheidsaanpassing vanuit de korte-verzamellocatie/nummerplaat, worden verwijderd.</td>
</tr>
<tr>
<td>Er wordt een werkuitzondering van het type <strong>Korte verzameling</strong> ingesteld, waarbij <strong>Artikelhertoewijzing</strong> = <strong>Automatisch</strong>, <strong>Voorraad aanpassen</strong> = <strong>Ja</strong> en <strong>Reserveringen verwijderen</strong> = <strong>Ja/nee</strong>.</td>
<td>Niet van toepassing</td>
<td>
<ol>
<li>Selecteer de menuoptie <strong>Korte verzameling</strong> in de mobiele app Magazijnbeheer wanneer u verzamelwerk uitvoert.</li>
<li>Typ <strong>0</strong> (nul) in het veld <strong>Korte-verzamelhoeveelheid</strong>.</li>
<li>Selecteer in het veld <strong>Reden</strong> de optie <strong>Kort orderverzamelen met automatische hertoewijzing</strong>.</li>
</ol>
</td>
<td>Kort orderverzamelen waarbij automatische hertoewijzing betrokken is, wordt niet ondersteund.</td>
<td>Kort orderverzamelen waarbij automatische hertoewijzing betrokken is, wordt niet ondersteund.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>De voorraadstatus wijzigen

> [!NOTE]
> Deze magazijnactie kan worden uitgevoerd vanuit meerdere ingangspunten. In het volgende voorbeeld wordt de actie **Wijziging van voorraadstatus** op de pagina **Voorhanden voorraad per locatie** gebruikt.

<table>
<thead>
<tr>
<th>Belangrijke instellingsparameter</th>
<th>Batchhoeveelheid is beschikbaar</th>
<th>Belangrijke gebruikersstappen</th>
<th>Magazijnwerk</th>
<th>Order-toegezegde batchreservering</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Op het tabblad <strong>Magazijn</strong> in de record <strong>Magazijn</strong> is het veld <strong>Reserveringen en markeringen verwijderen</strong> ingesteld op <strong>Reserveringen</strong> of <strong>Markeringen en reserveringen</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Selecteer een specifieke locatie.</li>
<li>Selecteer een regel met een specifiek artikel, locatie en nummerplaat (als de locatie door nummerplaten wordt beheerd).</li>
<li>Selecteer <strong>Wijziging van voorraadstatus</strong>.</li>
<li>Stel het veld <strong>Voorraadstatus</strong> in op <strong>Blokkeren</strong>.</li>
</ol>
</td>
<td>Wijzigingen van de voorraadstatus zijn niet toegestaan voor hoeveelheden die zijn gereserveerd voor werk.</td>
<td>
<ul>
<li>De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd. Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</li>
<li>Er worden twee voorraadtransacties van het type <strong>Wijziging van voorraadstatus</strong> gemaakt om de wijziging te vertegenwoordigen in de voorraadstatusdimensie.</li>
<li>Een voorraadtransactie van het type <strong>Voorraadblokkering</strong> en het uitgiftetype <strong>Fysiek gereserveerd</strong> wordt gemaakt om de reservering van de geblokkeerde hoeveelheid voor te stellen.</li>
</ul>
</td>
</tr>
<tr>
<td>Nee</td>
<td>Zie de vorige rij.</td>
<td>Wijzigingen van de voorraadstatus zijn niet toegestaan voor hoeveelheden die zijn gereserveerd voor werk.</td>
<td>
<ul>
<li>De reservering wordt verwijderd.</li>
<li>Er worden twee voorraadtransacties van het type <strong>Wijziging van voorraadstatus</strong> gemaakt om de wijziging te vertegenwoordigen in de voorraadstatusdimensie.</li>
<li>Een voorraadtransactie van het type <strong>Voorraadblokkering</strong> en het uitgiftetype <strong>Fysiek gereserveerd</strong> wordt gemaakt om de reservering van de geblokkeerde hoeveelheid voor te stellen.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Op het tabblad <strong>Magazijn</strong> in de record <strong>Magazijn</strong> wordt het veld <strong>Reserveringen en markeringen verwijderen</strong> ingesteld op <strong>Geen</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Selecteer een specifieke locatie.</li>
<li>Selecteer een regel met een specifiek artikel, locatie en nummerplaat (als de locatie door nummerplaten wordt beheerd).</li>
<li>Selecteer <strong>Wijziging van voorraadstatus</strong>.</li>
<li>Stel het veld <strong>Voorraadstatus</strong> in op <strong>Blokkeren</strong>.</li>
</ol>
</td>
<td>Wijzigingen van de voorraadstatus zijn niet toegestaan voor hoeveelheden die zijn gereserveerd voor werk.</td>
<td>De hoeveelheid wordt voor dezelfde batch opnieuw gereserveerd. Het systeem wijst willekeurig een locatie en een nummerplaat toe (als de locatie door nummerplaten wordt beheerd) waar de hoeveelheid beschikbaar is.</td>
</tr>
<tr>
<td>Nee</td>
<td>Zie de vorige rij.</td>
<td>Wijzigingen van de voorraadstatus zijn niet toegestaan voor hoeveelheden die zijn gereserveerd voor werk.</td>
<td>Wijzigingen van de voorraadstatus zijn niet toegestaan.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Beperkingen

- De functionaliteit voor flexibele dimensiereservering op magazijnniveau ondersteunt de volgende functies niet:

    - Catch weight-beheer
    - Fysieke negatieve voorraad
    - Reservering tegen besteld aanbod
    - overboekingsorders en picken van grondstoffen

- De containerconsolidatieregel voor verpakking per instructie-eenheid heeft beperkingen. Voor order-toegezegde reserveringen wordt aangeraden geen containervormingssjablonen te gebruiken waarvoor het veld **Verpakken per instructie-eenheid** is ingeschakeld. In het huidige ontwerp worden er geen locatie-instructies gebruikt wanneer magazijnwerk wordt gemaakt. Daarom wordt alleen de laagste eenheid in de eenheidsvolgordegroep toegepast tijdens de wavestap voor containervorming.

## <a name="see-also"></a>Zie ook

- [Batchnummers in Magazijnbeheer](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [Dezelfde batch reserveren voor een verkooporder](../sales-marketing/reserve-same-batch-sales-order.md)
- [Oudste batch verzamelen op een mobiel apparaat](pick-oldest-batch.md)
- [Bevestiging van batch en nummerplaat](batch-and-license-plate-confirmation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]