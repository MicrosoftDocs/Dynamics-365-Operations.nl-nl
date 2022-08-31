---
title: Vooraf gedefinieerde productvarianten maken
description: Deze procedure begeleidt u bij het maken van productvarianten voor een productmodel met behulp van de combinaties van productdimensies.
author: t-benebo
ms.date: 08/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a26439b8c7346cdce2b4c9804493fea94c29ac31
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335910"
---
# <a name="predefined-product-variants"></a>Vooraf gedefinieerde productvarianten

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Voorbeeldscenario: Vooraf gedefinieerde productvarianten maken

In dit voorbeeldscenario ziet u hoe u productvarianten maakt voor een productmodel met behulp van combinaties van productdimensies.

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Om dit scenario uit te voeren met de hier gegeven waarden, moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon *USMF* selecteren.

### <a name="step-1-create-a-product-master"></a>Stap 1: Een productmodel maken

U maakt als volgt een productmodel:

1. Ga naar **Productgegevensbeheer > Producten > Productmodellen**.
1. Selecteer **Nieuw**.
1. Als er in het veld **Productnummer** nog geen nummer staat, voert u een waarde in. Deze stap is alleen vereist als er geen nummerreeks voor dit veld is ingesteld.
1. Voer in het vak **Productnaam** een naam in.
1. Selecteer in het veld **Productdimensiegroep** de productdimensiegroep *SizeCol* (Maat en Kleur).
1. Selecteer **OK** om het nieuwe productmodel te maken en te openen.

### <a name="step-2-add-product-dimensions"></a>Stap 2: Productdimensies toevoegen

Dit voorbeeld toont hoe productdimensies handmatig worden ingevoerd. U kunt er ook voor kiezen een grootte, kleur of stijlgroep te selecteren die de productdimensiewaarden bevat die u wilt gebruiken.

U voegt als volgt productdimensies toe:

1. Als uw nieuwe productmodel nog steeds geopend is, selecteert u **Productdimensies** in het actievenster.
1. Open het tabblad **Grootte** en selecteer **Nieuw** op de werkbalk om een rij aan het raster toe te voegen. Voer voor de nieuwe rij de volgende instellingen in:
    - **Grootte**: selecteer een berekeningswaarde.
    - **Naam**: voer een naam in voor de grootte.
1. Selecteer **Nieuw** op de werkbalk en voeg een tweede grootte aan het raster toe met een nieuwe **Grootte** en **Naam**.
1. Open het tabblad **Kleuren** en selecteer **Nieuw** op de werkbalk om een rij aan het raster toe te voegen. Voer voor de nieuwe rij de volgende instellingen in:
    - **Kleur**: selecteer een kleurwaarde.
    - **Naam**: voer een naam in voor de kleur.
1. Selecteer **Nieuw** op de werkbalk en voeg een tweede kleur aan het raster toe met een nieuwe **Kleur** en **Naam**.
1. Selecteer **Opslaan**.
1. Sluit de pagina en ga terug naar uw nieuwe productmodel.

### <a name="step-3-generate-product-variants"></a>Stap 3: Productvarianten genereren

> [!NOTE]
> In deze sectie wordt beschreven hoe u productvarianten genereert wanneer de functie *Verbeteringen voor de pagina Variantsuggesties* niet is ingeschakeld. In het volgende gedeelte leest u meer over het genereren van productvarianten wanneer die functie beschikbaar is.

U genereert als volgt productvarianten:

1. Als uw nieuwe productmodel nog steeds geopend is, selecteert u **Productvarianten** in het actievenster.
1. Selecteer **Variantsuggesties** in het actievenster.
1. Er wordt een lijst gegenereerd met alle mogelijke combinaties van grootten en kleuren die u voor het product hebt gedefinieerd. Selecteer **Alles selecteren** op de werkbalk.
    - In dit voorbeeld selecteert u alle mogelijke varianten. Als u alleen een subset van de mogelijke productdimensiecombinaties wilt gebruiken, schakelt u alleen waar nodig de vereiste selectievakjes in.  
1. Selecteer **Maken**.
1. Selecteer **Opslaan**.

## <a name="improved-variant-suggestions"></a>Verbeterde variantsuggesties

De functie *Verbeteringen voor de pagina Variantsuggesties* verbetert de pagina **Variantsuggesties**, zodat prestatie- en bruikbaarheidsproblemen worden verholpen voor bedrijven die combinaties van productdimensies hebben. Het verbeterde proces voor selectie van de productdimensiewaarden waarvoor variantsuggesties moeten worden gegenereerd, maakt het sneller en eenvoudiger om de relevante set productvarianten te identificeren en vrij te geven.

De functie voegt de volgende verbeteringen toe:

- **Uitgestelde generatie van variantsuggesties**: Op de pagina **Variantsuggesties** worden geen suggesties meer weergegeven wanneer u deze voor het eerst opent. In plaats daarvan moet u expliciet kiezen welke waarden u nodig hebt en vervolgens op de knop **Voorstellen** klikken om de combinaties te genereren. Hierdoor wordt het proces zichtbaarder en interactiever.
- **Selectie van dimensiewaarden**: Wanneer u veel dimensiewaarden hebt, bent u meestal geïnteresseerd in het genereren van variantsuggesties die slechts enkele daarvan bevatten (bijvoorbeeld wanneer u een nieuwe reeks kleuren of stijlen wilt introduceren). Met het verbeterde ontwerp kunt u de dimensiewaarden selecteren waarvoor u productvariantsuggesties wilt genereren. Hierdoor wordt de voorgestelde varianten aanzienlijk relevanter en worden de systeemprestaties en de productiviteit van de gebruiker verbeterd.

### <a name="turn-the-variant-suggestions-page-improvements-feature-on-or-off"></a>De functie Verbeteringen voor de pagina Variantsuggesties in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Verbeteringen voor pagina met variantsuggesties* in de werkruimte [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="work-with-the-improved-variant-suggestions"></a>Werken met de verbeterde variantsuggesties

U genereert als volgt productvarianten wanneer de functie *Verbeteringen voor de pagina Variantsuggesties* is ingeschakeld:

1. Open of maak een productmodel en voeg hieraan de vereiste productdimenssie toe, zoals beschreven in de vorige sectie.
1. Als het productmodel geopend is, selecteert u **Productvarianten** in het actievenster.
1. Selecteer **Variantsuggesties** in het actievenster.
1. Selecteer de waarden die u wilt gebruiken voor elk van de dimensies.
1. Selecteer **Voorstellen** op de bovenste werkbalk.
1. Er wordt een lijst gegenereerd met alle mogelijke combinaties van grootten en kleuren die u hebt geselecteerd. Schakel op het sneltabblad **Voorgestelde varianten** het selectievakje in voor elke productdimensiecombinatie die u wilt gebruiken of selecteer **Alles selecteren** op de werkbalk om ze allemaal te selecteren.  
1. Selecteer **Maken** om de varianten aan het huidige productmodel toe te voegen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
