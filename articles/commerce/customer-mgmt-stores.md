---
title: Klantbeheer in winkels
description: In dit onderwerp wordt uitgelegd hoe detailhandelaren mogelijkheden voor klantbeheer kunnen inschakelen op het verkooppunt (POS) in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 05/25/2021
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
ms.openlocfilehash: ea2953510d134be0d33a6afa65027a6c9d2816f7dc16ca669859e80ee40f4278
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754411"
---
# <a name="customer-management-in-stores"></a>Klantbeheer in winkels

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe detailhandelaren mogelijkheden voor klantbeheer kunnen inschakelen op het verkooppunt (POS) in Microsoft Dynamics 365 Commerce.

Het is belangrijk dat winkelmedewerkers klantrecords kunnen maken en bewerken op het POS. Op die manier kunnen zij updates van klantgegevens vastleggen, zoals het e-mailadres, telefoonnummer en adres. Deze informatie is handig in downstream systemen zoals marketing, omdat de effectiviteit van die systemen afhankelijk is van de nauwkeurigheid van de klantgegevens.

Verkoopmedewerkers kunnen de workflow voor het maken van klanten starten vanaf twee POS-invoerpunten. Ze kunnen een knop selecteren die is toe te voegen aan de bewerking **Klant toevoegen** of ze kunnen **Klant maken** selecteren op de app-balk op de pagina met zoekresultaten. In beide gevallen wordt het dialoogvenster **Nieuwe klant** weergegeven, waar verkoopmedewerkers de vereiste klantgegevens kunnen invoeren, zoals de naam, het e-mailadres, het telefoonnummer, het adres en eventuele aanvullende gegevens die relevant zijn voor het bedrijf. Die extra informatie kan worden vastgelegd aan de hand van de klantkenmerken die aan de klant zijn gekoppeld. Zie [Klantkenmerken](dev-itpro/customer-attributes.md) voor meer informatie over klantkenmerken.

Verkoopmedewerkers kunnen ook secundaire e-mailadressen en telefoonnummers vastleggen. Bovendien kunnen ze de voorkeur van de klant bij het ontvangen van marketinggegevens vastleggen via een van die secundaire e-mailadressen of telefoonnummers. Om deze mogelijkheid in te kunnen stellen, moeten detailhandelaren de functie **Meerdere e-mails en telefoonnummers vastleggen en toestemming voor marketing voor deze functie voor contactpersonen** in het werkgebied **Functiebeheer** in Commerce Headquarters inschakelen (**Systeembeheer \> Werkgebieden \> Functiebeheer**).

## <a name="default-customer-properties"></a>Standaardklanteigenschappen

Detailhandelaren kunnen de pagina **Alle winkels** in Commerce Headquarters (**Retail en Commerce \> Afzetkanalen \> Winkels**) gebruiken om een standaardklant aan elke winkel te koppelen. Commerce kopieert vervolgens de eigenschappen die zijn gedefinieerd voor de standaardklant naar alle nieuwe klantrecords die zijn gemaakt. In het dialoogvenster **Klant maken** worden bijvoorbeeld eigenschappen weergegeven die zijn overgenomen van de standaardklant die aan de winkel is gekoppeld. Deze eigenschappen omvatten het **klanttype**, de **klantengroep**, de **ontvangstbewijsoptie**, **e-mail voor ontvangstbewijs**, de **valuta** en de **taal**. **Aansluitingen** (groeperingen van klanten) worden ook overgenomen van de standaardklant. **Financiële dimensies** worden echter overgenomen van de klantengroep die aan de standaardklant is gekoppeld, en niet van de standaardklant zelf.

> [!NOTE]
> De **e-mail voor ontvangstbewijs** wordt alleen van de standaardklant gekopieerd als de ID van de e-mail voor het ontvangstbewijs niet is opgegeven voor de nieuwe klanten. Dit betekent dat als de ID van de e-mail voor het ontvangstbewijs aanwezig is voor de standaardklant, alle klanten die op de e-commercesite zijn gemaakt, dezelfde ID van de e-mail voor het ontvangstbewijs krijgen omdat er geen gebruikersinterface is om de ID van de e-mail voor het ontvangstbewijs van de klant vast te leggen. We raden u aan het **e-mailveld voor ontvangstbewijzen** leeg te houden voor de standaardklant van de winkel en deze alleen te gebruiken als u een bedrijfsproces hebt dat afhankelijk is van het feit dat een e-mailadres voor een ontvangstbewijs aanwezig is. 

Verkoopmedewerkers kunnen meerdere adressen voor een klant vastleggen. De naam en het telefoonnummer van de klant worden overgenomen vanuit de contactgegevens die aan elk adres zijn gekoppeld. Het sneltabblad **Adressen** van een klantrecord bevat een veld **Doel** dat verkoopmedewerkers kunnen bewerken. Als het klanttype **Persoon** is, geldt **Start** als standaardwaarde. Als het klanttype **Organisatie** is, geldt **Business** als standaardwaarde. Andere waarden die in dit veld worden ondersteund, zijn onder andere **Start**, **Kantoor** en **Postbus**. De waarde van het veld **Land** voor een adres wordt overgenomen van het primaire adres dat is opgegeven op de pagina **Operationele eenheid** in Commerce Headquarters in **Organisatiebeheer \> Organisaties \> Operationele eenhden**.

