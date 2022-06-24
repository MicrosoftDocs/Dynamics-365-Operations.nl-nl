---
title: E-mailsjablonen maken voor transactiegebeurtenissen
description: In dit artikel wordt beschreven hoe u e-mailsjablonen kunt maken, uploaden en configureren voor transactiegebeurtenissen in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9a4d67d901608e210b4060a655ce39f0ea707a52
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910545"
---
# <a name="create-email-templates-for-transactional-events"></a>E-mailsjablonen maken voor transactiegebeurtenissen

[!include [banner](includes/banner.md)]


In dit artikel wordt beschreven hoe u e-mailsjablonen kunt maken, uploaden en configureren voor transactiegebeurtenissen in Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce biedt een kant-en-klare oplossing voor het verzenden van e-mails waarin klanten worden gewaarschuwd over transactionele gebeurtenissen. E-mails kunnen bijvoorbeeld worden verzonden wanneer er een order wordt geplaatst, klaar is om te worden opgehaald of als deze is verzonden. In dit artikel worden de stappen beschreven voor het maken, uploaden en configureren van de e-mailsjablonen die worden gebruikt voor het verzenden van transactionele e-mails.

## <a name="notification-types"></a>Meldingstypen

Meldingen kunnen worden geconfigureerd om klanten via e-mail te informeren wanneer specifieke gebeurtenissen plaatsvinden als onderdeel van de levenscyclus van orders en klanten. Als u meldingen wilt configureren, moet u een e-mailsjabloon aan een meldingstype toewijzen door een profiel voor e-mailmeldingen voor Commerce-te maken. Zie [Een profiel voor e-mailmeldingen instellen](email-notification-profiles.md) voor informatie over hoe u profielen voor e-mailmeldingen instelt.

Dynamics 365 Commerce ondersteunt de volgende typen meldingen.

### <a name="order-created"></a>Order gemaakt

Het meldingstype *Order gemaakt* wordt geactiveerd wanneer er in Commerce Headquarters een nieuwe verkooporder wordt gemaakt.

> [!NOTE]
> Het meldingstype Order gemaakt wordt niet geactiveerd voor cash-and-carry-transacties die plaatsvinden op een POS-terminal (point of sale, verkooppunt). In dit geval wordt er een e-mailontvangstbewijs of een afgedrukt ontvangstbewijs gegenereerd. Zie [E-mailontvangstbewijzen verzenden vanaf het MPOS (Modern POS)](email-receipts.md) voor meer informatie.

### <a name="order-confirmed"></a>Order is bevestigd

Het meldingstype *Order is bevestigd* wordt geactiveerd wanneer een orderbevestigingsdocument voor een verkooporder wordt gegenereerd vanuit Commerce Headquarters.

### <a name="picking-completed"></a>Verzamelen is voltooid

Het meldingstype *Verzamelen is voltooid* wordt geactiveerd wanneer een orderverzamellijst voor een order in Commerce Headquarters is gemarkeerd als voltooid.

> [!NOTE]
> Het meldingstype Verzamelen is voltooid wordt niet geactiveerd wanneer een artikel op een POS-terminal is gemarkeerd als verzameld.

### <a name="packing-completed"></a>Verpakken is voltooid

Het meldingstype *Verpakken is voltooid* wordt geactiveerd wanneer pakbondocument voor een order in Commerce Headquarters wordt gegenereerd.

Het meldingstype Verpakken is voltooid ondersteunt de volgende extra tijdelijke aanduidingen voor e-mails om 'Order gereed voor ophalen' en de functie voor het opzoeken van orders van transactionele e-mails mogelijk te maken.

| Naam van tijdelijke aanduiding    | Doel |
| ------------------- | ------- |
| `pickupstorename`     | De naam van de winkel waar de order kan worden opgehaald. |
| `pickupstoreaddress`  | Het adres van de winkel waar de order kan worden opgehaald. |
| `pickupstoreopenfrom` | De openingstijd van de winkel waar de order kan worden opgehaald. |
| `pickupstoreopento` | De sluitingstijd van de winkel waar de order kan worden opgehaald. |
| `pickupchannelid`     | De winkelkanaal-id van de winkel waar de order kan worden opgehaald. |
| `packingslipid`      | De id van de pakbon voor de order die wordt opgehaald. |
| `confirmationid`      | De orderbevestigings-id van de order die wordt opgehaald. (Deze id wordt ook wel de kanaalverwijzings-id genoemd.) |

