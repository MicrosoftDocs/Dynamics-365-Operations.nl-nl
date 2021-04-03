---
title: Bronbelastingaangifte voor Egypte
description: In dit onderwerp wordt uitgelegd hoe u de bronbelastingaangiften voor Egypte configureert en genereert.
author: sndray
manager: AnnBe
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cec903c56439957bcafb77c3da774a903d4433a1
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574320"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Bronbelastingaangifte voor Egypte (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Overzicht
In dit onderwerp wordt uitgelegd hoe u de bronbelastingaangifte en de bronbelastingaangifteformulieren 41 en 11 instelt en genereert voor rechtspersonen in Egypte 

Alle Egyptische entiteiten moeten formulier 41 voorbereiden, waarin alle belastingen worden samengevat die zijn ingehouden van lokale leveranciers en serviceproviders. Behalve formulier 41 moet ook formulier 11 worden gegenereerd voor alle ingehouden belastingen van buitenlandse leveranciers. 

Het rapport **Bronbelastingaangifte** in Dynamics 365 Finance bevat de volgende rapporten:

- Aangifteformuliernr. 41
- Aangifteformuliernr. 11
    
    
## <a name="prerequisites"></a>Vereisten
Het primaire adres van de rechtspersoon moet in Egypte zijn.
In het werkgebied **Functiebeheer** moet de volgende functie zijn ingeschakeld:

   - **Algemene bronbelasting**

Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie over het inschakelen van functies.

1. Ga naar **Belasting** > **Instellen** > **Parameters** > **Grootboekparameters** en stel op het tabblad **Bronbelasting** de optie **Algemene bronbelasting** in op **Ja**.
2. Importeer in het werkgebied **Elektronische rapportage** de volgende indelingen voor elektronische rapportage in vanuit de opslagplaats:

    - Bronbelastingaangifte Excel (EG)

    > [!NOTE]
    > De bovenstaande indeling is gebaseerd op het **belastingaangiftemodel** en maakt gebruik van de **Modeltoewijzing belastingaangifte**. Deze aanvullende configuratie wordt automatisch geïmporteerd.

Zie [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) voor meer informatie over het downloaden van ER-configuraties vanuit Lifecycle Services (LCS).

## <a name="download-electronic-reporting-configurations"></a>Configuraties van elektronische aangifte downloaden

De implementatie van de bronbelastingaangifteformulieren voor Egypte is gebaseerd op ER-configuraties (elektronische rapportage). Zie [Elektronische rapportage](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) voor meer informatie over de capaciteiten en concepten van configureerbare rapportage.

Volg de instructies in het onderwerp [Configuraties voor elektronische rapportage downloaden vanuit Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) voor meer informatie over productie- en gebruikersacceptatietestomgevingen (UAT).

Als u de bronbelastingsaangiften wilt genereren in een Egyptische rechtspersoon, moet u de volgende configuraties uploaden:

- Belastingaangiftemodel.versie.82.xml of hoger
- Belastingaangiftemodeltoewijzing.versie.82.133.xml of hoger
- Bronbelastingaangifte Excel (EG).versie.82.21 of een latere versie

Nadat u het downloaden van de ER-configuraties vanuit Lifecycle Services (LCS) of de algemene opslagplaats hebt voltooid, voert u de volgende stappen uit.

1. Ga naar het werkgebied **Elektronische rapportage** en selecteer de tegel **Rapportconfiguraties**.
1. Selecteer in het actievenster op de pagina **Configuraties** de optie **Uitwisselen > Laden uit XML-bestand**.
1. Upload alle bestanden in de volgorde waarin ze onder de vorige opsommingstekens zijn vermeld. Nadat alle configuraties zijn geüpload, moet de configuratiestructuur aanwezig zijn in Finance.

## <a name="set-up-application-specific-parameters"></a>Toepassingsspecifieke parameters instellen

Met de optie voor toepassingspecifieke parameters kunnen gebruikers bepalen hoe de btw-transacties worden geclassificeerd en berekend in elke regel van een gegenereerd rapport, afhankelijk van de configuratie voor **artikelgroep voor bronbelasting** of andere criteria die zijn vastgelegd in de definitie van opzoekcriteria.

