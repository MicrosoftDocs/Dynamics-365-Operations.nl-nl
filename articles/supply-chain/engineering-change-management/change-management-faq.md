---
title: Veelgestelde vragen over Beheer voor technische wijzigingen
description: Dit artikel biedt antwoorden op veelgestelde vragen over de functie Beheer voor technische wijzigingen.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 16d29fa6485bae866a5209a855dfb928e8bc4783
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870777"
---
# <a name="engineering-change-management-faq"></a>Veelgestelde vragen over Beheer voor technische wijzigingen

[!include [banner](../includes/banner.md)]

Dit artikel biedt antwoorden op veelgestelde vragen over de functie Beheer voor technische wijzigingen.

## <a name="should-i-track-the-version-in-transactions"></a>Moet ik de versie traceren in transacties?

Wanneer u een categorie voor technische wijzigingen maakt, bevat de pagina **Details van categorieën voor technische wijzigingen** een optie met de naam **Versie in transacties traceren**. Wat houdt deze instelling in en wat doet hij?

- Als u de optie **Versie in transacties traceren** instelt op *Ja*, wordt het veld **Dimensiegroep** gefilterd zodat alleen dimensiegroepen worden getoond waarin versie een actieve dimensie is.
- Als u de optie **Versie in transacties traceren instelt** op *Nee*, wordt het veld **Dimensiegroep** gefilterd zodat alleen dimensiegroepen worden getoond waarin versie **geen** actieve dimensie is.

### <a name="if-you-track-the-version-in-transactions"></a>Als u de versie traceert in transacties

Voor technische categorieën waarin u een dimensiegroep hebt geselecteerd waar versie een actieve dimensie is, kunt u versies traceren in transacties voor producten in die categorie. In dit geval is het technische product een productmodel voor het product en elke versie van het product is een productvariant die de dimensie versie gebruikt. Andere dimensies kunnen samen met de dimensie versie worden gebruikt.

In dit geval wordt elke technische versie in alle processen behandeld als een variant. Als u dus een specifieke variant in een transactie hebt (zodat u kunt bepalen welke variant is verkocht of ingekocht), moet u de voorraad beheren voor elke versie, wordt het aanbod in de hoofdplanning voor elke versie gepland, enzovoorts. Als u een versie uit de markt haalt, moet u handmatig de begin- en einddatums aanpassen zodat deze de wijziging weerspiegelen. U moet ook uw voorraad beheren om er zeker van te zijn dat u geen ongebruikte versies van artikelen in uw magazijnen hebt.

Hoewel deze optie meer beheersinspanning vereist, wordt dit aangeraden als u een hoge traceerbaarheid van de specifieke versies vereist die in elke transactie worden gebruikt.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Als u de versie niet traceert in transacties

Voor technische categorieën waarin u een dimensiegroep hebt geselecteerd waar versie **geen** actieve dimensie is, kunt u **niet** versies traceren in transacties voor producten in die categorie. Als u dan geen andere dimensie gebruikt, is het technische product een verschillend product. De versies van het product worden nog steeds bijgehouden en u kunt informatie beheren over specifieke versies (bijvoorbeeld de stuklijst \[BOM] en route), maar u kunt niet traceren welke specifieke versie in een transactie is gebruikt. Met de begin- en einddatums wordt de geldigheid van elke versie aangegeven.

Deze optie is veel eenvoudiger te beheren, omdat als u van de ene versie naar een volgende wilt gaan, u alleen de vereiste wijzigingen in een wijzigingsorder moet aanbrengen en vervolgens de begin- en einddatums in de technische versie moet bijwerken. De productieprocessen nemen vervolgens de vereiste stuklijst en route voor het product (en de specifieke versie) op.

De meeste organisaties kiezen deze optie omdat het versie- en wijzigingsbeheer biedt, maar niet de extra overhead toevoegt voor het traceren van de versie in elke transactie, in de voorraad en tijdens de hoofdplanning.

## <a name="which-fields-are-copied-from-the-released-item-template"></a>Welke velden worden vanuit de vrijgegeven artikelsjabloon gekopieerd?

Wanneer een technisch bedrijf een technisch product maakt, wordt dat product gemaakt als vrijgegeven product in het technische bedrijf. Het vrijgegeven product dat wordt gemaakt, is gebaseerd op de geselecteerde *vrijgegeven artikelsjabloon*. (De vrijgegeven artikelsjabloon is zelf een bestaand vrijgegeven product.) De vrijgegeven artikelsjabloon wordt ook gebruikt wanneer het product wordt vrijgegeven voor een operationeel bedrijf. In elk geval definieert de vrijgegeven artikelsjabloon de meeste veldwaarden voor het vrijgegeven product. Deze waarden zijn afkomstig van de bijbehorende pagina **Vrijgegeven productdetails**.

