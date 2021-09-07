---
title: Btw-aangifte voor Egypte
description: In dit onderwerp wordt uitgelegd hoe u het btw-aangifteformulier voor Egypte configureert en genereert.
author: sndray
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a67c6e00b94d49b3eb279416407f603923e53b2e
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403943"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>Btw-aangifte voor Egypte (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u het formulier voor btw-aangifte en verkoop- en inkoopboeken voor rechtspersonen in Egypte kunt instellen en genereren.

Het btw-aangifteformulier voor Egypte is het officiële document met een samenvatting van het totale verschuldigde btw-bedrag, het totale terug te vorderen btw-bedrag en de bijbehorende btw-belastingschuld. Het formulier wordt gebruikt voor alle typen belastingbetalers en moet handmatig worden ingevuld via de portal van de belastingdienst. Het btw-aangifteformulier wordt doorgaans btw-aangifte genoemd.

Het btw-aangifteformulier in Dynamics 365 Finance bevat de volgende rapporten:

- Formulier 10 voor btw-aangifte. Dit formulier bevat een uitsplitsing van bedragen, correcties en btw-bedrag per regelitem in het btw-aangifteformulier, zoals is beschreven in de wet.
- Verkooptransactieboek
- Inkooptransactieboek

## <a name="prerequisites"></a>Vereisten
Het primaire adres van de rechtspersoon moet in Egypte zijn.
Schakel in het werkgebied **Functiebeheer** de volgende functie in:

   - (Egypte) Categoriehiërarchie voor btw-rapport voor verkoop en inkoop.

Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie over het inschakelen van functies.

Importeer in het werkgebied **Elektronische rapportage** de volgende indeling voor elektronische rapportage in vanuit de opslagplaats:

- Btw-aangifte Excel (EG)

> [!NOTE]
> De bovenstaande indeling is gebaseerd op het **belastingaangiftemodel** en maakt gebruik van de **Modeltoewijzing belastingaangifte**. Aanvullende configuraties worden automatisch geïmporteerd.

Zie [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) voor meer informatie over het downloaden van ER-configuraties vanuit Lifecycle Services (LCS).

## <a name="download-electronic-reporting-configurations"></a>Configuraties van elektronische aangifte downloaden

De implementatie van het btw-aangifteformulier voor Egypte is gebaseerd op ER-configuraties (elektronische rapportage). Zie [Elektronische rapportage](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) voor meer informatie over de capaciteiten en concepten van configureerbare rapportage.

Zie [Configuraties voor elektronische rapportage downloaden vanuit Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) voor meer informatie over productie- en gebruikersacceptatietestomgevingen (UAT).

Upload de volgende configuraties als u het btw-aangifteformulier en gerelateerde rapporten wilt genereren in een rechtspersoon voor Egypte:

- Belastingaangiftemodel.versie.70.xml of hoger
- Belastingaangiftemodeltoewijzing.versie.70.120.xml of hoger
- Btw-aangifte Excel (EG).versie.70.32 of een latere versie

Nadat u de ER-configuraties hebt gedownload vanuit Lifecycle Services (LCS) of de algemene opslagplaats, voert u de volgende stappen uit.

1. Ga naar het werkgebied **Elektronische rapportage** en selecteer de tegel **Rapportconfiguraties**.
1. Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen** > **Laden uit XML-bestand**.
1. Upload de bestanden in de hierboven aangegeven volgorde. Nadat alle configuraties zijn geüpload, moet de configuratiestructuur aanwezig zijn in Finance.

## <a name="set-up-application-specific-parameters"></a>Toepassingsspecifieke parameters instellen

Met de toepassingsspecifieke parameters kunt u de criteria bepalen voor de classificatie en berekening van btw-transacties op elke regel wanneer het rapport wordt gegenereerd. De bepaling is gebaseerd op de configuratie van de btw-groep voor het artikel, de btw-groep, de btw-code en andere criteria die zijn vastgelegd in de opzoekdefinitie.

De rapporten van de verkoop- en inkoopboeken voor Egypte bevatten een reeks kolommen die overeenkomen met specifieke transactieclassificaties als typen bewerkingen, producten en documenten die specifiek zijn voor Egypte. In plaats van deze nieuwe classificaties als nieuwe invoergegevens op te nemen wanneer de transacties worden geboekt, worden de classificaties bepaald op basis van verschillende opzoekingen in **Configuraties** > **Toepassingsspecifieke parameters instellen** > **Instellen** om te voldoen aan de vereisten van btw-rapporten voor Egypte. 

