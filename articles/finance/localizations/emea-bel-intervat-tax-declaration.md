---
title: INTERVAT-belastingaangifte
description: Dit onderwerp biedt land-/regiospecifieke informatie over het instellen en maken van de INTERVAT-belastingaangifte voor rechtspersonen in alleen België.
author: anasyash
manager: AnnBe
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxIntervat
audience: Application User
ms.reviewer: kfend
ms.custom: 273023
ms.search.region: Belgium
ms.author: v-oloski
ms.dyn365.ops.version: AX 7.0.1
ms.search.validFrom: 2016-05-31
ms.openlocfilehash: 177f0cda9cb80e55ea96b97a7f5355cd403ed333
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236330"
---
# <a name="intervat-tax-declaration"></a>INTERVAT-belastingaangifte

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overzicht

Dit onderwerp biedt land-/regiospecifieke informatie over het instellen en maken van de INTERVAT-belastingaangifte voor rechtspersonen in België.

U kunt de INTERVAT-btw-aangifte als een XML-bestand maken. U kunt ook een voorbeeld weergeven van de bedragen van de btw-aangifte in een afdrukbare indeling.

De INTERVAT-aangifte die u maakt, omvat btw-transacties uit de huidige periode. Het kan ook correcties van de vorige periode bevatten als een transactie is geboekt in de vorige periode nadat deze periode werd afgesloten.

U kunt aanvullende informatie voor de aangifte invoeren en de gegevens handmatig corrigeren op de pagina **Aanvullende btw-rapportvakken**. Handmatige correctie kan nodig zijn als u bijvoorbeeld het bedrag van de aangiftecode in de INTERVAT-aangifte niet kunt afdrukken omdat het bedrag negatief is. Negatieve bedragen moeten worden afgetrokken van de volgende btw-aangifte en deze taak moet handmatig worden voltooid met behulp van correcties. Voordat u het gecorrigeerde bedrag kunt aangeven, moet u aangeven welke btw-aangiftecodes kunnen worden gecorrigeerd.

## <a name="prerequisites"></a>Vereisten
De volgende vereisten moeten worden ingesteld voordat u begint te werken met de INTERVAT-belastingaangifte:

-   Rechtspersoon
-   Registratienummer
-   Gegevens contactpersoon
-   Nummerreeksen
-   Boekingsjournaal
-   Btw-dienst
-   Btw-aangiftecodes
-   Btw-codes
-   Btw-nummer

### <a name="legal-entity"></a>Rechtspersoon

1.  Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen** en selecteer uw rechtspersoon.
2.  Maak een adres op het sneltabblad **Adressen**.
3.  Selecteer in het veld **Land/regio** de waarde **België**.
4.  Vul andere adrescomponenten in en markeer het adres als **primair**.
5.  In het Sneltabblad **Belastingregistratie**, in het veld **BTW-registratienummer**, specificeer het BTW-registratienummer van uw bedrijf.

### <a name="registration-number"></a>Registratienummer

1.  Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen**.
2.  Selecteer **Registratie-id's** en klik vervolgens op het tabblad **Registratie-id** op **Toevoegen**.
3.  Selecteer een waarde in het veld **Registratietype**.
4.  Voer een waarde in het veld **Registratienummer** in
5.  Voer op het tabblad **Algemeen** een ingangsdatum in. Zie [Registratienummer](emea-registration-ids.md) voor meer informatie.

### <a name="contact-information"></a>Gegevens contactpersoon

1.  Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen**.
2.  Voeg op het tabblad **Contactgegevens** regels toe voor het telefoonnummer en e-mailadres en stel deze in op **primair**.

### <a name="number-sequences"></a>Nummerreeksen

1.  Ga naar **Grootboek** \> **Grootboek instellen** \> **Grootboekparameters**.
2.  Stel op het tabblad **Nummerreeksen** nummerreeksen in voor de referenties **Id van jaarlijkse verkooplijst** en **INTERVAT-id**.

### <a name="posting-journal"></a>Boekingsjournaal

1.  Ga naar **Grootboek** \> **Journaalinstellingen** \> **Boekingsjournalen**.
2.  Selecteer op de pagina **Grootboekinstellingen** **Maken**. De boekstukreeks wordt automatisch gemaakt.

### <a name="sales-tax-authorities"></a>Btw-dienst

1.  Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw-dienst**.
2.  Controleer of het veld **Rapportindeling** moet worden ingesteld op **Indeling van Belgische aangifte**.

### <a name="sales-tax-reporting-codes"></a>Btw-aangiftecodes

-   Ga naar **Belasting** \> **Instellen** \> **Btw** \> **Btw-aangiftecodes** en maak nieuwe btw-aangiftecodes.

