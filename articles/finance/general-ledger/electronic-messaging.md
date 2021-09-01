---
title: Elektronische berichten
description: Dit onderwerp biedt overzichts- en instellingsinformatie voor elektronische berichten in Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 191abc37b7c349aaf3c9e871fe2f1885eec9fc896271d6fac27e5caa0b0fe3b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768334"
---
# <a name="electronic-messaging"></a>Elektronische berichten

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt overzichts- en instellingsinformatie voor de functionaliteit voor **elektronische berichten** (EM).

De overheden en wetgevende instanties van verschillende landen en regio's wereldwijd hebben onlang rapportagevereisten geïmplementeerd voor bedrijven die in deze landen of regio's zijn geregistreerd. Het doel van de vereisten is ervoor zorgen dat gegevens in elektronische indeling van die bedrijven worden verkregen, rechtstreeks van de systemen waarin deze zijn berekend, opgeslagen en verwerkt.

De EM-functionaliteit in Microsoft Dynamics 365 Finance ondersteunt diverse processen voor elektronische interactie tussen Finance en de systemen die overheden en wetgevende instanties bieden voor het rapporteren, indienen en ontvangen van officiële informatie.

De EM-functionaliteit is geïntegreerd met de module **Elektronische rapportage** (ER). U kunt ER-indelingen instellen voor elektronische berichten. Zie [Elektronische rapportage](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting) voor meer informatie.

## <a name="basic-concepts-for-em-functionality"></a>Basisconcepten voor EM-functionaliteit

De EM-functionaliteit is gebaseerd op de volgende entiteiten:

- **Elektronisch bericht**: een rapport dat of aangifte die intern moet worden gerapporteerd of verzonden, zoals een rapport dat naar een belastingkantoor wordt verzonden.
- **Items elektronisch bericht**: records die moeten worden opgenomen in het bericht dat wordt gerapporteerd.
- **Elektronische berichtverwerking**: een reeks acties die moeten worden uitgevoerd om de vereiste gegevens te verzamelen, rapporten te genereren, gegevens op te slaan in Azure-blobopslag, rapporten buiten het systeem om te verzenden, antwoorden van buiten het systeem te ontvangen en de database bij te werken, op basis van de ontvangen gegevens. De acties in de keten kunnen gekoppeld of ontkoppeld zijn.

In de volgende afbeelding wordt de gegevensstroom voor EM weergegeven.

![Gegevensstroom voor elektronische berichten.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>Scenario's die worden ondersteund door de EM-functionaliteit

De EM-functionaliteit ondersteunt de volgende scenario's:

- Handmatig berichten maken en rapporten genereren die zijn gebaseerd op bijbehorende ER-exportindelingen van verschillende typen. Deze typen omvatten Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst en Microsoft Word.
- Automatisch berichten maken en verwerken die zijn gebaseerd op informatie die is aangevraagd en ontvangen van een dienst met behulp van een bijbehorende ER-importindeling.
- Gegevens als berichtitems verzamelen en verwerken vanuit een gegevensbron. De gegevensbron voor een Finance-tabel
- Aanvullende informatie opslaan en verschillende waarden evalueren door speciaal gedefinieerde uitvoerbare klassen met betrekking tot berichten en berichtartikelen aan te roepen.
- Gegevens samenvoegen die worden verzameld in de berichtitems, die gegevens naar bericht opsplitsen en rapporten genereren in bijbehorende ER-uitvoerindelingen.
- De rapporten verzenden die naar een webservice zijn gegenereerd op basis van de beveiligingsgegevens die zijn opgeslagen in de Azure Key Vault.
- Antwoord ontvangen van een webservice, het antwoord interpreteren en gegevens bijwerken in Finance.
- Alle gegenereerde rapporten opslaan en controleren.
- Opslaan en controleren van alle logboekgegevens die betrekking hebben op acties die worden uitgevoerd voor een bericht of berichtitem.
- De verwerking door verschillende berichtstatussen en berichtitemstatussen beheren.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Landspecifieke wettelijk voorgeschreven functies die worden ondersteund door de EM-functionaliteit

De volgende tabel bevat informatie over bepaalde landspecifieke wettelijk voorgeschreven functies die worden ondersteund door de EM-functionaliteit.

| Land/regio     | Functienaam | Opname van functiedemo |
|-------------|--------------|------------------------|
| Spanje       | [Directe levering van informatie over btw (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Hongarije     | [Online factureringssysteem](../localizations/emea-hun-online-invoicing.md) | |
| Verenigd Koninkrijk | [Belasting digitaal maken - Wijziging in indiening van btw-aangifte](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: Digitale belasting- en btw-aangifte in het VK in Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litouwen   | [i.SAF-rapportage](../localizations/emea-ltu-isaf.md) | |
| Polen      | [Btw-aangifte met registers (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK btw-auditregisters](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nederland | [Btw-aangifte voor Nederland](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tsjechische Republiek | [Btw-aangifte](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brazilië      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rusland      | [Btw-aangifte](../localizations/rus-vat-declaration.md) | |
| Rusland      | [Boekhoudrapporten in elektronische opmaak](../localizations/rus-accounting-reporting.md) | |
| Rusland      | [Aangifte winstbelasting](../localizations/rus-profit-tax-declaration.md) | |
| Rusland      | [Beoordeelde belastingaangifte](../localizations/rus-assessed-tax-declaration.md) | |
| Rusland      | [Belastingaangifte van import](../localizations/rus-transport-tax-declaration.md) | |
| Rusland      | [Belastingaangifte land](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

