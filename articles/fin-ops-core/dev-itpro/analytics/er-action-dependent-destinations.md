---
title: Actieafhankelijke ER-bestemmingen configureren
description: In dit onderwerp wordt uitgelegd hoe actieafhankelijke bestemmingen worden geconfigureerd voor een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.
author: NickSelin
manager: AnnBe
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ea7543fddef085cfd1e92edf0b1dabf6d0aac38a
ms.sourcegitcommit: 5264aaec3723c40a219e4d2867afe1ba9cc5f2a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5153634"
---
# <a name="configure-action-dependent-er-destinations"></a>Actieafhankelijke ER-bestemmingen configureren

[!include [banner](../includes/banner.md)]

U kunt [bestemmingen](electronic-reporting-destinations.md) configureren voor elke uitvoercomponent (map of bestand) van een [Electronic reporting (ER)](general-electronic-reporting.md)-[indeling](general-electronic-reporting.md#FormatComponentOutbound)s[configuratie](general-electronic-reporting.md#Configuration) die wordt gebruikt voor het genereren van uitgaande documenten. Gebruikers die een ER-indeling van dit type uitvoeren en voor wie de juiste toegangsrechten gelden, kunnen ook de geconfigureerde bestemmingsinstellingen wijzigen tijdens runtime.

In Microsoft Dynamics 365 Finance **versie 10.0.17 en hoger** kan een ER-indeling worden uitgevoerd door [levering](er-apis-app10-0-17.md) van een actiecode die de gebruiker uitvoert door die ER-indeling uit te voeren. In de module **Klanten** kunt u bijvoorbeeld in de afdrukbeheerinstellingen een ER-indeling selecteren om een specifiek bedrijfsdocument te genereren, zoals een vrije-tekstfactuur. U kunt vervolgens **Weergeven** selecteren om een voorbeeld van de factuur weer te geven of **Afdrukken** om deze naar een printer te sturen. Als een gebruikersactie wordt doorgegeven voor de lopende ER-indeling tijdens runtime, kunt u verschillende ER-bestemmingen voor verschillende gebruikersacties configureren. In dit onderwerp wordt uitgelegd hoe u ER-bestemmingen voor dit type ER-indeling configureert.

## <a name="make-action-dependent-er-destinations-available"></a>Actieafhankelijke ER-bestemmingen beschikbaar maken

Als u actieafhankelijke ER-bestemmingen in het huidige exemplaar van Finance wilt configureren en de [nieuwe](er-apis-app10-0-17.md) ER API wilt inschakelen, opent u de werkruimte [Functiebeheer](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) en schakelt u de functie **Specifieke ER-bestemmingen configureren om te worden gebruikt voor verschillende PM-acties** in. Als u geconfigureerde ER-bestemmingen voor [specifieke](#reports-list-wave1) rapporten tijdens runtime wilt gebruiken, moet u de functie **Uitvoer van PM-rapporten routeren op basis van ER-bestemmingen die specifiek zijn voor gebruikersacties (wave 1)** inschakelen.

## <a name="configure-action-dependent-er-destinations"></a>Actieafhankelijke ER-bestemmingen configureren

Wanneer u de functie **Specifieke ER-bestemmingen configureren om te worden gebruikt voor verschillende PM-acties** inschakelt, kunt u actieafhankelijke ER-bestemmingen configureren op het sneltabblad **Bestandsbestemming** van de pagina **Bestemming elektronische rapportage**. Voor elk onderdeel kunt u een record toevoegen en specifieke ER-bestemmingen inschakelen. Voor elke record moet u het type document opgeven waar de geconfigureerde ER-bestemmingen op moeten worden toegepast. Selecteer in het veld **Documenttype** een van de volgende waarden:

- Selecteer **Elektronisch** om de geconfigureerde bestemmingen toe te passen als er geen gebruikersactiecode is opgegeven tijdens runtime.
- Selecteer **Afdrukbeheer** om de geconfigureerde bestemmingen toe te passen als er een gebruikersactiecode wordt opgegeven tijdens runtime.
- Selecteer **Elke** om altijd de geconfigureerde bestemmingen toe te passen, ongeacht of er een gebruikersactie wordt opgegeven tijdens runtime.

Als u het documenttype **Afdrukbeheer** selecteert, moet u de gebruikersacties opgeven waarop de geconfigureerde ER-bestemmingen moeten worden toegepast. Selecteer in het veld **Afdrukbeheeractie** een van de volgende waarden:

- Selecteer **Weergeven** om de geconfigureerde bestemmingen toe te passen als de gebruikersactie **Weergeven** tijdens runtime wordt opgegeven.
- Selecteer **Afdrukken** om de geconfigureerde bestemmingen toe te passen als de gebruikersactie **Afdrukken** tijdens runtime wordt opgegeven.
- Selecteer **Verzenden** om de geconfigureerde bestemmingen toe te passen als de gebruikersactie **Verzenden** tijdens runtime wordt opgegeven.

> [!NOTE]
> U kunt meerdere acties selecteren voor één bestemmingsrecord.

Als u het documenttype **Elke** selecteert, wordt **Automatische detectie** automatisch geselecteerd in het veld **Afdrukbeheeractie** als gebruikersactie en gebeurt het volgende:

- Als er geen gebruikersactiecode wordt opgegeven tijdens runtime, worden alle geconfigureerde ER-bestemmingen toegepast.
- Als een gebruikersactiecode wordt opgegeven tijdens runtime, wordt een ER-bestemming toegepast die vooraf is gedefinieerd voor een specifieke actie, **ongeacht of deze is ingeschakeld**:

    - Wanneer de actie **Weergeven** wordt opgegeven tijdens runtime, wordt de ER-bestemming **Scherm** toegepast.
    - Wanneer de actie **Verzenden** wordt opgegeven tijdens runtime, wordt de ER-bestemming **E-mail** toegepast.
    - Wanneer de actie **Afdrukken** wordt opgegeven tijdens runtime, wordt de ER-bestemming **Printer** toegepast.

U kunt bijvoorbeeld de ER-indeling **Vrije-tekstfactuur (Excel)** gebruiken om een [vrije-tekstfactuur](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new) af te drukken wanneer u deze boekt. Als u een gegenereerd document wilt routeren, moet u ER-bestemmingen configureren voor deze ER-indeling. U moet bijvoorbeeld mogelijk deze ER-bestemmingen configureren om het volgende uit te voeren voor een gegenereerd document:

- Het document archiveren als de ER-indeling wordt uitgevoerd, maar er geen actiecode is opgegeven (bijvoorbeeld wanneer het document elektronisch wordt verzonden).
- Een voorbeeld van het document weergeven in een webbrowser wanneer een gebruiker de actie **Weergeven** uitvoert.
- Het document archiveren en afdrukken wanneer een gebruiker de actie **Afdrukken** uitvoert.
- Het document archiveren en per e-mail verzenden als bijlage van een uitgaand e-mailbericht wanneer een gebruiker de actie **Verzenden** uitvoert.

In de volgende afbeelding wordt getoond hoe u het configureren van deze ER-bestemmingen kunt bereiken als de set afzonderlijke bestemmingsrecords wanneer elke record wordt geconfigureerd voor een afzonderlijke gebruikersactie:

![Pagina voor elektronische rapportagebestemming met actieafhankelijke bestemmingsinstellingen voor een ER-indeling wanneer elke bestemmingsrecord wordt geconfigureerd voor één gebruikersactie](./media/er-destination-action-dependent-01.png)

In de volgende afbeelding wordt getoond hoe u het alternatieve configureren van deze ER-bestemmingen kunt bereiken als de set afzonderlijke bestemmingsrecords wanneer elke record wordt geconfigureerd voor een afzonderlijke bestemming:

![Pagina voor elektronische rapportagebestemming met actieafhankelijke bestemmingsinstellingen voor een ER-indeling wanneer elke bestemmingsrecord wordt geconfigureerd voor één bestemming](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Als een actiecode wordt opgegeven voor de lopende ER-indeling maar er geen bestemmingen zijn geconfigureerd voor die actiecode, wordt het [standaard](electronic-reporting-destinations.md#default-behavior)bestemmingsgedrag toegepast.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Actieafhankelijke ER-bestemmingen tijdens runtime wijzigen

Wanneer er een ER-indeling wordt uitgevoerd en er gebruikersacties zijn opgegeven door gebruikers die de juiste [machtigingen](electronic-reporting-destinations.md#security-considerations) hebben om geconfigureerde bestemmingsinstellingen tijdens runtime te wijzigen, wordt een dialoogvenster weergegeven dat de optie biedt om de geconfigureerde bestemmingsinstellingen te wijzigen. Dit dialoogvenster is optioneel en heeft een uiterlijk dat afhankelijk is van hoe de oproep waarmee het ER-framework wordt uitgevoerd, een ER-indeling implementeert. Als dit dialoogvenster wordt weergegeven, worden de ER-bestemmingen in het dialoogvenster ingeschakeld op basis van de geleverde gebruikersactie.

Hieronder ziet u een voorbeeld van het dialoogvenster **Bestemming van indeling voor elektronische rapportage** dat wordt weergegeven wanneer er een vrije-tekstfactuur wordt [geboekt](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new) en de ER-indeling **Vrije-tekstfactuur** wordt uitgevoerd om dit document te genereren, als de actie **Printer** is opgegeven en ER-bestemmingen voor deze indeling zijn geconfigureerd, zoals eerder in dit onderwerp is beschreven.

![Dialoogvenster met de mogelijkheid om de oorspronkelijk geconfigureerde ER-bestemmingen te wijzigen voor de lopende ER-indeling](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Als u ER-bestemmingen hebt geconfigureerd voor verschillende onderdelen van de lopende ER-indeling, wordt er voor elk geconfigureerd onderdeel van de ER-indeling afzonderlijk een optie aangeboden.

## <a name="verify-the-provided-user-action"></a>De geleverde gebruikersactie controleren

U kunt nagaan welke gebruikersactie is opgegeven voor de lopende ER-indeling wanneer u een specifieke gebruikersactie voert. Dit is belangrijk wanneer u actieafhankelijke ER-bestemmingen moet configureren, maar u niet weet welke gebruikersactiecode er is opgegeven. Als u bijvoorbeeld een vrije-tekstfactuur begint te boeken en de optie **Factuur afdrukken** instelt op **Ja** in het dialoogvenster **Vrije-tekstfactuur boeken**, kunt u de optie **Doel van afdrukbeheer gebruiken** instellen op **Ja** of **Nee**.

Volg deze stappen om de opgegeven gebruikersactiecode te controleren.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. In het dialoogvenster **Gebruikersparameters** [stelt](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) u de optie **Uitvoeren in foutoplossingsmodus** in op **Ja**.
4. Voer een gebruikersactie uit door een ER-indeling uit te voeren. Houd er rekening mee dat ER-gebruikersparameter specifiek zijn voor de gebruiker en specifiek voor het bedrijf.
5. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Foutopsporingslogboeken voor configuraties**.
6. Filter op de pagina **Foutopsporingslogboeken voor configuraties** de ER-uitvoeringslogboeken om het logboek voor de uitvoering van uw ER-indeling te zoeken.
7. Controleer de logboekgegevens die de record moeten bevatten die de geleverde gebruikersactiecode vertegenwoordigt, als er een actie is geleverd voor de ER-indelingsuitvoering.

    ![Pagina Elektronische uitvoeringslogboeken die informatie bevat over de gebruikersactiecode die is opgegeven voor de gefilterde uitvoering van een ER-indeling](./media/er-destination-action-dependent-03.png)

## <a name=""></a><a name="reports-list-wave1">Lijst met bedrijfsdocumenten (wave 1)</a>

De volgende lijst met bedrijfsdocumenten wordt bepaald door de functie **Uitvoer van PM-rapporten routeren op basis van ER-bestemmingen die specifiek zijn voor gebruikersacties (wave 1)**:

- Klantfactuur (vrije-tekstfactuur)
- Klantfactuur (verkoopfactuur)
- Inkooporder
- Inkooporder inkooponderzoek
- Bevestiging verkooporder
- Notitie bij aanmaning
- Klantrekeningoverzicht
- Rentenota
- Advies leveranciersbetaling
- Offerteaanvraag

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)

[Wijzigingen in API voor raamwerk voor elektronische rapportage in Application update 10.0.17](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]