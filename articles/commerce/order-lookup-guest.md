---
title: Orders opzoeken voor gastbetalingen
description: In dit artikel wordt beschreven hoe u orders opzoeken voor gastbetalingen inschakelt in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4f381f1ec0ea08f18db3cac474e8990906364504
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286886"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Orders opzoeken voor gastbetalingen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u orders opzoeken voor gastbetalingen inschakelt in Microsoft Dynamics 365 Commerce.

Met de functie voor het opzoeken van orders voor gastbetalingen kunnen klanten die aankopen doen als gastgebruikers, hun orders opzoeken. De opzoekmogelijkheid voor orders is handig wanneer klanten acties willen uitvoeren, zoals het controleren van de afhandelingsstatus van producten op een order, het controleren van het adres waarnaar een order is verzonden, het opnieuw bestellen van een product of het bevestigen van de winkel waar een order wordt opgehaald.

Klanten die orders plaatsen als geregistreerde gebruikers kunnen hun orderdetails zien wanneer ze zijn aangemeld, maar klanten die gastbetalingen gebruiken om orders te plaatsen, kunnen dat niet. Wanneer de functie voor het zoeken naar orders voor gastbetalingen is ingeschakeld, is er echter een formulier beschikbaar dat klanten kunnen gebruiken om naar orders te zoeken die ze als gast hebben geplaatst. In dit formulier voeren klanten de orderbevestigings-id en (optioneel) het e-mailadres in die ze bij het betalen hebben opgegeven.

Bovendien kan er een koppeling of knop worden opgenomen waarmee de klant rechtstreeks naar de orderdetailpagina voor hun order kunnen gaan in alle ordergerelateerde transactionele e-mails. Deze koppeling of knop werkt voor orders die zowel door geregistreerde gebruikers als door gastgebruikers zijn geplaatst.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>De benodigde functies inschakelen in Commerce Headquarters

U moet de volgende functies inschakelen bij **Werkruimten \> Functiebeheer** in Commerce Headquarters om het opzoeken van orders voor gastbetalingen in te schakelen.

| Functie | Doel |
|---------|---------|
| Keuzefunctie voor zoekorderdetails voor anonieme gebruiker in Retail | Deze functie maakt de gebruikersinterface in Commerce-parameters beschikbaar, waarmee u de API voor het opzoeken van order voor niet-geverifieerde gebruikers kunt inschakelen en kunt configureren hoe persoonlijke gegevens worden weergegeven. |
| Genereren van een sterkere verwijzings-id voor een kanaal inschakelen | Deze functie genereert een beter beveiligde kanaalreferentie-id (orderbevestigings-id) van 12 tekens die aan de querytekenreeks kan worden doorgegeven wanneer een order wordt opgezocht. |
| Een consistente indeling voor kanaalverwijzings-id's voor alle kanalen genereren | Deze functie genereert een beveiligde kanaalreferentie-id voor orders die via een e-commercesite, het verkooppunt (POS) of een callcenter worden geplaatst. Voordat u deze functie kunt inschakelen, moet u de functie **Genereren van een sterkere kanaalverwijzings-id inschakelen** worden ingeschakeld. |

Nadat u de functie **Functie voor anoniem zoeken gebruikers orderdetails** hebt ingeschakeld, moet u de API inschakelen die het niet-geverifieerde opzoeken van orders in Commerce Headquarters ondersteunt. Ga naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Klantorders**. Stel op de pagina **Klantorders** op het sneltabblad **Order zoeken** de optie **Niet-geverifieerd opzoeken van orders inschakelen** in **Ja**, zoals in de onderstaande afbeelding wordt weergegeven.

## <a name="manage-the-display-of-personal-data"></a>De weergave van persoonlijke gegevens beheren

