---
title: Afmelden voor verzamelen van gebeurtenissen voor webactiviteit
description: In dit onderwerp wordt uitgelegd hoe u bezoekers van uw website in staat kunt stellen om zich af te melden voor het verzamelen van gebeurtenissen voor webactiviteiten in Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25464c89352f44a77a96dee6ad2f633b7a55669e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350275"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Afmelden voor verzamelen van gebeurtenissen voor webactiviteit
[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u klanten in staat kunt stellen zich af te melden voor het verzamelen van gebeurtenissen voor webactiviteiten in Microsoft Dynamics 365 Commerce.

Met Dynamics 365 Commerce kunnen sitebeheerders de webactiviteiten analyseren van gebruikers van hun e-commercesites. Op die manier kunnen ze beter begrijpen hoe hun sites worden gebruikt en kunnen ze de sites optimaliseren voor een verbeterde gebruikerservaring en voor het behalen van zakelijke doelstellingen.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Manieren voor beheerders om een afmeldingsmethode te implementeren

Beheerders hebben drie manieren om een afmeldingsmethode te implementeren.

### <a name="opt-out-on-behalf-of-users"></a>Afmelden namens gebruikers

In Accountbeheer in Commerce Headquarters (HQ) kunnen beheerders de afmelding uitvoeren namens gebruikers.

1. Zoek in de HQ-client op de pagina **Alle klanten** een klant en selecteer deze.
1. Stel op de pagina met klantdetails op het sneltabblad **Retail** in de sectie **Privacy** de optie **Webactiviteit niet bijhouden** in op **Ja**.

    ![Privacyinstellingen.](media/Disablepersonalizationpart2.png)

1. Selecteer **Opslaan** en sluit de pagina.

### <a name="module-based-opt-out-experience"></a>Modulegebaseerde afmelding

Beheerders kunnen geverifieerde gebruikers zichzelf laten afmelden voor het verzamelen van gebeurtenissen voor webactiviteiten. Voeg de afmeldingsmodule voor gebruikers toe aan klantrekeningprofielpagina's om deze methode van afmelding te kunnen bieden.

### <a name="custom-extensions"></a>Aangepaste extensies

Beheerders kunnen hun eigen extensies maken om de afmelding voor gebruikers te beheren. Zie [Retail Server-API's aanroepen](e-commerce-extensibility/call-retail-server-apis.md) en [Uitbreidbaarheid van online afzetkanaal](e-commerce-extensibility/overview.md). voor meer informatie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
