---
title: Een geautomatiseerde taak configureren in een workflow
description: In dit onderwerp wordt uitgelegd hoe u de eigenschappen van een geautomatiseerde taak configureert.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 56e29bd2e875b8bb729e5dfe0c5ac03fc997ecbe
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a>Een geautomatiseerde taak configureren in een workflow

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u de eigenschappen van een geautomatiseerde taak configureert.

Om een geautomatiseerde taak te configureren, klikt u in de workfloweditor met de rechtermuisknop op de taak en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen. Vervolgens kunt u door middel van de volgende procedures de eigenschappen voor de geautomatiseerde taak configureren.

## <a name="name-the-task"></a>Een naam opgeven voor de taak
Voer deze stappen uit om een naam op te geven voor de geautomatiseerde taak.

1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Geef in het veld **Naam** een unieke naam voor de taak op.

## <a name="specify-when-notifications-are-sent"></a>Opgeven wanneer meldingen worden verzonden
U kunt meldingen naar gebruikers verzenden wanneer een geautomatiseerde taak is uitgevoerd of geannuleerd. Volg deze stappen om op te geven wanneer meldingen moeten worden verzonden en naar wie de meldingen worden verzonden.

1.  Klik in het linkerdeelvenster op **Meldingen**.
2.  Schakel het selectievakje naast de gebeurtenissen waarvoor meldingen moeten worden verzonden:
    -   **Uitvoering**: meldingen worden verzonden wanneer de taak is uitgevoerd.
    -   **Geannuleerd**: meldingen worden verzonden wanneer de taak is geannuleerd.

3.  Selecteer de rij voor een gebeurtenis die u in stap 2 hebt geselecteerd.
4.  Geef op het tabblad **Meldingstekst** de tekst van de melding op.
5.  Als u de melding wilt personaliseren, kunt u tijdelijke aanduidingen invoegen. Wanneer de melding aan de gebruiker wordt getoond, worden tijdelijke aanduidingen vervangen door de juiste gegevens. Volg deze stappen om een tijdelijke aanduiding in te voegen:
    1.  Klik in het tekstvak op de plek waar u de tijdelijke aanduiding wilt plaatsen.
    2.  Klik op **Tijdelijke aanduiding invoegen**.
    3.  Selecteer in de lijst die wordt geopend de tijdelijke aanduiding die u wilt invoegen.
    4.  Klik op **Invoegen**.

6.  Voer de onderstaande stappen uit om vertalingen van de melding toe te voegen:
    1.  Klik op **Vertalingen**.
    2.  Klik in de pagina die wordt geopend op **Toevoegen**.
    3.  Selecteer in de lijst die wordt geopend de taal waarin u de tekst wilt invoeren.
    4.  Voer in het veld **Vertaalde tekst** de gewenste tekst in.
    5.  Als u de tekst wilt personaliseren, kunt u tijdelijke aanduidingen invoegen volgens de beschrijving in stap 5.
    6.  Klik op **Sluiten**.

7.  Geef op het tabblad **Ontvanger** op aan wie de meldingen moeten worden verzonden. Selecteer een van de opties in de volgende tabel en vervolg de bijkomende stappen voor de betreffende optie voordat u naar stap 8 gaat.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Optie</th>
    <th>Ontvangers van meldingen</th>
    <th>Bijkomende stappen</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Deelnemer</td>
    <td>Gebruikers die aan een specifieke groep of rol zijn toegewezen</td>
    <td><ol>
    <li>Selecteer op het tabblad <strong>Op rol gebaseerd</strong> de optie <strong>Deelnemer</strong> en selecteer vervolgens in de lijst <strong>Type deelnemer</strong> het type groep of rol waarnaar u meldingen wilt laten verzenden.</li>
    <li>Selecteer in de lijst <strong>Deelnemer</strong> de groep of rol waarnaar u meldingen wilt verzenden.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Werkstroomgebruiker</td>
    <td>Gebruikers die aan de huidige workflow deelnemen</td>
    <td><ul>
    <li>Selecteer op het tabblad <strong>Workflowgebruiker</strong> de optie <strong>Workflowgebruiker</strong>. Selecteer dan in de lijst <strong>Workflowgebruiker</strong> een gebruiker die aan de workflow deelneemt.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Gebruiker</td>
    <td>Specifieke Microsoft Dynamics 365 for Finance and Operations-gebruikers</td>
    <td><ol>
    <li>Selecteer <strong>Gebruiker</strong> en klik op het tabblad <strong>Gebruiker</strong>.</li>
    <li>De lijst <strong>Beschikbare gebruikers</strong> bevat alle Finance and Operations-gebruikers. Selecteer de gebruikers naar wie u meldingen wilt verzenden en verplaats deze gebruikers naar de lijst <strong>Geselecteerde gebruikers</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Herhaal stappen 3 tot en met 7 voor elke gebeurtenis die u in stap 2 hebt geselecteerd.