In de volgende tabellen ziet u de velden die tijdens deze processen worden gekopieerd.

| Sneltabblad | Velden die worden gekopieerd bij het maken van producten in het technische bedrijf | Velden die worden gekopieerd bij vrijgave naar een operationeel bedrijf |
|---|---|---|
| **Algemeen** | Alle velden in de sectie **Administratie** | Dezelfde velden die worden gekopieerd voor het technische bedrijf |
| **Inkoop** | Alle velden | Alle velden behalve **Eenheid** |
| **Verkopen** | Alle velden in de volgende secties: **Verkooporder**, **Administratie**, **Belasting**, **Prijsupdate**, **Basisverkoopprijs**, **Toeslagen**, **Kortingen** en **Alternatief product** | Al dezelfde velden die worden gekopieerd voor het technische bedrijf, behalve **Eenheid** |
| **Buitenlandse handel** | Alle velden | Alle velden |
| **Voorraadbeheer** | Alle velden en secties *behalve* **Fysieke afmetingen** en **Catch weight** | Al dezelfde velden die worden gekopieerd voor het technische bedrijf, behalve **Eenheid** |
| **Technicus**, **Plannen**, **Kosten beheren**, **Projecten beheren**, **Financiële dimensies** en **Magazijn** | Alle velden | Alle velden behalve **Stuklijsteenheid** |
| **Productvarianten** | Alle velden in de sectie **Standaardproductvariant** | Dezelfde velden die worden gekopieerd voor het technische bedrijf |

Naast de velden die worden vermeld in de vorige tabel, worden alle standaardorderinstellingen gekopieerd vanuit de vrijgegeven artikelsjabloon, zowel wanneer het product wordt gemaakt in het technische bedrijf als wanneer het is vrijgegeven voor een operationeel bedrijf. (Als u de standaardorderinstellingen wilt weergeven voor een vrijgegeven artikelsjabloon, opent u de relevante pagina **Details vrijgegeven product** en selecteert u in het actievenster op het tabblad **Voorraad beheren** de optie **Standaardorderinstellingen**.)

> [!NOTE]
>
> - De eenheid wordt standaard uit de sjabloon gebruikt.
> - Voor detailhandelaren die Dynamics 365 Commerce-functionaliteit gebruiken bij het toewijzen van een detailhandelcategorie aan een product, worden door de detailhandelcategorie standaardwaarden toegepast voor een groot aantal velden voor het vrijgegeven productniveau. Deze standaardwaarden overschrijven waarden die mogelijk al door de sjabloon zijn ingesteld of uit engineering zijn gekopieerd.

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Moet ik een afzonderlijke rechtspersoon voor technische producten maken of een bestaande rechtspersoon gebruiken?

Uw zakelijke behoeften bepalen of u een nieuwe rechtspersoon voor technische producten moet maken.

Door een afzonderlijk technisch bedrijf te maken, kunt u technische gegevens gescheiden houden en vervolgens wijzigingen toevoegen zoals vereist voor uw lokale operationele bedrijven. Met deze benadering kunt u de volgende doelen realiseren:

- Een afzonderlijke entiteit behouden waarin de technische producten worden gemaakt en beheerd.
- Voorkomen dat technische producten samen met de rest van uw vrijgegeven producten worden weergegeven totdat ze klaar zijn en worden vrijgegeven.
- Duidelijk de gegevens onderscheiden die worden dicteerd door technische en lokale gegevens.

Anderzijds moet u een bestaande rechtspersoon waarschijnlijk gebruiken als een technisch bedrijf als de volgende voorwaarden voor u gelden:

- U hebt slechts één rechtspersoon in het systeem en/of u vereist geen duidelijke scheiding tussen producten die worden ontworpen.
- U wilt bepaalde gegevens niet dupliceren, zoals resourcegroepen, resources, bewerkingen en (misschien) locaties.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Wat is de nomenclatuur voor technische versies en varianten?

De nomenclatuur voor technische producten en productvarianten werken als volgt:

- Voor het technische product (dat wil zeggen het verschillende product als er geen dimensies worden gebruikt, of het productmodel als een dimensie worden gebruikt), wordt de nummerregelnomenclatuur gedefinieerd in de categorie van het technische product. Hier hebt u de optie om een nummerreeks, tekstconstanten en kenmerknamen en -waarden te gebruiken.
- Voor elke variant van een technisch product (als uw technische product een productmodel is, worden varianten ingesteld in de technische-productcategorie waarin u de dimensiegroep opgeeft), wordt de nummerregelnomenclatuur voor elke variant gedefinieerd in de dimensiegroep. In dit geval kunt u de product-id van het hoofdmodel en de dimensiewaarden en -namen gebruiken.