![Pagina Toepassingsspecifieke parameters.](media/egypt-vat-declaration-setup1.png)

De volgende opzoekconfiguraties worden gebruikt om de transacties te classificeren in rapporten over inkoop- en verkoopboeken:

- **PurchaseItemTypeLookup** > Kolom O: Artikeltype
- **VatRateTypeLookup** > Kolom B: Btw-type
- **VATRateTypeLookup** > Kolom C: Type tabelartikel
- **PurchaseOperationTypeLookup** > Kolom A: Documenttype
- **CustomerTypeLookup** > kolom A: documenttype
- **SalesOperationTypeLookup** > Kolom N: Bewerkingstype
- **SalesItemTypeLookup** > Kolom O: Artikeltype

Voer de volgende stappen uit om de verschillende opzoekbewerkingen in te stellen die worden gebruikt om btw-aangiften en rapporten voor bijbehorende boeken te genereren. 

1. Ga naar het werkgebied **Elektronische rapportage** en selecteer **Configuraties** > **Instellen** om de regels in te stellen om de btw-transactie te identificeren in het gerelateerde vak van het btw-aangifteformulier.
2. Selecteer de huidige versie en selecteer de zoeknaam op het sneltabblad **Zoekopdrachten**. Bijvoorbeeld **SalesItemTypeLookup**. Deze opzoekbewerking identificeert de lijst met classificaties in het btw-boek voor verkopen die de belastingdienst vereist.
3. Selecteer op het sneltablijst **Voorwaarden** de optie **Toevoegen** en selecteer in de nieuwe regel in de kolom **Opzoekresultaat** de gerelateerde regel die de classificatie in **Kolom O** vertegenwoordigt.
4. Selecteer in de kolom **Btw-groep** de btw-groep die wordt gebruikt om de classificatie te identificeren. Bijvoorbeeld **Binnenlandse verkoopfactuur**. U kunt ook de btw-groep, de btw-code of de combinatie van structuurkenmerken gebruiken als de configuratie op een andere manier is gedefinieerd. 
5. Selecteer in de kolom **Naam** de classificatie van btw-transacties.
6. Herhaal stap 3-5 voor alle beschikbare opzoekbewerkingen.
7. Selecteer **Toevoegen** om de laatste recordregel op te nemen en selecteer in de kolom **Opzoekresultaat** de optie **Niet van toepassing**. 
8. Selecteer **Niet leeg** in de resterende kolommen. 
9. Selecteer **Voltooid** in het veld **Status**.
10. Selecteer **Opslaan** en sluit de pagina **Toepassingsspecifieke parameters**.

> [!NOTE]
> Wanneer u de laatste record, **Niet van toepassing**, toevoegt, definieert u de volgende regel: wanneer de btw-groep, de btw-groep voor artikel, de btw-code en de naam die is doorgegeven als een argument niet aan een van de vorige regels voldoet, worden de transacties niet opgenomen in het btw-boek voor verkopen. Hoewel deze regel niet wordt gebruikt bij het genereren van het rapport, helpt de regel bij het voorkomen van fouten bij het genereren van een rapport wanneer een regelconfiguratie ontbreekt.

De volgende tabellen bevatten een voorbeeld van voorgestelde configuratie voor de beschreven opzoekconfiguraties. 

**SalesItemTypeLookup**

