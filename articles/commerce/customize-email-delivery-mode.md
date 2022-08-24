---
title: Transactionele e-mails aanpassen per leveringsmethode
description: In dit artikel wordt beschreven hoe u aangepaste e-mailsjablonen instelt voor specifieke meldingstypen en leveringsmethoden in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 0c0bd218c10a373d142ddcc7780c5339569f7a07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275699"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Transactionele e-mails aanpassen per leveringsmethode

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u aangepaste e-mailsjablonen instelt voor specifieke meldingstypen en leveringsmethoden in Microsoft Dynamics 365 Commerce.

Transactionele e-mails kunnen nu worden aangepast voor een combinatie van een meldingstype (bijvoorbeeld **Bestelling gemaakt**, **Bestelling verpakt** of **Bestelling gefactureerd**) en een leveringsmethode (bijvoorbeeld nacht, afhalen in de winkel of afhalen bij een specifieke locatie). Aangepaste transactionele e-mails zorgen ervoor dat detailhandelaren hun klantenbestellingen kunnen afhandelen op een manier die is afgestemd op de leveringsmethode van de bestelling. De gebeurtenis 'Bestelling verpakt' kan bijvoorbeeld worden aangepast, zodat er instructies volgen voor klanten die afhalen op een specifieke locatie. Ook kunnen er vervoerders- en leveringsgegevens worden geleverd voor klanten die ervoor kiezen hun bestelling te verzenden.

> [!NOTE]
> Als u de functionaliteit voor aangepaste transactionele e-mails wilt gebruiken, moet u eerst de optie **Transactionele e-mailsjablonen aanpassen per leveringsmethode** inschakelen door naar **Werkruimten \> Functiebeheer** in Commerce Headquarters te gaan.

E-mails kunnen worden aangepast op basis van de leveringsmethode voor de volgende meldingstypen:

- **Bestelling geannuleerd** : dit type e-mailmelding is nieuw.
- **Order gemaakt**
- **Order is bevestigd**
- **Bestelling gefactureerd** : dit type e-mailmelding is nieuw. Deze kan worden gebruikt in plaats van de melding **Bestelling verzonden** waarmee een melding wordt verzonden voor elke factuur die een leveringsmethode heeft (niet ophalen, uitvoeren of elektronische leveringsmethode).
- **Bestelling opgezocht**
- **Bestelling verpakt**
- **Bestelling klaar voor ophalen** : dit type melding kan alleen worden aangepast aan de hand van de leveringsmethode als de functie **Ondersteuning voor meerdere ophaalmethodes** is ingeschakeld. In dat geval is dit meldingstype functioneel equivalent aan het meldingstype **Bestelling verpakt**.
- **Betaling is mislukt**
- **Vervangingsorder is gemaakt**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>E-mailsjablonen configureren voor specifieke leveringsmethoden

Voor deze procedure is de veronderstelling dat u uw nieuwe, aangepaste e-mailsjablonen al hebt gemaakt en deze aan de pagina **E-mailsjablonen van organisatie** hebt toegevoegd. Zie [E-mailsjablonen maken voor transactiegebeurtenissen](email-templates-transactions.md) voor informatie over het maken en uploaden van e-mailsjablonen.

Volg de volgende stappen om e-mailsjablonen te configureren voor specifieke leveringsmethoden in Commerce Headquarters.

1. Ga naar **E-mailmeldingsprofiel voor Commerce**.
1. Selecteer onder **Instellingen voor melding detailhandelgebeurtenissen** een bestaand meldingstype.
1. Terwijl het meldingstype nog steeds is geselecteerd, selecteert u **Leveringsmethoden configureren**.
1. In het dialoogvenster **Leveringsmethoden** selecteert u **Nieuw**.
1. Selecteer in de nieuwe rij, in het veld **Leveringsmethode** de leveringsmethode.
1. Selecteer in het veld **e-mail-id** het e-mailsjabloon waaraan u de leveringsmethode wilt toewijzen.
1. Schakel het selectievakje **Actief** in.
1. Herhaal stappen 4 tot en met 7 om meer leveringsmethoden toe te voegen.
1. Wanneer u klaar bent, selecteert u **OK**.

> [!NOTE]
> - Als er meer dan één leveringsmethode aanwezig is in een verkooporder, wordt het standaardsjabloon gebruikt. Het standaardsjabloon is het sjabloon dat is toegewezen aan het meldingstype op de pagina **E-mailmeldingsprofiel voor Commerce**.
> - Als een verkooporder een leveringsmethode heeft die niet is geconfigureerd voor een aangepast e-mailsjabloon, wordt het standaard e-mailsjabloon gebruikt.

## <a name="additional-resources"></a>Aanvullende bronnen

[Callcenterorders maken](tasks/create-call-center-orders.md)

[Leveringsmethode wijzigen in POS](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
