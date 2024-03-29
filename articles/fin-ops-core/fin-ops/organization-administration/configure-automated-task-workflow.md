---
title: Geautomatiseerde taken configureren in een workflow
description: In dit artikel wordt uitgelegd hoe u de eigenschappen van een geautomatiseerde taak configureert.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b482338c436ea9226d31f74c823ee1dc141b24cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891748"
---
# <a name="configure-automated-tasks-in-a-workflow"></a>Geautomatiseerde taken configureren in een workflow

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

In dit artikel wordt uitgelegd hoe u de eigenschappen van een geautomatiseerde taak configureert.

Om een geautomatiseerde taak te configureren, klikt u in de workfloweditor met de rechtermuisknop op de taak en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen. Vervolgens kunt u door middel van de volgende procedures de eigenschappen voor de geautomatiseerde taak configureren.

## <a name="name-the-task"></a>Een naam opgeven voor de taak

Voer deze stappen uit om een naam op te geven voor de geautomatiseerde taak.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Geef in het veld **Naam** een unieke naam voor de taak op.

## <a name="specify-when-notifications-are-sent"></a>Opgeven wanneer meldingen worden verzonden

U kunt meldingen naar gebruikers verzenden wanneer een geautomatiseerde taak is uitgevoerd of geannuleerd. Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.

1. Klik in het linkerdeelvenster op **Meldingen**.
2. Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:

    - **Uitvoering**: meldingen worden verzonden wanneer de taak is uitgevoerd.
    - **Geannuleerd**: meldingen worden verzonden wanneer de taak is geannuleerd.

3. Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.
4. Geef op het tabblad **Meldingstekst** de tekst van de melding op.
5. Als u de melding wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de melding aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:

    1. Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.
    2. Klik op **Tijdelijke aanduiding invoegen**.
    3. Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4. Klik op **Invoegen**.

6. Voer de onderstaande stappen uit om vertalingen van de melding toe te voegen:

    1. Klik op **Vertalingen**.
    2. Klik in de pagina die wordt geopend op **Toevoegen**.
    3. Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4. Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5. Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 5.
    6. Klik op **Sluiten**.

7. Geef op het tabblad **Ontvanger** op aan wie de meldingen moeten worden verzonden. Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de betreffende optie voordat u naar stap 8 gaat.

    <table>
    <thead>
    <tr>
    <th>Optie</th>
    <th>Ontvangers van meldingen</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deelnemer</td>
    <td>Gebruikers die aan een specifieke groep of rol zijn toegewezen</td>
    <td>
    <ol>
    <li>Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt laten verzenden.</li>
    <li>Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Werkstroomgebruiker</td>
    <td>Gebruikers die aan de huidige workflow deelnemen</td>
    <td>
    <ul>
    <li>Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Gebruiker</td>
    <td>Specifieke gebruikers</td>
    <td>
    <ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De lijst <strong>Beschikbare gebruikers</strong> bevat alle gebruikers. Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]