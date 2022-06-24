---
title: Module voor het opzoeken van orders
description: In dit artikel wordt de module voor het opzoeken van orders beschreven en wordt uitgelegd hoe u de module configureert in Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: c83463d9a0ece9605b0d22bee2a1c76057c8ed05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869425"
---
# <a name="order-lookup-module"></a>Module voor het opzoeken van orders

[!include [banner](includes/banner.md)]

In dit artikel wordt de module voor het opzoeken van orders beschreven en wordt uitgelegd hoe u de module configureert in Microsoft Dynamics 365 Commerce.

De module voor het opzoeken van orders biedt een formulier dat klanten kunnen gebruiken om orders op te zoeken die ze op een e-commercesite hebben geplaatst. Dit formulier wordt gebruikt als onderdeel van de functie [Opzoeken van orders voor gastbetalingen inschakelen](order-lookup-guest.md). De module voor het opzoeken van orders kan worden gebruikt om orders op te zoeken die zijn ingediend via een e-commercesite, het verkooppunt (POS) of een callcenter. Met het formulier kunnen orders worden opgehaald die zijn ingediend door gastgebruikers en door geregistreerde gebruikers.

In de volgende afbeelding ziet u een voorbeeld van het formulier dat wordt weergegeven door de module voor het opzoeken van orders. Wanneer klanten het formulier invullen en **Uw order opzoeken** selecteren, worden ze omgeleid naar de pagina met orderdetails.

![Formulier voor de module voor het opzoeken van orders op een pagina.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Eigenschappen van de module voor het opzoeken van orders

| Naam van eigenschap.     | Waarde     | Beschrijving |
|-------------------|-----------|-------------|
| Koptekst           | Tekst      | De kop die boven aan het formulier wordt weergegeven (bijvoorbeeld 'Uw order zoeken'). |
| RTF         | RTF | Optionele tekst met uitleg die onder de kop wordt weergegeven. |
| Type orderstatus | Vaste tekst      | <p>Selecteer het type gegevens dat via het formulier bij de klant wordt aangevraagd, naast de orderbevestigings-id. Momenteel worden de volgende waarden ondersteund:</p><ul><li><b>E-mail</b>: het formulier bevat een veld waarin klanten het e-mailadres kunnen invoeren dat ze hebben gebruikt bij het plaatsen van de order.</li><li><b>Geen</b>: er wordt in het formulier niet naar informatie gevraagd, behalve naar de orderbevestigings-id.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Een module voor het opzoeken van orders aan een pagina toevoegen

De module voor het opzoeken van orders kan worden toegevoegd aan de hoofdtekst van elke pagina van uw e-commercesite. Als u de module voor het opzoeken van orders wilt gebruiken om het opzoeken van orders voor gastbetalingen in te schakelen, moet u de module toevoegen aan een pagina waarvoor de gebruiker niet hoeft te zijn aangemeld. Als u de instelling **Aanmelden vereist?** van een pagina wilt opzoeken in de structuurweergave van Commerce Site Builder, selecteert u de **Standaardpagina (vereist)** en kijkt u onder in het rechterdeelvenster.

## <a name="additional-resources"></a>Aanvullende bronnen

[Orders opzoeken voor gastbetalingen](order-lookup-guest.md)

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
