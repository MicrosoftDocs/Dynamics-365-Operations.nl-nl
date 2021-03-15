---
title: Bevestigen en overboeken
description: In dit onderwerp wordt uitgelegd hoe u de functie Bevestigen en overboeken gebruikt, waarmee gebruikers ladingen uit het magazijn kunnen verzenden voordat ze alle werkzaamheden uitvoeren die gerelateerd zijn aan die ladingen.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ccfbe30e9d4a0fc4580c7036d222bfca9203a21
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996321"
---
# <a name="confirm-and-transfer"></a>Bevestigen en overboeken

[!include [banner](../includes/banner.md)]

Met de functie *Bevestigen en overboeken* kunnen gebruikers ladingen uit het magazijn verzenden voordat ze alle werkzaamheden uitvoeren die gerelateerd zijn aan die ladingen. Wanneer een zending wordt ontvangen met ladingsregels die niet volledig zijn verzameld, wordt de bevestigende gebruiker gevraagd de resterende hoeveelheden te splitsen naar een nieuwe lading of om de onvolledige hoeveelheden te annuleren.

Systemen die zijn ingesteld om het splitsen van ladingen toe te staan, ondersteunen scenario's waarin geplande en gedeeltelijk geladen ladingen moeten worden aangepast vanwege nieuwe of veranderende omstandigheden.

De client bevat logica waarmee een gedeeltelijk ingeladen lading kan worden gesloten en bevestigd als verzonden. Alle resterende verzendingen en ladingsregels (inclusief volledige of gedeeltelijke regelhoeveelheden) worden vervolgens doorgevoerd naar een nieuw gemaakte lading en zending, als deze rollover is vereist en de instelling dit toestaat. Nieuwe zendingen en ladingen worden automatisch gemaakt op basis van de initiële criteria voor het maken van zendingen en ladingen en hun hoofdkenmerken blijven ongewijzigd. Er is ook een optie voor het automatisch annuleren van resterende hoeveelheden, als een werkorder nog niet is gemaakt en de gebruiker deze annulering nodig acht.

Deze functionaliteit ondersteunt scenario's waarin de volledige lading niet in één vrachtwagen past of waarbij een deel van de lading het magazijn moet verlaten voordat de rest van de lading gereed is voor verzending. In deze scenario's kunnen de resterende producten worden overgeboekt naar een nieuwe lading en dus naar een nieuwe vrachtwagen. Omdat deze functie kan worden gebruikt met ladingen die anders zijn bedoeld om een zending met een volledige lading te vereisen, biedt dit extra flexibiliteit zodat transportbeheerders scenario's die onvoorzien of niet standaard zijn kunnen oplossen.

Wanneer een lading is gesplitst, voert de functie *Bevestigen en overboeken* de volgende acties uit:

- Waar nodig worden nieuwe ladingen en zendingen aangemaakt. Elke lading of zending heeft grotendeels dezelfde kenmerken als de oorspronkelijke lading of zending. De uitzondering is de ladingsstatus, die opnieuw wordt berekend op basis van de werkstatus.
- De gebruiker wordt geïnformeerd dat een nieuwe lading is gemaakt. De gebruiker krijgt ook een melding met de id van de nieuwe lading.
- De ladingsregels, werkkoptekst en werkregels die zijn gesplitst, worden bijgewerkt met de gegevens van de nieuwe lading en zending.
- Als een hele zending wordt gesplitst, blijft de zending behouden en worden alleen de ladingsverwijzingen bijgewerkt. Als de zending moet worden opgesplitst, wordt een nieuwe zending gemaakt.

Wanneer de resterende hoeveelheden worden geannuleerd, worden de hoeveelheden van de ladingregel die niet zijn verzameld en waaraan geen geannuleerd werk is gekoppeld, uit de lading verwijderd. Als er werk wordt uitgevoerd, kan de gebruiker de lading alleen splitsen. Resterende hoeveelheden kunnen niet worden geannuleerd.

U kunt alleen ladingen splitsen die voldoen aan de volgende criteria:

- Een of meer ladingregels hebben hoeveelheden die zijn verzameld.
- De ladingsstatus is minder dan geladen.
- Er zijn geen gegevens voor de ladingregel. (Deze gegevens worden gemaakt via de consolidatie van de nummerplaat op de klaarzetlocatie. De functie *Bevestigen en overboeken* ondersteunt geen nummerplaatconsolidatie.)
- Er is geen voorraad die wacht op verpakking op een verpakkingslocatie. (De functie *Bevestigen en overboeken* ondersteunt geen voorraad die is verzameld en op het verpakkingsstation staat, maar nog niet is ingepakt.)