## <a name="sync-customers-and-async-customers"></a>Synchrone klanten en asynchrone klanten

In Commerce zijn er twee manieren om klanten te maken: Synchroon (of Sync) en Asynchroon (of Async). Klanten worden standaard synchroon gemaakt. Dit wil zeggen dat ze in realtime worden gemaakt in Commerce Headquarters. De synchrone modus voor het maken van klanten is nuttig, omdat nieuwe klanten onmiddellijk in verschillende kanalen kunnen worden gezocht. Deze heeft echter ook een nadeel. Aangezien er [Commerce Data Exchange: realtime service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)-aanroepen naar Commerce Headquarters worden gegenereerd, kan dit gevolgen hebben voor de prestaties als er veel gelijktijdige aanroepen worden gedaan voor het maken van klanten.

Als de optie **Klant maken in asynchrone modus** is ingesteld op **Ja** in het functionaliteitsprofiel van de winkel (**Retail en Commerce \> Afzetkanaalinstellingen \> Onlinewinkel instellen \> Functionaliteitsprofielen**), worden realtime service-aanroepen niet gebruikt om klantrecords te maken in de afzetkanaaldatabase. De asynchrone modus voor het maken van klanten heeft geen invloed op de prestaties van Commerce Headquarters. Een tijdelijke Globally Unique Identifier (GUID) wordt toegewezen aan elke nieuwe asynchrone klantrecord en wordt gebruikt als de klantrekening-id. Deze GUID wordt niet weergegeven voor POS-gebruikers. In plaats daarvan krijgen deze gebruikers de **In afwachting van synchronisatie** te zien als klantrekening-id. Hoewel klanten door deze configuratie asynchroon moeten worden gemaakt, worden bewerkingen van klantrecords altijd synchroon uitgevoerd.

### <a name="convert-async-customers-to-sync-customers"></a>Asynchrone klanten converteren naar synchrone klanten

Als u asynchrone klanten wilt converteren naar synchrone klanten, moet u eerst de P-taak uitvoeren om de asynchrone klanten naar Commerce Headquarters te verzenden. Voer vervolgens de taak **Klanten en zakenpartner synchroniseren vanuit de asynchrone modus** om klantrekening-id's te maken. Voer tot slot de taak **1010** uit om de nieuwe klantrekening-id's te synchroniseren met de afzetkanalen.

### <a name="async-customer-limitations"></a>Beperkingen van asynchrone klanten

De functionaliteit voor asynchrone klanten heeft momenteel de volgende beperkingen:

- Asynchrone klantrecords kunnen niet worden bewerkt tenzij de klant is gemaakt in Commerce Headquarters en de nieuwe klantrekening-id weer met het afzetkanaal is gesynchroniseerd.
- Aansluitingen kunnen niet aan asynchrone klanten worden gekoppeld. Nieuwe asynchrone klanten nemen dus geen aansluitingen over van de standaardklant.
- Loyaliteitskaarten kunnen alleen aan asynchrone klanten worden uitgegeven als de nieuwe klantrekening-id is gesynchroniseerd met het afzetkanaal.
- Secundaire e-mailadressen en telefoonnummers kunnen niet worden vastgelegd voor asynchrone klanten.

### <a name="customer-creation-in-pos-offline-mode"></a>Klant maken in offlinemodus van POS

Als het POS offline gaat terwijl de modus voor het maken van asynchrone klanten is ingeschakeld, worden nieuwe klantrecords asynchroon gemaakt. Als het POS offline gaat terwijl de modus voor het maken van asynchrone klanten is uitgeschakeld, schakelt het systeem automatisch over op de modus voor het maken van asynchrone klanten. Met andere woorden, klantrecords worden mogelijk asynchroon gemaakt ook als de modus voor het maken van asynchrone klanten is uitgeschakeld. Beheerders van Commerce Headquarters moeten daarom een terugkerende batchtaak maken en plannen voor de P-taak, de taak **Klanten en zakenpartners synchroniseren vanuit de asynchrone modus** en de taak **1010**, zodat eventuele asynchrone klanten worden geconverteerd naar synchronisatieklanten in Commerce Headquarters.

> [!NOTE]
> Als de optie **Gedeelde klantgegevenstabellen filteren** is ingesteld op **Ja** op de pagina **Handelkanaalschema** (**Retail en Commerce \> Instelling van hoofdkantoor \> Commerce-planner \> Kanaaldatabasegroep**) worden er geen klantrecords gemaakt in de offlinemodus van het Commerce-kanaal. Zie [Uitsluiting van offlinegegevens](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Klantkenmerken](dev-itpro/customer-attributes.md)

[Uitsluiting van offlinegegevens](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
