---
title: Werken met CSS-overschrijvingsbestanden
description: In dit onderwerp wordt beschreven waarom, wanneer en hoe u CSS-overschrijvingsbestanden (Cascading Style Sheets) gebruikt in Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ef96070fe77b46622667301c7c7c402909ee7dfc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799488"
---
# <a name="work-with-css-override-files"></a>Werken met CSS-overschrijvingsbestanden

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven waarom, wanneer en hoe u CSS-overschrijvingsbestanden (Cascading Style Sheets) gebruikt in Microsoft Dynamics 365 Commerce.

Permanente sitestijlen moeten doorgaans worden afgehandeld via het thema van een site. Thema's bieden de fundamentele CSS- en stijlinstellingen voor de modules op elke pagina van uw site. Thema's worden gemaakt met behulp van de Dynamics 365 Commerce-SDK en ze worden geïmplementeerd op uw websites via Microsoft Dynamics Lifecycle Services (LCS). Met mogelijkheden voor het opsporen van themafouten en module-interfaceconfiguraties in de SDK kunnen site-ontwikkelaar aanpasbare en samenhangende site-ontwerppakketten maken. Wanneer deze ontwerppakketten worden geïmplementeerd op een site, kunnen site-auteurs zich concentreren op het maken, bewerken en publiceren van inhoud in plaats van op siteontwikkeling.

Gezien de gebruikelijke levenscyclus van een thema kan de afhankelijkheid van ontwikkelaars om stijlwijzigingen door te voeren via de SDK en de LCS-implementatiepijplijn in sommige scenario's belemmerend zijn. Prototypen of hotfixes voor de site kunnen omslachtig lijken als de SDK niet is geconfigureerd of als u geen tijd hebt om te wachten op een LCS-implementatie.

In deze scenario's kunnen CSS-overschrijvingsbestanden uitkomst bieden. In de Commerce-ontwerpprogramma's kunnen geverifieerde gebruikers een CSS-bestand uploaden en vervolgens activeren om het thema van een site te negeren. De overhead van SDK- of LCS-implementatie is niet vereist. De overschrijvingen die in een CSS-overschrijvingsbestand zijn opgegeven, kunnen zo klein zijn als één tekststijlwijziging of zo verstrekkend als een volledige merkrevisie zijn.

Houd rekening met de volgende beperkingen voordat u CSS-overschrijvingsbestanden gebruikt:

- Er kan altijd slechts één CSS-overschrijvingsbestand tegelijk actief zijn op een site. Daarom moeten alle actieve overschrijvingen aanwezig zijn in één overschrijvingsbestand.
- Hoewel u de overschrijvingen in de Commerce-ontwerpprogramma's kunt bekijken, zijn er geen speciale foutopsporingsfuncties om fouten te identificeren die door de overschrijvingen worden geïntroduceerd. Met andere woorden, wanneer u CSS-overschrijvingsbestanden gebruikt, hebt u niet dezelfde toolset die de SDK biedt voor module- en ontwerpvalidatie.

Desondanks bieden CSS-overschrijvingsbestanden een snelle manier om een ontwerpprototype te maken of een hotfix te implementeren voordat een volledige thema-update wordt ontwikkeld en geïmplementeerd.

## <a name="create-a-css-override-file"></a>Een CSS-overschrijvingsbestand maken

Als u een CSS-overschrijvingsbestand wilt maken, kunt u een IDE- (Integrated Development Environment), tekst of broncode-editor gebruiken. U kunt standaard foutopsporingsprogramma's in uw browser gebruiken om stijlselecties, eigenschappen en waarden op uw bestaande site te identificeren. In de meeste browsers kunt u waarden wijzigen en deze wijzigingen bekijken in het foutopsporingsprogramma. Nadat u de wijzigingen hebt geïdentificeerd die u wilt aanbrengen, kunt u deze opslaan in uw eigen CSS-bestand.

## <a name="upload-a-css-override-file"></a>Een CSS-overschrijvingsbestand uploaden

Volg deze stappen om een CSS-bestand naar uw site te uploaden in Commerce.

