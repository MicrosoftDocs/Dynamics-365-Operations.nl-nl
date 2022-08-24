---
title: Factureren voor onderhoud aan activa van klanten
description: In dit artikel wordt uitgelegd hoe u onderhoudswerkzaamheden aan de activa die uw klanten in eigendom hebben, maakt, verwerkt en factureert.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7c2c07f3e3eb76ff20e37e8d5d485dc08232c7a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220417"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Factureren voor onderhoud aan activa van klanten

[!include [banner](../../includes/banner.md)]

Met de functie *Facturering werkorder* kunt u onderhoudswerk maken, verwerken en factureren dat wordt uitgevoerd op activa van uw klanten. Met deze functie kunt u de volgende taken uitvoeren:

- Klanten koppelen aan de activa waarvan ze eigenaar zijn.
- Een klant selecteren en de activa bekijken die klant bezit wanneer u een werkorder maakt.
- Een bovenliggend project instellen voor elke klant.
- Uren, artikelen, onkosten en tarieven voor de werkorder registreren en vervolgens later een factuurvoorstel maken voor de klant.

Bovendien bevat de functie de volgende functionaliteit:

- Het projectcontract uit het bovenliggende project van een klant wordt automatisch gekopieerd naar het relevante werkorderproject.
- Activabeheer kan nu het type projecttransactie *tarief* gebruiken voor zowel werkorderprognoses als werkorderjournalen.

## <a name="turn-on-the-customer-billing-feature"></a>De functie klant factureren inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Projectbeheer en boekhouding*
- **Functienaam:** *Facturering werkorder*

## <a name="example-scenario"></a>Voorbeeldscenario

Als u wilt weten hoe deze functie werkt, doorloopt u de volgende voorbeeldscenario's.

Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd. U moet de rechtspersoon **USMF** selecteren voordat u begint.

U kunt dit scenario ook gebruiken als instructie voor het gebruik van deze functie wanneer u met een productiesysteem werkt. In dat geval moet u echter uw eigen waarden vervangen en hebt u mogelijk niet de beschikking over bepaalde typen vereiste records die met de standaard demogegevens worden verstrekt.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>Stap 1: Een nieuw projectcontract voor de klant maken

1. Ga naar **Projectbeheer en boekhouding \> Projecten \> Projectcontracten**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Nieuw projectcontract** de volgende waarden in:

    - **Naam:** *Pelican Wholesales*
    - **Financieringstype:** *Klant*
    - **Financieringsbron:** *US-013* (*Pelican Wholesales*)

1. Selecteer **OK**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>Stap 2: Een nieuw bovenliggend project voor de klant maken

Het bovenliggende project dat u hier maakt, wordt gebruikt wanneer werkorders voor de klant worden gemaakt.

1. Ga naar **Projectbeheer en boekhouding \> Projecten \> Alle projecten**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Nieuw project** de volgende waarden in:

    - **Projecttype:** *Tijd en materiaal*
    - **Projectnaam:** *Pelican Wholesales-werkorders*
    - **Projectgroep:** *TM*
    - **Projectcontract-ID:** *Pelican Wholesales* (het contract dat u eerder hebt gemaakt)
    - **Begindatum:** Selecteer de datum van vandaag.

1. Selecteer **Project maken**.
1. Het nieuwe project wordt geopend. Noteer de **Project-ID**. U moet deze later invoeren.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>Stap 3: Een nieuw type werkorder maken in Activabeheer

1. Ga naar **Activabeheer \> Instellen \> Werkorder \> Werkordertypen**.
1. Selecteer **Nieuw** in het actievenster.
1. Er wordt een nieuwe record aan de lijst toegevoegd. Stel de volgende waarden in:

    - **Werkordertype:** *Service*
    - **Naam:** *Servicewerkorders*
    - **Levenscyclusstatus van werkorder:** *Standaard*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>Stap 4: Het klantaccount aan het bovenliggende project koppelen

U moet nu het klantaccount koppelen aan het bovenliggende project in de projectinstellingen in Activabeheer.

1. Ga naar **Activabeheer \> Instellen \> Werkorders \> Projectinstellingen**.
1. Selecteer op het tabblad **Bovenliggend project** de optie **Toevoegen** om een regel toe te voegen.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Klantaccount:** *US-013* (*Pelican Wholesales*)
    - **Project-ID:** Voer de project-ID in die u eerder hebt genoteerd.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>Stap 5: De projectgroep en het type koppelen aan het werkorderproject

