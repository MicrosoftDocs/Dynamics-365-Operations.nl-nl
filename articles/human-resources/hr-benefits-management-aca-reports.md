---
title: ACA-rapporten genereren in Vergoedingenbeheer
description: In dit onderwerp wordt beschreven hoe Vergoedingenbeheer u helpt gegevens bij te houden die worden gerapporteerd met formulier 1095-B en formulier 1095-C voor het werkgeversmandaat van de Affordable Care Act (ACA).
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 24df18f428e4ca14859bc34048a6bda5e03d1b2f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464369"
---
# <a name="generate-aca-reports-in-benefits-management"></a>ACA-rapporten genereren in Vergoedingenbeheer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vergoedingenbeheer helpt u gegevens bij te houden die worden gerapporteerd met formulier 1095-B en formulier 1095-C voor het werkgeversmandaat van de Affordable Care Act (ACA). Net zoals de ACA-rapportagefunctionaliteit in het oude werkgebied **Vergoedingen**, is deze functionaliteit alleen van toepassing op rechtspersonen in de Verenigde Staten.

Als u deze functionaliteit wilt gebruiken, moet u eerst **Geavanceerd vergoedingenbeheer** inschakelen. Meer informatie, inclusief belangrijke voorbehouden voor Vergoedingenbeheer, vindt u in [Vergoedingenbeheer in- of uitschakelen](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> U kunt ACA-rapportages alleen gebruiken vanuit het werkgebied **Vergoedingenbeheer** of het oude werkgebied **Vergoedingen**, niet vanuit beide. Als u bijvoorbeeld bent overgestapt naar Vergoedingenbeheer, is ACA-rapportage alleen beschikbaar vanuit het werkgebied **Vergoedingenbeheer** en niet vanuit het oude werkgebied **Vergoedingen**.
>
> Als u midden in een inschrijvingsjaar overschakelt naar Vergoedingenbeheer, moet u in Vergoedingenbeheer de werknemersgegevens voor het hele jaar correct configureren. Op deze manier zorgt u ervoor dat u nauwkeurige rapporteringsinformatie voor het gehele jaar ontvangt.

## <a name="getting-started"></a>Aan de slag

Om informatie te volgen voor de 1095-formulieren moet u eerst een of meer ACA-dekkingsgroepen maken. In deze groepen wordt de volgende informatie geregistreerd:

- Het dekkingsaanbod dat aan een werknemer is geboden
- Het werknemersdeel van de maandelijkse premie van de laagste kosten als de kosten hoger zijn dan de federale armoedegrens
- Welke Safe Harbor de werkgever gebruikt, indien van toepassing

Met ACA-dekkingsgroepen kunt u deze informatie beheren voor meerdere werknemersrecords met dezelfde voorwaarden. U kunt eenvoudig groepen aan een of meer werknemers toewijzen.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Een ACA-dekkingsgroep maken of bewerken

1. Selecteer in het werkgebied **Vergoedingenbeheer** de optie **ACA-dekkingsgroep**.

    ![Een ACA-dekkingsgroep selecteren](./media/hr-benefits-management-aca-coverage-group.png)

2. Selecteer **Nieuw** om een nieuwe ACA-dekkingsgroep te maken of **Bewerken** om een bestaande groep te wijzigen.

    ![Nieuw of Bewerken selecteren](./media/hr-benefits-management-aca-new.png)

3. Stel de volgende velden in.

    | Veld | Beschrijving |
    |---|---|
    | Naam | Voer een naam voor de groep in. |
    | Beschrijving | Voer een omschrijving in van de groep. |
    | Dekkingsaanbod | De dekking die wordt geboden aan werknemers, hun echtgenoot/echtgenote of partner, en hun afhankelijken (gezinsleden). |
    | Werknemersdeel van kosten | Het bedrag dat voor rekening van de werknemer komt. |
    | Toepasselijke sectie 4980H Safe Harbor | De 4980H-code voor de Safe Harbor of Transition Relief. |
    | Beginmaand van plan | Selecteer de kalendermaand wanneer uw vergoedingsplanjaar begint. |
    | Groep geldig vanaf | De eerste datum waarop deze record geldig is. |
    | Groep geldig tot | De laatste datum waarop deze record geldig is. Voer **Nooit** in als er geen vervaldatum is. |

    ![Een dekkingsgroep maken](./media/hr-benefits-management-aca-new-group.png)

4. Selecteer **Opslaan**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Meerdere werknemers toewijzen aan een ACA-dekkingsgroep

1. Selecteer in het werkgebied **Vergoedingenbeheer** de optie **ACA-dekkingsgroep**.
2. Selecteer de groep waaraan u werknemers wilt toewijzen.
3. Selecteer **Groepsgewijze toewijzing**.

    ![Groepsgewijze toewijzing selecteren](./media/hr-benefits-management-aca-mass-assignment.png)

4. Selecteer werknemers in de lijst en selecteer vervolgens **Toewijzen**.

    ![Geselecteerde werknemers toewijzen aan een groep](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Meerdere versies van dekkingsopties onderhouden

U kunt van elke dekkingsgroep meerdere versies onderhouden. Wanneer er iets wijzigt in uw organisatie of de vergoedingen die worden geboden, kunt u de informatie van de groep up-to-date houden zonder dat u een nieuwe groep moet maken en daar weer werknemers aan moet toewijzen.

Nadat u ACA-dekkingsgroepen gemaakt hebt, kunt u er groepsgewijs werknemers aan toewijzen. U kunt werknemers ook afzonderlijk aan groepen toewijzen en aangeven of ACA-informatie wordt gevolgd en gerapporteerd.

Als u geen ACA-gegevens voor een werknemer hoeft bij te houden en te rapporteren, kunt u de optie **Dekking rapporteren** instellen op **Nee**. Bijvoorbeeld hebt u te maken met parttime werknemers waarvoor geen ACA-rapportage vereist is.

### <a name="override-default-values-for-an-employee"></a>Standaardwaarden voor een werknemer overschrijven

Voor werknemers die zijn toegewezen aan een ACA-dekkingsgroep kunt u de volgende opties wijzigen voor maanden die afwijkende waarden vereisen:

- Dekkingsaanbod
- Werknemersdeel van kosten
- Toepasselijke sectie 4980H Safe Harbor

> [!NOTE]
> Voor ACA-rapporten over 2020 moet u de postcodes van zowel het werkadres als het thuisadres vermelden op formulier 1095-C. Waarden worden automatisch ingevuld op basis van de huidige actieve locaties. Als een van beide locaties gedurende een deel van het jaar anders is, moet u de waarde overschrijven. Het veld **Postcode** (regel 17) van het 1095-C-rapport wordt alleen ingevuld als de code **Dekkingsaanbod** een waarde uit de reeks **1L** tot en met **1Q** bevat, als volgt:
>
> - **1L, 1M of 1N:** de postcode van de primaire woonadres
> - **1O, 1P, 1Q:** de postcode van het primaire werkadres

Voer de volgende stappen uit om uitzonderingen in te voeren voor alle waarden van een ACA-dekkingsgroep.

1. Selecteer in het werkgebied **Personeelsbeheer** de optie **Koppelingen** en selecteer vervolgens **Werknemers**.
2. Selecteer de werknemer in de lijst.
3. Selecteer op het tabblad **Dienstverband**, in de sectie **Meer informatie**, de optie **ACA-dekking**.

    ![Opties voor één werknemer wijzigen](./media/hr-benefits-management-aca-change-single-employee.png)

4. Selecteer **Bewerken**.
5. Schakel het selectievakje **Standaardwaarden overschrijven** in voor elke maand die moet worden gewijzigd en wijzig vervolgens de andere waarden waar nodig.

    ![Standaardwaarden overschrijven](./media/hr-benefits-management-aca-override-default.png)

6. Selecteer **Opslaan**.

## <a name="report-health-care-coverage"></a>Gezondheidszorgdekking rapporteren

U moet iedere door de werkgever gesponsorde zorgdekking uit interne verzekering bijhouden voor fulltime en parttime werknemers. Voeg elke werknemer toe, samen met diens afhankelijken, op het 1095-C-rapport voor de maanden waarin ze dekking kregen.

Volg deze stappen om aan te geven of een vergoedingsplan moet worden gerapporteerd.

1. Selecteer in het werkgebied **Vergoedingenbeheer** de optie **Vergoedingsplannen**.
2. Selecteer het vergoedingsplan waarover u wilt rapporteren.
3. Selecteer **Bewerken**.
4. Stel de optie **Aangegeven onder de Affordable Care Act** in op **Ja**.

    ![Gezondheidszorgdekking rapporteren](./media/hr-benefits-management-aca-report-coverage.png)

5. Selecteer **Opslaan**.

Als een werknemer zorgdekking kiest voor een afhankelijke, wordt de dekkingsperiode van de afhankelijke bepaald door de datum waarop de afhankelijke is ingeschreven of verwijderd. De dekkingsdatums voor een afhankelijke worden automatisch berekend op basis van de periode waarin de afhankelijke gedurende het inschrijvingsjaar in aanmerking komt en actief was in een plan.

## <a name="generate-1095-b-and-1095-c-forms"></a>Formulieren 1095-B en 1095-C genereren

U kunt ook de ACA-formulieren 1095-B en 1095-C genereren in het product en distribueren naar uw werknemers. U kunt ook formulier 1095-C en de bijbehorende 1094-C-verzendbestanden elektronisch genereren om naar de Internal Revenue Service (IRS) te verzenden.

1. Selecteer in het werkgebied **Vergoedingenbeheer** de optie **Formulier ACA 1095-B** of **Formulier ACA 1095-C**.
2. Wijzig waar nodig de parameters en selecteer **OK**.

    > [!NOTE]
    > Als u 1095-C-formulieren voor meer dan 500 werknemers afdrukt, ontvangt u meer dan één PDF-bestand. U wordt aangeraden de waarde van het veld **Maximumbestandsgrootte in megabytes** op de pagina **Parameters voor documentbeheer** te verhogen naar **150**. (Als u die pagina snel wilt openen, kunt u het zoekveld op de navigatiebalk gebruiken.)
    >
    > ![De maximumbestandsgrootte wijzigen](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Als u de status van uw rapporten wilt controleren en weergeven, gebruikt u het zoekveld op de navigatiebalk om de pagina **Elektronische rapportagetaken** te openen.

    ![De pagina Elektronische rapportagetaken zoeken](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Selecteer het rapport dat u wilt weergeven en selecteer vervolgens **Bestanden weergeven**.

    ![Bestanden weergeven](./media/hr-benefits-management-aca-show-files.png)

5. Selecteer **Openen**.

    ![Een bestand openen](./media/hr-benefits-management-aca-open-file.png)

6. Open vanuit de Meldingsbalk die onderin het browservenster wordt weergegeven het zip-bestand en selecteer het rapport. U kunt het PDF-bestand weergeven of afdrukken.

    ![Voorbeeldformulier 1095-C](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>Informatie over ACA-dekking weergeven

Op de pagina **Dekking betaalbare zorg werknemer** wordt de volgende informatie getoond:

- Werknemers die aan alle dekkingsgroepen zijn toegewezen
- Werknemers die niet in een rapport hoeven te worden opgenomen
- Niet-toegewezen werknemers

Voer de volgende stappen uit om deze informatie weer te geven.

1. Selecteer in het werkgebied **Vergoedingenbeheer** de optie **Dekking betaalbare zorg werknemer**.
2. Selecteer een groep in het veld **Groepsnaam**.

    ![ACA-dekking weergeven](./media/hr-benefits-management-aca-view-coverage.png)

Als een van de standaardwaarden van de ACA-dekkingsgroep is overschreven, wordt dit aangegeven met een asterisk naast de gewijzigde waarde. Als de waarden voor alle twaalf maanden hetzelfde zijn en niet zijn overschreven, wordt de waarde weergegeven in de kolom **Alle 12 maanden**.

U kunt werknemers weergeven die zijn gemarkeerd als niet vereist om aan te melden voor de ACA en waarvoor geen Formulier 1095-C vereist is. Selecteer in het veld **Filteren op** de optie **Niet aan te geven onder ACA**.

U kunt werknemers weergeven die niet aan een groep zijn toegewezen of die aan een verlopen groep zijn toegewezen. Selecteer in het veld **Filteren op** de optie **Niet-toegewezen of verlopen groep**.

### <a name="export-to-excel"></a>Exporteren naar Excel

Als u een van de lijsten wilt exporteren naar Microsoft Excel, gaat u als volgt te werk.

1. Selecteer de knop **Openen in Microsoft Office**.
2. Selecteer **HCM Human Resources tijdelijke tabel voor intern gebruik**.
3. Selecteer **Downloaden**.

### <a name="view-aca-reportable-dependents"></a>Onder ACA aan te geven afhankelijken weergeven

Als u gedekte personen moet rapporteren omdat u interne verzekering aanbiedt, kunt u alle afhankelijken weergeven die zijn gedekt door vergoedingsplannen die zijn gemarkeerd als **Aan te geven onder ACA**. Selecteer in het actievenster de optie **Gezinsdekking weergeven**.

![Gezinsdekking weergeven](./media/hr-benefits-management-aca-view-dependent-coverage.png)

De dekkingsinformatie voor de afhankelijken van de werknemer wordt weergegeven.

![Gezinsdekking](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Op de pagina worden alleen vergoedingsplannen weergegeven die zijn gemarkeerd als **Aan te geven onder ACA**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]