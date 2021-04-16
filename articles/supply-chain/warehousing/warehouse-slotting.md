---
title: Magazijnvakken
description: Dit onderwerp biedt informatie over magazijnvakken. Met magazijnvakken kunt u de vraag consolideren op basis van artikel en maateenheid vanuit orders met de status Besteld, Gereserveerd of Vrijgegeven. Hiermee kunnen magazijnbeheerders orderverzamellocaties intelligent plannen voordat orders naar het magazijn worden vrijgegeven en het orderverzamelwerk wordt gemaakt.
author: mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0dd1f42b7bb337ccb65b7e4bdd9d307d074ae0d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838149"
---
# <a name="warehouse-slotting"></a>Magazijnvakken

[!include [banner](../includes/banner.md)]

Met de diverse functies voor magazijnvakken kunnen magazijnbeheerders orderverzamellocaties intelligent plannen voordat orders naar het magazijn worden vrijgegeven en het orderverzamelwerk wordt gemaakt.

Met *Functie voor magazijnvakken* kunt u de vraag consolideren op basis van artikel en maateenheid vanuit orders met de status *Besteld*, *Gereserveerd* of *Vrijgegeven*. Gegenereerde vraag kan vervolgens worden toegepast op locaties die worden gebruikt voor orderverzamelen, op basis van hoeveelheid, eenheid, fysieke afmetinge, vaste locaties en meer. Nadat het vakkenplan is ingesteld, kunt u aanvullingswerk maken om de gewenste voorraadhoeveelheid naar alle locaties te brengen.

Met de functie *Magazijnvakken voor overboekingsorders* kunnen magazijnbeheerders de orderverzamellocaties aanvullen op basis van de vraag vanuit overboekingsorders die nog niet zijn vrijgegeven aan het magazijn. Hiermee zorgt u ervoor dat verzamellocaties alle artikelen bevatten die nodig zijn voor de overboekingsorders nadat ze zijn vrijgegeven aan het magazijn. Voor deze functie moet u ook de functie *Functie voor magazijnvakken* inschakelen.

Met de functie *Uitbreidingen voor vakkentoewijzing in magazijn* voegt u een optie toe voor de sjabloonregels die worden gebruikt door de functie *Functie voor magazijnvakken*. Met deze optie kan het systeem rekening houden met de bestaande voorhanden voorraad op een doellocatie. Het is dus mogelijk dat er minder aanvullingen worden gegenereerd voor magazijnvakken. Voor de functie *Uitbreidingen voor vakkentoewijzing in magazijn* moet u ook de functie *Functie voor magazijnvakken* inschakelen. Deze kan optioneel worden gebruikt in combinatie met de functie *Magazijnvakken voor overboekingsorders*.

## <a name="turn-on-the-warehouse-slotting-features"></a>De functies voor magazijnvakken inschakelen

Voordat u deze functies kunt gebruiken, moeten deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functies te controleren en deze zo nodig in te schakelen. Schakel zo nodig de volgende functies in:

- Functie Magazijnvakken
- Magazijnvakken voor overboekingsorders

    > [!IMPORTANT]
    > De functie *Functie voor magazijnvakken* moet voor deze functie zijn ingeschakeld.

- Uitbreidingen voor vakkentoewijzing in magazijn

    > [!IMPORTANT]
    > De functie *Functie voor magazijnvakken* moet voor deze functie zijn ingeschakeld.

## <a name="set-up-warehouse-slotting"></a>Magazijnvakken instellen

Om magazijnvakken te gebruiken, moet u de volgende elementen configureren in het systeem:

- Niveaus van maateenheden voor vakken
- Instructiecodes
- Vaksjablonen
- Locatie-instructies

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Niveaus van maateenheden maken voor vakken

Met niveaus van maateenheden kunnen meerdere maateenheden samen worden gegroepeerd ten behoeve van de vakken. Als bijvoorbeeld dozen met verschillende formaten allemaal worden verzameld in hetzelfde gebied voor doosverzamelen, kunt u één niveau maken voor alle formaten. **U moet een regel maken voor elke maateenheid die deel moet uitmaken van het niveau.**

1. Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Niveaus van maateenheden voor vakken**.
1. Selecteer **Nieuw**.
1. Stel in de koptekst de volgende waarden in:

    - **Maateenheid niveau:** *EaBoxPl*
    - **Beschrijving:** *Each doos pallet*

1. Selecteer **Opslaan**.
1. Ga naar het sneltabblad **Maateenheden** en selecteer **Nieuw** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Eenheid:** *Doos*
    - **Beschrijving:** Laat dit veld leeg. Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.
    - **Eenheidsklasse:** *Hoeveelheid*

