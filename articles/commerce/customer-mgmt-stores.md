---
title: Klantbeheer in winkels
description: In dit artikel wordt uitgelegd hoe detailhandelaren mogelijkheden voor klantbeheer kunnen inschakelen op het verkooppunt (POS) in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 805d0b5894b18e2fc34f481bdc32ada7a4b1aee0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863482"
---
# <a name="customer-management-in-stores"></a>Klantbeheer in winkels

[!include [banner](includes/banner.md)]

In dit artikel wordt uitgelegd hoe detailhandelaren mogelijkheden voor klantbeheer kunnen inschakelen op het verkooppunt (POS) in Microsoft Dynamics 365 Commerce.

Het is belangrijk dat winkelmedewerkers klantrecords kunnen maken en bewerken op het POS. Op die manier kunnen zij updates van klantgegevens vastleggen, zoals het e-mailadres, telefoonnummer en adres. Deze informatie is handig in downstream systemen zoals marketing, omdat de effectiviteit van die systemen afhankelijk is van de nauwkeurigheid van de klantgegevens.

Verkoopmedewerkers kunnen de werkstroom voor het maken van klanten starten vanaf twee POS-invoerpunten. Ze kunnen een knop selecteren die is toe te voegen aan de bewerking **Klant toevoegen** of ze kunnen **Klant maken** selecteren op de app-balk op de pagina met zoekresultaten. In beide gevallen wordt het dialoogvenster **Nieuwe klant** weergegeven, waar verkoopmedewerkers de vereiste klantgegevens kunnen invoeren, zoals de naam, het e-mailadres, het telefoonnummer, het adres en eventuele aanvullende gegevens die relevant zijn voor het bedrijf. Die extra informatie kan worden vastgelegd aan de hand van de klantkenmerken die aan de klant zijn gekoppeld. Zie [Klantkenmerken](dev-itpro/customer-attributes.md) voor meer informatie over klantkenmerken.

Verkoopmedewerkers kunnen ook secundaire e-mailadressen en telefoonnummers vastleggen. Bovendien kunnen ze de voorkeur van de klant bij het ontvangen van marketinggegevens vastleggen via een van die secundaire e-mailadressen of telefoonnummers. Om deze mogelijkheid in te kunnen stellen, moeten detailhandelaren de functie **Meerdere e-mails en telefoonnummers vastleggen en toestemming voor marketing voor deze functie voor contactpersonen** in de werkruimte **Functiebeheer** in Commerce Headquarters inschakelen (**Systeembeheer \> Werkruimten \> Functiebeheer**).

## <a name="default-customer-properties"></a>Standaardklanteigenschappen

Detailhandelaren kunnen de pagina **Alle winkels** in Commerce Headquarters (**Retail en Commerce \> Afzetkanalen \> Winkels**) gebruiken om een standaardklant aan elke winkel te koppelen. Commerce kopieert vervolgens de eigenschappen die zijn gedefinieerd voor de standaardklant naar alle nieuwe klantrecords die zijn gemaakt. In het dialoogvenster **Klant maken** worden bijvoorbeeld eigenschappen weergegeven die zijn overgenomen van de standaardklant die aan de winkel is gekoppeld. Deze eigenschappen omvatten het **klanttype**, de **klantengroep**, de **ontvangstbewijsoptie**, **e-mail voor ontvangstbewijs**, de **valuta** en de **taal**. **Aansluitingen** (groeperingen van klanten) worden ook overgenomen van de standaardklant. **Financiële dimensies** worden echter overgenomen van de klantengroep die aan de standaardklant is gekoppeld, en niet van de standaardklant zelf.

> [!NOTE]
> De **e-mail voor ontvangstbewijs** wordt alleen van de standaardklant gekopieerd als de ID van de e-mail voor het ontvangstbewijs niet is opgegeven voor de nieuwe klanten. Dit betekent dat als de ID van de e-mail voor het ontvangstbewijs aanwezig is voor de standaardklant, alle klanten die op de e-commercesite zijn gemaakt, dezelfde ID van de e-mail voor het ontvangstbewijs krijgen omdat er geen gebruikersinterface is om de ID van de e-mail voor het ontvangstbewijs van de klant vast te leggen. We raden u aan het veld **E-mail voor ontvangstbewijzen** leeg te houden voor de standaardklant van de winkel en dit veld alleen te gebruiken als u een bedrijfsproces hebt dat afhankelijk is van het aanwezig zijn van een e-mailadres voor een ontvangstbewijs. 

Verkoopmedewerkers kunnen meerdere adressen voor een klant vastleggen. De naam en het telefoonnummer van de klant worden overgenomen vanuit de contactgegevens die aan elk adres zijn gekoppeld. Het sneltabblad **Adressen** van een klantrecord bevat een veld **Doel** dat verkoopmedewerkers kunnen bewerken. Als het klanttype **Persoon** is, geldt **Start** als standaardwaarde. Als het klanttype **Organisatie** is, geldt **Business** als standaardwaarde. Andere waarden die in dit veld worden ondersteund, zijn onder andere **Start**, **Kantoor** en **Postbus**. De waarde van het veld **Land** voor een adres wordt overgenomen van het primaire adres dat is opgegeven op de pagina **Operationele eenheid** in Commerce Headquarters in **Organisatiebeheer \> Organisaties \> Operationele eenhden**.



## <a name="additional-resources"></a>Aanvullende bronnen

[Modus voor het maken van asynchrone klanten](async-customer-mode.md)

[Asynchrone klanten converteren naar synchrone klanten](convert-async-to-sync.md)

[Klantkenmerken](dev-itpro/customer-attributes.md)

[Uitsluiting van offlinegegevens](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