Het sneltabblad **Orders opzoeken** op de pagina **Klantorders** in Commerce Headquarters bevat een veld **Persoonlijke gegevens in orders opzoeken voor gasten opnemen** waarmee u kunt beheren of persoonlijke gegevens aan klanten worden weergegeven. Deze persoonlijke gegevens omvatten het verzendadres van de klant en de laatste vier cijfers van het creditcardnummer van de klant. Persoonlijke gegevens worden standaard niet weergegeven aan klanten wanneer het niet-geverifieerde opzoeken van orders is ingeschakeld. In de volgende tabel worden de beschikbare opties beschreven.

| Optie | Resultaat |
|--------|--------|
| Nooit | De standaardwaarde. Er worden geen persoonlijke gegevens weergegeven bij het opzoeken van orders. Wanneer geregistreerde gebruikers die zijn aangemeld, een order opzoeken die ze hebben gemaakt toen ze waren aangemeld, kunnen ze hun persoonlijke gegevens zien. |
| Alleen orders van gasten | Persoonlijke gegevens worden weergegeven bij het opzoeken van orders voor orders die klanten als gast hebben gemaakt. Als een order is gemaakt door een geregistreerde gebruiker, moet die gebruiker zich aanmelden om persoonlijke gegevens te bekijken. |
| Alle orders | Persoonlijke gegevens worden bij alle zoekopdrachten naar orders weergegeven. |

> [!NOTE]
> Deze opties bepalen wanneer persoonlijke gegevens, zoals het adres van de klant en de laatste vier cijfers van het creditcardnummer van de klant worden weergegeven aan anonieme gastgebruikers. Voor de beveiliging van de privacy van geregistreerde klanten raden we u aan de optie **Alleen gastorders** selecteren. De veiligste optie is echter **Nooit**.

Nadat u de waarde van het veld **Persoonlijke gegevens opnemen bij het opzoeken van gastorders** hebt gewijzigd, moet u taak 1070 (**Kanaalconfiguratie**) in Commerce Headquarters uitvoeren door naar **Retail en Commerce \> IT Retail en Commerce \> Distributieplanning** te gaan.

## <a name="configure-the-order-lookup-module"></a>De module voor orders opzoeken configureren

De module voor het opzoeken van orders in de modulebibliotheek van Commerce wordt gebruikt om het formulier weer te geven dat gastgebruikers gebruiken om orders op te zoeken. De module voor het opzoeken van orders kan worden opgenomen in het hoofdtekstvak van elke pagina waarvoor een klant zich niet hoeft aan te melden. Zie [De module voor het opzoeken van orders](order-lookup-module.md) voor informatie over het configureren van de module.

## <a name="configure-the-order-details-page"></a>De pagina met orderdetails configureren

Voordat gastgebruikers hun orderdetails kunnen bekijken, moet de pagina met orderdetails op uw e-commercesite zo worden geconfigureerd dat gebruikers zich niet hoeven aan te melden. Als u de aanmeldingsvereiste voor uw pagina met orderdetails wilt uitschakelen, opent u de pagina in Commerce Site Builder, selecteert u de slot **Standaardpagina (vereist)** in de structuurweergave en schakelt u het selectievakje **Aanmelden vereist?** onder in het deelvenster met eigenschappen aan de rechterkant uit.

## <a name="add-a-link-to-order-details-in-transactional-emails"></a>Een koppeling naar orderdetails in transactionele e-mails toevoegen

In ordergerelateerde e-mails kunt u een koppeling of knop plaatsen waarmee klanten naar de pagina met orderdetails voor hun order gaan. Als u deze koppeling of knop wilt toevoegen, maakt u een HTML-hyperlink die naar de pagina met orderdetails op uw e-commercesite wijst en geeft u de orderbevestigings-id en het e-mailadres van de klant door als URL-parameters, zoals in het volgende voorbeeld wordt weergegeven.

`<a href="https://[domain]/[orderdetailspage]?confirmationId=%orderconfirmationid%&propertyName=email&propertyValue=%customeremailaddress%" target="_blank">View my order status</a>`

## <a name="additional-resources"></a>Aanvullende bronnen

[Module voor het opzoeken van orders](order-lookup-module.md)

[Een profiel voor e-mailmeldingen instellen](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
