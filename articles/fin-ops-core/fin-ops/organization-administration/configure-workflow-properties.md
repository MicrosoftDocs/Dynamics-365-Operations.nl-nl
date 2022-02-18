---
title: Workfloweigenschappen configureren
description: In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een workflow configureert.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81f73f187f75e40297f1f8462e9fff58a309f7f0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069243"
---
# <a name="configure-workflow-properties"></a>Workfloweigenschappen configureren

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

In dit onderwerp wordt uitgelegd hoe u de verschillende eigenschappen van een workflow configureert.

Open de workflow in de workfloweditor om de eigenschappen van een specifiek workflowelement te configureren. Klik op het tekenpapier van de workfloweditor en klik op **Eigenschappen** om de pagina **Eigenschappen** te openen. Met behulp van de volgende procedures kunt u de verschillende eigenschappen van de workflow configureren.

## <a name="name-the-workflow"></a>Naam voor de workflow opgeven

Voer deze stappen uit om een naam op te geven voor de workflow.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Geef in het veld **Naam** een unieke naam voor de workflow op. Als u bijvoorbeeld een workflow voor opdrachten tot inkoop maakt voor elk land of elke regio waarin uw bedrijf actief is, kunt u als naam voor de workflow **Inkoopbestelopdrachten Denemarken** of **Inkoopbestelopdrachten Spanje** opgeven.

## <a name="specify-the-workflow-owner"></a>Eigenaar van de workflow opgeven

De eigenaar van de workflow is degene die deze workflow beheert en onderhoudt. Voer de volgende stappen uit om de eigenaar van de workflow op te geven.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Selecteer in de lijst **Eigenaar** de naam van degene die de workflow beheert.

## <a name="select-an-email-template"></a>Een e-mailsjabloon selecteren

Volg deze stappen om de e-mailsjabloon te selecteren die wordt gebruikt om meldingen te genereren voor deze workflow.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Selecteer in de lijst **E-mailsjabloon voor workflowmeldingen** de gewenste sjabloon.

## <a name="enter-instructions-for-users"></a>Instructies voor gebruikers opgeven

Het is mogelijk om instructies op te geven voor gebruikers die documenten voor verwerking en goedkeuring indienen. Deze gebruikers worden ook wel aangeduid als *opdrachtgevers*. Stel dat u een workflow voor inkoopbestelopdrachten voor Spanje maakt en instructies invoert. Deze instructies kunnen vervolgens door gebruikers worden bekeken die inkoopopdrachten invoeren op de pagina **Opdrachten tot inkoop**. De starter klikt op het pictogram op de berichtenbalk om instructies weer te geven. Voer de volgende stappen uit om instructies voor gebruikers op te geven.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Voer in het veld **Indieningsinstructies** de instructies in.
3. Als u de instructies wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de instructies aan gebruikers worden getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:

    1. Klik in het veld **Indieningsinstructies** om op te geven waar de tijdelijke aanduiding moet verschijnen.
    2. Klik op **Tijdelijke aanduiding invoegen**.
    3. Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4. Klik op **Invoegen**.

4. Voer de onderstaande stappen uit om vertalingen van de instructies toe te voegen:

    1. Klik op **Vertalingen**.
    2. Klik in de pagina die wordt geopend op **Toevoegen**.
    3. Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4. Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5. Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Zie de stap 3 voor instructies voor het invoeren van een tijdelijke aanduiding.
    6. Klik op **Sluiten**.

> [!NOTE]
> Tijdelijke aanduidingen kunnen niet worden toegevoegd met kopiëren en plakken, omdat de doelgegevens niet op de juiste manier worden geplakt. Gebruik de interface om tijdelijke aanduidingen toe te voegen.

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a>Geef op wanneer deze workflow wordt gebruikt via activeringsvoorwaarden

Het is mogelijk om op basis van hetzelfde workflowtype meerdere workflows te maken. Als u meerdere workflows op hetzelfde type hebt gebaseerd, moet u voor elke workflow opgeven wanneer deze wordt gebruikt met activeringsvoorwaarden. Als niet aan de activeringsvoorwaarden wordt voldaan, wordt de standaardworkflow gebruikt. Als er slechts één workflowconfiguratie is gedefinieerd voor een workflowtype, wordt die workflowconfiguratie gebruikt, ongeacht de activeringsvoorwaarden.

U kunt bijvoorbeeld een workflow voor opdrachten tot inkoop maken voor elk land of elke regio waarin uw bedrijf actief is, zoals Inkoopbestelopdrachten Denemarken en Inkoopbestelopdrachten Spanje, met de volgende voorwaarden:

- Opdrachten tot inkoop Denemarken wordt gebruikt als: land/regio = DK
- Opdrachten tot inkoop Spanje wordt gebruikt als: land/regio = ES.

