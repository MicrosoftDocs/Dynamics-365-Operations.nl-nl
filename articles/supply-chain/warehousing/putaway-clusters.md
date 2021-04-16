---
title: Wegzetclusters
description: Wegzetclusters bieden u de mogelijkheid om meerdere nummerplaten tegelijk te verzamelen en ze vervolgens mee te nemen om op verschillende locaties weg te zetten. Dit kan zeer nuttig zijn voor handelsbedrijven, waarbij de nummerplaten doorgaans geen volledige pallets met voorraad zijn.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b3a7d1b7109b83b26c8187a7f0d271f1c82f6d63
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840360"
---
# <a name="putaway-clusters"></a>Wegzetclusters

[!include [banner](../includes/banner.md)]

Wegzetclusters bieden u de mogelijkheid om meerdere nummerplaten tegelijk te verzamelen en ze vervolgens mee te nemen om op verschillende locaties weg te zetten. Naar dit proces wordt vaak verwezen als een *milk run*. Wegzetclusters kunnen zeer nuttig zijn voor handelsbedrijven, waarbij de nummerplaten doorgaans geen volledige pallets met voorraad zijn. 

## <a name="turn-on-the-cluster-putaway-feature"></a>De functie Cluster wegzetten inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functie naam:** *functie Cluster wegzetten*

## <a name="setup-for-the-example-scenario"></a>Instellingen voor het voorbeeldscenario

### <a name="cluster-profiles"></a>Clusterprofielen

Het wegzetclusterprofiel bepaalt waar een artikel naartoe gaat, op basis van de locatie die aan het artikel is toegewezen op het moment van ontvangst. Als verschillende wegzetclusters vereist zijn, moet voor elke menuoptie van het mobiele apparaat een ander wegzetcluster worden gemaakt.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Clusterprofielen**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de weergave **Koptekst** de volgende waarden in:

    - **Profiel-id van wegzetcluster:** *Cluster wegzetten*
    - **Naam profiel-id van wegzetcluster:** *Cluster wegzetten*
    - **Clustertype:** *Wegzetten*
    - **Volgnummer:** Accepteer de standaard waarde.

1. Selecteer **Opslaan** om de vereiste velden op het sneltabblad **Algemeen** beschikbaar te maken.
1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Toewijzingsmoment van cluster:** *bij ontvangst*

        Dit veld bepaalt of het wegzetcluster direct moet worden toegewezen wanneer de voorraad wordt ontvangen, of dat het later moet worden gesorteerd.

    - **Clustertoewijzingsregel:** *handmatig*

        Dit veld bepaald of de clustertoewijzing automatisch door het systeem moet worden bepaald, of handmatig door de gebruiker.

    - **Instructiecode:** Laat dit veld leeg.
    - **Wegzetcluster locatie:** *Bij ontvangst*

        De volgende waarden zijn beschikbaar:

        - **Bij ontvangst**: een locatie wordt direct gevonden tijdens ontvangst.
        - **Clusterafsluiting**: een locatie wordt gevonden wanneer het cluster wordt gesloten.
        - **Door gebruiker**: een locatie wordt gevonden wanneer de nummerplaat van het cluster wordt verzameld voor wegzetten. In dit geval wordt geen locatie opgegeven wanneer het wegzetwerk wordt gemaakt. Tijdens het wegzetten moet de gebruiker de nummerplaat of de werk-id scannen om de plaatsingsstap te initiëren. Het systeem zoekt vervolgens opnieuw de plaatsingslocatie en vertelt de gebruiker waar de verzamelde hoeveelheid moet worden geplaatst.

    - **Wegzetcluster per gebruiker:** *Nee*

        In dit veld definieert of elk cluster uniek moet zijn per gebruiker wanneer clusters automatisch worden toegewezen. Deze optie is alleen beschikbaar als het veld **Clustertoewijzingsregel** is ingesteld op *Automatisch*.

    - **Eenheidsbeperking:** laat dit veld leeg.

        In dit veld wordt de eenheid gedefinieerd die moet worden ontvangen voor een geldig profiel. Als dit veld leeg wordt gelaten, zijn alle eenheden geldig.

    - **Werkeenheid opbreken:** *individueel*

        In dit veld wordt gedefinieerd of alle voorraad moet worden geconsolideerd (met behulp van de cluster-id en de nummerplaat) op één nummerplaat wanneer een cluster wordt afgesloten en of het moet worden opgeslagen als een enkele nummerplaat of afzonderlijk op de ontvangen nummerplaten. Dit veld is niet beschikbaar als het veld **Wegzetcluster locatie** is ingesteld op *Bij ontvangst*.

    - **Cluster blijft als bovenliggende nummerplaat:** *Nee*

        Als deze optie is ingesteld op *Ja* en de plaatsingsstap is voltooid, wordt de cluster-id een bovenliggende nummerplaat en worden alle artikelen op de cluster-id aan die bovenliggende nummerplaat gekoppeld.