Zie [Geodetectie en omleiding instellen](geo-detection-redirection.md) en [Orders opzoeken voor het inchecken van klanten inschakelen](order-lookup-guest.md) voor meer informatie over het uitchecken van gasten en de functies voor het opzoeken van orders.

### <a name="order-ready-for-pickup"></a>Order gereed voor ophalen

Het meldingstype *Order gereed voor ophalen* wordt geactiveerd wanneer er een order is gemarkeerd als verpakt en de leveringsmethode is ingesteld op **Ophalen klant** op een of meer orderregels.

> [!NOTE]
> De order die gereed is voor het meldingstype voor ophalen, is afgeschaft en vervangen door het meldingstype Verpakken is voltooid. Dit meldingstype wordt aangepast door de leveringsmethode.

### <a name="order-shipped"></a>Order verzonden

Het meldingstype *Order verzonden* wordt geactiveerd wanneer er een order zonder een leveringsmethode voor het ophalen in de winkel, wordt gefactureerd.

> [!NOTE]
> Het meldingstype Order verzonden is afgeschaft en vervangen door het meldingstype Order gefactureerd. Dit meldingstype wordt aangepast door de leveringsmethode.

### <a name="order-invoiced"></a>Gefactureerde order

Het meldingstype *Order gefactureerd* wordt geactiveerd wanneer er in het POS of in Commerce Headquarters een order wordt gefactureerd.

### <a name="issue-gift-card"></a>Geschenkbon uitgeven

Het meldingstype *Geschenkbon uitgeven* wordt geactiveerd wanneer er een verkooporder met een product van het type geschenkbon wordt gefactureerd.

> [!NOTE]
> De e-mailmelding over de geschenkbon wordt verzonden naar de ontvanger van de geschenkbon. De ontvanger van de geschenkbon wordt opgegeven in Commerce Headquarters op een afzonderlijke verkooporderregel op het tabblad **Verpakking** onder **Regeldetails**. Deze kan handmatig of programmatisch worden opgegeven.

Het meldingstype Geschenkbon uitgeven ondersteunt de volgende extra tijdelijke aanduidingen.

| Naam van tijdelijke aanduiding      | Doel |
| --------------------- | ------- |
| `giftcardnumber`        | Het nummer van de geschenkbon, voor producten van het geschenkbontype. |
| `availablebalance` | Het resterende saldo op de geschenkbon. |
| `giftcardmessage`       | Het bericht van de geschenkbon, voor producten van het geschenkbontype. |
| `giftcardpin`         | De pincode van de geschenkbon, voor producten van het geschenkbontype. (Deze tijdelijke aanduiding is specifiek voor externe geschenkbonnen.) |
| `giftcardexpiration`    | De vervaldatum van de geschenkbon, voor producten van het geschenkbontype. (Deze tijdelijke aanduiding is specifiek voor externe geschenkbonnen.) |
| `giftcardrecipientname` | De naam van de ontvanger van de geschenkbon, voor producten van het geschenkbontype. |
| `giftcardbuyername`     | De naam van de koper van de geschenkbon, voor producten van het geschenkbontype. |

Zie [Digitale geschenkbonnen voor e-commerce](digital-gift-cards.md) en [Ondersteuning voor externe geschenkbonnen](dev-itpro/gift-card.md) voor meer informatie over geschenkbonnen.

### <a name="order-cancellation"></a>Order annuleren

Het meldingstype *Order annuleren* wordt geactiveerd wanneer er in Commerce Headquarters een order wordt geannuleerd.

### <a name="customer-created"></a>Klant gemaakt

Het meldingstype *Klant gemaakt* wordt geactiveerd wanneer er in Commerce Headquarters een nieuwe klantentiteit wordt gemaakt.

### <a name="b2b-prospect-approved"></a>B2B-prospect goedgekeurd

