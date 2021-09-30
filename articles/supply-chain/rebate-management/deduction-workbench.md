---
title: Inhoudingen beheren met de inhoudingsworkbench
description: In dit onderwerp wordt beschreven hoe u de inhoudingsworkbench gebruikt waarin u de klantbetalingen kunt verwerken die inhoudingen bevatten.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: bf98529176fbed368708ea925f542a70f2936037
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500397"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Inhoudingen beheren met de inhoudingsworkbench

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de inhoudingsworkbench gebruikt waarin u de klantbetalingen kunt verwerken die inhoudingen bevatten.

Een klant die een korting is verschuldigd, kan ervoor kiezen niet op de korting te wachten. In plaats daarvan kan de klant een betaling doen die een inhouding bevat voor het bedrag van de korting. Om dit type transactie te verwerken, kunt u de inhoudingsworkbench gebruiken om inhoudingen af te stemmen op open credittransacties, gesplitste inhoudingen, geweigerde inhoudingen en afschrijvingsinhoudingen.

> [!NOTE]
> De inhoudingswerkbank is lange tijd onderdeel van de verkoop- en marketingfunctie in Microsoft Dynamics 365 Supply Chain Management geweest. De module is nu echter verbeterd, zodat het ook werkt met de nieuwere **module** Kortingsbeheer. In dit onderwerp wordt beschreven hoe u zowel oudere functies als kortingsbeheerfuncties van de inhoudingsworkbench gebruikt. Als u [de module **Kortingsbeheer** echter niet hebt ingeschakeld voor het systeem](rebate-management-enable.md), is een aantal van de functionaliteit die hier wordt beschreven, niet beschikbaar.

## <a name="prerequisites"></a>Vereisten

### <a name="set-up-the-old-deduction-management-system"></a>Het oude inhoudingsbeheersysteem instellen

U kunt de inhoudingsworkbench samen met de oude inhoudingsbeheermogelijkheden van Supply Chain Management gebruiken, zelfs als u de module **Kortingsbeheer** niet gebruikt. U moet het systeem echter eerst voorbereiden zoals in deze sectie wordt beschreven.

Voordat u de inhoudingsworkbench kunt gebruiken, moet u de insteltaken voltooien die zijn beschreven in [Inhoudingsbeheer instellen](/dynamicsax-2012/appuser-itpro/set-up-deduction-management). U moet ook een type kortingsovereenkomst instellen voor de klant; een klantkorting zoals beschreven in [Klantkortingen instellen en beheren](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates) of een korting op de handelstoeslag.

Als u een korting op een klant aftrekt, moet u de volgende taken uitvoeren:

