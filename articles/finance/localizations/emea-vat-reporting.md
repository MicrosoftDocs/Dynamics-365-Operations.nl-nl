---
title: Btw-aangifte voor Europa
description: Dit artikel bevat algemene informatie over het instellen en genereren van het btw-overzicht (belasting toegevoegde waarde) voor een aantal Europese landen/regio's.
author: mrolecki
ms.date: 03/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 266844
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
ms.openlocfilehash: 54be8844fadf744cc5527001737ab470fcec46d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283411"
---
# <a name="vat-reporting-for-europe"></a>Btw-aangifte voor Europa

[!include [banner](../includes/banner.md)]

Dit artikel bevat algemene informatie over het instellen en genereren van het btw-overzicht (belasting toegevoegde waarde) voor een aantal Europese landen/regio's.

Dit artikel biedt een algemene aanpak voor het instellen en genereren van de btw-aangifte. Deze benadering geldt voor alle gebruikers in rechtspersonen in de volgende landen:

-   Oostenrijk
-   België
-   Tsjechische Republiek
-   Estland
-   Finland
-   Duitsland
-   Letland
-   Litouwen
-   Nederland
-   Zweden

> [!IMPORTANT]
> Functies die in dit artikel worden beschreven voor Oostenrijk, Tsjechische Republiek, Duitsland, Nederland en Zweden worden afgeschaft. Zie [Verwijderde en verouderde functies](../get-started/removed-deprecated-features-finance.md) voor meer informatie.
> Gebruik de koppelingen in de volgende tabel voor meer informatie over het nieuwe ontwerp van btw-aangiften in de overeenkomstige landen.
> 
>
> | Land/regio        | Aanvullende gegevens                                                          |
> |----------------|---------------------------------------------------------------------------------|
> | Oostenrijk        | [Btw-aangifte (Oostenrijk)](emea-aut-vat-declaration-austria.md)       |                                                                           
> | Tsjechische Republiek | [Btw-aangifte (Tsjechische Republiek)](emea-cze-vat-declaration-tax-declaration-model.md) |
> | Denemarken        | [Btw-aangifte (Denemarken)](emea-dnk-vat-declaration-denmark.md)         |
> | Frankrijk         | [Btw-aangifte (Frankrijk)](emea-fra-vat-declaration-preview-france.md)       |
> | Duitsland        | [Btw-aangifte (Duitsland)](emea-deu-vat-declaration-germany.md)           |
> | Nederland    | [Btw-aangifte (Nederland)](emea-nl-vat-declaration-netherlands.md)    |
> | Noorwegen         | [Btw-retouren met directe verzending naar Altinn](emea-nor-vat-return.md) |
> | Spanje          | [Btw-aangifte (Spanje)](emea-esp-vat-declaration-spain.md)              |
> | Zweden         | [Btw-aangifte (Zweden)](emea-swe-vat-declaration-sweden.md)          |
> | Zwitserland    | [Btw-aangifte (Zwitserland)](emea-che-vat-declaration-switzerland.md) |
> | VK             | [Voorbereiden op integratie met MRD voor btw](emea-gbr-mtd-vat-integration.md) |

## <a name="vat-statement-overview"></a>Overzicht btw-overzichten
Het btw-overzicht is gebaseerd op bedragen van belastingtransacties. Het proces voor het genereren van een btw-aangifte is onderdeel van het btw-betalingsproces dat is geïmplementeerd via de functie Btw vereffenen en boeken. Met deze functie wordt de btw berekend die verschuldigd is voor een bepaalde periode. De berekening van de vereffening omvat de geboekte btw voor de geselecteerde vereffeningsperiode voor de belastingtransacties. Het proces voor het berekenen van gegevens voor een btw-overzicht is gebaseerd op de relatie tussen btw-codes en btw-aangiftecodes, waarbij btw-aangiftecodes overeenkomen met de btw-overzichtvakken (of labels in XML). Voor elke btw-code moeten er btw-aangiftecodes worden ingesteld voor elk type transactie, zoals belastbare verkoop, belastbare inkopen, belastbare import. Dit transactietype wordt beschreven in het gedeelte Btw-codes voor btw-aangifte verderop in dit artikel.

Voor elke btw-aangiftecode moet een specifieke rapportindeling worden bepaald. Btw-codes worden tegelijkertijd gekoppeld aan een specifieke btw-dienst via btw-vereffeningsperioden. Voor elke btw-dienst moet een rapportindeling worden bepaald. Dus alleen btw-aangiftecodes met dezelfde rapportindeling als die is ingesteld voor een btw-dienst in btw-vereffeningsperioden voor btw-code, kunnen worden geselecteerd in de rapportinstelling van de btw-code. Een btw-transactie die is gegenereerd bij het boeken van een order of een journaal, bevat een btw-code, btw-bron, btw-richting en transactiebedragen (belastingbasisbedrag en belastingbedrag in valuta voor boekhouding, btw-valuta en transactievaluta). Op basis van de combinatie van belastingtransactiekenmerken bestaan transactiebedragen uit totaalbedragen voor btw-aangiftecodes die zijn opgegeven voor btw-codes. In de volgende afbeelding wordt de gegevensrelatie weergegeven.