Het meldingstype *B2B-prospects goedgekeurd* wordt geactiveerd wanneer er een aanvraag voor onboarding van een prospect wordt goedgekeurd in Commerce Headquarters. Zie [De beheerdergebruiker instellen voor een nieuwe zakenpartner](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner) voor meer informatie over het goedkeuren of afwijzen van B2B-prospects. 

Het meldingstype B2B-prospects goedgekeurd ondersteunt de volgende extra tijdelijke aanduidingen.

| Naam van tijdelijke aanduiding | Doel                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | De voornaam van de B2B-prospect zoals deze in de sollicitatie is ingevoerd. |
| `lastname`         | De achternaam van de B2B-prospect zoals deze in de sollicitatie is ingevoerd. |
| `company`          | De naam van het bedrijf van de sollicitant zoals deze in de sollicitatie is ingevoerd. |
| `email`            | Het e-mailadres zoals dit in de sollicitatie is ingevoerd.   |
| `zipcode`          | De postcode van het primaire adres van de prospect. |
| `comments`         | De opmerking die de prospect in de sollicitatie heeft ingevoerd. |
| `storename`        | De naam van het kanaal waarin de prospect is gemaakt. |
| `storeurl`         | Standaard is deze leeg. U moet een aangepaste extensie maken om deze tijdelijke aanduiding te kunnen gebruiken. |

### <a name="b2b-prospect-rejected"></a>B2B-prospect afgewezen

Het meldingstype *B2B-prospects afgewezen* wordt geactiveerd wanneer er een aanvraag voor onboarding van een prospect wordt afgewezen in Commerce Headquarters. Zie [De beheerdergebruiker instellen voor een nieuwe zakenpartner](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner) voor meer informatie over het goedkeuren of afwijzen van B2B-prospects. 

Het meldingstype B2B-prospect afgewezen ondersteunt de volgende extra tijdelijke aanduidingen.

| Naam van tijdelijke aanduiding | Doel                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | De voornaam van de B2B-prospect zoals deze in de sollicitatie is ingevoerd. |
| `lastname`         | De achternaam van de B2B-prospect zoals deze in de sollicitatie is ingevoerd. |
| `company`          | De naam van het bedrijf van de sollicitant zoals deze in de sollicitatie is ingevoerd. |

## <a name="create-an-email-template"></a>Een e-mailsjabloon maken

Voordat u een bepaalde transactiegebeurtenis aan een e-mailsjabloon kunt toewijzen, moet u de sjabloon maken.

Volg deze stappen om een e-mailsjabloon te maken.

1. Ga in Commerce Headquarters naar **Retail en Commerce \> Instelling van hoofdkantoor \> E-mailsjablonen van organisatie** of **Organisatiebeheer \> Instellingen \> E-mailsjablonen van organisatie**.
1. Selecteer **Nieuw**.
1. Stel onder **Algemeen** de volgende velden in:

    - **E-mail-id**: de e-mail-id is de unieke id voor een sjabloon. Het is de waarde die wordt weergegeven wanneer u een sjabloon selecteert om aan een gebeurtenis toe te wijzen.
    - **Beschrijving van e-mail**: u kunt dit optionele veld gebruiken om een beschrijving van de sjabloon te geven. De waarde die u invoert, wordt alleen weergegeven in Commerce Headquarters.
    - **Naam van afzender**: de naam die u invoert, wordt weergegeven in het veld Van van de meeste e-mailclients.
    - **E-mailadres afzender**: voer het e-mailadres in dat moet worden gebruikt voor e-mails die met deze sjabloon worden verzonden.
    - **Standaardtaalcode**: dit veld bevat de gelokaliseerde versie van het e-mailbericht dat standaard wordt verzonden als er geen taal is opgegeven door het kanaal dat deze sjabloon aanroept.

1. Selecteer **Nieuw** onder **Inhoud van e-mailbericht**.
1. Voer in het veld **Taal** de taal voor de e-mailsjabloon in. U kunt later meer talen en gelokaliseerde sjablonen toevoegen.
1. Voer in het veld **Onderwerp** het e-mailonderwerp in dat moet worden weergegeven in het veld Onderwerp van de e-mail.
1. Selecteer **Bewerken** om uw e-mailsjabloon te uploaden.

