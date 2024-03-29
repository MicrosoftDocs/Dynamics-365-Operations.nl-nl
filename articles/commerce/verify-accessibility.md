---
title: Toegankelijkheid van pagina-inhoud controleren
description: In dit artikel wordt beschreven hoe u de toegankelijkheid van pagina-inhoud in controleert in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 686ec37f24cf68902c4dd918c0ca8aea7612e1a9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291968"
---
# <a name="verify-page-content-accessibility"></a>Toegankelijkheid van pagina-inhoud controleren

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u de toegankelijkheid van pagina-inhoud in controleert in Microsoft Dynamics 365 Commerce.

Wanneer u klaar bent met het wijzigen van een pagina, moet u ervoor zorgen dat de inhoud toegankelijk is voor iedereen op het web. In de Commerce-ontwerpfunctie kunt u eenvoudig de toegankelijkheid van pagina-inhoud controleren met behulp van de geïntegreerde service [Microsoft Accessibility Insights](https://accessibilityinsights.io/). Met deze service wordt de inhoud van uw pagina geverifieerd aan de hand van de meest recente [W3C-toegankelijkheidsrichtlijnen](https://www.w3.org/standards/webdesign/accessibility) (World Wide Web Consortium).

De integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) moet worden ingeschakeld op tenant- of siteniveau voordat u deze kunt gebruiken.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Microsoft Accessibility Insights inschakelen voor alle sites in uw tenant

Ga als volgt te werk om de integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) voor alle Commerce-sites in uw tenant in te schakelen.

> [!NOTE]
> Als u tenantinstellingen wilt openen, moet u bij Commerce zijn aangemeld als systeembeheerder.

1. Meld u aan bij Commerce als systeembeheerder.
1. Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.
1. Selecteer **Functies** onder **Tenantinstellingen**.
1. Stel de opte **Toegankelijkheidscontrole** in op **Aan**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Microsoft Accessibility Insights voor één site inschakelen

Ga als volgt te werk om de integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) voor één Commerce-site in te schakelen.

1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer in het linkernavigatievenster de optie **Site-instellingen** om deze uit te vouwen.
1. Selecteer **Functies** onder **Site-instellingen**.
1. Stel de opte **Toegankelijkheidscontrole** in op **Aan**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>De toegankelijkheid van de inhoud op de startpagina controleren

Ga als volgt te werk om de geïntegreerde service [Microsoft Accessibility Insights](https://accessibilityinsights.io/) te gebruiken om de inhoud van uw startpagina in Commerce te scannen en te controleren.

1. Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).
1. Selecteer **Pagina's** in het navigatievenster aan de linkerkant.
1. Zoek en selecteer de startpagina om deze te openen in de pagina-editor.
1. Selecteer **Toegankelijkheid controleren** op de opdrachtbalk. De pagina **Toegankelijkheid controleren** wordt weergegeven.
1. Nadat de scan is voltooid, controleert u de inhoud van het rapport.
1. Als er controles zijn mislukt, kunt u elk mislukt controle-item uitvouwen voor meer details.
1. Als u het rapport wilt sluiten nadat u het hebt bekeken, schuift u omlaag op de pagina **Toegankelijkheid controleren** en selecteert u **OK**.

## <a name="additional-resources"></a>Aanvullende resources

[Een bestaande sitepagina wijzigen](modify-existing-page.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Pagina-indelingen selecteren](select-page-layouts.md)

[Metagegevens SEO beheren](manage-seo-metadata.md)

[Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md)

[Een productpagina verrijken](enrich-product-page.md)

[Een landingspagina voor een categorie verrijken](enrich-category-page.md)

[Dynamische e-commercepagina's maken op basis van URL-parameters](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
