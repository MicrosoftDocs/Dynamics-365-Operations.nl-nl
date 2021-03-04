---
title: Locatie-instructie voor naar ouderdom gerangschikte voorraadorderverzameling
description: In dit onderwerp wordt uitgelegd hoe u de richtlijnen voor de FIFO- (First in, first out) en LIFO-locaties (last in, first out) gebruikt tijdens het orderverzamelen.
author: mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ae2826b54cb2ff516840443e01185a5342aedcc
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425764"
---
# <a name="location-directive-inventory-picking-aging"></a>Locatie-instructie voor naar ouderdom gerangschikte voorraadorderverzameling

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de richtlijnen voor de FIFO- (First in, first out) en LIFO-locaties (last in, first out) gebruikt tijdens het orderverzamelen. Deze strategieën werken samen met de ouderdomsdatums die zijn vastgelegd voor locaties en die moeten worden gevolgd nadat de voorraad voor het eerst binnenkomt in het magazijn. De functie *Locatie-instructie voor naar ouderdom gerangschikte voorraadorderverzameling* gebruikt de de datum van de locatie om de ouderdom te bepalen. Met de functie *Status van magazijnlocatie* wordt de datum op de locatie bijgewerkt op basis van de datum van de nummerplaat.

U kunt FIFO- en LIFO-strategieën gebruiken om artikelen met en zonder batchtracering te verzenden, op basis van de datum waarop de voorraad in het magazijn binnenkomt. Deze mogelijkheid kan vooral nuttig zijn voor voorraad zonder batchtracering, waarbij een vervaldatum niet beschikbaar is voor sorteren.

Wanneer de voorraad voor het eerst wordt ontvangen of gemaakt in het magazijn, werkt het systeem de desbetreffende nummerplaat bij, zodat de huidige datum wordt weergegeven als ouderdomsdatum. Deze datum wordt vervolgens gebruikt door de locatierichtlijnstrategieën om de oudste of nieuwste voorraad in het magazijn te identificeren. Als de voorraad wordt verplaatst naar een locatie die niet wordt gevolgd met een nummerplaat, wordt de locatie zelf bijgewerkt met ouderdomsinformatie en wordt deze informatie door de strategieën gebruikt.

## <a name="turn-on-the-feature"></a>De functie inschakelen

Als u deze functie beschikbaar wilt maken, schakelt u de volgende functies in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in, in deze volgorde:

1. Status magazijnlocatie
1. Locatie-instructie voor naar ouderdom gerangschikte voorraadorderverzameling

## <a name="feature-requirements"></a>Functievereisten

Als u deze functie wilt gebruiken, moet u de optie **Locatiestatus inschakelen** instellen op *Ja* voor elk [locatieprofiel](tasks/create-location-profile.md) dat wordt gebruikt om voorraad op te slaan. Als u deze optie wilt instellen voor een locatieprofiel, gaat u naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locatieprofielen** en selecteert u het locatieprofiel. U vindt de optie op het sneltabblad **Algemeen**.

## <a name="feature-scenarios"></a>Functiescenario's

In deze sectie worden voorbeelden gegeven van het instellen en gebruiken van FIFO- en LIFO-strategieën.

> [!TIP]
> Deze sectie bevat twee scenario's, één voor FIFO en één voor LIFO. In de vermelde procedures wordt ervan uitgegaan dat u beide scenario's in volgorde doet. We raden u aan beide scenario's uit te voeren, zodat u de verschillen tussen de twee strategieën opmerkt.

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u deze scenario's wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

U kunt deze scenario's ook gebruiken als instructie voor het gebruiken van de functie in een productiesysteem. In dat geval moet u echter uw eigen waarden opgeven voor elke instelling die hier wordt beschreven.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>De scenario's configureren

De demogegevens vereisen instellingen en voorraadcorrecties ter ondersteuning van de scenario's. Voer de volgende stappen uit om de voorraadgegevens te maken die nodig zijn om via FIFO- en LIFO-scenario's te werken.

1. Meld u aan bij een systeem waarin demogegevens zijn geïnstalleerd en selecteer de rechtspersoon **USMF**.
1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer in de lijst met locatieprofielen de waarde **FLOOR-05**.
1. Stel op het sneltabblad **Algemeen** de optie **Locatiestatus inschakelen** in op *Ja*.
1. Selecteer **Opslaan**.
1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Selecteer in de lijst met locatie-instructies **63 Containers voor orderverzamelen**.
1. Selecteer de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. Zoek op het sneltabblad **Acties locatierichtlijn** de regel waarin het veld **Volgnummer** in ingesteld op *1* en voer een van de volgende stappen uit:

    - Als u een FIFO-scenario instelt, wijzigt u de waarde van het veld **Strategie** in *Ouderdom locatie FIFO*.
    - Als u een LIFO-scenario instelt, wijzigt u de waarde van het veld **Strategie** in *Ouderdom locatie LIFO*.

1. Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.
1. Selecteer in het querydialoogvenster op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen en stel vervolgens de volgende waarden in:

    - **Tabel:** *Locaties*
    - **Afgeleide tabel:** *Locaties*
    - **Veld:** *Zone-id*
    - **Criteria:** *Verdieping*

