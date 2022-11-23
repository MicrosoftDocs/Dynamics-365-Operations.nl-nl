---
title: Apple Pay met Adyen instellen in Dynamics 365 Commerce
description: In dit artikel wordt beschreven hoe u Apple Pay met Adyen instelt in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 0949b9d7a4b181605d43956932b4fc095940bd64
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780356"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Apple Pay met Adyen instellen in Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

In dit artikel wordt beschreven hoe u Apple Pay met Adyen instelt in Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Description |
|---|---|
| Apple Pay | Wordt ook wel de knop Apple Pay genoemd. Apple Pay is een walletbetalingsaanbod dat via de Adyen-connector wordt ondersteund. Hiermee worden de klantervaring en integratie mogelijk gemaakt die worden ondersteund door de Microsoft Dynamics 365 Apple Pay-connector. |
| Wallet | Een betalingstype dat geen traditionele betalingskenmerken bevat, zoals het BIN-bereik (Bank Identification Number) en de vervaldatum, die worden gebruikt om de creditcard- en betaalkaarttypen te onderscheiden. |

Dynamics 365 Commerce biedt een kant-en-klare integratie voor Apple Pay wanneer de Adyen-betalingsgatewayservice wordt gebruikt. Apple Pay is een digitale betalingswijze waarbij een Apple Pay-verkopersrekening wordt gebruikt in combinatie met de Adyen-betaalservice. Indien zo geconfigureerd, is de knop Apple Pay beschikbaar als een te selecteren betalingswijze op de betaalpagina van de online winkel. De knop Apple Pay wordt alleen als een betalingsoptie weergegeven voor ondersteunde Apple Pay-apparaten. Wanneer gebruikers **Apple Pay** in een ondersteunde browser of ondersteund apparaat selecteren, worden ze omgeleid naar de Apple Pay-service om de betaling rechtstreeks te voltooien. Vervolgens keren ze terug naar de online winkel om de order te voltooien.

De connectorverwijzing Dynamics 365 Payment Connector voor Apple Pay wordt gebruikt naast de Dynamics 365 Payment Connector voor Adyen zodat betalen via Apple Pay en creditcards op een site kunnen worden ingeschakeld. Apple Pay kan ook worden geconfigureerd voor gebruik in winkels met Adyen-betalingsterminals die de Dynamics 365 Payment Connector voor Adyen gebruiken met het Commerce-verkooppunt (POS). In dit geval verwerkt Dynamics 365 Payment Connector voor Adyen de tik op het Apple-betalingsapparaat via de terminal.

## <a name="prerequisites"></a>Vereisten

