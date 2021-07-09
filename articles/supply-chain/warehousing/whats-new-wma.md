---
title: Nieuwe of gewijzigde functies in de mobiele app Warehouse Management
description: In dit onderwerp worden de nieuwe en gewijzigde functies genoemd voor elke vrijgegeven versie van de mobiele app Warehouse Management voor Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261770"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Nieuwe of gewijzigde functies in de mobiele app Warehouse Management

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de nieuwe functies, oplossingen, verbeteringen en bekende problemen genoemd voor elke vrijgegeven versie van de mobiele app Warehouse Management voor Microsoft Dynamics 365 Supply Chain Management.

## <a name="version-2060"></a>Versie 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Nieuwe functies, oplossingen en verbeteringen in 2.0.6.0

Deze versie bevat de volgende nieuwe functies, verbeteringen en oplossingen voor fouten:

- In de demonstratiemodus worden nu alle labels in de apparaattaal vermeld.
- Het is minder waarschijnlijk dat u het volgende foutbericht ontvangt: 'Kan geen geschikte weergave vinden voor de opgegeven grootte'.
- De minimumhoogte voor werkkaarten is toegenomen (voor gevallen waarin er drie of minder velden zijn geconfigureerd voor de werklijst).
- De marges (wegvallen) onderaan de detailkaarten zijn verbeterd.
- Ongeldige symbolen in XML-bestanden die met de server worden uitgewisseld, worden nu op de een of andere manier verwerkt. (Niet-afdrukbare tekens worden nu op een andere manier verwerkt en zijn er niet langer de oorzaak van dat de app niet meer reageert.)
- HTTP-fouten (zoals 'fout 503') wanneer een serveraanvraag wordt ingediend, worden nu op een andere manier verwerkt.
- Als er een fout wordt weergegeven, wordt de lijst met opties niet meer automatisch weergegeven voor de besturingselementen van keuzelijsten met invoervak.
- De weergavestand die in de gebruikersinstellingen is geselecteerd, veroorzaakt niet meer dat de app stopt met reageren.
- Productafbeeldingen worden nu weergegeven in selfserviceomgevingen. (Deze wijziging is alleen van toepassing op versies met een lage resolutie. De bestandsbeheerservice ondersteunt geen afbeeldingen in een volledige grootte in selfserviceomgevingen.)
- Een probleem met een nulhoeveelheid voor korte verzamelingen is opgelost.
- Als een detailkaart meerdere identieke velden bevat, veroorzaakt dit niet meer dat de app stopt met reageren.

### <a name="known-issues-in-version-2060"></a>Bekende problemen in 2.0.6.0

De volgende bekende problemen komen in deze versie voor:

- De app (met name de werklijst) wordt na verloop van tijd langzamer.
- **Windows-versie**: wanneer onder Windows een USB-scanner wordt gebruikt om te scannen, veroorzaken inconsistente resultaten dat gescande symbolen door elkaar raken.

## <a name="version-2050"></a>Versie 2.0.5.0

Deze versie bevat de volgende nieuwe functies, verbeteringen en oplossingen voor fouten:

- Het clientgeheim wordt niet meer verborgen in de configuratie van de verbindingsinstellingen.
- U kunt nu elke tekst lang indrukken om deze volledig weer te geven.
- Het foutbericht wanneer er opslagmachtigingen ontbreken, is verbeterd.
- Er zijn nieuwe besturingsreeksen toegevoegd voor bepaalde stromen.
- De verzendknop wordt niet langer ten onrechte beschikbaar gesteld vanwege de venstergrootte.
- Schuifregelaars kunnen nu doorgaan op kleinere schermen wanneer grotere knoppengrootten worden gebruikt.
- De overlay met vier knoppen wordt niet meer afgesneden.
- De knop Verwijderen wordt nu ondersteund op het toetsenbord.
- Een probleem met de helderheid is verholpen dat zich kon voordoen wanneer op het toetsenbord werd gedrukt.
- Er zijn verschillende problemen met demogegevens opgelost.
- Er is een probleem verholpen dat gevolgen had voor numerieke velden op de detailpagina.
- Het toetsenbord verdwijnt niet meer af en toe op bepaalde apparaten.
- Er zijn diverse fouten met de gebruikersinterface (UI) verholpen, zoals fouten die van invloed waren op de kleur en positionering van de achtergrond.
- De Russische gebruikersinterface is verbeterd.
- Verschillende problemen waardoor het systeem niet meer reageerde, zijn opgelost.
- Een probleem in verband met het heropenen van de rekenmachine is opgelost.
- **Android-versie**: er is een probleem verholpen waardoor Android 4.4 niet meer reageerde bij het opstarten.
- **Android versie:** minimum voor schalen is verlaagd tot 50 procent.

## <a name="version-2040"></a>Versie 2.0.4.0

Versie 2.0.4.0 was de eerste algemeen beschikbare versie van de mobiele app Warehouse Management.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Nieuwe functies, oplossingen en verbeteringen in 2.0.4.0

Deze versie bevat de volgende nieuwe functies, correcties en verbeteringen die niet beschikbaar waren in de preview-versie:

- Als een detailkaart twee labels bevat met identieke gegevens, wordt één van de labels verborgen.
- Speciale tekens worden nu standaard weergegeven en de optie om ze te verbergen is uit de gebruikersinstellingen verwijderd.
- Uitgeschakelde verzendknoppen worden nu als niet beschikbaar weergegeven in de compacte weergave op de arm.
- Met een wijziging in de reekslogica voor besturingselementen verandert de schaal op verschillende apparaten gelijkmatiger. U hoeft de schaal van lettertypen of knoppen daarom niet zo sterk aan te passen.
- Het standaardkleurenthema is gewijzigd in *Donker*.
- Het ontbrekende pictogram voor de uitgeschakelde verzendknop is toegevoegd in de weergave in het lint.
- Bij time-out-uitzonderingen gaat u nu naar de verbindingspagina in plaats van dat een inlinefout wordt weergegeven.
- Als er geen verzendactie beschikbaar is (zoals **OK**, **Ja**, **Accepteren**, **Gereed** of **Voltooid**), wordt de verzendknop uitgeschakeld.
- De app-stabiliteit is verbeterd.
- Er is een oplossing voor beveiligingsprobleem [CVE-2021-26701. ](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701)
- **Windows-versie:** er is een probleem opgelost in Windows, waarbij menu's niet reageerden nadat het formaat van het venster was gewijzigd.

### <a name="known-issue-in-version-2040"></a>Bekend probleem in versie 2.0.4.0

Het volgende bekende probleem komt in deze versie voor:

- Deze versie heeft een probleem met apparaten die Android 4.4 gebruiken. U kunt problemen ondervinden wanneer u de app met deze versie van Android gebruikt.
