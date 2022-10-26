---
title: Modus voor het aanmaken van asynchrone klanten - veelgestelde vragen
description: Dit artikel bevat antwoorden op veelgestelde vragen over het aanmaken van asynchrone klanten in Microsoft Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 64c895fb9f3e55f7680759fa72626be6660aa67c
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690197"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Modus voor het aanmaken van asynchrone klanten - veelgestelde vragen

[!include [banner](includes/banner.md)]

Dit artikel bevat antwoorden op veelgestelde vragen over het aanmaken van asynchrone (async) klanten in Microsoft Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Waarom kan ik de functie 'Klanten bewerken in asynchrone modus inschakelen' niet inschakelen?

Voordat u de functie **Klanten bewerken in asynchrone modus inschakelen** inschakelt, moet u de volgende functies inschakelen:

- Prestatieverbeteringen voor klantorders en klanttransacties
- Verbeterde functies inschakelen voor het aanmaken van async-klanten
- Asynchrone aanmaak voor klantadressen inschakelen

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Waarom zie ik nog steeds real-time serviceaanroepen die in Commerce headquarters worden gedaan nadat de functie 'Klanten bewerken in asynchrone modus inschakelen' is ingeschakeld?

Dit probleem treedt op wanneer Commerce Data Exchange (CDX)-taken niet zijn uitgevoerd om te waarborgen dat de status van de functie en andere kanaalmetagegevens worden gesynchroniseerd met het kanaal. Voordat u het scenario opnieuw probeert, moet u ervoor zorgen dat de volgende CDX-taken worden uitgevoerd in Commerce headquarters:

- 1110 (Algemene configuratie)
- 1010 (Klanten)
- 1070 (Kanaalconfiguratie)

Gegevens die in de cache worden opgeslagen in CSU (Commerce Scale Unit) worden mogelijk niet direct weergegeven in Commerce headquarters nadat de CDX-taken zijn uitgevoerd.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Waarom wordt in Commerce headquarters het aanmaken of bijwerken van klanten vanaf het POS of e-commercekanaal niet getoond?

Controleer of de volgende acties zijn uitgevoerd in de volgorde waarin deze hier worden vermeld.

1. Voer de CDX P-taak in Commerce headquarters uit om ervoor te zorgen dat de klantgegevens die in de tabellen **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMEILIATION** en **RETAILASYNCCUSTOMERATTRIBUTEV2** zijn opgeslagen.
1. Voer de batchtaak **Klanten en kanaalaanvragen synchroniseren** uit in Commerce headquarters. Wanneer de batchtaak is uitgevoerd, is voor alle records die succesvol zijn verwerkt vanuit de eerder genoemde tabellen het veld **OnlineOperationCompleted** ingesteld op **1**.

### <a name="how-do-i-know-which-customer-management-in-asynchronous-mode-operation-has-failed-and-how-do-i-make-changes-if-they-are-required"></a>Hoe weet ik welk klantbeheer in een asynchrone modusbewerking is mislukt en hoe kan ik indien nodig wijzigingen aanbrengen?

Als u alle bewerken in asynchrone modus en hun synchronisatiestatus wilt weergeven, gaat u in Commerce headquarters naar **Commerce en Retail \> Klanten \> Synchronisatiestatus van klant**. Als u wijzigingen wilt aanbrengen, werkt u de velden bij, selecteert u **Opslaan** en selecteert u **Synchroniseren** om de wijzigingen te synchroniseren.