Voor het gebruik van Apple Pay met Adyen in Commerce is een Apple-verkopersrekening vereist. Informatie over het instellen van Apple Pay in uw testklantgebied vindt u in [Apple Pay-integraties insluiten](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Zie [Live gaan](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) voor informatie over wat u moet doen om live te gaan met uw productieomgeving.

De Apple Pay-betalingswijze moet ook met uw Adyen-rekening worden geïntegreerd. Adyen kan u helpen de betalingsmethode in te stellen en ervoor zorgen dat de domeinen waarvoor u het certificaat gebruikt, zijn toegewezen voor gebruik met het certificaat.

Ga naar **Werkgebieden \> Functiebeheer** en zoek naar de functie **Verbeterde walletondersteuning en betalingsverbeteringen**, om de functievlag Verbeterde walletondersteuning in Commerce headquarters in te schakelen. Selecteer de functie en selecteer **Inschakelen**. Nadat de functie is ingeschakeld, voert u de **1110**-distributieplanning uit om de wijziging beschikbaar te maken in alle kanalen.

## <a name="map-the-apple-pay-payment-method"></a>De Apple Pay-betalingswijze toewijzen

Apple Pay is een digitale walletbetalingswijze. Zie [Ondersteuning voor walletbetaling](../wallets.md) voor informatie over het instellen van betalingstoewijzing voor Apple Pay.

Volg deze stappen om de ApplePay-betalingswijze toe te wijzen in Commerce headquarters.

1. Ga naar **Retail en handel \> Afzetkanaalinstellingen \> Betalingswijzen \> Kaarttypen**.
1. Selecteer **Nieuw** om een regel voor Apple Pay toe te voegen en stel de volgende waarden in:

    - **ID:** ApplePay
    - **Naam elektronische betaling:** Apple Pay
    - **Type:** Wallet
    - **Uitgever:** Apple

1. Selecteer **Processortoewijzing** om het dialoogvenster **Toewijzingsmethoden voor processorbetaling** te openen. In de kolom **Niet-toegewezen betalingswijzen van processor** worden de ondersteunde betalingsmethoden voor elke beschikbare connector weergegeven (Adyen, PayPal en Apple).
1. Wijs de ondersteunde betalingswijzen toe die u wilt gebruiken voor zowel **Dynamics 365 Payment Connector voor Adyen** (voor gebruik op verkooppunten) als **Dynamics 365 Payment Connector voor Apple Pay** (voor het online kanaal).
1. Selecteer voor elke toewijzingsregel in de kolom **Niet-toegewezen betalingsmethoden van processor** de regel die u wilt ondersteunen en selecteer vervolgens **Toevoegen** om de selecties naar de kolom **Toegewezen betalingsmethoden van processor** te verplaatsen.
1. Selecteer **OK** en vervolgens **Opslaan** op de pagina **Kaarttypen**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Het Apple Pay-certificaat voor uw site instellen

Voor elke site moet u het domeinkoppelingsbestand uploaden (ook wel het Apple Pay-certificaat genoemd) zoals beschreven in [de documentatie bij Adyen Apple Pay](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). Met Commerce Site Builder kunt u het domeinkoppelingsbestand uploaden naar de Mediabibliotheek voor uw site.

Volg deze stappen om het Apple Pay-certificaat in te stellen in Site Builder.

1. Download het certificaat (domeinkoppelingsbestand) vanuit [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Voeg de txt-extensie toe aan het domeinkoppelingsbestand.
1. [Upload](../upload-serve-static-files.md) het domeinkoppelingsbestand in Site Builder naar de Mediabibliotheek van uw site.
1. Ga naar **URL's**.
1. Selecteer **Nieuw \> Nieuwe URL**.
1. Selecteer in het dialoogvenster **Nieuwe URL** de optie **Mediabibliotheekmaterialen**.
1. Voer in het veld **URL-pad** het URL-pad in (als dit nog niet is ingevoerd). Voer na de domeinbasis-URL de volgende vereiste Apple-reeks in: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`
1. Selecteer **Volgende**. De Mediabibliotheek toont alle mediamaterialen van het type **document** (.txt) dat zijn geüpload.
1. Selecteer het domeinkoppelingsbestand dat moet worden geleverd voor verzoeken naar de URL die u eerder hebt gedefinieerd.
1. Selecteer **Maken**.

Op dit moment bevindt de URL die u hebt gemaakt zich in een conceptstatus. Publiceer de URL om het proces te voltooien. Het bestand waarnaar de URL verwijst, wordt niet geretourneerd totdat u de URL publiceert.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Een online winkel voor Commerce configureren voor Apple Pay

Volg deze stappen om een online winkel voor Commerce te configureren voor Apple Pay.

1. Ga in Commerce headquarters naar **Retail en Commerce \> Kanalen \> Online winkels**.
1. Selecteer de waarde **Id van detailhandelafzetkanaal** voor het kanaal van de online winkel van uw site.
1. Voeg op het sneltabblad **Betalingsrekeningen** de **Dynamics 365 Payment Connector voor Adyen** toe, als dit nog niet is ingesteld, door de instructies in [Dynamics 365 Payment Connector voor Adyen instellen](adyen-connector-setup.md) te volgend.
1. Nadat de Adyen Connector is geconfigureerd, selecteert u **Toevoegen** om de **Dynamics 365 Payment Connector voor Apple Pay** toe te voegen.
1. Voer waarden in voor de verkopereigenschappen van de connector.

    | Eigenschap               | Description | Vereist | Automatisch ingesteld | Voorbeeldwaarde |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Assemblynaam          | De naam van de assembly voor Dynamics 365 Payment Connector voor Apple Pay. | Ja | Ja | Binaire naam |
    | Servicerekening-ID     | De unieke id van de instellingen voor de verkoperseigenschappen. Deze id wordt gebruikt voor betalingstransacties en identificeert de verkoperseigenschappen die in downstreamprocessen (zoals facturering) moeten worden gebruikt. | Ja | Ja | GUID |
    | Verkoperrekening-id    | Voer de unieke verkoper-id voor Adyen in. Deze waarde wordt verschaft wanneer u zich bij Adyen inschrijft zoals beschreven in [Aanmelden bij Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Ja | Nr. | MerchantIdentifier |
    | API-sleutel van cloud          | Voer de API-sleutel van de Adyen-cloud in. Volg de instructies in [De API-sleutel verkrijgen](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key) om deze sleutel te verkrijgen. | Ja | Nr. | abcdefg |
    | Gateway-omgeving    | Voer de Adyen-gatewayomgeving in waaraan moet worden toegewezen. De mogelijke waarden zijn **Test** en **Live**. Stel dit veld alleen in op **Live** voor productieapparaten en -transacties. | Ja | Ja | Live |
    | Ondersteunde valuta's   | Voer de valuta's in die via de connector moeten worden verwerkt. In scenario's met kaarten kan Adyen extra valuta's ondersteunen via [Dynamische valutaconversie](https://www.adyen.com/pos-payments/dynamic-currency-conversion) nadat de transactieaanvraag naar de betaalterminal is verzonden. Neem contact op met Adyen-ondersteuning voor een lijst met ondersteunde valuta's. | Ja | Ja | USD;EUR |
    | Ondersteunde betalingsmethoden | Voer de betalingstypen in die via de connector moeten worden verwerkt. | Ja | Ja | ApplePay |

1. Nadat de gegevens van de verkoper zijn ingevoerd, moet u de distributieplanningtaak **1070-kanaalconfiguratie** uitvoeren.

## <a name="configure-commerce-pos-for-apple-pay"></a>Verkooppunt (POS) van Commerce configureren voor Apple Pay

Voor de POS-configuratie wordt de configuratie van het veld **EFT-service** van het hardwareprofiel gebruikt voor Dynamics 365 Payment Connector voor Adyen. Configureer in Commerce headquarters de EFT-service voor Dynamics 365 Payment Connector voor Adyen, zoals wordt beschreven in [Een Dynamics 365 POS-hardwareprofiel instellen](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Zorg ervoor dat u **ApplePay** toevoegt aan de lijst met betalingstypen in het veld **Ondersteunde betalingsmethoden**. Gebruik puntkomma's (;) om de betalingsmethoden in de lijst van elkaar te scheiden.

Met de processortoewijzing voor de Adyen-connector worden de walletkaarttypen vastgelegd die door Apple Pay worden gebruikt op de POS-terminal.

### <a name="configure-content-security-policies-in-site-builder"></a>Inhoudsbeveiligingsbeleid configureren in Site Builder

Voordat u uw fragmenten of pagina´s configureert voor Apple Pay, moet u ervoor zorgen dat het inhoudsbeveiligingsbeleid (CSP) voor uw site is ingesteld in Commerce Site Builder.

Volg deze stappen om het beleid voor inhoudsbeveiliging te configureren in Site Builder.

1. Ga naar **Site-instellingen \> Extensies**.
1. Selecteer op het tabblad **Inhoudsbeveiligingsbeleid** **Toevoegen** om een regel met `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` toe te voegen aan de instructies **child-src**, **connect-src**, **frame-src**, **img-src**, **script-src** en **style-src**.
1. Wanneer u klaar bent, selecteert u **Opslaan en publiceren** om uw wijzigingen door te voeren.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Apple Pay instellen als een betalingsoptie op de afrekenpagina

Volg deze stappen om Apple Pay in te stellen als een betalingsoptie op de afrekenpagina (niet-spoed) van uw site.

1. Ga in Site Builder naar **Fragmenten** en selecteer het afrekenfragment van uw site.
1. Selecteer **Bewerken**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container voor uitchecksectie** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Apple Pay** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**.
1. Selecteer **Bewerken voltooien** om het fragment in te checken en selecteer **Publiceren** om te publiceren.

De instellingen voor de module **Apple Pay** worden ingebouwd en maken verbinding met de geconfigureerde Dynamics 365 Payment Connector voor Apple Pay die is ingesteld voor het online kanaal in Commerce headquarters.

### <a name="apple-pay-payment-behavior"></a>Gedrag van Apple Pay-betaling

De betalingsknop **Apple Pay** wordt alleen weergegeven op ondersteunde Apple Pay-apparaten (iPhones, iPads en Safari-browsers die Apple Pay ondersteunen). Als een gebruiker van niet een van deze apparaten gebruikt, wordt de knop **Apple Pay** verborgen.

Wanneer een gebruiker de knop **Apple Pay** selecteert, verschijnt het dialoogvenster **Apple Pay**. Hier kan de gebruiker zich verifiëren met het Apple Pay-apparaat of de browser. In het dialoogvenster **Apple Pay** wordt een overzicht weergegeven van het orderbedrag en de betalingsmethode die de gebruiker heeft geconfigureerd voor hun Apple Wallet. De gebruiker kan deze details bekijken en vervolgens **Betalen** selecteren om de betaling te voltooien. Nadat de betaling is voltooid, wordt de gebruiker doorverwezen naar de pagina **Order voltooid** met een gedetailleerd orderoverzicht voor de voltooide transactie.

## <a name="additional-resources"></a>Aanvullende bronnen

[Veelgestelde vragen over betalingen](payments-retail.md)

[Kassamodule](../add-checkout-module.md)

[Betalingsmodule](../payment-module.md)
