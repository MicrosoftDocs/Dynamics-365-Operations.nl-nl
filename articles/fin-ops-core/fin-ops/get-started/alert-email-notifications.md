---
title: Clientwaarschuwingen per e-mail
description: Dit onderwerp biedt informatie over het instellen van regels die e-mailberichten verzenden wanneer vooraf gedefinieerde gebeurtenissen optreden.
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9fb5b851c71ac632a045cf09c725a088d13f21ad
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360253"
---
# <a name="client-alert-notifications-by-email"></a>Clientwaarschuwingen per e-mail

[!include [banner](../includes/banner.md)]

U kunt aangepaste waarschuwingsregels definiëren die gefilterde weergaven van gegevens controleren en automatisch e-mailberichten verzenden wanneer vooraf gedefinieerde gebeurtenissen plaatsvinden. De optie voor het verzenden van e-mailmeldingen is beschikbaar voor alle ondersteunde typen waarschuwingen en kan ook worden ingeschakeld voor bestaande waarschuwingsregels.

U kunt ingebouwde besturingselementen gebruiken om waarschuwingsregels te maken die de gefilterde weergaven van systeembatchtaken controleren. Door de waarde te controleren van het veld **Status** kunt u ook waarschuwingsregels configureren die e-mail verzenden wanneer een batchtaak mislukt. Nadat deze waarschuwingsregels zijn gemaakt, hoeft u niet langer rapporten te controleren op wijzigingen in zakelijke gegevens. In plaats daarvan kunt u de intelligente wijzigingsdetectieservice deze controle voor u laten uitvoeren.

Clientwaarschuwingen,zijn afhankelijk van het e-mailsubsysteem dat wordt geleverd via integratie met Microsoft Office. We raden aan dat u de SMTP-provider (Simple Mail Transfer Protocol) gebruikt, zodat e-distributie niet hoeft te vertrouwen op een lokale e-mailclient.

Om meldingen te verzenden per e-mail moeten klanten geïntegreerde e-mailservices configureren. E-mailberichten worden verzonden naar ontvangers namens de eigenaren van waarschuwingen.

Zie voor meer informatie over het configureren van e-mail [E-mail configureren en verzenden](../organization-administration/configure-email.md).

In de volgende afbeelding ziet u het dialoogvenster **Waarschuwingsregel maken**, dat nu een optie **E-mail verzenden** bevat.

[![Dialoogvenster Waarschuwingsregel maken met de optie E-mail verzenden ingesteld op Ja.](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Wanneer de optie **E-mail verzenden** is ingesteld op **Ja**, blijven waarschuwingen afgeleverd worden vanuit het actiecentrum.

## <a name="alert-notification-email-templates"></a>Sjablonen voor e-mails met waarschuwingsberichten

De service verzendt e-mailberichten met behulp van vooraf gedefinieerde e-mailsjablonen die de basisgegevens van het waarschuwingsbericht leveren.

De volgende afbeelding toont de structuur van de waarschuwingsmeldingen die per e-mail worden ontvangen.

[![Waarschuwingsberichten op basis van een sjabloon voor maken van records, veldwijzigingen en sjabloonverwijdering.](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]