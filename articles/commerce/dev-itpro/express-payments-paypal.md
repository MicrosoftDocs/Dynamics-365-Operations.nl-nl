---
title: Spoedbetalingen configureren voor PayPal
description: In dit onderwerp wordt beschreven hoe u spoedbetalingen voor PayPal kunt configureren om sneller uit te checken in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5fff17959e7ed9299df169c68b2ed07f6b7c7d2c
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743567"
---
# <a name="configure-express-payments-for-paypal"></a>Spoedbetalingen configureren voor PayPal

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u spoedbetalingen voor PayPal kunt configureren om sneller uit te checken in Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Description |
|---|---|
| PayPal Wallet | De klantervaring en integratie die worden ondersteund door de PayPal-connector. Dit wordt ook wel de PayPal-knop genoemd. |
| Portemonnee | Een betalingstype dat geen traditionele betalingskenmerken bevat, zoals het BIN-bereik (Bank Identification Number) en de vervaldatum, die worden gebruikt om de creditcard- en betaalkaarttypen te onderscheiden. |
| Snelle betaling | Een Commerce-module die sneller afrekengedrag ondersteunt wanneer ondersteunde betalingswijzen worden gebruikt. In dit onderwerp wordt het gebruik van de module voor snelle betaling met PayPal besproken. |

Dynamics 365 Commerce biedt een kant-en-klare integratie voor PayPal Wallet. Wanneer de Dynamics 365 Payment Connector voor PayPal is geconfigureerd, wordt de PayPal-knop weergegeven als een te selecteren betalingswijze tijdens het afrekenen van online orders. Wanneer gebruikers PayPal selecteren, worden ze omgeleid om hun betaling rechtstreeks via PayPal te voltooien en keren ze vervolgens terug naar de online winkel om de order te voltooien. Met PayPal-betalingen via het winkelwagentje kunnen klanten hun betalingsrekeninggegevens gebruiken om het formulier voor afrekenen vooraf in te vullen, zodat ze het proces sneller kunnen voltooien.

Commerce heeft een module voor snelle betaling toegevoegd om snel afrekenen te vergemakkelijken. Deze module kan worden gebruikt in een fragment dat kan worden opgenomen op een afreken- of winkelwagenpagina. Wanneer PayPal is geconfigureerd, wordt dezelfde Dynamics 365 Payment Connector voor PayPal-connectorverwijzing gebruikt voor de optie voor snelle betaling en de normale afrekenoptie.

## <a name="paypal-checkout-in-commerce"></a>Via PayPal afrekenen in Commerce

### <a name="prerequisites"></a>Vereisten

Stel PayPal Wallet voor uw omgeving in zoals wordt beschreven in [Dynamics 365 Payment Connector voor PayPal](../paypal.md).