Bronbelastingaangifteformulier 41 bevat een specifieke kolom waarin de bronbelastingtransactie moet worden geclassificeerd in overeenstemming met de classificatie van de belastingdienst met de naam **Kortingscodetype**. In plaats van deze nieuwe classificaties als nieuwe invoergegevens op te nemen wanneer de transacties worden geboekt, worden de classificaties bepaald op basis van de verschillende opzoekacties in **Configuraties** > **Toepassingsspecifieke parameters instellen** > **Instellen** om te voldoen aan de vereisten van bronbelastingrapporten voor Egypte. 

De volgende configuratie wordt gebruikt om de transacties te classificeren in het rapport Bronbelastingaangifteformulier 41:

- **DiscountTaxTypeLookup** -> Kolomnr. 18 

Voer de volgende stappen uit om de verschillende opzoekbewerkingen in te stellen die worden gebruikt om de bronbelastingaangiften en rapporten voor bijbehorende boeken te genereren. 

1. Ga naar het werkgebied **Elektronische rapportage** en selecteer **Configuraties** > **Instellen** om de regels in te stellen om te identificeren hoe transacties worden geclassificeerd in het bronbelastingaangifterapport. 
2. Selecteer de huidige versie en selecteer de zoeknaam op het sneltabblad **Zoekopdrachten**. Bijvoorbeeld **DiscountTaxTypeLookup**. Deze opzoekactie identificeert de lijst met kortingstypen die de belastingdienst vereist.
3. Selecteer op het sneltablijst **Voorwaarden** de optie **Toevoegen** en selecteer in de nieuwe regel in de kolom **Opzoekresultaat** de gerelateerde regel die de classificatie in **Kolom 18** vertegenwoordigt.
4. Selecteer in de kolom **Artikelgroep voor bronbelasting** de gerelateerde code die wordt gebruikt om de classificatie te identificeren. Bijvoorbeeld **Toegestane korting**.  
5. Herhaal stappen 3 en 4 voor alle beschikbare opzoekbewerkingen.
6. Selecteer nogmaals **Toevoegen** om de laatste recordregel op te nemen en selecteer in de kolom **Opzoekresultaat** de optie **Niet van toepassing**. 
7. Selecteer **Niet leeg** in de resterende kolommen. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Grootboekparameters instellen

Als u de bronbelastingaangifteformulierrapporten wilt genereren in Microsoft Excel, definieert u een ER-indeling op de pagina **Grootboekparameters**.

1. Ga naar **Belasting** > **Instellen** > **Grootboekparameters**.
2. Selecteer op het tabblad **Bronbelasting** in het veld **Indelingstoewijzing voor bronbelastingaangifte** de optie **Bronbelastingaangifte Excel (EG)**. Als u het veld leeg laat, wordt de standaard btw-aangifte gegenereerd in de SSRS-indeling.


![Aangifteformulier](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>De formulieren voor bronbelastingaangifte genereren
Het proces van het voorbereiden en indienen van een bronbelastingaangifteformulier voor een specifieke periode is gebaseerd op de bronbelastingtransacties die tijdens de taak voor het vereffenen en boeken van belastingbetalingen zijn geboekt. Zie [Algemene bronbelasting](../general-ledger/global-withholding-tax-overview.md) voor meer informatie over algemene bronbelasting.

Voltooi de volgende stappen om het belastingaangifterapport te genereren.

1. Ga naar **Belasting** > **Aangiften** > **Bronbelasting** > **Betaling van bronbelasting*.
2. Selecteer de vereffeningsperiode en selecteer vervolgens de vanaf-datum voor het rapport. 
3. Voer de transactiedatum in en selecteer vervolgens **OK**.
4. Selecteer een of meer formuliertypen **Formulier 41**, **Formulier 11** of **Geen** in het dialoogvenster dat wordt geopend. Als u **Geen** selecteert, wordt het standaardrapport gegenereerd. 
5. Selecteer de taal. Alle rapporten worden vertaald in **en-us** en **ar-eg**.
6. Voer het filiaal en de naam in van de bank waar de belastingbetaling plaatsvindt.
7. Selecteer het type bedrijf en voer vervolgens de cheque- en documentnummers in. 
8. Voer het entiteitstype in. 
9. Voer de naam in van de persoon die is geregistreerd om het formulier toe te wijzen en selecteer **OK** om het genereren van het rapport te bevestigen. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