- [Klantkortingen instellen](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- De korting goedkeuren en verwerken, zodat u de inhoudingsworkbench kunt gebruiken.

Als u een korting toepast op een handelstoeslag, moet u de volgende taken uitvoeren:

- Terugbetalingskortingen instellen.
- Terugbetalingskortingen toepassen.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Klanten en inhoudingen configureren

Alle inhoudingsgebeurtenissen worden in een claimjournaal registreert. Daarom moet uw systeem een journaal bevatten dat hiervoor kan worden gebruikt. Als u nog geen claimjournaal hebt, stelt u dit nu in. Dit journaal is vereist om inhoudingen rechtstreeks te maken op de inhoudingsworkbench, klantvereffening of klantpagina.

Volg de onderstaande stappen om een nieuw claimjournaal voor inhoudingen in te stellen.

1. Ga naar **Grootboek \> Journaalinstellingen \> Journaalnamen**.
1. Selecteer **Nieuw** en stel de volgende velden in voor de nieuwe journaalnaam:

    - **Naam** – Een unieke naam voor het claimjournaal invoeren.
    - **Omschrijving** – Een korte omschrijving van het nieuwe journaal invoeren.
    - **Journaltype** – Selecteer *Dagelijks*.
    - **boekstuknummering**– Een bestaande nummerreeks toewijzen. U kunt ook een nieuwe nummerreeks met een bedrijfsbereik maken en deze toewijzen aan de nieuwe journaalnaam.

1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
1. Stel op het tabblad **Inhoudingen** op het sneltabblad **Algemeen** het veld **Claimjournaalnaam** in op de journaalnaam die u zojuist hebt gemaakt.
1. Stel op het sneltabblad **Retourorder** de volgende velden in:

    - **Retourorder maken** – Stel deze optie in om op te geven wat het systeem moet doen als een claim op basis van hoeveelheden wordt goedgekeurd:

        - *Ja* – Maak een retourorder.
        - *Nee* – Maak een negatieve verkooporder.

    - **Maken zonder gekoppelde factuur** – Selecteer een waarde om op te geven wat het systeem moet doen als een claim op basis van hoeveelheden wordt goedgekeurd maar er geen factuur is gekoppeld:

        - *Accepteren* – Maak een retourorder.
        - *Waarschuwing* – Een retourorder maken, maar het volgende waarschuwingsbericht tonen: 'Claim is niet aan een factuur gekoppeld'.
        - *Fout* – Maak geen retourorder maar toon het volgende waarschuwingsbericht: 'Claim is niet aan een factuur gekoppeld'. Update is geannuleerd."

    - **Retourorder maken vóór inhoudingsgoedkeuring** – Stel deze optie in op *Ja* als retourorders kunnen worden gemaakt voordat de claim wordt goedgekeurd. Deze instelling is alleen van toepassing op claims op basis van hoeveelheden waarbij de optie **Retourorder** maken is ingesteld op *Ja*.

### <a name="configure-general-ledger-parameters"></a>Parameters voor grootboek configureren

Wanneer er een claimjournaal wordt gemaakt voor een nieuwe inhouding, worden er twee nieuwe klanttransacties gemaakt: een om het bedrag van de claim op de oorspronkelijke factuur te compenseren en één om het schuldbedrag van een klant te registreren op het bedrag van de claim (omdat de claim nog niet is goedgekeurd). Daarom moet u het systeem zo instellen dat één boekstuk meerdere klantregels kan hebben.

Als u wilt dat één boekstuk meerdere klantregels heeft, gaat u als volgt te werk.

1. Ga naar **Grootboek \> Grootboek instellen \> Grootboekparameters**.
1. Stel op het tabblad **Grootboek** op het sneltabblad **Algemeen** de optie **Meerdere transacties binnen één boekstukoptie toestaan** in op *Ja*.
1. Als u een waarschuwingsbericht ontvangt, selecteert u **Sluiten** om de wijziging te accepteren.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Redenen voor inhouding maken

Het systeem vereist dat gebruikers een reden opgeven voor elke inhouding die ze rechtstreeks invoeren op de inhoudingsworkbench, klantafhandeling of klantpagina. De reden bepaalt hoe de inhouding wordt verwerkt wanneer deze wordt goedgekeurd.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Redenen voor inhoudingen**.
1. Selecteer **Nieuw** om een rij toe te voegen aan het raster en stel de volgende velden in:

    - **Claimreden** – Een unieke naam voor de reden invoeren.
    - **Beschrijving** – voer een beschrijving van de reden in om meer informatie te geven over hoe deze moet worden gebruikt.
    - **Claimbasis**– Selecteer een claimbasis voor de claimreden:

        - *Prijs gebaseerd* – Een vrije-tekstkrediet maken bij goedkeuring.
        - *Hoeveelheid gebaseerd* – Een negatieve verkooporder of retourorder maken bij goedkeuring.

    - **Retourredencode** – Selecteer een retourredencode die u wilt toepassen als de waarde **Retourredencode** voor de retourorder.
    - **Type** – Selecteer een vooraf inhoudingstype: De waarde **Inhoudingscompensatie** voor het geselecteerde type wordt gebruikt om het veld **Inhoudingscompensatie** in te stellen wanneer er een inhouding of claim wordt gemaakt. Typen inhouding worden gedefinieerd op de pagina **Inhoudingstypen** (**Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingstypen**).
    - **Boekingsrekening claimen** – Dit veld is alleen beschikbaar als het veld **Claimbasis** is ingesteld op *Prijs gebaseerd*. Wanneer een claim op basis van prijzen wordt goedgekeurd, wordt de grootboekrekening toegewezen die u hier selecteert als de **Hoofdrekening** waarde voor de conceptvrije-tekst voor de creditnota.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>De periodieke taak voor vereffening goedgekeurde inhoudingen instellen

Voor inhoudingen die worden gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantaftrek of klantpagina, kunt u de periodieke taak *Goedgekeurde inhoudingen vereffenen* instellen om automatisch inhoudingen en creditbedragen met overeenkomende **Inhoudings-ID** waarden en bedragen te matchen.

Als u deze taak wilt plannen, gaat u naar **Verkoopmarketing \> Periodieke taken \> Goedgekeurde inhoudingen vereffenen** en stelt u opties, filters en een planning in, net als voor andere typen periodieke taken.

> [!NOTE]
> Als de optie voor **Automatische vereffening** is ingesteld op *Ja* op het tabblad **Vereffening** van de pagina **Parameters van module Klanten** (**Klanten \> Instellen \> Parameters voor module Klanten**), doet de periodieke taak *Goedgekeurde inhoudingen* vereffenen niets, omdat het krediet automatisch wordt vereffend.

## <a name="create-a-deduction"></a>Een inhouding maken

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Een journaalboeking voor inhoudingen maken met behulp van het klantbetalingsjournaal

Volg deze stappen om een inhoudingsjournaalboeking te maken.

1. Ga naar **Klanten \> Betalingen \> Journaal met betalingen van klant**.
1. Selecteer **Nieuw** om een rij toe te voegen aan het raster.
1. Selecteer de naam van het journaal in het veld **Naam** voor de nieuwe rij.
1. Selecteer **Regels** in het actievenster.
1. Voer de datum, de bedrijfsrekening, en het klantrekeningnummer in.
1. Selecteer in het veld **Factuur** de factuur waar de inhouding aan is gekoppeld.
1. Voer in het veld **Krediet** het bedrag in dat de klant heeft betaald.
1. Selecteer **OK** om te bevestigen dat het bedrag kleiner is dan het totaal van de gemarkeerde transactie.
1. Selecteer het tegenrekeningtype en de tegenrekening.
1. Selecteer **Inhoudingen** op de werkbalk boven het raster.
1. Selecteer op de pagina **Inhouding** in het actievenster de optie **Nieuw** om een rij aan het raster toe te voegen. Het veld **Inhouding-ID** voor de nieuwe rij wordt automatisch ingesteld.
1. Selecteer in het veld **Type** het inhoudingstype.
1. Voer in het veld **Bedrag** het bedrag in dat wordt weergegeven in het veld **Saldo** onder de inhoudingslijst. Dit bedrag is het bedrag dat de klant van de betaling aftrok.
1. Sluit de pagina **Inhouding**. U bent weer terug op de pagina **Klantbetalingen**, die nu een nieuwe regel voor de inhouding laat zien.
1. Selecteer **Valideren \> Valideren in het actievenster**. U moet het volgende bericht ontvangen: "journaal is OK."
1. Selecteer **Boeken** in het actievenster.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Inhoudingen maken met de inhoudingsworkbench

Volg de onderstaande stappen om een inhouding te maken in de inhoudingsworkbench.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer in het actievenster **Onderhouden \> Nieuwe inhouding**.

    In het dialoogvenster **Nieuwe inhouding** wordt het veld **Inhoudings-ID** ingesteld op basis van de nummerreeks voor de **Inhoudings-ID** die is gedefinieerd op de pagina **Beheerparameters voor handelstoeslag** (**Verkoop en marketing \> Instellen \> Handelstoeslagen \> Beheerparameters voor handelstoeslag**)

1. Stel de volgende velden in:

    - **Klantrekening** – Selecteer de klantrekening waarop de inhouding van toepassing is.
    - **Extern claimnummer** – Voer de claimverwijzing van de klant in.
    - **Claimbedrag** – Voer het bedrag van de claim inclusief btw in. De waarde moet positief zijn.
    - **Valuta**– Selecteer de valuta voor de inhouding. De standaardwaarde is de valuta die is ingesteld voor de geselecteerde klantrekening.
    - **Claimbasis** – Selecteer de basis van de claim. Op basis van de claim wordt het type credittransactie bepaald dat wordt gemaakt nadat de inhouding of claim is goedgekeurd.

        - *Prijs gebaseerd* – Er wordt een concept vrije-tekstfactuur gemaakt.
        - *Hoeveelheid gebaseerd* – Een negatieve verkooporder of retourorder wordt gemaakt.

    - **Claimdatum** – Selecteer de datum van de claim. De standaardwaarde is de huidige datum.
    - **Claimreden** – Selecteer de redencode die van toepassing is op de huidige inhouding. De door u geselecteerde claimbasis heeft invloed op de opties die van toepassing zijn. Zie de sectie [Redenen voor inhouding maken](#deduction-reasons) eerder in dit onderwerp voor meer informatie over het maken en configureren van de claimredenen die hier voor selectie beschikbaar zijn.
    - **Opmerkingen** – Opmerkingen toevoegen die van toepassing zijn. Wanneer de claim is goedgekeurd, kan de fiattur de opmerkingen van de claim bewerken of toevoegen.
    - **Claimjournaal maken** – Stel deze optie in om op te geven of het claimjournaal moet worden gemaakt wanneer de claim of inhouding wordt gemaakt:

        - *Ja* – Er wordt een algemeen journaal gemaakt en geboekt via het claimjournaal dat is ingesteld op de **Parameters van module Klanten**. (Zie voor meer informatie de sectie [Klanten en inhoudingen configureren](#accounts-receivable-deductions) eerder in dit onderwerp.) Wanneer er een factuur aan de claim is gekoppeld, wordt het claimjournaal gebruikt om het saldo van de toepasselijke factuur te verminderen. Als de claim later wordt afgewezen, worden het claimjournaal en de vereffeningen (als er een factuur was gekoppeld) teruggeboekt.
        - *Nee*– Er wordt op dit moment geen claimjournaal gemaakt. Deze wordt gemaakt wanneer de claim wordt goedgekeurd. Er kan nog steeds een factuur aan de nieuwe claim worden gekoppeld, ook als er geen claimjournaaljournaal is gemaakt. Vereffening kan echter niet zonder het claimjournaal worden uitgevoerd.

1. Selecteer **OK**.

    Er wordt een nieuwe inhouding gemaakt. Als u de optie **Claimjournaal maken** in stelt op *Ja*, worden de volgende transacties geboekt:

    - **Twee nieuwe klanttransacties** – Eén transactie compenseert het bedrag van de claim op de oorspronkelijke factuur. Met de andere transactie wordt de schuld van een klant op het bedrag van de claim geregistreerd, omdat de claim nog niet is goedgekeurd. De oorspronkelijke factuurtransactie en de tegenrekeningsclaimstransactie worden automatisch gemarkeerd voor vereffening wanneer u de factuur koppelt door **Onderhouden \> Factuur koppelen** te selecteren in het actievenster.
    - **Twee tegenrekeningstransacties** – Deze transacties worden geboekt naar de **Inhoudingstegenrekening** in het grootboek.
    - **Claimjournaal** – Als u het claimjournaal wilt weergeven voor elke inhouding die wordt vermeld op de inhoudingsworkbench, selecteert u het tabblad **Verwijzingen**. Het claimjournaal wordt weergegeven in het veld **Journaalbatchnummer**. U kunt ook het claimjournaal bekijken op het tabblad **Inhoudingsgebeurtenissen**. Hier heeft het een **Bijwerkingstype** waarde van *Vereffen*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Een inhouding maken van een klantvereffening

Het proces waarbij een inhouding wordt gemaakt van een vereffening voor klanten lijkt op het proces waarbij een inhouding wordt gemaakt via de inhoudingsworkbench. De klant en de factuurvaluta worden echter automatisch ingesteld en de factuur wordt gekoppeld. U hoeft **Onderhouden \> Factuur koppelen** niet te selecteren in het actievenster wanneer u een claim of inhouding maakt via de klantvereffeningspagina.

1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Selecteer de klant waarvoor u een inhouding wilt maken.
1. Selecteer in het actievenster op het tabblad **Incasso** in de groep **Vereffenen** de optie **Transacties vereffenen**.
1. Selecteer in het dialoogvenster **Transacties instellen** op het tabblad **Overzicht** de factuur voor het maken van de inhouding.
1. Selecteer **Inhoudingen \> Nieuwe inhouding** op de werkbalk.

    In het dialoogvenster **Nieuwe inhouding** wordt het veld **Inhoudings-ID** ingesteld op basis van de nummerreeks voor de **Inhoudings-ID** die is gedefinieerd op de pagina **Beheerparameters voor handelstoeslag** (**Verkoop en marketing \> Instellen \> Handelstoeslagen \> Beheerparameters voor handelstoeslag**) Het veld **Klantrekening** is ingesteld op de klantrekening waarop de inhouding van toepassing is.

1. Stel de volgende velden in:

    - **Extern claimnummer** – Voer de claimverwijzing van de klant in.
    - **Claimbedrag** – Voer het bedrag van de claim inclusief btw in. De waarde moet positief zijn.
    - **Valuta**– Selecteer de valuta voor de inhouding. De standaardwaarde is de valuta die is ingesteld voor de geselecteerde klantrekening.
    - **Claimbasis** – Selecteer de basis van de claim. Op basis van de claim wordt het type credittransactie bepaald dat wordt gemaakt nadat de inhouding of claim is goedgekeurd.

        - *Prijs gebaseerd* – Er wordt een concept vrije-tekstfactuur gemaakt.
        - *Hoeveelheid gebaseerd* – Een negatieve verkooporder of retourorder wordt gemaakt.

    - **Claimdatum** – Selecteer de datum van de claim. De standaardwaarde is de huidige datum.
    - **Claimreden** – Selecteer de redencode die van toepassing is op de huidige inhouding. De door u geselecteerde claimbasis heeft invloed op de opties die van toepassing zijn. Zie de sectie [Redenen voor inhouding maken](#deduction-reasons) eerder in dit onderwerp voor meer informatie over het maken en configureren van de claimredenen die hier voor selectie beschikbaar zijn.
    - **Opmerkingen** – Opmerkingen toevoegen die van toepassing zijn. Wanneer de claim is goedgekeurd, kan de fiattur de opmerkingen van de claim bewerken of toevoegen.
    - **Claimjournaal maken** – Stel deze optie in om op te geven of het claimjournaal moet worden gemaakt wanneer de claim of inhouding wordt gemaakt:

        - *Ja* – Er wordt een algemeen journaal gemaakt en geboekt via het claimjournaal dat is ingesteld op de **Parameters van module Klanten**. (Zie voor meer informatie de sectie [Klanten en inhoudingen configureren](#accounts-receivable-deductions) eerder in dit onderwerp.) Wanneer er een factuur aan de claim is gekoppeld, wordt het claimjournaal gebruikt om het saldo van de toepasselijke factuur te verminderen. Als de claim later wordt afgewezen, worden het claimjournaal en de vereffeningen (als er een factuur was gekoppeld) teruggeboekt.
        - *Nee*– Er wordt op dit moment geen claimjournaal gemaakt. Deze wordt gemaakt wanneer de claim wordt goedgekeurd. Er kan nog steeds een factuur aan de nieuwe claim worden gekoppeld, ook als er geen claimjournaaljournaal is gemaakt. Vereffening kan echter niet zonder het claimjournaal worden uitgevoerd.

1. Selecteer **OK**.

    Er wordt een nieuwe inhouding gemaakt. Als u de optie **Claimjournaal maken** in stelt op *Ja*, worden de volgende transacties geboekt:

    - **Twee nieuwe klanttransacties** – Eén transactie compenseert het bedrag van de claim op de oorspronkelijke factuur. Met de andere transactie wordt de schuld van een klant op het bedrag van de claim geregistreerd, omdat de claim nog niet is goedgekeurd. De oorspronkelijke factuurtransactie en de tegenrekeningsclaimstransactie worden automatisch gemarkeerd voor vereffening wanneer u de factuur koppelt door **Onderhouden \> Factuur koppelen** te selecteren in het actievenster.
    - **Twee tegenrekeningstransacties** – Deze transacties worden geboekt naar de **Inhoudingstegenrekening** in het grootboek.
    - **Claimjournaal** – Als u het claimjournaal wilt weergeven voor elke inhouding die wordt vermeld op de inhoudingsworkbench, selecteert u het tabblad **Verwijzingen**. Het claimjournaal wordt weergegeven in het veld **Journaalbatchnummer**. U kunt ook het claimjournaal bekijken op het tabblad **Inhoudingsgebeurtenissen**. Hier heeft het een **Bijwerkingstype** waarde van *Vereffen*.

    U bent weer terug op de pagina **Transacties vereffenen**, die nu de geselecteerde factuur als gemarkeerd laat zien. De knop **Boeken** is alleen beschikbaar als u de optie **Claimjournaal maken** instelt op *Ja*. Als deze beschikbaar is, selecteert u **Boeken** om het saldo op de factuur te verminderen met de waarde van het **claimbedrag**.

### <a name="create-a-deduction-from-a-customer-page"></a>Een inhouding maken van een klantpagina

Het proces waarbij een inhouding wordt gemaakt van een klantpagina lijkt op het proces waarbij een inhouding wordt gemaakt via de inhoudingsworkbench. De klant wordt echter automatisch ingesteld.

1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Selecteer de klant waarvoor u een inhouding wilt maken.
1. Selecteer in het Actievenster op het tabblad **Incasso** in de groep **Inhoudingen** de optie **Inhoudingen maken**.

    In het dialoogvenster **Nieuwe inhouding** wordt het veld **Inhoudings-ID** ingesteld op basis van de nummerreeks voor de **Inhoudings-ID** die is gedefinieerd op de pagina **Beheerparameters voor handelstoeslag** (**Verkoop en marketing \> Instellen \> Handelstoeslagen \> Beheerparameters voor handelstoeslag**) Het veld **Klantrekening** is ingesteld op de klantrekening waarop de inhouding van toepassing is.

1. Stel de volgende velden in:

    - **Extern claimnummer** – Voer de claimverwijzing van de klant in.
    - **Claimbedrag** – Voer het bedrag van de claim inclusief btw in. De waarde moet positief zijn.
    - **Valuta**– Selecteer de valuta voor de inhouding. De standaardwaarde is de valuta die is ingesteld voor de geselecteerde klantrekening.
    - **Claimbasis** – Selecteer de basis van de claim. Op basis van de claim wordt het type credittransactie bepaald dat wordt gemaakt nadat de inhouding of claim is goedgekeurd.

        - *Prijs gebaseerd* – Er wordt een concept vrije-tekstfactuur gemaakt.
        - *Hoeveelheid gebaseerd* – Een negatieve verkooporder of retourorder wordt gemaakt.

    - **Claimdatum** – Selecteer de datum van de claim. De standaardwaarde is de huidige datum.
    - **Claimreden** – Selecteer de redencode die van toepassing is op de huidige inhouding. De door u geselecteerde claimbasis heeft invloed op de opties die van toepassing zijn. Zie de sectie [Redenen voor inhouding maken](#deduction-reasons) eerder in dit onderwerp voor meer informatie over het maken en configureren van de claimredenen die hier voor selectie beschikbaar zijn.
    - **Opmerkingen** – Opmerkingen toevoegen die van toepassing zijn. Wanneer de claim is goedgekeurd, kan de fiattur de opmerkingen van de claim bewerken of toevoegen.
    - **Claimjournaal maken** – Stel deze optie in om op te geven of het claimjournaal moet worden gemaakt wanneer de claim of inhouding wordt gemaakt:

        - *Ja* – Er wordt een algemeen journaal gemaakt en geboekt via het claimjournaal dat is ingesteld op de **Parameters van module Klanten**. (Zie voor meer informatie de sectie [Klanten en inhoudingen configureren](#accounts-receivable-deductions) eerder in dit onderwerp.) Wanneer er een factuur aan de claim is gekoppeld, wordt het claimjournaal gebruikt om het saldo van de toepasselijke factuur te verminderen. Als de claim later wordt afgewezen, worden het claimjournaal en de vereffeningen (als er een factuur was gekoppeld) teruggeboekt.
        - *Nee*– Er wordt op dit moment geen claimjournaal gemaakt. Deze wordt gemaakt wanneer de claim wordt goedgekeurd. Er kan nog steeds een factuur aan de nieuwe claim worden gekoppeld, ook als er geen claimjournaaljournaal is gemaakt. Vereffening kan echter niet zonder het claimjournaal worden uitgevoerd.

1. Selecteer **OK**.

    Er wordt een nieuwe inhouding gemaakt. Als u de optie **Claimjournaal maken** in stelt op *Ja*, worden de volgende transacties geboekt:

    - **Twee nieuwe klanttransacties** – Eén transactie compenseert het bedrag van de claim op de oorspronkelijke factuur. Met de andere transactie wordt de schuld van een klant op het bedrag van de claim geregistreerd, omdat de claim nog niet is goedgekeurd. De oorspronkelijke factuurtransactie en de tegenrekeningsclaimstransactie worden automatisch gemarkeerd voor vereffening wanneer u de factuur koppelt door **Onderhouden \> Factuur koppelen** te selecteren in het actievenster.
    - **Twee tegenrekeningstransacties** – Deze transacties worden geboekt naar de **Inhoudingstegenrekening** in het grootboek.
    - **Claimjournaal** – Als u het claimjournaal wilt weergeven voor elke inhouding die wordt vermeld op de inhoudingsworkbench, selecteert u het tabblad **Verwijzingen**. Het claimjournaal wordt weergegeven in het veld **Journaalbatchnummer**. U kunt ook het claimjournaal bekijken op het tabblad **Inhoudingsgebeurtenissen**. Hier heeft het een **Bijwerkingstype** waarde van *Vereffen*.

## <a name="create-a-credit-note-for-a-customer"></a>Een creditnota maken voor een klant

Als er een goedgekeurde korting bestaat voor de klant, maakt u een creditnota op de rekening van de klant om de korting zoals vereist voor te stellen. Het krediet verschijnt vervolgens in de inhoudingsworkbench waarin dit aan een korting kan worden gekoppeld.

Volg deze stappen om een creditnota te maken.

1. Ga naar **Verkoop en marketing \> Klanten \> Alle klanten**.
1. Selecteer de gewenste klant.
1. Selecteer in het actievenster op het tabblad **Incasso** in de groep **Vereffenen** de optie **Transacties vereffenen**.
1. Selecteer de transactie waarop de korting is toegepast in het dialoogvenster **Transacties vereffenen**.
1. Selecteer op de werkbalk in het menu **Functies** het type kortingsprogramma dat van toepassing is.
1. Schakel op de pagina **Korting** op het tabblad **Overzicht** het selectievakje **Markeren** naast de relevante kortings-ID in.
1. Selecteer In het actievenster **Functies \> Creditnota maken**.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Een inhouding verwerken in de inhoudingsworkbench

In de inhoudingsworkbench kunt u kortingen afstemmen op open credittransacties, gesplitste inhoudingen, geweigerde inhoudingen en afschrijvingsinhoudingen.

Afhankelijk van hoe u de inhouding wilt verwerken, voltooit u een of meer van de volgende procedures in de volgende subsecties. U kunt de procedures desgewenst combineren. U kunt bijvoorbeeld een inhouding opsplitsen in twee delen, en vervolgens een deel afstemmen op een krediet maar het resterende gedeelte in de workbench laten om later af te stemmen op een ander krediet. U kunt ook kunt een korting afstemmen op een krediet dat kleiner is dan het inhoudingsbedrag, en vervolgens het resterende saldo van de inhouding weigeren of afschrijven.

### <a name="match-a-deduction-to-a-credit"></a>Een inhouding afstemmen op een krediet

Volg deze stappen om een inhouding op een krediet af te stemmen.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Schakel in de sectie **Openstaande transacties** het selectievakje **Markeren** voor het krediet in dat moet worden afgestemd op de inhouding. Als meerdere kredietbedragen worden vermeld, kunt u meer dan één krediet selecteren om af te stemmen op de inhouding. Als u automatisch kredieten wilt laten selecteren die overeenkomen met het bedrag van de inhouding, selecteert u op de werkbalk een geschikte optie in het menu **Inhoudingsbedrag selecteren**.
1. Klik in het actievenster op **Onderhouden \> Afstemmen**. Het systeem stemt de inhouding af op het krediet. Als er een saldo blijft in de inhouding, wordt dit weergegeven in het veld **Resterend bedrag** op het tabblad **Inhoudingen**.

    > [!NOTE]
    > Voor inhoudingen die zijn gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina, is de opdracht **Onderhouden \> Afstemmen** alleen beschikbaar als het veld **Claimstatus** is ingesteld op *Geaccepteerd*. Deze opdracht kan worden gebruikt om de op prijs of hoeveelheid gebaseerde transactie handmatig af te stemmen op de gekoppelde krediet in de sectie **Openstaande transacties**. Dit krediet wordt gemaakt als de inhouding is goedgekeurd (via de opdracht **Onderhouden \> Inhouding goedkeuren**) of wanneer de inhouding is gekoppeld aan een bestaand krediet, zoals wordt beschreven in de sectie [Verwerken van kredieten gemaakt buiten het inhoudingsgoedkeuringsproces om](#credits-outside-approval) verder in dit onderwerp. De periodieke taak *Goedgekeurde inhoudingen vereffenen* (**Verkoopmarketing \> Periodieke taken \> Goedgekeurde inhoudingen vereffenen**) kan ook worden gebruikt om automatisch inhoudingen en kredietbedragen met overeenkomende **Inhoudings-ID**-waarden en bedragen af te stemmen.

### <a name="split-a-deduction"></a>Inhouding splitsen

Volg deze stappen om een inhouding te splitsen.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Klik in het actievenster op **Onderhouden \> Splitsen**.
1. Voer in het dialoogvenster **Splitsen**, in het veld **Bedrag splitsen**, het bedrag in dat moet worden opgesplitst van de hoofdinhouding. Selecteer vervolgens **OK**.
1. Merk op dat op het tabblad **Inhoudingen** een nieuw record verschijnt voor het gesplitste bedrag. Het oorspronkelijke inhoudingsrecord bevat de rest van het inhoudingssaldo. U kunt nu de twee delen van de oorspronkelijke korting afzonderlijk beheren.
1. Selecteer het oorspronkelijke inhoudingsrecord en selecteer vervolgens het tabblad **Verwijzingen**. In het veld **Gesplitst bedrag** wordt het bedrag getoond dat is opgesplitst van het oorspronkelijke bedrag.

### <a name="attach-an-invoice-to-a-deduction"></a>Een factuur aan een inhouding koppelen

U kunt een factuur aan een inhouding koppelen als de inhouding is gemaakt via de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina, en als er momenteel geen factuur aan is gekoppeld (dat wil zeggen dat de kolom **Factuur** leeg is).

Volg deze stappen om een factuur aan een inhouding te koppelen.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Selecteer in het actievenster **Onderhouden \> Factuur koppelen**.
1. Selecteer een factuur in het dialoogvenster **Factuur koppelen** en selecteer vervolgens **OK**.
1. Volg een van deze stappen in het dialoogvenster **Transacties vereffenen**, afhankelijk van of er een claimjournaal is geboekt toen de inhouding werd gemaakt:

    - Als er een claimjournaal is geboekt, wordt op de geselecteerde factuur en de klantkrediettransactie van het claimjournaal een vinkje in de kolom **Markeren** vermeld. Selecteer **Boeken**. Het resterende saldo op de gekoppelde factuur wordt verminderd met het claimbedrag.
    - Als een claimjournaal niet is geboekt, wordt er in de kolom **Markeren** geen vinkje bij de transactie getoond. Omdat u een claimjournaal pas kunt compenseren als de inhouding is goedgekeurd, selecteert u **Annuleren**.

### <a name="detach-an-invoice-from-a-deduction"></a>Een factuur aan een inhouding ontkoppelen

U kunt een factuur van een inhouding ontkoppelen als de inhouding is gemaakt via de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina, als er momenteel een factuur aan is gekoppeld (dat wil zeggen dat de kolom **Factuur** een factuurnummer toont en als het veld **Claimstatus** ingesteld is op *Openstaand*). U zou deze taak kunnen voltooien omdat er een onjuiste factuur is gekoppeld. De factuur wordt verwijderd uit de inhouding en het resterende saldo wordt bijgewerkt als deze is verminderd toen de factuur werd gekoppeld.

Volg deze stappen om een factuur te ontkoppelen.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Selecteer in het actievenster **Onderhouden \> Factuur ontkoppelen**.

### <a name="approve-a-deduction"></a>Inhouding goedkeuren

U kunt inhoudingen goedkeuren die zijn gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina. U kunt echter alleen inhoudingen goedkeuren waarbij het veld **Claimstatus** is ingesteld op *Openstaand*.

Volg deze stappen om een inhouding goed te keuren.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Selecteer in het actievenster **Onderhouden \> Inhouding goedkeuren**.
1. Bewerk of voeg waar nodig informatie aan de **Notitie** waarde toe in het dialoogvenster **Inhouding goedkeuren**.
1. Als de inhouding op prijs is gebaseerd en er is geen factuur aan gekoppeld, selecteert u een btw-groep voor artikelen. Doorgaans wordt de btw-artikelgroep ingesteld op de factuur. Daarom moet de btw-artikelcode worden opgegeven wanneer deze niet aan een factuur is gekoppeld.
1. Selecteer **OK**.

    Op dit punt kunnen er geen verdere wijzigingen meer worden aangebracht in de inhouding. Als de optie **Claimjournaal maken** is ingesteld op *Nee* bij het maken van de inhouding, wordt het claimjournaal gemaakt en geboekt wanneer de inhouding wordt goedgekeurd. Nadat de inhouding is goedgekeurd, wordt het krediet automatisch gemaakt en geopend. Het type is afhankelijk van de waarde van de **Claimbasis** van de inhouding:

    - *Prijs gebaseerd* – Als de inhouding op prijzen is gebaseerd, wordt een vrije-tekstfactuur gemaakt voor de klantrekening. U kunt een omschrijving toevoegen en het krediet boeken. Bij het maken van het concept worden de volgende velden ingevuld met inhouding:

        - **Inhoudings-ID** – Dit veld wordt aan de koptekst toegevoegd om de traceerbaarheid naar de inhouding terug te herleiden.
        - **Hoofdrekening** – De waarde wordt bepaald door de waarde van de **Boekingsrekening claimen** die is ingesteld voor de inhoudingsreden die is toegewezen aan de inhouding.
        - **Btw-groep voor artikel** – De waarde wordt bepaald door de gekoppelde factuur of door de waarde die u hebt geselecteerd toen u de inhouding hebt goedgekeurd.
        - **Eenheidsprijs** – De waarde is het krediet van het claimbedrag van de inhouding.
        - **Factuurtekst** – Dit veld is standaard ingesteld op de waarde **Notities** van de inhouding.

    - *Hoeveelheid gebaseerd* – Als de inhouding op hoeveelheid is gebaseerd, wordt een openstaande verkooporder of retourorder gemaakt. De instelling **Retourorder maken** op de pagina **[Parameters van module Klanten](#accounts-receivable-deductions)** bepaalt of een verkooporder of een retourorder wordt gemaakt wanneer de korting wordt goedgekeurd. De pagina **Orders kopiëren** wordt weergegeven en gefilterd om rijen weer te geven waarin het veld **Factuurrekening** is ingesteld op de klantrekening van de inhouding. Volg vervolgens deze stappen:

        1. Op het sneltab tabblad **Facturen** ziet u in de sectie **Kopteksten** verkoopfacturen waar de **Factuurrekening** waarde overeenkomt met de klantrekening van de inhouding. Selecteer een van toepassing zijnde verkoopfactuur.
        1. In de sectie **Regels** worden de regels van de geselecteerde verkoopfactuur vermeld. Schakel het selectievakje **Selecteren** in voor elke regel die u wilt kopiëren. U kunt ook in de sectie **Kopteksten** het selectievakje **Alle selecteren** selecteren voor de verkooporder om alle regels te selecteren.
        1. Pas de waarde **Hoeveelheid** voor een of meer regels naar behoefte aan.

            Alle regels die u tot nu toe hebt geselecteerd, staan op het sneltabblad **Te kopiëren geselecteerde regels of koptekst**.

        1. Herhaal waar nodig de vorige twee stappen tot alle vereiste regels worden weergegeven op het sneltabblad **Te kopiëren geselecteerde regels of koptekst**.
        1. Selecteer **OK**.

            De nieuwe retourorder wordt geopend en de volgende velden worden automatisch ingesteld:

            - **Inhoudings-ID** – Dit veld wordt aan de koptekst toegevoegd om de traceerbaarheid naar de inhouding terug te herleiden.
            - **Redencode retour** – Dit veld wordt standaard ingesteld op de waarde **Redencode retour** die is ingesteld voor de inhoudingsreden die aan de inhouding is toegewezen.

Nadat het krediet is gefactureerd, wordt deze weergegeven in de sectie **Openstaande transacties** van de inhoudingsworkbench ten opzichte van de van toepassing zijnde **Inhoudings-ID**-waarde en wordt het veld **Claimtype** ingesteld op *Overige kredieten*. Het krediet is beschikbaar totdat dit is vereffend met de inhouding op een van de volgende manieren:

- U vereffent deze handmatig door **Onderhouden \> Afstemmen** te selecteren in het actievenster.
- Dit wordt automatisch vereffend door de periodieke taak *Goedgekeurde claims vereffenen* (**Verkoop en marketing \> Periodieke taken \> Goedgekeurde claims vereffenen**).
- Dit wordt automatisch vereffend, omdat de optie **Automatische vereffening** op het tabblad **Vereffening** van de pagina **Parameters van module Klanten** is ingesteld op *Ja*.

Als u het krediet wilt weergeven dat is gemaakt wanneer de inhouding is goedgekeurd, kunt u ook de knop **Openstaand krediet** gebruiken in de sectie **Openstaande transacties** van de inhoudingsworkbench.

### <a name="create-a-return-order"></a>Retourorder maken

U kunt een retourorder maken voor inhoudingen die zijn gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina. Er moet echter aan alle volgende voorwaarden worden voldaan:

- Het veld **Claimbasis** is ingesteld op *Hoeveelheid gebaseerd*.
- Het veld **Claimstatus** is ingesteld op *Openstaand*.
- De optie **Retourorder maken** op het tabblad **Inhoudingen** op de pagina **[Parameters van module Klanten](#accounts-receivable-deductions)** is ingesteld op *Ja*.
- De optie **Retourorder maken vóór inhoudingsgoedkeuring** op het tabblad **Inhoudingen** op de pagina **[Parameters van module Klanten](#accounts-receivable-deductions)** is ingesteld op *Ja*.

Voer de volgende stappen uit om een retourorder te maken.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Selecteer in het actievenster **Onderhouden \> Retourorder maken**.
1. Bewerk of voeg waar nodig informatie aan de bestaande **Notitie** waarde toe in het dialoogvenster **Inhouding goedkeuren** en selecteer vervolgens **OK**.
1. In het dialoogvenster **Orders kopiëren** op het sneltabblad **Facturen** ziet u in de sectie **Kopteksten** verkoopfacturen waar de **Factuurrekening** waarde overeenkomt met de klantrekening van de inhouding. Selecteer een van toepassing zijnde verkoopfactuur.
1. In de sectie **Regels** worden de regels van de geselecteerde verkoopfactuur vermeld. Schakel het selectievakje **Selecteren** in voor elke regel die u wilt kopiëren. U kunt ook in de sectie **Kopteksten** het selectievakje **Alle selecteren** selecteren voor de verkooporder om alle regels te selecteren.
1. Pas de waarde **Hoeveelheid** voor een of meer regels naar behoefte aan.

    Alle regels die u tot nu toe hebt geselecteerd, staan op het sneltabblad **Te kopiëren geselecteerde regels of koptekst**.

1. Herhaal waar nodig de vorige twee stappen tot alle vereiste regels worden weergegeven op het sneltabblad **Te kopiëren geselecteerde regels of koptekst**.
1. Selecteer **OK**.

    De nieuwe retourorder wordt geopend en de volgende velden worden automatisch ingesteld:

    - **Inhoudings-ID** – Dit veld wordt aan de koptekst toegevoegd om de traceerbaarheid naar de inhouding terug te herleiden.
    - **Redencode retour** – Dit veld wordt standaard ingesteld op de waarde **Redencode retour** die is ingesteld voor de inhoudingsreden die aan de inhouding is toegewezen.

### <a name="deny-a-deduction"></a>Inhouding weigeren

Volg deze stappen om een inhouding af te wijzen.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Klik in het actievenster op **Onderhouden \> Afwijzen**.
1. Selecteer de redencode voor de afwijzing in het dialoogvenster **Afwijzen** en selecteer **OK**.
1. Selecteer *Gesloten* in het veld **Tonen** onder het Actievenster.

    Het tabblad **Inhoudingen** toont de afgewezen inhouding en het veld **Resterende bedrag** voor de inhouding is ingesteld op *0.00*.

    Voor inhoudingen die zijn gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina, vinden de volgende gebeurtenissen plaats:

    - Op het tabblad **Verwijzingen** worden de velden in de sectie **Afwijzing** bijgewerkt.
    - Als u ervoor hebt gekozen om het claimjournaal te maken bij het maken van de inhouding en als er een factuur is gekoppeld aan de inhouding die het saldo van de factuur heeft verlaagd, wordt de factuur niet opgeslagen en wordt het resterende saldo van de eerder gekoppelde factuur verhoogd met het bedrag van de afgewezen claim.
    - Het veld **Status** van de inhouding is ingesteld op *Gesloten*.
    - Het veld **Claimstatus** van de inhouding is ingesteld op *Geweigerd*.

Volg deze stappen om een afwijzing terug te draaien.

1. Selecteer een geweigerde inhouding op het tabblad **Inhoudingen**.
1. Selecteer in het actievenster **Afwijzing terugdraaien**.

    Voor inhoudingen die zijn gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina, vinden de volgende gebeurtenissen plaats:

    - Op het tabblad **Verwijzingen** worden de velden in de sectie **Afwijzing** bijgewerkt.
    - Het veld **Status** van de inhouding is ingesteld op *Openstaand*.
    - Het veld **Claimstatus** van de inhouding is ingesteld op *Openstaand*.

### <a name="write-off-a-deduction"></a>Een inhouding afschrijven

Volg deze stappen om een inhouding af te schrijven.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Klik in het actievenster op **Onderhouden \> Afschrijven**.
1. Selecteer de redencode voor de afschrijving in het dialoogvenster **Afschrijven** en selecteer **OK**.
1. Selecteer *Gesloten* in het veld **Weergeven**.

    Het tabblad **Inhoudingen** toont de afgeschreven inhouding en het veld **Resterend bedrag** voor de inhouding is ingesteld op *0.00*.

    Voor inhoudingen die zijn gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina, vinden de volgende gebeurtenissen plaats:

    - Op het tabblad **Verwijzingen** worden de velden in de sectie **Afschrijven** bijgewerkt.
    - Als u het claimjournaal hebt gemaakt toen de inhouding werd gemaakt, wordt een claimjournaal geboekt naar de afschrijvingsredencode van de inhouding. U kunt dit item weergeven op het tabblad **Gebeurtenissen inhouding**, waar het een waarde **type Update** heeft van *Afschrijven*.
    - Het veld **Status** van de inhouding is ingesteld op *Gesloten*
    - Het veld **Claimstatus** van de inhouding is ingesteld op *Afschrijven*.

Volg deze stappen om een afschrijving terug te boeken.

1. Selecteer een geweigerde inhouding op het tabblad **Inhoudingen**.
1. Klik in het actievenster op **Afschrijving terugboeken**.

    Voor inhoudingen die zijn gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina, vinden de volgende gebeurtenissen plaats:

    - Op het tabblad **Verwijzingen** worden de velden in de sectie **Afschrijven** bijgewerkt.
    - Als u het claimjournaal hebt gemaakt toen de inhouding werd gemaakt, wordt een claimjournaal geboekt naar de afschrijvingsredencode van de inhouding. U kunt dit item weergeven op het tabblad **Gebeurtenissen inhouding**, waar het een waarde **type Update** heeft van *Afschrijving terugboeken*.
    - Het veld **Status** van de inhouding is ingesteld op *Openstaand*.
    - Het veld **Claimstatus** van de inhouding is ingesteld op *Openstaand*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Kredieten die zijn gemaakt buiten het inhoudingsproces goedkeuren

Deze sectie is alleen van toepassing op inhoudingen die zijn gemaakt met de opdracht **Nieuwe inhouding** op de inhoudingsworkbench, klantvereffening of klantpagina.

Verschillende gebruikers hebben mogelijk al een vrije-tekstfactuur, retourorder of negatieve verkooporder gemaakt voor een claim van een klant buiten het proces voor **Inhoudingen goedkeuren**. Wanneer de bestaande inhouding wordt goedgekeurd op de inhoudingsworkbench, wordt automatisch nog een vrije-tekstfactuur, retourorder of negatieve verkooporder gemaakt. In deze sectie wordt beschreven hoe u bestaande kredieten kunt koppelen aan een inhouding voordat de inhouding wordt goedgekeurd om dubbele crediteringen te voorkomen.

### <a name="attach-a-credit-to-deduction"></a>Een krediet aan een inhouding koppelen

In deze sectie wordt beschreven hoe u een krediet kunt koppelen aan een inhouding op het krediet.

Nadat het krediet is gekoppeld aan de inhouding, kunt u het weergeven via de knop **Openstaand krediet** op de werkbalk in de sectie **Openstaande transacties** van de inhoudingsworkbench.

Nadat het krediet is gefactureerd, en de inhouding is goedgekeurd, wordt het krediet weergegeven in de sectie **Openstaande transacties** van de inhoudingsworkbench ten opzichte van de van toepassing zijnde **Inhoudings-ID**-waarde en wordt het veld **Claimtype** ingesteld op *Overige kredieten*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Een vrije-tekstfactuur aan een inhouding koppelen

Volg deze stappen om een vrije-tekstfactuur aan een inhouding te koppelen.

1. Ga naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**.
1. Selecteer de betreffende factuur.
1. Selecteer in het actievenster op het tabblad **Factuur** de optie **Krediet aan inhouding koppelen**. Deze knop is alleen beschikbaar als de **Inhoudings-ID** van de vrije-tekstfactuur leeg is. Als het veld leeg is, is de vrije-tekstfactuur nog niet aan een inhouding gekoppeld.
1. Op de pagina **Krediet aan inhouding koppelen** kunt u *één* inhouding selecteren. Alleen openstaande *prijs-gebaseerde* inhoudingen kunnen worden geselecteerd.
1. Selecteer **OK**. Het veld **Inhouding-ID** wordt ingesteld op de koptekst van de vrije-tekstfactuur.

#### <a name="attach-a-return-order-to-a-deduction"></a>Een retourorder koppelen aan een inhouding

Volg deze stappen om een retourorder aan een inhouding te koppelen.

1. Ga naar **Klanten \> Orders \> Alle retourorders**.
1. Selecteer het RMA-nummer (Received of Open Return Merchandise Authorization).
1. Selecteer in het actievenster op het tabblad **Retourorder** de optie **Krediet aan inhouding koppelen**. Deze knop is alleen beschikbaar als de **Inhoudings-ID** van de retourorder leeg is. Als het veld leeg is, is de retourorder nog niet aan een inhouding gekoppeld.
1. Op de pagina **Krediet aan inhouding koppelen** kunt u *één* inhouding selecteren. Alleen openstaande *hoeveelheid-gebaseerde* inhoudingen kunnen worden geselecteerd.
1. Selecteer **OK**. Het veld **Inhouding-ID** wordt ingesteld op de koptekst van de retourorder.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Een verkooporder koppelen aan een inhouding

Volg deze stappen om een verkooporder aan een inhouding te koppelen.

1. Ga naar **Klanten \> Orders \> Alle verkooporders**.
1. Selecteer de van toepassing zijnde openstaande, geleverde of gefactureerde verkooporder.
1. Selecteer in het actievenster op het tabblad **Factuur** de optie **Krediet aan inhouding koppelen**. Deze knop is alleen beschikbaar als de **Inhoudings-ID** van de verkooporder leeg is. Als het veld leeg is, is de verkooporder nog niet aan een inhouding gekoppeld.
1. Op de pagina **Inhouding koppelen** kunt u *één* inhouding selecteren. Alleen openstaande *hoeveelheid-gebaseerde* inhoudingen kunnen worden geselecteerd.
1. Selecteer **OK**. Het veld **Inhouding-ID** wordt ingesteld op de koptekst van de verkooporder.

#### <a name="detach-a-deduction-from-a-credit"></a>Een inhouding van een krediet loskoppelen

Als er een onjuiste inhouding is gekoppeld, kunt u deze loskoppelen van de credit. Er moet echter aan alle volgende voorwaarden worden voldaan:

- Aan de inhouding is een credit gekoppeld.
- Het veld **Claimstatus** is ingesteld op *Openstaand*.

Als u een inhouding van een krediet wilt loskoppelen, volgt u een van deze stappen, afhankelijk van het krediettype:

- **Vrije-tekstfacturen**: selecteer een factuur op de pagina **Alle vrije-tekstfacturen**.  Selecteer vervolgens in het actievenster op het tabblad **Factuur** de optie **Krediet van inhouding loskoppelen**.
- **Retourorders**: selecteer een order op de pagina **Alle retourorders**. Selecteer vervolgens in het actievenster op het tabblad **Retourorder** de optie **Krediet van inhouding loskoppelen**.
- **Verkooporders**: selecteer een order op de pagina **Alle verkooporders**. Selecteer vervolgens in het actievenster op het tabblad **Factuur** de optie **Krediet van inhouding loskoppelen**.

### <a name="attach-a-deduction-to-a-credit"></a>Een inhouding aan een krediet koppelen

In deze sectie wordt beschreven hoe u een inhouding kunt koppelen aan een krediet van de inhouding.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Een inhouding koppelen aan een vrije-tekst-, retourorder- of verkooporderkrediet

Ga als volgt te werk om een inhouding te koppelen aan een vrije-tekst-, retourorder- of verkooporderkrediet.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer de betreffende openstaande inhouding.
1. Selecteer in het actievenster **Onderhouden \> Inhouding aan krediet koppelen**. Deze knop is alleen beschikbaar als het veld **Claimstatus** is ingesteld op *Openstaand*.
1. Op de pagina **Krediet koppelen** kunt u *één* krediet selecteren. Het type krediet dat wordt weergegeven, is afhankelijk van de waarde van de **Claimbasis** van de inhouding:

    - *Prijs gebaseerd* – Op de pagina worden vrije-tekstfacturen weergegeven voor de klantrekening waar het veld **Inhoudings-ID** leeg is. Klantvorderingen worden ook weergegeven omdat de vrije-tekstfactuur mogelijk niet is geboekt. Daarom is het mogelijk dat er geen nummer is waarnaar kan worden verwezen.
    - *Hoeveelheid gebaseerd* – Het type krediet dat wordt weergegeven, is afhankelijk van de instelling van de optie **Retourorder maken** op de pagina **[Parameters van module Klanten](#accounts-receivable-deductions)**:

        - *Ja* – Op de pagina worden retourorders weergegeven voor de klantrekening waar het veld **Inhoudings-ID** leeg is.
        - *Nee* – Op de pagina worden verkooporders weergegeven voor de klantrekening waar het veld **Inhoudings-ID** leeg is.

1. Selecteer **OK**. Het veld **Inhouding-ID** wordt ingesteld op de koptekst van het krediet.

Nadat het krediet is gekoppeld aan de inhouding, kunt u het weergeven via de knop **Openstaand krediet** op de werkbalk in de sectie **Openstaande transacties** van de inhoudingsworkbench.

Nadat het krediet is gefactureerd, en de inhouding is goedgekeurd, wordt het krediet weergegeven in de sectie **Openstaande transacties** van de inhoudingsworkbench ten opzichte van de van toepassing zijnde **Inhoudings-ID**-waarde en wordt het veld **Claimtype** ingesteld op *Overige kredieten*.

#### <a name="detach-a-credit-from-the-deduction"></a>Een krediet van een inhouding loskoppelen

Als er een onjuist krediet is gekoppeld, kunt u deze loskoppelen van de inhouding. Selecteer in het actievenster in de groep **Onderhouden** de optie **Inhouding van krediet loskoppelen**. De waarde voor de **Inhouding-ID** wordt uit het krediet verwijderd.

De knop **Inhouding van krediet loskoppelen** is alleen beschikbaar als aan de volgende voorwaarden is voldaan:

- Aan de inhouding is een credit gekoppeld.
- Het veld **Claimstatus** is ingesteld op *Openstaand*.

## <a name="create-a-one-time-promotion"></a>Een eenmalige promotie maken

Soms hebt u geen goedgekeurde korting om af te stemmen met een inhouding. In dat geval, kunt u de functie *Eenmalige promotie* gebruiken om de inhouding af te stemmen op een handelstoelage die aan de klant is gekoppeld. De functie *Eenmalige promotie* maakt een nieuwe handelsovereenkomst en een handelsgebeurtenis met een totaalbedrag. De functie stemt vervolgens het totale bedrag af op de inhouding en maakt de boekingen die nodig zijn om de inhouding te sluiten.

Deze functie is handig als u handelstoeslagen gebruikt. Zie [Beheer van handelstoeslag](../sales-marketing/trade-allowance.md) voor meer informatie over handelstoeslagen.

Eerst moet u een sjabloon maken die kan worden gebruiken om de nieuwe overeenkomst voor handelstoeslagen te maken. Ga als volgt te werk om een sjabloon in te stellen.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Sjablonen**.
1. Selecteer **Nieuw** in het actievenster.
1. Vul de velden met de informatie die moet verschijnen in de overeenkomsten die vanaf de sjabloon worden gemaakt.
1. Selecteer een hiërarchieniveau in het sneltabblad **Klanten** in het veld **Hiërarchie**.
1. Selecteer in de hiërarchielijst de klant met een niet-overeenkomende inhouding en selecteer vervolgens de pijl-rechts (**\>**). De klant wordt toegevoegd aan de lijst met klanten **van de** handelsovereenkomst.
1. Stel de resterende velden in zoals u wilt en sluit vervolgens de pagina.
1. Ga naar **Verkoop en marketing \> Instellen \> Handelstoeslag \> Beheerparameters voor handelstoeslag**.
1. Selecteer op het tabblad **Overzicht** in het veld **Sjabloon eenmalige promotie** de naam van de sjabloon die u wilt gebruiken om eenmalige promoties te maken.

Vervolgens kunt u een eenmalige promotie maken in de inhoudingsworkbench. Volg deze stappen om eenmalige promotie te maken.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer het selectievakje **Markeren** naast de te verwerken inhouding.
1. Selecteer in het actievenster de optie **Onderhouden \> Inhouding vereffenen als eenmalige promotie**. 
1. Volg deze stappen in het dialoogvenster **Eenmalige promotie** om de inhouding te koppelen aan een of meer fondsen:

    1. Klik op **Nieuw** en selecteer vervolgens een fonds-ID in het veld **Fonds-ID**. Herhaal deze stap om zo veel fondsen te voegen als nodig is.
    1. Voer in het veld **Procent** naast elk fonds-ID het percentage van de inhouding in om aan het fonds toe te wijzen. De bedragen die u in de velden **Procent** invoert moeten 100 procent zijn in totaal.

1. Selecteer **OK**. Het systeem maakt een nieuwe handelstoeslagovereenkomst met een handelsgebeurtenis voor het totaalbedrag en stemt het totale bedrag af op de inhouding.

## <a name="do-a-mass-update-of-deductions"></a>Werk de inhoudingen groepsgewijs bij

Als u dezelfde wijziging voor meerdere inhoudingen moet maken, kunt u deze inhoudingen selecteren en de velden groepsgewijs bijwerken.

Volg de onderstaande stappen om een groepsgewijze update uit te voeren.

1. Ga naar **Verkoop en marketing \> Handelstoeslagen \> Inhoudingen \> Inhoudingsworkbench**.
1. Selecteer in het veld **Weergeven** onder het Actievenster het type te bekijken inhoudingen.
1. Schakel het selectievakje in naast elke inhouding die u wilt bijwerken. Selecteer vervolgens in het actievenster **Onderhouden \> Groepsgewijs bijwerken**.
1. In het dialoogvenster **Groepsgewijs bijwerken** worden de geselecteerde inhoudingen weergegeven. Werk de velden bij zoals u wilt en selecteer **OK** om de wijzigingen te accepteren.
