---
title: Betalingsmodule
description: In dit onderwerp wordt de betalingsmodule beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 894ac35973927c193d6e9c54e326daefb8a3f4a5
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055376"
---
# <a name="payment-module"></a>Betalingsmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de betalingsmodule beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

De betalingsmodule laat klanten betalen voor orders met behulp van creditcards of debitcards. Integratie van betalingen voor deze module wordt verzorgd door de Dynamics 365-betalingsconnector voor Adyen. Raadpleeg [Dynamics 365-betalingsconnector voor Adyen](dev-itpro/adyen-connector.md) voor meer informatie over het instellen en configureren van de Adyen-betalingsconnector.

De betalingsmodule beheert de betalingsgegevens die via Adyen in een HTML inline frame (iFrame) worden aangeleverd. De betalingsmodule communiceert met de Commerce Scale Unit om de Adyen-betalingsgegevens op te halen. Als onderdeel van de Commerce Scale Unit-interactie kan de betalingsmodule toestaan dat factuuradresgegevens worden verwerkt in het iFrame of als een afzonderlijke module. In het thema Fabrikam wordt het factuuradres in een aparte module weergegeven. Deze aanpak biedt meer flexibele opmaakmogelijkheden, omdat de adresregels zo kunnen worden weergegeven dat ze lijken op de regels van het verzendadres.

Aangemelde klanten kunnen in de betalingsmodule ook hun betalingsgegevens opslaan. De betalingsgegevens en het factuuradres worden opgeslagen en beheerd via de Adyen-betalingsconnector.

De betalingsmodule omvat alle orderkosten die nog niet zijn gedekt door loyaliteitspunten of een geschenkbon. Als het totaal van een order volledig wordt gedekt door loyaliteitspunten of geschenkbonnen, wordt de betalingsmodule verborgen en kan de klant de order zonder de module plaatsen.

De Adyen-betalingsconnector ondersteunt ook sterke klantverificatie (SCA). Als onderdeel van de EU-richtlijn voor betalingsdiensten 2.0 (PSD 2.0) van de Europese Unie is vereist dat online klanten worden geverifieerd buiten hun online winkelervaring wanneer ze een elektronische betalingsmethode gebruiken. Tijdens het afhandelingsverkeer worden klanten omgeleid naar hun banksite. Na de verificatie worden ze vervolgens omgeleid naar de Commerce-afhandelingsstroom. Tijdens deze omleiding blijft de informatie behouden die een klant heeft ingevoerd in de checkoutstroom (bijvoorbeeld het verzendadres, de leveringsopties, informatie over geschenkbonnen en loyaliteitsgegevens). Voordat u deze functie kunt inschakelen, moet de betalingsconnector worden geconfigureerd voor SCA in Commerce Headquarters. Zie voor meer informatie [Sterke klantverificatie met Adyen](adyen_redirect.md).

> [!NOTE]
> Voor de Adyen-betalingsconnector kan de iframe-module in de betalingsmodule alleen worden weergegeven als u de Adyen-URL toevoegt aan de toegestane lijst van uw site. Als u deze stap wilt uitvoeren, voegt u **\*adyen.com** toe aan de richtlijnen **child-src** , **connect-src** , **img-src** , **script-src** en **style-src** van het inhoudsbeveiligingsbeleid van uw site. Zie [Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md) voor meer informatie. 

De volgende afbeelding toont een voorbeeld van de modules voor geschenkbon, loyaliteitspunten en betaling op een uitcheckpagina.

![Voorbeeld van modules voor geschenkbonnen, loyaliteitspunten en betalingen op een uitcheckpagina](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Eigenschappen van betalingsmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Kop | Koptekst | Een optionele koptekst voor de betalingsmodule. |
| De hoogte van het iFrame. | Pixel | De hoogte van het iFrame, in pixels. De hoogte kan zo nodig worden aangepast. |
| Factureringsadres weergeven | **True** of **False** | Als deze eigenschap is ingesteld op **Waar** , wordt het factuuradres door Adyen geleverd binnen het iFrame van de betalingsmodule. Als de eigenschap is ingesteld op **Onwaar** , wordt het factuuradres niet aangeleverd door Adyen en moet een Commerce-gebruiker een module configureren om het factuuradres op de uitcheckpagina weer te geven. |
| Betalingsstijl overschrijven | Cascading Style Sheets-code (CSS) | Omdat de betalingsmodule wordt gehost in een iFrame, zijn er beperkte opmaakmogelijkheden. U kunt opmaak aanbrengen met behulp van deze eigenschap. Als u sitestijlen wilt overschrijven, plakt u de CSS-code als waarde voor deze eigenschap. Overschrijvingen en stijlen van site builder-CSS zijn niet van toepassing op deze module. |

## <a name="billing-address"></a>Factureringsadres

De betalingsmodule laat klanten een factuuradres opgeven voor hun betalingsgegevens. Ook kunnen ze hun verzendadres gebruiken als het factuuradres, zodat de afhandelingsprocedure eenvoudiger en sneller wordt. Als de eigenschap **Factureringsadres weergeven** is ingesteld op **Onwaar** , moet de betalingsmodule worden geconfigureerd op de uitcheckpagina.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Een betalingsmodule aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen

Een betalingsmodule kan alleen aan een uitcheckmodule worden toegevoegd. Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van een betalingsmodule voor een kassapagina.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Module winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Module voor verzendadressen](ship-address-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Geschenkbonmodule](add-giftcard.md)

[Dynamics 365-betalingsconnector voor Adyen](dev-itpro/adyen-connector.md)

[SCA (sterke klantverificatie) met Adyen-connector](adyen_redirect.md)