Als het veld **Btw-correctie** is ingeschakeld voor een btw-aangiftecode, is die code beschikbaar voor selectie op de pagina **Aanvullende btw-rapportvakken**.

Voorbeelden van btw-aangiftecodes worden gegeven in het gedeelte [Btw-aangiftecodes instellen](#set-up-sales-tax-reporting-codes), verderop in dit onderwerp.

### <a name="sales-tax-codes"></a>Btw-codes

1.  Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw-codes**.
2.  Voeg informatie toe of selecteer deze op de tabbladen **Rapport** en **Rapport – creditnota**.
3.  Selecteer de vereiste waarden in het raster **Btw-aangiftecodes**.

### <a name="tax-exempt-number"></a>Btw-nummer

1.  Ga naar **Belasting** \> **Instellen** \> **Btw** \> **Btw-vrijstellingsnummers**.
2.  Maak voor elk btw-vrijstellingsnummer een record die de volgende informatie bevat:

    -   Selecteer in het veld **Land/regio** de btw registratie van de andere partij.
    -   Voer in het veld **Btw-vrijstellingsnummer** het btw-vrijstellingsnummer van de andere partij in.
    -   Voer in het veld **Bedrijfsnaam** de naam van de andere partij in.

Zie [Btw-aangifte voor Europa](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/localizations/emea-vat-reporting.md) voor meer informatie over het opstellen van het btw-overzicht.

## <a name="settings"></a>Instellingen

### <a name="set-up-intervat"></a>INTERVAT instellen

Maak regels op de pagina **INTERVAT-instellingen** (**Belasting \> Instellen \> Btw \> INTERVAT-instellingen**). De informatie die u op deze pagina invoert wordt gebruikt wanneer u **Website openen** selecteert op de pagina **INTERVAT-belastingaangifte**. Maak voor elke taal een element. Stel de volgende velden in: **Taal**, **Beschrijving** en **URL**.

![Pagina Intervat-instellingen](media/1_Intervat_setup.png)

### <a name="set-up-sales-tax-reporting-codes"></a>Btw-aangiftecodes instellen

Zie voor meer informatie over het instellen van btw-aangiftecodes [Btw-aangiftecodes instellen](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/general-ledger/tasks/set-up-sales-tax-reporting-codes.md).

Als gebruikers een aangiftecode handmatig kunnen corrigeren, schakelt u het selectievakje **Btw-correcties** in. De volgende tabel bevat een voorbeeld van btw-aangiftecodes voor België.

<table width="100%">
<thead>
<tr>
<td width="17%">
<p><strong>Code en corresponderend vakje in de btw-aangifte</strong></p>
</td>
<td width="71%">
<p><strong>Beschrijving</strong></p>
</td>
<td width="10%">
<p><strong>Basis/btw</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><strong>Sectie II. Uitvoer</strong></p>
</td>
</tr>
<tr>
<td width="17%">
<p>100 (vak 00)</p>
</td>
<td width="71%">
<p>Verkopen die aan een speciale verordening zijn onderworpen.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>01</p>
</td>
<td width="71%">
<p>Belastbare leveringen en diensten met een btw-tarief van 6 procent.</p>
<p>De levering van een product of service met een btw-tarief van 6 procent.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>02</p>
</td>
<td width="71%">
<p>Belastbare leveringen en diensten met een btw-tarief van 12 procent.</p>
<p>De levering van een product of service met een btw-tarief van 12 procent.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>03</p>
</td>
<td width="71%">
<p>Belastbare leveringen en diensten met een btw-tarief van 21 procent.</p>
<p>De levering van een product of service met een btw-tarief van 21 procent.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>44</p>
</td>
<td width="71%">
<p>Services waarvoor de contractpartner buitenlandse btw verschuldigd is.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>45</p>
</td>
<td width="71%">
<p>Omzet waarover de contractpartner btw verschuldigd is.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>46</p>
</td>
<td width="71%">
<p>Intracommunautaire levering van goederen en soortgelijke transacties (verzendingen).</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>47</p>
</td>
<td width="71%">
<p>Overige verkoop zonder btw en andere verkoop die in het buitenland wordt gegenereerd.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>48</p>
</td>
<td width="71%">
<p>Bedrag van de verzonden creditnota's en negatieve correcties die zijn gerelateerd aan de verkoop uit vakken 44 en 46.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>49</p>
</td>
<td width="71%">
<p>Het bedrag van verzonden kredieten en negatieve correcties die verband houden met vakken van sectie II, "Uitvoer".</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><strong>Sectie III. Invoer</strong></p>
</td>
</tr>
<tr>
<td width="17%">
<p>81</p>
</td>
<td width="71%">
<p>Het bedrag van alle aankopen van goederen, grondstoffen en verbruiksartikelen, plus gerelateerde verwervingskosten, exclusief btw-aftrek.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>82</p>
</td>
<td width="71%">
<p>Het bedrag van diverse goederen en services, ongeacht of hierop btw van toepassing is, exclusief btw-aftrek.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>83</p>
</td>
<td width="71%">
<p>Het bedrag van de aankoop van kapitaalgoederen, ongeacht of hierop btw van toepassing is, exclusief btw-aftrek.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>84</p>
</td>
<td width="71%">
<p>Bedrag van ontvangen kredieten en negatieve correcties die zijn gerelateerd aan verkoop uit vakken 86 en 88.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>8684</p>
</td>
<td width="71%">
<p>Technische aangiftecode voor het weergeven van creditnotabedragen in vakken 86 en 84.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>8884</p>
</td>
<td width="71%">
<p>Technische aangiftecode voor het weergeven van creditnotabedragen in vakken 88 en 84.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>85</p>
</td>
<td width="71%">
<p>Bedrag van ontvangen creditbedragen en negatieve correcties die betrekking hebben op andere vakken uit sectie III, "Invoer", exclusief btw-bedrag (aftrekbaar en niet aftrekbaar)</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>8185</p>
</td>
<td width="71%">
<p>Technische aangiftecode voor het weergeven van creditnotabedragen in vakken 81 en 85.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>8285</p>
</td>
<td width="71%">
<p>Technische rapporteringscode voor het weergeven van creditnotabedragen in vakken 82 en 85.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>8385</p>
</td>
<td width="71%">
<p>Technische rapporteringscode voor het weergeven van creditnotabedragen in vakken 83 en 85.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>8785</p>
</td>
<td width="71%">
<p>Technische rapporteringscode voor het weergeven van creditnotabedragen in vakken 87 en 85.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>86</p>
</td>
<td width="71%">
<p>Intracommunautaire verwervingen en vergelijkbare transacties.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>87</p>
</td>
<td width="71%">
<p>Andere ontvangsten waarover de persoon die zich moet registreren, btw verschuldigd is.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td width="17%">
<p>88</p>
</td>
<td width="71%">
<p>Intracommunautaire diensten met overdracht van het onderzoek.</p>
</td>
<td width="10%">
<p>Basis</p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><strong>Sectie IV. Te betalen belasting</strong></p>
</td>
</tr>
<tr>
<td width="17%">
<p>54</p>
</td>
<td width="71%">
<p>Btw die moet worden betaald over de omzet die is opgenomen in codes <strong>01</strong>, <strong>02</strong> en <strong>03</strong>.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td width="17%">
<p>55</p>
</td>
<td width="71%">
<p>Btw die moet worden betaald over de omzet die is opgenomen in codes <strong>86</strong> en <strong>88</strong>.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td width="17%">
<p>56</p>
</td>
<td width="71%">
<p>Btw op verkopen die in vak 87 zijn aangegeven, met uitzondering van invoer met betrekking tot de verplaatsing van het onderzoek.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td width="17%">
<p>57</p>
</td>
<td width="71%">
<p>Btw op de invoer waarbij het onderzoek wordt overgebracht.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td width="17%">
<p>61</p>
</td>
<td width="71%">
<p>Diverse btw-aanpassingen ten voordele van de staat.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td width="17%">
<p>63</p>
</td>
<td width="71%">
<p>Btw die moet worden aangegeven, zoals weergegeven op de kredieten die zijn ontvangen.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><strong>Sectie V. Aftrekbare belastingen</strong></p>
</td>
</tr>
<tr>
<td width="17%">
<p>59</p>
</td>
<td width="71%">
<p>Bedrag van aftrekbare btw.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td width="17%">
<p>62</p>
</td>
<td width="71%">
<p>Diverse btw-correcties ten voordele van de declarant.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td width="17%">
<p>64</p>
</td>
<td width="71%">
<p>Btw die moet worden terugbetaald als gevolg van kredieten die zijn toegekend.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><strong>Sectie VI. Saldo</strong></p>
</td>
</tr>
<tr>
<td width="17%">
<p>71</p>
</td>
<td width="71%">
<p>Belasting die moet worden betaald. In het INTERVAT-rapport wordt de waarde in dit vak automatisch berekend als de som van de rapporteringscodes <strong>54</strong>, <strong>55</strong>, <strong>56</strong>, <strong>57</strong>, <strong>61</strong> en <strong>63</strong>, minus rapporteringscodes <strong>59</strong>, <strong>62</strong> en <strong>64</strong>.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td width="17%">
<p>72</p>
</td>
<td width="71%">
<p>Belasting die moet worden terugbetaald. In het INTERVAT-rapport wordt de waarde in dit vak automatisch berekend als de som van de rapporteringscodes <strong>59</strong>, <strong>62</strong> en <strong>64</strong>, minus rapporteringscodes <strong>54</strong>, <strong>55</strong>, <strong>56</strong>, <strong>57</strong>, <strong>61</strong> en <strong>63</strong>.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><strong>Sectie VII. Deposito</strong></p>
</td>
</tr>
<tr>
<td width="17%">
<p>91</p>
</td>
<td width="71%">
<p>Btw die verschuldigd is voor de periode van 1 december t/m 20 december. Deze code is van toepassing op de maandelijkse aangifte voor december.</p>
</td>
<td width="10%">
<p>Belasting</p>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> U hoeft geen codes **71**, **72** en **91** in te voeren omdat deze automatisch worden gegenereerd.

Als u een toewijzing van btw-aangiftecodes aan btw-codes wilt instellen, gaat u naar **Btw-codes \> Rapportinstellingen/Rapportinstellingen - Creditnota**. Houd rekening met de volgende relaties tussen btw-aangiftecodes:

-   Als er een bedrag voorkomt in code **01**, **02** of **03**, moet er ook een bedrag voorkomen in code **54**.
-   Als er een bedrag voorkomt in code **54**, moet er ook een bedrag voorkomen in code **01**, **02** of **03**.
-   Als er een bedrag voorkomt in code **86**, moet er ook een bedrag voorkomen in code **55**.
-   Als er een bedrag voorkomt in code **87**, moet er ook een bedrag voorkomen in code **56** of **57**.
-   Het verschil tussen het bedrag in code **54** en de som van codes **01**, **02** en **03**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet hoger zijn dan 61,97 EUR.
-   Het verschil tussen het bedrag in code **55** en de som van codes **84** en **86**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet hoger zijn dan 610,97 EUR.
-   Het verschil tussen het totaal van de bedragen in code **56** en **57** en de som van codes **85** en **87**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet hoger zijn dan 61,97 EUR.
-   Het bedrag in code **59** moet hoger zijn dan de som van de codes **81**, **82**, **83**, **84** en **85**.
-   Het bedrag in code **63** en code **85**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet meer zijn dan 61,97 EUR.
-   Het bedrag in code **64** en code **49**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet meer zijn dan 61,97 EUR.


### <a name="download-the-format-for-the-report"></a>Download de indeling voor het rapport

In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van ER-configuraties (elektronische aangifte) voor de volgende indeling van de btw-aangifte:

-   INTERVAT-indeling (BE)

Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](https://docs.microsoft.com/dynamics365/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

## <a name="additional-sales-tax-report-boxes"></a>Aanvullende btw-rapportvakken

1.  Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Aanvullende btw-rapportvakken**.
2.  Selecteer **Nieuw** als u regels wilt maken met extra informatie over rapporteringscodes, waaronder handmatige correcties van de INTERVAT-belastingaangifte. Voordat u een vereffeningsperiode sluit, moet u de regel hiervoor maken door de btw-betaling te boeken of door een INTERVAT-aangifte te maken die is gemarkeerd als **Update**. In de volgende tabel worden de velden beschreven die u moet instellen voor een nieuwe regel.

| **Veld**         | **Beschrijving**                                                                                                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vereffeningsperiode | Selecteer de toepasselijke aangifteperiode.                                                                                                                                                   |
| Begindatum         | Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend. Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**. |
| Einddatum           | Voer de laatste datum van de btw-vereffeningsperiode in.                                                                                                                                   |

3.  Stel op het sneltabblad **Algemeen** de volgende velden in:

-   Sectie **Orders**

| **Veld**                                 | **Beschrijving**                                                                                                                                                                                                                                              |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vraagt om terugbetaling van teruggevorderde btw | Selecteer deze optie om de terugbetaling van teruggevorderde btw aan te vragen.                                                                                                                                                                                      |
| Voorschot                              | Voer het voorschotbedrag in. Een voorschot kan alleen worden uitbetaald voor de maand december (maandelijkse aangifte). Het voorschot komt overeen met vak 91 in de Belgische btw-aangifte. U kunt dit veld alleen instellen als de maand gelijk is aan december (**12**). |
| Depositoformulier bestellen                        | Selecteer deze optie als u depositopagina's voor btw-aangifte wilt bestellen.                                                                                                                                                                                        |
| Geen jaaroverzichten                        | Selecteer deze optie om aan te geven dat er geen transacties zijn om aan te geven en dat het bedrijf geen verplichting aan de Belgische overheid heeft om de jaaraangifte van het vorige jaar te doen.                                                                |

-   Sectie **Omslagpercentages**

| **Veld**           | **Beschrijving**                                                                                                                                                                                                                 |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Omslagpercentage | Voer de waarde in van het pro-rata percentage dat in de **\<AdjustedValue\>**-code in het XML-bestand wordt geëxporteerd.                                                                                                              |
| B1, B2, B3, B4, B5  | Voer bedragen in voor de waarden van B1, B2, B3, B4 en B5, die worden geëxporteerd in de **\<SpecialProRataPercentage\>**-code in het XML-bestand, waarbij **\<SpecialProRataGridNumber\>**=**1**, **2**, **3**, **4**, **5** wordt gebruikt. |

### <a name="tax-corrections"></a>Belastingcorrecties

Voer de volgende stappen uit om handmatige correctiebedragen in te voeren.

1.  Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Aanvullende btw-rapportvakken**.
2.  Selecteer **Btw-correcties** \> **Correcties** en stel de volgende velden in.

| **Veld**         | **Beschrijving**                                                                                                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vereffeningsperiode | Selecteer de toepasselijke aangifteperiode.                                                                                                                                                   |
| Begindatum         | Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend. Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**. |
| Einddatum           | Voer de laatste dag van de btw-vereffeningsperiode in.                                                                                                                                    |
| Aangiftecode    | Selecteer de aangiftecode. Alleen de aangiftecodes waarvoor het selectievakje **Btw-correcties** is ingeschakeld, zijn beschikbaar tijdens het invoeren van btw-correcties.                                 |
| Bedrag            | Voer het correctiebedrag in.                                                                                                                                                              |

> [!NOTE]
> Bestaande aangiftecodes die worden gebruikt voor creditnota's. zoals code **8185**, zijn niet beschikbaar voor selectie. Codes **71**, **72** en **91** zijn ook niet beschikbaar. Codes **71** en **72** worden automatisch berekend wanneer Belgische btw-aangifte wordt uitgevoerd. Code **91** wordt op een andere manier ingevoerd (zie omschrijving van het veld **Voorschot** hierboven).
>
> Als een belastingperiode wordt bijgewerkt, worden een boekstuknummer en een datum weergegeven. (Zie voor meer informatie de omschrijving van het selectievakje **Update** in de sectie [Een INTERVAT-btw-aangifte genereren](#generate-an-intervat-tax-declaration), verderop in dit onderwerp.) De periode die een boekstuknummer en een datum heeft, is een afgesloten btw-periode voor België. Daarom zijn alle waarden op het tabblad **Algemeen** van de pagina **Btw-correcties** alleen-lezen. Wanneer er nieuwe transacties met belastingen zijn ingevoerd voor de afgesloten btw-periode, wordt de btw doorgestuurd naar de volgende beschikbare openstaande belastingperiode.


## <a name="generate-an-intervat-tax-declaration"></a>Een INTERVAT-btw-aangifte genereren
1.  Ga naar **Belasting** \>**Aangiften \> Btw \> INTERVAT-belastingaangifte**.
2.  Selecteer **Nieuwe aangifte** om een INTERVAT-belastingaangifte te genereren.
3.  Stel in het dialoogvenster **INTERVAT: Belgische btw-aangifte** de volgende velden in.

| **Veld**                | **Beschrijving**                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vereffeningsperiode        | Selecteer de toepasselijke aangifteperiode.                                                                                                                                                                                                                                                                                                                                                                                    |
| Begindatum                | Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend. Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**.                                                                                                                                                                                                                                  |
| Transactiedatum         | Voer de datum in waarvoor de btw-aangifte wordt berekend. De standaardwaarde is de huidige datum. De btw-betaling wordt berekend voor alle transacties die zijn geboekt tijdens de vereffeningsperiode.                                                                                                                                                                                                                     |
| Update                   | Met een ingeschakeld selectievakje wordt de periode afgesloten en wordt een btw-betaling gemaakt, als deze nog niet is gemaakt. Daarom worden alle btw-transacties die in deze periode zijn ingevoerd na de update, doorgestuurd naar de volgende beschikbare openstaande periode. Een ingeschakeld selectievakje maakt ook de regel op de pagina **Extra btw-aangifte vakken**, als deze nog niet is gemaakt. Geen van de waarden op deze nieuwe regel kan worden bewerkt. |
| Vervangen btw-aangifte | Voer het identificatienummer in van de te vervangen aangifte.                                                                                                                                                                                                                                                                                                                                                             |
| Bestand                     | Voer de bestandsnaam in waarnaar de INTERVAT-belastingaangifte zal worden geëxporteerd.                                                                                                                                                                                                                                                                                                                                                 |
| Indelingstoewijzing           | Selecteer de ER-indeling **INTERVAT-indeling (BE)** die u eerder hebt gedownload.                                                                                                                                                                                                                                                                                                                                                 |

U kunt de belastingperiode ook afsluiten door een btw-betaling te genereren (**Btw \> Aangiften \> Btw \> Btw vereffenen en boeken**).

4.  Selecteer **OK**. Het systeem genereert de INTERVAT-belastingaangifteregel en een INTERVAT XML-bestand.
5.  Bekijk de gegevens in de aangifte.

![Pagina INTERVAT-belastingaangifte](media/2_Intervat_tax%20declaration.png)

6.  Controleer de volgende velden op het tabblad **Algemeen**: **INTERVAT-id**, **Datum**, **Periode**, **Begindatum**, **Einddatum**, **Periodefrequentie**, **Status** en **Bestandsnaam**.
7.  Controleer de volgende velden op het tabblad **Frame I: Algemene informatie**. U kunt deze velden bewerken, zelfs als de periode is afgesloten. De uitzonderingen zijn de velden in de sectie **Omslagpercentages**. Deze velden zijn alleen-lezen.

| **Veld**                        | **Beschrijving**                                                                                                                                                                                                                                                                           |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bedrijfsnaam                     | De bedrijfsnaam.                                                                                                                                                                                                                                                                         |
| Btw-nummer                 | Het btw-registratienummer dat wordt overgenomen uit de instelling die u hebt gedefinieerd in de sectie [Vereisten](#prerequisites), eerder in dit onderwerp.                                                                                                                                   |
| Ondernemingsnummer                | Het ondernemingsnummer dat wordt overgenomen uit de instelling die u hebt gedefinieerd in de sectie [Vereisten](#prerequisites), eerder in dit onderwerp.                                                                                                                                                               |
| Telefoon, e-mail                 | Contactgegevens die worden overgenomen uit de instelling die u hebt gedefinieerd in de sectie [Vereisten](#prerequisites), eerder in dit onderwerp.                                                                                                                                                                 |
| Aanvraag van teruggaaf        | Schakel dit selectievakje in om een terugbetaling van de belasting aan te vragen.                                                                                                                                                                                                                                  |
| Aanvraag van betalingsformulieren        | Schakel dit selectievakje in om betalingspagina's voor de INTERVAT-belastingaangifte aan te vragen.                                                                                                                                                                                                         |
| Geen jaaroverzichten               | Een aangevinkt selectievakje geeft aan dat deze aangifte een lege aangifte is. De waarde wordt overgenomen van de pagina **Aanvullende btw-rapportvakken**, die wordt beschreven in de sectie [Aanvullende btw-rapportvakken](#additional-sales-tax-report-boxes), eerder in dit onderwerp |
| Vervangen btw-aangifte         | Het identificatienummer van de aangifte, om te vervangen wat u hebt gedefinieerd in het dialoogvenster **INTERVAT: Belgisch btw-aangifte**, dat eerder in deze sectie is beschreven.                                                                                                          |
| Sectie **Omslagpercentages** | Controleer de bedragen in de velden **Omslagpercentage**, **B1**, **B2**, **B3**, **B4** en **B5**, die u hebt gedefinieerd op de pagina **Aanvullende btw-rapportvakken** die wordt beschreven in de sectie [Aanvullende btw-rapportvakken](#additional-sales-tax-report-boxes).         |

Op de pagina **INTERVAT-belastingaangifte** kunt u de volgende acties uitvoeren met behulp van de knoppen in het actievenster.

| **Knop**     | **Beschrijving**                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Instellen          | De pagina **Aanvullende btw-rapportvakken** openen die wordt beschreven in de sectie [Aanvullende btw-rapportvakken](#additional-sales-tax-report-boxes).                                                                                                     |
| Bestand opnieuw maken | Het INTERVAT-bestand opnieuw maken als de periode niet is afgesloten.                                                                                                                                                                                                           |
| Bestand openen      | Het gegenereerde XML-bestand openen.                                                                                                                                                                                                                                      |
| Website openen  | De website (URL) openen die u hebt gedefinieerd op de pagina **INTERVAT-instellingen**.                                                                                                                                                                                           |
| Status wijzigen  | De cursusstatus wijzigen in **Verzonden**. Wanneer een aangifte wordt gemaakt, heeft deze de status **Gemaakt**. Nadat u het gegenereerde bestand dat de INTERVAT-aangifte bevat, op de INTERVAT-site handmatig hebt geïmporteerd, kunt u deze knop gebruiken om de status te wijzigen in **Verzonden**. |
| Details        | De pagina **Intervat-gegevens** openen, waar u de bedragen in de bijbehorende aangiftecodes kunt bekijken.                                                                                                                                                        |

## <a name="generate-an-intervat-summary-tax-declaration"></a>Een samenvatting van een INTERVAT-belastingaangifte genereren
Als u een INTERVAT-belastingaangifte wilt afdrukken voor verschillende belastingperioden, volgt u deze stappen.

1.  Ga naar **Belasting** \> **Query's en rapporten** \> **Btw-aangiften** \> **INTERVAT-belastingaangifte**.
2.  Gebruik de filters om criteria op te geven voor het selecteren van gegevens en bekijk vervolgens de informatie in het rapport.

![Gegenereerd rapport voor overzicht INTERVAT-belastingaangiften](media/3_Intervat_summary_tax_declarations.png)

## <a name="example"></a>Voorbeeld
In het volgende voorbeeld ziet u hoe u btw-codes en btw-aangiftecodes kunt instellen, transacties kunt boeken en de INTERVAT-belastingaangifte kunt genereren.

1.  Ga naar **Organisatiebeheer \> Organisaties \> Rechtspersonen**.
2.  Voer het op het sneltabblad **Belastingregistratie** in het veld **Btw-registratienummer** **0466.158.640** in.
3.  Selecteer **Registratie-id's** om een regel toe te voegen en stel de volgende waarden in:

-   **Registratietype:** ENTNUM
-   **Registratienummer:** BTW BE 0466.158.640

4.  Ga naar **Belasting \> Indirecte belastingen \> Btw \> Btw-codes** en stel de volgende btw-codes in.

| **Btw-code** | **Percentage** | **Beschrijving**                                                                      |
|--------------------|----------------|--------------------------------------------------------------------------------------|
| BE21               | 21             | Binnenlandse verkoop en inkoop met een tarief van 21 procent.                                |
| BE12               | 12             | Binnenlandse verkoop en inkoop met een tarief van 12 procent.                                |
| BE6                | 6              | Binnenlandse verkoop en inkoop met een tarief van 6 procent.                                 |
| BEEU21             | 21             | EU-inkoop met een tarief van 21 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**. |
| BEEU12             | 12             | EU-inkoop met een tarief van 12 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**. |
| BEEU6              | 6              | EU-inkoop met een tarief van 6 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.  |
| BEEUS              | 21             | EU-verkoop waarvoor de optie **Vrijstelling** is ingesteld op **Ja**.                              |

5.  Wijs op de pagina **Btw-codes** op het sneltabblad **Rapportinstellingen** aangiftecodes toe aan btw-codes.

In de volgende tabel wordt aangegeven hoe u de btw-aangiftecodes aan btw-codes kunt toewijzen.

| **Btw-code** | **Belastbare verkoop** | **Verkoop zonder btw** | **Te betalen btw** | **Belastbare inkopen** | **Te ontvangen btw** | **Belastbare import** | **Gebruiksbelasting** | **Gebruiksbelasting tegenrekenen** |
|--------------------|-------------------|-------------------|-----------------------|-----------------------|--------------------------|--------------------|-------------|--------------------|
| BE21               | 03                |                   | 54                    |                       |                          |                    |             |                    |
| BE12               | 02                |                   | 54                    |                       |                          |                    |             |                    |
| BE6                | 01                |                   | 54                    |                       |                          |                    |             |                    |
| BEEU21             |                   |                   |                       |                       | 81                       | 86                 | 59          | 55                 |
| BEEU12             |                   |                   |                       |                       | 81                       | 86                 | 59          | 55                 |
| BEEU6              |                   |                   |                       |                       | 81                       | 86                 | 59          | 55                 |
| BEEUS              |                   | 46                |                       |                       |                          |                    |             |                    |

6.  Wijs op de pagina **Btw-codes** op het sneltabblad **Rapportinstellingen - creditnota** aangiftecodes toe aan btw-codes.

In de volgende tabel wordt aangegeven hoe u de btw-aangiftecodes aan btw-codes kunt toewijzen.

| **Btw-code** | **Belastbare verkoop CN** | **Verkoop zonder btw CN** | **Te betalen btw CN** | **Belastbare inkopen CN** | **Te ontvangen btw CN** | **Belastbare import CN** | **Gebruiksbelasting CN** | **Gebruiksbelasting tegenrekenen CN** |
|--------------------|----------------------|----------------------|--------------------------|--------------------------|-----------------------------|-----------------------|----------------|-----------------------|
| BEEU21             |                      |                      |                          |                          | 8184                        | 86                    | 59             | 55                    |
| BEEU12             |                      |                      |                          |                          | 8184                        | 86                    | 59             | 55                    |
| BEEU6              |                      |                      |                          |                          | 8184                        | 86                    | 59             | 55                    |

In plaats van de codes **55** en **59** kunt u correctiecodes **63** en **64** gebruiken.

> [!NOTE]
> De voorgaande configuratie is slechts een voorbeeld en is afhankelijk van de structuur van de btw-codes die worden gebruikt. Als u wilt dat waarden worden berekend en overgeboekt naar de btw-aangifte, moet u voor elke btw-code die in het btw-betalingsproces wordt gebruikt, een relevante btw-aangiftecode instellen in een of meer velden op het tabblad **Rapportinstellingen**.

7.  Boek de volgende transacties. Voor klantfacturen gaat u bijvoorbeeld naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**. Voor leveranciersfacturen gaat u naar **Leveranciers** \> **Facturen** \> **Facturenjournaal**.

| **Datum**         | **Transactietype**  | **Nettobedrag** | **Btw-bedrag** | **Btw-code** | **Verwachte belastingbasis: aangiftecode**                 | **Verwacht belastingbedrag: aangiftecode** |
|------------------|-----------------------|----------------|----------------|--------------------|--------------------------------------------------------|------------------------------------------|
| 1 februari 2020 | Klantfactuur      | 1,100          | 132            | BE12               | 02                                                     | 54                                       |
| 1 februari 2020 | Leveranciersfactuur (EU)   | 1.000          | 210            | BEEU21             | 86 – Te betalen basis 81 – basisinhouding                  | 55 – te betalen belasting 59 – belastingaftrek      |
| 2 februari 2020 | Leveranciersfactuur (EU)   | \-200          | \-42           | BEEU21             | 86 – Te betalen basis 81 – basisinhouding 84 – kredietbasis | 55 – te betalen belasting 59 – belastingaftrek      |
| 1 februari 2020 | Klantfactuur (EU) | 100            | 0              | BEEUS              | 46                                                     | Niet van toepassing                           |

8.  Ga naar **Belasting \> Aangiften \> Btw \> Btw rapporteren voor vereffeningsperiode**.
9.  Selecteer in het dialoogvenster **Btw rapporteren voor vereffeningsperiode** in het veld **Versie van btw-betaling** de optie **Origineel**.
10.  Selecteer **OK** en bekijk de gegevens.

![Gegenereerde pagina INTERVAT-btw-aangifte](media/4_Intervat_tax_declaration.png)

U ziet dat het bedrag van de creditnota wordt weergegeven in code **84**.

11.  Ga naar **Belasting \> Aangiften \> Btw \> Aanvullende btw-rapportvakken**.
12.  Selecteer **Nieuw** om een regel voor februari 2020 te maken.
13.  Selecteer **Btw-correcties \> Correcties** en maak een regel.

![Pagina Correcties](media/5_Adjustments.png)

14.  Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Btw vereffenen en boeken**.
15.  Selecteer in het dialoogvenster **Btw vereffenen en boeken** in het veld **Versie van btw-betaling** de optie **Origineel**.
16.  Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **INTERVAT-belastingaangifte**.
17.  Selecteer **Nieuwe aangifte** en stel de volgende waarden in:

   -   **Vereffeningsperiode:** MEN
   -   **Vanaf datum:** 1-2-2020 (1 februari 2020)
   -   **Transactiedatum:** 29-2-2020 (29 februari 2020)
   -   **Update:** Nee
   -   **Indelingstoewijzing:** INTERVAT-indeling (BE)

![Pagina Nieuwe INTERVAT-belastingaangifte](media/6_Intervat.png)

18.  Selecteer **OK**, open het bestand en bekijk het rapport.

![xml-rapport met INTERVAT-belastingaangifte](media/7_Intervat_XML.png)

19.  Selecteer **Details** en bekijk de gegevens.

![Pagina INTERVAT-gegevens](media/8_Intervat_details.png)

Zoals u ziet, is het bedrag in code **62** gelijk aan **200**.
    
## <a name="reconciliation-reports-for-belgium"></a>Afstemmingsrapporten voor België

Zie voor informatie over afstemmingsrapporten voor België [Afstemmingsrapporten voor België](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/localizations/emea-bel-reconciliation-reports.md).






[!INCLUDE[footer-include](../../includes/footer-banner.md)]