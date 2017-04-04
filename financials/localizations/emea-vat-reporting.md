---
title: Btw-aangifte voor europa
description: Dit onderwerp biedt algemene informatie over het instellen en genereren van de belasting toegevoegde waarde (btw)-overzicht voor een aantal europese landen.
author: ShylaThompson
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266844
ms.assetid: 06798e29-6140-489e-9b4e-66b45b26be2b
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 84a639b25c64821e00ca4397f42f69298953e599
ms.lasthandoff: 03/31/2017


---

# <a name="vat-reporting-for-europe"></a>Btw-aangifte voor europa

Dit onderwerp biedt algemene informatie over het instellen en genereren van de belasting toegevoegde waarde (btw)-overzicht voor een aantal europese landen.

In dit onderwerp biedt een algemene aanpak voor het instellen en de btw-aangifte te genereren. Deze benadering geldt voor gebruikers met rechtspersonen in de volgende landen:

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

## <a name="vat-statement-overview"></a>Overzicht van btw-overzicht
De btw-aangifte is gebaseerd op btw-transacties bedragen. Het proces voor het genereren van een btw-aangifte is onderdeel van het betalingsproces btw die is geïmplementeerd door de functie van de btw vereffenen en boeken. Deze functie berekent de btw die moet worden betaald voor een bepaalde periode. De berekening van de vereffening omvat de geboekte btw voor de geselecteerde vereffeningsperiode voor de btw-transacties. Het proces voor het berekenen van gegevens voor een btw-aangifte is gebaseerd op de relatie tussen de btw-codes en btw-codes, waar btw-aangiftecodes overeenkomen met de btw-aangiften vakken (of in XML-labels). Voor elke btw-code, btw aangiftecodes moeten worden ingesteld voor elk type transactie, zoals belastbare verkoop belastbare inkopen belastbare import. Deze soorten transacties worden beschreven in de [btw-codes voor btw-aangifte](#Sales tax codes for VAT reporting) sectie verderop in dit onderwerp.

Voor elke btw-code, moet een specifieke rapportindeling worden bepaald. Op hetzelfde moment worden btw-codes zijn gekoppeld aan een specifieke belastingdienst t/m btw-vereffeningsperioden. Voor elke btw-dienst moet een rapportindeling worden bepaald. Dus kan alleen btw-codes met dezelfde indeling die is ingesteld voor een btw-dienst in btw-vereffeningsperioden voor btw-code worden geselecteerd in de instelling van het rapport van btw-code. Een btw-transactie gegenereerd bij het boeken van een order of een journaal, bevat een btw-code, btw-bron, btw-richting en transactiebedragen (btw-bedrag en btw-bedrag in valuta voor boekhouding, btw-valuta en valuta voor transactie). Op basis van de combinatie van btw-transactiekenmerken, samenstellen transactiebedragen totaalbedragen voor btw-codes die zijn opgegeven voor btw-codes. De volgende afbeelding toont de relatie van de gegevens.

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>Instellingen voor btw-overzicht
U moet u de volgende instellen voor het genereren van een btw-aangifte.

### <a name="sales-tax-authorities-for-vat-reporting"></a>Btw-dienst voor de btw-aangifte

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Voordat u btw-codes instellen kunt, moet u de juiste indeling voor de belastingdienst. Op de **btw-dienst** pagina in de **algemeen** sectie, selecteer een **rapportindeling**. Deze indeling wordt gebruikt bij het instellen van btw-codes.

### <a name="sales-tax-reporting-codes"></a>Btw-aangiftecodes

Btw-aangiftecodes zijn vak codes in de namen van de btw-overzicht of code in XML-indeling. Deze codes worden gebruikt voor het samenvoegen en bedragen voor het rapport voor te bereiden. De namen van de bedragen van het resultaat wordt gebruikt bij het configureren van de elektronische aangifte-indeling van de btw-aangifte. U kunt maken en onderhouden van de btw-codes op de **Sales tax reporting codes** pagina. U moet elke code een rapportindeling toewijzen. Als u de btw-aangiftecodes maken, kunt u de codes in de **rapportinstellingen** gedeelte op de **btw-codes** pagina. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Btw-codes voor btw-aangifte

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-codes/).-->Baseer bedragen en btw-bedragen van btw transacties kunnen worden samengevoegd op aangiftecodes in de btw-aangifte (XML-codes of aangifte vakken). U kunt dit instellen door het koppelen van btw-codes voor verschillende transactietypen voor btw-codes op de **btw-codes** pagina. De volgende tabel beschrijft de transactietypen in de instelling van het rapport voor btw-codes. De berekening omvat de transacties voor alle typen bronnen met uitzondering van btw.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transaction type</strong></td>
<td><strong>Omschrijving van transacties en bedragen moeten worden geteld op het transactietype</strong></td>
</tr>
<tr class="even">
<td><strong>Belastbare verkoop</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode /</li>
<li>De verkoop is binnenland (<strong>btw-richting</strong> is <strong>te betalen btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Onbelaste verkoop</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop wordt geëxporteerd (<strong>btw-richting</strong> is <strong>onbelaste verkoop</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax payable</strong></td>
<td>Som van <strong>btw-bedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop is binnenland (<strong>btw-richting</strong> is <strong>te betalen btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable sales credit note</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop is binnenland (<strong>btw-richting</strong> is <strong>te betalen btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Fax Creditnota vrijgestelde verkoop</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop wordt geëxporteerd (<strong>btw-richting</strong> is <strong>onbelaste verkoop</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on sales credit note</strong></td>
<td>Som van <strong>btw-bedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De verkoop is binnenland (<strong>btw-richting</strong> is <strong>te betalen btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable purchases</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is binnenland (<strong>btw-richting</strong> is <strong>terug te vorderen btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tax-free purchase</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is importeren (<strong>btw-richting</strong> is <strong>inkoop zonder btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax receivable</strong></td>
<td>Som van <strong>btw-bedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is binnenland (<strong>btw-richting</strong> is <strong>terug te vorderen btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable purchase credit note</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is binnenland (<strong>btw-richting</strong> is <strong>terug te vorderen btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tax exempt purchase credit note</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is importeren (<strong>btw-richting</strong> is <strong>inkoop zonder btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on purchase credit note</strong></td>
<td>Som van <strong>btw-bedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>De inkoop is binnenland (<strong>btw-richting</strong> is <strong>terug te vorderen btw</strong>).</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li><strong>btw-richting</strong> is <strong>gebruiksbelasting</strong></li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import</strong></td>
<td>Omgekeerde som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li><strong>btw-richting</strong> is <strong>gebruiksbelasting</strong>.</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import credit note</strong></td>
<td>Som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
e<li><strong>btw-richting</strong> is <strong>gebruiksbelasting</strong>.</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import credit note</strong></td>
<td>Omgekeerde som van <strong>btw-basisbedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li>Btw-richting is <strong>gebruiksbelasting</strong>.</li>
d<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Use tax</strong></td>
<td>Som van <strong>btw-bedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li><strong>btw-richting</strong> is <strong>gebruiksbelasting</strong>.</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset use tax</strong></td>
<td>Omgekeerde som van <strong>btw-bedragen</strong> van de btw-transacties die voldoen aan de volgende voorwaarden:
<ul>
<li>Transactiedatum bevindt zich in de geselecteerde periode.</li>
<li><strong>btw-richting</strong> is <strong>gebruiksbelasting</strong>.</li>
<li>De transactie <strong>btw-basisbedrag</strong> of <strong>btw-bedrag</strong>&gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Voor de tabel, wordt ervan uitgegaan dat de volgende criteria wordt voldaan: 
> -   Het btw-bedrag is een transactiebedrag van de **oorsprong in valuta voor boekhouding** veld.
> -   Het btw-bedrag is een bedrag van de overgang van de **werkelijk btw-bedrag in valuta voor boekhouding** veld.

### <a name="configure-the-er-model-and-format-for-the-report"></a>De Emergency Recovery-model en de indeling voor het rapport configureren

U kunt elektronische rapportage (ER)-instructies en -rapport configureren en te exporteren gegevens verschillende elektronische indelingen zonder X ++-code. Voor meer informatie:

-   [Overzicht van elektronische rapportage](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Vereisten te lokaliseren: een configuratie Duits maken](/dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>Countryspecific resources voor btw-aangiften
De btw-aangifte voor elk land moet voldoen aan de eisen van de wetgeving van het land. Er zijn vooraf gedefinieerde algemene modellen en indelingen van btw-aangiften voor de landen vermeld in de volgende tabel.


| Land/regio        | Aanvullende gegevens                                                          |
|----------------|---------------------------------------------------------------------------------|
| Oostenrijk        |  [Details van de btw-overzicht voor Oostenrijk](emea-aut-vat-statement-details.md)         |
| België        |                                                                                 |
| Tsjechische Republiek |  [Details van de btw-overzicht voor Tsjechië](emea-cze-vat-statement-details.md)   |
| Estland        |  [Details van de btw-overzicht voor Estland](emea-est-vat-statement-details.md) |
| Finland        |                                                                                 |
| Duitsland        |                                                                                 |
| Italië          | [Details van de btw-overzicht voor Italië](emea-ita-vat-statements-details.md)            |
| Letland         | [Details van de btw-overzicht voor Letland](emea-lva-vat-statement-details.md)           |
| Litouwen      | [Details van de btw-overzicht voor Litouwen](emea-ltu-vat-statement-details.md)         |
| Nederland    |                                                                                 |
| Zweden         |                                                                                 |




