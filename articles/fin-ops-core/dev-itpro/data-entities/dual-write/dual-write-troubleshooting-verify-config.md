---
title: Controleer of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Common Data Service
description: In dit onderwerp wordt uitgelegd hoe u kunt bepalen of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172640"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Controleer of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Common Data Service

[!include [banner](../../includes/banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service. In dit onderwerp wordt specifiek uitgelegd hoe u kunt bepalen of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Common Data Service.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Controleren of Twee keer wegschrijven is geconfigureerd in een Finance and Operations-app

Om te bepalen of de fouten die worden weergegeven wanneer u records voor de update probeert op te slaan, afkomstig zijn van Twee keer wegschrijven, controleert u eerst of Twee keer wegschrijven is geconfigureerd.

+ Als u beheerdersrechten hebt in de Finance and Operations-app, gaat u naar **Werkruimten \> Gegevensbeheer** en selecteert u de tegel voor **Twee keer wegschrijven**. Als de details van de gekoppelde omgevingen en de lijst met actieve entiteitstoewijzingen worden weergegeven, wordt Twee keer wegschrijven geconfigureerd.

    ![De verbinding met de Finance and Operations-app controleren als u beheerdersbevoegdheden hebt](media/verify_fin_ops_1.png)

+ Als u geen beheerdersbevoegdheden hebt, wordt er een foutbericht weergegeven, *Kan geen gegevens schrijven naar entiteit \<naam entiteit\>*. In het voorbeeld in de volgende afbeelding kunt u geen klantrecord in de Finance and Operations-app maken, omdat Twee keer wegschrijven is geconfigureerd, maar de verwijzingsgegevens voor de klantengroep en de betalingsvoorwaarden zijn niet aanwezig in Common Data Service.

    ![De verbinding met de Finance and Operations-app controleren als u beheerdersbevoegdheden hebt](media/verify_fin_ops_2.png)

Voor informatie over het oplossen van problemen wanneer u gegevens maakt in Finance and Operations-apps leest u [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Controleren of Twee keer wegschrijven is geconfigureerd in Common Data Service

Wanneer u gegevens maakt en u het veld **Bedrijf** ziet op pagina's in Common Data Service, is Twee keer wegschrijven geconfigureerd.

![De Common Data Service-verbinding controleren](media/verify_cds.png)

Voor informatie over het oplossen van problemen wanneer u gegevens maakt in Common Data Service leest u [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md).

Voor informatie over het weergeven van foutdetails als u fouten tegenkomt bij het maken van gegevens in Common Data Service, raadpleegt u [Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Common Data Service om foutdetails weer te geven](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