![diagram.](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>Instelling btw-overzicht
Als u een btw-overzicht wilt genereren, moet u het volgende instellen.

### <a name="sales-tax-authorities-for-vat-reporting"></a>Btw-diensten voor btw-rapportage

Voordat u btw-aangiftecodes kunt instellen, moet u de juiste rapportindeling voor de btw-dienst selecteren. Selecteer op de pagina **Btw-diensten** in de sectie **Algemeen** een **Rapportindeling**. Deze indeling wordt gebruikt bij het instellen van btw-aangiftecodes.

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a>Btw-aangiftecodes

Btw-aangiftecodes zijn vakcodes in het btw-overzicht of labelnamen in XML-indeling. Deze codes worden gebruikt voor het samenvoegen en voorbereiden van bedragen voor het rapport. De namen van de resultaatbedragen worden gebruikt bij het configureren van de ER-indeling (elektronische rapportage) van het btw-overzicht. U kunt btw-aangiftecodes maken en onderhouden op de pagina **Btw-aangiftecodes**. U moet aan elke code een rapportindeling toewijzen. Nadat u de btw-aangiftecodes hebt gemaakt, kunt u de codes kiezen in de sectie **Rapport instellen** op de pagina **Btw-codes**. <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Btw-codes voor btw-aangifte

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Basisbedragen en belastingbedragen van btw-transacties kunnen worden samengevoegd in aangiftecodes in het btw-overzicht (XML-labels of aangiftevakken). U kunt dit instellen door btw-aangiftecodes voor verschillende transactietypen te koppelen voor btw-codes op de pagina <strong>Btw-codes</strong>. In de volgende tabel worden de transactietypen beschreven in de rapportinstelling voor btw-codes. De berekening omvat de transacties voor alle typen bronnen met uitzondering van btw.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transactietype</strong></td>
<td><strong>Omschrijving van transacties en bedragen die moeten worden geteld voor het transactietype</strong></td>
</tr>
<tr class="even">
<td><strong>Belastbare verkoop</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode/</li>
<li>De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verkoop zonder btw</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop is export (<strong>Belastingrichting</strong> is <strong>Verkoop zonder btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Te betalen btw</strong></td>
<td>Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Creditnota belastbare verkoop</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Creditnota vrijgestelde verkoop</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop is export (<strong>Belastingrichting</strong> is <strong>Verkoop zonder btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Btw op creditnota verkoop</strong></td>
<td>Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Belastbare inkopen</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Inkoop zonder btw</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is import (<strong>Belastingrichting</strong> is <strong>Inkoop zonder btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Te ontvangen btw</strong></td>
<td>Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Creditnota belastbare inkoop</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Creditnota vrijgestelde inkoop</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is import (<strong>Belastingrichting</strong> is <strong>Inkoop zonder btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Btw op creditnota inkoop</strong></td>
<td>Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Belastbare import</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong></li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Belastbare import tegenrekenen</strong></td>
<td>Omgekeerde som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Creditnota belastbare import</strong></td>
<td>Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
e<li><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Creditnota belastbare import tegenrekenen</strong></td>
<td>Omgekeerde som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>Belastingrichting is <strong>Gebruiksbelasting</strong>.</li>
d<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Gebruiksbelasting</strong></td>
<td>Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Gebruiksbelasting tegenrekenen</strong></td>
<td>Omgekeerde som van <strong>Belastingbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</li>
<li>De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Voor de bovenstaande tabel wordt ervan uitgegaan dat aan de volgende criteria wordt voldaan: 
> -   Het belastingbasisbedrag is een transactiebedrag van het veld **Oorsprong in valuta voor boekhouding**.
> -   Het belastingbedrag is een transitiebedrag van het veld **Werkelijke btw-bedrag in valuta voor boekhouding**.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Het ER-model configureren en indelen voor het rapport

U kunt elektronische rapportage (ER) gebruiken om overzichten en aangifte te configureren en om gegevens te exporteren in verschillende elektronische indelingen zonder de X ++-code te wijzigen. Voor aanvullende informatie:

-   [Overzicht van elektronische rapportage](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
-   [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [Lokalisatievereisten: een GER-configuratie maken](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a>Landspecifieke resources voor btw-overzichten
Het btw-overzicht voor elk land moet voldoen aan de vereisten van de wetgeving van het land. Er zijn vooraf gedefinieerde algemene modellen en indelingen van btw-overzichten voor de landen die in de volgende tabel staan.


| Land/regio        | Aanvullende gegevens                                                          |
|----------------|---------------------------------------------------------------------------------|
| Oostenrijk        | [Details btw-overzicht voor Oostenrijk](emea-aut-vat-statement-details.md)         |
| België        |                                                                                 |
| Tsjechische Republiek | [Btw-overzicht voor Tsjechië](emea-cze-vat-statement-details.md)   |
| Estland        | [Details btw-overzicht voor Estland](emea-est-vat-statement-details.md) |
| Finland        | [Btw-rapport voor Finland](emea-fin-sales-tax-payment-report-finland.md)          |
| Duitsland        | [Btw-aangifte voor Duitsland](emea-de-vat-declaration.md)                       |
| Italië          | [Details btw-overzichten voor Italië](emea-ita-vat-statements-details.md)            |
| Letland         | [Details btw-overzicht voor Letland](emea-lva-vat-statement-details.md)           |
| Litouwen      | [Details btw-overzicht voor Litouwen](emea-ltu-vat-statement-details.md)         |
| Nederland    | [Btw-aangifte voor Nederland](emea-nl-vat-declaration.md)           |
| Zweden         | [Btw-rapport voor Zweden](emea-swe-sales-tax-payment-report-sweden.md)          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