1. Op het sneltabblad **Clustersortering** kunt u sorteercriteria voor wegzetten definiëren. Selecteer **Nieuw** op de werkbalk om een tweede regel toe te voegen en stel de volgende waarden in:

    - **Volgnummer:** Accepteer de standaard waarde.
    - **Veldnaam:** *WMSLocationId*

        In dit veld wordt het veld gedefinieerd dat door deze regel als een sorteercriterium moet worden gebruikt.

    - **Sorteren:** *Oplopend*

        Met dit veld bepaalt u of de sortering in oplopende of aflopende volgorde wordt uitgevoerd.

1. Selecteer in het sneltabblad **Werksjabloon voor cluster** **Nieuw** op de werkbalk om een regel toe te voegen en stel de volgende waarden in:

    - **Werkordertype:** *Inkooporders*
    - **Werksjabloon:** *61 PO direct*

1. Selecteer in het actievenster **Opslaan** en vervolgens **Query bewerken**.
1. Selecteer in het dialoogvenster **Cluster wegzetten** op het tabblad **Bereik** de optie **Toevoegen** om een tweede regel aan de query toe te voegen. Werk vervolgens de queryregels bij, zoals wordt weergegeven in de volgende tabel.

    | Tabel | Afgeleide tabel | Veld | Criteria |
    |---|---|---|---|
    | Werk | Werk | Magazijn | *61* |
    | Werk | Werk | Werk-id | Laat dit veld leeg. |

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Selecteer **Opslaan** in het actievenster en sluit de pagina.

> [!IMPORTANT]
> Velden in het clusterprofiel die grijs worden weergegeven wanneer **Cluster-id genereren** is ingesteld op *Ja*, zijn niet beschikbaar en worden niet meegenomen als deze functie wordt gebruikt.

### <a name="mobile-device-menu-items"></a>Menuopties voor mobiel apparaat

Voor deze functie zijn twee nieuwe menuopties voor mobiele apparaten beschikbaar. De menuoptie **Cluster ontvangen en sorteren** wordt gebruikt om de ontvangen voorraad bij ontvangst te sorteren in een wegzetcluster. De menuoptie **Cluster wegzetten** wordt gebruikt om het cluster na toewijzing te plaatsen.

#### <a name="receive-and-sort-cluster"></a>Cluster ontvangen en sorteren

Maak een nieuw menuoptie voor een mobiel apparaat voor het ontvangen van voorraad en het sorteren in een cluster. Met deze menuoptie wordt inkomend werk gemaakt nadat de voorraad is ontvangen, waarmee wordt aangegeven dat de ontvangende menuoptie wordt gebruikt voor wegzetclusters.

> [!NOTE]
> De menuoptie **Cluster ontvangen en sorteren** kan worden gebruikt met de volgende ontvangende menuopties:
>
> - Ontvangen van inkooporderregel
> - Ontvangen van inkooporderartikel
> - Artikelontvangst laden

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de weergave **Koptekst** de volgende waarden in:

    - **Naam van menuoptie:** *Cluster ontvangen en sorteren*
    - **Titel:** *Cluster ontvangen en sorteren*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Nee*

1. Stel op het sneltabblad **Algemeen** de volgende waarden in:

    - **Werkcreatieproces:** *Inkooporderartikelen ontvangen*
    - **Nummerplaat maken:** *Ja*
    - **Wegzetcluster toewijzen:** *Ja*

        > [!NOTE]
        > De optie **Wegzetcluster toewijzen** is alleen beschikbaar voor de enkele activiteit *Werkcreatieproces* voor ontvangst.

    Accepteer de standaardwaarden voor de overige velden.

