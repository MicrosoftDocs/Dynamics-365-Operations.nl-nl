---
title: Actieafhankelijke ER-bestemmingen configureren
description: In dit artikel wordt uitgelegd hoe actieafhankelijke bestemmingen worden geconfigureerd voor een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.
author: kfend
ms.date: 12/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 80a432a431891c02e4bf5c71cfe2bd9642c41c75
ms.sourcegitcommit: e9000d0716f7fa45175b03477c533a9df2bfe96d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/13/2022
ms.locfileid: "9843792"
---
# <a name="configure-action-dependent-er-destinations"></a>Actieafhankelijke ER-bestemmingen configureren

[!include [banner](../includes/banner.md)]

U kunt [bestemmingen](electronic-reporting-destinations.md) configureren voor elke uitvoercomponent (map of bestand) van een [Electronic reporting (ER)](general-electronic-reporting.md)-indelings[configuratie](general-electronic-reporting.md#Configuration) die wordt gebruikt voor het genereren van uitgaande documenten. Gebruikers die een ER-indeling van dit type uitvoeren en voor wie de juiste toegangsrechten gelden, kunnen ook de geconfigureerde bestemmingsinstellingen wijzigen tijdens runtime.

In Microsoft Dynamics 365 Finance **versie 10.0.17 en hoger** kan een ER-indeling worden uitgevoerd door [levering](er-apis-app10-0-17.md) van een actiecode die de gebruiker uitvoert door die ER-indeling uit te voeren. In de module **Klanten** kunt u bijvoorbeeld in de afdrukbeheerinstellingen een ER-indeling selecteren om een specifiek bedrijfsdocument te genereren, zoals een vrije-tekstfactuur. U kunt vervolgens **Weergeven** selecteren om een voorbeeld van de factuur weer te geven of **Afdrukken** om deze naar een printer te sturen. Als een gebruikersactie wordt doorgegeven voor de lopende ER-indeling tijdens runtime, kunt u verschillende ER-bestemmingen voor verschillende gebruikersacties configureren. In dit artikel wordt uitgelegd hoe u ER-bestemmingen voor dit type ER-indeling configureert.

## <a name="make-action-dependent-er-destinations-available"></a>Actieafhankelijke ER-bestemmingen beschikbaar maken

Als u actieafhankelijke ER-bestemmingen in het huidige exemplaar van Finance wilt configureren en de [nieuwe](er-apis-app10-0-17.md) ER API wilt inschakelen, opent u de werkruimte [Functiebeheer](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) en schakelt u de functie **Specifieke ER-bestemmingen configureren om te worden gebruikt voor verschillende PM-acties** in. Als u geconfigureerde ER-bestemmingen voor rapporten tijdens runtime wilt gebruiken, schakelt u de functie **Uitvoer van PM-rapporten routeren op basis van ER-bestemmingen die specifiek zijn voor gebruikersacties (wave 1)** in.

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

U kunt bijvoorbeeld de ER-indeling **Vrije-tekstfactuur (Excel)** gebruiken om een [vrije-tekstfactuur](../../../finance/accounts-receivable/create-free-text-invoice-new.md) af te drukken wanneer u deze boekt. Als u een gegenereerd document wilt routeren, moet u ER-bestemmingen configureren voor deze ER-indeling. U moet bijvoorbeeld mogelijk deze ER-bestemmingen configureren om het volgende uit te voeren voor een gegenereerd document:

- Het document archiveren als de ER-indeling wordt uitgevoerd, maar er geen actiecode is opgegeven (bijvoorbeeld wanneer het document elektronisch wordt verzonden).
- Een voorbeeld van het document weergeven in een webbrowser wanneer een gebruiker de actie **Weergeven** uitvoert.
- Het document archiveren en afdrukken wanneer een gebruiker de actie **Afdrukken** uitvoert.
- Het document archiveren en per e-mail verzenden als bijlage van een uitgaand e-mailbericht wanneer een gebruiker de actie **Verzenden** uitvoert.

In de volgende afbeelding wordt getoond hoe u het configureren van deze ER-bestemmingen kunt bereiken als de set afzonderlijke bestemmingsrecords wanneer elke record wordt geconfigureerd voor een afzonderlijke gebruikersactie:

![Pagina voor elektronische rapportagebestemming met actieafhankelijke bestemmingsinstellingen voor een ER-indeling wanneer elke bestemmingsrecord wordt geconfigureerd voor één gebruikersactie.](./media/er-destination-action-dependent-01.png)

In de volgende afbeelding wordt getoond hoe u het alternatieve configureren van deze ER-bestemmingen kunt bereiken als de set afzonderlijke bestemmingsrecords wanneer elke record wordt geconfigureerd voor een afzonderlijke bestemming:

![Pagina voor elektronische rapportagebestemming met actieafhankelijke bestemmingsinstellingen voor een ER-indeling wanneer elke bestemmingsrecord wordt geconfigureerd voor één bestemming.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Als een actiecode wordt opgegeven voor de lopende ER-indeling maar er geen bestemmingen zijn geconfigureerd voor die actiecode, wordt het [standaard](electronic-reporting-destinations.md#default-behavior)bestemmingsgedrag toegepast.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Actieafhankelijke ER-bestemmingen tijdens runtime wijzigen

Wanneer er een ER-indeling wordt uitgevoerd en er gebruikersacties zijn opgegeven door gebruikers die de juiste [machtigingen](electronic-reporting-destinations.md#security-considerations) hebben om geconfigureerde bestemmingsinstellingen tijdens runtime te wijzigen, wordt een dialoogvenster weergegeven dat de optie biedt om de geconfigureerde bestemmingsinstellingen te wijzigen. Dit dialoogvenster is optioneel en heeft een uiterlijk dat afhankelijk is van hoe de oproep waarmee het ER-framework wordt uitgevoerd, een ER-indeling implementeert. Als dit dialoogvenster wordt weergegeven, worden de ER-bestemmingen in het dialoogvenster ingeschakeld op basis van de geleverde gebruikersactie.

Hieronder ziet u een voorbeeld van het dialoogvenster **Bestemming van indeling voor elektronische rapportage** dat wordt weergegeven wanneer er een vrije-tekstfactuur wordt [geboekt](../../../finance/accounts-receivable/create-free-text-invoice-new.md) en de ER-indeling **Vrije-tekstfactuur** wordt uitgevoerd om dit document te genereren, als de actie **Printer** is opgegeven en ER-bestemmingen voor deze indeling zijn geconfigureerd, zoals eerder in dit artikel is beschreven.

![Dialoogvenster met de mogelijkheid om de oorspronkelijk geconfigureerde ER-bestemmingen te wijzigen voor de lopende ER-indeling.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Als u ER-bestemmingen hebt geconfigureerd voor verschillende onderdelen van de lopende ER-indeling, wordt er voor elk geconfigureerd onderdeel van de ER-indeling afzonderlijk een optie aangeboden.

Als verschillende ER-indelingen van toepassing zijn als rapportsjablonen voor het geselecteerde document, worden alle ER-bestemmingen voor alle toepasselijke ER-rapportsjablonen weergegeven in het dialoogvenster en beschikbaar voor handmatige correctie tijdens runtime.

Als er geen [SSRS-rapportsjablonen (SQL Server Reporting Services)](SSRS-report.md) van toepassing zijn op het geselecteerde document, is de standaardselectie van afdrukbeheerbestemmingen dynamisch verborgen.

Vanaf Finance versie **10.0.31** kunt u de toegewezen ER-bestemmingen tijdens runtime handmatig wijzigen voor de volgende bedrijfsdocumenten:

- Klantrekeningoverzicht
- Rentenota
- Notitie bij aanmaning
- Betalingsadvies voor klant
- Betalingsadvies voor leverancier

Als u de mogelijkheid wilt activeren om ER-bestemmingen tijdens runtime te wijzigen, moet u de functie **ER-bestemmingen bij runtime** in de [Functiebeheer](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace)-werkruimte inschakelen.

> [!IMPORTANT]
> Voor de rapporten **Betalingsadvies voor klant** en **Betalingsadvies voor leverancier** is de mogelijkheid om ER-bestemmingen handmatig te wijzigen alleen beschikbaar als de **ForcePrintJobSettings**-flight is ingeschakeld.

[![ER-bestemmingen aanpassen tijdens runtime.](./media/ERdestinaiotnChangeUI.jpg)](./media/ERdestinaiotnChangeUI.jpg)

> [!NOTE]
> Wanneer de optie **Doel van afdrukbeheer gebruiken** op **Ja** is ingesteld, gebruikt het systeem de standaardbestemmingen voor ER die zijn geconfigureerd voor specifieke ER-rapporten. Alle handmatige wijzigingen die in het dialoogvenster worden aangebracht, worden genegeerd. Stel de optie **Doel van afdrukbeheer gebruiken** in op **Nee** om documenten te verwerken op de ER-bestemmingen die in het dialoogvenster zijn gedefinieerd onmiddellijk voordat u de rapporten gaat uitvoeren.

Voor de volgende bedrijfsdocumenten wordt niet aangenomen dat ze expliciet door de gebruiker zijn geselecteerd wanneer ze worden uitgevoerd:

- Klantrekeningoverzicht
- Rentenota
- Notitie bij aanmaning
- Betalingsadvies voor klant
- Betalingsadvies voor leverancier

De volgende logica wordt gebruikt om te bepalen welke actie wordt gebruikt terwijl de voorgaande rapporten worden verwerkt:

- Als de **ForcePrintJobSettings**-vlucht is ingeschakeld:

    - Als de optie **Doel van afdrukbeheer gebruiken** is ingesteld op **Ja**, wordt de actie **Afdrukken** gebruikt.
    - Als de optie **Doel van afdrukbeheer gebruiken** is ingesteld op **Nee**, wordt de actie **Weergeven** gebruikt.

- Als de **ForcePrintJobSettings**-flight niet is ingeschakeld:

    - Als de optie **Doel van afdrukbeheer gebruiken** is ingesteld op **Ja**, wordt de actie **Afdrukken** gebruikt voor de rapporten **Betalingsadvies voor klant** en **Betalingsadvies voor leverancier**.
    - Als de optie **Doel van afdrukbeheer gebruiken** op **Nee** is ingesteld, wordt de standaardsjabloon voor SSRS-rapporten altijd gebruikt voor de rapporten **Betalingsadvies voor klant** en het **Betalingsadvies voor leverancier**, ongeacht de ER-instellingen die zijn geconfigureerd.
    - De actie **Afdrukken** wordt altijd gebruikt voor de rapporten **Klantrekeningoverzicht**, **Rentenota** en **Notitie bij aanmaning**.

Voor de voorgaande logica kan de actie **Afdrukken** of de actie **Weergeven** worden gebruikt om actieafhankelijke ER-rapportbestemmingen te configureren. Tijdens runtime worden alleen ER-bestemmingen die voor een specifieke actie zijn geconfigureerd, in het dialoogvenster gefilterd.

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

    ![Pagina Elektronische uitvoeringslogboeken die informatie bevat over de gebruikersactiecode die is opgegeven voor de gefilterde uitvoering van een ER-indeling.](./media/er-destination-action-dependent-03.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)

[Wijzigingen in API voor raamwerk voor elektronische rapportage in Application update 10.0.17](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
