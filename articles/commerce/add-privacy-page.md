---
title: Een pagina met het privacybeleid toevoegen
description: In dit onderwerp wordt beschreven hoe u een pagina met het privacybeleid toevoegt in Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945995"
---
# <a name="add-a-privacy-policy-page"></a>Een pagina met het privacybeleid toevoegen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een pagina met het privacybeleid toevoegt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Naleving van de privacy omvat organisatorische maatregelen die sitegebruikers informeren over hoe hun gegevens worden verzameld en verwerkt. Gebruikers kunnen vervolgens beslissen hoe ze willen dat hun persoonlijke gegevens worden verwerkt en kunnen passende maatregelen nemen.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>De privacyverklaring van Microsoft in Dynamics 365 Commerce bekijken

Als u de privacyverklaring van Microsoft wilt bekijken terwijl u bent aangemeld bij de Dynamics 365 Commerce-ontwerpfuncties, selecteert u de knop **Help** (**?**) in de rechterbovenhoek en selecteert u vervolgens **Privacy en cookies**. Er wordt een nieuw tabblad geopend met een koppeling naar de [privacyverklaring van Microsoft](https://privacy.microsoft.com/privacystatement).

## <a name="build-a-privacy-policy-page-for-your-site"></a>Een pagina met het privacybeleid maken voor uw site

In Dynamics 365 Commerce zijn er verschillende manieren om gebruikers van uw site toegang te geven tot uw privacybeleid. In deze sectie wordt beschreven hoe u een pagina met het privacybeleid maakt en hier vervolgens naar verwijst met een voettekstfragment.

Middels een voorbeeld wordt hieronder beschreven hoe u een algemene pagina voor het privacybeleid voor een Commerce-site bouwt. U bent verantwoordelijk voor het ontwerpen en implementeren van een oplossing voor een privacybeleidspagina die het beste voldoet aan de wettelijke vereisten van uw bedrijf.

Ga om te beginnen in de ontwerphulpmiddelen naar de site waarvoor u een privacybeleidspagina wilt maken.

### <a name="create-a-template"></a>Een sjabloon maken

> [!NOTE]
> Als er al een sjabloon is gemaakt die kan worden gebruikt voor de privacybeleidspagina, gaat u verder naar de sectie [Een privacybeleidspagina maken](#build-a-privacy-policy-page).

Volg deze stappen om een sjabloon te maken.

1. Ga naar **Sjablonen \> NIeuwe sjabloon**.
1. Voer de sjabloonnaam in en selecteer vervolgens **OK**.
1. Voeg in de sjabloon alle vereiste modules toe aan de vereiste paginavakken. Beweeg de muisaanwijzer over de rode uitroeptekens voor hulp.

    Het vak **HTML-kop** kan bijvoorbeeld een module **Standaard extern script** vereisen.

1. Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.
1. Voeg in de module **Standaardpagina** in het vak **Hoofdonderdeel** een module **Blok met uitgebreide inhoud** toe.
1. Voeg in de module **Blok met uitgebreide inhoud** een module **Blokitem met uitgebreide inhoud** toe.
1. Check de sjabloon in en publiceer deze.

### <a name="build-a-privacy-policy-page"></a>Een privacybeleidspagina maken

Ga als volgt te werk om een privacybeleidspagina te maken.

1. Ga naar **Pagina's \> Nieuwe pagina**.
1. Selecteer de sjabloon voor de privacybeleidspagina.
1. Voer een paginanaam en -URL in en selecteer vervolgens **OK**. 
1. Voeg in het vak **Hoofdonderdeel** van de pagina een module **Blok met uitgebreide inhoud** toe.
1. Voeg in de module **Blok met uitgebreide inhoud** een module **Blokitem met uitgebreide inhoud** toe.
1. Selecteer in het deelvenster voor de module **Blok met uitgebreide inhoud** de optie **Gegevensbron toevoegen** en selecteer vervolgens **Tekst met opmaak**.
1. Voer in de RTF-editor de inhoud voor de privacybeleidspagina in. Vouw de RTF-editor desgewenst uit naar het volledige scherm.
1. Wanneer u klaar bent met het invoeren van inhoud, selecteert u **Voorbeeld** om de pagina in de webbrowser te bekijken.
1. Voltooi alle resterende toevoegingen aan de pagina- en module-eigenschappen.
1. Check de privacybeleidspagina in en publiceer deze.

Volg deze stappen om de URL voor de privacybeleidspagina te publiceren.

1. Ga naar **URL's** en selecteer de URL voor de privacybeleidspagina.
1. Publiceer de geselecteerde URL.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Een koppeling naar de privacybeleidspagina maken in een voettekst

U kunt aan een fragment een koppeling naar de privacybeleidspagina toevoegen. Op deze manier kunt u de koppeling delen en deze bijwerken op meerdere sitepagina's door te verwijzen naar het fragment. Dit voorbeeld laat zien hoe u een koppeling naar de privacybeleidspagina toevoegt aan een voettekstfragment.

Ga als volgt te werk om een koppeling aan een voettekstfragment toe te voegen.

1. Ga naar **Paginafragmenten \> Nieuw paginafragment**.
1. Selecteer de module **Voettekst** en voer een naam in het veld **Naam van paginafragment** in.
1. Voeg in het vak **Voettekstcategorie** een module **Voettekstitem** toe.
1. Selecteer **Koppelingstekst** in het eigenschappenvenster aan de rechterkant.
1. Voer in het dialoogvenster **Koppelingstekst** de koppelingstekst en het koppelingsdoel van de privacybeleidspagina in en klik op **OK**.

    Voor de URL van de privacybeleidspagina gaat u naar **Pagina's**, naar de privacybeleidspagina en kopieert u de URL vanuit het deelvenster Eigenschappen.

1. Sla het fragment op, check het in en publiceer het.
1. Bekijk het fragment en test de koppeling naar de privacybeleidspagina.

Naar het fragment kan nu worden verwezen in de sjabloon voor andere sitepagina's. Wanneer naar dit fragment wordt verwezen in de module **Voettekst** van een sjabloon, wordt de koppelingsverwijzing weergegeven op alle pagina's die zijn gemaakt met behulp van die sjabloon.

## <a name="additional-resources"></a>Aanvullende resources

[Conformiteitsoverzicht](compliance-overview.md)

[Toegankelijkheidsfuncties en -mogelijkheden](accessibility.md)

[Conformiteit van cookie](cookie-compliance.md)