1. Selecteer **Nieuw** om een tweede regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Eenheid:** *EA*
    - **Beschrijving:** Laat dit veld leeg. Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.
    - **Eenheidsklasse:** *Hoeveelheid*

1. Selecteer **Nieuw** om een derde regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Eenheid:** *PL*
    - **Beschrijving:** Laat dit veld leeg. Dit wordt automatisch ingevuld wanneer u de wijzigingen opslaat.
    - **Eenheidsklasse:** *Hoeveelheid*

1. Selecteer **Opslaan** om het niveau op te slaan.

### <a name="create-a-directive-code-for-slotting"></a>Een instructiecode maken voor vakken

U moet de instructiecode selecteren die aan een sjabloon moet worden gekoppeld.

1. Ga naar **Magazijnbeheer \> Instellen \> Instructiecodes**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het veld **Instructiecode** de tekst *Vakken* in.
1. Voer in het veld **Instructiebeschrijving** de tekst *Vakken* in.

### <a name="set-up-slotting-templates"></a>Vakkensjablonen configureren

Elke vakkensjabloon bepaalt hoe de voorraad wordt toegewezen aan locaties voor een bepaald magazijn. Elke sjabloon moet voor elke vakspecificatie een regel bevatten. Met de procedures in deze sectie kunt u vakkensjablonen instellen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen**.
1. Selecteer **Nieuw** om een sjabloon te maken.

Vervolgens moet u de koptekst van de sjabloon, vakspecificaties en de locatie-instructies instellen, zoals in de volgende subsecties wordt uitgelegd. De instelling voor overboekingsorders lijkt op de instelling voor magazijnvakken voor verkooporders, maar het veld **Type vraag** wordt ingesteld op *overboekingsorders* in plaats van op *Verkooporder*.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>De koptekst instellen voor een vakkensjabloon voor verkooporders

1. Stel in de koptekst van de sjabloon de volgende waarden in:

    - **Vaksjabloon:** _61_
    - **Beschrijving:** _61_
    - **Vraagtype:** *Verkooporder*

        > [!NOTE]
        > Momenteel zijn *Verkooporders* en *overboekingsorders* de enige ondersteunde vraagtypen. U kunt *overboekingsorders* alleen selecteren als de functie *Magazijnvakken voor overboekingsorders* is ingeschakeld.

    - **Vraagstrategie:** _Besteld_

        De volgende waarden zijn beschikbaar in dit veld:

        - **Besteld:** De volledige bestelde hoeveelheid op de verkooporder moet als vraag worden beschouwd.
        - **Gereserveerd:** Alleen de verkooporderregelhoeveelheden die zijn gereserveerd (fysiek en besteld) moeten als vraag worden beschouwd.
        - **Vrijgegeven**: de vrijgegeven hoeveelheid moet als vraag worden beschouwd.

    - **Magazijn:** _61_
    - **Gebruik van niet-gereserveerde hoeveelheid door waveaanvraag toestaan:** _Ja_

U kunt ook een query opgeven om het bereik te beperken van de vraag die wordt beoordeeld.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Vakspecificaties instellen voor elke sjabloon

Voer voor elke verkooporder die u maakt de volgende stappen uit om een regel voor elke vakspecificatie toe te voegen.

