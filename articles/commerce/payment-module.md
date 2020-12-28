---
title: Betalingsmodule
description: In dit onderwerp wordt de betalingsmodule beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/18/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 27b73f7a05605e4e3ee8f8b72400172b7a8bfc33
ms.sourcegitcommit: ec78608eb96478b7a57928b60aece129d6799c5b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/19/2020
ms.locfileid: "4581907"
---
# <a name="payment-module"></a>Betalingsmodule

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de betalingsmodule beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.

De betalingsmodule laat klanten betalen voor orders met behulp van creditcards of debitcards. Integratie van betalingen voor deze module wordt verzorgd door de Dynamics 365-betalingsconnector voor Adyen. Raadpleeg [Dynamics 365-betalingsconnector voor Adyen](dev-itpro/adyen-connector.md) voor meer informatie over het instellen en configureren van de Adyen-betalingsconnector.  

Vanaf Commerce-versie 10.0.14 is de betalingsmodule ook geïntegreerd met de Dynamics 365-betalingsconnector voor PayPal zodat klanten ook met PayPal kunnen betalen. Raadpleeg [Dynamics 365-betalingsconnector voor Paypal](paypal.md) voor meer informatie over het instellen en configureren van de Dynamics 365-betalingsconnector voor PayPal. 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Dynamics 365-betalingsconnector voor Adyen 

De betalingsmodule beheert de betalingsgegevens die via Adyen in een HTML inline frame (iFrame) worden aangeleverd. De betalingsmodule communiceert met de Commerce Scale Unit om de Adyen-betalingsgegevens op te halen. Als onderdeel van de Commerce Scale Unit-interactie kan de betalingsmodule toestaan dat factuuradresgegevens worden verwerkt in het iFrame via Adyen of als een afzonderlijke module. In het thema Fabrikam wordt het factuuradres in een aparte module ingeschakeld. Deze aanpak biedt meer flexibele opmaakmogelijkheden, omdat de adresregels zo kunnen worden weergegeven dat ze lijken op de regels van het verzendadres.

Aangemelde klanten kunnen in de betalingsmodule ook hun betalingsgegevens opslaan. De betalingsgegevens en het factuuradres worden opgeslagen en beheerd via de Adyen-betalingsconnector.

De betalingsmodule omvat alle orderkosten die nog niet zijn gedekt door loyaliteitspunten of een geschenkbon. Als het totaal van een order volledig wordt gedekt door loyaliteitspunten of geschenkbonnen, wordt de betalingsmodule verborgen en kan de klant de order zonder de module plaatsen.

De Adyen-betalingsconnector ondersteunt ook sterke klantverificatie (SCA). Als onderdeel van de EU-richtlijn voor betalingsdiensten (PSD2) van de Europese Unie is vereist dat online klanten worden geverifieerd buiten hun online winkelervaring wanneer ze een elektronische betalingsmethode gebruiken. Tijdens de uitcheckstroom worden klanten omgeleid naar hun bankpagina en na de verificatie vervolgens teruggestuurd naar de commerce-uitcheckstroom. Tijdens deze omleiding blijft de informatie behouden die een klant heeft ingevoerd tijdens de checkoutstroom (bijvoorbeeld het verzendadres, de leveringsopties, informatie over geschenkbonnen en loyaliteitsgegevens). Voordat u de Adyen-betalingsconnector kunt inschakelen, moet deze worden geconfigureerd voor SCA in Commerce Headquarters. Zie voor meer informatie [Sterke klantverificatie met Adyen](adyen_redirect.md). Deze functie is ingeschakeld Commerce versie 10.0.12.

> [!NOTE]
> Voor de Adyen-betalingsconnector kan de iframe-module in de betalingsmodule alleen worden weergegeven als u de Adyen-URL toevoegt aan de toegestane lijst van uw site. Als u deze stap wilt uitvoeren, voegt u **\*adyen.com** toe aan de richtlijnen **child-src**, **connect-src**, **img-src**, **script-src** en **style-src** van het inhoudsbeveiligingsbeleid van uw site. Zie [Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md) voor meer informatie. 