| Zoekresultaat         | Regel | Btw-groep    | Btw-groep voor artikel    | Btw-code (code) | Naam                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Binnenlands              | 1    | VAT_LOCAL          | *Niet leeg*             | *Niet leeg*     | Verkopen                 |
| Binnenlands              | 2    | VAT_LOCAL          | *Niet leeg*             | *Niet leeg*     | SalesCreditNote       |
| Binnenlands              | 3    | VAT_FINALC         | *Niet leeg*             | *Niet leeg*     | Verkopen                 |
| Binnenlands              | 4    | VAT_FINALC         | *Niet leeg*             | *Niet leeg*     | SalesCreditNote       |
| Binnenlands              | 5    | VAT_PUBLIO         | *Niet leeg*             | *Niet leeg*     | Verkopen                 |
| Binnenlands              | 6    | VAT_PUBLIO         | *Niet leeg*             | *Niet leeg*     | SalesCreditNote       |
| Exporteren                | 7    | VAT_EXPORT         | *Niet leeg*             | *Niet leeg*     | Verkopen                 |
| Exporteren                | 8    | VAT_EXPORT         | *Niet leeg*             | *Niet leeg*     | SalesCreditNote       |
| Machine en apparatuur | 9    | *Niet leeg*        | VAT_M&E                 | *Niet leeg*     | Verkopen                 |
| Machine en apparatuur | 10   | *Niet leeg*        | VAT_M&E                 | *Niet leeg*     | SalesCreditNote       |
| Onderdelenapparaten        | 11   | *Niet leeg*        | VAT_PARTS               | *Niet leeg*     | Verkopen                 |
| Onderdelenapparaten        | 12   | *Niet leeg*        | VAT_PARTS               | *Niet leeg*     | SalesCreditNote       |
| Vrijstellingen            | 13   | VAT_EXE            | *Niet leeg*           | *Niet leeg*     | SaleExempt            |
| Vrijstellingen            | 14   | VAT_EXE            | *Niet leeg*           | *Niet leeg*     | SalesExemptCreditNote |
| Niet van toepassing        | 15   | *Leeg*            | *Leeg*                 | VAT_ADJ         | *Niet leeg*           |
| Niet van toepassing        | 16   | *Niet leeg*        | *Niet leeg*             | *Niet leeg*     | *Niet leeg*           |

 **SalesOperationTypeLookup**

| Zoekresultaat  | Regel | Btw-groep voor artikel    | Belastingcode    | Naam                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Goederen          | 1    | VAT_GOODS               | *Niet leeg* | Verkopen                 |
| Goederen          | 2    | VAT_GOODS               | *Niet leeg* | SalesCreditNote       |
| Goederen          | 3    | VAT_GOODS               | *Niet leeg* | SaleExempt            |
| Goederen          | 4    | VAT_GOODS               | *Niet leeg* | SalesExemptCreditNote |
| Services       | 5    | VAT_SERV                | *Niet leeg* | Verkopen                 |
| Services       | 6    | VAT_SERV                | *Niet leeg* | SalesCreditNote       |
| Services       | 7    | VAT_SERV                | *Niet leeg* | SaleExempt            |
| Services       | 8    | VAT_SERV                | *Niet leeg* | SalesExemptCreditNote |
| Correcties    | 9    | *Leeg*                 | VAT_ADJ     | Verkopen                 |
| Correcties    | 10   | *Leeg*                 | VAT_ADJ     | SalesCreditNote       |
| Niet van toepassing | 11   | *Niet leeg*             | *Niet leeg* | *Niet leeg*           |

**PurchaseItemTypeLookup**

| Zoekresultaat          | Regel | Btw-groep voor artikel    | Belastingcode    | Naam                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Goederen                  | 1    | VAT_GOODS               | *Niet leeg* | Inkoop                 |
| Goederen                  | 2    | VAT_GOODS               | *Niet leeg* | PurchaseCreditNote       |
| Services               | 3    | VAT_SERV                | *Niet leeg* | Inkoop                 |
| Services               | 4    | VAT_SERV                | *Niet leeg* | PurchaseCreditNote       |
| Machine en apparatuur  | 5    | VAT_M&E                 | *Niet leeg* | Inkoop                 |
| Machine en apparatuur  | 6    | VAT_M&E                 | *Niet leeg* | PurchaseCreditNote       |
| Onderdelenapparaten         | 7    | VAT_PARTS               | *Niet leeg* | Inkoop                 |
| Onderdelenapparaten         | 8    | VAT_PARTS               | *Niet leeg* | PurchaseCreditNote       |
| Vrijstellingen             | 9    | VAT_EXE                 | *Niet leeg*  | PurchaseExempt           |
| Vrijstellingen             | 10   | VAT_EXE                 | *Niet leeg* | PurchaseExemptCreditNote |
| Niet van toepassing         | 11   | *Niet leeg*             | *Niet leeg* | *Niet leeg*              |

**PurchaseOperationTypeLookup**

