---
title: Google Pay met Adyen configureren
description: In dit artikel wordt beschreven hoe u Google Pay met Adyen kunt configureren in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115026"
---
# <a name="configure-google-pay-with-adyen"></a>Google Pay met Adyen configureren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u Google Pay met Adyen kunt configureren in Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce biedt een kant-en-klare integratie voor Google Pay wanneer de Adyen-betalingsgatewayservice wordt gebruikt. Google Pay is een digitale betalingswijze waarbij een Google Pay-verkopersrekening wordt gebruikt in combinatie met de Adyen-betaalservice. Indien zo geconfigureerd, is de knop Google Pay beschikbaar als een te selecteren betalingswijze tijdens het online afrekenen van de order. Wanneer gebruikers **Google Pay** in een ondersteunde browser of ondersteund apparaat selecteren, worden ze omgeleid om de betaling rechtstreeks met de Google Pay-service te voltooien. Vervolgens keren ze terug naar de online winkel om de order te voltooien.

Wanneer Google Pay wordt gebruikt met de module voor snel afrekenen in Commerce, worden de betalingsrekeninggegevens van de gebruiker automatisch vooraf ingevuld in het afrekenformulier zodat de gebruiker het afrekenproces sneller kan doorlopen. Commerce bevat een module voor snel betalen waarmee snel kan worden afgerekend. Deze module kan worden gebruikt in een fragment dat wordt opgenomen op de afreken- of winkelwagenpagina. De connectorverwijzing Dynamics 365 Payment Connector voor Google Pay wordt gebruikt naast de Dynamics 365 Payment Connector voor Adyen zodat zowel opties voor snel betalen als normale afrekenopties kunnen worden ingeschakeld als PayPal is geconfigureerd. Google Pay kan ook worden geconfigureerd met Adyen-betaalterminals en het Commerce-verkooppunt voor gebruik in de winkel.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Description |
|---|---|
| Google Pay | Wordt ook wel de "knop" Google Pay genoemd. Google Pay is een walletbetalingsaanbod dat via de Adyen-connector wordt ondersteund. Hiermee worden de klantervaring en integratie mogelijk gemaakt die worden ondersteund door de Dynamics Google Pay Connector. |
| Wallet | Een betalingstype dat geen traditionele betalingskenmerken bevat, zoals het BIN-bereik (Bank Identification Number) en de vervaldatum, die worden gebruikt om de creditcard- en betaalkaarttypen te onderscheiden. |
| Module voor snelle betaling | Een Dynamics 365 Commerce-module die sneller afrekengedrag ondersteunt wanneer ondersteunde betalingswijzen worden gebruikt. |

## <a name="prerequisites"></a>Vereisten