## <a name="create-an-email-message-body-by-using-html"></a>De hoofdtekst van een e-mailbericht maken met behulp van HTML

De hoofdtekst van het e-mailbericht is opgesteld in HTML. U kunt elke indeling, opmaak en huisstijl gebruiken die door HTML en inline CSS (Cascading Style Sheets) worden ondersteund. U kunt ook afbeeldingen gebruiken als u deze op een openbaar beschikbaar webeindpunt host. Als u een afbeelding wilt toevoegen, voert u de URL van de afbeelding in het kenmerk **src** van de HTML-tag **&lt;img&gt;** in.

> [!NOTE]
> E-mailclients leggen indelings- en stijlbeperkingen op die mogelijk wijzigingen vereisen in de HTML en CSS die u voor de hoofdtekst van het bericht gebruikt. We raden u aan uzelf vertrouwd te maken met de best practices voor het maken van HTML die worden ondersteund door de populairste e-mailclients.

## <a name="add-placeholders-to-the-email-message-body"></a>Tijdelijke aanduidingen toevoegen aan de hoofdtekst van een e-mailbericht

Uw e-mail kan tijdelijke aanduidingen bevatten die worden vervangen door klantspecifieke en transactiespecifieke waarden wanneer het e-mail bericht wordt gegenereerd. Tijdelijke aanduidingen worden altijd omgeven door percentagetekens (%%) en worden rechtstreeks in het HTML-document ingevoegd.

Hier volgt een voorbeeld.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Tijdelijke aanduidingen voor orders (verkooporderniveau)

Met de volgende tijdelijke aanduidingen worden gegevens opgehaald en weergegeven die zijn gedefinieerd op het niveau van de verkooporder (in tegenstelling tot het niveau van de verkoopregel).

| Naam van tijdelijke aanduiding     | Doel                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | De naam van de klant die de order heeft geplaatst.               |
| `customeraddress`      | Het adres van de klant.                                 |
| `customeremailaddress` | Het e-mailadres dat de klant bij het uitchecken heeft ingevoerd.     |
| `salesid`              | De verkoop-id van de order.                                   |
| `orderconfirmationid`  | De cross-channel-ID die is gegenereerd bij het maken van de order.   |
| `channelid`            | De ID van het detailhandel- of online kanaal waarin de order is geplaatst. |
| `deliveryname`         | De naam die voor het afleveradres staat aangegeven.         |
| `deliveryaddress`      | Het afleveradres voor verzonden orders.                     |
| `deliverydate`         | De leveringsdatum.                                           |
| `shipdate`             | De verzenddatum.                                               |
| `modeofdelivery`       | De leveringsmethode van de order.                              |
| `ordernetamount`       | Het totaalbedrag voor de order, min de totale belasting.         |
| `discount`            | De totale korting voor de order.                            |
| `charges`              | De totale kosten voor de order.                             |
| `tax`                  | De totale belasting voor de order.                                 |
| `total`                | Het totale bedrag voor de order.                              |
| `storename`            | De naam van de winkel waar de order is geplaatst.            |
| `storeaddress`         | Het adres van de winkel die de order heeft geplaatst.              |
| `storeopenfrom`        | De openingstijd van de winkel die de order heeft geplaatst.         |
| `storeopento`          | De sluitingstijd van de winkel die de order heeft geplaatst.         |
| `pickupstorename`      | De naam van de winkel waar de order wordt opgehaald.\*   |
| `pickupstoreaddress`   | Het adres van de winkel waar de order wordt opgehaald.\* |
| `pickupopenstorefrom`  | De openingstijd van de winkel waar de order wordt opgehaald.\* |
| `pickupopenstoreto`    | De sluitingstijd van de winkel waar de order wordt opgehaald.\* |
| `pickupchannelid`     | De kanaal-ID van de winkel die is opgegeven voor een ophaalmodus van levering.\* |
| `packingslipid`        | De ID van de pakbon die is gegenereerd toen regels in een order werden verpakt.\* |

