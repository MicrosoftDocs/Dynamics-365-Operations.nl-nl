---
title: Toegankelijkheid van pagina-inhoud controleren
description: In dit onderwerp wordt beschreven hoe u de toegankelijkheid van pagina-inhoud in controleert in Microsoft Dynamics 365 Commerce.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fc3dca673510e1636f497bb7d5c295bebe025677
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015098"
---
# <a name="verify-page-content-accessibility"></a>Toegankelijkheid van pagina-inhoud controleren


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de toegankelijkheid van pagina-inhoud in controleert in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

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