Als u PayPal als optie gebruikt in de normale afrekenstroom (waarbij gebruikers hun rekeninggegevens handmatig invoeren zonder de acties van de module voor snelle betaling voor vooraf invullen te gebruiken), volgt u de instellingsinstructies in [Betalingsmodule](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Module voor snelle betaling met PayPal

De module voor snelle betaling werkt met ondersteunende betalingswijzen om klanten van de site de mogelijkheid te bieden sneller af te rekenen door hun rekeninggegevens van de betaalservice vooraf in te vullen tijdens het afrekenproces. De module voor snelle betaling gebruikt de geconfigureerde betalingsconnector om het afrekenformulier vooraf te vullen met gebruikersrekeninggegevens, zoals het adres, de contactgegevens en de geselecteerde betalingsmethode.

Wanneer snel afrekenen met PayPal wordt gebruikt en een gebruiker de knop PayPal selecteert in de sectie voor snelle betaling van de afrekenpagina, wordt een iFrame-venster voor PayPal-betaling geopend. De gebruiker meldt zich vervolgens aan bij de PayPal-rekening om het verzendadres, het factuuradres, het e-mailadres en de PayPal-betalingsmethode op te geven voor de transactie.

Nadat de gebruiker de actie in het PayPal-venster heeft voltooid, wordt deze weer omgeleid naar de afrekenpagina van de Commerce-site, waar het afrekenformulier vooraf is ingevuld met de geselecteerde details. In de stroom voor snelle betaling wordt de eerste leveringsoptie die beschikbaar is voor het verzendadres dat wordt geretourneerd vooraf ingevuld voor de gebruiker. De gebruiker heeft vervolgens de mogelijkheid om de order te controleren en details van de afrekenorder te wijzigen voordat deze **Order plaatsen** selecteert om de order te voltooien.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>De module voor snelle betaling met PayPal toevoegen aan een fragment

Voer de volgende stappen uit om de module voor snelle betaling met PayPal toe te voegen aan een fragment in Commerce Site Builder.

1. Ga naar uw site.
1. Selecteer **Fragmenten** in het navigatievenster links en selecteer **Nieuw**.
1. Selecteer in het dialoogvenster **Nieuw fragment** de module **Snelle betaling** en voer vervolgens onder **Naam fragment** een naam in voor het fragment (bijvoorbeeld **Snel afrekenen**).
1. Selecteer **OK** om het fragment te maken.
1. Selecteer in de overzichtsweergave het slot van de module voor snelle betaling die u hebt gemaakt.
1. Selecteer **Kop** in het eigenschappenvenster.
1. Voer in het dialoogvenster **Kop** in het veld **Koptekst** de koptekst in die u wilt weergeven voor het gedeelte voor snel afrekenen van uw site (bijvoorbeeld **Snel afrekenen**).
1. Selecteer onder **Kopniveau** het kopniveau (bijvoorbeeld **K2**).
1. Selecteer **OK**.
1. In het eigenschappenvenster kunt u in het veld **Hoogte van het iFrame** de hoogte van het iFrame-element opgeven of aanpassen (bijvoorbeeld **60**).
1. Voer in het **Ondersteunde betalingsmethoden** de optie **PayPal** in.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Het fragment voor snelle betaling aan de afrekenpagina toevoegen

Voer de volgende stappen uit om het fragment voor snelle betaling aan de afrekenpagina toe te voegen.

1. Ga naar uw site.
1. Selecteer in het linkernavigatievenster **Pagina's** en selecteer vervolgens de afrekenpagina van uw site.
1. Om de pagina te bewerken, selecteert u **Bewerken**.
1. Selecteer het weglatingsteken (**...**) in het vak **Hoofd** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.

    > [!NOTE]
    > Als er al een containermodule met een fragment voor afrekenen bestaat, verplaatst u het gedeelte voor snelle betaling, zodat het boven een bestaande afrekencontainer in het vak **Hoofd** wordt weergegeven. Het gedeelte voor snelle betaling wordt dan weergegeven boven de normale afrekencontainer. Als u een containermodule omhoog of omlaag wilt verplaatsen, selecteert u het weglatingsteken (**...**) en vervolgens **Omhoog** of **Omlaag**.

1. In het deelvenster **Containereigenschappen** is het raadzaam de eigenschapsinstellingen als volgt te configureren:

    - **Containerindeling**: selecteer **Gestapeld**.
    - **Breedte**: selecteert **Container vullen**.
    - **Onderliggende items weergegeven**: selecteer **Drie**.

1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Fragment toevoegen**.
1. Selecteer in het dialoogvenster **Fragment selecteren** het fragment voor snelle betaling dat u eerder hebt gemaakt en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Het fragment voor snelle betaling aan de winkelwagenpagina toevoegen

Voer de volgende stappen uit om het fragment voor snelle betaling aan de winkelwagenpagina toe te voegen.

1. Ga naar uw site.
1. Selecteer in het linkernavigatievenster **Pagina's** en selecteer vervolgens de winkelwagenpagina van uw site.
1. Om de pagina te bewerken, selecteert u **Bewerken**.
1. Zoek in het vak **Hoofd** de container met de module **Winkelwagen**. De module **Winkelwagen** bevat een vak **Snelle betaling**.
1. Selecteer het vak **Snelle betaling**, het weglatingsteken (**...**) en **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Snelle betaling** en selecteer vervolgens **OK**.
1. Voer in het eigenschappenvenster in het veld **Ondersteunde betalingsmethoden** **Paypal** in.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

### <a name="modes-of-delivery"></a>Leveringsmethoden

Wanneer de module voor snelle betaling is geconfigureerd voor het gebruik van PayPal, wordt de eerste leveringsoptie die wordt geretourneerd voor het verzendadres dat is geselecteerd voor de PayPal-rekening, vooraf ingevuld. Gebruikers kunnen zo het verzendadres desgewenst wijzigen.

De volgorde van de leveringsmethode wordt geconfigureerd in de sectie **Leveringsmethoden** voor het kanaal in Commerce Headquarters. Zie [Leveringsmethoden instellen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor meer informatie.

De afrekenmodule gebruikt ook de leveringsoptiemodule wanneer leveringsmethoden worden weergegeven tijdens het afrekenen. Zie [Module voor leveringsopties](../delivery-options-module.md) voor meer informatie.

Leveringsmethoden worden toegevoegd aan de lijst voor de online winkel in Commerce Headquarters. Ga naar **Retail en handel \> Kanalen \> Online winkels** en selecteer de kanaal-id voor uw winkel. Selecteer vervolgens **Instellen \> Leveringsmethoden**. De leveringsmethoden voor de module die in de configuratie worden weergegeven, worden op een vergelijkbare manier op de site weergegeven. Als u leveringsmethoden voor een detailhandelkanaal of -product wilt toevoegen of verwijderen, selecteert u **Leveringsmethoden beheren** in het actievenster.

## <a name="additional-resources"></a>Aanvullende bronnen

[Veelgestelde vragen over betalingen](payments-retail.md)

[Kassamodule](../add-checkout-module.md)

[Betalingsmodule](../payment-module.md)

[Leveringsmethoden instellen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Module voor leveringsopties](../delivery-options-module.md)
