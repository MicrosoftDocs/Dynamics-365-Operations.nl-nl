---
title: De boekhoudings- of aangiftevaluta wijzigen
description: In dit onderwerp wordt uitgelegd hoe u de boekhoudings- of aangiftevaluta wijzigt of een aangiftevaluta toevoegt aan de instellingen van een grootboek.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 38b2cdb618d92dca7909a145e7fc07ddfc5f4d45
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017050"
---
# <a name="change-the-accounting-or-reporting-currency"></a>De boekhoudings- of aangiftevaluta wijzigen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de boekhoudings- of aangiftevaluta wijzigt of een aangiftevaluta toevoegt aan de instellingen van een grootboek.

## <a name="symptom"></a>Symptoom

U wilt de boekhoudings- of aangiftevaluta wijzigen of een aangiftevaluta toevoegen aan de grootboekinstellingen. Dit gebeurt doorgaans in de volgende scenario's:

- Bij het instellen van een rechtspersoon is niet de juiste boekhoudings- of aangiftevaluta opgegeven. U wilt die valuta nu wijzigen.
- Bij het instellen van een rechtspersoon is geen aangiftevaluta opgegeven (een aangiftevaluta is optioneel). U wilt nu een aangiftevaluta toevoegen.

Een organisatie die de functie voor twee valuta's eerder niet gebruikte, wil hier nu mee beginnen. Dit probleem doet zich doorgaans voor in de volgende scenario's.

- Er is een aangiftevaluta opgegeven toen een rechtspersoon werd ingesteld, maar de organisatie wil de aangiftevaluta nu verwijderen.
- De organisatie is aan het upgraden of migreren naar Microsoft Dynamics 365 Finance en wil de boekhoudings- of aangiftevaluta wijzigen.

## <a name="resolution"></a>Oplossing

Bepaal eerst of er transacties (werkelijk of budget) in de rechtspersoon zijn geboekt voor de grootboekinstellingen. **U kunt de boekhoudings- of aangiftevaluta niet wijzigen of een aangiftevaluta toevoegen als er transacties (werkelijk of budget) in de rechtspersoon zijn geboekt.** Voer de stappen in een van de volgende secties uit, afhankelijk van of er transacties zijn geboekt.

### <a name="no-transactions-have-been-posted"></a>Er zijn geen transacties geboekt

1. Ga in de rechtspersoon waarvoor u valuta's bijwerkt naar **Grootboek \> Grootboekinstellingen \> Grootboek**.
2. Selecteer **Bewerken** op de pagina **Grootboek**.
3. Selecteer op het sneltabblad **Valuta** de boekhoudings- en aangiftevaluta die u voor de rechtspersoon wilt gebruiken.
4. Selecteer **Opslaan**.

Als de velden voor de boekhoudings- en aangiftevaluta niet beschikbaar zijn op de pagina **Grootboek**, zijn een of meer transacties (werkelijk of budget) geboekt in de rechtspersoon. Daarom kunnen de valuta's niet worden gewijzigd. Voer in dit geval de stappen in de volgende sectie uit.

### <a name="transactions-have-been-posted"></a>Er zijn transacties geboekt

**Als er transacties in de rechtspersoon zijn geboekt, kunt u alleen boekhoudings- of aangiftevaluta wijzigen of toevoegen door een nieuwe rechtspersoon met de juiste valuta's te maken.** Om dit proces gemakkelijker te maken, kunt u met Gegevensbeheer in het systeem instellingsrecords en hoofdrecords van de huidige rechtspersoon naar een nieuwe rechtspersoon kopiëren.

Wijzigingen in de boekhoudings- en aangiftevaluta's worden overal doorgevoerd. Ze hebben niet alleen invloed op het grootboek, maar ook op elk subgrootboek (Klanten, Leveranciers, Voorraad, Project, enzovoort), alle ISV-oplossingen en elke uitbreiding die u hebt gemaakt waarin bedragen worden opgeslagen.

Het proces van het vinden en vertalen van elk bedrag naar een andere valuta is onderhevig aan fouten. Daarom keurt het engineeringteam geen scripts goed waarmee boekhoudings- en aangiftevaluta's worden gewijzigd of toegevoegd. Voor Microsoft Dynamics AX 2012 was wel een hulpprogramma beschikbaar waarmee u boekhoudings- en aangiftevaluta's kon wijzigen of toevoegen, maar dit programma werd afgeschaft voor AX 2012 R3 en Finance.

Voer de volgende stappen uit om de instellings- en hoofdgegevens uit de huidige rechtspersoon naar een nieuwe rechtspersoon te kopiëren.

1. Ga naar **Werkruimten \> Gegevensbeheer**.
2. Selecteer **Sjablonen** onder de groep **Importeren/exporteren**.
3. Zorg ervoor dat er sjablonen beschikbaar zijn. Als er geen sjablonen beschikbaar zijn, selecteert u **Standaardsjablonen laden** en wacht u tot de sjablonen zijn gegenereerd.
4. Keer terug naar het werkgebied **Gegevensbeheer**.
5. Selecteer **Kopiëren naar rechtspersoon**.
6. Voer een groepsnaam en -omschrijving in.
7. Selecteer in het veld **Bronbedrijf** de rechtspersoon waaruit u gegevens wilt kopiëren.
8. Selecteer op het sneltabblad **Doelrechtspersonen** de optie **Rechtspersonen maken** om een nieuwe rechtspersoon te maken waarnaar u de gegevens van de bronrechtspersoon kunt kopiëren. Selecteer **Bestaande selecteren** om gegevens naar een bestaande rechtspersoon te kopiëren.
9. Optioneel: stel het veld **Nummerreeksen kopiëren** in op **Ja**. (Deze stap wordt aanbevolen wanneer u gegevens kopieert.)
10. Selecteer **Sjabloon toevoegen** in het gebied **Geselecteerde entiteiten**.
11. Selecteer de gewenste sjabloon. Voorgestelde sjablonen voor een nieuwe rechtspersoon zijn onder andere **025 - Grootboek** en **Financials**. We raden u aan alle andere beschikbare sjablonen te bekijken om te bepalen of ze van toepassing zijn op uw vereisten.
12. Selecteer **Kopiëren naar rechtspersoon** om een batchproces te starten waarmee de geselecteerde entiteiten worden gemaakt en naar de doelrechtspersoon worden gekopieerd.
13. Nadat het proces is voltooid, maar voordat er een transactie is geboekt, gaat u naar het grootboek en werkt u de boekhoudings- en aangiftevaluta's bij op de eerder beschreven wijze.

Als u een nieuwe rechtspersoon hebt gemaakt om de boekhoudings- of aangiftevaluta te wijzigen, controleert u of de beginsaldi van de valuta's van de oude rechtspersoon naar de nieuwe valuta's zijn vertaald.

Op de pagina [Kopiëren naar rechtspersoon](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017) kunt u een video bekijken waarin de voorgaande stappen worden weergegeven.