1. Selecteer **Opslaan** in het actievenster.

#### <a name="cluster-putaway"></a>Clusteropslag

Maak een nieuwe menuoptie voor mobiele apparaten om het cluster na toewijzing te plaatsen.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in de weergave **Koptekst** de volgende waarden in:

    - **Naam menuoptie:** *Cluster wegzetten*
    - **Titel:** *Cluster wegzetten*
    - **Modus:** *werk*
    - **Bestaand werk gebruiken:** *Ja*

1. Stel op het sneltabblad **Algemeen** het veld **Bestuurd door** in op *Cluster wegzetten*. Accepteer de standaardwaarden voor de overige velden.
1. Stel op het sneltabblad **Werkklassen** de geldige werkklasse in voor deze menuoptie voor een mobiel apparaat:

    - **Werkklasse-id:** *Aankoop*
    - **Werkordertype:** *Inkooporders*

1. Selecteer **Opslaan** in het actievenster.

### <a name="mobile-device-menu"></a>Menu voor mobiel apparaat

Voeg de menuopties die u zojuist hebt gemaakt toe aan het inkomende menu van de mobiele app.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer **Inkomend** in de menulijst.
1. Zoek en selecteer in de lijst **Beschikbare menu's en menuopties** de optie **Cluster ontvangen en sorteren**.
1. Selecteer de knop pijl-rechts om de geselecteerde menuoptie te verplaatsen naar de lijst **Menustructuur**.
1. Gebruik de knop pijl-omhoog of pijl-omlaag om de menuoptie naar de gewenste positie in het menu te verplaatsen.
1. Selecteer **Opslaan** in het actievenster.
1. Herhaal stap 4 tot en met 7 om de resterende menuopties toe te voegen:

    - Cluster toewijzen
    - Clusteropslag

## <a name="example-scenario"></a>Voorbeeldscenario

Dit scenario simuleert het verwerken van wegzetclusters.

### <a name="create-a-purchase-order"></a>Inkooporder maken

1. Ga naar **Leveranciers \> Inkooporders \> Alle inkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Inkooporder maken** de volgende waarden in:

    - **Leverancieraccount:** *1001*
    - **Magazijn:** *61*

1. Selecteer **OK**.

    De pagina **Alle inkooporders** wordt weergegeven.

1. Op de pagina **Alle inkooporders** in het sneltabblad **Inkooporderregels**, gebruikt u de knop **Regel toevoegen** om de volgende regels toe te voegen:

    - Inkooporderregel 1:

        - **Artikelnummer:** *A0001*
        - **Hoeveelheid:** *10*

    - Inkooporderregel 2:

        - **Artikelnummer:** *A0002*
        - **Hoeveelheid:** *20*

    - Inkooporderregel 3:

        - **Artikelnummer:** *M9215*
        - **Hoeveelheid:** *30*

1. Selecteer **Opslaan** in het actievenster.
1. Noteer het nummer van de inkooporder.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Voorraad ontvangen en wegzetten vanaf het mobiele apparaat

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>De voorraad ontvangen en in een cluster sorteren

1. Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker die is ingesteld voor magazijn *61*.
1. Selecteer **Inkomend** in het hoofdmenu.
1. Selecteer in het menu **Inkomend** de optie **Cluster ontvangen en sorteren**.
1. Voer in het veld **Inkoopordernummer** het inkoopordernummer in.
1. Selecteer **OK** (vinkjesknop).
1. Selecteer het veld **Artikel**, voer het artikelnummer *A0001* in en selecteer **OK**.
1. Selecteer het veld **Hoeveelheid**, voer *10* in met behulp van het numerieke blok en selecteer vervolgens de vinkjesknop.
1. Op de taakpagina **Hoeveelheid** selecteert u **OK** (vinkjesknop) om de ingevoerde hoeveelheid te bevestigen.
1. Op de taakpagina **Artikel** selecteert u **OK** om te bevestigen dat artikel *A0001* is ingevoerd.
1. Selecteer het veld **Cluster-id** en voer een waarde in om een id toe te wijzen aan het cluster dat u wilt maken.

    De id die u hier invoert, wordt gebruikt wanneer de twee resterende artikelen op de inkooporder worden ontvangen.