\* Deze tijdelijke aanduidingen retourneren alleen gegevens wanneer deze worden gebruikt voor het meldingstype **Order gereed voor ophalen**. 

### <a name="order-line-placeholders-sales-line-level"></a>Tijdelijke aanduidingen voor orderregels (verkoopregelniveau)

Met de volgende tijdelijke aanduidingen worden gegevens voor afzonderlijke producten (regels) in de verkooporder opgehaald en weergegeven.

| Naam van tijdelijke aanduiding               | Doel |
|--------------------------------|-------------------|
| `productid`                      | <p>De ID van het product. Deze ID is bedoeld voor varianten.</p><p><strong>Opmerking:</strong> Deze tijdelijke aanduiding is afgeschaft en vervangen door `lineproductrecid`.</p> |
| `lineproductrecid`               | De ID van het product. Deze ID is bedoeld voor varianten. Identificeert een artikel als uniek op variantniveau. |
| `lineitemid`                     | De ID van het product op productniveau. (Deze ID is niet bedoeld voor varianten.) |
| `lineproductvariantid`           | De ID van de productvariant. |
| `lineproductname`                | De naam van het product. |
| `lineproductdescription`         | De beschrijving van het product. |
| `linequantity`                   | Het aantal eenheden dat is besteld voor de regel, plus de maateenheid (bijvoorbeeld **stuks** of **paar**). |
| `lineunit`                       | De maateenheid voor de regel. |
| `linequantity_withoutunit`       | Het aantal eenheden dat is besteld voor de regel, zonder de maateenheid. |
| `linequantitypicked`             | Het aantal opgenomen eenheden wanneer de gebeurtenis **PickOrder** wordt gebruikt. Anders **0** (nul). |
| `linequantitypicked_withoutunit` | Het aantal opgenomen eenheden, zonder de maateenheid, wanneer de gebeurtenis **PickOrder** wordt gebruikt. Anders **0** (nul). |
| `linequantitypacked`             | Het aantal verpakte eenheden wanneer de gebeurtenissen **PackOrder** en **Order gereed voor ophalen** worden gebruikt. Anders **0** (nul). |
| `linequantitypacked_withoutuom`  | Het aantal verpakte eenheden, zonder de maateenheid, wanneer de gebeurtenissen **PackOrder** en **Order gereed voor ophalen** worden gebruikt. Anders **0** (nul). |
| `linequantityshipped`            | Altijd **0**, behalve wanneer specifieke gebeurtenissen worden gebruikt, zoals wordt beschreven in de volgende rij. |
| `linequantityshipped_withoutuom` | Het aantal opgenomen eenheden, zonder de maateenheid, wanneer de gebeurtenis **ShipOrder** wordt gebruikt. Anders **0** (nul). |
| `lineprice`                      | De prijs van één eenheid. |
| `linenetamount`                  | De prijs van de regel nadat het aantal eenheden en de korting zijn toegepast. |
| `linediscount`                   | De korting voor een afzonderlijke eenheid. |
| `lineshipdate`                   | De verzenddatum voor de regel. |
| `linedeliverydate`               | De leveringsdatum voor de regel. |
| `linedeliverymode`               | De leveringsmethode voor de regel. |
| `linedeliveryaddress`            | Het afleveradres voor de regel. |
| `linepickupdate`                 | De ophaaldatum die de klant heeft opgegeven voor orders die een ophaalmodus voor levering gebruiken. |
| `linepickuptimeslot`             | De het tijdsbereik voor ophalen dat de klant heeft opgegeven voor orders die een ophaalmodus voor levering gebruiken. |
| `giftcardnumber`                 | Het nummer van de geschenkbon, voor producten van het geschenkbontype. |
| `giftcardbalance`                | Het saldo van de geschenkbon, voor producten van het geschenkbontype. |
| `giftcardmessage`                | Het bericht van de geschenkbon, voor producten van het geschenkbontype. |
| `giftcardpin`                    | De pincode van de geschenkbon voor producten van het geschenkbontype. (Deze tijdelijke aanduiding is specifiek voor externe geschenkbonnen.) |
| `giftcardexpiration`             | De vervaldatum van de geschenkbon, voor producten van het geschenkbontype. (Deze tijdelijke aanduiding is specifiek voor externe geschenkbonnen.) |
| `giftcardrecipientname`          | De naam van de ontvanger van de geschenkbon, voor producten van het geschenkbontype. |
| `giftcardbuyername`              | De naam van de koper van de geschenkbon, voor producten van het geschenkbontype. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Indeling van tijdelijke aanduidingen voor orderregel in de hoofdtekst van een e-mailbericht