| Zoekresultaat  | Regel | Btw-groep  | Belastingcode    | Naam                     |
|----------------|------|------------------|-------------|--------------------------|
| Binnenlands       | 1    | VAT_LOCAL        | *Niet leeg* | Inkoop                 |
| Binnenlands       | 2    | VAT_LOCAL        | *Niet leeg* | PurchaseCreditNote       |
| Binnenlands       | 3    | VAT_LOCAL        | *Niet leeg* | PurchaseExempt           |
| Binnenlands       | 4    | VAT_LOCAL        | *Niet leeg* | PurchaseExemptCreditNote |
| Geïmporteerd       | 5    | VAT_IMPORT       | *Niet leeg* | Inkoop                 |
| Geïmporteerd       | 6    | VAT_IMPORT       | *Niet leeg* | PurchaseCreditNote       |
| Geïmporteerd       | 7    | VAT_IMPORT       | *Niet leeg* | PurchaseExempt           |
| Geïmporteerd       | 8    | VAT_IMPORT       | *Niet leeg* | PurchaseExemptCreditNote |
| Correcties    | 9    | *Leeg*          | VAT_ADJ     | PurchaseCreditNote       |
| Correcties    | 10   | *Leeg*          | VAT_ADJ     | Inkoop                 |
| Niet van toepassing | 11   | *Niet leeg*      | *Niet leeg* | *Niet leeg*              |

**CustomerTypeLookup**

|    Zoekresultaat    | Regel | Btw-groep |
|---------------------|------|-----------------|
| Organisatie        |  1   | VAT_LOCAL       |
| Organisatie        |  2   | VAT_EXPORT      |
| Organisatie        |  3   | VAT_EXE         |
| Uiteindelijke consument      |  4   | VAT_FINALC      |
| Openbare organisatie |  5   | VAT_PUBLIO      |
| Niet van toepassing      |  6   | *Niet leeg*     |

**VATRateTypeLookup**

| Zoekresultaat  | Regel | Btw-code (code) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Niet leeg*     |
| SecondTable    | 4    | *Niet leeg*     |
| Niet van toepassing | 5    | *Niet leeg*     |


## <a name="set-up-general-ledger-parameters"></a>Grootboekparameters instellen

Als u het btw-aangifteformulierrapport wilt genereren in Microsoft Excel-indeling, definieert u een ER-indeling op de pagina **Grootboekparameters**.

1. Ga naar **Belasting** > **Instellen** > **Grootboekparameters**.
2. Selecteer op het tabblad **Btw** in de sectie **Btw-opties** in het veld **Toewijzing indeling btw-overzicht** de optie **Btw-aangifte Excel (EG)**. Als u het veld leeg laat, wordt de standaard btw-aangifte gegenereerd in de SSRS-indeling.
3. Selecteer de **categoriehiërarchie**. Met deze categorie kan de basisproductcode in transacties op het tabblad Buitenlandse handel worden gebruikt, zodat gebruikers goederen en diensten kunnen selecteren en classificeren. De beschrijving van deze classificatie is gedetailleerd in verkoop- en inkooptransactierapporten. Deze configuratie is optioneel.

![Aangifteformulier.](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>Een btw-aangifterapport genereren
Het proces voor het voorbereiden en indienen van een btw-aangifterapport voor een periode is gebaseerd op btw-betalingstransacties die zijn geboekt tijdens de taak Btw vereffenen en boeken. Zie [Btw-overzicht](../general-ledger/indirect-taxes-overview.md) voor meer informatie over het vereffenen en aangeven van btw.

Voltooi de volgende stappen om het belastingaangifterapport te genereren.

1. Ga naar **Belasting** > **Aangiften** > **Btw** > **Btw rapporteren voor vereffeningsperiode** of **Btw vereffenen en boeken**.
2. Selecteer de **vereffeningsperiode**.
3. Selecteer de vanaf-datum en selecteer vervolgens de btw-betalingsversie.
5. Selecteer **OK**. 
6. Voer het creditbedrag van de vorige periode in, indien van toepassing, of laat nul staan als bedrag.
7. Selecteer in het veld **Rapportdetails** een van de volgende beschikbare opties. 
   - **Inkoop-btw-boek**: genereer het detailrapport voor de inkoopbelastingtransacties.
   - **Verkoop-btw-boek**: genereer het detailrapport voor de verkoopbelastingtransacties.
   - **Btw-aangifte**: genereer alleen het formulier voor btw-aangifte.
8. Voer de naam in van de persoon die is geregistreerd om het formulier toe te wijzen.
9. Selecteer de taal. Alle rapporten worden vertaald in **en-us** en **ar-eg**.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