De volgende afbeelding toont een voorbeeld van de modules voor geschenkbon, loyaliteitspunten en Adyen-betaling op een uitcheckpagina.

![Voorbeeld van modules voor geschenkbonnen, loyaliteitspunten en Adyen-betalingen op een uitcheckpagina](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365-betalingsconnector voor PayPal

Vanaf Commerce-versie 10.0.14 is de betalingsmodule ook geïntegreerd met de Dynamics 365-betalingsconnector voor PayPal. Raadpleeg [Dynamics 365-betalingsconnector voor PayPal](paypal.md) voor meer informatie over het instellen en configureren van deze betalingsconnector.
 
Op de pagina uitchecken kunt u zowel de Adyen als de PayPal-connectors configureren. De betalingsmodule is uitgebreid met aanvullende eigenschappen om te helpen bij het identificeren van de connector waarmee deze moet werken. Zie de module-eigenschappen in **Ondersteunde betalingsmethoden** en **Is primaire betaling** in de volgende tabel voor meer informatie.
  
Wanneer de betalingsmodule is geconfigureerd voor gebruik van de PayPal-betalingsconnector, wordt op de betalingspagina een PayPal-knop weergegeven. Wanneer de betalingsmodule door de klant wordt opgeroepen, wordt een IFRAME met PayPal-informatie gegenereerd. De klant kan zich aanmelden en hun PayPal-informatie in dit iframe ingeven om hun transactie te voltooien. Wanneer een klant betaalt voor betaling met PayPal, wordt het resterende saldo van de order in rekening gebracht via PayPal.

Voor de PayPal-betalingsconnector is geen factureringsadresmodule nodig, omdat alle informatie die met de facturering verband houdt, door PayPal wordt afgehandeld binnen het iFrame. De modules verzendadres en leveringsopties zijn echter wel verplicht.

In de volgende afbeelding ziet u een voorbeeld van twee betalingsmodules op een uitcheckpagina, één die is geconfigureerd met de Adyen-betalingsconnector en de andere met de betalingsconnector van PayPal.
![Voorbeeld van Adyen- en PayPal-modules op een uitcheckpagina](./media/ecommerce-paypal.png)

In de volgende afbeelding ziet u een voorbeeld van het PayPal-iFrame dat is opgeroepen via de PayPal-knop. 
![Voorbeeld van Paypal-iFrame op een uitcheckpagina](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Eigenschappen van betalingsmodule

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Kop | Koptekst | Een optionele koptekst voor de betalingsmodule. |
| De hoogte van het iFrame. | Pixel | De hoogte van het iFrame, in pixels. De hoogte kan zo nodig worden aangepast. |
| Factureringsadres weergeven | **True** of **False** | Als deze eigenschap is ingesteld op **Waar**, wordt het factuuradres door Adyen geleverd binnen het iFrame van de betalingsmodule. Als de eigenschap is ingesteld op **Onwaar**, wordt het factuuradres niet aangeleverd door Adyen en moet een Commerce-gebruiker een module configureren om het factuuradres op de uitcheckpagina weer te geven. Voor de PayPal-betalingsconnector heeft dit veld geen effect, omdat het factuuradres volledig wordt verwerkt binnen PayPal. |
| Betalingsstijl overschrijven | Cascading Style Sheets-code (CSS) | Omdat de betalingsmodule wordt gehost in een iFrame, zijn er beperkte opmaakmogelijkheden. U kunt opmaak aanbrengen met behulp van deze eigenschap. Als u sitestijlen wilt overschrijven, plakt u de CSS-code als waarde voor deze eigenschap. Overschrijvingen en stijlen van site builder-CSS zijn niet van toepassing op deze module. |
|Ondersteunde betalingsmethoden| Tekenreeks| Als er meerdere betalingsconnectors zijn geconfigureerd, moet u de ondersteunde reeks betalingstypes opgeven zoals gedefinieerd in de betalingsconnectorconfiguratie van Commerce Headquarters (zie de volgende afbeelding). Als deze leeg is, wordt standaard de Adyen-betalingsconnector gebruikt. Toegevoegd in Commerce-release 10.0.14.|
|Is primaire betaling|  **True** of **False** | Indien **Waar**, worden eventuele foutberichten gegenereerd door de primaire betalingsconnector op de uitcheckpagina. Als zowel Adyen- als PayPal-betalingsconnectors zijn geconfigureerd, stelt u Adyen in op **Waar**, die is toegevoegd in Commerce-versie 10.0.14.|

In de volgende afbeelding ziet u een voorbeeld van de **Ondersteunde betalingsmethoden** die zijn ingesteld op "PayPal" in de configuratie van betalingsconnector in Commerce Headquarters.
![Voorbeeld van ondersteunde betalingsmethoden in Commerce Headquarters](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Factuuradres

Een factuuradresmodule kan worden gebruikt op de uitcheckpagina als de factuuradresregels van de Adyen-betalingsconnector niet voldoende overeenkomen met de weergave van de rest van de site. 

Als u een factuuradresmodule op de uitcheckpagina wilt gebruiken wanneer de betalingsmodule is geïntegreerd met de Adyen-betalingsconnector, stelt u de eigenschap **Factuuradres weergeven** in op **Onwaar** zodat een toegewezen factuuradresmodule kan worden gebruikt in plaats van het standaard Adyen-factuuradres. In dit geval moet de auteur van de site een factuuradresmodule op de uitcheckpagina opnemen. Met de Adyen-betalingsconnector kan ook het verzendadres als factuuradres worden gebruikt om het aantal stappen voor de sitegebruiker te minimaliseren.

Net als bij betalingsmodules, is een eigenschap **Ondersteunde betalingsmethoden** toegevoegd aan de factuuradresmodule in Commerce-versie 10.0.14. De waarde van deze eigenschap moet gelijk zijn aan de waarde in de betalingsmodule om er zeker van te zijn dat ze samenwerken. Voor de Adyen-betalingsconnector moeten de betalingsmodule en de factuuradresmodule deze waarde leeg laten (de standaard status). Voor de PayPal-connector is een speciale factuuradresmodule niet vereist. Voor andere typen betalingsconnectors moet de tekenreeks worden opgegeven zoals deze is geconfigureerd in Commerce Headquarters.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Een betalingsmodule aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen

Een betalingsmodule kan alleen aan een uitcheckmodule worden toegevoegd. Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van een betalingsmodule voor een kassapagina.

Als zowel Adyen- als PayPal-betalingsconnectors nodig zijn, voegt u beide modules aan de sectie betaling toe. Zorg ervoor dat de eigenschapswaarde **Ondersteunde betalingsmethoden** is geconfigureerd voor PayPal en laat het veld leeg voor Adyen. Stel ook de eigenschap **Is primaire betaling** in op **Waar** voor Adyen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Winkelwagenmodule](add-cart-module.md)

[Module voor winkelwagenpictogram](cart-icon-module.md)

[Kassamodule](add-checkout-module.md)

[Module voor verzendadressen](ship-address-module.md)

[Module voor leveringsopties](delivery-options-module.md)

[Module ophaalinformatie](pickup-info-module.md)

[Module voor orderdetails](order-confirmation-module.md)

[Geschenkbonmodule](add-giftcard.md)

[Dynamics 365-betalingsconnector voor Adyen](dev-itpro/adyen-connector.md)

[Dynamics 365-betalingsconnector voor PayPal](paypal.md)

[SCA (sterke klantverificatie) met Adyen-connector](adyen_redirect.md)