Wanneer u de HTML maakt voor de afzonderlijke orderregels in de hoofdtekst van het e-mailbericht, plaatst u het HTML-blok dat wordt herhaald en tijdelijke aanduidingen voor de regels tussen de volgende tijdelijke aanduidingen. De tijdelijke aanduidingen staan tussen HTML-opmerkingencodes.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Hier volgt een voorbeeld.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Een sjabloon voor per e-mail verzonden ontvangstbewijzen

U kunt ontvangstbewijzen per e-mail verzenden naar klanten die aankopen doen bij een POS-verkooppunt. Over het algemeen komen de stappen voor het maken van de sjabloon voor per e-mail verzonden ontvangstbewijzen overeen met de stappen voor het maken van sjablonen voor andere transactiegebeurtenissen. De volgende wijzigingen zijn echter vereist:

- De tijdelijke aanduiding **%message%** wordt gebruikt om de tekst van de ontvangstbon in het e-mailbericht in te voegen. Om er zeker van te zijn dat de tekst van het ontvangstbewijs juist wordt weergegeven, plaatst u de tijdelijke aanduiding **%message%** tussen de HTML-tags **&lt;pre&gt;** en **&lt;/pre&gt;**.
- De tijdelijke aanduiding **%receiptid%** kan worden gebruikt om een QR-code of streepjescode weer te geven die de ontvangst-id vertegenwoordigt. (QR-codes en streepjescodes worden dynamisch gegenereerd en gebruikt door een service van derden.) Zie [Een QR-code of streepjescode toevoegen aan transactionele e-mails en ontvangstberichten](add-qr-code-barcode-email.md) voor meer informatie over het weergeven van een QR-code of streepjescode in een per e-mail verzonden ontvangstbewijs.

## <a name="upload-the-email-html"></a>De e-mail-HTML uploaden

Nadat u de HTML voor de berichttekst hebt gemaakt en getest, moet u deze uploaden naar Commerce Headquarters. Op dit moment kan e-mail-HTML niet worden geëxporteerd. Daarom moet u de hoofdkopie van uw HTML-code buiten Commerce Headquarters beheren.

Als u een nieuwe of bewerkte HTML-sjabloon wilt uploaden, gaat u als volgt te werk.

1. Ga in Commerce Headquarters naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> E-mailsjablonen van organisatie**.
1. Selecteer de rij voor de taal waarin u HTML wilt toevoegen of vervangen. U kunt ook **Nieuw** selecteren om een rij voor een nieuwe taal te maken.
1. Selecteer **Bewerken**.
1. Selecteer in het dialoogvenster dat verschijnt **Bladeren**. Blader naar het HTML-document dat u wilt uploaden, selecteer het en selecteer vervolgens **Openen**.
1. Selecteer **Uploaden**.
1. Nadat uw e-mail-HTML in het voorbeeldvenster wordt weergegeven, selecteert u **OK**.
1. Zorg ervoor dat het selectievakje **Heeft hoofdtekst** is ingeschakeld voor de rij.

Als u Commerce Headquarters al hebt geconfigureerd om e-mail te verzenden, wordt het nieuwe of bijgewerkte e-mailbericht verzonden naar alle klanten die een transactie uitvoeren die de gebeurtenis aanroept die aan de sjabloon is toegewezen.

Zie voor meer informatie over het configureren van e-mails in Dynamics 365 Commerce [E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Aanvullende bronnen 

[Een profiel voor e-mailmeldingen instellen](email-notification-profiles.md)

[E-mail configureren en verzenden](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[E-mail ontvangstbewijzen instellen](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[E-mailontvangstbewijzen verzenden vanuit Modern POS ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
