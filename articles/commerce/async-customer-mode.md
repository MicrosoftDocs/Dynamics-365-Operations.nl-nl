---
title: Modus voor het maken van asynchrone klanten
description: In dit onderwerp wordt de modus voor het maken van asynchrone klanten in Microsoft Dynamics 365 Commerce beschreven.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 43418b61778d187364d4d52a05178078a37623eb
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984265"
---
# <a name="asynchronous-customer-creation-mode"></a>Modus voor het maken van asynchrone klanten

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de modus voor het maken van asynchrone klanten in Microsoft Dynamics 365 Commerce beschreven.

In Commerce zijn er twee manieren om klanten te maken: synchroon en asynchroon. Klanten worden standaard synchroon gemaakt. Dit wil zeggen dat ze in realtime worden gemaakt in Commerce Headquarters. De modus voor het maken van synchrone klanten is nuttig omdat nieuwe klanten onmiddellijk in verschillende kanalen kunnen worden gezocht. Deze heeft echter ook een nadeel. Aangezien er [Commerce Data Exchange: realtime service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)-aanroepen naar Commerce Headquarters worden gegenereerd, kan dit gevolgen hebben voor de prestaties als er veel gelijktijdige aanroepen worden gedaan voor het maken van klanten.

Als de optie **Klant maken in asynchrone modus** is ingesteld op **Ja** in het functionaliteitsprofiel van de winkel (**Retail en Commerce \> Afzetkanaalinstellingen \> Onlinewinkel instellen \> Functionaliteitsprofielen**), worden realtime service-aanroepen niet gebruikt om klantrecords te maken in de afzetkanaaldatabase. De modus voor het maken van asynchrone klanten heeft geen invloed op de prestaties van Commerce Headquarters. Een tijdelijke Globally Unique Identifier (GUID) wordt toegewezen aan elke nieuwe asynchrone klantrecord en wordt gebruikt als de klantrekening-id. Deze GUID wordt niet weergegeven voor POS-gebruikers. In plaats daarvan krijgen deze gebruikers de **In afwachting van synchronisatie** te zien als klantrekening-id.

> [!IMPORTANT]
> Wanneer het POS offline gaat, maakt het systeem de klanten automatisch asynchroon aan, zelfs wanneer de modus voor het maken van asynchrone klanten is uitgeschakeld. Commerce Headquarters-beheerders moeten daarom, ongeacht of er nu synchrone of asynchrone klanten worden gemaakt, een terugkerende batchtaak aanmaken en inplannen voor de **P-taak**, de taak **Klanten en zakenpartners synchroniseren vanuit asynchrone modus** (eerder ook wel **Klanten en zakenpartners synchroniseren vanuit asynchrone modus** genoemd) en de taak **1010**, zodat alle asynchrone klanten worden geconverteerd naar synchrone in Commerce Headquarters.

## <a name="async-customer-limitations"></a>Beperkingen van asynchrone klanten

De functionaliteit voor asynchrone klanten heeft momenteel de volgende beperkingen:

- Asynchrone klantrecords kunnen niet worden bewerkt tenzij de klant is gemaakt in Commerce Headquarters en de nieuwe klantrekening-id weer met het afzetkanaal is gesynchroniseerd.
- Loyaliteitskaarten kunnen alleen aan asynchrone klanten worden uitgegeven als de nieuwe klantrekening-id is gesynchroniseerd met het afzetkanaal.

## <a name="async-customer-enhancements"></a>Verbeteringen in asynchrone klanten

Vanaf versie 10.0.24 van Commerce kunt u de functie **Verbeterde functie voor maken van asynchrone klanten** in de werkruimte **Functiebeheer** inschakelen. Met deze functie wordt de lacune tussen de modi voor het maken van asynchrone en synchrone klanten in POS en e-commerce op de volgende manieren gesynchroniseerd:

- Aansluitingen kunnen niet aan asynchrone klanten worden gekoppeld.
- Titels kunnen aan asynchrone klanten worden toegevoegd.
- Secundaire e-mailadressen en telefoonnummers kunnen worden vastgelegd voor asynchrone klanten.

Vanaf versie 10.0.22 van Commerce kunt u de functie **Asynchroon aanmaken voor klantadressen inschakelen** in de werkruimte **Functiebeheer** inschakelen. Met deze functie kunnen nieuwe klantadressen asynchroon worden opgeslagen voor synchrone en asynchrone klanten.

Nadat u de eerder gemelde functies hebt ingeschakeld, moet u een terugkerende batchtaak maken en plannen voor de **P-taak**, de taak **Klanten en zakenpartners synchroniseren vanuit de asynchrone modus** en de taak **1010**, zodat eventuele asynchrone klanten worden geconverteerd naar synchrone klanten in Commerce Headquarters.

### <a name="customer-creation-in-pos-offline-mode"></a>Klant maken in offlinemodus van POS

Zoals eerder aangegeven, maakt het systeem klanten automatisch asynchroon aan als het POS offline gaat, zelfs wanneer de modus voor het asynchrone klanten is uitgeschakeld. Beheerders van Commerce Headquarters moeten daarom een terugkerende batchtaak maken en plannen voor de **P-taak**, de taak **Klanten en zakenpartners synchroniseren vanuit de asynchrone modus** en de taak **1010**, zodat eventuele asynchrone klanten worden geconverteerd naar synchrone klanten in Commerce Headquarters.

> [!NOTE]
> Als de optie **Gedeelde klantgegevenstabellen filteren** is ingesteld op **Ja** op de pagina **Handelkanaalschema** (**Retail en Commerce \> Instelling van hoofdkantoor \> Commerce-planner \> Kanaaldatabasegroep**) worden er geen klantrecords gemaakt in de offlinemodus van het Commerce-kanaal. Zie [Uitsluiting van offlinegegevens](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion) voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Klantbeheer in winkels](customer-mgmt-stores.md)

[Asynchrone klanten converteren naar synchrone klanten](convert-async-to-sync.md)

[Klantkenmerken](dev-itpro/customer-attributes.md)

[Uitsluiting van offlinegegevens](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