Voor het gebruik van Google Pay met Adyen in Commerce is een Google-verkopersrekening vereist. Zie de [Adyen-documentatie voor Google Pay](https://docs.adyen.com/payment-methods/google-pay/) en [Controlelijst voor integratie](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist) voor informatie over het instellen van uw Google-verkopersrekening.

De Google Pay-betalingswijze moet ook met uw Adyen-rekening worden geïntegreerd. Zie [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay) voor instructies voor integratiekoppelingen.

U moet ook de verbeterde walletfunctie in Dynamics 365 Commerce Headquarters inschakelen. Ga naar **Werkgebieden \> Functiebeheer**, zoek naar de functie **Verbeterde walletondersteuning en betalingsverbeteringen**, selecteer de functie en selecteer vervolgens **Inschakelen**. Nadat de functie is ingeschakeld, voert u de **1110**-distributieplanning uit om de wijziging beschikbaar te maken in alle kanalen.

## <a name="map-the-google-pay-payment-method"></a>De Google Pay-betalingswijze toewijzen

Google Pay is een digitale walletbetalingswijze. Zie [Ondersteuning voor walletbetaling](../wallets.md) voor informatie over het instellen van betalingstoewijzing voor Google Pay.

Voer de volgende stappen uit als u de Google Pay-betalingswijze wilt toewijzen aan kaartbetalingsmethoden voor zowel verkooppunten als online kanalen.

1. Ga in Commerce Headquarters naar **Retail en commerce \> Afzetkanaalinstellingen \> Betalingswijzen \> Kaarttypen**.
1. Selecteer **Nieuw** om een regel voor Google Pay toe te voegen.
1. Geef in het veld **Id** **GooglePay** op.
1. Typ **Google Pay** in het veld **Naam elektronische betaling**.
1. Voer in het veld **Type** **Wallet** in.
1. Voer in het veld **Verlener** **Google** in.
1. Selecteer in het actievenster **Processortoewijzing** om het dialoogvenster **Toewijzingsmethoden voor processorbetaling** te openen.
1. Onder **Niet-toegewezen betalingswijzen van processor** ziet u een lijst met betalingswijzen voor niet-gekoppelde processoren, die elk zijn gekoppeld aan de juiste connector. Voer de volgende stappen uit om niet-toegewezen Google Pay-betalingswijzen van processor toe te wijzen aan elke kaartbetalingsmethode:

    1. Selecteer onder **Kaartbetalingsmethoden** een kaartbetalingstype.
    1. Selecteer in de kolom **Niet-toegewezen betalingswijzen van processor** zowel **Dynamics 365 Payment Connector voor Adyen** (voor gebruik op verkooppunten) als **Dynamics 365 Payment Connector voor Google Pay** (voor gebruik in online kanalen).
    1. Selecteer **Toevoegen**. De selecties worden toegevoegd aan de kolom **Toegewezen betalingswijzen van processor**.

1. Wanneer u klaar bent met het toewijzen van betalingswijzen, selecteert u **Opslaan**.
1. Selecteer **Opslaan** op de pagina **Kaarttypen**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Een online winkel voor Commerce configureren voor Google Pay

Volg deze stappen om een online winkel voor Commerce te configureren voor het gebruik van Google Pay.

1. Ga in Commerce Headquarters naar **Retail en Commerce \> Kanalen \> Online winkels**.
1. Selecteer het kanaal van de online winkel van uw site door de waarde **Id van detailhandelafzetkanaal** te selecteren.
1. Controleer op het sneltabblad **Betalingsrekeningen** onder **Connector** of de connector **Dynamics 365 Payment Connector voor Adyen** wordt weergegeven. Als deze niet wordt weergegeven, volgt u de instructies in [Dynamics 365 Payment Connector voor Adyen instellen](adyen-connector-setup.md) om deze toe te voegen.

    > [!NOTE]
    > In de meeste gevallen moet de connector **Dynamics 365 Payment Connector voor Adyen** worden weergegeven als de eerste connector voor uw kanaal (de eerste connector wordt ook wel de primaire connector genoemd). Vervolgens moet deze worden gevolgd door andere connectoren die worden gebruikt, zoals de connector **Dynamics 365 Payment Connector voor PayPal** en de connector **Dynamics 365 Payment Connector voor Google Pay**.

1. Nadat de connector **Dynamics 365 Payment Connector voor Adyen** is toegevoegd, selecteert u **Toevoegen** om de connector **Dynamics 365 Payment Connector voor Google Pay** toe te voegen. Stel vervolgens de volgende eigenschappen voor de connector in.

    | Veld                  | Description | Vereist | Automatisch ingesteld | Voorbeeldwaarde |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Assemblynaam          | De naam van de assembly voor Dynamics 365 Payment Connector voor Google Pay. | Ja | Ja | *Binaire naam* |
    | Servicerekening-ID     | De unieke id voor de instellingen van de verkoperseigenschappen. Deze id wordt gebruikt voor betalingstransacties en identificeert de verkoperseigenschappen die in downstreamprocessen (zoals facturering) moeten worden gebruikt. | Ja | Ja | *GUID* |
    | Verkoper-id voor Google     | Voer de verkoper-id voor Google in die is toegewezen aan uw verkopersrekening voor Google. Deze eigenschap is vereist voor productieomgevingen, maar is optioneel voor testomgevingen. Ga naar <https://pay.google.com/> voor meer informatie. | Ja | Nr. | *Numerieke id* |
    | Verkoperrekening-id    | Voer de unieke verkoper-id voor Adyen in. Deze waarde wordt verschaft wanneer u zich bij Adyen inschrijft zoals beschreven in [Aanmelden bij Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Ja | Nr. | *Verkoper-id* |
    | API-sleutel van cloud          | Voer de API-sleutel van de Adyen-cloud in. Volg de instructies in [De API-sleutel verkrijgen](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key) om deze sleutel te verkrijgen. | Ja | Nr. | "abcdefg" |
    | Gateway-omgeving    | De Adyen-gatewayomgeving waaraan moet worden toegewezen. De mogelijke waarden zijn **Test** en **Live**. Stel dit veld alleen in op **Live** voor productieapparaten en -transacties. | Ja | Ja | "Live" |
    | Ondersteunde valuta's   | De valuta's die via de connector moeten worden verwerkt. In scenario's met kaarten kan Adyen extra valuta's ondersteunen via [Dynamische valutaconversie](https://www.adyen.com/pos-payments/dynamic-currency-conversion) nadat de transactieaanvraag naar de betaalterminal is verzonden. Neem contact op met Adyen-ondersteuning voor een lijst met ondersteunde valuta's. | Ja | Ja | "USD;EUR" |
    | Ondersteunde betalingsmethoden | De betalingstypen die via de connector moeten worden verwerkt. | Ja | Ja | "GooglePay" |

1. Nadat u de connectoreigenschappen hebt ingesteld, moet u de distributieplanningstaak **1070 (kanaalconfiguratie)** uitvoeren.

## <a name="configure-commerce-pos-for-google-pay"></a>Verkooppunt (POS) van Commerce configureren voor Google Pay

Voor de POS-configuratie wordt de instelling van het veld **EFT-service** van het hardwareprofiel gebruikt voor Dynamics 365 Payment Connector voor Adyen. Zie voor informatie over het configureren van de EFT-service (Electronic Funds Transfer) voor Dynamics 365 Payment Connector voor Adyen in Commerce Headquarters het gedeelte [Een Dynamics 365 POS-hardwareprofiel instellen](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Met de processortoewijzing voor de Adyen-connector worden de walletkaarttypen vastgelegd die door Google Pay worden gebruikt op de POS-terminal.

### <a name="use-the-payment-express-module-with-google-pay"></a>De module voor snelle betaling gebruiken met Google Pay

De module voor snelle betaling van Commerce werkt met ondersteunende betalingswijzen om klanten van de site de mogelijkheid te bieden sneller af te rekenen door hun rekeninggegevens van de betaalservice vooraf in te vullen tijdens het afrekenproces. De module voor snelle betaling verwijst naar de geconfigureerde connectorknop en retourneert de door de gebruiker geselecteerde ordergegevens (het adres, de contactgegevens en de betalingswijze) om het afrekenformulier vooraf in te vullen.

Wanneer de module voor snelle betaling wordt gebruikt met Google Pay en als klanten de knop Google Pay in de sectie **Snelle betaling** selecteren, wordt het iframe-venster van Google Pay geopend. Gebruikers kunnen zich vervolgens aanmelden bij hun Google-rekening om het verzendadres, het factuuradres, het e-mailadres en de Google Pay-betalingswijze op te geven voor de transactie.

Wanneer de gebruikers de actie in het Google Pay-venster hebben voltooid, worden ze omgeleid naar de afrekenpagina van de Commerce-site, waar het afrekenformulier vooraf is ingevuld met hun Google Pay-rekeninggegevens. Wanneer gebruikers terugkeren naar de afrekenpagina van het Google Pay-venster, zien ze de volgende details:

- In de stroom voor snelle betaling wordt de eerste leveringsoptie die beschikbaar is voor het verzendadres dat is geretourneerd, vooraf geselecteerd voor de klant.
- Wanneer Google Pay wordt gebruikt, wordt geen e-mailadres van de contactpersoon geretourneerd. Gastgebruikers die afrekenen moeten een e-mailadres invoeren in de sectie Contactpersoon van de afrekenpagina. Voor aangemelde gebruikers worden de contactgegevens automatisch ingevuld via de Dynamics-klantrekening (het primaire e-mailadres dat ze hebben gebruikt voor verificatie).

Klanten hebben de mogelijkheid om orders te controleren en orderdetails voor afrekenen te wijzigen voordat ze **Order plaatsen** selecteren om de order te voltooien.

### <a name="configure-google-pay-in-site-builder"></a>Google Pay in Site Builder configureren 

Voordat u uw fragmenten of pagina´s configureert met Google Pay, moet u ervoor zorgen dat uw inhoudsbeveiligingsbeleid voor uw site is ingesteld in Commerce Site Builder.

Volg deze stappen om er zeker van te zijn dat uw beleid voor inhoudsbeveiliging is ingesteld in Site Builder.

1. Ga op uw site naar **Site-instellingen \> Extensies**.
1. Voeg op het tabblad **Inhoudsbeveiligingsbeleid** een regel voor `*.google.com` toe aan de instructies **child-src**, **connect-src**, **frame-ancestors**, **frame-src**, **img-src**, **script-src** en **style-src**.
1. Wanneer u klaar bent, selecteert u **Opslaan en publiceren**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Het fragment voor snelle betaling configureren voor Google Pay in Site Builder

Volg deze stappen om het fragment voor snelle betaling met Google Pay in te stellen voor de online winkel.

1. Ga naar **Fragmenten** in Site Builder.
1. Selecteer **Nieuw**.
1. Selecteer in het dialoogvenster **Nieuw fragment** de module **Container**, voer een naam in voor het fragment (bijvoorbeeld **Snel afrekenen**) en selecteer vervolgens **OK**. 
1. Selecteer het vak **Standaardcontainer** van het nieuwe fragment.
1. Voer in het eigenschappenvenster rechts de eigenschappen in voor de containermodule:

    - **Kop**: voer een kop in die u wilt weergeven voor de sectie Snel afrekenen van uw site (bijvoorbeeld **Snel afrekenen**).
    - **Containerindeling**: selecteer **Stroom**.
    - **Breedte**: selecteert **Container vullen**.
    - **Onderliggende items weergegeven**: selecteer **Drie** om het aantal onderliggende items op te geven dat past in een rij van de sectie Snel afrekenen (bijvoorbeeld een tekstvak, snelle betaling voor PayPaL en snelle betaling voor Google Pay).
    - **CSS-klassenaam**: voer **msc-express-payment-container** in (vereist).

    > [!IMPORTANT]
    > - De waarde **CSS-klassenaam** moet worden ingesteld op **msc-express-payment-container** om het gedrag van de container tijdens het afrekenen te bepalen. Dit gedrag omvat verbergen, samenvouwen en andere acties die van toepassing zijn op de sectie Snel afrekenen tijdens de afrekenstroom. De klasse **msc-express-payment-container** werkt met de standaardbewerkingen die worden vrijgegeven met de module Afrekenen van de modulebibliotheek.
    > - Voor de **CSS-klassenaam** kunnen extra stijlen worden opgenomen. Als u het gedrag van de module aanpast, controleer dan de stijlbesturingselementen goed als u hetzelfde met de modulebibliotheek gecodeerde gedrag in de afrekenmodule gebruikt voor het gedrag van snel afrekenen.

1. Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Snelle betaling** en selecteer vervolgens **OK**.
1. In het eigenschappenvenster van de module **Snelle betaling** kunt u de waarde **Hoogte van iFrame** in pixels (bijvoorbeeld **60**) instellen of aanpassen.
1. Voer in het veld **Ondersteunde betalingsmethoden** de optie **Google Pay** in. De waarde moet overeenkomen met de tekenreeks **Ondersteunde betalingsmethoden** in de connector die is ingesteld voor het kanaal (zoals is beschreven in de sectie [Een online winkel voor Commerce configureren voor Google Pay](#configure-a-commerce-online-store-for-google-pay), eerder in dit artikel).

    > [!NOTE]
    > U kunt stap 6 tot en met 9 herhalen om **Snelle betaling** toe te voegen voor andere betalingswijzen. Lijn de waarde voor **Ondersteunde betalingsmethoden** uit met de extra geconfigureerde betalingstypen (bijvoorbeeld **Paypal**).

1. Optioneel: u kunt een tekstblokmodule toevoegen aan de standaardcontainermodule om instructies of openbaarmakingsinformatie op te nemen. Nadat u de module hebt toegevoegd, voert u in het eigenschappenvenster de gewenste tekst in het veld **Tekst met opmaak**. U kunt de tekst boven of onder de modules voor snelle betaling plaatsen door het beletselteken (**...**) te selecteren in het vak **Tekstblok** en vervolgens **Omhoog** of **Omlaag** te selecteren.
1. Selecteer **Opslaan** om uw wijzigingen op te slaan en vervolgens **Bewerken voltooien** te selecteren.
1. Selecteer **Publiceren** om het fragment te publiceren.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Het fragment voor snelle betaling aan de afrekenpagina toevoegen

Voer de volgende stappen uit om het fragment voor snelle betaling aan de afrekenpagina toe te voegen.

1. Ga in Site Builder naar **Pagina's** en selecteer vervolgens de afrekenpagina van uw site.
1. Selecteer **Bewerken**.
1. Selecteer in **Hoofdvak** het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster rechts de eigenschappen in voor de containermodule:

    - **Containerindeling**: selecteer **Gestapeld**.
    - **Breedte**: selecteert **Container vullen**.
    - **Onderliggende items weergegeven**: selecteer **Drie** om het aantal onderliggende items op te geven dat past in een rij van de sectie Snel afrekenen (bijvoorbeeld een tekstvak, snelle betaling voor PayPaL en snelle betaling voor Google Pay).

1. Selecteer in het modulevak **Container** het beletselteken (**...**) en selecteer vervolgens **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Een fragment selecteren** het fragment voor snelle betaling dat u hebt gemaakt en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** om uw wijzigingen op te slaan en vervolgens **Bewerken voltooien** te selecteren.
1. Selecteer **Publiceren** om de pagina te publiceren.

> [!NOTE]
> Als de afrekenpagina al een container bevat met het afrekenfragment en u wilt dat de module voor snelle betaling boven de normale afrekencontainer wordt weergegeven, kunt u deze boven of onder de bestaande afrekening plaatsen door het beletselteken (**...**) te selecteren in **Hoofdvak** en vervolgens **Omhoog** of **Omlaag** te selecteren.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Het fragment voor snelle betaling aan de winkelwagenpagina toevoegen

Voer de volgende stappen uit om het fragment voor snelle betaling aan de winkelwagenpagina toe te voegen.

1. Ga in Site Builder naar **Pagina's** en selecteer vervolgens de winkelwagenpagina van uw site.
2. Selecteer **Bewerken**.
3. Vouw in de overzichtsweergave **Hoofdvak** in de structuurweergave uit en zoek de container met de module **Winkelwagen**.
4. Selecteer in de module **Winkelwagen** het vak **Snelle betaling**, selecteer het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
5. Selecteer in het dialoogvenster **Modules selecteren** de module **Snelle betaling** en selecteer vervolgens **OK**.
6. Selecteer het vak van de module **Snelle betaling**. Voer vervolgens in het eigenschappenvenster aan de rechterkant onder **Ondersteunde betalingsmethoden** **GooglePay** in. De waarde moet overeenkomen met de tekenreeks **Ondersteunde betalingsmethoden** in de connector die is ingesteld voor het kanaal (zoals is beschreven in de sectie [Een online winkel voor Commerce configureren voor Google Pay](#configure-a-commerce-online-store-for-google-pay), eerder in dit artikel).
1. Selecteer **Opslaan** om uw wijzigingen op te slaan en vervolgens **Bewerken voltooien** te selecteren.
1. Selecteer **Publiceren** om de pagina te publiceren.

Gebruikers kunnen maximaal drie ondersteunde modules voor **Snelle betaling** opnemen (met andere woorden: drie beschikbare ondersteunde betalingsopties) in het vak **Snelle betaling** van de winkelwagen.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Google Pay instellen als een optie in de sectie Betaling afrekenen

U kunt Google Pay instellen als een optie in de sectie voor het afrekenen van betalingen voor alleen betaling, niet voor snelle betaling. Het afrekenformulier wordt ingevuld door de gebruiker en op de betalingspagina van Google Pay kunnen alleen betalingen door Google Pay worden afgerekend. Er worden geen Google Pay-rekeninggegevens gebruikt om de ingevulde afrekengegevens te overschrijven.

> [!NOTE]
> In de volgende procedure wordt ervan uitgegaan dat uw site een afrekenfragment gebruikt dat is geconfigureerd met ophaalgegevens, een verzendadres, leveringsopties, contactgegevens, optionele algemene voorwaarden en een sectie voor afrekenelementen. De standaardafrekenmodule van de modulebibliotheek wordt vrijgegeven met een afrekensectiecontainer die tekstblokken, loyaliteitspunten, geschenkbonnen en betalingsmodules bevat. Zie [Betalingsmodule](../payment-module.md) voor meer informatie.

Volg deze stappen om Google Pay in te stellen als een normale betalingsoptie in de sectie **Betalingswijze** van de afrekenpagina.

1. Ga in Site Builder naar **Fragmenten** en selecteer vervolgens het afrekenfragment van uw site.
1. Selecteer **Bewerken**.
1. Selecteer in het vak **Kassagegevens** het beletselteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Betaling** en selecteer vervolgens **OK**.
1. Stel in het eigenschappenvenster van de module **Betaling** aan de rechterkant de eigenschappen in voor de containermodule:

    - **Kop**: voer een kop in die u wilt weergeven voor de sectie Snel afrekenen van uw site (bijvoorbeeld **Google Pay**).
    - **Hoogte van iFrame**: wijzig de waarde in de gewenste ontwerphoogte in pixels (bijvoorbeeld **75**). 
    - **Ondersteunde betalingsmethoden**: voer **Google Pay** in zodat dit overeenkomt met de configuratie voor de Google Pay-connector in Commerce Headquarters.
    - **Is primaire betaling**: laat het selectievakje uitgeschakeld. (Deze eigenschap wordt meestal ingeschakeld voor de afrekenmodule Adyen.)
    - **Betalingsstijl overschrijven**: deze eigenschap wordt niet ondersteund voor de Google Pay-configuratie.
    - **Connector-id gebruiken**: deze eigenschap moet worden geselecteerd als er meerdere betalingsconnectoren worden gebruikt op de pagina.

1. Plaats de module boven of onder andere betalingsmodules door het beletselteken (**...**) te selecteren in het vak **Betaling** en vervolgens **Omhoog** of **Omlaag** te selecteren.
1. Selecteer **Opslaan** om uw wijzigingen op te slaan en vervolgens **Bewerken voltooien** te selecteren.
1. Selecteer **Publiceren**.

### <a name="modes-of-delivery"></a>Leveringsmethoden

Bij de module voor snelle betaling die wordt gebruikt door Google Pay, wordt de eerste leveringsoptie die wordt geretourneerd voor het verzendadres dat is geselecteerd voor de Google Pay-rekening, vooraf geselecteerd. Gebruikers kunnen desgewenst het verzendadres aan een andere optie aanpassen.

De volgorde waarin de leveringsmethoden worden weergegeven in de module Snelle betaling, wordt geconfigureerd op de pagina **Leveringsmethoden** van het kanaal in Commerce Headquarters. Ga in Commerce Headquarters naar **Retail en Commerce \> Kanalen \> Online winkels** en selecteer de waarde **Id van detailhandelafzetkanaal** voor uw winkel. Selecteer in het actievenster op het tabblad **Instellingen** de optie **Leveringsmethoden**. De weergegeven leveringsmethoden worden in dezelfde volgorde weergegeven in de module Snelle betaling. Als u leveringsmethoden voor een detailhandelkanaal of -product wilt toevoegen of verwijderen, selecteert u **Leveringsmethoden beheren** in het actievenster. Zie [Leveringsmethoden instellen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor meer informatie over het instellen van leveringsmethoden.

In de afrekenmodule wordt ook de module voor leveringsopties gebruikt wanneer leveringsmethoden tijdens het afrekenen worden weergegeven. Zie [Module voor leveringsopties](../delivery-options-module.md) voor meer informatie.

Leveringsmethoden worden weergegeven wanneer ze worden toegevoegd aan de lijst **Leveringsmethoden** in de online winkel.

## <a name="additional-resources"></a>Aanvullende bronnen

[Veelgestelde vragen over betalingen](payments-retail.md)

[Kassamodule](../add-checkout-module.md)

[Betalingsmodule](../payment-module.md)
