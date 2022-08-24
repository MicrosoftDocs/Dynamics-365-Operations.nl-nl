---
title: Factuurbeheer voor B2B-e-commercewebsites
description: In dit artikel worden de factuurbeheermogelijkheden van B2B-e-commercewebsites met Microsoft Dynamics 365 Commerce beschreven.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: c1f3533eb711bf87fe226f5c61678b6939f35e13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274423"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>Factuurbeheer voor B2B-e-commercewebsites

[!include [banner](../../includes/banner.md)]

In dit artikel worden de factuurbeheermogelijkheden van B2B-e-commercewebsites met Microsoft Dynamics 365 Commerce beschreven.

Het is gebruikelijk voor bedrijven die B2B-transacties verwerken om orders op klantkrediet te accepteren en vervolgens een factuur naar klanten te sturen nadat ze de order hebben afgehandeld. Er worden betalingsvoorwaarden gedefinieerd voor klanten en er kunnen enkele kortingen zijn om klanten te motiveren om tijdig of voortijdig te betalen. Om de waarschijnlijkheid te vergroten dat betalingen op tijd worden ontvangen, kunnen klanten op B2B-e-commercewebsites al hun facturen bekijken. De klant kan de facturen eenvoudig filteren om betaalde, onbetaalde of gedeeltelijk betaalde facturen en de vervaldatums weer te geven.

![De factuurpagina op een B2B-website.](../media/ViewInvoices.png)

> [!NOTE]
> Een aangemelde gebruiker kan alleen zijn eigen facturen weergeven en betalen. Als een organisatierekening is geconfigureerd in het vervolgkeuzemenu **Factuurrekening** op het sneltabblad **Factuur en levering** van de klantrecord in Commerce Headquarters, kan de gebruiker facturen voor de organisatierekening weergeven en betalen.

Op de pagina **Facturen** van een B2B-website kan een gebruiker een onbetaalde of gedeeltelijk betaalde factuur selecteren en vervolgens **Factuur betalen** selecteren. De geselecteerde factuur wordt toegevoegd aan de winkelwagen en de gebruiker kan doorgaan met betalen. De gebruiker kan vervolgens beslissen of het volledige factuurbedrag of een gedeeltelijk bedrag moet worden betaald. De gebruiker kan de a conto-betalingswijze gebruiken om voor facturen te betalen.

> [!NOTE]
> Facturen kunnen alleen aan de winkelwagen worden toegevoegd als er momenteel geen artikelen in staan. En artikelen kunnen alleen aan de winkelwagen worden toegevoegd als er momenteel geen facturen in staan. Microsoft is van plan deze beperking te verwijderen in toekomstige Commerce-versies.

![Winkelwagenpagina op een B2B-website.](../media/PayInvoice.png)

Op de pagina **Facturen** kan een gebruiker ook **Factuur aanvragen** naast een factuur selecteren. Op deze manier kan de gebruiker aanvragen dat de details van de factuur worden verzonden naar zijn/haar geregistreerde e-mailadres.

![Het dialoogvenster Factuur aanvragen.](../media/RequestInvoice2.png)

Nadat een gebruiker een factuur heeft aangevraagd, wordt de aanvraag verplaatst naar de sectie **B2B-aanvragen** van de pagina **Mijn rekening**. Nadat de taken **P-0001** en **Orders en kanaalaanvragen synchroniseren** zijn uitgevoerd in Commerce Headquarters, wordt de factuur-e-mail geactiveerd en wordt de status van de B2B-aanvraag als voltooid gemarkeerd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
