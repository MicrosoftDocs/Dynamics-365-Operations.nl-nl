---
title: Afschrijving naar rato van verbruik
description: Dit artikel biedt een overzicht van de afschrijvingsmethode Verbruik.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b0bc761160dc7d46519aad13ec2575cb882fc0641830b76952763b54834a64d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747484"
---
# <a name="consumption-depreciation"></a>Afschrijving naar rato van verbruik

[!include [banner](../includes/banner.md)]

Dit artikel biedt een overzicht van de afschrijvingsmethode Verbruik.

Wanneer u een profiel voor de afschrijving van vaste activa instelt en **Verbruik** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, worden vaste activa toegewezen aan het afschrijvingsprofiel op basis van hun gebruik. U hoeft geen percentages en intervallen in te stellen op de pagina **Afschrijvingsprofielen**. Wanneer u een afschrijvingsprofiel maakt dat de methode Verbruik gebruikt, kunt u de methode op verschillende manieren instellen.

## <a name="set-up-and-use-consumption-depreciation"></a>Afschrijving naar rato van verbruik instellen en gebruiken
1.  Maak een afschrijvingsprofiel aan op de pagina **Afschrijvingsprofielen**. Voor verbruikberekeningen moet het afschrijvingsprofiel een ID en een naam hebben, en moet **Verbruik** zijn geselecteerd in het veld **Methode**.
2.  Stel op de pagina **Verbruiksfactoren** de verbruiksfactoren in. Elke verbruiksfactor moet een ID en een naam hebben, en een verbruiksfactor die is opgegeven als een hoeveelheid of een percentage.
3.  Stel op de pagina **Verbruiksfactoren** de verbruikseenheden in. Elke verbruikseenheid moet een ID en een naam hebben. De afschrijvingseenheden worden gebruikt om de afschrijving naar rato van verbruik te berekenen op de pagina **Afschrijving naar rato van verbruik**. Voorbeelden van eenheden zijn kilometer (km), kilogram (kg) en uur.
4.  Configureer op de pagina **Vaste activa** afzonderlijke vaste activa. Selecteer waardemodellen en afschrijvingsboeken met afschrijvingsprofielen voor elk vast activum. U moet waardemodellen of afschrijvingsboeken voor verbruiksafschrijving instellen als u vaste activa met afschrijvingsprofielen hebt die zijn gebaseerd op de methode Verbruik. Deze instellingen wordt uitgevoerd op het tabblad **Afschrijving** van de pagina **Waardemodellen**, of op het sneltabblad **Algemeen** van de pagina **Afschrijvingsprofiel**. U kunt voor meerdere vaste activa hetzelfde waardemodel gebruiken. Afschrijvingsprofielen maken deel uit van het waardemodel of afschrijvingsboek dat u voor de vaste activa selecteert. U kunt afschrijvingsprofielen niet rechtstreeks in het formulier **Vaste activa** toevoegen of wijzigen. Afschrijvingsprofielen kunt u alleen op de pagina **Afschrijvingsboeken** wijzigen.
5.  Voer op de pagina **Waardemodellen** of de pagina **Afschrijvingsboeken** in de veldgroep **Afschrijving naar rato van verbruik** in de hieronder genoemde velden de volgende gegevens in:
    -   Verbruiksfactor
    -   Eenheid
    -   Eenheidsafschrijving
    -   Geraamd verbruik

    Het veld **Geboekt verbruik** bevat de verbruiksafschrijving, in eenheden, die al is geboekt voor de combinatie van het vaste activum en het waardemodel, of voor het afschrijvingsboek. U kunt de waarde in dit veld niet handmatig bijwerken.

## <a name="examples"></a>Voorbeelden
### <a name="example-1"></a>Voorbeeld 1

De volgende verbruiksfactor is ingesteld voor 31 januari:

-   De hoeveelheid is 1000.
-   De eenheidsprijs van de afschrijving die is opgegeven voor het vaste activum is 1,5.

Het afschrijvingsvoorstel op 31 januari luidt als volgt: Hoeveelheid x eenheidsafschrijving 1000 x 1,5 = 1500. Als de factor die is ingesteld voor de vaste activa een percentagefactor is, wordt de geraamde hoeveelheid in het veld **Geraamd verbruik** voor het waardemodel van de vaste activa vermenigvuldigd met het percentage dat is ingesteld voor de geselecteerde einddatum. De uitkomst van de berekening wordt als hoeveelheid voorgesteld als de afschrijvingshoeveelheid voor de periode.

### <a name="example-2"></a>Voorbeeld 2

De volgende factor voor verbruiksafschrijving is ingesteld voor 31 januari:

-   Het percentage is 10 procent.
-   De eenheidsprijs van de afschrijving die is opgegeven voor het vaste activum is 1,5.
-   De geschatte hoeveelheid van de vaste activa is 2.000.

Het afschrijvingsvoorstel op 31 januari luidt als volgt: Geschatte hoeveelheid x percentage x eenheidsafschrijving 2000 x 0,10 x 1,5 = 300





[!INCLUDE[footer-include](../../includes/footer-banner.md)]