1. Selecteer **OK**.

    De taakpagina **Inkoopordernummer** wordt weergegeven en toont een bericht dat het werk is voltooid.

    Artikel *A0001* is nu ontvangen op de locatie *RECV* en is toegewezen aan de cluster-id die u in stap 10 hebt ingevoerd.

1. Herhaal stap 4 tot en met 11 om de overige twee artikelen van de inkooporder te ontvangen en toe te wijzen aan de cluster-id:

    - Een hoeveelheid van *20* voor artikel *A0002*
    - Een hoeveelheid van *30* voor artikel *M9215*

#### <a name="close-the-cluster"></a>Het cluster afsluiten

Voordat de artikelen in het cluster kunnen worden weggezet, moet het cluster worden gesloten.

1. Ga in Supply Chain Management naar **Magazijnbeheer \> Werk \> Uitgaand \> Werkclusters**.
1. Op de pagina **Werkclusters**, in de sectie **Werkcluster** zoekt u in het veld **Cluster-id** naar de cluster-id die u eerder hebt ingevoerd.
1. Als het cluster niet wordt weergegeven, is het mogelijk al gesloten. Om te bepalen of het cluster is gesloten, schakelt u het selectievakje **Gesloten werk weergeven** in en zoekt u naar de cluster-id die u eerder hebt ingevoerd. Voer vervolgens een van deze stappen uit:

    - Als het cluster is gesloten, slaat u de resterende stappen van deze procedure over en gaat u door met de volgende procedure, [Het cluster wegzetten](#put-the-cluster-away).
    - Als het cluster niet is gesloten, voert u de resterende stappen van deze procedure uit om het cluster handmatig te sluiten. Ga vervolgens door met de volgende procedure.

1. Selecteer in de sectie **Werkcluster** de cluster-id die u eerder hebt ingevoerd.
1. Selecteer **Cluster sluiten** in het actievenster.

    Nadat het cluster is afgesloten, wordt het niet meer weergegeven in de sectie **Werkcluster** (tenzij het selectievakje **Gesloten werk weergeven** is ingeschakeld).

#### <a name="put-the-cluster-away"></a>Het cluster wegzetten

1. Meld u aan bij de mobiele app Magazijnbeheer als een gebruiker die is ingesteld voor magazijn *61*.
1. Selecteer **Inkomend** in het hoofdmenu.
1. Selecteer in het menu **Inkomend** de optie **Cluster wegzetten**.
1. Selecteer **Cluster-id** en voer de cluster-id in die u eerder voor het gesloten cluster hebt ingevoerd.
1. Selecteer **OK**.

    De pagina **Cluster wegzetten: verzamelen** wordt weergegeven. Het bevat de cluster-ID, de orderverzamellocatie, de artikelen (de waarde *Meerdere* wordt weergegeven) en de totale hoeveelheid in het cluster dat moet worden verzameld.

1. Selecteer **OK**.

    De pagina **Cluster wegzetten: plaatsen** wordt weergegeven. De instructies **Plaatsen** identificeren de cluster-id, de plaatsingslocatie, de artikelen, de totale hoeveelheid en de nummerplaat-id's voor de artikelen die op het cluster zijn ontvangen.

    U hebt de standaardopties om deze stap te overschrijven of te negeren.

    ![De pagina Cluster wegzetten: plaatsen](media/Cluster_putaway-Put.png "De pagina Cluster wegzetten: plaatsen")

1. Selecteer **OK** om het wegzetten van het cluster te bevestigen.

    Het bericht Cluster voltooid wordt weergegeven.

## <a name="notes-and-tips"></a>Opmerkingen en tips

Als de cluster-id de bovenliggende nummerplaat voor een genest pallet wordt, wordt de plaatsingspositie automatisch gegeven wanneer de cluster-id wordt gescand. Er moet geen verdere nummerplaat worden gescand, zelfs als het genereren van nummerplaten is ingesteld op handmatig.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]