> [!NOTE]
> Deze functionaliteit verschilt van de functie transportlading, die moet worden gebruikt in magazijnen die nooit ladingen kunnen plannen en maken vóór het orderverzamelen, maar die in plaats daarvan de beschikbare transportruimte laden nadat het orderverzamelen is voltooid.
>
> Gebruik de functie *Bevestigen en overboeken* in situaties waarin de lading meestal van tevoren wordt gepland en aangemaakt, maar waarin soms uitzonderingen optreden waarbij de lading niet past in het beschikbare transportmiddel (zoals een vrachtwagen).

## <a name="turn-on-confirm-and-transfer"></a>Bevestigen en overboeken inschakelen

Voordat u de functie *Bevestigen en overboeken* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Bevestigen en overboeken*

## <a name="set-up-confirm-and-transfer"></a>Bevestigen en overboeken configureren

Om de functie *Bevestigen en overboeken* te gebruiken, moet u deze inschakelen in elke relevante ladingsslabloon. Bovendien kunt u, afhankelijk van uw behoeften, uw werksjablonen voorbereiden om deze functie te ondersteunen. Als u het voorbeeldscenario wilt doorlopen dat verderop in dit onderwerp wordt beschreven, stelt u uw systeem in zoals in deze sectie wordt beschreven. Dit scenario is gebaseerd op **USMF**-voorbeeldgegevens.

### <a name="prepare-your-load-templates"></a>De ladingssjablonen voorbereiden

