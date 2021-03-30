---
title: Aangepaste antwoordpagina's bouwen voor fouten met de statuscode 4xx/5xx
description: In dit onderwerp wordt beschreven hoe u aangepaste antwoordpagina's kunt maken voor de statusfoutcodes 4xx en 5xx met behulp van de ontwerpfuncties in Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee2f74581ded6020d075377f931c465d7c89f9e5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211100"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Aangepaste antwoordpagina's bouwen voor fouten met de statuscode 4xx/5xx


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u aangepaste antwoordpagina's kunt maken voor de statusfoutcodes 4xx en 5xx met behulp van de ontwerpfuncties in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Als een aanvraag misukt, verzendt de server een reactie met een HTTP-statuscode. De 404-statuscode wordt vastgelegd en geretourneerd als een pagina niet wordt gevonden en de 500-statuscode wordt vastgelegd en geretourneerd als er een serverfout optreedt. In Dynamics 365 Commerce kunnen toepassingsgebruikers aangepaste antwoordpagina's met statusfoutcodes maken die worden weergegeven aan gebruikers als reactie voor deze statuscodes.

## <a name="build-a-status-code-error-response-page"></a>Een antwoordpagina maken voor statusfoutcodes

Ga als volgt te werk om een antwoordpagina voor een statusfoutcode te maken.

1. Meld u aan bij Dynamics 365 Commerce in de webbrowser van uw voorkeur. 
1. Selecteer de site waarvoor u een antwoordpagina wilt maken voor fouten met de statuscode 4xx/5xx.

### <a name="build-the-template"></a>De sjabloon samenstellen

Ga als volgt te werk om de sjabloon te maken voor een antwoordpagina voor de statusfoutcode.

1. Ga naar **Sjablonen**.
1. Selecteer **Nieuw** om een paginasjabloon te maken.
1. Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** een naam in voor de nieuwe sjabloon en selecteer **OK**.
1. Bouw de sjabloon op basis van de gewenste structuur voor de antwoordpagina van de statusfoutcode.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren. 

### <a name="build-the-status-code-error-response-page"></a>De antwoordpagina maken voor statusfoutcodes

Ga als volgt te werk om de antwoordpagina voor een statusfoutcode te maken.

1. Ga naar **Pagina's**.
1. Selecteer **Nieuw** om een pagina te maken.
1. Selecteer in het dialoogvenster **Een sjabloon kiezen** een sjabloon en voer vervolgens onder **Paginanaam** een naam in voor de pagina met de statusfoutcode. Laat het veld **Pagina-URL** leeg.
1. Maak de pagina.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

> [!NOTE]
> U kunt afzonderlijke antwoordpagina's maken voor fouten met de statuscodes 4xx en 5xx. U kunt ook dezelfde algemene antwoordpagina met de statusfoutcode gebruiken voor beide foutcategorieën.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Een omleiding instellen voor de antwoordpagina voor de statusfoutcode

Ga als volgt te werk om een omleiding te maken voor een antwoordpagina voor de statusfoutcode.

1. Ga naar **URL's \> Nieuw \> Nieuwe alias** en selecteer de antwoordpagina voor de statusfoutcode die u eerder hebt gemaakt.
1. Voer in het veld **Alias** de waarde **default-4xx** of **default-5xx** in, afhankelijk van de antwoordpagina voor de statusfoutcode waarvoor u een omleiding wilt instellen. Deze aliassen moeten worden gepubliceerd. Anders werkt de omleiding niet.
1. Selecteer **OK** om de koppeling uit te voeren.

> [!NOTE]
> Als u één antwoordpagina voor de statusfoutcode gebruikt voor beide foutcategorieën, herhaalt u deze procedure om een alias voor de andere foutcategorie aan dezelfde pagina te koppelen.

## <a name="additional-resources"></a>Aanvullende resources

[Werken met sjablonen](work-with-templates.md)

[Een nieuwe sitepagina toevoegen](add-new-page.md)

[Een pagina-URL maken](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]