1. Ga in de ontwerpfuncties naar uw site.
1. Selecteer **Ontwerp** in het navigatievenster aan de linkerkant.

    > [!NOTE]
    > Afhankelijk van de versie van de Commerce-ontwerpprogramma's die u gebruikt, moet u mogelijk **Instellingen** in het navigatievenster uitvouwen voordat u **Ontwerp** kunt selecteren.

1. Selecteer boven in het hoofdontwerpvenster het tabblad **CSS-overschrijving** als dit nog niet is geselecteerd.
1. Onder **Beschikbare CSS-overschrijvingen** de optie **CSS-bestand uploaden**. Verkenner wordt geopend.
1. Blader in Verkenner naar en selecteer een CSS-bestand en selecteer vervolgens **Openen**. Het geüploade CSS-bestand wordt nu weergegeven onder **Beschikbare CSS-overschrijvingen**.

## <a name="preview-a-css-override-file"></a>Een CSS-overschrijvingsbestand bekijken

Als u een CSS-overschrijvingsbestand wilt bekijken voordat u het actief maakt op uw live site, volgt u deze stappen.

1. Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand waarvan u een voorbeeld wilt bekijken.
1. Selecteer naast de CSS-bestandsnaam de optie **Site bekijken**.
1. Selecteer in het dialoogvenster **Een URL selecteren** de URL van de site waarvoor u de toegepaste overschrijving wilt bekijken en selecteer vervolgens **OK**.
1. Als er meerdere varianten zijn voor de geselecteerde URL, selecteert u de gewenste variant in het dialoogvenster **Variaties bekijken** dat wordt weergegeven.

Er wordt een nieuw browsertabblad of -venster geopend waarin u uw stijloverschrijvingen voor uw site kunt valideren. U kunt de URL vervolgens delen met andere geverifieerde commerce-gebruikers voor revisie en feedback.

## <a name="activate-a-css-override-file-on-your-live-site"></a>Een CSS-overschrijvingsbestand op uw live site activeren

Nadat u het CSS-overschrijvingsbestand hebt bekeken en goedgekeurd, kunt u het op uw live site activeren.

> [!NOTE]
> Er kan altijd slechts één CSS-overschrijvingsbestand tegelijk actief zijn op uw site. Als u een nieuw overschrijvingsbestand activeert, wordt het vorige overschrijvingsbestand gedeactiveerd. Zorg er daarom voor dat alle vereiste overschrijvingen aanwezig zijn in één CSS-overschrijvingsbestand.

Ga als volgt te werk om een CSS-overschrijvingsbestand te activeren.

1. Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand dat u wilt activeren.
1. Onder de CSS-bestandsnaam selecteert u **Activeren**. Het overschrijvingsbestand wordt onmiddellijk actief op uw live site.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>Een CSS-overschrijvingsbestand op uw live site deactiveren

Ga als volgt te werk om een CSS-overschrijvingsbestand op uw site te deactiveren.

1. Selecteer in het navigatiedeelvenster aan de linkerkant **Ontwerp**. Op het tabblad **CSS-overschrijving** onder **Beschikbare CSS-overschrijvingen** vindt u het CSS-bestand dat u wilt deactiveren.
1. Onder de CSS-bestandsnaam selecteert u **Deactiveren**. Het overschrijvingsbestand wordt onmiddellijk inactief op uw live site.

> [!TIP]
> Voor toegang tot extra opties voor CSS-overschrijvingsbestanden selecteert u het beletselteken (**...**) naast de CSS-bestandsnaam. De opties **Downloaden**, **Naam wijzigen** en **Vervangen** zijn handig voor snelle wijzigingen in een bestaand CSS-overschrijvingsbestand.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een logo toevoegen](add-logo.md)

[Selecteer een thema voor de site](select-site-theme.md)

[Werken met vooraf ingestelde stijlen](style-presets.md)

[Een favicon toevoegen](add-favicon.md)

[Een welkomstbericht toevoegen](add-welcome-message.md)

[Een auteursrechtmelding toevoegen](add-copyright-notice.md)

[Talen toevoegen aan uw site](add-languages-to-site.md)

[Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
