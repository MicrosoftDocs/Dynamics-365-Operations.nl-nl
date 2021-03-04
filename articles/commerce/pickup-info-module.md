---
title: Module ophaalinformatie
description: In dit onderwerp wordt beschreven wat de ophaalinformatiemodule is en hoe u deze toevoegt aan uitcheckpagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 61b97d72b6a397737c10476cd6c02764e60f10b1
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665343"
---
# <a name="pickup-information-module"></a>Module ophaalinformatie

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven wat de ophaalinformatiemodule is en hoe u deze toevoegt aan uitcheckpagina's in Microsoft Dynamics 365 Commerce.

De module ophaalinformatie kan worden gebruikt in een uitcheckmodule om informatie over het ophalen van orders weer te geven. Klanten kunnen de beschikbare ophaaldatums en tijdvakken weergeven en vervolgens een geschikte tijd selecteren om de order op te halen. Een klant kan bijvoorbeeld kiezen om een order op te halen op 21 maart om 15.00 uur in de winkel in San Francisco.

Tijdvakken voor ophalen in de desbetreffende winkels moeten worden geconfigureerd in Commerce Headquarters. Zie [Tijdvakken voor ophalen door klanten maken en bijwerken](dev-itpro/pickup-timeslots.md) voor meer informatie.

Als er een ophaalinformatiemodule is gemaakt op een uitcheckpagina, maar er geen tijdvakken zijn gedefinieerd voor de winkel die is geselecteerd voor ophalen, wordt in de module informatie weergegeven, maar kan de gebruiker geen tijdvakken selecteren. Tijdvakken zijn optioneel en niet nodig om een order te plaatsen.

Als er meerdere artikelen zijn geselecteerd om te worden opgehaald in meerdere winkels, kan de gebruiker in de ophaalinformatiemodule een tijdvak selecteren voor elke winkel, mits er tijdvakken beschikbaar zijn.

> [!NOTE]
> Ondersteuning voor tijdvakken en de ophaalinformatiemodule is beschikbaar in Dynamics 365 Commerce versie 10.0.15 en hoger.

In de volgende afbeelding ziet u een voorbeeld van een tijdvakselectie via de ophaalinformatiemodule op een uitcheckpagina.

![Voorbeeld van een ophaalinformatiemodule voor verzendadressen op een betalingspagina](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Module-eigenschappen

- **Koptekst** - Voer een koptekst in voor de module.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Informatie over tijdvakken weergeven nadat een order is geplaatst

Nadat een order is geplaatst, kunt u informatie over het geselecteerde tijdvak weergeven in de [module orderbevestiging](order-confirmation-module.md) en de [module orderdetails](account-management.md#order-details-page). Beide modules hebben de eigenschap **Tijdvakinformatie weergeven**. Voordat ze de geselecteerde tijdvakken kunnen weergeven tijdens het orderproces, moet deze eigenschap worden ingesteld op **Waar**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Een ophaalinformatiemodule toevoegen op een betalingspagina

Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een ophaalinformatiemodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.

In de volgende afbeelding ziet u een voorbeeld van een e-commerce uitcheckpagina met tijdvakken voor het ophalen van artikelen.

![Voorbeeld van een e-commerce uitcheckpagina met tijdvakken voor het ophalen van artikelen](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Aanvullende bronnen

[Tijdvakken voor het ophalen door klanten maken en bijwerken](dev-itpro/pickup-timeslots.md)

[Kassamodule](add-checkout-module.md)

[Orderbevestigingsmodule](order-confirmation-module.md)

[Module voor orderdetails](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]