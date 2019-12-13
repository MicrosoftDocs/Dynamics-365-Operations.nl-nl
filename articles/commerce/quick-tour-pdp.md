---
title: Overzicht van de pagina met productgegevens
description: In dit onderwerp vindt u een overzicht van de pagina's met productgegevens (PDP's) in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697860"
---
# <a name="overview-of-product-details-pages"></a>Overzicht van de pagina met productgegevens

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp vindt u een overzicht van de pagina's met productgegevens (PDP's) in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Een PDP biedt gedetailleerde informatie over een product, en laat klanten productopties selecteren zoals grootte, stijl en kleur. Een PDP moet alle productinformatie presenteren die een klant nodig heeft om een inkoopbeslissing te nemen.

In de volgende afbeelding ziet u een voorbeeld van een PDP.

![Voorbeeld van een pagina met productgegevens](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Koptekst- en voettekstmodules

Een PDP bevat bovenaan een koptekst waarin alle productcategorieën en andere pagina's worden weergegeven waar de detailhandelaar de klanten doorheen wil laten bladeren. Onder aan de pagina staat een voettekst die snelkoppelingen bevat naar verschillende onderwerpen waarin klanten mogelijk geïnteresseerd zijn.

## <a name="buy-box-module"></a>Koopvakmodule

De belangrijkste module op een PDP is de koopvakmodule. Daarom is dit het eerste item in de hoofdsectie van de pagina. Een koopvakmodule is een containermodule die verschillende modules bevat met de belangrijkste informatie over het product. Deze informatie omvat de productnaam, productafbeeldingen, de omschrijving, de prijs en productbeoordelingen.

Met de koopvakmodule kan de klant product opties selecteren (bijvoorbeeld grootte, stijl en kleur) en het product aan de winkelwagen toevoegen. Bovendien kan de klant het product online kopen en in een winkel ophalen. De module Online kopen en ophalen in winkel gebruikt integratie met Bing Maps-API's (Application Programming Interface) om te zoeken naar winkels in de buurt of op een andere locatie die door de klant is opgegeven.

Voor een koopvakmodule is een product-id vereist. Deze id wordt afgeleid van de paginacontext. Als een koopvakmodule wordt toegevoegd aan een pagina waarop de paginacontext geen product-id bevat, wordt de informatie niet correct weergegeven.

## <a name="product-specifications-module"></a>Module Productspecificaties

U kunt de module Productspecificaties gebruiken om extra informatie over het product weer te geven. Deze gegevens worden opgehaald uit productkenmerken in Dynamics 365 Retail. In de module Productspecificaties wordt elk kenmerk weergegeven waarvan de eigenschap **Zichtbaar** is ingesteld op **True**. Hiervoor is een product-id nodig om de productkenmerken op te halen.

## <a name="recommendations-module"></a>Aanbevelingsmodule

De aanbevelingsmodule is een belangrijke module op een PDP. Als klanten zoeken naar producten, moeten er meer productopties worden gepresenteerd, zodat ze het juiste product kunnen vinden en een aankoop kunnen maken. Met aanbevelingen kunnen klanten gemakkelijk verwante inhoud ontdekken en doorgaan met winkelen.

Er zijn verschillende typen aanbevelingslijsten beschikbaar:

- De lijst **Anderen vinden dit ook leuk** is gebaseerd op machine learning. De transactiehistorie van andere klanten wordt gebruikt om aanbevelingen te geven. Deze lijst wordt gegenereerd door de aanbevelingenservice en lijkt op de lijsten 'Klanten die dit hebben gekocht, kochten ook...'. Voor het genereren van deze lijst is een product-id vereist.
- Een lijst **Verwant** kan worden geconfigureerd voor een detailhandelsproduct. Voor bijvoorbeeld een bruine leren reistas kunt u meer tassen voor de lijst configureren die zijn gemaakt van leer of die zijn ontworpen voor reisdoeleinden. Andere typen verwante lijsten, zoals **Accessoires** en **Meer als dit**, kunnen ook worden geconfigureerd. Voor het genereren van deze lijst is een product-id vereist. Daarom is de lijst leeg als deze wordt toegevoegd aan een startpagina als de paginacontext geen product-id bevat.
- Algoritmisch gegenereerde aanbevelingslijsten, zoals **Trending**, **Best verkocht** en **Nieuw**, kunnen worden gebruikt voor PDP's. Hoewel deze lijsten mogelijk niet rechtstreeks verband houden met het product op de PDP, is het ook een manier waarmee klanten producten kunnen vinden die ze interessant vinden. Voor deze typen lijsten is geen product-id vereist. Dit zijn algemene lijsten die worden gegenereerd op basis van winkelpatronen op de site.
- Redactionele lijsten zijn handmatig opgesteld. Een detailhandelaar kan bijvoorbeeld handmatig lijsten maken van producten die hij wil laten opvallen.

## <a name="ratings-and-reviews-module"></a>Beoordelings- en recensiemodule

In de Beoordelings- en recensiemodule worden beoordelingen en recensies van andere klanten weergegeven. Ook kan een klant zijn of haar eigen beoordeling van het product schrijven. Bovendien bevat de module een histogram waarin de trend van de beoordelingen voor het product wordt weergegeven. Zie voor meer informatie [Overzicht beoordelingen en recensies](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Marketingmodules

Als marketinginhoud uniek is voor een specifiek product, kan elke marketingmodule aan de PDP worden toegevoegd. U kunt marketingmodules toevoegen aan een PDP door de pagina te verrijken. 

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van de startpagina](quick-tour-home-page.md)

[Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md)

[Overzicht van pagina's met winkelwagen en kassa](quick-tour-cart-checkout.md)

[Overzicht van pagina's voor accountbeheer](quick-tour-account-management.md)
