---
title: Een nieuwe sitepagina toevoegen
description: In dit artikel wordt beschreven hoe u een nieuwe sitepagina toevoegt in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f6714463c9d5dc844b03f78f0f6ff60c5f270da3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270313"
---
# <a name="add-a-new-site-page"></a>Een nieuwe sitepagina toevoegen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een nieuwe sitepagina toevoegt in Microsoft Dynamics 365 Commerce.

Nadat u sjablonen en fragmenten voor uw site hebt gemaakt, is de volgende stap het maken van pagina's die deze gebruiken. Om aan de slag te gaan moet u een sjabloon of indeling, een paginanaam en een pagina-URL selecteren.

## <a name="template-or-layout"></a>Sjabloon of indeling

U kunt een sjabloon of een indeling gebruiken voor uw nieuwe pagina. Zie voor meer informatie [Overzicht met sjablonen en indelingen](templates-layouts-overview.md).

## <a name="specify-the-page-name"></a>De paginanaam opgeven

De paginanaam moet uniek voor uw site zijn en een duidelijke omschrijving geven, zodat u deze gemakkelijk kunt terugvinden en andere mensen weten waarvoor de pagina bedoeld is. U kunt de naam van uw pagina later wijzigen door deze te bewerken en vervolgens het pensymbool naast de paginanaam in het eigenschappenvenster te selecteren.

## <a name="specify-the-page-url"></a>De pagina-URL opgeven

U kunt kiezen of u een URL wilt invoeren voor uw nieuwe pagina. Wanneer u een pagina maakt, kunt u een tekenreeks invoeren die wordt gebruikt om een volledige URL te vormen. De tekenreeks staat bekend als relatieve URL of URL-slug genoemd. Vervolgens wordt een volledige URL gegenereerd op basis van de URL-slug en wordt de nieuwe pagina hieraan toegewezen. U kunt de URL-slug later wijzigen voordat u de pagina publiceert. Zie [Een pagina-URL maken](create-page-URL.md) voor meer informatie.

> [!NOTE]
> in Dynamics 365 Commerce worden URL's en inhoud losgekoppeld. Dit betekent dat een pagina kan worden gemaakt die niet is gekoppeld aan een URL en een URL die niet aan een pagina is gekoppeld. Daarom kan de inhoudomwisseling voor een URL worden uitgevoerd zonder dat uitvaltijd nodig is en zijn omleidingen eenvoudiger te beheren.

## <a name="add-a-new-page"></a>Een nieuwe pagina toevoegen

Voer de volgende stappen uit om een nieuwe sitepagina aan uw site toe te voegen.

1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer **Nieuwe pagina**.
1. Selecteer in het dialoogvenster **Nieuwe pagina** een sjabloon en selecteer vervolgens **OK**.
1. Voer in het veld **Paginanaam** een paginanaam in (bijvoorbeeld **Mijn nieuwe pagina**).
1. Voer in het veld **URL** een tekenreeks (de URL-slug) in om de URL te voltooien (bijvoorbeeld **mynewpage**).
1. Selecteer **OK**. De pagina-editor wordt weergegeven. U ziet dat een koptekst en een voettekst automatisch worden toegevoegd aan de pagina op basis van de sjabloon die u hebt geselecteerd.
1. Selecteer in het paginaoverzicht het vak **Hoofd** de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer **Container** en vervolgens **OK**
1. Selecteer in **Vloeibare container** de knop met het weglatingsteken en selecteer **Module toevoegen**.
1. Selecteer **Blok met uitgebreide inhoud** en selecteer vervolgens **OK**.
1. Selecteer **Blok met uitgebreide inhoud**, de knop met het weglatingsteken en vervolgens **Module toevoegen**.
1. Selecteer **Blokitem met uitgebreide inhoud** en selecteer vervolgens **OK**.
1. Selecteer **Alinea** in het deelvenster Eigenschappen aan de rechterkant en voer vervolgens **Mijn testtekst** in het veld in.
1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Voer in het veld **Opmerkingen** **Toegevoegde nieuwe pagina** in en selecteer vervolgens **OK**.
1. Selecteer **Voorbeeld** om uw pagina te bekijken. Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.
1. Selecteer **Publiceren**.
1. Selecteer **Fabrikam** (of de naam van uw site) in het navigatiepad (broodkruimels).
1. Selecteer **URL's** in het navigatievenster aan de linkerkant.
1. Zoek en selecteer uw URL (**mynewpage**) in de lijst.
1. Selecteer **Publiceren**.

## <a name="additional-resources"></a>Aanvullende resources

[Een bestaande sitepagina wijzigen](modify-existing-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Metagegevens SEO beheren](manage-seo-metadata.md)

[Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md)

[Een productpagina verrijken](enrich-product-page.md)

[Een landingspagina voor een categorie verrijken](enrich-category-page.md)

[Toegankelijkheid van pagina-inhoud controleren](verify-accessibility.md)

[Dynamische e-commercepagina's maken op basis van URL-parameters](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
