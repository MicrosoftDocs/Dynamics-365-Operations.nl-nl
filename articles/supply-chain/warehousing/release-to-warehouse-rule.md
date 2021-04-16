---
title: Regel voor vrijgave naar magazijn
description: Dit onderwerp biedt informatie over de Functie Regel voor vrijgave naar magazijn, die flexibiliteit biedt tijdens de vrijgave naar het magazijn. Er wordt een configuratieoptie toegevoegd waarmee wordt bepaald of gedeeltelijk gereserveerde orderregels in het systeem mogen worden vrijgegeven.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 77714d6bda27d8d29b10177dd87e61839295e47e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823258"
---
# <a name="release-to-warehouse-rule"></a>Regel voor vrijgave naar magazijn

[!include [banner](../includes/banner.md)]

De functie *Regel voor vrijgave naar magazijn* biedt flexibiliteit tijdens de vrijgave naar het magazijn. Er wordt een configuratieoptie toegevoegd voor elk magazijn. U kunt met deze optie opgeven of gedeeltelijk gereserveerde orderregels voor dat magazijn kunnen worden vrijgegeven. De functie werkt samen met funtionaliteit voor geavanceerd cross-docking in situaties waarin een deel van een orderregelhoeveelheid is gemarkeerd voor een voorraadbron, maar het resterende deel kan worden verwerkt in het magazijn. Daarom kan de regel worden vrijgegeven, zodat de magazijnverwerking van de beschikbare voorraadhoeveelheid kan doorgaan.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>De functie Regel voor vrijgave naar magazijn inschakelen en initialiseren

### <a name="turn-on-the-feature"></a>De functie inschakelen

Voordat u de functie *Regel voor vrijgave naar magazijn* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Regel voor vrijgave naar magazijn*

### <a name="initialize-the-feature"></a>De functie initialiseren

Nadat de functie is ingeschakeld in uw systeem, moet u deze initialiseren om de regel in te stellen op de juiste beginstatus voor alle magazijnen.

- Bij magazijnen waarvoor magazijnbeheer niet is ingeschakeld, wordt de regel in eerste instantie ingesteld op **Niet van toepassing**.
- Bij magazijnen waarvoor magazijnbeheer wel is ingeschakeld, wordt de regel in eerste instantie ingesteld op **Gedeeltelijke reservering toestaan**.

Voer de volgende stappen uit om de functie te initialiseren en de regel voor vrijgave naar magazijn in te stellen voor alle magazijnen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Op de pagina **Parameters voor magazijnbeheer** op het tabblad **Algemeen** in de sectie **Bedrijfsgegevens** selecteert u de koppeling voor de regel **initialisatie van vrijgave naar magazijn**. (Als deze koppeling niet wordt weergegeven, is de functie niet ingeschakeld of is deze al geïnitialiseerd.)
1. Wanneer u wordt gevraagd de actie te bevestigen, selecteert u **Ja** om de functie te initialiseren.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>De regel voor vrijgave naar magazijn instellen voor elk magazijn

Nadat de functie is ingeschakeld en geïnitialiseerd, krijgen alle magazijnen een initiële instelling, zoals wordt beschreven in de vorige sectie. U kunt deze instelling voor afzonderlijke magazijnen wijzigen door de volgende stappen uit te voeren.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Magazijnen**.
1. Selecteer het magazijn dat u wilt configureren.
1. Selecteer de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. Op het sneltabblad **Magazijn** in de sectie **Reserveringen** wordt met het veld **Vereiste voor voorraadreservering** bepaald of gedeeltelijke vrijgave van orders is toegestaan. Selecteer een van de volgende waarden:

    - **Niet van toepassing**: Wanneer de functie voor het eerst wordt ingeschakeld en geïnitialiseerd, wordt deze waarde automatisch toegewezen aan alle magazijnen waarvoor magazijnbeheer niet is ingeschakeld. Deze waarde kan niet worden gewijzigd. Deze waarde is niet beschikbaar voor magazijnen waarvoor magazijnbeheer is ingeschakeld.
    - **Gedeeltelijke reservering toestaan**: Orders kunnen worden vrijgegeven wanneer een hoeveelheid gereserveerd is. Het wordt geëvalueerd of de niet-gereserveerde hoeveelheid moet worden gemarkeerd voor geavanceerd cross-docking en de betreffende hoeveelheid wordt gemarkeerd als vereist. Als er geen markering is, maakt het systeem alleen werk voor de gereserveerde hoeveelheid. Wanneer de functie voor het eerst wordt ingeschakeld en geïnitialiseerd, wordt deze waarde automatisch toegewezen aan alle magazijnen waarvoor magazijnbeheer is ingeschakeld. Deze waarde is niet beschikbaar voor magazijnen waarvoor magazijn beheerniet is ingeschakeld.
    - **Volledige reservering vereisen**: Orders kunnen alleen vrijgegeven worden als de gehele hoeveelheid gereserveerd is. Ze kunnen niet worden vrijgegeven als de totale hoeveelheid niet fysiek gereserveerd of gepland is voor cross-docken. Deze waarde is niet beschikbaar voor magazijnen waarvoor magazijn beheerniet is ingeschakeld.