1. Ga naar **Magazijnbeheer \> Instellen \> Lading \> Ladingssjablonen**.
1. Selecteer in het actievenster de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. Schakel het selectievakje **Lading splitsen toestaan tijdens verzending bevestigen** in voor elke sjabloon waarvoor u de functie wilt inschakelen. U kunt ook **Nieuw** selecteren om een nieuwe sjabloon te maken en deze naar wens te configureren. Elke lading die u maakt met die sjabloon, neemt deze functionaliteit over. (Als u werkt met de **USMF**-voorbeeldgegevens, schakelt u de functie in voor de ladingssjabloon **20' Container**.)

### <a name="prepare-your-work-templates"></a>De werksjablonen voorbereiden

Het is niet voor alle situaties vereist om dit te configureren. Het volgende voorbeeld zorgt ervoor dat werk per zending kan worden opgesplitst, ter ondersteuning van het voorbeeldscenario dat verderop in dit onderwerp wordt besproken. Er zijn ook andere manieren om dit resultaat te bereiken.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Selecteer in het raster in het bovenste gedeelte van de pagina een bestaande werksjabloon waarvoor u de functie *Bevestigen en overboeken* wilt instellen. (Als u werkt met de **USMF**-voorbeeldgegevens, selecteert u de werksjabloon **51 Orderverzamelen naar klaarzetten**. U kunt er ook voor kiezen om een nieuwe werksjabloon te maken.)
1. Selecteer in het actievenster de optie **Query bewerken** om het dialoogvenster **Verkoop** te openen.
1. Selecteer in het dialoogvenster **Verkoop** op het tabblad **Sorteren** de optie **Toevoegen** om een rij aan het raster toe te voegen.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Tabel:** *Tijdelijke werktransacties*
    - **Afgeleide tabel:** *Tijdelijke werktransacties*
    - **Veld:** *Zending-id*
    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK** om de instellingen op te slaan en het dialoogvenster **Verkoop** te sluiten.
1. Als u een melding krijgt waarin wordt aangegeven dat groepering opnieuw wordt ingesteld, selecteert u **Ja** om door te gaan.
1. Selecteer in het raster in het bovenste gedeelte van de pagina **Werksjablonen** de sjabloon die u zojuist hebt bewerkt en selecteer vervolgens in het actievenster de optie voor **Opsplitsingen voor werkkoptekst**.
1. Selecteer in het actievenster de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. Stel in het raster de volgende waarden in:

    - **Tabelnaam:** *Tijdelijke werktransacties*
    - **Veldnaam:** *Zending-id*
    - **Groeperen op dit veld:** Schakel dit selectievakje in.

1. Selecteer **Opslaan** in het actievenster.
1. Sluit de pagina.

## <a name="scenario"></a>Scenario's

In dit scenario ziet u een voorbeeld waarin het orderverzamelproces nog niet is voltooid, maar de artikelen die tot nu toe zijn verzameld toch al in een vrachtwagen moeten worden geladen en verzonden. De gebruiker kan hierdoor de niet-verzamelde ladingsregels splitsen naar een nieuwe lading. Alle gegevensrelaties worden dan automatisch bijgewerkt.

> [!NOTE]
> De specifieke waarden die in dit scenario worden beschreven, zijn gebaseerd op de **USMF**-voorbeeldgegevens. U wordt aangeraden deze voorbeeldgegevens te gebruiken terwijl u het gebruik van deze functie demonstreert of leert hoe u deze gebruikt. Als u de **USMF**-voorbeeldgegevens niet gebruikt, moet u uw eigen waarden zo nodig invullen.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>Stap 1: Maak een lading met meerdere ladingsregels

Voordat u deze functionaliteit kunt gebruiken, moet u een lading hebben met meerdere ladingsregels. U moet er ook voor zorgen dat de de picklocaties voldoende voorraad hebben voor alle artikelen op alle verkooporders die u gaat maken. Controleer de configuratie van de locatie-instructie (**Magazijnbeheer \> Instellen \> Locatie-instructies**) en noteer de orderverzamellocaties die worden gebruikt voor het verzamelen van verkooporders. Als u de voorraad moet corrigeren, maak dan handmatige verplaatsingen en gebruik aanvulling of elke andere stroom die hiervoor nodig is.

Om een kwalificerende lading te maken, maakt u eerst drie verkooporders door de volgende stappen uit te voeren.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer in het actievenster de optie **Nieuw** om het dialoogvenster **Verkooporder maken** te openen.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in (minimumwaarden):

    - Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-004* (*Cave Wholesales*).
    - Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *51*.

1. Selecteer **OK** om het dialoogvenster **Verkooporder maken** te sluiten en de nieuwe verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Voeg in het raster **Verkooporderregels** een regel toe met de volgende waarden:

    - **Artikelnummer:** *M9200*
    - **Hoeveelheid:** *40*
    - **Eenheid:** *EA*

1. Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer in het actievenster de optie **Partij reserveren** om de pagina **Reservering** te openen.
1. Reserveer de voorraad op de verkoopregel en sluit vervolgens de pagina **Reservering**.
1. Voeg een tweede verkooporder toe voor dezelfde klant en hetzelfde magazijn door de stappen 1 tot en met 4 te herhalen.
1. Voeg twee verkoopregels toe met de volgende waarden. Telkens nadat u een regel hebt toegevoegd, reserveert u voorraad ervoor volgens de beschrijving in stappen 6 tot en met 8.

    - **Regel 1:** Stel op de nieuwe regel het veld **Artikelnummer** in op *M9200* en het veld **Hoeveelheid** op *30* en het veld **Eenheid** op *ea*.
    - **Regel 2:** Stel op de nieuwe regel het veld **Artikelnummer** in op *M9201* en het veld **Hoeveelheid** op *20* en het veld **Eenheid** op *ea*.

1. Voeg een derde verkooporder toe voor dezelfde klant en hetzelfde magazijn door de stappen 1 tot en met 4 te herhalen.
1. Voeg twee verkoopregels toe met de volgende waarden. Telkens nadat u een regel hebt toegevoegd, reserveert u voorraad ervoor volgens de beschrijving in stappen 6 tot en met 8.

    - **Regel 1:** Stel op de nieuwe regel het veld **Artikelnummer** in op *M9201* en het veld **Hoeveelheid** op *20* en het veld **Eenheid** op *ea*.
    - **Regel 2:** Stel op de nieuwe regel het veld **Artikelnummer** in op *M9202* en het veld **Hoeveelheid** op *60* en het veld **Eenheid** op *ea*.

#### <a name="load-planning-workbench"></a>Workbench ladingplanning

In de workbench voor ladingplanning wordt de id van de ladingssjabloon gebruikt om de zendingen te maken en de verkooporderregels vrij te geven naar het magazijn.

1. Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.
1. Selecteer **51** in het veld *Magazijn*.

    Nu gaat u de lading samenstellen voor de verkooporders die u zojuist hebt gemaakt.

1. Selecteer op het tabblad **Verkoopregels** in het raster de verkoopregels voor de nieuwe verkooporders.
1. Selecteer in het actievenster op het tabblad **Vraag en aanbod** in de groep **Toevoegen** de optie **Aan nieuwe lading**.
1. Stel in het dialoogvenster **Ladingsjabloon toewijzen** het veld **Ladingsjabloon-id** in op *20' Container*.
1. Selecteer **OK**.
1. Zoek in de sectie **Ladingen** van de pagina **Workbench ladingplanning** in het raster de nieuw gemaakte ladings-id voor magazijn *51*. Schuif naar rechts totdat u de kolom **Lading splitsen toestaan tijdens verzending bevestigen** ziet. Het selectievakje moet zijn ingeschakeld voor uw lading.
1. Selecteer de lading.
1. Selecteer in het menu **Vrijgeven** boven het raster de optie **Vrijgeven naar magazijn** om werk te maken.
1. Controleer in het dialoogvenster **Lading vrijgeven naar magazijn** of op het tabblad **Op te nemen records** uw ladings-id wordt weergegeven.
1. Selecteer **OK**.

    Mogelijk wordt het bericht "Bezig met verwerken" getoond terwijl het systeem de zendingen en het werk aanmaakt.

1. In de sectie **Ladingen** van de pagina **Workbench ladingplanning** moet de lading nu de status *In wave* hebben. Selecteer de lading en selecteer vervolgens in het menu **Verwante informatie** boven het raster de optie **Wave-gegevens** om de gemaakte zending-id's weer te geven. Sluit de pagina **Waves** wanneer u klaar bent.
1. Selecteer in de sectie **Ladingen** van de pagina **Workbench ladingplanning** de lading en selecteer vervolgens in het menu **Verwante informatie** boven het raster de optie **Werkgegevens** om het werk weer te geven dat voor de verkooporders is gemaakt.
1. Noteer de werk-id's die zijn aangemaakt. U moet mogelijk naar rechts schuiven om het verkoopordernummer en de zending-id te zien die aan de werk-id zijn gekoppeld.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>Stap 2: Stel de uitvoeringsstroom in voor mobiele apparaten

Bij taken op mobiele apparaten moet de gebruiker gegevens invoeren, zoals de werk-id of de nummerplaat-id. In de velden wordt deze informatie doorgaans verstrekt aan gebruikers in het magazijn in de vorm van streepjescodes die worden aangetroffen op documentatie, verpakking of rek. Als u de stappen voor het mobiele apparaat wilt uitvoeren voor scenario's, controleert u of u de werk-id's voor de transacties hebt geïdentificeerd en de nummerplaat-id's voor het artikel en de locatie in de transacties.

1. Meld u aan bij het mobiele apparaat met een gebruikers-id en wachtwoord voor magazijn *51*.
1. Selecteer **Uitgaand**.
1. Selecteer **Orderverzamelen**.
1. U kunt de werk-id of de nummerplaat-id invoeren. Voer de werk-id voor de eerste verkooporder in en selecteer vervolgens **Enter**.
1. Voer in het veld **Loc** de locatie in die wordt weergegeven om de orderverzamellocatie te bevestigen. Selecteer vervolgens **Enter**.
1. Voer in het veld **NP** de nummerplaat-id in. De nummerplaat-id moet overeenkomen met het artikel, het magazijn en de locatie van het artikel dat wordt verzameld van de geselecteerde locatie. Wanneer u klaar bent, selecteert u **Enter**.
1. Voer in het veld **Artikel** het artikelnummer in om het artikel dat wordt verzameld te bevestigen en selecteer **Enter**.
1. Voer in het veld **Hoeveelheid** de hoeveelheid in die wordt verzameld van het artikel en selecteer **Enter**.
1. Voer in het veld **Doel-NP** de id van de doelnummerplaat in. De doelnummerplaten zijn door de gebruiker gedefinieerde waarden. Zorg ervoor dat u een nummerplaat-id invoert die u kunt onthouden. Een aanbeveling is om een notatie te gebruiken met de huidige datum plus een volgnummer van twee cijfers (jjmmdd\#\#), bijvoorbeeld *19112301*. Wanneer u klaar bent, selecteert u **Enter**.
1. Bekijk de informatie die wordt weergegeven. Deze gegevens zijn de *verzamel* gegevens, die nu de *wegzet* gegevens voor de wegzettransactie worden. Wanneer u klaar bent, selecteert u **Enter**.

    - U ontvangt een melding **Werk voltooid**.

1. Herhaal de stappen 4 tot en met 10 voor de werk-id van de tweede verkooporder.

In de volgende stap worden de twee verzamelde nummerplaten in de vrachtwagen geladen.

1. Meld u aan bij het mobiele apparaat met een gebruikers-id en wachtwoord voor magazijn *51*.
1. Selecteer **Uitgaand**.
1. Selecteer **Verkoop laden**.
1. Voer de door de gebruiker gedefinieerde id van de doelnummerplaat in die u in de vorige procedure hebt gemaakt voor de eerste werk-id. Selecteer vervolgens **Enter** om de doelnummerplaat in de locatie **KLAARZETTEN** te plaatsen.
1. Geef de id van de doelnummerplaat opnieuw op en selecteer vervolgens **Enter** om de plaat op de locatie **LAADDEUR** te plaatsen.
1. Herhaal stap 4 tot en met 5 voor de id van de doelnummerplaat die u hebt gemaakt voor de tweede werk-id.

De twee werk-id's worden nu gesloten (geladen).

### <a name="step-3-confirm-the-outbound-shipment"></a>Stap 3: Bevestig de uitgaande zending

In deze stap bevestigt u de twee verkooporders en het werk dat is voltooid voor de lading om de verzamelde artikelen van de lading te verzenden en een nieuwe lading te maken voor de niet-verzamelde artikelen. Bevestiging van de uitgaande zending moet worden uitgevoerd op de pagina **Gegevens lading**.

1. Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.
1. Selecteer in de sectie **Ladingen** in het raster de rij voor de ladings-id die u hebt gemaakt.
1. Selecteer de koppeling van de ladings-id om de pagina **Gegevens lading** te openen.
1. Ga naar de pagina **Gegevens lading** en selecteer in het actievenster op het tabblad **Verzenden en ontvangen** in de groep **Bevestigen** de optie **Uitgaande zending** om de bevestiging te initiëren.
1. Selecteer in het dialoogvenster **Verzending bevestigen** in het veld **Ladingsplitsmethode tijdens bevestigen verzenden** de optie *Hoeveelheid splitsen voor nieuwe lading*.
1. Selecteer **OK**.

    Mogelijk krijgt u de melding "Bezig met verwerken" te zien.

    U ontvangt informatieve meldingen die aangeven dat de zending voor uw lading is bevestigd en dat een nieuwe lading is gemaakt op basis van de gesplitste hoeveelheid.

Vernieuw de pagina **Workbench ladingplanning** om de nieuwe lading weer te geven.

U kunt ook op de volgende manieren bevestigen dat transactierelaties zijn bijgewerkt:

- De resterende (niet-verwerkte) zending en zendingsregels worden bijgewerkt met de nieuwe ladings-id.
- De verkooporder wordt gekoppeld aan de nieuwe ladings-id.
- De oorspronkelijke lading bevat niet meer de resterende ladingsregels.
- Het resterende werk is bijgewerkt met de nieuwe ladings-id.
- De wave blijft hetzelfde.
- De status van de nieuwe lading wordt correct bijgewerkt. (Als de werkstatus _Onderhanden_ is, moet ook de ladingsstatus _Onderhanden_ worden.)

## <a name="notes-and-tips"></a>Opmerkingen en tips

- U kunt ook de parameter **Lading splitsen toestaan tijdens verzending bevestigen** inschakelen nadat de lading is gemaakt met de parameter **Ladingssjabloon** is uitgeschakeld maar voordat het ladingsproces is gestart. Ga naar de betreffende lading en schakel vervolgens in de koptekstweergave de parameter in.
- De optie **Hoeveelheid splitsen voor nieuwe lading** werkt ook wanneer enkele van de resterende werkkopteksten de status *Onderhanden* hebben. U kunt de functionaliteit dus nog steeds gebruiken als werknemers de verzamelingsorders uitvoeren.
- Als u **Niet-afgehandelde hoeveelheid annuleren** kiest terwijl er nog werk over is dat de status *Open* of *Onderhanden* heeft, wordt het volgende foutbericht weergegeven: "Kan resterende hoeveelheid voor lading niet annuleren. Er bestaat werk voor de lading."
- Als u **Niet-afgehandelde hoeveelheid annuleren** selecteert wanneer er geen resterend werk is, maar er niet-vrijgegeven ladingregels in de lading zijn, wordt het volgende foutbericht getoond: "Kan de zending voor de lading niet bevestigen, omdat de hoeveelheid voor het artikel het percentage overschrijdt dat is gedefinieerd voor minderlevering". Als u deze fout wilt voorkomen, kunt u het percentage voor **Minderlevering** op de niet-vrijgegeven ladingsregel instellen op 100 procent. Niet-vrijgegeven regels worden niet naar een nieuwe lading verplaatst, maar de huidige lading wordt bevestigd met minderlevering. In dat geval kunt u de oorspronkelijke order niet opnieuw vrijgeven. Daarom moet u dit dus op een andere manier afhandelen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]