U moet nog steeds op de pagina **Projectinstellingen** staan (**Activabeheer \> Instellen \> Werkorders \> Projectinstellingen**).

1. Selecteer op het tabblad **Projectgroep** de optie **Toevoegen** om een regel toe te voegen.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Type werkorder:** *Service* (het werkordertype dat u eerder hebt gemaakt)
    - **Projectgroep:** *TM*

> [!NOTE]
> Het projectcontract voor het werkorderproject wordt altijd overgenomen van het bovenliggende project.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>Stap 6: Een activum aan de klant-ID koppelen

1. Ga naar **Activabeheer \> Activa \> Actieve activa**.
1. Voer in het veld **Filter** *VE-102* in en selecteer om te filteren op **Activum**.
1. Selecteer het activum om de instellingen te openen.
1. Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-013* (*Pelican Wholesales*).

    Het veld **Naam** wordt automatisch bijgewerkt naar *Pelican Wholesales*.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>Stap 7: Een nieuw type werkorder maken voor het activum

1. Ga naar **Activabeheer \> Werkorders \> Actieve werkorders**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Werkorder maken** de volgende waarden in:

    - **Werkordertype:** *Service*
    - **Omschrijving:** *Vrachtwagen repareren*
    - **Klantaccount:** *US-013* (*Pelican Wholesales*)
    - **Activum:** *VE-102*

        > [!NOTE]
        > De opzoekactie toont alleen activa die aan het geselecteerde klantaccount zijn gekoppeld.

    - **Onderhoudstaaktype:** *Repareren*
    - **Handel:** *Mechanisch*
    - **Serviceniveau:** *4*

1. Selecteer **OK**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>Stap 8: De werkorder controleren en er aan beginnen te werken

In deze sectie werkt u aan de werkorder die u in de vorige sectie hebt gemaakt.

1. Volg deze stappen om te controleren of het bovenliggende project het project *Pelican Wholesales-werkorder* is:

    1. Selecteer in de sectie **Onderhoudstaken voor werkorders** een regel.
    1. Controleer op het sneltabblad **Regeldetails** de waarde **Project-ID**. Dit moet een nummer met een streepje zijn in de vorm *\<Parent-Project-ID\>-\<Project-ID\>*. Deze waarde is een koppeling.
    1. Selecteer de koppeling van een project-ID om een pagina te openen waarin u het bovenliggende project en de projectnamen kunt bekijken.

1. Selecteer in het actievenster op het tabblad **Werkorder** in de groep **Levenscyclusstatus** de optie **Status van werkorder bijwerken**.
1. Schakel in het dialoogvenster **Status van werkorder bijwerken** in de kolom **Selecteren** het selectievakje in voor de rij waar het veld **Levenscyclusstatus** is ingesteld op *In uitvoering*.
1. Selecteer **OK**.
1. Klik in het dialoogvenster **Levenscyclusstatus: in uitvoering** op **OK**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>Stap 9: De uren die aan de werkorder zijn besteed boeken en een nieuw factuurvoorstel maken

In deze sectie werkt u door aan de werkorder waaraan u werkte in de vorige sectie.

1. Ga in het Actievenster naar het tabblad **Werkorder** en selecteer in de groep **Project** de optie **Journalen**.

    De pagina **Werkorderjournalen** verschijnt. Hier kunt u de tijd registreren die u aan de werkorder hebt besteed.

1. Selecteer op het sneltabblad **Uren** de optie **Regel toevoegen**.
1. Stel op de nieuwe regel het veld **Uren** in op *4*.
1. Selecteer **Journalen boeken** in het actievenster.
1. Sluit de pagina **Werkorderjournalen** om terug te keren naar de werkorder.
1. Selecteer in het actievenster op het tabblad **Factureren** de optie **Nieuw factuurvoorstel**.
1. Schakel in het dialoogvenster **Factuurvoorstel maken** in de sectie **Projecttransacties** het selectievakje **Selecteren** in voor elke regel die u wilt factureren.
1. Selecteer **OK** om het dialoogvenster te sluiten en het nieuwe factuurvoorstel te bekijken.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]