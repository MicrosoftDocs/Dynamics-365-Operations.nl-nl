---
title: Clientwaarschuwingen per e-mail
description: Dit onderwerp biedt informatie over het instellen van regels die e-mailberichten verzenden wanneer vooraf gedefinieerde gebeurtenissen optreden.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2019
ms.locfileid: "373754"
---
# <a name="client-alert-notifications-by-email"></a>Clientwaarschuwingen per e-mail

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In Microsoft Dynamics 365 for Finance and Operations kunt u aangepaste waarschuwingsregels definiëren die gefilterde weergaven van gegevens controleren en automatisch e-mailberichten verzenden wanneer vooraf gedefinieerde gebeurtenissen plaatsvinden. De optie voor het verzenden van e-mailmeldingen is beschikbaar voor alle ondersteunde typen waarschuwingen en kan ook worden ingeschakeld voor bestaande waarschuwingsregels.

U kunt ingebouwde besturingselementen gebruiken om waarschuwingsregels te maken die de gefilterde weergaven van systeembatchtaken controleren. Door de waarde te controleren van het veld **Status** kunt u ook waarschuwingsregels configureren die e-mail verzenden wanneer een batchtaak mislukt. Nadat deze waarschuwingsregels zijn gemaakt, hoeft u niet langer rapporten te controleren op wijzigingen in zakelijke gegevens. In plaats daarvan kunt u de intelligente wijzigingsdetectieservice van Finance and Operations deze controle voor u laten uitvoeren.

Clientwaarschuwingen,zijn afhankelijk van het e-mailsubsysteem dat wordt geleverd via integratie met Microsoft Office. We raden aan dat u de SMTP-provider (Simple Mail Transfer Protocol) gebruikt, zodat e-distributie niet hoeft te vertrouwen op een lokale e-mailclient.

Om meldingen te verzenden per e-mail moeten klanten geïntegreerde e-mailservices configureren. E-mailberichten worden verzonden naar ontvangers namens de eigenaren van waarschuwingen.

Zie voor meer informatie over het configureren van e-mail in Finance and Operations [E-mail configureren en verzenden](../organization-administration/configure-email.md).

In de volgende afbeelding ziet u het dialoogvenster **Waarschuwingsregel maken**, dat nu een optie **E-mail verzenden** bevat.

[![Dialoogvenster Waarschuwingsregel maken met de optie E-mail verzenden ingesteld op Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Wanneer de optie **E-mail verzenden** is ingesteld op **Ja**, blijven waarschuwingen afgeleverd worden vanuit het actiecentrum.

## <a name="alert-notification-email-templates"></a>Sjablonen voor e-mails met waarschuwingsberichten

De service verzendt e-mailberichten met behulp van vooraf gedefinieerde e-mailsjablonen die de basisgegevens van het waarschuwingsbericht leveren. Deze gegevens omvatten een directe koppeling naar de pagina waar de waarschuwingsregel is gedefinieerd.

De volgende afbeelding toont de structuur van de waarschuwingsberichten die per e-mail worden ontvangen.

[![Waarschuwingsberichten op basis van een sjabloon voor maken van records, veldwijzigingen en sjabloonverwijdering](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