1. Selecteer **Opslaan**.

## <a name="scenarios"></a>Scenario's

Deze sectie bespreekt twee scenario's waarmee u kunt leren wat de functie doet en hoe u deze gebruikt.

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u deze scenario's wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

U kunt deze scenario's ook gebruiken als instructie voor deze functie wanneer u met een productiesysteem werkt. In dat geval moet u echter uw eigen waarden vervangen en hebt u mogelijk niet de beschikking over bepaalde typen vereiste records die met de standaard demogegevens worden verstrekt.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>Scenario 1: Volledige vrijgave vereisen (geen gepland cross-docken)

In dit scenario ziet u hoe de functie werkt voor magazijnen die zijn ingesteld op **Volledige reservering vereist**.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Magazijnen**.
1. Voor magazijn _62_ stelt u het veld **Vereisten voor voorraadreservering** in op **Volledige reservering vereisen**, zoals wordt beschreven in de sectie [De regel voor vrijgave naar magazijn instellen voor elk magazijn](#set-option-warehouse) die eerder in dit onderwerp is beschreven.
1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** om een verkooporder te maken.
1. Stel in het dialoogvenster **Verkooporder maken** de volgende waarden in:

    - Stel op het sneltabblad **Klant** het veld **Klantaccount** in op _US-004_.
    - Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op _62_.

1. Selecteer **OK** om het dialoogvenster te sluiten en de nieuwe verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Deze bevat een lege regel in het raster in de sectie **Verkooporderregels**. Stel op deze regel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *2*

1. Selecteer **Regel toevoegen** om een nieuwe regel toe te voegen en stel de volgende waarden in:

    - **Artikelnummer:** *A0002*
    - **Hoeveelheid:** *2*

1. Selecteer de eerste orderregel en selecteer vervolgens in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Reserveer de tweede orderregel niet.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.
1. Het volgende foutbericht wordt weergegeven: "De volledige hoeveelheid moet fysiek worden gereserveerd." Daarom maakt het systeem geen werk, zending of lading voor de order.

    > [!NOTE]
    > Het foutbericht wordt weergegeven als u de tweede regel gedeeltelijk reserveert.

### <a name="scenario-2-allow-partial-release"></a>Scenario 2: Gedeeltelijke vrijgave toestaan

In dit scenario ziet u hoe de functie werkt voor magazijnen die zijn ingesteld op **Gedeeltelijke vrijgave toestaan**.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Magazijnen**.
1. Voor magazijn _62_ stelt u het veld **Vereisten voor voorraadreservering** in op **Gedeeltelijke reservering toestaan**, zoals wordt beschreven in de sectie [De regel voor vrijgave naar magazijn instellen voor elk magazijn](#set-option-warehouse) die eerder in dit onderwerp is beschreven.
1. Zoals u in het [vorige scenario](#scenario1) deed, gaat u naar **Verkoop- en marketing \> Verkooporders \> Alle verkooporders** en maakt u een verkooporder voor klantaccount _VS-004_ uit magazijn _62_. Voeg de volgende twee orderregels toe:

    - **Regel 1:** Stel op de nieuwe regel het veld **Artikelnummer** in op _A0001_ en het veld **Hoeveelheid** op _2_ en het veld **Eenheid** op _Stuks_.
    - **Regel 2:** Stel op de nieuwe regel het veld **Artikelnummer** in op _A0002_ en het veld **Hoeveelheid** op _2_ en het veld **Eenheid** op _Stuks_.

1. Zoals u in het [vorige scenario](#scenario1) hebt gedaan, moet u de volledige hoeveelheid reserveren voor order regel 1, maar orderregel 2 niet reserveren.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.
1. Merk op dat u deze keer geen foutmelding krijgt. In plaats daarvan maakt het systeem werk, zendingen en lading aan zoals vereist en worden de resultaten weergegeven.
1. U kunt de gegevens voor zending, lading en werk weergeven met de opties in het menu **Magazijn** boven het raster:

    - **Regel 1:** Er zijn drie opties beschikbaar: **Details van zending**, **Gegevens lading** en **Werkgegevens**. Selecteer elke optie om de details weer te geven van de zending, de lading en het werk die zijn gemaakt toen de order werd vrijgegeven naar het magazijn.
    - **Regel 2:** Alleen de optie **Werkgegevens** is beschikbaar. Selecteer de optie en merk op dat er geen werk is gemaakt omdat er geen voorraad is gereserveerd. Daarom is er ook geen zending of lading gemaakt.

> [!NOTE]
> Hetzelfde resultaat wordt verwacht wanneer de tweede regel gedeeltelijk is gereserveerd. In dit geval wordt werk gemaakt voor de gereserveerde regelhoeveelheid, maar niet voor de niet-gereserveerde hoeveelheid.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]