Voer de volgende stappen uit om op te geven wanneer de workflow die u configureert, wordt gebruikt.

1. Klik in het linkerdeelvenster op **Activering**.
2. Schakel het selectievakje **De voorwaarden voor het uitvoeren van deze workflow instellen** in.
3. Klik op **Voorwaarde toevoegen**.
4. Een voorwaarde invoeren.
5. Geef desgewenst vereiste extra voorwaarden op.
6. Voer de workflow uit met een aantal doelrecords om te controleren of de voorwaarde op de juiste manier records opneemt en uitsluit.

## <a name="specify-when-notifications-are-sent"></a>Opgeven wanneer meldingen worden verzonden

Als een document wordt ingediend voor verwerking, wordt een workflowexemplaar gemaakt. Het is mogelijk om meldingen aan gebruikers te verzenden wanneer workflowexemplaren op basis van de workflow worden gestart, voltooid, beëindigd of gestopt vanwege een fout. Voer de volgende stappen uit om op te geven wanneer meldingen worden verzonden.

1. Klik in het linkerdeelvenster op **Meldingen**.
2. Vink het selectievakje aan voor elke gebeurtenis die meldingen moet activeren:

    - **Gestart**: meldingen verzenden wanneer een workflowexemplaar wordt gestart.
    - **Gestopt**: meldingen verzenden wanneer een workflowexemplaar wordt gestopt vanwege een fout.
    - **Voltooid**: meldingen verzenden wanneer een workflowexemplaar is voltooid.
    - **Onherstelbaar**: meldingen verzenden wanneer een workflowexemplaar wordt gestopt vanwege een onherstelbare fout.
    - **Beëindigd**: meldingen verzenden wanneer een workflowexemplaar is beëindigd.

3. Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.
4. Geef op het tabblad **Meldingstekst** de tekst van de melding op.
5. Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de tekst aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:

    1. Klik in het veld om op te geven waar de tijdelijke aanduiding moet verschijnen.
    2. Klik op **Tijdelijke aanduiding invoegen**.
    3. Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4. Klik op **Invoegen**.
    5. Een algemene tijdelijke aanduiding **meldingstekst** om op te nemen is 'Laatste notities: %Workflow.Last note%', waarmee alle opmerkingen uit de vorige stap worden weergegeven.

6. Voer de onderstaande stappen uit om vertalingen van de tekst toe te voegen:

    1. Klik op **Vertalingen**.
    2. Klik in de pagina die wordt geopend op **Toevoegen**.
    3. Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4. Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5. Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Zie de stap 5 voor instructies voor het invoeren van een tijdelijke aanduiding.
    6. Klik op **Sluiten**.

7. Geef met de volgende opties op het tabblad **Ontvanger** op wie de meldingen moet ontvangen.

    <table>
    <thead>
    <tr>
    <th>Optie</th>
    <th>Meldingen worden verzend naar deze gebruikers</th>
    <th>Voer de volgende stappen uit meldingen te laten verzenden.</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deelnemer</td>
    <td>Gebruikers die aan een specifieke groep of rol zijn toegewezen</td>
    <td>
    <ol>
    <li>Klik op het tabblad <strong>Ontvanger</strong> op <strong>Deelnemer</strong>.</li>
    <li>Selecteer op het tabblad <strong>Op rol gebaseerd</strong> in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt verzenden.</li>
    <li>Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Werkstroomgebruiker</td>
    <td>Gebruikers die deelnemers zijn in deze workflow</td>
    <td>
    <ol>
    <li>Klik op het tabblad <strong>Ontvanger</strong> op <strong>Workflowgebruiker</strong>.</li>
    <li>Selecteer op het tabblad <strong>Workflowgebruiker</strong> in de lijst <strong>Workflowgebruiker</strong> een deelnemer aan deze workflow.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Gebruiker</td>
    <td>Specifieke gebruikers</td>
    <td>
    <ol>
    <li>Klik op het tabblad <strong>Ontvanger</strong> op <strong>Gebruiker</strong>.</li>
    <li>Op het tabblad <strong>Gebruiker</strong> bevat de lijst <strong>Beschikbare gebruikers</strong> alle gebruikers. Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Ppmerkingen invoeren over de wijzigingen die u in de workflow hebt aangebracht

Voer de volgende stappen uit om opmerkingen in te voeren over de wijzigingen die u in deze workflow hebt aangebracht.

1. Klik in het linkerdeelvenster op **Opmerkingen**.
2. Voer in het veld **Opmerkingen over de workflow invoeren** uw opmerkingen in.
3. Uw opmerkingen controleren. Nadat u opmerkingen hebt toegevoegd, kunt u deze niet meer wijzigen.
4. Klik op **Toevoegen** om uw opmerkingen aan het gebied **Opmerkingshistorie** toe te voegen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]