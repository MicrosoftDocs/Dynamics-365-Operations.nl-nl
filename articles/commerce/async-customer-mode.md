---
title: Modus voor het maken van asynchrone klanten
description: In dit artikel wordt de modus voor het maken van asynchrone klanten in Microsoft Dynamics 365 Commerce beschreven.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 95102936871e15f8e525abca736fa75927569b34
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473701"
---
# <a name="asynchronous-customer-creation-mode"></a>Modus voor het maken van asynchrone klanten

[!include [banner](includes/banner.md)]

In dit artikel wordt de modus voor het maken van asynchrone klanten in Microsoft Dynamics 365 Commerce beschreven.

In Commerce zijn er twee manieren om klanten te maken: synchroon en asynchroon. Klanten worden standaard synchroon gemaakt. Dit wil zeggen dat ze in realtime worden aangemaakt in Commerce headquarters. De modus voor het maken van synchrone klanten is nuttig omdat nieuwe klanten onmiddellijk in verschillende kanalen kunnen worden gezocht. Deze heeft echter ook een nadeel. Aangezien er [Commerce Data Exchange: realtime service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)-aanroepen naar Commerce Headquarters worden gegenereerd, kan dit gevolgen hebben voor de prestaties als er veel gelijktijdige aanroepen worden gedaan voor het maken van klanten.

Als de optie **Klant maken in asynchrone modus** is ingesteld op **Ja** in het functionaliteitsprofiel van de winkel (**Retail en Commerce \> Afzetkanaalinstellingen \> Onlinewinkel instellen \> Functionaliteitsprofielen**), worden realtime service-aanroepen niet gebruikt om klantrecords te maken in de afzetkanaaldatabase. De modus voor het maken van asynchrone klanten heeft geen invloed op de prestaties van Commerce Headquarters. Een tijdelijke Globally Unique Identifier (GUID) wordt toegewezen aan elke nieuwe asynchrone klantrecord en wordt gebruikt als de klantrekening-id. Deze GUID wordt niet weergegeven voor POS-gebruikers. In plaats daarvan krijgen deze gebruikers de **In afwachting van synchronisatie** te zien als klantrekening-id.

> [!IMPORTANT]
> Wanneer het POS offline gaat, maakt het systeem de klanten automatisch asynchroon aan, zelfs wanneer de modus voor het maken van asynchrone klanten is uitgeschakeld. Daarom moeten beheerders van Commerce headquarters, onafhankelijk van de keuze voor synchrone of asynchrone aanmaak van klanten, een terugkerende batchtaak aanmaken en inplannen voor de **P-taak**, de taak **Klanten en zakenpartners synchroniseren vanuit de asynchrone modus** en de taak **1010**, zodat eventuele asynchrone klanten worden geconverteerd naar synchronisatieklanten in Commerce headquarters.

## <a name="async-customer-limitations"></a>Beperkingen van asynchrone klanten

De functionaliteit voor asynchrone klanten heeft momenteel de volgende beperking:

- Loyaliteitskaarten kunnen alleen aan asynchrone klanten worden uitgegeven als de nieuwe klantrekening-id is gesynchroniseerd met het afzetkanaal.

## <a name="async-customer-enhancements"></a>Verbeteringen in asynchrone klanten

De volgende verbeteringen zijn uitgerold om te zorgen voor pariteit tussen synchrone en asynchrone modi in kanalen, om organisaties te helpen bij het gebruik van asynchrone aanmaak van klanten om klanten te beheren en om te helpen de realtime communicatie met Commerce headquarters te verminderen. 

| Functieverbetering | Commerce versie | Functiedetails |
|---|---|---|
| Prestatieverbeteringen wanneer klantgegevens worden opgehaald uit de kanaaldatabase | 10.0.20 en later | De klantentiteit is opgesplitst in kleinere entiteiten om de prestaties te verbeteren. Het systeem haalt vervolgens alleen de vereiste informatie op uit de kanaaldatabase. |
| De mogelijkheid om asynchrone adressen aan te maken tijdens het uitchecken | 10.0.22 en later | <p>Functieschakelaar: **Asynchroon aanmaken van klantadressen inschakelen**</p><p>Informatie functie:</p><ul><li>De mogelijkheid om adressen toe te voegen zonder dat er realtime serviceaanroepen worden gedaan naar Commerce headquarters</li><li>De mogelijkheid om adressen in de kanaaldatabase uniek te identificeren zonder een record-ID te gebruiken (waarde **RecId**)</li><li>Traceringstijden voor het aanmaken van adressen</li><li>Synchronisatie van adressen in Commerce headquarters</li></ul><p>Deze functie is zowel van invloed op synchrone als asynchrone klanten. De functie **Klanten bewerken in asynchrone modus** moet worden ingeschakeld om naast het asynchroon aanmaken van adressen deze adressen asynchroon te kunnen bewerken .</p> |
| Pariteit inschakelen tussen het aanmaken van synchrone en asynchrone klanten. | 10.0.24 en later | <p>Functieschakelaar: **Geavanceerd asynchrone klanten aanmaken inschakelen**</p><p>Informatie functie: De mogelijkheid om extra informatie vast te leggen, zoals de titel, aansluitingen van de standaardklant en secundaire contactgegevens (telefoonnummer en e-mailadres), terwijl u klanten asynchroon aanmaakt</p> |
| Gebruiksvriendelijke foutberichten | 10.0.28 en later | Deze verbeteringen helpen bij het verbeteren van gebruiksvriendelijke foutberichten als een gebruiker niet onmiddellijk informatie kan bewerken terwijl de synchronisatie wordt uitgevoerd. U kunt deze verbeteringen inschakelen door de instelling **Bepaalde UI-elementen niet laten bewerken door een asynchrone klant** onder **Site-instellingen \> Uitbreidingen** in Commerce site builder te gebruiken. |
| De mogelijkheid om klantgegevens asynchroon te bewerken | 10.0.29 en later | <p>Functieschakelaar: **Klanten bewerken in asynchrone modus inschakelen**</p><p>Informatie functie: De mogelijkheid om klantgegevens asynchroon te bewerken</p><p>Raadpleeg [Modus voor het aanmaken van asynchrone klanten - veelgestelde vragen](async-customer-mode-faq.md) voor antwoorden op veel voorkomende vragen over problemen die betrekking hebben op het asynchroon bewerken van klantgegevens.</p> |

### <a name="feature-switch-hierarchy"></a>Hiërarchie functieschakelaars

Door de hiërarchie van functieschakelaars moet u, voordat u de functie **Klanten bewerken in asynchrone modus inschakelen** inschakelt, de volgende functies inschakelen: 

- **Prestatieverbeteringen voor klantorders en klanttransacties**: deze functie is verplicht sinds de release van Commerce versie 10.0.28. 
- **Verbeterde functies inschakelen voor het asynchroon aanmaken van klanten**
- **Asynchrone aanmaak voor klantadressen inschakelen**

Raadpleeg [Modus voor het aanmaken van asynchrone klanten - veelgestelde vragen](async-customer-mode-faq.md) voor antwoorden op algemene vragen met betrekking tot probleemoplossing. 

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
