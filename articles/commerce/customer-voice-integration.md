---
title: Customer Voice integreren in e-commercesitepagina's
description: In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Customer Voice in e-commercesitepagina's van Dynamics 365 Commerce integreert.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 272ec1a59ed45b2d2336dcfea16051d27011360f
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767945"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Customer Voice integreren in e-commercesitepagina's

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Customer Voice in e-commercesitepagina's van Dynamics 365 Commerce integreert.

U kunt [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) integreren in uw e-commercesite om realtime feedback van klanten te verzamelen, te analyseren en te volgen. Als u aan de slag wilt met de integratie, moet u een account maken en een Customer Voice-projectsjabloon selecteren voor het type feedback dat u wilt verzamelen.

## <a name="integrate-the-customer-voice-service"></a>De Customer Voice-service integreren

Als u een Customer Voice-account wilt maken, gaat u naar [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) en volgt u de aanwijzingen.

Nadat u een Customer Voice-account hebt gemaakt en u zich hebt aangemeld, moet u een projectsjabloon selecteren voor het type feedback dat u wilt verzamelen.

Volg deze stappen om een Customer Voice-projectsjabloon te selecteren.

1. Ga naar de [pagina voor Customer Voice-projectsjablonen](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Selecteer **Aan de slag**.
1. Selecteer de projectsjabloon in voor het feedbacktype dat u wilt verzamelen en selecteer vervolgens **Volgende**.
1. Selecteer op het tabblad **Verzenden** onder **Een insluitingsindeling kiezen** een insluitingsindeling. In het veld **Ingesloten code** ziet u de code die moet worden ingesloten in Commerce Site Builder.

Voor de voorbeelden in dit onderwerp wordt gebruikgemaakt van de projectsjabloon **Periodiek klantonderzoek** en de insluitingsindeling **Knop**.

In het volgende voorbeeld wordt de projectsjabloonpagina **Periodiek klantonderzoek** weergegeven, waar de optie voor de insluitingsindeling **Knop** is geselecteerd. De insluitingscode voor die optie wordt weergegeven in het veld **Ingesloten code**. Drie afzonderlijke acties zijn vereist om de geleverde code in uw sitepagina's in te voegen, zoals wordt beschreven in de volgende secties.

![De Customer Voice-pagina Periodiek klantonderzoek met de geselecteerde optie Knop.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>De URL van het externe script insluiten

Op alle sitepagina's die een Customer Voice-onderzoek moeten bevatten, moet u de URL van het externe script in de insluitcode van Customer Voice insluiten. U kunt het script het beste op meerdere sitepagina's insluiten door een fragment in Site Builder te maken met de URL van het externe script en vervolgens het fragment aan de betreffende paginasjablonen toe te voegen. Nadat u een bijgewerkte sjabloon hebt gepubliceerd, lijkt de ingesloten externe scriptcode op het volgende voorbeeld op de betreffende sitepagina's.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Zie [Werken met fragmenten](work-with-fragments.md) voor meer informatie over fragmenten.

> [!NOTE]
> U hoeft alleen de URL aan het fragment toe te voegen. De externe scriptmodule voegt de andere scriptcode toe.

Als u de URL van het externe script in een fragment wilt insluiten, gaat u als volgt te werk.

1. Maak in Site Builder een fragment dat is gebaseerd op de [module Extern script](script-module.md).
1. Selecteer **Standaard extern script** in het nieuwe fragment.
1. Voer in het eigenschappenvenster **Standaard extern script** in het veld **Scriptbron** de URL van het externe script in, zoals in de onderstaande voorbeeldafbeelding is weergegeven.

    ![Externe script-URL in het veld Scriptbron voor het nieuwe fragment.](media/customer-voice-integration-2.png)

1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren** om het fragment te publiceren.

Het nieuwe fragment dat het ingesloten externe scriptblok bevat, is nu klaar om te worden toegevoegd aan de juiste paginasjabloon.

### <a name="embed-the-external-style-sheet-code"></a>De code voor externe opmaakmodellen insluiten

Vervolgens moet u op alle sitepagina's die een Customer Voice-onderzoek moeten bevatten de code voor externe opmaakmodellen in de insluitcode van Customer Voice insluiten. Zoals in de vorige sectie kunt u de code voor externe opmaakmodellen het beste op meerdere sitepagina's insluiten door een fragment in Site Builder te maken met de code van het opmaakmodel en vervolgens het fragment aan de betreffende paginasjablonen toe te voegen. De ingesloten code voor externe opmaakmodellen lijkt op de volgende voorbeeldcode.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Als u de code voor externe opmaakmodellen in een fragment wilt insluiten, gaat u als volgt te werk.

1. Maak in Site Builder een fragment dat is gebaseerd op de [module Metatags](metatags-module.md).
1. Selecteer in het fragment het vak **Standaard metatags**.
1. Voer in het eigenschappenvenster **Standaard metatags** in het veld **Metacodes** de code voor externe opmaakmodellen in, zoals in de onderstaande voorbeeldafbeelding is weergegeven.

    ![Code voor externe opmaalmodellen in het veld Metacodes voor het nieuwe fragment.](media/customer-voice-integration-3.png)

1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren** om het fragment te publiceren.

Het nieuwe fragment dat de ingesloten code voor externe opmaakmodellen bevat, is nu klaar om te worden toegevoegd aan de juiste paginasjabloon.

### <a name="embed-the-inline-script-code"></a>De inline scriptcode insluiten 

Vervolgens moet u op alle sitepagina's die een Customer Voice-onderzoek moeten bevatten de inline script in de insluitcode van Customer Voice insluiten. Zoals in de vorige secties kunt u de inline scriptcode het beste op meerdere sitepagina's insluiten door een fragment in Site Builder te maken met de inline scriptcode en vervolgens het fragment aan de betreffende paginasjablonen toe te voegen.

In het volgende voorbeeld van inline scriptcode is **ONDERZOEKS\_SLEUTEL** tijdelijke aanduiding. De waarde **ONDERZOEKS\_SLEUTEL** moet overeenkomen met de werkelijke onderzoekssleutel die Customer Voice via de insluitcode heeft geleverd. De laatste regel roept de code aan om de onderzoeksknop na één seconde weer te geven, om ervoor te zorgen dat de scripts voldoende tijd hebben om te worden geladen. Afhankelijk van het onderzoek dat u hebt geselecteerd, moet u mogelijk ook andere metagegevens toevoegen of bijwerken, zoals de bedrijfsnaam.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Als u de inline scriptcode in een fragment wilt insluiten, gaat u als volgt te werk.

1. Maak in Site Builder een fragment dat is gebaseerd op de [module Inline script](script-module.md).
1. Selecteer **Standaard inline script** in het nieuwe fragment.
1. Voer in het eigenschappenvenster **Standaard inline script** in het veld **Inline script** de inline scriptcode in, zoals in de onderstaande voorbeeldafbeelding is weergegeven.

    ![Inline scriptcode in het veld Inline script voor het nieuwe fragment.](media/customer-voice-integration-4.png)

1. Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.
1. Selecteer **Publiceren** om het fragment te publiceren.

Het nieuwe fragment dat de ingesloten inline scriptcode bevat, is nu klaar om te worden toegevoegd aan de juiste paginasjabloon.

## <a name="add-fragments-to-a-template"></a>Fragmenten aan een sjabloon toevoegen

Wanneer u klaar bent met het maken van de fragmenten die de ingesloten Customer Voice-code bevatten, moet u deze toevoegen aan de paginasjablonen die zijn gekoppeld aan de sitepagina's waar u ze wilt gebruiken. In de onderstaande voorbeeldillustratie zijn de drie voorbeeldfragmenten toegevoegd aan een PDP-sjabloon (pagina met productgegevens).

![Voorbeeldfragmenten die aan een PDP-sjabloon zijn toegevoegd.](media/customer-voice-integration-5.png)

Nadat de bijgewerkte sjabloon is gepubliceerd, wordt het Customer Voice-onderzoek weergegeven op alle pagina's die via de sjabloon worden beheerd.

Zie [Werken met sjablonen](work-with-templates.md) voor meer informatie over sjablonen.

## <a name="configure-content-security-policy"></a>Inhoudsbeveiligingsbeleid configureren

Inhoudsbeveiligingsbeleid staat standaard aanroepen naar andere services niet toe, tenzij er extra configuratie wordt uitgevoerd. Als u de bijgewerkte sjablonen hebt gepubliceerd, is het daarom waarschijnlijk dat het onderzoek niet op de betreffende sitepagina's wordt geladen. Als u de fouten met betrekking tot inhoudsbeveiligingsbeleid wilt weergeven, opent u de tools voor ontwikkelaars in uw webbrowser (F12) en gaat u naar een pagina met het onderzoek. De fouten gerelateerd aan inhoudsbeveiligingsbeleid worden in de uitvoer van de console weergegeven.

Volg deze stappen om inhoudsbeveiligingsbeleid in Site Builder te configureren om de fouten te corrigeren.

1. Ga naar **Vestigingsinstellingen \> Uitbreidingen**.
1. Voeg op het tabblad **Inhoudsbeveiligingsbeleid** `https://customervoice.microsoft.com/` toe aan de instructie **child-src**.
1. Voeg `https://customervoice.microsoft.com/` toe aan de instructie **frame-src**.
1. Voeg `https://mfpembedcdnmsit.azureedge.net` en **.azureedge.net** toe aan de instructie **img-src**.

Zie voor meer informatie [Beveiligingsbeleid voor inhoud](manage-csp.md).

## <a name="additional-resources"></a>Aanvullende bronnen

[Externe scriptmodule](script-module.md)

[Module Metatags](metatags-module.md)

[Inline scriptmodule](script-module.md)

[Inhoudsbeveiligingsbeleid](manage-csp.md)

[Werken met fragmenten](work-with-fragments.md)

[Werken met sjablonen](work-with-templates.md)
