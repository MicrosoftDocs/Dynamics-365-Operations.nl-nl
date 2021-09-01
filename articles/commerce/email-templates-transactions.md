---
title: E-mailsjablonen maken voor transactiegebeurtenissen
description: In dit onderwerp wordt beschreven hoe u e-mailsjablonen kunt maken, uploaden en configureren voor transactiegebeurtenissen in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 05/28/2021
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
ms.openlocfilehash: 2da1044cd332d841a8c18f7139d0d8c09bad95f446494034060e59416b4018b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718702"
---
# <a name="create-email-templates-for-transactional-events"></a>E-mailsjablonen maken voor transactiegebeurtenissen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u e-mailsjablonen kunt maken, uploaden en configureren voor transactiegebeurtenissen in Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce biedt een kant-en-klare oplossing voor het verzenden van e-mails die klanten waarschuwen over transactiegebeurtenissen (bijvoorbeeld wanneer een order wordt geplaatst, een order gereed is voor ophalen of een order is verzonden). In dit onderwerp worden de stappen beschreven voor het maken, uploaden en configureren van de e-mailsjablonen die worden gebruikt voor het verzenden van transactionele e-mails.

## <a name="create-an-email-template"></a>Een e-mailsjabloon maken

Voordat u een bepaalde transactiegebeurtenis aan een e-mailsjabloon kunt toewijzen, moet u de sjabloon maken.

Volg deze stappen om een e-mailsjabloon te maken.

1. Ga in Commerce Headquarters naar **Retail en Commerce \> Instelling van hoofdkantoor \> E-mailsjablonen van organisatie** of **Organisatiebeheer \> Instellingen \> E-mailsjablonen van organisatie**.
1. Selecteer **Nieuw**.
1. Stel onder **Algemeen** de volgende velden in:

    - **E-mail-id**: de e-mail-id is de unieke id voor een sjabloon en is de waarde die wordt weergegeven wanneer u een sjabloon selecteert om aan een gebeurtenis toe te wijzen.
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

Uw e-mail kan tijdelijke aanduidingen bevatten die worden vervangen door klantspecifieke en transactiespecifieke waarden wanneer het e-mail bericht wordt gegenereerd. Tijdelijke aanduidingen worden altijd omgeven door percentagetekens (%) en worden rechtstreeks in het HTML-document ingevoegd.

Hier volgt een voorbeeld.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Tijdelijke aanduidingen voor orders (verkooporderniveau)

Met de volgende tijdelijke aanduidingen worden gegevens opgehaald en weergegeven die zijn gedefinieerd op het niveau van de verkooporder (in tegenstelling tot het niveau van de verkoopregel).

| Naam van tijdelijke aanduiding     | Waarde van tijdelijke aanduiding                                            |
| -------------------- | ------------------------------------------------------------ |
| customername         | De naam van de klant die de order heeft geplaatst.               |
| customeraddress      | Het adres van de klant.                                 |
| customeremailaddress | Het e-mailadres dat de klant bij het uitchecken heeft ingevoerd.     |
| salesid              | De verkoop-id van de order.                                   |
| id-orderbevestiging  | De cross-channel-ID die is gegenereerd bij het maken van de order. |
| kanaal-id            | De ID van het detailhandel- of online kanaal waarin de order is geplaatst. |
| leveringsnaam         | De naam die voor het afleveradres staat aangegeven.        |
| deliveryaddress      | Het afleveradres voor verzonden orders.                     |
| deliverydate         | De leveringsdatum.                                           |
| shipdate             | De verzenddatum.                                               |
| modeofdelivery       | De leveringsmethode van de order.                              |
| ordernetamount       | Het totaalbedrag voor de order, min de totale belasting.         |
| korting             | De totale korting voor de order.                            |
| toeslagen              | De totale kosten voor de order.                             |
| btw                  | De totale belasting voor de order.                                 |
| totaal                | Het totale bedrag voor de order.                              |
| storename            | De naam van de winkel waar de order is geplaatst.            |
| storeaddress         | Het adres van de winkel die de order heeft geplaatst.              |
| storeopenfrom        | De openingstijd van de winkel die de order heeft geplaatst.         |
| storeopento          | De sluitingstijd van de winkel die de order heeft geplaatst.         |
| pickupstorename      | De naam van de winkel waar de order wordt opgehaald.\* |
| pickupstoreaddress   | Het adres van de winkel waar de order wordt opgehaald.\* |
| pickupopenstorefrom  | De openingstijd van de winkel waar de order wordt opgehaald.\* |
| pickupopenstoreto    | De sluitingstijd van de winkel waar de order wordt opgehaald.\* |
| id-pickupkanaal      | De kanaal-ID van de winkel die is opgegeven voor een ophaalmodus van levering.\* |
| id-pakbon        | De ID van de pakbon die is gegenereerd toen regels in een order werden verpakt.\* |

\* Deze tijdelijke aanduidingen retourneren alleen gegevens wanneer deze worden gebruikt voor het meldingstype **Order gereed voor ophalen**. 