1. Selecteer **OK** om de instellingen toe te passen en het querydialoogvenster te sluiten.
1. Selecteer **Opslaan** om de wijzigingen in de locatie-instructie op te slaan.
1. Op een mobiel apparaat of in de app *Dynamics 365 for Finance and Operations - Magazijn* op uw pc voert u de volgende stappen uit om bestaande voorraad uit de magazijnlocatie te verwijderen ter ondersteuning van de scenario's:

    1. Meld u aan magazijn *63* met de juiste gebruikers-id en wachtwoord.
    1. Selecteer **Kwaliteit** in het hoofdmenu.
    1. Selecteer **Uitval** in het menu **Kwaliteitsbeheer**.
    1. Selecteer op de pagina **Uitval** het veld **LOC/LP** en voer *63\_1* in.
    1. Selecteer **Enter** of **OK**.
    1. Bevestig de details voor **Uitval** voor **Correctie uit** door **Enter** of **OK** te selecteren.

    Wanneer de voorraad van de nummerplaat wordt aangepast, wordt het bericht 'Werk voltooid' weergegeven.

    Met deze stappen blijft de voorraad op twee locaties in de demogegevens staan. Elke locatie heeft een andere ouderdomsdatum. Locatie *FL-001* heeft een ouderdomsdatum van 15 april 2017 en locatie *FL-002* heeft een ouderdomsdatum van 29 januari 2017. Op beide locaties bevindt zich artikel *A0001*.

    Als u deze gegevens wilt weergeven, gaat u **Voorraadbeheer \> Query's en rapporten \> Voorhanden lijst** en filtert u vervolgens op magazijn *63* en artikel *A0001*. Selecteer in de rijen waarin het veld **Locatie** is ingesteld op *FL-001* of *FL-002* een regel met een positieve waarde voor **Fysieke voorraad** en selecteer vervolgens in het actievenster **Transacties**. In het veld **Fysieke datum** wordt een datum weergegeven die overeenkomt met een van de eerder vermelde ouderdomsdatums.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Scenario 1: FIFO-locatie instellen en gebruiken

De FIFO-strategie zoekt naar de locatie die de oudste ouderdomsdatum bevat en wijst op basis van die ouderdomsdatum orderverzamelen toe.

1. Als u dit nog niet hebt gedaan, [moet u de voorbeeldgegevens voorbereiden](#demo-set-up) die voor dit scenario vereist zijn.
1. Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.
1. Selecteer **Nieuw**.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-001*.
    - Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *63*.

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Dit omvat een nieuwe, lege regel in het raster op het sneltabblad **Verkooporderregels**. Stel voor deze orderregel het veld **Artikelnummer** in op *A0001* en het veld **Hoeveelheid** op *1*.
1. Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** de optie **Partij reserveren** om de bestelde hoeveelheid van dit artikel te reserveren in de voorraad van het geselecteerde magazijn.
1. Sluit de pagina **Reservering**.
1. Selecteer op de pagina **Verkooporder** in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgave naar magazijn**. U ontvangt meldingen. Het systeem maakt een zending, voegt deze toe aan een nieuwe lading en maakt het vereiste werk.
1. Selecteer op het sneltabblad **Verkooporderregels** in het menu **Magazijn** de optie **Werkdetails** om het werk dat voor deze verkooporder is gemaakt, te openen. De regel waar het veld **Werktype** de waarde *Orderverzamelen* bevat, geeft een **Locatie** weer met de waarde *FL-002*. Deze locatie bevat de nummer plaat met de oudste ouderdomsdatum (FIFO).
1. Selecteer **Magazijn \> Details van zending**.
1. Op het sneltabblad ***Algemeen** noteert u de wave-id zodat u deze kunt gebruiken in scenario 2.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Scenario 2: LIFO-locatie instellen en gebruiken

De LIFO-strategie zoekt naar de locatie die de nieuwste ouderdomsdatum bevat en wijst op basis van die ouderdomsdatum orderverzamelen toe. In scenario 2 bewerkt u de instelling voor scenario 1 (FIFO) en hergebruikt u de verkooporder en de wave die tijdens dat scenario zijn gemaakt.

1. Voordat u dit scenario start, moet u het volledige FIFO-scenario instellen en voltooien, zoals wordt beschreven in de [vorige sectie](#fifo-demo). In dit scenario maakt u opnieuw gebruik van de wave en de meeste instellingen die voor dat scenario zijn gemaakt.
1. Bewerk de locatierichtlijn **63 Containers voor orderverzamelen** zodat deze gebruikmaakt van de strategie *Ouderdom locatie LIFO*, zoals wordt beschreven in het eerste deel van de procedure [De scenario's configureren](#demo-set-up).

    Vervolgens wijzigt u de wave die voor de verkooporder in scenario 1 is gemaakt, zodat de strategie *Ouderdom locatie LIFO* wordt gebruikt.

1. Ga naar **Magazijnbeheer \> Uitgaande waves \> Zendingwaves \> Alle waves**.
1. Selecteer en open de wave die de volgorde bevat die u voor het FIFO-scenario hebt gemaakt.
1. Selecteer in het actievenster op het tabblad **Werk** de optie **Annuleren** om het werk te annuleren dat u hebt gemaakt voor het FIFO-scenario.
1. Selecteer in het actievenster op het tabblad **Wave** in de groep **Wave** de optie **Verwerken**.
1. Wanneer de verwerking is voltooid, selecteert u in het actievenster op het tabblad **Wave** in de groep **Verwante informatie** de optie **Werk** om het werk te openen dat voor deze wave is gemaakt.
1. Op de pagina **Werk**, op het tabblad **Overzicht**, moeten u twee regels zien. Selecteer de regel waarin het veld **Werkstatus** is ingesteld op *Open*.
1. De regel waar het veld **Werktype** de waarde *Orderverzamelen* bevat, geeft een **Locatie** weer met de waarde *FL-001*. Deze locatie bevat de nummer plaat met de nieuwste ouderdomsdatum (LIFO).

In deze scenario's hebt u gezien hoe de de locatiestrategie op basis van ouderdom werk naar de voorraadlocatie stuurt met de oudste voorraad of met de nieuwste voorraad, afhankelijk van de geselecteerde strategie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]