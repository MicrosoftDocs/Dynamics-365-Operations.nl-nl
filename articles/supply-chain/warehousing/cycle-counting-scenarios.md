---
title: Voorbeeldscenario's van cyclustelling
description: Dit artikel biedt een verzameling scenario's waarin de functies voor cyclustelling van Microsoft Dynamics 365 Supply Chain Management onder de loep worden genomen.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 90a3f132a96081b56ab60f5b0ba5cc328b820879
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899319"
---
# <a name="cycle-counting-example-scenarios"></a>Voorbeeldscenario's van cyclustelling

[!include [banner](../includes/banner.md)]

Dit artikel biedt een verzameling scenario's waarin de functies voor cyclustelling van Microsoft Dynamics 365 Supply Chain Management onder de loep worden genomen. Eerst worden de vereisten voor uw bestaande Supply Chain Management-omgeving beschreven. Vervolgens wordt uitgelegd hoe u de cyclustelling kunt configureren en worden alle fasen voor de cyclustelling beschreven. Wanneer u klaar bent, moet u een goed inzicht hebben in cyclustelling, waaronder begeleide cyclustelling, blinde cyclustelling, plaatscyclustelling, drempels voor cyclustellingen en cyclustelplannen.

## <a name="prerequisites"></a>Vereisten

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Elk scenario in dit artikel verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Supply Chain Management worden geleverd. Als u de waarden wilt gebruiken die hier worden weergegeven wanneer u de scenario's doorloopt, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Ondersteuning voor de mobiele app Warehouse Management inschakelen

Om de mobiele app Warehouse Management te gebruiken die in dit onderwerp wordt beschreven, moet de functie *Gebruikersinstellingen, pictogrammen en stapnamen voor de nieuwe magazijnapp* worden ingeschakeld voor het systeem. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Gebruikersinstellingen, pictogrammen en stapnamen voor de nieuwe magazijnapp* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Demogegevens voorbereiden voor de scenario's

Volg deze stappen om te controleren of alle vereiste demogegevens voor de scenario's beschikbaar zijn in het bedrijf USMF in uw systeem. Maak eventueel records of waarden als deze ontbreken.

1. Ga naar **Magazijnbeheer \> Instellen \> Medewerker**.
1. Selecteer in het lijstvenster **Julia Funderburk**.
1. Selecteer op het sneltabblad **Gebruikers** de rij met de volgende waarden. Als er geen bestaande rij is met deze waarden, maakt u deze rij.

    - **Gebruikers-id:** *61*
    - **Gebruikersnaam:** *WH61*
    - **Standaardmagazijn:** *61*
    - **Menunaam:** *Hoofd*

1. Stel op het sneltabblad **Werk** de volgende waarden in voor gebruiker *61* als deze nog niet zijn ingesteld:

    - **Is een cyclustellingssupervisor:** *Nee*
    - **Maximale percentagelimiet:** *0*
    - **Maximale hoeveelheidslimiet:** *0*
    - **Maximale waardelimiet:** *0*

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkpools**.
1. Werkgroepen worden gebruikt om het magazijnwerk te onderscheiden op basis van het type werk (in dit geval, cyclustellingswerk). Zorg ervoor dat er een record bestaat met de volgende instellingen:

    - **Werkgroep-id:** *CycleCount*
    - **Omschrijving:** *Cyclustelling*

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer in het lijstdeelvenster de record met de naam *Cyclustelling*. Als er geen record bestaat met deze naam, maakt u deze record. De volgende waarden voor de record bevestigen of instellen:

    - **Naam menuopdracht:** *Cyclustelling*
    - **Titel:** *Cyclustelling Begeleid*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Ja*
    - **Bestuurd door:** *Door systeem bestuurd* (Deze waarde geeft aan dat in Supply Chain Management een werk-id voor de cyclustelling wordt toegewezen aan de werknemer.)
    - **Voorraadstatus weergeven:** *Ja*