### <a name="order-line-placeholders-sales-line-level"></a>Tijdelijke aanduidingen voor orderregels (verkoopregelniveau)

Met de volgende tijdelijke aanduidingen worden gegevens voor afzonderlijke producten (regels) in de verkooporder opgehaald en weergegeven.

| Naam van tijdelijke aanduiding               | Waarde van tijdelijke aanduiding |
|--------------------------------|-------------------|
| productid                      | <p>De ID van het product. Deze ID is bedoeld voor varianten.</p><p><strong>Opmerking:</strong> deze tijdelijke aanduiding is afgeschaft en vervangen door **regelproductrecid**.</p> |
| id-regelproductrec               | De ID van het product. Deze ID is bedoeld voor varianten. Identificeert een artikel als uniek op variantniveau. |
| id-regelartikel                     | De ID van het product op productniveau. (Deze ID is niet bedoeld voor varianten.) |
| id-regelproductvariant           | De ID van de productvariant. |
| lineproductname                | De naam van het product. |
| lineproductdescription         | De beschrijving van het product. |
| linequantity                   | Het aantal eenheden dat is besteld voor de regel, plus de maateenheid (bijvoorbeeld **stuks** of **paar**). |
| lineunit                       | De maateenheid voor de regel. |
| linequantity_withoutunit       | Het aantal eenheden dat is besteld voor de regel, zonder de maateenheid. |
| linequantitypicked             | Het aantal opgenomen eenheden wanneer de gebeurtenis **PickOrder** wordt gebruikt. Anders **0** (nul). |
| linequantitypicked_withoutunit | Het aantal opgenomen eenheden, zonder de maateenheid, wanneer de gebeurtenis **PickOrder** wordt gebruikt. Anders **0** (nul). |
| linequantitypacked             | Het aantal verpakte eenheden wanneer de gebeurtenissen **PackOrder** en **Order gereed voor ophalen** worden gebruikt. Anders **0** (nul). |
| linequantitypacked_withoutuom  | Het aantal verpakte eenheden, zonder de maateenheid, wanneer de gebeurtenissen **PackOrder** en **Order gereed voor ophalen** worden gebruikt. Anders **0** (nul). |
| linequantityshipped            | Altijd **0**, behalve wanneer specifieke gebeurtenissen worden gebruikt, zoals wordt beschreven in de volgende rij. |
| linequantityshipped_withoutuom | Het aantal opgenomen eenheden, zonder de maateenheid, wanneer de gebeurtenis **ShipOrder** wordt gebruikt. Anders **0** (nul). |
| lineprice                      | De prijs van één eenheid. |
| linenetamount                  | De prijs van de regel nadat het aantal eenheden en de korting zijn toegepast. |
| linediscount                   | De korting voor een afzonderlijke eenheid. |
| lineshipdate                   | De verzenddatum voor de regel. |
| linedeliverydate               | De leveringsdatum voor de regel. |
| linedeliverymode               | De leveringsmethode voor de regel. |
| linedeliveryaddress            | Het afleveradres voor de regel. |
| datumophalenregel                 | De ophaaldatum die de klant heeft opgegeven voor orders die een ophaalmodus voor levering gebruiken. |
| tijdslotophalenregel             | De het tijdsbereik voor ophalen dat de klant heeft opgegeven voor orders die een ophaalmodus voor levering gebruiken. |
| giftcardnumber                 | Het nummer van de geschenkbon, voor producten van het geschenkbontype. |
| giftcardbalance                | Het saldo van de geschenkbon, voor producten van het geschenkbontype. |
| giftcardmessage                | Het bericht van de geschenkbon, voor producten van het geschenkbontype. |
| giftcardpin                    | De pincode van de geschenkbon, voor producten van het geschenkbontype. (Deze tijdelijke aanduiding is specifiek voor externe geschenkbonnen.) |
| giftcardexpiration             | De vervaldatum van de geschenkbon, voor producten van het geschenkbontype. (Deze tijdelijke aanduiding is specifiek voor externe geschenkbonnen.) |
| giftcardrecipientname          | De naam van de ontvanger van de geschenkbon, voor producten van het geschenkbontype. |
| giftcardbuyername              | De naam van de koper van de geschenkbon, voor producten van het geschenkbontype. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Indeling van tijdelijke aanduidingen voor orderregel in de hoofdtekst van een e-mailbericht

Wanneer u de HTML maakt voor de afzonderlijke orderregels in de hoofdtekst van het e-mailbericht, plaatst u het herhalende blok van HTML en tijdelijke aanduidingen voor de regels tussen de volgende tijdelijke aanduidingen in HTML-commentaartags.

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

- De tekst van het ontvangstbewijs wordt in het e-mailbericht ingevoegd met de tijdelijke aanduiding **%message%**. Om er zeker van te zijn dat de tekst van het ontvangstbewijs juist wordt weergegeven, plaatst u de tijdelijke aanduiding **%message%** tussen de HTML-tags **&lt;pre&gt;** en **&lt;/pre&gt;**.
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