1. Ga naar het sneltabblad **Vaksjabloondetails** en selecteer **Nieuw** om een sjabloonregel te maken.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Reeks:** _1_
    - **Beschrijving:** _Vaste locatie_
    - **Minimumhoeveelheid:** _1_

        Dit veld bepaalt de minimumhoeveelheid van vraag die nodig is voor de regel.

    - **Maximumhoeveelheid:** _1000000_

        Dit veld bepaalt de maximumhoeveelheid van vraag die geldig is voor de regel.

    - **Eenheid:** Laat dit veld leeg.

        Dit veld bepaalt de maateenheid waarnaar de minimum- en maximumhoeveelheden verwijzen.

    - **Maateenheid niveau:** _EaBoxPl_

        Dit veld bepaalt de maateenheden van vraag die geldig zijn voor de regel. (Voor meer informatie, zie de sectie [Niveaus van maateenheden maken voor vakken](#unit-tiers) eerder in dit onderwerp.)

    - **Criteria voor vaktoewijzing:** _Hoeveelheid overwegen_

        De volgende waarden zijn beschikbaar in dit veld:

        - **Uitgaan van leeg:** Er moet vanuit worden gegaan dat alle locaties in het orderverzamelgebied leeg zijn en dat deze locaties niet moeten worden gecontroleerd op voorraad.
        - **Hoeveelheid overwegen:** De lcoaties in het orderverzamelgebied moete worden gecontroleerd op voorraad en alle locaties die niet leeg zijn, moeten worden overgeslagen.
        - **Voorhanden voorraad in aanmerking nemen**: het systeem controleert of een doellocatie niet-gereserveerde hoeveelheden bevat voor het artikel op de vraagregel. Als de hoeveelheid groot genoeg is om te voldoen aan ten minste één eenheid van de vraagregel, wordt de gegenereerde vakkenplanrecord verlaagd met de beschikbare hoeveelheid. Als de vraag bijvoorbeeld 10 kisten is en er één kist voorhanden is, wordt de gevonden vraag negen kisten. Als de vraag bijvoorbeeld 10 kisten is en elke kist voorhanden is, wordt de gevonden vraag 10 kisten. Deze waarde is alleen beschikbaar wanneer de functie *Uitbreidingen voor vakkentoewijzing in magazijn* is ingeschakeld.

    - **Instructiecode:** _Vakken_

        In dit veld wordt de locatie-instructie gedefinieerd die wordt gebruikt om de orderverzamellocatie van het aanvullingswerk te zoeken.

    - **Overlooplocatie:** Laat dit veld leeg.

        In dit veld wordt de locatie gedefinieerd waar de voorraad wordt geplaatst als geen locatie voor de hoeveelheid wordt gevonden wanneer de regel wordt verwerkt.

    - **Afname toestaan:** _Ja_

        Als deze optie is ingesteld op *Ja* en er vraag is die niet in vakken kan worden geplaatst, wordt mutatiewerk gemaakt om de voorraad weg te nemen van locaties waar er voorraad is, maar waar niets in vakken is geplaatst. De sjabloon wordt vervolgens opnieuw uitgevoerd. Deze keer word de voorraad op de locaties genegeerd. Deze functionaliteit werkt het beste wanneer het veld **Criteria voor vaktoewijzing** is ingesteld op _Hoeveelheid overwegen_.

    - **Gebruik vaste locaties:** _Alleen vaste locaties voor het product_

        De volgende waarden zijn beschikbaar in dit veld:

        - **Vaste en niet-vaste locaties:** Het systeem mag niet worden beperkt tot het gebruik van vaste locaties.
        - **Alleen vaste locaties voor het product:** Het systeem moet alleen vakken toewijzen voor locaties die vaste locaties zijn voor het product.
        - **Alleen vaste locaties voor de productvarian:** Het systeem moet alleen vakken toewijzen voor locaties die vaste locaties zijn voor de productvariant.

> [!NOTE]
> Als de vakkensjabloon ten minste één regel bevat waar het veld **Criteria voor vaktoewijzing** is ingesteld op *Voorhanden voorraad in aanmerking nemen*, zijn afnames niet langer toegestaan voor alle regels in de sjabloon.

1. Selecteer **Opslaan**.
1. Selecteer **Nieuw** om een tweede sjabloonregel te maken.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Reeks:** _2_
    - **Beschrijving:** _Overige_
    - **Minimale hoeveelheid:** _1_
    - **Maximale hoeveelheid:** _1000000_
    - **Eenheid:** Laat dit veld leeg.
    - **Maateenheid niveau:** _EaBoxPl_
    - **Criteria voor vaktoewijzing:** _Hoeveelheid overwegen_
    - **Instructiecode:** _Vakken_
    - **Overlooplocatie:** Laat dit veld leeg.
    - **Afname toestaan:** _Ja_
    - **Vaste locaties gebruiken:** _Vaste en niet-vaste locaties_

    In de query voor de tweede regel geeft u nu de criteria op waarmee wordt bepaald naar welke locaties de vraag voor die regel kan worden toegewezen.

1. Selecteer de regel waarin het veld **Volgnummer** is ingesteld op *2*.
1. Selecteer **Query bewerken**.
1. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Tabel:** *Locaties*
    - **Afgeleide tabel:** *Locaties*
    - **Veld:** *Locatieprofiel-id*
    - **Criteria:** *Pick-06* (Selecteer het dubbele plusteken \[**++**\] in het veld om de lijst uit te vouwen en selecteer vervolgens *Pick-06* - *Orderverzamellocatie 6*.)

1. Selecteer **OK**.

#### <a name="set-up-location-directives"></a>Locatie-instructies instellen

Er moet ten minste één locatie-instructie zijn ingesteld om het toewijzen van orderverzamelen te ondersteunen. Met de procedures in deze sectie kunt u een nieuwe *aanvullingslocatie-instructie* instellen om orderverzamelen toe te wijzen.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Selecteer in het linkerdeelvenster in het veld **Werkordertype** de waarde *Aanvulling*.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in de koptekst van de nieuw locatie-instructie in het veld **Naam** de tekst *61 Slotting pick* in.
1. Accepteer de standaardwaarde in het veld **Volgnummer**.

##### <a name="configure-the-location-directives-fasttab"></a>Het sneltabblad Locatie-instructies configureren

1. Stel op het sneltabblad **Locatie-instructies** de volgende waarden in. Accepteer de standaardwaarden voor alle overige velden.

    - **Werktype:** _Orderverzamelen_
    - **Locatie:** _6_
    - **Magazijn:** _61_
    - **Instructiecode:** _Vakken_

1. Selecteer **Opslaan** om het sneltabblad **Regels** beschikbaar te maken.

##### <a name="configure-the-lines-fasttab"></a>Het sneltabblad Regels configureren

1. Selecteer op het sneltabblad **Regels** de optie **Nieuw** om een regel te maken.
1. Stel op de nieuwe regel de volgende waarden in.

    - **Vanaf hoeveelheid:** _0_
    - **Tot hoeveelheid:** _1000000_

1. Accepteer de standaardwaarden voor de overige velden.
1. Selecteer **Opslaan** om het sneltabblad **Locatie-instructieacties** beschikbaar te maken.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Het sneltabblad Locatie-instructieacties configureren

1. Ga naar het sneltabblad **Locatie-instructieacties** en selecteer **Nieuw** om een regel te maken.
1. Stel op de nieuwe regel de volgende waarden in. Accepteer de standaardwaarden voor alle overige velden.

    - **Volgnummer:** Accepteer de standaard waarde.
    - **Naam:** _Bulk_
    - **Strategie:** _Geen_

1. Accepteer de standaardwaarden voor de overige velden.
1. Selecteer **Opslaan** om de knop **Query bewerken** beschikbaar te maken.

##### <a name="edit-the-query"></a>De query bewerken

1. Selecteer op het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.
1. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een regel toe te voegen aan het raster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Tabel:** *Locaties*
    - **Afgeleide tabel:** *Locaties*
    - **Veld:** *Zone-id*
    - **Criteria:** *Bulk* (Selecteer het dubbele plusteken \[**++**\] in het veld om de lijst uit te vouwen en selecteer vervolgens *Bulk*.)

1. Selecteer **OK**.

## <a name="scenario"></a>Scenario's

### <a name="set-up-the-scenario"></a>Het scenario configureren

Gebruik voor dit scenario de ingebouwde voorbeeldgegevens en maak de records die in deze sectie worden beschreven.

#### <a name="use-the-usmf-sample-data"></a>De voorbeeldgegevens voor USMF gebruiken

Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

#### <a name="create-demand"></a>Vraag maken

Voer de volgende stappen uit om de vraag te maken waarop u het toewijzen van vakken gaat toepassen.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om een verkooporder te maken.
1. Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde _US-007_.
1. Selecteer **61** in het veld _Magazijn_.
1. Selecteer **OK**.
1. De nieuwe verkooporder wordt geopend. Deze bevat een lege rij in het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikel:** _L0101_
    - **Hoeveelheid:** _20_

1. Selecteer **Regel toevoegen** om een nieuwe regel toe te voegen en stel de volgende waarden in:

    - **Artikel:** _T0100_
    - **Hoeveelheid:** _8_

1. Selecteer **Opslaan**.
1. Selecteer **Nieuw** om een tweede verkooporder te maken.
1. Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde _US-008_.
1. Selecteer **61** in het veld _Magazijn_.
1. De nieuwe verkooporder wordt geopend. Deze bevat een lege rij in het sneltabblad **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikel:** _T0100_
    - **Hoeveelheid:** _1_

1. Selecteer **Opslaan**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Een veelvoorkomend scenario voor vaktoewijzing doorlopen

Nadat alle vereiste elementen zijn geïmplementeerd zoals beschreven in het vorige gedeelte, kunt u de functie uitproberen door alle oefening in deze sectie te doorlopen.

#### <a name="generate-demand"></a>Vraag genereren

1. Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Vakkensjablonen** en selecteer de vakkensjabloon die u eerder hebt gemaakt.
1. Selecteer **Vraag genereren** in het actievenster. Met deze opdracht evalueert u alle vraag in het systeem die voldoet aan de criteria in de query op de vakkensjabloon. De totale vraag voor alle orders wordt vervolgens geconsolideerd in één regel per hoeveelheid/eenheid. Er wordt een informatief bericht weergegeven wanneer het proces is voltooid.

#### <a name="slotting-demand"></a>Vraag per vak

De *vakkenvraag* geeft de resultaten weer van het genereren van de vraag op basis van de instellingen van de vakkensjabloon.

- Selecteer in het actievenster **Vakkenvraag** om de resultaten weer te geven van de opdracht **Vraag genereren**. De regels in de vakkenvraag kunnen worden bewerkt. U kunt een regel verwijderen, een nieuwe regel toevoegen of de regeldetails bewerken.

> [!NOTE]
> U kunt de vraag handmatig bewerken of u kunt deze vanuit een extern systeem importeren met gegevensbeheer. Wat er in de vakvraag staat, wordt in de volgende stap gebruikt, ongeacht waar de vraag vandaan komt.

#### <a name="locate-demand"></a>Vraag zoeken

Nadat de vraag is gegenereerd, moet u de opdracht **Vraag zoeken** gebruiken om het *vakkenplan* te genereren.

- Selecteer **Vraag zoeken** in het actievenster. Het vakkenproces wordt uitgevoerd. Er wordt een informatief bericht weergegeven wanneer het proces is voltooid.

#### <a name="slotting-plan"></a>Plan voor vakken

Het vakkenplan toont de locatie waaraan elk artikel/elke hoeveelheid is toegewezen, of de overschrijding is gebruikt, of afnamewerk is gemaakt, en de sjabloonregel die werd gebruikt. *Elke vraag die niet aan vakken kan worden toegewezen, is rood gemarkeerd.*

- Selecteer in het actievenster de optie **Vakkenplan** om de resultaten weer te geven.

> [!NOTE]
> - De processen **Vraag genereren**, **Vraag zoeken** en **Aanvulling uitvoeren** worden nu in een sandbox uitgevoerd. (Deze processen zijn beschikbaar vanuit het actievenster op de pagina **Vakkensjablonen**.)
> - De processen **Vraag genereren**, **Vraag zoeken** en **Aanvulling uitvoeren** hebben een vergrendeling om ervoor te zorgen dat deze niet tegelijkertijd kunnen worden geactiveerd. Anders kunnen de gegevens die worden gebruikt, worden verwijderd.
> - De processen **Vraag genereren** en **Vraag zoeken** geven een waarschuwing weer als de uitvoering geen records heeft gegenereerd of als er gegevens ontbreken in de records.
> - Wanneer u **Vakkenplan** selecteert, bevat de pagina geen knoppen **Nieuw**, **Bewerken** of **Verwijderen** in het actievenster, omdat de gegevensbron niet kan worden bewerkt.
> - Wanneer u **Aanvulling uitvoeren** selecteert, valideert het systeem de geselecteerde vakkensjabloon en -processen.

#### <a name="create-replenishment"></a>Aanvulling maken

Nadat het vakkenplan is gemaakt, moet u *aanvullingswerk maken* op basis van het plan.

- Selecteer **Aanvulling uitvoeren** in het actievenster. Er wordt een informatief bericht weergegeven wanneer het proces is voltooid. Dit bericht geeft het aantal kopteksten aan dat is gemaakt voor de werkbuild-id.

De locatie-instructies die worden gebruikt, worden geïdentificeerd op basis van de instructiecode die op elke sjabloonregel is opgegeven.

## <a name="tips"></a>Tips

### <a name="set-up-automatic-slotting"></a>Automatisch vakkentoewijzing configureren

Nadat alle vereiste elementen zijn ingesteld, kunt u vaktoewijzing configureren om automatisch te worden uitgevoerd. U doet dit met de volgende stappen.

1. Ga naar **Magazijnbeheer \> Aanvulling \> Vakken uitvoeren**.
1. Geef op welke vakkenstappen moeten worden uitgevoerd. Selecteer een of meer van de volgende vakkenstappen:

    - Vraag genereren
    - Vraag zoeken
    - Aanvullingswerk maken

    > [!NOTE]
    > De vakkenstappen zijn progressief. Als u de optie *Vraag zoeken* wilt selecteren , moet u eerst de optie *Vraag genereren* selecteren.

1. Geef op welke vakkensjabloon u wilt laten gebruiken.
1. Stel het herhalingspatroon desgewenst in op automatisch herhalen.

Stel voor de oefeningen in het scenario **niet** automatische vaktoewijzing in.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]