1. Selecteer in het actievenster **Cyclustelling**.
1. Bevestig de volgende waarden of stel deze in het dialoogvenster **Cyclustelling mobiele apparaat** in:

    - **Artikelnummer weergeven:** *Ja*
    - **Nummerplaat weergeven:** *Ja*
    - **Aantal pogingen:** *1*

1. Selecteer **OK** om het dialoogvenster te sluiten.
1. Selecteer in het lijstdeelvenster de record met de naam *Cyclustelling Blind*. Als er geen record bestaat met deze naam, maakt u deze record. De volgende waarden voor de record bevestigen of instellen:

    - **Naam menuopdracht:** *Cyclustelling Blind*
    - **Titel:** *Cyclustelling Blind*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Ja*
    - **Bestuurd door** *Groepering van cyclustelling* (Deze waarde geeft aan dat de werknemer cyclustellingswerk-id's kan groeperen die specifiek zijn voor een bepaalde locatie, zone of een werkgroep.)

1. Selecteer in het actievenster **Cyclustelling**.
1. Bevestig de volgende waarden of stel deze in het dialoogvenster **Cyclustelling mobiele apparaat** in:

    - **Artikelnummer weergeven:** *Nee*
    - **Nummerplaat weergeven:** *Nee*
    - **Aantal pogingen:** *0*

1. Selecteer **OK** om het dialoogvenster te sluiten.
1. Selecteer in het lijstdeelvenster de record met de naam *Plaatcyclusstelling*. Als er geen record bestaat met deze naam, maakt u deze record. De volgende waarden voor de record bevestigen of instellen:

    - **Naam menuopdracht:** *Plaatcyclusstelling*
    - **Titel:** *Plaatscyclustelling*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Nee*
    - **Procedure voor het maken van werk**: *Plaatscyclustelling* (Deze waarde geeft aan dat de werknemer artikelen op elk moment kan tellen in een magazijnlocatie, zonder cyclustellingswerk te maken. Om plaatscyclustelling op een locatie uit te voeren, voert de werknemer de locatie-id in.)

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer in het lijstdeelvenster de record met de naam *Voorraad*. Als er geen record bestaat met deze naam, maakt u deze record. Controleer of de volgende menuopdrachten voor een cyclustelling worden weergegeven in de kolom **Menustructuur**:

    - Cyclustelling
    - Cyclustelling Blind
    - Plaatcyclusstelling

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het tabblad **Cyclustelling** de volgende waarden in:

    - **Standaardtype cyclustellingscorrectie:** *Cyclustelling* (Dit veld geeft het journaaltype aan dat wordt geboekt wanneer de cyclustelling wordt uitgevoerd.)
    - **Standaard werkklasse-id cyclustelling:** *CCount* (Dit veld geeft de werkklasse aan die wordt gebruikt voor de cyclustelling.)
    - **Standaardwerkprioriteit cyclustelling:** *50* (In dit veld wordt de prioriteit ingesteld die cyclustellingswerkzaamheden hebben ten opzichte van andere typen werk in het magazijn. Als u een nummer invoert dat lager is dan het nummer dat is ingevoerd voor andere typen werk, verhoogt u de prioriteit van het cyclustellingswerk.)

1. Ga naar **Magazijnbeheer \> Instellingen \> Voorraad \> Correctietypen**.
1. Met de pagina **Correctietypen** kunt u codes maken voor de verschillende in- en uitcorrecties die kunnen optreden. Bevestig dat er een record bestaat met de volgende instellingen:

    - **Voorraadcorrectietype:** *Cyclustelling*
    - **Omschrijving:** *Cyclustelling*
    - **Naam:** *ICnt*

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijninstellingen \> Magazijnen**.
1. Selecteer magazijn *61* in het lijstvenster. Als er geen record bestaat met deze naam, maakt u deze record.
1. Stel op het sneltabblad **Magazijn** de volgende waarden in:

    - **Magazijnbeheerproces gebruiken:** *Ja* (Met deze waarde wordt het magazijn voor magazijnbeheerprocessen geactiveerd.)
    - **Verplaatsingen nummerplaat gedurende cyclustelling toestaan:** *Ja* (met deze waarde kunnen werknemers nummerplaten verplaatsen tijdens een cyclustelling.)

## <a name="scenario-1-guided-cycle-counting"></a>Scenario 1: Begeleide cyclustelling

Voordat een begeleide cyclustelling kan plaatsvinden, moet u enkele werkzaamheden maken. Deze werkzaamheden leiden de toegewezen persoon door het magazijn, van locatie tot locatie, om de tellingen te voltooien die in het werk zijn ingesteld.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Cyclustellingswerk maken voor scenario 1

Volg deze stappen om cyclustellingswerkzaamheden te maken voor artikellocatie *01A02R2S2B* (BULK-06) in magazijn *61*.

1. Ga naar **Magazijnbeheer \> Cyclustelling \> Cyclustellingswerk volgens locatie**.
1. Stel in het dialoogvenster **Cyclustellingswerk volgens locatie maken** het veld **Werkgroep-id** in op *CycleCount*.
1. Selecteer **Filter** op het sneltabblad **Op te nemen records**.
1. Ga als volgt te werk in het dialoogvenster Query-editor in het tabblad **Bereik**:

    - Stel het veld **Criteria** in op *61* voor de rij waarin het veld **Veld** is ingesteld op *Magazijn*.
    - Stel het veld **Criteria** in op *01A02R2S2B* voor de rij waarin het veld **Veld** is ingesteld op *Locatie*.

1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.
1. Selecteer **OK** om het dialoogvenster **Cyclustellingswerk volgens locatie maken** te sluiten.

    Wanneer het werkcreatieproces is voltooid, wordt een bericht weergegeven in het actiecentrum.

1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. U kunt het nieuwe werk zoeken door een filter in te stellen op de kolom **Werkgroep-id** om te zoeken naar records met de waarde *CycleCount*.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Cyclustellingswerk doen voor scenario 1

Nadat u het cyclustellingswerk hebt gemaakt, kunt u het werk uitvoeren door artikelen in een magazijnlocatie te tellen en vervolgens het resultaat via een mobiel apparaat in Supply Chain Management in te voeren. Volg deze stappen om het werk voor de cyclustelling uit te voeren in de mobiele app Warehouse Management.

1. Meld u aan bij de mobiele app Warehouse Management als de werkgebruiker die u hebt ingesteld in de sectie [Demogegevens voorbereiden voor de scenario's](#prepare-demo-data) eerder in dit artikel. In het voorbeeld in dit artikel heeft de gebruiker de naam *Julia Funderburk* en is deze ingesteld voor magazijn *61*. (Met de demonstratiegegevens van USMF moet u zich aanmelden als deze werkgebruiker door *61* in te voeren als gebruikers-id en *1* als wachtwoord.)
1. Selecteer **Voorraad** in het hoofdmenu.
1. Selecteer **Cyclustelling Begeleid** in het menu **Voorraad**.
1. Selecteer het veld **Hoev.**, voer *9* in met behulp van het numerieke blok en selecteer vervolgens **OK** (de vinkjesknop).
1. Er werd verwacht dat u het aantal van 10 stuks voor dit artikel, de locatie en de nummerplaat zou invoeren. Daarom wordt u gevraagd om opnieuw te tellen. Selecteer het veld **Hoev.**, voer nogmaals *9* in met behulp van het numerieke blok en selecteer vervolgens **OK** (de vinkjesknop). Bij de tweede poging wordt de telling geaccepteerd.

    > [!NOTE]
    > Toen het systeem een verschil aantrof tussen de verwachte voorhanden hoeveelheid en de hoeveelheid die u hebt ingevoerd, heeft het u gevraagd om een tweede keer te tellen omdat het veld **Aantal pogingen** is ingesteld op *1* voor de menuopdracht **Cyclustelling Begeleid** van het mobiele apparaat. U bent begeleid naar een specifiek artikelnummer en nummerplaatnummer, omdat zowel de optie **Artikelnummer weergeven** als de optie **Nummerplaat weergeven** is ingesteld op *Ja* voor de menuopdracht van het mobiele apparaat.

1. Selecteer **OK** (vinkjesknop).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>De cyclustellingsverschillen voor scenario 1 controleren

Volg deze stappen om de verschillen in de cyclustelling te controleren.

1. Keer terug naar Supply Chain Management.
1. Ga naar **Magazijnbeheer \> Instellingen \> Werk > Werkdetails**.
1. Zoek en selecteer het werk voor de cyclustelling dat u eerder hebt bekeken. (Stel bijvoorbeeld een filter in op de kolom voor de **Werkgroep-id** om records te zoeken die de waarde *CycleCount* hebben.) Het veld **Werkstatus** voor dit werk is nu ingesteld op *In afwachting van controle*.

    > [!NOTE]
    > Voor de werkgebruikersaccount die u hebt gebruikt voor het tellen, wordt de optie **Cyclustellingssupervisor** ingesteld op *Nee* en de velden **Maximale percentagelimiet**, **Maximale hoeveelheidslimiet** en **Maximale waardelimiet** worden allemaal ingesteld op *0* (nul). Daarom moeten alle tellingsverschillen die deze gebruiker rapporteert handmatig worden goedgekeurd en wordt het veld **Werkstatus** voor het betreffende werk ingesteld op *In afwachting van controle*. Als de getelde waarde binnen de afwijkingslimieten (zoals is opgegeven in het veld **Maximale percentagelimiet** of **Maximale hoeveelheidslimiet** op de pagina **Werkgebruikers**) of als de optie **Cyclustellingssupervisor** is ingesteld op *Ja* voor de gebruiker, dan zou het werk automatisch zijn afgesloten.

1. Selecteer in het actievenster op het tabblad **Werk** de optie **Cyclustelling**.
1. Selecteer in het actievenster **Telling accepteren**.

    Het verschil wordt geboekt via de standaardtellijst en er wordt een nieuwe werkorder gemaakt.

1. Selecteer op de pagina **Cyclustellingstransacties** in het actievenster de optie **Afgeleid werk** om het werk te zoeken dat voor het goedgekeurde verschil is gemaakt.

## <a name="scenario-2-blind-cycle-counting"></a>Scenario 2: Blinde cyclustelling

Voor dit scenario moet scenario 1 al zijn voltooid in het systeem.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Cyclustellingswerk maken voor scenario 2

Voordat een blinde cyclustelling kan plaatsvinden, moet u enkele werkzaamheden maken. Volg deze stappen om cyclustellingswerkzaamheden te maken voor artikellocatie *01A02R2S2B* (BULK-06) in magazijn *61*.

1. Ga naar **Magazijnbeheer \> Cyclustelling \> Cyclustellingswerk volgens artikel**.
1. Stel in het dialoogvenster **Cyclustellingswerk volgens artikel maken** het veld **Werkgroep-id** in op *CycleCount*.
1. Selecteer **Filter** op het sneltabblad **Op te nemen records**.
1. Voeg in het dialoogvenster Query-editor op het tabblad **Bereik** drie rijen toe met de volgende instellingen:

    - Rij 1:

        - **Tabel:** *Artikelen*
        - **Veld:** *Artikelnummer*
        - **Criteria:** *L0101*

    - Rij 2:

        - **Tabel:** *Voorraaddimensies*
        - **Veld:** *Magazijn*
        - **Criteria:** *61*

    - Rij 3:

        - **Tabel:** *Voorraaddimensies*
        - **Veld:** *Locatie*
        - **Criteria:** *01A02R2S2B*

1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.
1. Selecteer **OK** om het dialoogvenster **Cyclustellingswerk volgens artikel maken** te sluiten.

    Wanneer het proces voor het maken van het werk is voltooid, ontvangt u een informatief bericht.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Cyclustellingswerk doen voor scenario 2

Nadat u het cyclustellingswerk hebt gemaakt, volgt u deze stappen om het werk uit te voeren in de mobiele app Warehouse Management.

1. Meld u aan bij de mobiele app Warehouse Management als de werkgebruiker die u hebt ingesteld in de sectie [Demogegevens voorbereiden voor de scenario's](#prepare-demo-data) eerder in dit artikel. In het voorbeeld in dit artikel heeft de gebruiker de naam *Julia Funderburk* en is deze ingesteld voor magazijn *61*. (Met de demonstratiegegevens van USMF moet u zich aanmelden als deze werkgebruiker door *61* in te voeren als gebruikers-id en *1* als wachtwoord.)
1. Selecteer **Voorraad** in het hoofdmenu.
1. Selecteer **Cyclustelling Blind** in het menu **Voorraad**.
1. Selecteer het veld **Zone-id**, voer *BULK06* in en selecteer **OK** (de vinkjesknop).
1. Selecteer het veld **Artikel**, voer *L0101* in en selecteer **OK** (de vinkjesknop).
1. Selecteer het veld **Nummerplaat**, voer *LP\_BULK\_06\_01* in en selecteer **OK** (de vinkjesknop).
1. Selecteer het veld **Hoev.**, voer *10* in en selecteer **OK** (de vinkjesknop).

    > [!NOTE]
    > Hoewel het systeem een verschil aantrof tussen de verwachte voorhanden hoeveelheid en de hoeveelheid die u hebt gescand, heeft het u niet gevraagd om een tweede keer te tellen omdat het veld **Aantal pogingen** is ingesteld op *0* (nul) voor de menuopdracht **Cyclustelling Blind** van het mobiele apparaat. U bent gevraagd om het artikelnummer en de nummerplaat te scannen, omdat zowel de optie **Artikelnummer weergeven** als de optie **Nummerplaat weergeven** is ingesteld op *Nee* voor de menuopdracht van het mobiele apparaat.

1. Selecteer **OK** (vinkjesknop).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>De cyclustellingsverschillen voor scenario 2 controleren

Volg deze stappen om de verschillen in de cyclustelling te controleren.

1. Keer terug naar Supply Chain Management.
1. Ga naar **Magazijnbeheer \> Algemeen \> Werk \> Cyclustellingswerk in afwachting van controle**.
1. Selecteer in het actievenster op het tabblad **Werk** de optie **Cyclustelling**.
1. Selecteer in het actievenster **Telling weigeren**.

    Omdat het tellingsverschil is geweigerd, wordt het werk afgesloten.

## <a name="scenario-3-spot-cycle-counting"></a>Scenario 3: Plaatscyclustelling

In de voorhanden-record staat dat er een voorhanden hoeveelheid is van artikel *L0101* op locatie *01A02R2S2B*. De magazijnmedewerker is op locatie *01A02R2S1B*. Hoewel deze locatie leeg moet zijn, is de locatie vol. Daarom doet de magazijnwerker onmiddellijk een plaatcyclusstelling voor deze locatie.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Cyclustellingswerk doen voor scenario 3

Volg deze stappen om het werk voor de cyclustelling uit te voeren in de mobiele app Warehouse Management.

1. Meld u aan bij de mobiele app Warehouse Management als de werkgebruiker die u hebt ingesteld in de sectie [Demogegevens voorbereiden voor de scenario's](#prepare-demo-data) eerder in dit artikel. In het voorbeeld in dit artikel heeft de gebruiker de naam *Julia Funderburk* en is deze ingesteld voor magazijn *61*. (Met de demonstratiegegevens van USMF moet u zich aanmelden als deze werkgebruiker door *61* in te voeren als gebruikers-id en *1* als wachtwoord.)
1. Selecteer **Voorraad** in het hoofdmenu.
1. Selecteer **Plaatcyclusstelling** in het menu **Voorraad**.
1. Selecteer het veld **Locatie**, voer *01A02R2S1B* in en selecteer **OK** (de vinkjesknop).

    Het systeem detecteert dat de locatie leeg is in Supply Chain Management.

1. Selecteer **LP of artikel toevoegen**.
1. Selecteer het veld **Artikel**, voer *L0101* in en selecteer **OK** (de vinkjesknop).
1. Selecteer het veld **Nummerplaat**, voer *LP\_BULK\_06\_01* in en selecteer **OK** (de vinkjesknop).
1. Selecteer het veld **Hoev.**, voer *9* in en selecteer **OK** (de vinkjesknop).

    Omdat het systeem detecteert dat de opgegeven nummerplaat al beschikbaar is op een andere locatie in Supply Chain Management, wordt die nummerplaat naar de huidige locatie verplaatst. Daarom wordt u gevraagd de verplaatsing te bevestigen.

1. Selecteer **OK** (vinkjesknop).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>De cyclustellingsverschillen voor scenario 3 controleren

Volg deze stappen om het cyclustellingsresultaat te controleren.

1. Keer terug naar Supply Chain Management.
1. Ga naar **Magazijnbeheer \> Algemeen \> Werkdetails**.
1. Schakel het selectievakje **Afgesloten weergeven** boven in het raster in.
1. Stel het filter voor de kolom **Werkordertype** in op *Voorraadmutatie*.

    Het systeem heeft deze telling automatisch gedetecteerd als voorraadmutatie. Deze mutatie is toegestaan omdat de optie **Verplaatsingen nummerplaat gedurende cyclustelling toestaan** is ingesteld op *Ja* voor magazijn *61* op de pagina **Magazijnen**.

## <a name="scenario-4-define-cycle-count-thresholds"></a>Scenario 4: drempels voor cyclustelling definiëren

Eén manier om werk voor cyclustellingen te maken, is drempels gebruiken. Een cyclustellingsdrempel wijst op de hoeveelheid of percentagelimiet van voorraadartikelen. Cyclustellingswerk wordt automatisch gemaakt wanneer de drempel wordt bereikt.

Er zijn bijvoorbeeld 60 artikelen op een locatie met een cyclustellingsdrempel van 40. Tijdens een verkoopordertransactie worden 25 artikelen verzameld vanaf de locatie en op een tijdelijke locatie geplaatst. Omdat de nieuwe artikeltelling minder is dan de drempelhoeveelheid van 35, wordt het cyclustelling werk automatisch aangemaakt voor de locatie.

Als u cyclustellingsdrempels wilt instellen, gaat u als volgt te werk:

1. Ga naar **Magazijnbeheer \> Instellingen \> Cyclustelling \> Drempels voor cyclustelling**.
1. Selecteer in het actievenster de optie **Nieuw** om een drempel te maken en stel hiervoor de volgende waarden in:

    - **Id cyclustellingsdrempel:** *L0101*
    - **Omschrijving:** *Drempel L0101*
    - **Drempelhoeveelheid:** *2*
    - **Eenheid:** *EA*
    - **Capaciteitsdrempel op basis van percentage:** *0,00*
    - **Type cyclustellingsdrempel:** *Hoeveelheid*
    - **Cyclustelling onmiddellijk verwerken:** *Ja*
    - **Dagen tussen cyclustellingen:** *1*
    - **Werkgroep-id:** *CycleCount*

1. Selecteer **Artikelen selecteren** in het actievenster.
1. Zoek in het dialoogvenster Query-editor op het tabblad **Bereik** de rij waar het veld **Veld** is ingesteld op *Artikelnummer*. Stel het veld **Criteria** voor die rij in op *L0101*.
1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.

    U hebt nu een drempel voor de cyclustelling voor artikel *L0101* gedefinieerd.

Er wordt nu een cyclustelling gemaakt voor artikel *L0101* op elke locatie als de voorhanden hoeveelheid kleiner is dan 2 en als de datum van de laatste cyclustelling voor de locatie niet vandaag is.

## <a name="scenario-5-define-cycle-count-plans"></a>Scenario 5: cyclustelplannen definiëren

Met cyclustelplannen kunt u het maken van cyclustellingswerk automatiseren. U kunt elk cyclustelplan instellen met specifieke artikel- en locatiequery's. Wanneer de batchtaak wordt uitgevoerd, wordt het werk voor de cyclustelling gemaakt voor alle locaties die overeenkomen met de criteria voor het artikel en de locatie (tot het maximum aantal tellingen dat voor het plan is opgegeven). Wanneer het cyclustellingswerk is gemaakt, bevat de werkregel voor de telling informatie over de locatie waar moet worden geteld. De voorhanden voorraad die aan die locatie is gekoppeld, is niet geblokkeerd. Deze is dus beschikbaar voor reservering en uitgaande verwerking, ook als er open tellingswerk bestaat.

Als u een cyclustelplan wilt instellen, gaat u als volgt te werk.

1. Ga naar **Magazijnbeheer \> Instellingen \> Cyclustelling \> Cyclustelplannen**.
1. Selecteer in het actievenster **Nieuw** om een rij toe te voegen aan het raster en er de volgende waarden voor in te stellen:

    - **Id cyclustelplan:** *BULK06*
    - **Omschrijving:** *Telling van locatie voor BULK06*
    - **Werkgroep-id:** *CycleCount*
    - **Maximumaantal cyclustellingen:** *10*
    - **Dagen tussen cyclustellingen:** *10*
    - **Lege locaties:** *Lege uitsluiten*
    - **Werksjabloon**: Laat dit veld leeg.

1. Selecteer **Locaties selecteren** in het actievenster.
1. Er wordt een standaarddialoogvenster voor Query-editor weergegeven. Voeg op het tabblad **Bereik** een rij toe en stel er de volgende waarden voor in:

    - **Tabel:** *Locaties*
    - **Veld:** *Zone-id*
    - **Criteria:** *BULK06*

1. Selecteer **OK** om het dialoogvenster Query-editor te sluiten.
1. Selecteer in het actievenster **Cyclustellingsplan verwerken**.
1. Stel in het dialoogvenster **Cyclustelplannen** op het sneltabblad **Op de achtergrond uitvoeren** de optie **Batchverwerking** in op *Ja*.
1. Selecteer **Terugkeerpatroon**.
1. Stel in het dialoogvenster **Terugkeerpatroon definiëren** de batchtaak zo in dat deze direct wordt gestart en elke minuut wordt uitgevoerd, zodat er geen einddatum is.
1. Selecteer **OK** om het dialoogvenster **Terugkeerpatroon definiëren** te sluiten.
1. Selecteer **OK** om het dialoogvenster **Cyclustelplannen** te sluiten.

    Er wordt een bericht weergegeven dat de taak is toegevoegd aan de batchwachtrij.

1. Klik op **Magazijnbeheer \> Algemeen \> Planning cyclustelling**. Het plan begint onmiddellijk en maakt tellingswerk. Omdat het tellingswerk niet is voltooid, wordt het veld **Status** ingesteld op *Onderhanden*. Na één minuut wordt de waarde in de kolom **Totale cyclustellingen** gewijzigd in *1*.

    > [!NOTE]
    > Het cyclustellingswerk wordt niet gemaakt als het aantal dagen sinds de laatste cyclustelling kleiner is dan de waarde die u hebt ingesteld voor het veld **Dagen tussen cyclustellingen** voor het cyclustellingsplan. Als de waarde in het veld **Dagen tussen cyclustellingen** bijvoorbeeld *5* is, wordt om de vijf dagen cyclustellingswerk gemaakt. Als het cyclustellingswerk echter op dag drie wordt verwerkt, wordt het volgende cyclustellingswerk gecreëerd vijf dagen nadat de laatste cyclustelling werd verwerkt, dus op dag acht.

1. Selecteer **Werk** in het actievenster om het gemaakte tellingswerk weer te geven.
